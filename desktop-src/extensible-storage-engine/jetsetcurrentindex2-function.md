---
description: Weitere Informationen zur JetSetCurrentIndex2-Funktion
title: JetSetCurrentIndex2-Funktion
TOCTitle: JetSetCurrentIndex2 Function
ms:assetid: da94465e-bd35-45c2-9ccc-1d2e8c34aa9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294110(v=EXCHG.10)
ms:contentKeyID: 32765725
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex2W
- JetSetCurrentIndex2A
- JetSetCurrentIndex2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 814813e90446161942775e5c1a26611ed834886f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472486"
---
# <a name="jetsetcurrentindex2-function"></a>JetSetCurrentIndex2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetcurrentindex2-function"></a>JetSetCurrentIndex2-Funktion

Die **JetSetCurrentIndex2-Funktion** legt den aktuellen Index eines Cursors fest, der definiert, welche Datensätze in einer Tabelle für diesen Cursor sichtbar sind, und die Reihenfolge, in der sie angezeigt werden, indem der Satz von Indexeinträgen ausgewählt wird, die zum Verfügbar machen dieser Datensätze verwendet werden sollen.

```cpp
    JET_ERR JET_API JetSetCurrentIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*szIndexName*

Der Name des Indexes, der für den Cursor ausgewählt werden soll.

Wenn dieser Parameter NULL oder eine leere Zeichenfolge ist, wird der gruppierte Index ausgewählt. Wenn ein primärer Index für die Tabelle definiert ist, wird dieser Index ausgewählt, da er mit dem gruppierten Index identisch ist. Wenn kein primärer Index für die Tabelle definiert ist, wird der sequenzielle Index ausgewählt. Der sequenzielle Index verfügt über keine Indexdefinition. Weitere Informationen finden Sie unter [JetCreateIndex.](./jetcreateindex-function.md)

Wenn *pindexid* nicht NULL ist, wird der Indexname ignoriert, und der Index wird anhand seiner Index-ID ausgewählt.

*grbit*

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten, die null oder mehr der folgenden Elemente enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitMoveFirst</p> | <p>Diese Option gibt an, dass der Cursor auf dem ersten Eintrag des angegebenen Indexes positioniert werden soll. Wenn der gruppierte Index ausgewählt wird (Primärindex oder sequenzieller Index), und der aktuelle Index ein sekundärer Index ist, wird JET_bitMoveFirst angenommen. Wenn der aktuelle Index ausgewählt wird, wird diese Option ignoriert, und es wird keine Änderung an der Cursorposition vorgenommen.</p> | 
| <p>JET_bitNoMove</p> | <p>Diese Option gibt an, dass der Cursor auf dem Indexeintrag des neuen Index positioniert werden soll, der dem Datensatz entspricht, der dem Indexeintrag an der aktuellen Position des Cursors auf dem alten Index zugeordnet ist.</p><p>Wenn die Definition für den neuen Index mindestens eine mehrwertige Schlüsselspalte enthält, ist der Zielindexeintrag mehrdeutig. In diesem Fall wird die angegebene <em>itagSequence</em> verwendet, um auszuwählen, welcher Mehrwert der wichtigsten mehrwertigen Schlüsselspalte zum Positionieren des Cursors verwendet wird. Es ist nur erforderlich, auch bei mehreren mehrwertigen Schlüsselspalten eine einzelne <em>itagSequence</em> zu übergeben, da die Engine nur alle Werte für die wichtigste mehrwertige Schlüsselspalte erweitert. Weitere Informationen finden Sie unter <a href="gg294099(v=exchg.10).md">JetCreateIndex.</a></p><p>Wenn JET_bitMoveFirst angegeben wird, wird diese Option ignoriert.</p><p>Wenn der aktuelle Index ausgewählt wird, wird diese Option ignoriert, und es wird keine Änderung an der Cursorposition vorgenommen. Wenn dieser Parameter nicht vorhanden ist, wird davon ausgegangen, dass sein Wert JET_bitMoveFirst ist.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBadItagSequence</p> | <p>Ein sekundärer Index wird mit der Option JET_bitNoMove ausgewählt, und es gibt keinen Wert für die erste mehrwertige Schlüsselspalte in der neuen Definition für den Index, der der angegebenen Sequenznummer entspricht.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidIndexId</p> | <p>Der Inhalt der Index-ID war ungültig oder abgelaufen und muss aktualisiert werden. Dies kann für <strong>JetSetCurrentIndex2</strong> passieren, wenn:</p><ul><li><p>pindexid– &gt; cbStruct hat nicht die erwartete Größe (Windows Server 2003 und höhere Versionen).</p></li><li><p>Die Engine wurde heruntergefahren, seit die Index-ID abgerufen wurde.</p></li><li><p>Alle Cursor, die auf die Tabelle verweisen, die den Index enthält, der der Index-ID entspricht, wurden geschlossen, und die Engine hat die Definition für den Index aus dem Schemacache entfernt.</p></li><li><p>Die Index-ID wird mit einem Cursor verwendet, der in der falschen Tabelle geöffnet ist.</p></li><li><p>Der Index wurde gelöscht oder ist noch nicht für die Sitzung sichtbar.</p></li></ul> | 
| <p>JET_errInvalidName</p> | <p>Einer der angegebenen Objektnamen war ungültig. Alle Objektnamen müssen demselben Satz von Regeln entsprechen. Nachfolgend sind diese Regeln aufgeführt:</p><ul><li><p>Objektnamen müssen aus ASCII-Zeichen bestehen.</p></li><li><p>Objektnamen müssen mindestens ein Zeichen lang sein.</p></li><li><p>Objektnamen dürfen JET_cbNameMost (64) Zeichen nicht überschreiten.</p></li><li><p>Objektnamen beginnen möglicherweise nicht mit einem Leerzeichen.</p></li><li><p>Objektnamen dürfen keine ASCII-Steuerzeichen enthalten (0x00 bis 0x1F).</p></li><li><p>Objektnamen dürfen kein Ausrufezeichen (!), einen Punkt (.), eine linke Klammer ([) oder eine rechte Klammer (]) enthalten.</p></li><li><p>Nach der Überprüfung wird nur der Teil der Zeichenfolge bis zum ersten Leerzeichen (sofern vorhanden) für den Objektnamen verwendet. Dies bedeutet, dass Objektnamen möglicherweise auch kein Leerzeichen enthalten.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann bei <strong>JetSetCurrentIndex2</strong> passieren, wenn <em>pindexid</em> nicht NULL und pindexid- &gt; cbStruct nicht die erwartete Größe hat (Windows XP und frühere Versionen).</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Ein sekundärer Index wird mit der Option JET_bitNoMove ausgewählt, und es gibt keinen Indexeintrag im neuen Index, der dem Datensatz entspricht, der dem Indexeintrag an der aktuellen Position des Cursors auf dem alten Index zugeordnet ist.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errOutOfCursors</p> | <p>Die Engine hat ihren Ressourcenpool zum Öffnen von Cursorn erschöpft. Die maximale Anzahl von Cursorn, die jederzeit geöffnet werden können, wird <a href="gg269201(v=exchg.10).md">mit</a>JET_paramMaxCursors gesteuert. Weitere Informationen finden Sie unter <a href="gg294044(v=exchg.10).md">JetSetSystemParameter.</a> Dies kann bei <strong>JetSetCurrentIndex2</strong> passieren, wenn ein sekundärer Index ausgewählt wurde und die Engine keinen internen Cursor öffnen kann, um diesen Index zu verwenden.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden.</p><p>Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird der aktuelle Index des Cursors auf den angeforderten Index festgelegt. Indexeinträge können jetzt mit [JetSeek](./jetseek-function.md) gemäß der Indexdefinition des angeforderten Index gesucht werden. Indexeinträge können auch mitHilfe von [JetMove](./jetmove-function.md) in der von dieser Indexdefinition angegebenen Reihenfolge aufzählt werden. Die aktuelle Position des Cursors wird entweder auf den ersten Indexeintrag im Index (JET_bitMoveFirst) oder auf einen bestimmten Indexeintrag festgelegt, der mit der aktuellen Position des Cursors auf dem alten Index verknüpft ist (JET_bitNoMove). Es erfolgt keine Änderung des Datenbankzustands.

Bei einem Fehler befinden sich der aktuelle Index und die aktuelle Position des Cursors in einem nicht definierten Zustand. Es erfolgt keine Änderung des Datenbankzustands.

#### <a name="remarks"></a>Hinweise

Wenn der Index-ID-Hinweis veraltet ist, schlägt die API einfach fehl. Es gibt in diesem Fall keinen Fallback auf den Textnamen des Indexes, wie man erwarten könnte. Dieser Fallback muss manuell vom Aufrufer der API durchgeführt werden.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetSetCurrentIndex2W</strong> (Unicode) und <strong>JetSetCurrentIndex2A</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetGetCurrentIndex](./jetgetcurrentindex-function.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetMove](./jetmove-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetSeek](./jetseek-function.md)  
[JetStopService](./jetstopservice-function.md)
