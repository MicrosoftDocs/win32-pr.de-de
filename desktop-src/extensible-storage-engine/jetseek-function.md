---
description: 'Weitere Informationen zu: JetSeek-Funktion'
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
ms.openlocfilehash: 6910c9aabd53a5fa4d648831ec2651395c154453
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478976"
---
# <a name="jetseek-function"></a>JetSeek-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetseek-function"></a>JetSeek-Funktion

Die **JetSeek-Funktion** positioniert einen Cursor effizient an einem Indexeintrag, der den vom Suchschlüssel in diesem Cursor angegebenen Suchkriterien und der angegebenen Ungleichheit entspricht. Ein Suchschlüssel muss zuvor mit [JetMakeKey](./jetmakekey-function.md)erstellt worden sein.

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

Eine Gruppe von Bits, die die Optionen enthalten, die für diesen Aufruf verwendet werden sollen. *Grbit* muss ungleich 0 (null) sein und mindestens einen der in der folgenden Tabelle aufgeführten Werte enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitCheckUniqueness</p> | <p>Ein spezieller Fehlercode, JET_wrnUniqueKey, wird zurückgegeben, wenn kostengünstig festgestellt werden kann, dass genau ein Indexeintrag mit dem Suchschlüssel übereinstimmt.</p><p>Diese Option wird ignoriert, es sei denn, JET_bitSeekEQ wird ebenfalls angegeben.</p><p>Diese Option ist nur in Windows Server 2003 und höher verfügbar.</p> | 
| <p>JET_bitSeekEQ</p> | <p>Der Cursor wird am Indexeintrag positioniert, der am nächsten am Anfang des Indexes liegt und genau mit dem Suchschlüssel übereinstimmt. Der Anfang des Indexes ist der Indexeintrag, der beim Verschieben zum ersten Datensatz in diesem Index gefunden wird. Der Anfang des Indexes entspricht nicht dem unteren Indexende, das sich je nach Sortierreihenfolge der Schlüsselspalten im Index ändern kann.</p><p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mit <a href="gg269329(v=exchg.10).md">jetMakeKey</a> mithilfe einer Platzhalteroption erstellt wurde.</p> | 
| <p>JET_bitSeekGE</p> | <p>Der Cursor wird am Indexeintrag positioniert, der dem Indexanfang am nächsten ist, der größer oder gleich einem Indexeintrag ist, der genau den Suchkriterien entsprechen würde. Der Anfang des Indexes ist der Indexeintrag, der beim Verschieben zum ersten Datensatz in diesem Index gefunden wird. Der Anfang des Indexes entspricht nicht dem unteren Indexende, das sich je nach Sortierreihenfolge der Schlüsselspalten im Index ändern kann.</p><p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mithilfe von <a href="gg269329(v=exchg.10).md">JetMakeKey</a> mithilfe einer Platzhalteroption erstellt wurde, um Indexeinträge zu finden, die am nächsten am Ende des Indexes liegen.</p> | 
| <p>JET_bitSeekGT</p> | <p>Der Cursor wird am Indexeintrag positioniert, der dem Indexanfang am nächsten liegt und größer als ein Indexeintrag ist, der genau den Suchkriterien entsprechen würde. Der Anfang des Indexes ist der Indexeintrag, der beim Verschieben zum ersten Datensatz in diesem Index gefunden wird. Der Anfang des Indexes entspricht nicht dem unteren Indexende, das sich je nach Sortierreihenfolge der Schlüsselspalten im Index ändern kann.</p><p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mithilfe von <a href="gg269329(v=exchg.10).md">JetMakeKey</a> mithilfe einer Platzhalteroption erstellt wurde, um Indexeinträge zu finden, die am nächsten am Anfang des Indexes liegen.</p> | 
| <p>JET_bitSeekLE</p> | <p>Der Cursor wird am Indexeintrag positioniert, der dem Indexende am nächsten liegt und kleiner oder gleich einem Indexeintrag ist, der genau den Suchkriterien entsprechen würde. Das Ende des Indexes ist der Indexeintrag, der beim Verschieben zum letzten Datensatz in diesem Index gefunden wird. Das Ende des Indexes ist nicht dasselbe wie das obere Ende des Indexes, das sich je nach Sortierreihenfolge der Schlüsselspalten im Index ändern kann.</p><p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mithilfe von <a href="gg269329(v=exchg.10).md">JetMakeKey</a> mithilfe einer Platzhalteroption erstellt wurde, um Indexeinträge zu finden, die am nächsten am Anfang des Indexes liegen.</p> | 
| <p>JET_bitSeekLT</p> | <p>Der Cursor wird am Indexeintrag positioniert, der dem Indexende am nächsten liegt und kleiner als ein Indexeintrag ist, der genau den Suchkriterien entsprechen würde. Das Ende des Indexes ist der Indexeintrag, der beim Verschieben zum letzten Datensatz in diesem Index gefunden wird. Das Ende des Indexes ist nicht dasselbe wie das obere Ende des Indexes, das sich je nach Sortierreihenfolge der Schlüsselspalten im Index ändern kann.</p><p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mithilfe von <a href="gg269329(v=exchg.10).md">JetMakeKey</a> mithilfe einer Platzhalteroption erstellt wurde, um Indexeinträge zu finden, die am nächsten am Ende des Indexes liegen.</p> | 
| <p>JET_bitSetIndexRange</p> | <p>Ein Indexbereich wird automatisch für alle Schlüssel eingerichtet, die genau mit dem Suchschlüssel übereinstimmen. Der resultierende Indexbereich ist identisch mit dem Indexbereich, der andernfalls durch einen Aufruf von <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> mit den Optionen JET_bitRangeInclusive und JET_bitRangeUpperLimit erstellt worden wäre. Weitere Informationen finden Sie unter <a href="gg294112(v=exchg.10).md">JetSetIndexRange.</a></p><p>Dies ist eine praktische Methode zum Ermitteln aller Indexeinträge, die den gleichen Suchkriterien entsprechen.</p><p>Diese Option wird ignoriert, es sei denn, JET_bitSeekEQ wird ebenfalls angegeben.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion ermöglicht die Rückgabe aller [JET_ERRs,](./jet-err.md) die in dieser API definiert sind. Weitere Informationen zu Jet-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p><p>Für <strong>JetSeek</strong>bedeutet dies, dass ein Indexeintrag gefunden wurde, der genau mit den Suchkriterien übereinstimmt.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errKeyNotMade</p> | <p>Es gibt keinen aktuellen Suchschlüssel für den Cursor. <strong>JetSeek</strong> erfordert, dass der Cursor über einen gültigen Suchschlüssel verfügen muss, da dieser für die Suchkriterien verwendet wird, die zum Suchen von Indexeinträgen verwendet werden.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRecordNotFound</p> | <p>Es wurde kein Indexeintrag gefunden, der den Suchkriterien entspricht.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_wrnSeekNotEqual</p> | <p>Es wurde ein Indexeintrag gefunden, der den Suchkriterien entspricht. Dieser Indexeintrag war jedoch keine genaue Übereinstimmung.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden.</p><p>Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_wrnUniqueKey</p> | <p>Es wurde genau ein Indexeintrag gefunden, der genau mit den Suchkriterien übereinstimmte. Dieser Fehler wird nur zurückgegeben, wenn JET_bitSeekCheckUniqueness angegeben wurde und es kostengünstig war, festzustellen, ob der übereinstimmende Indexeintrag der einzige Indexeintrag war, der genau mit den Suchkriterien übereinstimmt.</p><p>Dieser Fehler wird nur von Windows Server 2003 und höher zurückgegeben.</p> | 



