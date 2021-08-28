---
description: 'Weitere Informationen zu: JetBeginTransaction3-Funktion'
title: JetBeginTransaction3-Funktion
TOCTitle: JetBeginTransaction3 Function
ms:assetid: 7f8ed059-0b97-46fa-9925-e46cdcbee6ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835043(v=EXCHG.10)
ms:contentKeyID: 49894665
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetBeginTransaction3
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ca07ad3957efadfb86ac5df9b1994d5c4525c7a2
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989043"
---
# <a name="jetbegintransaction3-function"></a>JetBeginTransaction3-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetBeginTransaction3-Funktion** bewirkt, dass eine Sitzung eine Transaktion eingibt und einen neuen Speicherpunkt erstellt. Diese Funktion kann in einer einzelnen Sitzung mehr als einmal aufgerufen werden, um zusätzliche Speicherpunkte zu erstellen. Diese Sicherungspunkte können selektiv verwendet werden, um Änderungen an der Datenbank beizubehalten oder zu verwerfen.

Die **JetBeginTransaction3-Funktion** wurde im Windows 8 Betriebssystem eingeführt.

``` c++
JET_ERR JET_API JetBeginTransaction3(
  __in          JET_SESID sesid,
  __in          int64 trxid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*trxid*

Ein optionaler Bezeichner, der vom Benutzer bereitgestellt wird, um die Transaktion zu identifizieren.

*grbit*

Eine Gruppe von Bits, die null oder mehr der in der folgenden Tabelle aufgeführten Aufrufoptionswerte angibt.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitTransactionReadOnly</p> | <p>Die Transaktion ändert die Datenbank nicht. Wenn ein Update versucht wird, schlägt dieser Vorgang mit JET_errTransReadOnly Antwortcode fehl. Diese Option wird ignoriert, es sei denn, sie wird angefordert, wenn sich die angegebene Sitzung nicht bereits in einer Transaktion befindet. Diese Option ist in Versionen des Windows Betriebssystems ab Windows XP verfügbar.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der in der folgenden Tabelle aufgeführten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs der <a href="gg269240(v=exchg.10).md">JetStopService-Funktion</a> ausgeführt wurden.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Rückgabecode wird von Versionen von Windows zurückgegeben, die mit Windows XP beginnen.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden. Dieser Fehler wird von Versionen von Windows zurückgegeben, die mit Windows XP beginnen.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errTransTooDeep</p> | <p>Eine neue Transaktion kann nicht gestartet werden, da die Sitzung bereits die maximale Speicherpunkttiefe erreicht, die von der Datenbank-Engine zugelassen wird.</p> | 



Bei Erfolg befindet sich die bereitgestellte Sitzung innerhalb einer Transaktion. Wenn sich die Sitzung zuvor innerhalb einer Transaktion befand, wird ein neuer Speicherpunkt erstellt.

Bei einem Fehler bleibt der Transaktionsstatus der Sitzung unverändert. Es wird keine Änderung am Datenbankzustand vorgenommen.

#### <a name="remarks"></a>Bemerkungen

Weitere Informationen zur Funktionsweise von Transaktionen finden Sie unter [JetBeginTransaction](./jetbegintransaction-function.md).

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
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
