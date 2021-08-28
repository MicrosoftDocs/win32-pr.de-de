---
description: 'Weitere Informationen zu: JetMove-Funktion'
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
ms.openlocfilehash: 020018ede6be6ff13d65667deee5c189d98e1e53
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474056"
---
# <a name="jetmove-function"></a>JetMove-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetmove-function"></a>JetMove-Funktion

Die **JetMove-Funktion** positioniert einen Cursor am Anfang oder Ende eines Indexes und durchläuft die Einträge in diesem Index entweder vorwärts oder rückwärts. Es ist auch möglich, den Cursor um eine angegebene Anzahl von Indexeinträgen vorwärts oder rückwärts auf den aktuellen Index zu bewegen. Ein weiterer Ansatz besteht darin, die Indexeinträge, die mit **JetMove** aufzählt werden können, durch Einrichten eines Indexbereichs auf dem Cursor mit [jetSetIndexRange](./jetsetindexrange-function.md)auf künstliche Weise einzuschränken.

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
| <p>JET_MoveFirst</p> | <p>Verschiebt den Cursor zum ersten Indexeintrag im Index (sofern vorhanden).</p><p><strong>Hinweis</strong>   Der Literalwert von -2147483648 wird verwendet, um diese Option zu kennzeichnen. Verwenden Sie diesen Wert nicht als gewöhnlichen Offset, oder es kann zu unbeabsichtigtem Verhalten führen.</p> | 
| <p>JET_MoveLast</p> | <p>Verschiebt den Cursor auf den letzten Indexeintrag im Index (sofern vorhanden).</p><p><strong>Hinweis</strong>   Der Literalwert von 2147483647 wird verwendet, um diese Option zu kennzeichnen. Verwenden Sie diesen Wert nicht als gewöhnlichen Offset, oder es kann zu unbeabsichtigtem Verhalten führen.</p> | 
| <p>JET_MoveNext</p> | <p>Verschiebt den Cursor zum nächsten Indexeintrag im Index (sofern vorhanden). Dieser Wert ist genau gleich einem normalen Offset von +1.</p> | 
| <p>JET_MovePrevious</p> | <p>Verschiebt den Cursor zum vorherigen Indexeintrag im Index (sofern vorhanden).</p><p>Dieser Wert ist genau gleich einem normalen Offset von -1 oder 0 (Null).</p><p>Der Cursor verbleibt an der aktuellen logischen Position, und das Vorhandensein des Indexeintrags, der dieser logischen Position entspricht, wird getestet.</p> | 



*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angeben.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitMoveKeyNE</p> | <p>Verschiebt den Cursor nach vorn oder rückwärts um die Anzahl der Indexeinträge, die erforderlich sind, um die angeforderte Anzahl von Indexschlüsselwerten im Index zu überspringen. Dies hat den Effekt, dass Indexeinträge mit doppelten Schlüsselwerten in einen einzelnen Indexeintrag reduziert werden. Normalerweise bewegt ein Offset den Cursor um die angegebene Anzahl von Indexeinträgen, unabhängig von ihren Schlüsselwerten.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen. Für <strong>JetMove</strong>bedeutet dies, dass ein Indexeintrag am angeforderten Speicherort oder Offset für den aktuellen Index gefunden wurde.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>beendet wurden.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Der Cursor befindet sich derzeit nicht in einem Indexeintrag. Für <strong>JetMove</strong>bedeutet dies, dass am angeforderten Speicherort oder Offset für den aktuellen Index kein Indexeintrag gefunden wurde.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Der Cursor ist derzeit logisch auf einem Indexeintrag positioniert, der einem gelöschten Datensatz entspricht.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden.</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p> | 



Wenn diese Funktion erfolgreich ausgeführt wird, wird der Cursor an einem Indexeintrag positioniert, der der angeforderten Position oder dem angeforderten Offset entspricht. Wenn ein Datensatz für das Update vorbereitet wurde, wird dieses Update abgebrochen. Wenn ein Indexbereich wirksam ist und JET_MoveFirst oder JET_MoveLast angegeben wurde, wird dieser Indexbereich abgebrochen. Es wird keine Änderung am Datenbankzustand vorgenommen.

Wenn diese Funktion fehlschlägt, bleibt die Position des Cursors unverändert, es sei denn, JET_errNoCurrentRecord wurde zurückgegeben. In diesem Fall wird der Cursor an der Stelle positioniert, an der sich der Indexeintrag befindet, der mit der angeforderten Position oder dem angeforderten Offset übereinstimmt. Der Cursor kann relativ zu dieser Position verschoben werden, befindet sich aber immer noch nicht in einem gültigen Indexeintrag. Wenn ein Datensatz für das Update vorbereitet wurde, wird dieses Update abgebrochen. Wenn ein Indexbereich wirksam ist und JET_MoveFirst oder JET_MoveLast angegeben wurde, wird dieser Indexbereich abgebrochen. Es wird keine Änderung am Datenbankzustand vorgenommen.