Bei Erfolg wird der Cursor an einem Indexeintrag positioniert, der den Suchkriterien entspricht. Wenn ein Datensatz für das Update vorbereitet wurde, wird dieses Update abgebrochen. Wenn ein Indexbereich in Kraft ist, wird dieser Indexbereich abgebrochen. Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird dieser Suchschlüssel gelöscht. Es erfolgt keine Änderung des Datenbankzustands. Wenn mehrere Indexeinträge denselben Wert aufweisen, wird immer der Eintrag ausgewählt, der dem Indexanfang am nächsten liegt.

Bei einem Fehler bleibt die Position des Cursors unverändert, es sei denn, JET_errRecordNotFound wurde zurückgegeben. In diesem Fall wird der Cursor an der Stelle positioniert, an der der Indexeintrag, der mit den suchkriterien übereinstimmt, die durch den Suchschlüssel in diesem Cursor angegeben wurden, und die angegebene Ungleichheit gewesen wäre. Der Cursor kann relativ zu dieser Position verschoben werden, befindet sich aber immer noch nicht in einem gültigen Indexeintrag. Wenn ein Datensatz für das Update vorbereitet wurde, wird dieses Update abgebrochen. Wenn ein Indexbereich in Kraft ist, wird dieser Indexbereich abgebrochen. Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird dieser Suchschlüssel gelöscht. Es erfolgt keine Änderung des Datenbankzustands.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
