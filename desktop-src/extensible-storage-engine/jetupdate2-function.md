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
ms.openlocfilehash: 34cc43aea463c186d68c0fa0cadc447ba2a02acb
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983243"
---
# <a name="jetupdate2-function"></a>JetUpdate2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetupdate2-function"></a>JetUpdate2-Funktion

Die **JetUpdate2-Funktion** führt einen Aktualisierungsvorgang aus, einschließlich einfügen einer neuen Zeile in eine Tabelle oder Aktualisieren einer vorhandenen Zeile. Diese Funktion enthält eine Liste von *Grbitoptionen,* die beim Ausführen eines Updates festgelegt werden können. Das Löschen einer Tabellenzeile erfolgt durch Aufrufen von [JetDelete.](./jetdelete-function.md)

**Windows Server 2003: JetUpdate2** wird in Windows Server 2003 eingeführt.

**JetUpdate2** ist der letzte Schritt beim Ausführen einer Einfügung oder eines Updates. Das Update wird gestartet, indem [JetPrepareUpdate](./jetprepareupdate-function.md) aufgerufen und [jetSetColumns](./jetsetcolumn-function.md) oder [JetSetColumns](./jetsetcolumns-function.md) einmal oder mehrmals aufgerufen wird, um den Datensatzzustand festzulegen. Schließlich wird **JetUpdate2** aufgerufen, um den Updatevorgang abzuschließen. Indizes werden nur von [JetUpdate](./jetupdate-function.md) oder **JetUpdate2** und nicht während [JetSetColumns](./jetsetcolumn-function.md) oder [JetSetColumns](./jetsetcolumns-function.md)aktualisiert.

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

Größe des Puffers, auf den *von pvBookmark* gezeigt wird.

*actual*

Die zurückgegebene Größe des Lesezeichens für die eingefügte Zeile, die in *pvBookmark* zurückgegeben wird.

*grbit*

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten, die 0 (null) oder mehr der folgenden Elemente enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitUpdateCheckESE97Compatibility</p> | <p>Dieses Flag bewirkt, dass das Update einen Fehler zurückgibt, wenn das Update in der Windows 2000-Version von ESE nicht möglich gewesen wäre, die eine kleinere maximale Anzahl von mehrwertigen Spalteninstanzen in jedem Datensatz erzwungen hat als höhere Versionen von ESE. Dies ist nur für Anwendungen wichtig, die Daten zwischen Anwendungen replizieren möchten, die auf Windows 2000 gehostet werden, und Anwendungen, die auf Windows Server 2003 oder höher von ESE gehostet werden. Dies sollte für die meisten Anwendungen nicht erforderlich sein.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Der angegebene Puffer für das Datensatzlesezeichen ist nicht groß genug, um das Datensatzlesezeichen zu speichern.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errDiskFull</p> | <p>Der Aktualisierungsvorgang erfordert eine Vergrößerung der Datenbankdatei oder eine Protokolldateizuordnung, aber das Laufwerk, auf dem sich die Datenbankdatei oder Protokollreihe befindet, ist voll. Alternativ befindet sich die Datenbankdatei auf einem FAT32-formatierten Volume, und die Datenbankdatei ist bereits auf 4 GB festgelegt. Dies ist der Grenzwert pro Datei für FAT32.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
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
| <p>JET_errUpdateNotPrepared</p> | <p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> wurde mit JET_prepCancel aufgerufen, aber der Cursor befand sich nicht im vorbereiteten Zustand.</p> | 
| <p>JET_errWriteConflict</p> | <p>Ein Datensatzersetzungsvorgang, für den noch keine Schreibsperre zugeordnet wurde, kann zum Zeitpunkt der Aktualisierung auf einen Schreibkonflikt stoßen.</p> | 



Bei Erfolg wird der Vorgang zum Öffnen des Updates für den Cursor abgeschlossen. Wenn für die Tabelle eine Spalte mit automatischem Inkrement definiert ist, wird dieser Wert für eingefügte Datensätze festgelegt. Wenn eine Versionsspalte für die Tabelle definiert ist, wird ihr Wert für neu eingefügte Datensätze initialisiert oder jedes Mal erhöht, wenn ein Datensatz ersetzt wird. Alle Indizes, einschließlich gruppierter und nicht gruppierter Indizes, werden aktualisiert.

Bei einem Fehler werden keineRlei Änderungen an der Datenbank vorgenommen. Vor dem Einfügen und vor dem Ersetzen wurden möglicherweise Rückruffunktionen aufgerufen, aber nach dem Einfügen und nach dem Ersetzen wurden rückrufe nicht aufgerufen, da letzteres nicht dazu führen kann, dass ein Update fehlschlägt. Der Cursorkopierpuffer befindet sich im vorbereiteten Zustand, sodass die Möglichkeit besteht, die Probleme, die Fehler verursacht haben, inkrementell zu beheben und den Updatevorgang zu wiederholen.

#### <a name="remarks"></a>Bemerkungen

Einschränkungen der Datensatzgröße werden von [JetSetColumn](./jetsetcolumn-function.md)erzwungen, und nicht im Allgemeinen durch [JetUpdate.](./jetupdate-function.md) Die einzige Ausnahme ist, wenn das JET_bitUpdateCheckESE97Compatibility-Kompatibilitätsflag verwendet wird. In diesem Fall wird der gesamte Datensatz überprüft, da ein einzelner [JetSetColumn-Vorgang,](./jetsetcolumn-function.md) der den Grenzwert überschritten hat, durch einen nachfolgenden Aufruf von [JetSetColumn](./jetsetcolumn-function.md)kompensiert werden kann.

Weitere Informationen finden Sie im Abschnitt "Hinweise" in [JetUpdate.](./jetupdate-function.md)

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



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
