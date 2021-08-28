---
description: 'Weitere Informationen finden Sie unter: JetRetrieveColumn-Funktion'
title: JetRetrieveColumn-Funktion
TOCTitle: JetRetrieveColumn Function
ms:assetid: 1e55063f-6033-4416-a9a6-894032fed069
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269198(v=EXCHG.10)
ms:contentKeyID: 32765501
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f8a9ce96be028329dea18f32459fbde88b80b75f
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985623"
---
# <a name="jetretrievecolumn-function"></a>JetRetrieveColumn-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetretrievecolumn-function"></a>JetRetrieveColumn-Funktion

Die **JetRetrieveColumn-Funktion** ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist. Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursorkopierpuffer erstellt wird. Diese Funktion kann auch Spaltendaten aus einem Indexeintrag abrufen, der auf den aktuellen Datensatz verweist. Zusätzlich zum Abrufen des tatsächlichen Spaltenwerts kann **JetRetrieveColumn** auch verwendet werden, um die Größe einer Spalte abzurufen, bevor die Spaltendaten selbst abgerufen werden, damit die Größe der Anwendungspuffer entsprechend angepasst werden kann.

```cpp
    JET_ERR JET_API JetRetrieveColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __out_opt     void* pvData,
      __in          unsigned long cbData,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit,
      __in_out_opt  JET_RETINFO* pretinfo
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*Columnid*

Die [JET_COLUMNID](./jet-columnid.md) der abzurufenden Spalte.

Es *kann ein columnid-Wert* von 0 (null) angegeben werden, der selbst nicht auf eine einzelne Spalte bezieht. Wenn *columnid* 0 (null) angegeben wird, werden alle markierten Spalten, Sparsespalten und mehrwertigen Spalten als eine einzelne Spalte behandelt. Dies erleichtert das Abrufen aller Sparsespalten, die in einem Datensatz vorhanden sind.

*pvData*

Der Ausgabepuffer, der den Spaltenwert empfängt.

*cbData*

Die maximale Größe des Ausgabepuffers in Bytes.

*–actual*

Empfängt die tatsächliche Größe des Spaltenwerts in Bytes.

Wenn dieser Parameter **NULL ist,** wird die tatsächliche Größe des Spaltenwerts nicht zurückgegeben.

*grbit*

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten, die null oder mehr der folgenden Elemente enthalten:


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitRetrieveCopy</p> | <p>Dieses Flag bewirkt, dass die Abrufspalte den geänderten Wert anstelle des ursprünglichen Werts abruft. Wenn der Wert nicht geändert wurde, wird der ursprüngliche Wert abgerufen. Auf diese Weise kann ein Wert, der noch nicht eingefügt oder aktualisiert wurde, während des Einfügens oder Aktualisierens eines Datensatzes abgerufen werden.</p> | 
| <p>JET_bitRetrieveFromIndex</p> | <p>Diese Option wird verwendet, um Spaltenwerte möglichst ohne Zugriff auf den Datensatz aus dem Index abzurufen. Auf diese Weise kann unnötiges Laden von Datensätzen vermieden werden, wenn die benötigten Daten über Indexeinträge selbst verfügbar sind. In Fällen, in denen der ursprüngliche Spaltenwert aufgrund von nicht rückgängig gemachten Transformationen oder Datenschneidungen nicht aus dem Index abgerufen werden kann, wird auf den Datensatz zugegriffen, und die Daten werden wie gewohnt abgerufen. Dies ist eine Leistungsoption und sollte nur angegeben werden, wenn der Spaltenwert wahrscheinlich aus dem Index abgerufen werden kann. Diese Option sollte nicht angegeben werden, wenn der aktuelle Index der gruppierte Index ist, da die Indexeinträge für den gruppierten oder primären Index die Datensätze selbst sind. Dieses Bit kann nicht festgelegt werden, wenn JET_bitRetrieveFromPrimaryBookmark auch festgelegt ist.</p> | 
| <p>JET_bitRetrieveFromPrimaryBookmark</p> | <p>Diese Option wird verwendet, um Spaltenwerte aus dem Index-Lesezeichen abzurufen, und kann sich vom Indexwert unterscheiden, wenn eine Spalte sowohl im primären als auch im aktuellen Index angezeigt wird. Diese Option sollte nicht angegeben werden, wenn der aktuelle Index der gruppierte oder primäre Index ist. Dieses Bit kann nicht festgelegt werden, wenn JET_bitRetrieveFromIndex auch festgelegt ist.</p> | 
| <p>JET_bitRetrieveTag</p> | <p>Diese Option wird verwendet, um die Sequenznummer eines mehrwertigen Spaltenwerts in pretinfo- &gt; itagSequence abzurufen. Das itagSequence-Feld ist in der Regel eine Eingabe zum Abrufen von mehrwertigen Spaltenwerten aus einem Datensatz. Beim Abrufen von Werten aus einem Index ist es jedoch auch möglich, den Indexeintrag einer bestimmten Sequenznummer zu zuordnen und diese Sequenznummer abzurufen. Das Abrufen der Sequenznummer kann ein kostspieliger Vorgang sein und sollte nur bei Bedarf erfolgen.</p> | 
| <p>JET_bitRetrieveNull</p> | <p>Diese Option wird verwendet, um wertewertige <strong>Spalten-NULL-Werte</strong> abzurufen. Wenn diese Option nicht angegeben wird, werden die <strong>NULL-Werte</strong> der mehrwertigen Spalte automatisch übersprungen.</p> | 
| <p>JET_bitRetrieveIgnoreDefault</p> | <p>Diese Option wirkt sich nur auf mehrwertige Spalten aus und bewirkt, dass ein <strong>NULL-Wert</strong> zurückgegeben wird, wenn die angeforderte Sequenznummer 1 ist und keine festgelegten Werte für die Spalte im Datensatz enthalten sind.</p> | 
| <p>JET_bitRetrieveLongId</p> | <p>Dieses Flag ist nur für die interne Verwendung vorgesehen und nicht für die Verwendung in Ihrer Anwendung vorgesehen.</p> | 
| <p>JET_bitRetrieveLongValueRefCount</p> | <p>Dieses Flag ist nur für die interne Verwendung vorgesehen und nicht für die Verwendung in Ihrer Anwendung vorgesehen.</p> | 
| <p>JET_bitRetrieveTuple</p> | <p>Dieses Flag ermöglicht das Abrufen eines Tupelsegments des Indexes. Dieses Bit muss mit dem JET_bitRetrieveFromIndex.</p> | 



*pretinfo*

Wenn *pretinfo* als **NULL** angegeben wird, verhält sich die Funktion so, als ob eine *ItagSequence* von 1 und *ein ibLongValue* von 0 (null) angegeben würden. Dies bewirkt, dass der Spaltenabruf den ersten Wert einer mehrwertigen Spalte abruft und lange Daten bei Offset 0 (null) abruft.

Dieser Parameter wird verwendet, um eine oder mehrere der folgenden Informationen zur Verfügung zu stellen:


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>ibLongValue</p> | <p>Gibt einen binären Offset in einen long-Spaltenwert zurück, wenn ein Teil eines Spaltenwerts abgerufen wird.</p> | 
| <p>itagSequence</p> | <p>Gibt die Sequenznummer des gewünschten mehrwertigen Spaltenwerts an. Beachten Sie, dass dieses Feld nur festgelegt wird, wenn die JET_bitRetrieveTag angegeben ist. Andernfalls ist sie unverändert.</p> | 
| <p>columnidNextTagged</p> | <p>Gibt die Spalten-ID des zurückgegebenen Spaltenwerts zurück, wenn alle markierten, sparse- und mehrwertigen Spalten abgerufen werden, indem <em>columnid von</em> 0 (null) übergeben wird.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBadColumnId</p> | <p>Die angegebenen Spalten-IDs liegen außerhalb der rechtlichen Grenzen einer Spalten-ID.</p> | 
| <p>JET_errBadItagSequence</p> | <p>In pretinfo- itagSequence wurde ein ungültiger Wert für eine mehrwertige &gt; Spaltensequenznummer übergeben. Gültige Werte für die Sequenznummern für mehrwertige Spaltenwerte sind 1 oder höher. Der Wert 0 (null) ist für diese Funktion ungültig.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errColumnNotFound</p> | <p>Die von der angegebenen <em>columnid beschriebene</em> Spalte ist in der Tabelle nicht vorhanden.</p> | 
| <p>JET_errIndexTuplesCannotRetrieveFromIndex</p> | <p>Als Teilzeichenfolgen indizierte Spalten können nicht aus dem Index abgerufen werden, da in der Regel nur ein kleiner Teil der Spalte in jedem Indexeintrag vorhanden ist.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>In einigen Fällen muss der für die Abrufspalte angegebene Puffer ausreichend groß sein, um eine beliebige Menge des Spaltenwerts zurückzugeben. Aktualisierbare Spalten werden beispielsweise so angepasst, dass sie für den Transaktionskontext der aufrufenden Sitzung konsistent sind, und diese Anpassung erfordert den vom Aufrufer bereitgestellten Puffer. Wenn nicht genügend Pufferspeicher bereitgestellt wird, wird JET_errInvalidBufferSize zurückgegeben, und es werden keine Spaltendaten zurückgegeben.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Mindestens einer der angegebenen Parameter ist falsch. Dies kann passieren, wenn retinfo.cbStruct kleiner als die Größe <a href="gg294049(v=exchg.10).md">von JET_RETINFO</a>ist.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Die angegebenen Optionen sind unbekannt oder eine unzulässige Kombination bekannter Biteinstellungen.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Der Cursor wird nicht auf einem Datensatz positioniert. Dafür sind viele verschiedene Gründe möglich. Dies geschieht beispielsweise, wenn der Cursor derzeit nach dem letzten Datensatz im aktuellen Index positioniert ist.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden.</p><p><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>Der gesamte Spaltenwert konnte nicht abgerufen werden, da der angegebene Puffer kleiner als die Größe der Spalte ist.</p> | 
| <p>JET_wrnColumnNull</p> | <p>Der abgerufene Spaltenwert ist <strong>NULL.</strong></p> | 



Bei Erfolg wird der Spaltenwert für die angegebene Spalte in den angegebenen Puffer kopiert. Weniger als der gesamte Spaltenwert wird mit der Warnung kopiert, JET_wrnBufferTruncated zurückgegeben wird. Wenn das *"actual"* angegeben wurde, wird die tatsächliche Größe des Spaltenwerts zurückgegeben. Beachten Sie, dass **NULL-Werte** die Länge 0 (null) haben und daher die zurückgegebene Größe auf 0 (null) festlegen. Wenn die abgerufene Spalte eine mehrwertige Spalte war und *pretinfo* angegeben wurde und JET_bitReturnTag als Option festgelegt wurde, wird die Sequenznummer des Spaltenwerts in pretinfo- \> itagSequence zurückgegeben.

Bei einem Fehler bleibt die Cursorposition unverändert, und es werden keine Daten in den bereitgestellten Puffer kopiert.

#### <a name="remarks"></a>Bemerkungen

Dieser Aufruf wird nur einmal verwendet, um Daten mit fester oder bekannter Größe für nicht mehrwertige Spalten abzurufen. Wenn Spaltendaten jedoch eine unbekannte Größe aufweisen, wird dieser Aufruf in der Regel zweimal verwendet. Sie wird zuerst aufgerufen, um die Größe der Daten zu bestimmen, damit sie den erforderlichen Speicherplatz zuordnen können. Anschließend wird derselbe Aufruf erneut durchgeführt, um die Spaltendaten abzurufen. Wenn die tatsächliche Anzahl von Werten unbekannt ist, da eine Spalte mehrwertige Werte enthält, wird der Aufruf in der Regel dreimal verwendet. Zuerst, um die Anzahl der Werte abzurufen, und dann zweimal mehr, um Speicher zuzuordnen und die tatsächlichen Daten abzurufen.

Das Abrufen aller Werte für eine mehrwertige Spalte kann erfolgen, indem diese Funktion wiederholt mit einem pretinfo- \> itagSequence-Wert aufgerufen wird, der bei 1 beginnt und bei jedem nachfolgenden Aufruf erhöht wird. Es ist bekannt, dass der letzte Spaltenwert abgerufen wird, wenn ein JET_wrnColumnNull von der Funktion zurückgegeben wird. Beachten Sie, dass diese Methode nicht ausgeführt werden kann, wenn in der Wertsequenz der Spalte mit mehreren Werten **explizite NULL-Werte** festgelegt sind, da diese Werte übersprungen werden würden. Wenn eine Anwendung alle mehrwertigen Spaltenwerte abrufen möchte, einschließlich der werte, die explizit auf **NULL** festgelegt sind, muss [JetRetrieveColumns](./jetretrievecolumns-function.md) anstelle von **JetRetrieveColumn** verwendet werden. Beachten Sie, dass diese Funktion nicht die Anzahl der Werte für eine mehrwertige Funktion zurückgibt, wenn ein *itagSequence-Wert* von 0 (null) angegeben wird. Nur [JetRetrieveColumns](./jetretrievecolumns-function.md) gibt die Anzahl der Werte eines Spaltenwerts zurück, wenn ein *itagSequence-Wert* von 0 (null) übergeben wird.

Wenn diese Funktion auf Transaktionsebene 0 (null) aufgerufen wird, z. B. ist die aufrufende Sitzung nicht selbst in einer Transaktion, wird eine Transaktion innerhalb der Funktion geöffnet und geschlossen. Der Zweck besteht darin, konsistente Ergebnisse zurückzugeben, falls sich ein langer Wert über Datenbankseiten erstreckt. Beachten Sie, dass die Transaktion zwischen Funktionsaufrufen und einer Reihe von Aufrufen dieser Funktion freigegeben wird, wenn sich die Sitzung nicht in einer Transaktion befindet und nach dem ersten Aufruf dieser Funktion aktualisierte Daten zurückgeben kann.

Der Standardspaltenwert wird abgerufen, wenn die Spalte nicht explizit auf einen anderen Wert festgelegt wurde, es sei denn, die option JET_bitRetrieveIgnoreDefault ist festgelegt.

Das Abrufen des Spaltenwerts für die automatische Inkrementierung aus dem Kopierpuffer vor dem Einfügen ist ein gängiges Mittel, um einen Datensatz eindeutig für die Verknüpfung zu identifizieren, wenn normalisierte Daten in mehrere Tabellen eingefügt werden. Der Wert für die automatische Inkrementierung wird zugeordnet, wenn der Einfügevorgang beginnt, und kann jederzeit aus dem Kopierpuffer abgerufen werden, bis das Update abgeschlossen ist.

Beim Abrufen aller markierten, mehrwertigen und Sparsespalten durch Festlegen von *columnid* auf 0 (null) werden Spalten in *columnid-Reihenfolge* von der niedrigsten *columnid* zur höchsten *columnid* abgerufen. Jedes Mal, wenn Spaltenwerte abgerufen werden, wird die gleiche Reihenfolge von Spaltenwerten zurückgegeben. Die Reihenfolge ist deterministisch.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RETINFO](./jet-retinfo-structure.md)  
[JetSetColumn](./jetretrievekey-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
