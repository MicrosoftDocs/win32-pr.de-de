---
description: Weitere Informationen finden Sie unter JetCreateTableColumnIndex3-Funktion.
title: JetCreateTableColumnIndex3-Funktion
TOCTitle: JetCreateTableColumnIndex3 Function
ms:assetid: c1a1b091-b4a6-4cdc-a0ea-af21c1462449
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294079(v=EXCHG.10)
ms:contentKeyID: 32765694
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex3
- JetCreateTableColumnIndex3W
- JetCreateTableColumnIndex3A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b1e22b8816f3083fdf3cf623107197bc8a06883
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985952"
---
# <a name="jetcreatetablecolumnindex3-function"></a>JetCreateTableColumnIndex3-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcreatetablecolumnindex3-function"></a>JetCreateTableColumnIndex3-Funktion

Die **JetCreateTableColumnIndex3-Funktion** erstellt eine Tabelle in einer ESE-Datenbank mit einem anfänglichen Satz von Indizes und einem anfänglichen Satz von Spalten aus einem Array JET_TABLECREATE3 [Strukturen.](./jet-tablecreate3-structure.md) Die [JET_TABLECREATE3-Struktur](./jet-tablecreate3-structure.md) ermöglicht die Angabe einer Rückruffunktion.

**Windows 7:** **JetCreateTableColumnIndex3** wird im Windows 7 eingeführt.

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex3(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE3* ptablecreate
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*Dbid*

Der Datenbankbezeichner, der für den API-Aufruf verwendet werden soll.

*ptablecreate*

Ein Zeiger auf eine [JET_TABLECREATE3](./jet-tablecreate3-structure.md) Struktur, die die zu erstellende Tabelle definiert. Weitere [JET_TABLECREATE3](./jet-tablecreate3-structure.md) finden Sie unter JET_TABLECREATE3.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>Die Rückruffunktion konnte nicht aufgelöst werden. Die DLL wurde möglicherweise nicht gefunden, oder die Funktion in der DLL wurde möglicherweise nicht gefunden. Wenn eine ausreichende Protokollierung aktiviert ist, werden im Ereignisprotokoll weitere Details angezeigt.</p> | 
| <p>JET_errCannotIndex</p> | <p>Es wurde versucht, eine Escrow-Update- oder SLV-Spalte zu indizieren (beachten Sie, dass SLV-Spalten veraltet sind).</p> | 
| <p>JET_errCannotNestDDL</p> | <p>Wenn ptablecreate- &gt; grbit JET_bitTableCreateTemplateTable, aber ptablecreate- &gt; szTemplateTableName ist auf NULL festgelegt.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Eine Spalte ist bereits vorhanden.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Es wurde versucht, eine Indizierung über eine nicht vorhandene Spalte zu erstellen. Der Versuch, eine nicht vorhandene Spalte bedingt zu indizieren, kann ebenfalls zu diesem Fehler führen.</p> | 
| <p>JET_errColumnRedundant</p> | <p>Es wurde versucht, eine redundante Spalte hinzuzufügen. Es sollte nicht mehr als eine Spalte für die automatische Inkrementierung und nicht mehr als eine Versionsspalte pro Tabelle geben.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Dieser Fehler wird zurückgegeben, wenn der <strong>ulDensity-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> auf eine Zahl kleiner als 20 oder mehr als 100 festgelegt ist.</p> | 
| <p>JET_errDDLNotInheritable</p> | <p>Gibt an, dass die Tabelle mit dem Namen im <strong>szTemplateTableName-Element</strong> der <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3-Struktur</a> nicht als Vorlagentabelle markiert wurde (d. h., für diese Tabelle wurde JET_bitTableCreateTemplateTable festgelegt).</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Es wurde versucht, zwei identische Indizes zu definieren.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Es wurde versucht, mehrere primäre Indizes für eine Tabelle anzugeben. Eine Tabelle muss genau einen primären Index haben. Wenn kein primärer Index angegeben wird, erstellt die Datenbank-Engine transparent einen.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Es wurde eine ungültige Indexdefinition angegeben. Im Folgenden finden Sie einige mögliche Gründe für den Empfang dieses Fehlers:</p><ul><li><p>Ein primärer Index ist bedingt (d. h., das <strong>Grbit-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> verfügt über eine JET_bitIndexPrimary-Menge, und <strong>das cConditionalColumn-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> ist größer als 0 (null).</p></li><li><p>Windows Server 2003 und neuere Versionen von Windows. Es wurde versucht, einen Tupelindex mit Tupelgrenzwerten zu erstellen, ohne jedoch das <strong>ptuplelimits-Member</strong> in der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> zu übergeben (d. h., das <strong>Grbit-Member</strong> der JET_INDEXCREATE2-Struktur hat JET_bitIndexTupleLimits festgelegt, aber der <strong>ptuplelimits-Zeiger</strong> ist NULL).</p></li><li><p>Übergeben einer ungültigen Schlüsseldefinition im <strong>szKey-Member</strong> <a href="gg294082(v=exchg.10).md">der</a> JET_INDEXCREATE2 Struktur. Unter <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> finden Sie eine Erörterung gültiger Definitionen.</p></li><li><p>Festlegen des <strong>cbVarSegMac-Mitglieds</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> auf größer als JET_cbPrimaryKeyMost (für einen primären Index) oder größer als JET_cbSecondaryKeyMost (für einen sekundären Index).</p></li><li><p>Übergeben einer ungültigen Kombination für einen benutzerdefinierten Unicode-Index (einer, bei dem das JET_bitIndexUnicode-Bit im <strong>Grbit-Member</strong> von <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2.</a> Einige häufige Ursachen sind das pidxunicode-Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> struktur ist NULL, oder die in der <strong>pidxunicode-Struktur</strong> angegebene LCID ist ungültig. <strong></strong></p></li><li><p>Angeben einer mehrwertigen Spalte für einen primären Index.</p></li><li><p>Es wird versucht, zu viele bedingte Spalten zu indizieren. Das <strong>cConditionalColumn-Member</strong> der JET_INDEXCREATE2 <a href="gg294082(v=exchg.10).md">darf</a> nicht größer als JET_ccolKeyMost.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP und neuere Versionen Windows. Eine <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS-Struktur</a> wurde angegeben, und ihre Grenzwerte werden nicht unterstützt. Weitere Informationen finden Sie im Abschnitt "Hinweise" <a href="gg269207(v=exchg.10).md">der JET_TUPLELIMITS</a> Struktur.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP und neuere Versionen Windows. Ein Tupelindex darf nicht eindeutig sein (d. h. der <em>Grbit-Member</em> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexUnique haben).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP und neuere Versionen Windows. Ein Tupelindex kann sich nur über einer einzelnen Spalte (d. h., wenn für das <strong>Grbitelement</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> JET_bitIndexTuples festgelegt ist und das <strong>szKey-Element</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> mehr als eine Spalte angibt).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP und neuere Versionen Windows. Ein Tupelindex kann kein primärer Index sein (d.h. das <strong>Grbit-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexTuples haben).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP und neuere Versionen Windows. Ein Tupelindex kann nur für eine Text- oder Unicode-Spalte verwendet werden. Der Versuch, andere Spalten (z. B. binäre Spalten) zu indizieren, führt zu JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP und neuere Versionen Windows. Ein Tupelindex lässt das Festlegen des <strong>cbVarSegMac-JET_INDEXCREATE2</strong> der Struktur nicht zu. <a href="gg294082(v=exchg.10).md"></a></p> | 
| <p>JET_errInTransaction</p> | <p>Es wurde versucht, während einer Transaktion einen Index ohne Versionsinformationen zu erstellen.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>Der <strong>cp-Member</strong> der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE-Struktur</a> wurde nicht auf eine gültige Codepage festgelegt. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Der <strong>Coltyp-Member</strong> der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> wurde nicht auf einen gültigen Spaltentyp festgelegt.</p> | 
| <p>JET_errInvalidCreateIndex</p> | <p>Im Folgenden finden Sie einige Gründe, warum dieser Fehler auftreten kann:</p><ul><li><p>Der <strong>rgindexcreate-Member</strong> der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> wurde auf NULL festgelegt.</p></li><li><p>Der <strong>rgcolumncreate-Member</strong> der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> wurde auf NULL festgelegt.</p></li><li><p>Der <strong>cbStruct-Member</strong> einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> wurde nicht auf einen gültigen Wert festgelegt.</p></li></ul> | 
| <p>JET_errInvalidgrbit</p> | <p>Eine ungültige Kombination von <strong>Grbit-Membern</strong> wurde <a href="gg269264(v=exchg.10).md">in</a>JET_TABLECREATE3.</p><p>Die Indexdefinition ist ungültig, da <strong>das Grbit-Member</strong> inkonsistente Werte enthält. Im Folgenden finden Sie einige mögliche Gründe:</p><ul><li><p>Für einen primären Index wurde ein Ignore-Bit angegeben (d. b. JET_bitIndexPrimary wurde mit JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull oder JET_bitIndexIgnoreFirstNull übergeben).</p></li><li><p>Ein leerer Index ignoriert keine NULL-Member (das heißt, der <strong>grbit-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> hat JET_bitIndexEmpty festgelegt, verfügt jedoch nicht über JET_bitIndexIgnoreAnyNull).</p></li><li><p>Übergeben einer <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN-Struktur</a> mit einem ungültigen <strong>Grbitmember.</strong></p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Eine ungültige Gebietsschema-ID (LCID) wurde übergeben (entweder über den <strong>lcid-Member</strong> der <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX-Struktur,</a> auf den der <strong>pidxunicode-Member</strong> in der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> zeigt, oder über das <strong>lcid-Feld</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur).</a></p> | 
| <p>JET_errInvalidParameter</p> | <p>Ein ungültiger Parameter wurde angegeben. Folgende Gründe sind möglich:</p><ul><li><p>Der <strong>rgcolumncreate-Member</strong> der <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3-Struktur</a> ist NULL.</p></li><li><p>Der <strong>cbStruct-Member</strong> einer der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE-Strukturen,</a> die im <strong>rgcolumncreate-Member</strong> der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2-Struktur</a> angegeben sind, wurde nicht auf sizeof( JET_COLUMNCREATE ) festgelegt.</p></li><li><p>Der <strong>cbKey-Member</strong> einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> ist auf 0 (null) festgelegt.</p></li><li><p>Der <strong>cbStruct-Member</strong> einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> ist nicht auf sizeof( JET_INDEXCREATE2 ) festgelegt.</p></li></ul> | 
| <p>JET_errRecordTooBig</p> | <p>Der Datensatz ist zu groß. Die Summe des <strong>cbMax-Elements</strong> der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE-Struktur</a> für alle festen Spalten darf einen bestimmten Wert nicht überschreiten.</p> | 
| <p>JET_errTableDuplicate</p> | <p>Die Tabelle ist bereits vorhanden.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen. Eine Tabelle darf nicht mehr als JET_ccolFixedMost festen Spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost markierten Spalten enthalten.</p> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Fehler beim Normalisieren einer Unicode-Spalte. Dies kann dadurch verursacht werden, dass nicht mehr die Systemressourcen verfügbar sind.</p> | 
| <p>JET_errSpaceHintsInvalid</p> | <p>Ein Element der JET-Raumhinweisstruktur war nicht richtig oder veranstellbar.</p> | 



#### <a name="remarks"></a>Bemerkungen

Der Name **JetCreateTableColumnIndex3** stammt aus der Reihenfolge der Erstellung der Objekte: Er erstellt zunächst eine Tabelle, Spalten und schließlich Indizes. **JetCreateTableColumnIndex3** erstellt eine Tabelle mit einem anfänglichen Satz von Spalten und Indizes. Zusätzliche Spalten und Indizes können dynamisch mit [JetAddColumn,](./jetaddcolumn-function.md) [JetDeleteColumn,](./jetdeletecolumn-function.md) [JetDeleteColumn2,](./jetdeletecolumn2-function.md) [JetCreateIndex,](./jetcreateindex-function.md) [JetCreateIndex2,](./jetcreateindex2-function.md) [JetCreateIndex3](./jetcreateindex3-function.md)und [JetDeleteIndex](./jetdeleteindex-function.md)hinzugefügt und entfernt werden.

Wenn die Anwendung wie [JetOpenTable](./jetopentable-function.md)die zurückgegebene *tableid* verwendet, sollte sie in der Regel mit [JetCloseTable](./jetclosetable-function.md)geschlossen werden.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetCreateTableColumnIndex3W</strong> (Unicode) und <strong>JetCreateTableColumnIndex3A</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_CBTYP](./jet-cbtyp.md)  
[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateIndex3](./jetcreateindex3-function.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDeleteColumn](./jetdeletecolumn-function.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
