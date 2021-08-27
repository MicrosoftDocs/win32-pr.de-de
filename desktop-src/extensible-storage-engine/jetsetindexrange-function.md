---
description: Weitere Informationen finden Sie unter JetSetIndexRange-Funktion.
title: JetSetIndexRange-Funktion
TOCTitle: JetSetIndexRange Function
ms:assetid: dac99576-707d-4713-9825-ddad1980723e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294112(v=EXCHG.10)
ms:contentKeyID: 32765726
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetIndexRange
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 918d1c7f70f4f02158473ad4b97a510058787a6b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477466"
---
# <a name="jetsetindexrange-function"></a>JetSetIndexRange-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetindexrange-function"></a>JetSetIndexRange-Funktion

Die **JetSetIndexRange-Funktion** schränkt vorübergehend den Satz von Indexeinträgen ein, die der Cursor mit [JetMove](./jetmove-function.md) auf diejenigen einschränkt, die vom aktuellen Indexeintrag bis zum Indexeintrag beginnen, der den suchkriterien entspricht, die vom Suchschlüssel in diesem Cursor und den angegebenen gebundenen Kriterien angegeben werden. Ein Suchschlüssel muss zuvor mit [JetMakeKey erstellt worden sein.](./jetmakekey-function.md)

```cpp
    JET_ERR JET_API JetSetIndexRange(
      __in          JET_SESID sesid,
    __in          JET_TABLEID tableidSrc,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableidSrc*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*grbit*

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten, die null oder mehr der folgenden Elemente enthalten:


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitRangeInclusive</p> | <p>Dieses Vorhandensein oder Fehlen dieser Option gibt die Begrenzungskriterien des Indexbereichs an. Wenn diese Option vorhanden ist, gibt diese Option an, dass der Indexbereich inklusiv ist. Wenn diese Option nicht vorhanden ist, gibt diese Option an, dass der Indexbereich exklusiv ist. Wenn das Limit des Indexbereichs inklusiv ist, werden alle Indexeinträge, die genau mit den Suchkriterien übereinstimmen, in den Bereich aufgenommen.</p> | 
| <p>JET_bitRangeInstantDuration</p> | <p>Diese Option fordert an, dass der Indexbereich entfernt wird, sobald er eingerichtet wurde. Alle anderen Aspekte des Vorgangs bleiben unverändert. Dies ist nützlich, um zu testen, ob Indexeinträge vorliegen, die den Suchkriterien entsprechen.</p> | 
| <p>JET_bitRangeRemove</p> | <p>Diese Option fordert an, dass ein vorhandener Indexbereich auf dem Cursor abgebrochen wird. Nachdem der Indexbereich abgebrochen wurde, ist es möglich, mit JetMove über das Ende des <a href="gg294117(v=exchg.10).md">Indexbereichs hinaus zu wechseln.</a> Wenn ein Indexbereich noch nicht wirksam ist, tritt bei <strong>JetSetIndexRange</strong> ein Fehler auf, JET_errInvalidOperation.</p><p>Wenn diese Option angegeben wird, werden alle anderen Optionen ignoriert.</p> | 
| <p>JET_bitRangeUpperLimit</p> | <p>Wenn diese Option verwendet wird, stellt der Suchschlüssel im Cursor die Suchkriterien für den Indexeintrag dar, der dem Ende des Indexes am nächsten ist, der dem Indexbereich entspricht. Der Indexbereich wird zwischen der aktuellen Position des Cursors und diesem Indexeintrag festgelegt, sodass alle Übereinstimmungen gefunden werden können, indem sie im Index mit <a href="gg294117(v=exchg.10).md">JetMove</a> mit JET_MoveNext oder einem positiven Offset vorwärts gehen.</p><p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mit <a href="gg269329(v=exchg.10).md">JetMakeKey</a> mithilfe einer Platzhalteroption erstellt wurde, um Indexeinträge zu finden, die dem Indexanfang am nächsten sind.</p><p>Wenn diese Option weggelassen wird, stellt der Suchschlüssel im Cursor die Suchkriterien für den Indexeintrag dar, der dem Anfang des Indexes am nächsten ist, der dem Indexbereich entspricht. Der Indexbereich wird zwischen der aktuellen Position des Cursors und diesem Indexeintrag festgelegt, sodass alle Übereinstimmungen gefunden werden können, indem sie im Index mit <a href="gg294117(v=exchg.10).md">JetMove</a> mit JET_MovePrevious oder einem negativen Offset rückwärts gehen.</p><p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel auslassen, der mit <a href="gg269329(v=exchg.10).md">JetMakeKey</a> mithilfe einer Platzhalteroption erstellt wurde, um Indexeinträge zu finden, die dem Ende des Indexes am nächsten sind.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p><p>Für <strong>JetSetIndexRange</strong>bedeutet dies, dass entweder ein vorhandener Indexbereich abgebrochen wurde oder mindestens ein Indexeintrag innerhalb des Indexbereichs vorhanden ist.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidOperation</p> | <p>Dieser Fehler wird von <strong>JetSetIndexRange</strong> zurückgegeben, wenn JET_bitRangeRemove angegeben wurde und kein Indexbereich in Kraft war.</p> | 
| <p>JET_errKeyNotMade</p> | <p>Es gibt keinen aktuellen Suchschlüssel für den Cursor. <strong>JetSetIndexRange</strong> erfordert, dass der Cursor einen gültigen Suchschlüssel hat, da er diesen für die Suchkriterien verwendet, die zum Suchen von Indexeinträgen verwendet werden.</p> | 
| <p>JET_errNoCurrentIndex</p> | <p>Es gibt keinen aktuellen Index für den Cursor. Dies geschieht für <strong>JetSetIndexRange,</strong> wenn sich der Cursor auf dem gruppierten Index einer Tabelle befindet und kein primärer Index definiert wurde. Das Festlegen eines Indexbereichs für einen solchen Index wird nicht unterstützt.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Dieser Fehler wird von <strong>JetSetIndexRange zurückgegeben,</strong> um anzugeben, dass im Indexbereich keine Indexeinträge enthalten sind.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden.</p><p>Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird JET_bitRangeRemove index range, der derzeit in Kraft ist, abgebrochen. Wenn JET_bitRangeRemove nicht angegeben und JET_bitRangeInstantDuration angegeben wird, ist kein Indexbereich wirksam. Wenn weder JET_bitRangeRemove noch JET_bitRangeInstantDuration ist, ist ein neuer Indexbereich wirksam. Dieser Indexbereich schränkt vorübergehend den Satz von Indexeinträgen ein, die der Cursor mit [JetMove](./jetmove-function.md) auf diejenigen einschränkt, die vom aktuellen Indexeintrag bis zum Indexeintrag beginnen, der den Suchkriterien entspricht. Die Position des Cursors bleibt unverändert. Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird dieser Suchschlüssel gelöscht. Es erfolgt keine Änderung des Datenbankstatus.

Wenn bei einem Fehler JET_errNoCurrentRecord zurückgegeben wird, ist kein Indexbereich wirksam. Wenn JET_errNoCurrentRecord zurückgegeben wird, ist ein neuer Indexbereich wirksam. Dieser Indexbereich schränkt vorübergehend den Satz von Indexeinträgen ein, die der Cursor mit [JetMove](./jetmove-function.md) auf diejenigen einschränkt, die vom aktuellen Indexeintrag bis zum Indexeintrag beginnen, der den Suchkriterien entspricht. Die Position des Cursors bleibt unverändert. Wenn JET_errNoCurrentRecord zurückgegeben wurde und ein Suchschlüssel für den Cursor erstellt wurde, wird dieser Suchschlüssel gelöscht. Es erfolgt keine Änderung des Datenbankstatus.

#### <a name="remarks"></a>Hinweise

Ein Indexbereich ist flüchtig und wird automatisch abgebrochen, wenn eine andere Navigation als [JetMove](./jetmove-function.md) auf dem Cursor ausgeführt wird.

Indexbereiche funktionieren nur in einer Richtung. Wenn eine Obergrenze festgelegt wird, wird nur die Vorwärtsbewegung mit [JetMove](./jetmove-function.md) mit JET_MoveNext oder ein positiver Offset verhindert, sobald das Ende des Indexbereichs erreicht wurde. Es ist weiterhin möglich, den Indexbereich in diesem Fall zu verlassen, indem [JetMove](./jetmove-function.md) mit JET_MovePrevious oder einem negativen Offset verwendet wird. Eine analoge Situation tritt bei einer unteren Grenze auf.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetMove](./jetmove-function.md)  
[JetSetIndexRange]()  
[JetStopService](./jetstopservice-function.md)
