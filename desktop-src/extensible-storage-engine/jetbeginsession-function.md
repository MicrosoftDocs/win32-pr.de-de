---
description: 'Weitere Informationen zu: JetBeginSession-Funktion'
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
ms.openlocfilehash: 3e6263916211e5d21e0032ba6de8d98e46fedfa9
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989073"
---
# <a name="jetbeginsession-function"></a>JetBeginSession-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetbeginsession-function"></a>JetBeginSession-Funktion

Die **JetBeginSession-Funktion** startet eine Sitzung und initialisiert und gibt ein ESE-Sitzungshandle zurück ([JET_SESID](./jet-sesid.md)). Sitzungen steuern den gesamten Zugriff auf die Datenbank und werden zum Steuern des Transaktionsumfangs verwendet. Die Sitzung kann zum Starten, Committen oder Abbrechen von Transaktionen verwendet werden. Die Sitzung wird auch zum Anfügen, Erstellen oder Öffnen einer Datenbank verwendet. Die Sitzung wird als Kontext für alle DDL- und DML-Vorgänge verwendet. Um die Parallelität und den parallelen Zugriff auf die Datenbank zu erhöhen, können mehrere Sitzungen gestartet werden.

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

Zeiger auf die Variable, die das Sitzungshandle bei erfolgreicher Rückgabe initialisiert.

*szUserName*

Dieser Parameter ist reserviert.

*szPassword*

Dieser Parameter ist reserviert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion ermöglicht die Rückgabe aller [JET_ERR,](./jet-err.md)die in dieser API definiert sind. Weitere Informationen zu Jet-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Fehler beim Vorgang, weil kein Arbeitsspeicher zugeordnet werden konnte.</p> | 
| <p>JET_errOutOfSessions</p> | <p>Die Anzahl der Sitzungen, die die Engine dem Client den Start erlaubt, ist begrenzt. Dieser Wert kann mithilfe von <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> mit der JET_paramMaxSessions Konstante geändert werden. Die Standardanzahl von Sitzungen beträgt 16. Ausführliche Informationen zu JET_paramMaxSessions finden Sie unter <a href="gg294139(v=exchg.10).md">Systemparameter.</a></p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird das Sitzungshandle initialisiert und kann für Datenbankvorgänge verwendet werden.

Bei einem Fehler sind keine Sitzungen verfügbar, oder eine neue Sitzung konnte nicht initialisiert werden.

#### <a name="remarks"></a>Bemerkungen

Bei der Verwendung von Sitzungen über verschiedene Threads hinweg muss sorgfältig darauf geachtet werden. Eine Sitzung verfolgt, für welchen Thread sie während [JetBeginTransaction,](./jetbegintransaction-function.md) [JetCommitTransaction](./jetcommittransaction-function.md)oder [JetRollback](./jetrollback-function.md)verwendet wurde, und löst einen Fehler aus, wenn er in mehreren Threads mit einer geöffneten Transaktion verwendet wird. [JetResetSessionContext](./jetresetsessioncontext-function.md)und [JetSetSessionContext](./jetsetsessioncontext-function.md) können dieses Verhalten ändern. Da die Sitzung immer noch ein serialisierter Kontext ist und mehrere Datenbankvorgänge nicht gleichzeitig, sondern nur seriell für eine einzelne Sitzung ausgeführt werden können. Sie können jedoch mehrere Sitzungen verwenden, um gleichzeitigen Datenbankzugriff zu erhalten. Sitzungen können innerhalb einer Transaktion threadübergreifend verwendet werden, indem die Sitzungskontexte festgelegt und zurückgesetzt werden.

Das Sitzungshandle sollte mit [JetEndSession](./jetendsession-function.md)geschlossen werden.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetBeginSessionW</strong> (Unicode) und <strong>JetBeginSessionA</strong> (ANSI).</p> | 



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
