---
description: 'Weitere Informationen zu: JetUpdate-Funktion'
title: JetUpdate-Funktion
TOCTitle: JetUpdate Function
ms:assetid: 6c9a53d0-46bc-403b-bdba-9020e023c14a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269288(v=EXCHG.10)
ms:contentKeyID: 32765580
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e02550fb40987906e21d588263daed9dc68aa5d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478246"
---
# <a name="jetupdate-function"></a>JetUpdate-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetupdate-function"></a>JetUpdate-Funktion

Die **JetUpdate-Funktion** führt einen Aktualisierungsvorgang aus, einschließlich einfügen einer neuen Zeile in eine Tabelle oder Aktualisieren einer vorhandenen Zeile. Das Löschen einer Tabellenzeile erfolgt durch Aufrufen von [JetDelete.](./jetdelete-function.md)

**JetUpdate** ist der letzte Schritt beim Ausführen eines Einfüge- oder Aktualisierungsschritts. Das Update wird gestartet, indem [JetPrepareUpdate](./jetprepareupdate-function.md) und dann [jetSetColumns](./jetsetcolumn-function.md) oder [JetSetColumns](./jetsetcolumns-function.md) einmal oder mehrmals aufgerufen werden, um den Datensatzzustand festzulegen. Schließlich wird **JetUpdate** aufgerufen, um den Updatevorgang abzuschließen. Indizes werden nur von **JetUpdate** oder [JetUpdate2](./jetupdate2-function.md)und nicht während [JetSetColumns](./jetsetcolumn-function.md) oder [JetSetColumns](./jetsetcolumns-function.md)aktualisiert.

