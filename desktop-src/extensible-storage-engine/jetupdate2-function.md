---
description: Weitere Informationen finden Sie unter JetUpdate2-Funktion.
title: JetUpdate2-Funktion
TOCTitle: JetUpdate2 Function
ms:assetid: 125f372c-9c4c-4be8-b0df-bbf53d79e90b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269190(v=EXCHG.10)
ms:contentKeyID: 32765493
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f85633a16077c3957bebb1e236f5bbca6180778a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479566"
---
# <a name="jetupdate2-function"></a>JetUpdate2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetupdate2-function"></a>JetUpdate2-Funktion

Die **JetUpdate2-Funktion** führt einen Aktualisierungsvorgang aus, einschließlich einfügen einer neuen Zeile in eine Tabelle oder Aktualisieren einer vorhandenen Zeile. Diese Funktion enthält eine Liste von *Grbit-Optionen,* die beim Ausführen eines Updates festgelegt werden können. Das Löschen einer Tabellenzeile erfolgt durch Aufrufen von [JetDelete.](./jetdelete-function.md)

**Windows Server 2003: JetUpdate2** wird in Windows Server 2003 eingeführt.

**JetUpdate2** ist der letzte Schritt beim Ausführen eines Einfüge- oder Aktualisierungsschritts. Das Update wird gestartet, indem [JetPrepareUpdate](./jetprepareupdate-function.md) und dann [JetSetColumn](./jetsetcolumn-function.md) oder [JetSetColumns](./jetsetcolumns-function.md) einmal oder mehrmals zum Festlegen des Datensatzstatus aufruft. Schließlich wird **JetUpdate2 aufgerufen,** um den Aktualisierungsvorgang abschließen zu können. Indizes werden nur von [JetUpdate](./jetupdate-function.md) oder **JetUpdate2** und nicht während [JetSetColumn oder](./jetsetcolumn-function.md) [JetSetColumns aktualisiert.](./jetsetcolumns-function.md)