#### <a name="remarks"></a>Hinweise

Ein Cursor kann mit **JetMove**, Before First und After Last an zwei spezielle Positionen verschoben werden. Wenn sich der Cursor auf dem ersten Indexeintrag in der Tabelle befindet und **JetMove** mit JET_MovePrevious aufgerufen wird, schlägt der Aufruf mit JET_errNoCurrentRecord fehl, und der Cursor wird logisch vor dem ersten Eintrag im Index positioniert. Diese logische Position wird auch dann beibehalten, wenn vor dem ersten Eintrag im Index ein anderer Indexeintrag eingefügt wird. Eine analoge Situation tritt für After Last relativ zum Ende des Indexes auf. Vor und nach der Letzten sind am nützlichsten, wenn Sie einen Bereich von Indexeinträgen einrichten, die mit **JetMove** iteriert werden sollen, indem Sie ein Iteratormodell verwenden, das erwartet, immer zum nächsten (oder vorherigen) Element zu wechseln, bevor dieses Element verwendet wird.

Der Satz von Indexeinträgen, die von **JetMove** aufgerufen werden können, kann durch Einrichten eines Indexbereichs für den Cursor eingeschränkt werden. Dies ist nützlich für Anwendungen, die einen Satz von Indexeinträgen aufzählen, die einfachen Kriterien entsprechen, die durch ein Suchschlüsselpaar ausgedrückt werden können, das für diesen Index erstellt wurde. Weitere Informationen finden Sie unter [JetSetIndexRange.](./jetsetindexrange-function.md)

In Releases vor Windows Server 2003 SP1 tritt in **JetMove** ein Problem auf, das sich in bestimmten Fällen auf die korrekte Erzwingung eines Indexbereichs auswirkt, wie von der [JetSetIndexRange-Funktion](./jetsetindexrange-function.md) eingerichtet. Wenn sich der Cursor derzeit vor dem ersten Indexeintrag befindet und ein Indexbereich mit einer Obergrenze festgelegt ist, die kleiner als der erste Indexeintrag ist, wird der nächste Aufruf von **JetMove** fälschlicherweise zu diesem Indexeintrag wechseln, anstatt wie erwartet mit JET_errNoCurrentRecord zu fehlschlagen. Der gleiche Fehler tritt für die analoge Situation ab dem Ende des Indexes auf. Diese Situation kann in einer Anwendung auftreten, die einen Indexbereich einrichtet und mithilfe eines Iterators navigiert, der erwartet, vor dem ersten Indexeintrag zu starten, der ein Member der aufzuzählenden Einträge ist, anstatt mit dem ersten Indexeintrag dieser Gruppe zu beginnen. Diese Situation tritt auch bei analogem Fall ab dem Ende des Indexes auf. Die Problemumgehung besteht darin, dass die Anwendung manuell überprüft, ob sich der abgerufene Indexeintrag innerhalb des Indexbereichs befindet, indem der Schlüssel für den aktuellen Indexeintrag (abgerufen mit [JetRetrieveKey)](./jetretrievekey-function.md)mit dem Schlüssel verglichen wird, der das Ende des aktuellen Indexbereichs darstellt (abgerufen mit [JetRetrieveKey](./jetretrievekey-function.md) mithilfe von JET_bitRetrieveCopy).

Es ist wichtig, vorsichtig zu sein, wenn Berechnete Offsets an **JetMove** übergeben werden. Wenn der berechnete Offset kleiner oder gleich JET_MoveFirst ist, muss dieser Offset in mehrere Teile aufgeteilt werden, die jeweils separat an **JetMove** übergeben werden, jedoch innerhalb einer einzelnen Transaktion, um den gewünschten Effekt zu erzielen. Dasselbe gilt für Offsets, die größer oder gleich JET_MoveNext sind. Es ist unwahrscheinlich, dass eine Anwendung dies in der realen Welt durchläuft, aber es ist gut, einen Schutz gegen diesen Fall zu haben, angesichts der sehr unterschiedlichen Semantik von JET_MoveFirst und JET_MoveLast von einem gewöhnlichen Offset.

Wenn **JetMove** mit einem sehr großen Offset aufgerufen wird, z. B. wenn der cRow-Parameter auf 1000 festgelegt ist, durchläuft **JetMove** alle 1.000 Indexeinträge, um die endgültige Position zu erreichen. Derzeit bietet die ESE-API keine effiziente Möglichkeit, direkt zu einem bestimmten Indexeintrag per Offset zu wechseln, ohne jeden Indexeintrag zu durchlaufen.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
