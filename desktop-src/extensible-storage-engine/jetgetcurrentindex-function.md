---
description: 'Weitere Informationen zu: JetGetCurrentIndex-Funktion'
title: JetGetCurrentIndex-Funktion
TOCTitle: JetGetCurrentIndex Function
ms:assetid: 9db3b875-0b95-4027-9742-c36d2d7e64cf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294041(v=EXCHG.10)
ms:contentKeyID: 32765642
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCurrentIndexW
- JetGetCurrentIndex
- JetGetCurrentIndexA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82f24afb4d8e36d95d6e3be480f32358c1c5dba2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468307"
---
# <a name="jetgetcurrentindex-function"></a>JetGetCurrentIndex-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetcurrentindex-function"></a>JetGetCurrentIndex-Funktion

Die **JetGetCurrentIndex-Funktion** bestimmt den Namen des aktuellen Indexes eines angegebenen Cursors. Dieser Name wird auch verwendet, um diesen Index später mit [jetSetCurrentIndex](./jetsetcurrentindex-function.md)als aktuellen Index erneut auszuwählen. Sie kann auch verwendet werden, um die Eigenschaften dieses Indexes mit [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)zu ermitteln.

```cpp
    JET_ERR JET_API JetGetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_PSTR szIndexName,
      __in          unsigned long cchIndexName
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*szIndexName*

Der Ausgabepuffer, der den Namen des aktuellen Indexes des Cursors empfängt.

*cchIndexName*

Die maximale Größe des Ausgabepuffers in Zeichen.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen, aber der Ausgabepuffer war zu klein, um den gesamten Indexnamen zu empfangen.</p><p>Der Ausgabepuffer wurde mit so vielen Indexnamen gefüllt, wie es passt. Wenn der Ausgabepuffer mindestens ein Zeichen lang ist, wird die Zeichenfolge in diesem Ausgabepuffer mit NULL beendet.</p><p><strong>Hinweis  </strong> Dieser Fehler wird nicht zurückgegeben, wenn cchIndexName 0 (null) ist. Weitere Informationen finden Sie im Abschnitt "Hinweise".</p> | 



Bei Erfolg wird der Name des aktuellen Indexes des angegebenen Cursors im Ausgabepuffer zurückgegeben. Wenn JET_wrnBufferTruncated zurückgegeben wird, enthält der Ausgabepuffer so viel des Indexnamens, wie er in den bereitgestellten Bereich passt. Wenn der Ausgabepuffer mindestens ein Zeichen lang ist, wird die in diesem Puffer zurückgegebene Zeichenfolge mit NULL beendet. Es wird keine Änderung am Datenbankzustand vorgenommen.

Bei einem Fehler ist der Status des Ausgabepuffers nicht definiert. Es wird keine Änderung am Datenbankzustand vorgenommen.

#### <a name="remarks"></a>Hinweise

Wenn kein aktueller Index für den Cursor vorhanden ist, wird eine leere Zeichenfolge zurückgegeben. Dies kann passieren, wenn sich der Cursor auf dem gruppierten Index der Tabelle befindet und kein primärer Index definiert wurde. Dieser Index wird als sequenzieller Index der Tabelle bezeichnet und weist keine Definition auf. Wenn Sie den aktuellen Index mit [JetSetCurrentIndex](./jetsetcurrentindex-function.md) auf eine leere Zeichenfolge festlegen, wird der gruppierte Index unabhängig vom Vorhandensein einer primären Indexdefinition ausgewählt.

Es gibt einen wichtigen Fehler in dieser Funktion, der in allen Releases vorhanden ist. Wenn der Ausgabepuffer zu klein ist, um den gesamten Indexnamen zu empfangen, und der Ausgabepuffer mindestens ein Zeichen lang ist, wird JET_wrnBufferTruncated NICHT zurückgegeben. stattdessen werden JET_errSuccess zurückgegeben. Um dieses Problem zu vermeiden, sollte der Ausgabepuffer immer mindestens JET_cbNameMost + 1 (65) Zeichen lang sein.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetGetCurrentIndexW</strong> (Unicode) und <strong>JetGetCurrentIndexA</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetSetCurrentIndex](./jetsetcurrentindex-function.md)
