---
description: Weitere Informationen finden Sie unter JetBeginTransaction3-Funktion.
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
ms.openlocfilehash: ed7c963da40f72fb7ea54c5614836a1de81a0b3d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479236"
---
# <a name="jetbegintransaction3-function"></a>JetBeginTransaction3-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetBeginTransaction3-Funktion** bewirkt, dass eine Sitzung eine Transaktion einträgt und einen neuen Speicherpunkt erstellt. Diese Funktion kann in einer einzelnen Sitzung mehr als einmal aufgerufen werden, um zusätzliche Speicherpunkte zu erstellen. Diese Speicherpunkte können verwendet werden, um Änderungen an der Datenbank selektiv zu speichern oder zu verwerfen.

Die **JetBeginTransaction3-Funktion** wurde im Windows 8 eingeführt.

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
| <p>JET_bitTransactionReadOnly</p> | <p>Die Datenbank wird von der Transaktion nicht geändert. Wenn ein Update versucht wird, wird dieser Vorgang mit JET_errTransReadOnly nicht durchgeführt. Diese Option wird ignoriert, es sei denn, sie wird angefordert, wenn sich die gegebene Sitzung nicht bereits in einer Transaktion befindet. Diese Option ist in Versionen des Betriebssystems Windows ab xp Windows verfügbar.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR-Datentyp](./jet-err.md) mit einem der in der folgenden Tabelle aufgeführten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs der <a href="gg269240(v=exchg.10).md">JetStopService-Funktion beendet</a> wurden.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Rückgabecode wird von Versionen von zurückgegeben, die Windows XP Windows werden.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden. Dieser Fehler wird von Versionen von zurückgegeben, die Windows xp Windows xp.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errTransTooDeep</p> | <p>Eine neue Transaktion kann nicht gestartet werden, da die Sitzung bereits die maximale Speicherpunkttiefe hat, die von der Datenbank-Engine zulässig ist.</p> | 



Bei Erfolg befindet sich die bereitgestellte Sitzung innerhalb einer Transaktion. Wenn sich die Sitzung zuvor innerhalb einer Transaktion befindet, wird ein neuer Speicherpunkt erstellt.

Bei einem Fehler bleibt der Transaktionszustand der Sitzung unverändert. Es erfolgt keine Änderung des Datenbankstatus.

#### <a name="remarks"></a>Hinweise

Weitere Informationen zur Funktionsweise von Transaktionen finden Sie unter [JetBeginTransaction](./jetbegintransaction-function.md).

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows 8.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2012.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

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