```cpp
    JET_ERR JET_API JetUpdate2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual,
      __in            const JET_GRBIT grbit
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

Größe des Puffers, auf den *pvBookmark zeigt.*

*–actual*

Die zurückgegebene Größe des Lesezeichens für die eingefügte Zeile, die in *pvBookmark zurückgegeben wird.*

*grbit*

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten, die null oder mehr der folgenden Elemente enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitUpdateCheckESE97Compatibility</p> | <p>Dieses Flag bewirkt, dass das Update einen Fehler zurück gibt, wenn das Update in der Windows 2000-Version von ESE nicht möglich gewesen wäre, die eine geringere maximale Anzahl von mehrwertigen Spalteninstanzen in jedem Datensatz erzwungen hat als spätere Versionen von ESE. Dies ist nur für Anwendungen wichtig, die Daten zwischen anwendungen replizieren möchten, die auf Windows 2000 gehostet werden, und Anwendungen, die auf Windows Server 2003 oder höher von ESE gehostet werden. Dies sollte für die meisten Anwendungen nicht erforderlich sein.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Der puffer für das Datensatz-Lesezeichen ist nicht groß genug, um das Datensatz-Lesezeichen zu speichern.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errDiskFull</p> | <p>Für den Updatevorgang ist eine Vergrößerung der Datenbankdatei oder eine Protokolldateizuordnung erforderlich, aber das Laufwerk, auf dem sich die Datenbankdatei oder Protokollreihe befindet, ist voll. Alternativ befindet sich die Datenbankdatei auf einem FAT32-formatierten Volume, und die Datenbankdatei beträgt bereits 4 GB, das Limit pro Datei für FAT32.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong>  Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Der <em>angegebenen Prep-Parameter</em> in der <a href="gg269339(v=exchg.10).md">JetPrepareUpdate-Funktion</a> ist kein gültiges Flag.</p> | 
| <p>JET_errKeyDuplicate</p> | <p>Ein Indexschlüssel für diesen Datensatz ist ein Duplikat eines anderen Indexschlüssels für einen anderen Datensatz, der bereits in der Tabelle vorhanden ist, und der Index lässt keine Duplikate zu.</p> | 
| <p>JET_errKeyTruncated</p> | <p>Der eingefügte oder aktualisierte Datensatz verfügt über einen oder mehrere Indizes, für die der generierte Schlüssel die maximal zulässige Größe überschritten hätte. Daher konnte der Vorgang das Abschneiden von Schlüsseln nicht verhindern.</p> | 
| <p>JET_errMultiValuedIndexViolation</p> | <p>Der eingefügte oder aktualisierte Datensatz verfügt über eine indizierte Mehrwertspalte mit zwei oder mehr Werten, die innerhalb der für den Index festgelegten Schlüsselgröße mit maximaler Länge identisch sind. Daher verfügt der Datensatz über zwei identische Einträge im Index, die ungültig sind.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errNullInvalid</p> | <p>Mindestens eine Spalte im Datensatz, der eingefügt werden soll, oder im aktualisierten Zustand eines Datensatzes, der ersetzt wird, ist <strong>NULL,</strong> was gegen die definierte Einschränkung für diese Spalten verstößt.</p> | 
| <p>JET_errNullKeyDisallowed</p> | <p>Mindestens ein Index ist so definiert, dass kein <strong>NULL-Schlüssel</strong> zulässig ist, und der eingefügte oder aktualisierte Zustand eines Datensatzes, der ersetzt wird, verstößt gegen diese definierte Einschränkung.</p> | 
| <p>JET_errRecordPrimaryChanged</p> | <p>Bei einem Datensatzersetzungsvorgang wurde der Primärschlüssel aktualisiert. Aktualisierungen an Primärschlüsselspalten müssen durch Löschen des vorhandenen Datensatzes und Einfügen eines neuen Datensatzes mit den gewünschten Daten erfolgen.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden.</p><p><strong>Windows XP:</strong>  Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> wurde mit JET_prepCancel, aber der Cursor war nicht im vorbereiteten Zustand.</p> | 
| <p>JET_errWriteConflict</p> | <p>Bei einem Datensatzersetzungsvorgang, für den noch keine Schreibsperre zugeordnet wurde, kann zum Zeitpunkt der Aktualisierung ein Schreibkonflikt auftreten.</p> | 



Bei Erfolg wird der geöffnete Aktualisierungsvorgang für den Cursor abgeschlossen. Wenn für die Tabelle eine Spalte mit automatischer Inkrementerhöhung definiert ist, wird dieser Wert für eingefügte Datensätze festgelegt. Wenn eine Versionsspalte für die Tabelle definiert ist, wird ihr Wert für neu eingefügte Datensätze initialisiert oder jedes Mal erhöht, wenn ein Datensatz ersetzt wird. Alle Indizes, einschließlich gruppierter und nicht gruppierter Indizes, werden aktualisiert.

Bei einem Fehler werden keine Änderungen an der Datenbank vorgenommen. Vor dem Einfügen und vor dem Ersetzen wurden rückruffunktionen möglicherweise aufgerufen, aber nach dem Einfügen und nach dem Ersetzen wurden keine Rückrufe aufgerufen, da letzteres nicht dazu führen kann, dass ein Update fehlschlägt. Der Cursorkopierpuffer bleibt im vorbereiteten Zustand, sodass die Möglichkeit besteht, die Fehler inkrementell zu beheben und den Aktualisierungsvorgang zu wiederholen.

#### <a name="remarks"></a>Hinweise

Einschränkungen der Datensatzgröße werden von [JetSetColumn](./jetsetcolumn-function.md)und nicht im Allgemeinen von [JetUpdate erzwungen.](./jetupdate-function.md) Die einzige Ausnahme ist, wenn das JET_bitUpdateCheckESE97Compatibility-Kompatibilitätsflag verwendet wird. In diesem Fall wird der gesamte Datensatz überprüft, da ein einzelner [JetSetColumn-Vorgang,](./jetsetcolumn-function.md) der den Grenzwert überschritten hat, durch einen nachfolgenden Aufruf von [JetSetColumn ausgeglichen werden kann.](./jetsetcolumn-function.md)

Weitere Informationen finden Sie im Abschnitt "Hinweise" in [JetUpdate.](./jetupdate-function.md)

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



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
