---
description: 'Weitere Informationen zu: JetSetColumns-Funktion'
title: JetSetColumns-Funktion
TOCTitle: JetSetColumns Function
ms:assetid: a5b011dc-0da6-44bf-aaf5-352d8a57e5bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294050(v=EXCHG.10)
ms:contentKeyID: 32765649
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumns
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4cf9639ded8774be2b46c3a62bc97c6b56b9f15e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465667"
---
# <a name="jetsetcolumns-function"></a>JetSetColumns-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetcolumns-function"></a>JetSetColumns-Funktion

Die **JetSetColumns-Funktion** ähnelt dem Verhalten von [JetSetColumn,](./jetsetcolumn-function.md) ermöglicht einer Anwendung jedoch das Festlegen mehrerer Spaltenwerte in einem einzelnen Vorgang. Ein Array von [JET_SETCOLUMN](./jet-setcolumn-structure.md) Strukturen wird verwendet, um den Satz der festzulegenden Spaltenwerte und eingabepuffer für jeden festzulegenden Spaltenwert zu beschreiben.

```cpp
    JET_ERR JET_API JetSetColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_SETCOLUMN* psetcolumn,
      __in          unsigned long csetcolumn
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*psetcolumn*

Ein Zeiger auf ein Array einer oder mehrerer [JET_SETCOLUMN](./jet-setcolumn-structure.md) Strukturen. Jede Struktur enthält Beschreibungen darüber, welcher Spaltenwert festgelegt werden soll und von wo aus die festzulegenden Spaltendaten abzurufen sind.

*csetcolumn*

Die Anzahl der [JET_SETCOLUMN](./jet-setcolumn-structure.md) Strukturen im Array, die von *psetcolumn* angegeben werden.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errBadColumnId</p> | <p>Die angegebene Spalten-ID liegt außerhalb der rechtlichen Grenzen einer Spalten-ID.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errColumnIllegalNull</p> | <p>Entspricht JET_errNullInvalid.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Die von der angegebenen <em>columnid</em> beschriebene Spalte ist in der Tabelle nicht vorhanden.</p> | 
| <p>JET_errColumnNotUpdatable</p> | <p>Es wurde ein unzulässiger Versuch unternommen, einen long-Wert während eines ursprünglichen Aktualisierungsvorgangs zum Löschen eines Einfügekopiervorgangs zu aktualisieren.</p> | 
| <p>JET_errColumnTooBig</p> | <p>Die angegebenen Spaltenwertdaten, die im Eingabepuffer angegeben werden, überschreiten die Größenbeschränkung , entweder natürlich für eine Spalte fester Länge oder konfiguriert für Text mit fester Länge oder binäre Spalten. Dieser Fehler wird auch zurückgegeben, wenn für eine lange Spalte mehr als 1.024 Byte an Daten übergeben und das flag JET_bitSetIntrinsicLV festgelegt wird.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Die Datengröße des angegebenen Spaltenwerts stimmt nicht mit der natürlichen Größe des Datentyps mit fester Länge überein.</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Es wurde ein unzulässiger Versuch unternommen, eine Spalte für automatische Inkremente entweder während eines Einfüge- oder Aktualisierungsvorgangs oder während eines Ersetzungsvorgangs zu aktualisieren.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Die angegebenen Optionen sind unbekannt oder eine unzulässige Kombination bekannter Biteinstellungen.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Die angegebene psetinfo- &gt; cbStruct ist keine gültige Größe für die <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> Struktur.</p> | 
| <p>JET_errMultiValuedDuplicate</p> | <p>Der Vorgang zum Festlegen der Spalte hat versucht, einen doppelten Wert zu erstellen, und es wurde entweder JET_bitSetUniqueMultiValues oder JET_bitSetUniqueNormalizedMultiValues angegeben.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errNotInTransaction</p> | <p>Es wurde ein unzulässiger Versuch unternommen, einen long-Spaltenwert zu aktualisieren, wenn sich die aufrufende Sitzung nicht in einer Transaktion befand.</p> | 
| <p>JET_errNullInvalid</p> | <p>Es wurde ein unzulässiger Versuch unternommen, eine Spalte ungleich NULL auf NULL festzulegen.</p> | 
| <p>JET_errRecordTooBig</p> | <p>Der Spaltenwert konnte nicht auf den Wert im Eingabepuffer festgelegt werden, da er dazu geführt hätte, dass der Datensatz die Größenbeschränkung der Seite überschreitet. Spalten vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> können getrennt von den verbleibenden Datensatzdaten gespeichert werden. Andere Spalten müssen jedoch mit dem Datensatz gespeichert werden und können dazu führen, dass die Größenbeschränkung des Datensatzes überschritten wird. Selbst lange Spalten benötigen 5 Bytes Speicherplatz innerhalb des Datensatzes als Verknüpfung. Dies kann auch dazu führen, dass JET_errRecordTooBig zurückgegeben wird.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p>Der Cursor ist derzeit nicht dabei, entweder einen neuen Datensatz einzufügen oder einen vorhandenen Datensatz zu aktualisieren.</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>Der Spaltenwert im Eingabepuffer hat die maximal konfigurierte Länge für eine Spalte variabler Länge überschritten und wurde abgeschnitten.</p> | 



Bei Erfolg wird für jede in den Spalten beschriebene Spalte der gewünschte Teil des Spaltenwerts mit Daten festgelegt, die aus dem Eingabepuffer kopiert werden. Das Spaltendatensatz wurde möglicherweise abgeschnitten, wenn es die für eine Spalte variable Länge angegebene maximale Länge überschritten hat.

Bei einem Fehler bleibt die Cursorposition unverändert, und im Kopierpuffer werden keine Spaltenwertdaten aktualisiert.

#### <a name="remarks"></a>Hinweise

Wenn ein einzelner Set Column-Vorgang einen Fehler zurückgibt, gibt der gesamte **JetSetColumns-Vorgang** einen Fehler zurück. Warnungen werden im Allgemeinen in psetcolumns- error und \> nicht im Rückgabecode dieser Funktion zurückgegeben. Wenn der letzte Spaltensatz jedoch eine Warnung enthält, wird diese Warnung von **JetSetColumns** selbst zurückgegeben.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SETCOLUMN](./jet-setcolumn-structure.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
