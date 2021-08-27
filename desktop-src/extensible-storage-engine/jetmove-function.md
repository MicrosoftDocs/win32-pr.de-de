---
description: Weitere Informationen finden Sie unter JetMove-Funktion.
title: JetMove-Funktion
TOCTitle: JetMove Function
ms:assetid: ded3cd21-8586-4d90-9efc-61213132d201
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294117(v=EXCHG.10)
ms:contentKeyID: 32765731
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMove
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a0d00578f4f66af0b0cef76cef7193d0174e253a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983393"
---
# <a name="jetmove-function"></a>JetMove-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetmove-function"></a>JetMove-Funktion

Die **JetMove-Funktion** positioniert einen Cursor am Anfang oder Ende eines Indexes und durchläuft die Einträge in diesem Index entweder vorwärts oder rückwärts. Es ist auch möglich, den Cursor um eine angegebene Anzahl von Indexeinträgen auf dem aktuellen Index vorwärts oder rückwärts zu bewegen. Ein anderer Ansatz besteht in der künstlichen Einschränkung der Indexeinträge, die mit **JetMove** aufzählt werden können, indem ein Indexbereich für den Cursor mit [JetSetIndexRange eingerichtet wird.](./jetsetindexrange-function.md)

```cpp
    JET_ERR JET_API JetMove(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          long cRow,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*Krähe*

Ein beliebiger Offset, der die gewünschte Bewegung des Cursors auf dem aktuellen Index angibt.

Zusätzlich zu Standardoffsets kann dieser Parameter auch mit einer der folgenden Optionen festgelegt werden.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_MoveFirst</p> | <p>Verschiebt den Cursor zum ersten Indexeintrag im Index (sofern vorhanden).</p><p><strong>Hinweis:</strong>   Der Literalwert von -2147483648 wird verwendet, um diese Option zu bezeichnen. Verwenden Sie diesen Wert nicht als normalen Offset oder unbeabsichtigtes Verhalten.</p> | 
| <p>JET_MoveLast</p> | <p>Verschiebt den Cursor zum letzten Indexeintrag im Index (sofern vorhanden).</p><p><strong>Hinweis:</strong>   Der Literalwert von 2147483647 wird verwendet, um diese Option zu bezeichnen. Verwenden Sie diesen Wert nicht als normalen Offset oder unbeabsichtigtes Verhalten.</p> | 
| <p>JET_MoveNext</p> | <p>Verschiebt den Cursor zum nächsten Indexeintrag im Index (sofern vorhanden). Dieser Wert entspricht genau einem normalen Offset von +1.</p> | 
| <p>JET_MovePrevious</p> | <p>Verschiebt den Cursor zum vorherigen Indexeintrag im Index (sofern vorhanden).</p><p>Dieser Wert ist genau gleich einem normalen Offset von -1 oder 0 (Null).</p><p>Der Cursor verbleibt an der aktuellen logischen Position, und das Vorhandensein des Indexeintrags, der dieser logischen Position entspricht, wird getestet.</p> | 



*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angeben.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitMoveKeyNE</p> | <p>Verschiebt den Cursor um die Anzahl der Indexeinträge, die erforderlich sind, um die angeforderte Anzahl von Indexschlüsselwerten im Index zu überspringen. Dies hat den Effekt, dass Indexeinträge mit doppelten Schlüsselwerten in einen einzelnen Indexeintrag eingeklappt werden. Normalerweise bewegt ein Offset den Cursor um die angegebene Anzahl von Indexeinträgen, unabhängig von ihren Schlüsselwerten.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen. Für <strong>JetMove</strong>bedeutet dies, dass ein Indexeintrag an der angeforderten Position oder am Offset für den aktuellen Index gefunden wurde.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die -Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in xp Windows eingeführt.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Der Cursor ist derzeit nicht auf einem Indexeintrag positioniert. Für <strong>JetMove</strong>bedeutet dies, dass ein Indexeintrag am angeforderten Speicherort oder Offset im aktuellen Index nicht gefunden wurde.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die -Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Der Cursor ist derzeit logisch auf einem Indexeintrag positioniert, der einem gelöschten Datensatz entspricht.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden.</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in xp Windows eingeführt.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die -Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p> | 



Wenn diese Funktion erfolgreich ist, wird der Cursor an einem Indexeintrag positioniert, der der angeforderten Position oder dem angeforderten Offset entspricht. Wenn ein Datensatz für das Update vorbereitet wurde, wird dieses Update abgebrochen. Wenn ein Indexbereich in Kraft ist und JET_MoveFirst oder JET_MoveLast wurde, wird dieser Indexbereich abgebrochen. Es erfolgt keine Änderung des Datenbankstatus.

Wenn diese Funktion fehlschlägt, bleibt die Position des Cursors unverändert, es sei denn, JET_errNoCurrentRecord zurückgegeben wurde. In diesem Fall wird der Cursor an der Position des Indexeintrags positioniert, der der angeforderten Position oder dem angeforderten Offset entspricht. Der Cursor kann relativ zu dieser Position verschoben werden, befindet sich aber immer noch nicht in einem gültigen Indexeintrag. Wenn ein Datensatz für das Update vorbereitet wurde, wird dieses Update abgebrochen. Wenn ein Indexbereich in Kraft ist und JET_MoveFirst oder JET_MoveLast wurde, wird dieser Indexbereich abgebrochen. Es erfolgt keine Änderung des Datenbankstatus.

#### <a name="remarks"></a>Bemerkungen

Ein Cursor kann mit **JetMove**, Before First und After Last an zwei spezielle Positionen verschoben werden. Wenn sich der Cursor auf dem ersten Indexeintrag in der Tabelle befindet und **JetMove** mit JET_MovePrevious aufgerufen wird, ist der Aufruf mit JET_errNoCurrentRecord nicht möglich, und der Cursor wird logisch vor dem ersten Eintrag im Index positioniert. Diese logische Position wird auch dann beibehalten, wenn vor dem ersten Eintrag im Index ein anderer Indexeintrag eingefügt wird. Eine analoge Situation tritt für After Last relativ zum Ende des Indexes auf. Before First und After Last sind besonders nützlich, wenn Sie einen Bereich von Indexeinträgen einrichten, der mit **JetMove** iteriert werden soll. Verwenden Sie dabei ein Iteratormodell, das erwartet, vor der Verwendung dieses Elements immer zum nächsten (oder vorherigen) Element zu wechseln.

Der Satz von Indexeinträgen, die **von JetMove** besucht werden können, kann durch Einrichten eines Indexbereichs für den Cursor eingeschränkt werden. Dies ist nützlich für Anwendungen, die einen Satz von Indexeinträgen aufzählen, die einfachen Kriterien entsprechen, die über ein Für diesen Index erstelltes Suchschlüsselpaar ausgedrückt werden können. Weitere Informationen finden Sie unter [JetSetIndexRange](./jetsetindexrange-function.md).

Bei Releases vor Windows Server 2003 SP1 liegt in **JetMove** ein Problem vor, das in einigen bestimmten Fällen auftritt, das sich auf die korrekte Erzwingung eines Indexbereichs auswirken kann, wie er von der [JetSetIndexRange-Funktion](./jetsetindexrange-function.md) eingerichtet wurde. Wenn sich der Cursor derzeit vor dem ersten Indexeintrag befindet und ein Indexbereich mit einer Obergrenze festgelegt wird, die kleiner als der erste Indexeintrag ist, wird der nächste Aufruf von **JetMove** fälschlicherweise zu diesem Indexeintrag wechseln, anstatt wie erwartet mit JET_errNoCurrentRecord zu fehlschlagen. Der gleiche Fehler tritt für die analoge Situation ab dem Ende des Indexes auf. Diese Situation kann in einer Anwendung auftreten, die einen Indexbereich ein richtet und ihn mithilfe eines Iterators navigiert, der erwartet, dass er vor dem ersten Indexeintrag beginnt, der ein Member der aufzählten Einträge ist, anstatt mit dem ersten Indexeintrag dieser Gruppe zu beginnen. Diese Situation tritt auch auf der analogen Fall vom Ende des Indexes an auf. Die Problemumgehung besteht darin, dass die Anwendung manuell überprüft, ob sich der abgerufene Indexeintrag innerhalb des Indexbereichs befindet, indem der Schlüssel für den aktuellen Indexeintrag (abgerufen mit [JetRetrikey)](./jetretrievekey-function.md)mit dem Schlüssel verglichen wird, der das Ende des aktuellen Indexbereichs darstellt (abgerufen mit [JetRetrikey mithilfe](./jetretrievekey-function.md) von JET_bitRetrieveCopy).

Beim Übergeben von berechneten Offsets an **JetMove** ist Vorsicht geboten. Wenn der berechnete Offset kleiner oder gleich JET_MoveFirst ist, muss dieser Offset in mehrere Teile zerbrochen werden, von denen jedes separat, aber innerhalb einer einzelnen Transaktion an **JetMove** übergeben wird, um den gewünschten Effekt zu erzielen. Dasselbe gilt für Offsets, die größer oder gleich JET_MoveNext. Es ist unwahrscheinlich, dass eine Anwendung dies in der realen Welt durchläuft, aber es ist gut, einen Schutz gegen diesen Fall zu haben, da sich die Semantik von JET_MoveFirst und JET_MoveLast von einem normalen Offset stark unterscheiden kann.

Wenn **JetMove** mit einem sehr großen Offset aufgerufen wird, z. B. wenn der cRow-Parameter auf 1000 festgelegt ist, durchläuft **JetMove** alle 1.000 Indexeinträge, um die endgültige Position zu erreichen. Derzeit bietet die ESE-API keine effiziente Möglichkeit, direkt zu einem bestimmten Indexeintrag durch Offset zu wechseln, ohne jeden Indexeintrag zu durchlaufen.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetRetrikey](./jetretrievekey-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
