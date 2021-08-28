---
description: Weitere Informationen finden Sie unter JetGetBookmark-Funktion.
title: JetGetBookmark-Funktion
TOCTitle: JetGetBookmark Function
ms:assetid: 35bb481d-44a0-45d5-97e0-f36cbcc6aaab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269221(v=EXCHG.10)
ms:contentKeyID: 32765524
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7806770d528d83f18d6f3eb061dc3043e15a0e53
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984843"
---
# <a name="jetgetbookmark-function"></a>JetGetBookmark-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetbookmark-function"></a>JetGetBookmark-Funktion

Die **JetGetBookmark-Funktion** ruft das Lesezeichen für den Datensatz ab, der dem Indexeintrag an der aktuellen Position eines Cursors zugeordnet ist. Dieses Lesezeichen kann dann verwendet werden, um den Cursor mit [JetGoToBookmark](./jetgotobookmark-function.md)wieder auf denselben Datensatz zu positionieren.

```cpp
    JET_ERR JET_API JetGetBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*pvBookmark*

Der Ausgabepuffer, der das Lesezeichen empfängt.

*cbMax*

Die maximale Größe des Ausgabepuffers in Bytes.

*–actual*

Die tatsächliche Größe des Lesezeichens in Bytes.

Wenn dieser Parameter **NULL ist,** wird die tatsächliche Größe des Lesezeichens nicht zurückgegeben.

Wenn der Ausgabepuffer zu klein ist, wird weiterhin die tatsächliche Größe des Lesezeichens zurückgegeben. Das bedeutet, dass diese Zahl größer als die Größe des Ausgabepuffers ist.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen, aber der Ausgabepuffer war zu klein, um das gesamte Lesezeichen zu empfangen. Der Ausgabepuffer wurde mit so viel Lesezeichen gefüllt, wie es passen würde. Die tatsächliche Größe des Lesezeichens wurde auch zurückgegeben, wenn dies angefordert wird.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die -Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong> Diese Rückgabewerte werden in xp Windows eingeführt.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Der Cursor ist nicht auf einem Datensatz positioniert. Dafür sind viele verschiedene Gründe möglich. Dies geschieht beispielsweise, wenn der Cursor nach dem letzten Datensatz im aktuellen Index positioniert ist.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die -Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden.</p><p><strong>Windows XP:</strong> Dieser Rückgabewert wird in xp Windows eingeführt.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die -Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p> | 



Wenn diese Funktion erfolgreich ist, wird das Lesezeichen für den Datensatz, der dem Indexeintrag an der aktuellen Position eines Cursors zugeordnet ist, im Ausgabepuffer zurückgegeben. Es erfolgt keine Änderung des Datenbankstatus.

Wenn diese Funktion fehlschlägt, sind der Status des Ausgabepuffers und die tatsächliche Größe des Lesezeichens nicht definiert, es sei denn, JET_errBufferTooSmall zurückgegeben wurde. Für den Fall, JET_errBufferTooSmall zurückgegeben wird, enthält der Ausgabepuffer so viel Lesezeichen, wie in den bereitgestellten Platz passen, und die tatsächliche Größe des Lesezeichens ist genau. Es erfolgt keine Änderung des Datenbankstatus.

#### <a name="remarks"></a>Bemerkungen

Lesezeichen sollten in der Regel als nicht transparente Datenbrocken behandelt werden. Es sollte nicht versucht werden, die interne Struktur dieser Daten auszunutzen. Die folgenden Bedingungen gelten jedoch für alle ESENT-Lesezeichen:

  - Ein Lesezeichen identifiziert einen Datensatz in einer bestimmten Tabelle eindeutig.

  - Das Lesezeichen eines Datensatzes ändert sich während der Lebensdauer dieses Datensatzes nicht.

  - Das Lesezeichen eines Datensatzes ist mit dem Schlüssel dieses Datensatzes auf dem primären Index für die Tabelle identisch, die diesen Datensatz enthält. Wenn kein primärer Index für diese Tabelle definiert ist, erstellt die Datenbank-Engine ein eigenes Lesezeichen für den Datensatz.

  - Lesezeichen können mithilfe der [memcmp-Funktion](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) miteinander verglichen werden, um ihre relative Reihenfolge im primären Index für die Tabelle der Quelldatensätze zu erstellen. Wenn kein primärer Index für diese Tabelle definiert ist, ist es nicht sinnvoll, die relative Reihenfolge der Lesezeichen aus dieser Tabelle zu verwenden.

  - Es ist bedeutungslos, Lesezeichen von Datensätzen aus verschiedenen Tabellen miteinander zu vergleichen.

  - Ein Lesezeichen ist vor der Verwendung von Vista immer kleiner oder Windows gleich JET_cbBookmarkMost (256) Bytes.
    
**Windows Vista:** In Windows Vista und höheren Versionen können Lesezeichen größer als JET_cbBookmarkMost (256) Bytes sein. Die maximale Größe eines Lesezeichens entspricht dem aktuellen Wert von JET_paramKeyMost + 1.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGoToBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
