---
description: Weitere Informationen finden Sie unter JetGetCursorInfo-Funktion.
title: JetGetCursorInfo-Funktion
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
ms.openlocfilehash: c0b5d3410ddb7f4210317508739b4f7dd00dd592
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470776"
---
# <a name="jetgetcursorinfo-function"></a>JetGetCursorInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetcursorinfo-function"></a>JetGetCursorInfo-Funktion

Die **JetGetCursorInfo-Funktion** wird verwendet, um basierend auf dem aktuellen Updatestatus des Datensatzes zu bestimmen, ob eine Aktualisierung des aktuellen Datensatzes eines Cursors zu einem Schreibkonflikt führt. Es ist möglich, dass letztendlich ein Schreibkonflikt zurückgegeben wird, auch wenn **JetGetCursorInfo** JET_errSuccess zurückgibt, da eine andere Sitzung den Datensatz aktualisieren kann, bevor die aktuelle Sitzung denselben Datensatz aktualisieren kann.

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

*sesid*

Die Sitzung, die für diesen Aufruf verwendet wird.

*tableid*

Der Cursor, der für diesen Aufruf verwendet wird.

*pvResult*

Für die zukünftige Verwendung reserviert.

*cbMax*

Muss auf 0 (null) festgelegt werden, andernfalls nicht verwendet. Sie ist für zukünftige Funktionen vorhanden.

*InfoLevel*

Muss auf 0 (null) festgelegt werden, andernfalls nicht verwendet. Sie ist für zukünftige Funktionen vorhanden.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Entweder <em>ist cbMax</em> nicht 0 (null) oder <em>InfoLevel</em> ist nicht 0 (null).</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Der Cursor befindet sich derzeit nicht in einem Datensatz, und Informationen zu einem logischen Datensatz können daher nicht zurückgegeben werden.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errWriteConflict</p> | <p>Der aktuelle Datensatz des Cursors wurde von einer anderen Sitzung aktualisiert, und eine Aktualisierung dieses Datensatzes durch diese Sitzung führt zu einem Schreibkonflikt.</p> | 



Bei Erfolg hat dieser Vorgang keine Auswirkungen auf die Position des Cursors, gibt jedoch nur an, dass dieser Datensatz derzeit von keiner anderen Sitzung aktualisiert wurde.

Wenn bei einem Fehler ein negativer Fehlercode zurückgegeben wird, hat dies keine Auswirkungen auf den Cursor oder die Datenbank.

#### <a name="remarks"></a>Hinweise

Dieser Vorgang wirkt sich nicht auf den Zustand des Cursors oder der Daten aus. Es wird nur ein Fehlercode zurückgegeben, der beschreibt, ob eine Aktualisierung des aktuellen Datensatzes durch die aufrufende Sitzung bekanntermaßen zu einer JET_errWriteConflict führt oder unbekannt ist, um JET_errWriteConflict zurückzugeben. Wenn dieser Datensatz bereits von einer anderen Sitzung zur Verwendung aktualisiert wurde, ist es sicher, dass eine Aktualisierung dieses Datensatzes durch diese Sitzung zu einem Schreibkonflikt führt. Dies gilt, bis für diese Sitzung ein Commit oder rollback der Transaktionen auf Die Transaktionsebene 0 (null) ausgeführt wird. Wenn **JetGetCursorInfo** jedoch JET_errSuccess zurückgibt, ist es immer noch möglich, dass eine andere Sitzung diesen Datensatz vor der aktuellen Sitzung aktualisiert. Daher ist es weiterhin möglich, dass eine Aktualisierung des aktuellen Datensatzes durch diese Sitzung in der aktuellen Transaktion zu einem Schreibkonflikt führt.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetLock](./jetgetlock-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
