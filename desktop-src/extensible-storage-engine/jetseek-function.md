---
description: Weitere Informationen finden Sie unter JetSeek-Funktion.
title: JetSeek-Funktion
TOCTitle: JetSeek Function
ms:assetid: d3d5bfae-dd27-47ab-96c4-6bc9a01a501b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294103(v=EXCHG.10)
ms:contentKeyID: 32765718
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSeek
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fbc980a838742971d2ecc3dfeebf5efb6295ea3
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985543"
---
# <a name="jetseek-function"></a>JetSeek-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetseek-function"></a>JetSeek-Funktion

Die **JetSeek-Funktion** positioniert einen Cursor effizient an einem Indexeintrag, der den suchkriterien entspricht, die vom Suchschlüssel in diesem Cursor und der angegebenen Ungleichheit angegeben werden. Ein Suchschlüssel muss zuvor mit [JetMakeKey erstellt worden sein.](./jetmakekey-function.md)

```cpp
    JET_ERR JET_API JetSeek(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*grbit*

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten. *Grbit* muss ungleich 0 (null) sein und mindestens einen der in der folgenden Tabelle aufgeführten Werte enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitCheckUniqueness</p> | <p>Ein spezieller Fehlercode, JET_wrnUniqueKey, wird zurückgegeben, wenn kostengünstig ermittelt werden kann, dass genau ein Indexeintrag mit dem Suchschlüssel stimmt.</p><p>Diese Option wird ignoriert, es sei denn, JET_bitSeekEQ wird ebenfalls angegeben.</p><p>Diese Option ist nur auf Windows Server 2003 und höher verfügbar.</p> | 
| <p>JET_bitSeekEQ</p> | <p>Der Cursor wird an dem Indexeintrag positioniert, der dem Anfang des Indexes am nächsten ist, der genau mit dem Suchschlüssel entspricht. Der Anfang des Index ist der Indexeintrag, der beim Verschieben zum ersten Datensatz in diesem Index gefunden wird. Der Anfang des Indexes ist nicht mit dem unteren Ende des Indexes identisch, der sich je nach Sortierreihenfolge der Schlüsselspalten im Index ändern kann.</p><p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mit <a href="gg269329(v=exchg.10).md">JetMakeKey</a> mithilfe einer Platzhalteroption erstellt wurde.</p> | 
| <p>JET_bitSeekGE</p> | <p>Der Cursor wird an dem Indexeintrag positioniert, der dem Indexanfang am nächsten liegt, der größer oder gleich einem Indexeintrag ist, der genau mit den Suchkriterien übereinstimmen würde. Der Anfang des Index ist der Indexeintrag, der beim Verschieben zum ersten Datensatz in diesem Index gefunden wird. Der Anfang des Indexes ist nicht mit dem unteren Ende des Indexes identisch, der sich je nach Sortierreihenfolge der Schlüsselspalten im Index ändern kann.</p><p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mit <a href="gg269329(v=exchg.10).md">JetMakeKey</a> mithilfe einer Platzhalteroption erstellt wurde, um Indexeinträge zu finden, die dem Ende des Indexes am nächsten sind.</p> | 
| <p>JET_bitSeekGT</p> | <p>Der Cursor wird an dem Indexeintrag positioniert, der dem Indexanfang am nächsten liegt, der größer als ein Indexeintrag ist, der genau den Suchkriterien entspricht. Der Anfang des Index ist der Indexeintrag, der beim Verschieben zum ersten Datensatz in diesem Index gefunden wird. Der Anfang des Indexes ist nicht mit dem unteren Ende des Indexes identisch, der sich je nach Sortierreihenfolge der Schlüsselspalten im Index ändern kann.</p><p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mit <a href="gg269329(v=exchg.10).md">JetMakeKey</a> mithilfe einer Platzhalteroption erstellt wurde, um Indexeinträge zu finden, die dem Indexanfang am nächsten sind.</p> | 
| <p>JET_bitSeekLE</p> | <p>Der Cursor wird an dem Indexeintrag positioniert, der dem Ende des Indexes am nächsten liegt, der kleiner oder gleich einem Indexeintrag ist, der genau den Suchkriterien entspricht. Das Ende des Indexes ist der Indexeintrag, der beim Wechsel zum letzten Datensatz in diesem Index gefunden wird. Das Ende des Indexes ist nicht dasselbe wie das obere Ende des Index, das sich je nach Sortierreihenfolge der Schlüsselspalten im Index ändern kann.</p><p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mit <a href="gg269329(v=exchg.10).md">JetMakeKey</a> mithilfe einer Platzhalteroption erstellt wurde, um Indexeinträge zu finden, die dem Indexanfang am nächsten sind.</p> | 
| <p>JET_bitSeekLT</p> | <p>Der Cursor wird an dem Indexeintrag positioniert, der dem Ende des Indexes am nächsten liegt, der kleiner als ein Indexeintrag ist, der genau mit den Suchkriterien übereinstimmen würde. Das Ende des Indexes ist der Indexeintrag, der beim Wechsel zum letzten Datensatz in diesem Index gefunden wird. Das Ende des Indexes ist nicht dasselbe wie das obere Ende des Index, das sich je nach Sortierreihenfolge der Schlüsselspalten im Index ändern kann.</p><p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mit <a href="gg269329(v=exchg.10).md">JetMakeKey</a> mithilfe einer Platzhalteroption erstellt wurde, um Indexeinträge zu finden, die dem Ende des Indexes am nächsten sind.</p> | 
| <p>JET_bitSetIndexRange</p> | <p>Ein Indexbereich wird automatisch für alle Schlüssel eingerichtet, die genau mit dem Suchschlüssel übereinstimmen. Der resultierende Indexbereich ist identisch mit dem, der andernfalls durch einen Aufruf von <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> mit den Optionen JET_bitRangeInclusive und JET_bitRangeUpperLimit wurde. Weitere Informationen finden Sie unter <a href="gg294112(v=exchg.10).md">JetSetIndexRange.</a></p><p>Dies ist eine praktische Methode zum Suchen aller Indexeinträge, die denselben Suchkriterien entsprechen.</p><p>Diese Option wird ignoriert, es sei denn, JET_bitSeekEQ wird ebenfalls angegeben.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion ermöglicht die Rückgabe aller [JET_ERRs,](./jet-err.md) die in dieser API definiert sind. Weitere Informationen zu Jet-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p><p>Für <strong>JetSeek bedeutet</strong>dies, dass ein Indexeintrag gefunden wurde, der genau den Suchkriterien entspricht.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errKeyNotMade</p> | <p>Es gibt keinen aktuellen Suchschlüssel für den Cursor. <strong>JetSeek erfordert,</strong> dass der Cursor einen gültigen Suchschlüssel hat, da er diesen für die Suchkriterien verwendet, die zum Suchen von Indexeinträgen verwendet werden.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRecordNotFound</p> | <p>Es wurde kein Indexeintrag gefunden, der den Suchkriterien entspricht.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_wrnSeekNotEqual</p> | <p>Es wurde ein Indexeintrag gefunden, der den Suchkriterien entspricht. Dieser Indexeintrag war jedoch keine genaue Übereinstimmung.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden.</p><p>Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_wrnUniqueKey</p> | <p>Es wurde genau ein Indexeintrag gefunden, der genau den Suchkriterien entspricht. Dieser Fehler wird nur zurückgegeben, wenn JET_bitSeekCheckUniqueness angegeben wurde, und es war kostengünstig zu ermitteln, dass der übereinstimmende Indexeintrag der einzige Indexeintrag war, der genau den Suchkriterien entspricht.</p><p>Dieser Fehler wird nur von Windows Server 2003 und höher zurückgegeben.</p> | 



Bei Erfolg wird der Cursor an einem Indexeintrag positioniert, der den Suchkriterien entspricht. Wenn ein Datensatz für das Update vorbereitet wurde, wird dieses Update abgebrochen. Wenn ein Indexbereich in Kraft ist, wird dieser Indexbereich abgebrochen. Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird dieser Suchschlüssel gelöscht. Es erfolgt keine Änderung des Datenbankstatus. Wenn mehrere Indexeinträge denselben Wert haben, wird immer der Eintrag ausgewählt, der dem Anfang des Indexes am nächsten liegt.

Bei einem Fehler bleibt die Position des Cursors unverändert, es sei denn, JET_errRecordNotFound zurückgegeben wurde. In diesem Fall wird der Cursor an der Stelle positioniert, an der der Indexeintrag, der den suchkriterien entspricht, die vom Suchschlüssel in diesem Cursor angegeben wurden, und der angegebenen Ungleichheit entspricht. Der Cursor kann relativ zu dieser Position verschoben werden, befindet sich aber immer noch nicht in einem gültigen Indexeintrag. Wenn ein Datensatz für das Update vorbereitet wurde, wird dieses Update abgebrochen. Wenn ein Indexbereich in Kraft ist, wird dieser Indexbereich abgebrochen. Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird dieser Suchschlüssel gelöscht. Es erfolgt keine Änderung des Datenbankstatus.

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
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
