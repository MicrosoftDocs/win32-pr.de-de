---
description: Weitere Informationen finden Sie unter JetDupSession-Funktion.
title: JetDupSession-Funktion
TOCTitle: JetDupSession Function
ms:assetid: fa8fbaca-fe48-401e-9700-1303f4842ad9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294141(v=EXCHG.10)
ms:contentKeyID: 32765755
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupSession
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c22be08630c446f6c5ba106b38be6bc24415325
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466627"
---
# <a name="jetdupsession-function"></a>JetDupSession-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdupsession-function"></a>JetDupSession-Funktion

Die **JetDupSession-Funktion** startet eine Sitzung und initialisiert und gibt ein ESE-Sitzungshand handle ([JET_SESID ) zurück.](./jet-sesid.md) Sitzungen steuern den zugriff auf die Datenbank und werden verwendet, um den Umfang von Transaktionen zu steuern. Die Sitzung kann zum Starten, Commit oder Abbrechen von Transaktionen verwendet werden. Die Sitzung wird auch zum Anfügen, Erstellen oder Öffnen einer Datenbank verwendet. Die Sitzung wird als Kontext für alle DDL- und DML-Vorgänge verwendet. Um die Parallelität und den parallelen Zugriff auf die Datenbank zu erhöhen, können mehrere Sitzungen gestartet werden.

**Hinweis:** Diese API wird auf alle Arten als [JetBeginSession-Instanz](./jetbeginsession-function.md) verwendet, die für die instanz der übergebenen Sitzung aufgerufen wird. Diese Funktion wird nicht empfohlen. [JetBeginSession](./jetbeginsession-function.md) wird bevorzugt.

```cpp
    JET_ERR JET_API JetDupSession(
      __in          JET_SESID sesid,
      __out         JET_SESID* psesid
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die als Quelle für das Duplizieren oder Starten der Sitzung verwendet werden soll.

*psesid*

Ein Zeiger auf die Variable, die das Sitzungshand handle bei erfolgreicher Rückgabe initialisiert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Fehler beim Vorgang, weil der Arbeitsspeicher nicht zugeordnet werden konnte.</p> | 
| <p>JET_errOutOfSessions</p> | <p>Die Anzahl der Sitzungen, die der Client durch die Engine starten kann, ist begrenzt. Dieser Wert kann mithilfe von <a href="gg294044(v=exchg.10).md">JetSetSystemParameter mit der</a> <em>JET_paramMaxSessions</em> geändert werden. Die Standardanzahl der Sitzungen beträgt 16. Unter <a href="gg294139(v=exchg.10).md">Systemparameter</a> finden Sie Details zu <em>JET_paramMaxSessions</em>.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird das Sitzungshand handle initialisiert und kann für Datenbankvorgänge verwendet werden.

Bei einem Fehler sind keine Sitzungen verfügbar, oder eine neue Sitzung konnte nicht initialisiert werden.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_SESID](./jet-sesid.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
