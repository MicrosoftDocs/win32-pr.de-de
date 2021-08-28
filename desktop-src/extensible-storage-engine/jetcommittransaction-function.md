---
description: 'Weitere Informationen zu: JetCommitTransaction-Funktion'
title: JetCommitTransaction-Funktion
TOCTitle: JetCommitTransaction Function
ms:assetid: 140ca76a-b3a7-4ae8-bc7e-73941fbfc759
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269191(v=EXCHG.10)
ms:contentKeyID: 32765494
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCommitTransaction
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b19e193fa0dc911112d0bd8ed8e672de6fc57a2b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983533"
---
# <a name="jetcommittransaction-function"></a>JetCommitTransaction-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcommittransaction-function"></a>JetCommitTransaction-Funktion

Die **JetCommitTransaction-Funktion** committet die Änderungen, die während des aktuellen Speicherpunkts am Zustand der Datenbank vorgenommen wurden, und migriert sie zum vorherigen Sicherungspunkt. Wenn für den äußersten Sicherungspunkt ein Commit ausgeführt wird, werden die während dieses Speicherpunkts vorgenommenen Änderungen in den Zustand der Datenbank übernommen, und die Sitzung beendet die Transaktion.

```cpp
    JET_ERR JET_API JetCommitTransaction(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angibt.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitCommitLazyFlush</p> | <p>Für die Transaktion wird normal ein Commit ausgeführt, aber diese API wartet nicht, bis die Transaktion in die Transaktionsprotokolldatei geleert wird, bevor sie an den Aufrufer zurückgegeben wird. Dadurch wird die Dauer eines Commitvorgangs auf Kosten der Dauerhaftigkeit drastisch reduziert. Jede Transaktion, die vor einem Absturz nicht in das Protokoll geleert wird, wird während der Absturzwiederherstellung beim nächsten Aufruf von <a href="gg294068(v=exchg.10).md">JetInit</a>automatisch abgebrochen.</p><p>Wenn JET_bitWaitLastLevel0Commit oder JET_bitWaitAllLevel0Commit angegeben sind, wird diese Option ignoriert.</p><p>Wenn dieser Aufruf von <strong>JetCommitTransaction</strong> nicht mit dem ersten Aufruf von <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> für diese Sitzung übereinstimmt, wird diese Option ignoriert. Dies liegt daran, dass die letzte Aktion, die am äußersten Sicherungspunkt ausgeführt wird, der bestimmende Faktor ist, ob für die gesamte Transaktion tatsächlich ein Commit auf den Datenträger ausgeführt wird.</p> | 
| <p>JET_bitWaitAllLevel0Commit</p> | <p>Alle Transaktionen, für die zuvor von einer Sitzung ein Commit ausgeführt wurde, die noch nicht in die Transaktionsprotokolldatei geleert wurden, werden sofort geleert. Diese API wartet, bis die Transaktionen geleert wurden, bevor sie an den Aufrufer zurückgegeben wird.</p><p>Diese Option kann auch dann verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet.</p><p>Diese Option kann nicht in Kombination mit einer anderen Option verwendet werden.</p><p>Diese Option ist nur ab Windows Server 2003 verfügbar.</p> | 
| <p>JET_bitWaitLastLevel0Commit</p> | <p>Wenn für die Sitzung zuvor ein Commit für Transaktionen ausgeführt wurde und sie noch nicht in die Transaktionsprotokolldatei geleert wurden, sollten sie sofort geleert werden. Diese API wartet, bis die Transaktionen geleert wurden, bevor sie an den Aufrufer zurückgegeben wird. Dies ist nützlich, wenn die Anwendung zuvor mithilfe von JET_bitCommitLazyFlush mehrere Transaktionen ausgeführt hat und nun alle Transaktionen auf den Datenträger leeren möchte.</p><p>Diese Option kann auch dann verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet.</p><p>Diese Option kann nicht in Kombination mit einer anderen Option verwendet werden.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Eine der angeforderten Optionen war ungültig oder nicht implementiert. Dieser Fehler wird von <strong>JetCommitTransaction</strong> zurückgegeben, wenn:</p><ul><li><p>Ein ungültiges <em>Grbit</em> wird angegeben.</p></li><li><p>JET_bitWaitLastLevel0Commit wurde in Kombination mit einem anderen <em>grbit</em>angegeben.</p></li><li><p>JET_bitWaitAllLevel0Commit wurde in Kombination mit einem anderen <em>grbit</em>angegeben.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errNotInTransaction</p> | <p>Fehler beim Vorgang, weil sich die angegebene Sitzung nicht in einer Transaktion befindet.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden.</p><p>Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird für alle Änderungen, die während des aktuellen Speicherpunkts für die angegebene Sitzung an der Datenbank vorgenommen wurden, ein Commit ausgeführt, und dieser Sicherungspunkt wird beendet. Wenn der letzte Sicherungspunkt für die Sitzung beendet wurde, wird die Transaktion optional in die Transaktionsprotokolldatei geleert, und die Sitzung beendet die Transaktion.

Bei einem Fehler bleibt der Transaktionsstatus der Sitzung unverändert. Es wird keine Änderung am Datenbankzustand vorgenommen. Die Anwendung sollte [JetRollback](./jetrollback-function.md) aufrufen, um die Transaktion abzubricht.

#### <a name="remarks"></a>Bemerkungen

Es muss ein Aufruf von **JetCommitTransaction** oder [JetRollback](./jetrollback-function.md) vorhanden sein, damit jeder Aufruf von [JetBeginTransaction](./jetbegintransaction-function.md) für eine bestimmte Sitzung übereinstimmt.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction]()  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)
