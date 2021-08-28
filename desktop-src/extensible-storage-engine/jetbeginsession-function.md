---
description: Weitere Informationen finden Sie unter JetBeginSession-Funktion.
title: JetBeginSession-Funktion
TOCTitle: JetBeginSession Function
ms:assetid: f1c33b78-f2d1-44ea-8ec9-94b729b94e24
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294131(v=EXCHG.10)
ms:contentKeyID: 32765745
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginSessionA
- JetBeginSession
- JetBeginSessionW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0796d35990a8a53704d64ab8cea6b9503570a124
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479286"
---
# <a name="jetbeginsession-function"></a>JetBeginSession-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetbeginsession-function"></a>JetBeginSession-Funktion

Die **JetBeginSession-Funktion** startet eine Sitzung und initialisiert und gibt ein ESE-Sitzungshand handle ([JET_SESID ) zurück.](./jet-sesid.md) Sitzungen steuern den zugriff auf die Datenbank und werden verwendet, um den Umfang von Transaktionen zu steuern. Die Sitzung kann zum Starten, Commit oder Abbrechen von Transaktionen verwendet werden. Die Sitzung wird auch zum Anfügen, Erstellen oder Öffnen einer Datenbank verwendet. Die Sitzung wird als Kontext für alle DDL- und DML-Vorgänge verwendet. Um die Parallelität und den parallelen Zugriff auf die Datenbank zu erhöhen, können mehrere Sitzungen gestartet werden.

```cpp
    JET_ERR JET_API JetBeginSession(
      __in          JET_INSTANCE instance,
      __out         JET_SESID* psesid,
      __in_opt      JET_PCSTR szUserName,
      __in_opt      JET_PCSTR szPassword
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Die Datenbankinstanz, die für diesen Aufruf verwendet werden soll.

*psesid*

Zeiger auf die Variable, die das Sitzungshand handle bei erfolgreicher Rückgabe initialisiert.

*szUserName*

Dieser Parameter ist reserviert.

*szPassword*

Dieser Parameter ist reserviert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion ermöglicht die Rückgabe aller [JET_ERR,](./jet-err.md)die in dieser API definiert sind. Weitere Informationen zu Jet-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Fehler beim Vorgang, weil der Arbeitsspeicher nicht zugeordnet werden konnte.</p> | 
| <p>JET_errOutOfSessions</p> | <p>Die Anzahl der Sitzungen, die der Client durch die Engine starten kann, ist begrenzt. Dieser Wert kann mithilfe von <a href="gg294044(v=exchg.10).md">JetSetSystemParameter mit der</a> JET_paramMaxSessions geändert werden. Die Standardanzahl der Sitzungen beträgt 16. Unter <a href="gg294139(v=exchg.10).md">Systemparameter</a> finden Sie Details zu JET_paramMaxSessions.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird das Sitzungshand handle initialisiert und kann für Datenbankvorgänge verwendet werden.

Bei einem Fehler sind keine Sitzungen verfügbar, oder eine neue Sitzung konnte nicht initialisiert werden.

#### <a name="remarks"></a>Hinweise

Wenn Sie Sitzungen über verschiedene Threads hinweg verwenden, müssen Sie sorgfältig darauf achten. Eine Sitzung verfolgt, auf welchem Thread sie während [JetBeginTransaction,](./jetbegintransaction-function.md) [JetCommitTransaction](./jetcommittransaction-function.md)oder [JetRollback](./jetrollback-function.md)verwendet wurde, und löst einen Fehler aus, wenn sie in mehreren Threads mit einer geöffneten Transaktion verwendet wird. [JetResetSessionContext](./jetresetsessioncontext-function.md)und [JetSetSessionContext](./jetsetsessioncontext-function.md) können dieses Verhalten ändern. Da die Sitzung immer noch ein serialisierter Kontext ist und mehrere Datenbankvorgänge nicht gleichzeitig für eine einzelne Sitzung ausgeführt werden können, nur seriell. Sie können jedoch mehrere Sitzungen verwenden, um gleichzeitigen Datenbankzugriff zu erzielen. Sitzungen können innerhalb einer Transaktion threadübergreifend verwendet werden, indem die Sitzungskontexte einstellungs- und zurücksetzen werden.

Das Sitzungshand handle sollte mit [JetEndSession geschlossen werden.](./jetendsession-function.md)

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetBeginSessionW</strong> (Unicode) und <strong>JetBeginSessionA</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetDupSession](./jetdupsession-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
