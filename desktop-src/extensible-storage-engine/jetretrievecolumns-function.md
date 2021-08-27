---
description: Weitere Informationen finden Sie unter JetRetrieveColumns-Funktion.
title: JetRetrieveColumns-Funktion
TOCTitle: JetRetrieveColumns Function
ms:assetid: f7158fe8-ba4b-420c-9d45-185791a5759b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294135(v=EXCHG.10)
ms:contentKeyID: 32765749
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad6e1d39797c9a9ff965644ceea7858cb4af1a56
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472496"
---
# <a name="jetretrievecolumns-function"></a>JetRetrieveColumns-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetretrievecolumns-function"></a>JetRetrieveColumns-Funktion

Die **JetRetrieveColumns-Funktion** ruft mehrere Spaltenwerte aus dem aktuellen Datensatz in einem einzigen Vorgang ab. Ein Array [von JET_RETRIEVECOLUMN-Strukturen](./jet-retrievecolumn-structure.md) wird verwendet, um den Satz der abzurufenden Spaltenwerte zu beschreiben und Ausgabepuffer für jeden abzurufenden Spaltenwert zu beschreiben.

```cpp
    JET_ERR JET_API JetRetrieveColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_RETRIEVECOLUMN* pretrievecolumn,
      __in          unsigned long cretrievecolumn
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*pretrivorgecolumn*

Ein Zeiger auf ein Array von einer oder JET_RETRIEVECOLUMN [Strukturen.](./jet-retrievecolumn-structure.md) Jede Struktur enthält Beschreibungen, welcher Spaltenwert abgerufen werden soll und wo zurückgegebene Daten gespeichert werden.

*cretriredocolumn*

Die Anzahl der [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) Strukturen im Array, die von *pretrivorgefertigtcolumn angegeben werden.*

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBadItagSequence</p> | <p>In pretinfo- itagSequence wurde ein ungültiger Wert für eine mehrwertige &gt; Spaltensequenznummer übergeben. Gültige Werte für die Sequenznummern für mehrwertige Spaltenwerte sind 1 oder höher. Der Wert 0 (null) ist für diese Funktion gültig, aber für <a href="gg269198(v=exchg.10).md">JetRetrieveColumn ungültig.</a></p> | 
| <p>JET_errBadColumnId</p> | <p>Die angegebenen Spalten-IDs liegen außerhalb der rechtlichen Grenzen einer Spalten-ID.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errColumnNotFound</p> | <p>Die von der angegebenen <em>columnid beschriebene</em> Spalte ist in der Tabelle nicht vorhanden.</p> | 
| <p>JET_errIndexTuplesCannotRetrieveFromIndex</p> | <p>Als Teilzeichenfolgen indizierte Spalten können nicht aus dem Index abgerufen werden, da in der Regel nur ein kleiner Teil der Spalte in jedem Indexeintrag vorhanden ist.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>In einigen Fällen muss der puffer, der für die Abrufspalte angegeben wird, ausreichend groß sein, um eine beliebige Menge des Spaltenwerts zurückgeben zu können. Beispielsweise werden veraltete Spalten so angepasst, dass sie für den Transaktionskontext der aufrufenden Sitzung konsistent sind. Für diese Anpassung ist der vom Aufrufer bereitgestellte Puffer erforderlich. Wenn nicht genügend Pufferspeicher bereitgestellt wird, wird JET_errInvalidBufferSize zurückgegeben, und es werden keine Spaltendaten zurückgegeben.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Die angegebenen Optionen sind unbekannt oder eine unzulässige Kombination bekannter Biteinstellungen.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Mindestens einer der angegebenen Parameter ist falsch. Dies kann passieren, wenn retinfo.cbStruct kleiner als die Größe von <a href="gg294049(v=exchg.10).md">JET_RETINFO.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong>  Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Der Cursor ist nicht auf einem Datensatz positioniert. Dafür sind viele verschiedene Gründe möglich. Dies geschieht beispielsweise, wenn der Cursor derzeit nach dem letzten Datensatz im aktuellen Index positioniert ist.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden.</p><p><strong>Windows XP:</strong>  Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>Der gesamte Spaltenwert konnte nicht abgerufen werden, da der gegebene Puffer kleiner als die Größe der Spalte ist.</p> | 



Bei Erfolg werden Die Spaltendaten und die Spaltengröße in bereitgestellten Puffern zurückgegeben, die unter Array von JET_RETRIEVECOLUMN [werden.](./jet-retrievecolumn-structure.md) Wenn *eine itagSequence* auf 0 (null) festgelegt wurde, um anzugeben, dass die Anzahl der Instanzen eines mehrwertigen Felds anstelle von Spaltendaten gewünscht wurde, wird die Anzahl der Instanzen einer mehrwertigen Spalte im *itagSequence-Feld* selbst zurückgegeben. Jede [JET_RETRIEVECOLUMN-Struktur](./jet-retrievecolumn-structure.md) verfügt über ein Fehlerfeld, das Warnungen für die abgerufene Spalte enthält. Wenn die Spalte **nullwertig** war, wird der Fehlercode auf JET_wrnColumnNull.

Bei einem Fehler bleibt die Cursorposition unverändert, und es werden keine Daten in den bereitgestellten Puffer kopiert.

#### <a name="remarks"></a>Hinweise

**JetRetrieveColumns unterstützt** ein Feature, das [JetRetrieveColumn nicht](./jetretrievecolumn-function.md) unterstützt. Dies ist die Möglichkeit, die Anzahl der Instanzen einer mehrwertigen Spalte abzurufen. Der Zweck dieses Features besteht im Zulassen, dass eine Anwendung alle Werte einer Spalte abruft. Dies kann erfolgen, indem zuerst die Anzahl der Werte bestimmt wird, über die eine Spalte verfügt. Als Nächstes können ihre Längen durch einen erneuten Aufruf von **JetRetrivorColumns** mit einer [JET_RETRIEVECOLUMN-Struktur](./jet-retrievecolumn-structure.md) bestimmt werden, die für jeden Wert zugeordnet ist, um die Länge der Spaltendaten zu bestimmen. Dies kann erreicht werden, indem _NULL-pvData-Zeiger_ mit *cbMax* von 0 (null) übergeben und die Spaltenlänge in *cbActual abgerufen wird.* Der dritte und letzte Aufruf kann mit zugeordneter Arbeitsspeicher für die Spaltenwertdaten vorgenommen werden.

Wenn eine abgerufene Spalte aufgrund eines Puffers mit unzureichender Länge abgeschnitten wird, gibt die API JET_wrnBufferTruncated. Andere Fehler, JET_wrnColumnNull werden jedoch nur im Fehlerfeld [in](./jet-retrievecolumn-structure.md)JET_RETRIEVECOLUMN. Der Grund dafür ist, dass Anwendungen häufig sicherstellen möchten, dass alle Daten abgerufen wurden, und die Rückgabe dieses Fehlers von **JetRetrieveColumns** erleichtert dieses Verständnis.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
