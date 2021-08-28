---
description: 'Weitere Informationen zu: JetOpenTempTable3-Funktion'
title: JetOpenTempTable3-Funktion
TOCTitle: JetOpenTempTable3 Function
ms:assetid: 58d6e264-705e-402b-928f-96eefe5e9771
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269255(v=EXCHG.10)
ms:contentKeyID: 32765557
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable3
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d27531b9d70098746f60238a264c4762ff8f2058
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474466"
---
# <a name="jetopentemptable3-function"></a>JetOpenTempTable3-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetopentemptable3-function"></a>JetOpenTempTable3-Funktion

Die **JetOpenTempTable3-Funktion** erstellt eine temporäre Tabelle mit einem einzelnen Index, die zum Speichern und Abrufen von Datensätzen verwendet werden kann, genau wie eine gewöhnliche Tabelle, die mit [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)erstellt wurde. Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen. Sie können auch verwendet werden, um datensätzensätze sehr schnell zu sortieren und doppelte Entfernungen durchzuführen, wenn ausschließlich sequenziell darauf zugegriffen wird.

```cpp
    JET_ERR JET_API JetOpenTempTable3(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in_opt      JET_UNICODEINDEX* pidxunicode,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*prgcolumndef*

Identifiziert die Spaltendefinitionen der Spalten, die in der temporären Tabelle erstellt werden sollen.

Für die Spaltendefinitionsoptionen, die mit einer temporären Tabelle verwendet werden können, gelten wichtige Einschränkungen. Weitere Informationen finden Sie im Abschnitt Hinweise.

Zusätzlich zu den üblichen Spaltendefinitionsoptionen können auch null oder mehr der folgenden Optionen angegeben werden, die nur im Kontext einer temporären Tabelle relevant sind.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitColumnTTDescending</p> | <p>Diese Option gibt an, dass die Sortierreihenfolge der Schlüsselspalte für die temporäre Tabelle absteigend und nicht aufsteigend sein sollte. Wenn diese Option ohne JET_bitColumnTTKey angegeben wird, wird diese Option ignoriert.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>Diese Option gibt an, dass die Spalte eine Schlüsselspalte für die temporäre Tabelle ist.</p><p>Die Reihenfolge der Spaltendefinitionen mit dieser Option, die im Eingabearray angegeben ist, bestimmt die Rangfolge jeder Schlüsselspalte für die temporäre Tabelle. Die erste Spaltendefinition im Array, für die diese Option festgelegt ist, ist die wichtigste Schlüsselspalte usw. Wenn mehr Schlüsselspalten angefordert werden, als von der Datenbank-Engine unterstützt werden können, wird diese Option für die nicht unterstützten Schlüsselspalten ignoriert.</p> | 



*ccolumn*

Siehe *prgcolumndef*.

*pidxunicode*

Die Gebietsschema-ID und normalisierungsflags, die zum Vergleichen aller Unicode-Schlüsselspaltendaten in der temporären Tabelle verwendet werden.

Wenn dieser Parameter nicht vorhanden ist, wird die STANDARD-LCID verwendet, um alle Unicode-Schlüsselspalten in der temporären Tabelle zu vergleichen. Die LCID-Standardeinstellung ist das gebietsschema für Englisch in den USA.

Wenn dieser Parameter nicht vorhanden ist, werden die Standardnormalisierungsflags verwendet, um alle Unicode-Schlüsselspaltendaten in der temporären Tabelle zu vergleichen. Die Standardnormalisierungsflags sind: NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.

*grbit*

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten, die 0 (null) oder mehr der folgenden Elemente enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitTTErrorOnDuplicateInsertion</p> | <p>Diese Option fordert an, dass jeder Versuch, einen Datensatz mit demselben Indexschlüssel wie ein zuvor eingefügter Datensatz einzufügen, sofort mit JET_errKeyDuplicate fehlschlägt. Wenn diese Option nicht angefordert wird, wird möglicherweise sofort ein Duplikat erkannt und ein Fehler ausgelöst oder später automatisch entfernt, je nachdem, welche Strategie die Datenbank-Engine zum Implementieren der temporären Tabelle basierend auf der angeforderten Funktionalität gewählt hat.</p><p>Wenn diese Funktion nicht erforderlich ist, ist es am besten, sie nicht anzufordern. Wenn diese Funktionalität nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p> | 
| <p>JET_bitTTForceMaterialization</p> | <p>Diese Option zwingt den temporären Tabellen-Manager, jeden Versuch zu verwerfen, eine clevere Strategie für die Verwaltung der temporären Tabelle auszuwählen, die zu einer verbesserten Leistung führt.</p> | 
| <p>JET_bitTTForwardOnly</p> | <p>Diese Option fordert an, dass die temporäre Tabelle nur erstellt wird, wenn der temporäre Tabellen-Manager die für Zwischenabfrageergebnisse optimierte Implementierung verwenden kann. Wenn ein Merkmal der temporären Tabelle die Verwendung dieser Optimierung verhindern würde, schlägt der Vorgang mit JET_errCannotMaterializeForwardOnlySort fehl.</p><p>Ein Nebeneffekt dieser Option besteht darin, dass die temporäre Tabelle Datensätze mit doppelten Indexschlüsseln enthalten kann. Weitere Informationen finden Sie unter JET_bitTTUnique.</p><p>Diese Option ist nur in Windows Server 2003 und höher verfügbar.</p> | 
| <p>JET_bitTTIndexed</p> | <p>Diese Option fordert an, dass die temporäre Tabelle flexibel genug ist, um die Verwendung von <a href="gg294103(v=exchg.10).md">JetSeek</a> zum Suchen von Datensätzen nach Indexschlüssel zu ermöglichen.</p><p>Wenn diese Funktion nicht erforderlich ist, ist es am besten, sie nicht anzufordern. Wenn diese Funktionalität nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p> | 
| <p>JET_bitTTUnique</p> | <p>Diese Option fordert an, dass Datensätze mit doppelten Indexschlüsseln aus dem endgültigen Satz von Datensätzen in der temporären Tabelle entfernt werden.</p><p>Vor Windows Server 2003 hat die Datenbank-Engine diese Option immer als wirksam angesehen, da alle gruppierten Indizes ebenfalls ein Primärschlüssel sein müssen und daher eindeutig sein müssen. Ab Windows Server 2003 ist es jetzt möglich, eine temporäre Tabelle zu erstellen, die KEINE Duplikate entfernt, wenn auch die option JET_bitTTForwardOnly angegeben ist.</p><p>Es ist nicht möglich zu wissen, welches Duplikat gewinnt und welche Duplikate im Allgemeinen verworfen werden. Wenn jedoch die option JET_bitTTErrorOnDuplicateInsertion angefordert wird, wird der erste Datensatz mit einem angegebenen Indexschlüssel, der in die temporäre Tabelle eingefügt werden soll, immer gewonnen.</p> | 
| <p>JET_bitTTUpdatable</p> | <p>Mit dieser Option wird angefordert, dass die temporäre Tabelle flexibel genug ist, damit datensätze, die zuvor eingefügt wurden, später geändert werden können. Wenn diese Funktion nicht erforderlich ist, ist es am besten, sie nicht anzufordern.</p><p>Wenn diese Funktionalität nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p> | 
| <p>JET_bitTTScrollable</p> | <p>Diese Option fordert an, dass die temporäre Tabelle flexibel genug ist, damit Datensätze mithilfe von <a href="gg294117(v=exchg.10).md">JetMove</a>in beliebiger Reihenfolge und Richtung gescannt werden können.</p><p>Wenn diese Funktion nicht erforderlich ist, ist es am besten, sie nicht anzufordern. Wenn diese Funktionalität nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p> | 
| <p>JET_bitTTSortNullsHigh</p> | <p>Diese Option fordert an, dass NULL-Schlüsselspaltenwerte näher am Ende des Indexes als Werte für Schlüsselspalten ungleich NULL sortiert werden.</p> | 
| <p>JET_bitTTIntrinsicLVsOnly</p> | <p>Anforderungen, um nur systeminterne long-Werte zuzulassen.</p><p><strong>Windows 7:</strong> <strong>JET_bitTTIntrinsicLVsOnly</strong> wird in Windows 7 eingeführt.</p> | 



*Ptableid*

Der Ausgabepuffer, der den neuen Cursor empfängt, der für die neu erstellte temporäre Tabelle geöffnet wurde.

*prgcolumnid*

Der Ausgabepuffer, der das Array von Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert wurden.

Die Spalten-IDs in diesem Array entsprechen genau dem Eingabearray der Spaltendefinitionen. Daher muss die Größe dieses Puffers der Größe des Eingabearrays entsprechen.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errCannotMaterializeForwardOnlySort</p> | <p>Fehler bei <strong>JetOpenTempTable3,</strong> weil JET_bitTTForwardOnly angegeben wurde und die angegebene temporäre Tabelle nicht mithilfe der vorwärts gerichteten Optimierung erstellt werden konnte. Dieser Fehler wird nur von Windows Server 2003 und höher zurückgegeben.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Der Index konnte nicht erstellt werden, da eine ungültige Indexdefinition angegeben wurde. <strong>JetOpenTempTable3</strong> gibt diesen Fehler zurück, wenn:</p><ul><li><p>Das gebietsschema "Sprachneutral" wird angegeben.</p></li><li><p>Es wird ein ungültiger Satz von Normalisierungsflags angegeben.</p></li></ul><p>Dieser Fehler wird nur von Windows 2000 zurückgegeben.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>Der <strong>cp-Member</strong> der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> wurde nicht auf eine gültige Codepage festgelegt. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Der <strong>Coltyp-Member</strong> der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> wurde nicht auf einen gültigen Spaltentyp festgelegt.</p> | 
| <p>JET_errInvalidLanguageId</p> | <p>Der Index konnte nicht erstellt werden, da versucht wurde, eine ungültige Locale ID zu verwenden. Die Locale-ID ist möglicherweise vollständig ungültig, oder das zugeordnete Sprachpaket ist möglicherweise nicht installiert.</p> | 
| <p>JET_errInvalidLCMapStringFlags</p> | <p>Der Index konnte nicht erstellt werden, weil versucht wurde, einen ungültigen Satz von Normalisierungsflags zu verwenden. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben. Bei Windows 2000 führen ungültige Normalisierungsflags stattdessen JET_errIndexInvalidDef zurück.</p> | 
| <p>JET_errInvalidSesid</p> | <p>Das Sitzungshandy ist ungültig oder verweist auf eine geschlossene Sitzung. Dieser Fehler wird nicht unter allen Umständen zurückgegeben. Handles werden nur nach bestem Aufwand überprüft.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errOutOfCursors</p> | <p>Der Vorgang ist fehlgeschlagen, da die Engine nicht die Ressourcen zuordnen kann, die zum Öffnen eines neuen Cursors erforderlich sind. Cursorressourcen werden mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter mit JET_paramMaxCursors.</a> <a href="gg269201(v=exchg.10).md"></a></p> | 
| <p>JET_errOutOfMemory</p> | <p>Fehler beim Vorgang, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um ihn abschließen zu können.</p><p><strong>JetOpenTempTable3 kann</strong> JET_errOutOfMemory zurückgeben, wenn der Adressraum des Hostprozesses zu fragmentiert wird. Der temporäre Tabellen-Manager ordnet für jede temporäre Tabelle, die erstellt wird, immer einen Adressraum von 1 MB zu, unabhängig von der zu speichernden Datenmenge.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden.</p><p>Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen. Eine Tabelle kann nicht mehr als JET_ccolFixedMost Spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost spalten enthalten.</p> | 
| <p>JET_errTooManyOpenIndexes</p> | <p>Der Vorgang ist fehlgeschlagen, da die Engine nicht die Ressourcen zuordnen kann, die zum Zwischenspeichern der Indizes der Tabelle erforderlich sind. Die Anzahl der Indizes, deren Schema zwischengespeichert werden kann, wird mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter mit</a> <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables.</a></p> | 
| <p>JET_errTooManyOpenTables</p> | <p>Fehler beim Vorgang, da die Engine nicht die Ressourcen zuordnen kann, die zum Zwischenspeichern des Schemas der Tabelle erforderlich sind. Die Anzahl der Tabellen, deren Schema zwischengespeichert werden kann, wird mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter mit</a> <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables.</a></p> | 
| <p>JET_errTooManySorts</p> | <p>Der Vorgang ist fehlgeschlagen, da die Engine nicht die Ressourcen zuordnen kann, die zum Erstellen einer temporären Tabelle erforderlich sind. Temporäre Tabellenressourcen werden mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter und</a> <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables.</a></p> | 



Bei Erfolg wird ein Cursor zurückgegeben, der in der neu erstellten temporären Tabelle geöffnet wird. Der Status der temporären Datenbank wird so vorbereitet, dass er die neue temporäre Tabelle enthält. Der Status normaler Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.

Bei einem Fehler wird die temporäre Tabelle nicht erstellt, und es wird kein Cursor zurückgegeben. Der Status der temporären Datenbank kann geändert werden. Der Status normaler Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[Erweiterbare Storage Engine-Fehler](./extensible-storage-engine-errors.md)  
[Fehlerbehandlungsparameter](./error-handling-parameters.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetMove](./jetmove-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