```cpp
    JET_ERR JET_API JetUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*pvBookmark*

Zeiger auf ein zurückgegebenes Lesezeichen für eine eingefügte Zeile.

*cbBookmark*

Größe des Puffers, auf den *von pvBookmark* gezeigt wird.

*actual*

Die zurückgegebene Größe des Lesezeichens für die eingefügte Zeile, die in *pvBookmark* zurückgegeben wird.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Der angegebene Puffer für das Datensatzlesezeichen ist nicht groß genug, um das Datensatzlesezeichen zu speichern.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errColumnIllegalNull</p> | <p>Entspricht JET_errNullInvalid.</p> | 
| <p>JET_errDiskFull</p> | <p>Der Aktualisierungsvorgang erfordert eine Vergrößerung der Datenbankdatei oder eine Protokolldateizuordnung, aber das Laufwerk, auf dem sich die Datenbankdatei oder Protokollreihe befindet, ist voll. Alternativ befindet sich die Datenbankdatei auf einem FAT32-formatierten Volume, und die Datenbankdatei ist bereits auf 4 GB festgelegt. Dies ist der Grenzwert pro Datei für FAT32.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Der angegebene <em>prep-Parameter</em> in der <a href="gg269339(v=exchg.10).md">JetPrepareUpdate-Funktion</a> ist kein gültiges Flag.</p> | 
| <p>JET_errKeyDuplicate</p> | <p>Ein Indexschlüssel für diesen Datensatz ist ein Duplikat eines anderen Indexschlüssels für einen anderen Datensatz, der sich bereits in der Tabelle befindet, und der Index lässt keine Duplikate zu.</p> | 
| <p>JET_errKeyTruncated</p> | <p>Der eingefügte oder aktualisierte Datensatz verfügt über einen oder mehrere Indizes, für die der generierte Schlüssel die maximal zulässige Größe überschritten hätte. Daher konnte der Vorgang das Abschneiden von Schlüsseln nicht verhindern.</p> | 
| <p>JET_errMultiValuedIndexViolation</p> | <p>Der eingefügte oder aktualisierte Datensatz verfügt über eine indizierte Mehrwertspalte mit zwei oder mehr Werten, die innerhalb der für den Index festgelegten Schlüsselgröße der maximalen Länge identisch sind. Daher weist der Datensatz zwei identische Einträge im Index auf, die ungültig sind.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errNullInvalid</p> | <p>Mindestens eine Spalte im einzufügenden Datensatz oder im aktualisierten Zustand eines zu ersetzenden Datensatzes ist <strong>NULL,</strong> was gegen die definierte Einschränkung für diese Spalten verstößt.</p> | 
| <p>JET_errNullKeyDisallowed</p> | <p>Mindestens ein Index ist so definiert, dass kein <strong>NULL-Schlüssel</strong> zulässig ist, und der eingefügte oder aktualisierte Zustand eines ersetzten Datensatzes verstößt gegen diese definierte Einschränkung.</p> | 
| <p>JET_errRecordPrimaryChanged</p> | <p>Durch einen Datensatzersetzungsvorgang wurde der Primärschlüssel aktualisiert. Aktualisierungen an Primärschlüsselspalten müssen durch Löschen des vorhandenen Datensatzes und Einfügen eines neuen Datensatzes mit den gewünschten Daten erfolgen.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden.</p><p><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Es ist unzulässig, ein Update zu versuchen, wenn es sich innerhalb des Bereichs einer schreibgeschützten Transaktion befindet. Eine schreibgeschützte Transaktion ist eine Transaktion, die mithilfe eines Aufrufs von <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> mit JET_bitTransactionReadOnly gestartet wurde.</p><p><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> wurde mit JET_prepCancel aufgerufen, aber der Cursor befand sich nicht im vorbereiteten Zustand.</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>Fehler beim Vorgang, weil nicht genügend Arbeitsspeicher vorhanden ist, um Transaktionsinformationen zum Update beizubehalten.</p> | 
| <p>JET_errWriteConflict</p> | <p>In einer anderen Sitzung wurde der Datensatz zuvor für das Update gesperrt. Das von dieser Sitzung versuchten Update schlägt fehl.</p> | 



Bei Erfolg wird der Vorgang zum Öffnen des Updates für den Cursor abgeschlossen. Wenn für die Tabelle eine Spalte mit automatischem Inkrement definiert ist, wird dieser Wert für eingefügte Datensätze festgelegt. Wenn eine Versionsspalte für die Tabelle definiert ist, wird ihr Wert für neu eingefügte Datensätze initialisiert oder jedes Mal erhöht, wenn ein Datensatz ersetzt wird. Alle Indizes, einschließlich gruppierter und nicht gruppierter Indizes, werden aktualisiert.

Bei einem Fehler werden keineRlei Änderungen an der Datenbank vorgenommen. Vor dem Einfügen und vor dem Ersetzen wurden möglicherweise Rückruffunktionen aufgerufen, aber nach dem Einfügen und nach dem Ersetzen wurden rückrufe nicht aufgerufen, da letzteres nicht dazu führen kann, dass ein Update fehlschlägt. Der Cursorkopierpuffer befindet sich im vorbereiteten Zustand, sodass die Möglichkeit besteht, die Probleme, die Fehler verursacht haben, inkrementell zu beheben und den Updatevorgang zu wiederholen.

#### <a name="remarks"></a>Hinweise

Rückruffunktionen können registriert werden, um vor oder nach dem Einfügen und vor oder nach dem Update aufgerufen zu werden.

Einschränkungen der Datensatzgröße werden von [JetSetColumn](./jetsetcolumn-function.md)erzwungen, nicht im Allgemeinen durch **JetUpdate.**

Es ist wichtig, die Auswirkungen einer großen Anzahl von Updatevorgängen innerhalb einer einzelnen Transaktion zu verstehen. Jedes Update der Datenbank muss von der Datenbank-Engine im Versionsspeicher nachverfolgt werden. Der Versionsspeicher enthält einen Livedatensatz aller verschiedenen Versionen jedes Datensatzes oder Indexeintrags in der Datenbank, der von allen aktiven Transaktionen angezeigt werden kann. Diese Versionen werden verwendet, um die parallele Steuerung mit mehreren Versionen zu unterstützen, die von der Datenbank-Engine verwendet wird, um Transaktionen mit Momentaufnahmeisolation zu unterstützen. Sobald die Datenbank-Engine die Zum Speichern dieser Versionen verwendeten Ressourcen erschöpft hat, kann sie keine weiteren Änderungen mehr akzeptieren, bis einige Transaktionen abgeschlossen sind, um die Wiederverwendung dieser Ressourcen zu ermöglichen. Wenn sich die Engine in diesem Zustand befindet, schlagen alle Updates mit JET_errVersionStoreOutOfMemory fehl. Die ressourcen, die der Datenbank-Engine zum Speichern dieser Versionen zur Verfügung stehen, können mit [JetSetSystemParameter](./jetsetsystemparameter-function.md) mit [JET_paramMaxVerPages](./resource-parameters.md) und [JET_paramGlobalMinVerPages](./resource-parameters.md)gesteuert werden.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDelete](./jetdelete-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetRegisterCallback](./jetregistercallback-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
