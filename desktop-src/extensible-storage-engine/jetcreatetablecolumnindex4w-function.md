---
description: 'Weitere Informationen zu: JetCreateTableColumnIndex4W-Funktion'
title: JetCreateTableColumnIndex4W-Funktion
TOCTitle: JetCreateTableColumnIndex4W Function
ms:assetid: 5a74b397-dfb4-4a1d-807b-284329239bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835042(v=EXCHG.10)
ms:contentKeyID: 49894664
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateTableColumnIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e0ecb22fe9936c9843c603211b0594599de7fcd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479186"
---
# <a name="jetcreatetablecolumnindex4w-function"></a>JetCreateTableColumnIndex4W-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetCreateTableColumnIndex4W-Funktion** erstellt eine Tabelle in einer ESE-Datenbank (Extensible Storage Engine) mit einem anfänglichen Satz von Indizes und einem anfänglichen Satz von Spalten aus einem Array von [JET_TABLECREATE3](./jet-tablecreate3-structure.md) Strukturen. Mit [der JET_TABLECREATE3-Struktur](./jet-tablecreate3-structure.md) kann eine Rückruffunktion angegeben werden.

Die **JetCreateTableColumnIndex4W-Funktion** wurde im Windows 8 Betriebssystem eingeführt.

``` c++
JET_ERR JET_API JetCreateTableColumnIndex4W(
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

Ein Zeiger auf eine [JET_TABLECREATE3](./jet-tablecreate3-structure.md) Struktur, die die zu erstellende Tabelle definiert. Weitere Informationen finden [Sie unter JET_TABLECREATE3.](./jet-tablecreate3-structure.md)

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der in der folgenden Tabelle aufgeführten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Enginge) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>Die Rückruffunktion konnte nicht aufgelöst werden. Die DLL wurde möglicherweise nicht gefunden, oder die Funktion in der DLL wurde möglicherweise nicht gefunden. Wenn eine ausreichende Protokollierung aktiviert ist, enthält das Ereignisprotokoll weitere Details.</p> | 
| <p>JET_errCannotIndex</p> | <p>Es wurde versucht, eine Indizierung über eine Escrow-Update- oder SLV-Spalte zu erstellen (beachten Sie, dass SLV-Spalten veraltet sind).</p> | 
| <p>JET_errCannotNestDDL</p> | <p>Wird zurückgegeben, wenn der <em>ptablecreate-grbit-Parameter &gt; </em> den JET_bitTableCreateTemplateTable Wert angibt, der <em>ptablecreate-szTemplateTableName-Parameter &gt; </em> jedoch auf NULL festgelegt ist.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Eine Spalte ist bereits vorhanden.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Es wurde versucht, eine nicht vorhandene Spalte zu indizieren. Ein Versuch, eine bedingte Indizierung für eine nicht vorhandene Spalte zu erstellen, kann auch diesen Fehler erzeugen.</p> | 
| <p>JET_errColumnRedundant</p> | <p>Es wurde versucht, eine redundante Spalte hinzuzufügen. Es sollte nicht mehr als eine Spalte für die automatische Inkrementierung vorhanden sein, und pro Tabelle sollte nicht mehr als eine Versionsspalte vorhanden sein.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Dieser Fehler wird zurückgegeben, wenn der <strong>ulDensity-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> auf eine Zahl kleiner als 20 oder mehr als 100 festgelegt ist.</p> | 
| <p>JET_errDDLNotInheritable</p> | <p>Gibt an, dass die Im <strong>szTemplateTableName-Element</strong> der <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3-Struktur</a> benannte Tabelle nicht als Vorlagentabelle markiert wurde (d.b. in dieser Tabelle wurde der JET_bitTableCreateTemplateTable Parameterwert nicht festgelegt).</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Es wurde versucht, zwei identische Indizes zu definieren.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Es wurde versucht, mehr als einen primären Index für eine Tabelle anzugeben. Eine Tabelle muss genau einen primären Index aufweisen. Wenn kein primärer Index angegeben wird, erstellt die Datenbank-Engine transparent einen.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Es wurde eine ungültige Indexdefinition angegeben. Im Folgenden sind einige der möglichen Gründe für diesen Fehler zu nennen:</p><ul><li><p>Ein primärer Index ist bedingt (das heißt, für den <strong>Grbit-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> ist der JET_bitIndexPrimary Wert festgelegt, und der <strong>cConditionalColumn-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> ist größer als 0 (null).</p></li><li><p>Gilt für Versionen des betriebssystems Windows Server ab Windows Server 2003. Es wurde versucht, einen Tupelindex mit Tupelgrenzwerten zu erstellen, aber ohne das <strong>Ptuplelimits-Element</strong> in der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur zu übergeben (d. b. für das <strong>Grbit-Element</strong> der <strong>JET_INDEXCREATE2-Struktur</strong> ist JET_bitIndexTupleLimits Wert festgelegt, aber der <strong>Ptuplelimitzeiger</strong> ist NULL).</p></li><li><p>Übergeben einer ungültigen Schlüsseldefinition im <strong>szKey-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur.</a> Informationen zu gültigen Definitionen finden Sie unter <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</p></li><li><p>Festlegen des <strong>cbVarSegMac-Members</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2,</a> dass es größer als der JET_cbPrimaryKeyMost Wert (für einen primären Index) oder größer als der JET_cbSecondaryKeyMost Wert (für einen sekundären Index) ist.</p></li><li><p>Übergeben einer ungültigen Kombination für einen benutzerdefinierten Unicode-Index (einer, für den das JET_bitIndexUnicode Wertbit im <strong>grbit-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> festgelegt ist). Einige häufige Ursachen sind der <strong>Pidxunicode-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur NULL ist oder die in der <strong>pidxunicode-Struktur</strong> angegebene LCID ungültig ist.</p></li><li><p>Angeben einer mehrwertigen Spalte für einen primären Index.</p></li><li><p>Versuch, zu viele bedingte Spalten zu indizierung. Der <strong>cConditionalColumn-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> darf nicht größer als <strong>JET_ccolKeyMost</strong>sein.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Gilt für Versionen von Windows, die mit Windows XP beginnen. Es wurde <a href="gg269207(v=exchg.10).md">eine JET_TUPLELIMITS</a> -Struktur angegeben, und ihre Grenzwerte werden nicht unterstützt. Weitere Informationen finden Sie im Abschnitt <a href="gg269207(v=exchg.10).md"></a> "Hinweise" der JET_TUPLELIMITS-Struktur.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Gilt für Versionen von Windows, die mit Windows XP beginnen. Ein Tupelindex kann nicht eindeutig sein (das heißt, für das <em>Grbit-Element</em> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> dürfen nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexUnique Werte festgelegt sein).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Gilt für Versionen von Windows, die mit Windows XP beginnen. Ein Tupelindex kann sich nur über einer einzelnen Spalte befinden (d.amp;quot;, wenn für das <strong>Grbit-Element</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> JET_bitIndexTuples Wert festgelegt ist und das <strong>szKey-Element</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur mehr als eine Spalte angibt).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Gilt für Versionen von Windows, die mit Windows XP beginnen. Ein Tupelindex darf kein primärer Index sein (d.amp;quot;das <strong>Grbit-Element</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexTuples festgelegt sein).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Gilt für Versionen von Windows, die mit Windows XP beginnen. Ein Tupelindex kann sich nur in einer Text- oder Unicode-Spalte befinden. Der Versuch, andere Spalten (z. B. binäre Spalten) zu indizieren, führt zu einem JET_errIndexTuplesTextColumnsOnly Antwortcode.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Gilt für Versionen von Windows, die mit Windows XP beginnen. Ein Tupelindex lässt nicht zu, dass der <strong>cbVarSegMac-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> festgelegt wird.</p> | 
| <p>JET_errInTransaction</p> | <p>Es wurde versucht, während einer Transaktion einen Index ohne Versionsinformationen zu erstellen.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>Der <strong>cp-Member</strong> der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE-Struktur</a> wurde nicht auf eine gültige Codepage festgelegt. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Der <strong>Coltypmember</strong> der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE-Struktur</a> wurde nicht auf einen gültigen Spaltentyp festgelegt.</p> | 
| <p>JET_errInvalidCreateIndex</p> | <p>Im Folgenden finden Sie einige Gründe, warum dieser Fehler auftreten kann:</p><ul><li><p>Der <strong>rgindexcreate-Member</strong> der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2-Struktur</a> wurde auf NULL festgelegt.</p></li><li><p>Der <strong>rgcolumncreate-Member</strong> der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2-Struktur</a> wurde auf NULL festgelegt.</p></li><li><p>Der <strong>cbStruct-Member</strong> einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> wurde nicht auf einen gültigen Wert festgelegt.</p></li></ul> | 
| <p>JET_errInvalidgrbit</p> | <p>In der <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3-Struktur</a> wurde eine ungültige Kombination von <strong>Grbitmembern</strong> angegeben.</p><p>Die Indexdefinition ist ungültig, da der <strong>grbit-Member</strong> inkonsistente Werte enthält. Folgende Gründe sind möglich:</p><ul><li><p>Für einen primären Index wurde ein Ignore-Bit angegeben (d. b. JET_bitIndexPrimary Wert mit den werten JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull oder JET_bitIndexIgnoreFirstNull übergeben wurde).</p></li><li><p>Ein leerer Index ignoriert keine NULL-Member (das heißt, für den <strong>Grbit-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> ist der JET_bitIndexEmpty Wert festgelegt, aber nicht JET_bitIndexIgnoreAnyNull Wert festgelegt).</p></li><li><p>Übergeben einer <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN-Struktur</a> mit einem ungültigen <strong>Grbitmember.</strong></p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Eine ungültige Gebietsschema-ID (LCID) wurde übergeben (entweder über den <strong>lcid-Member</strong> der <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX-Struktur,</a> auf die der <strong>pidxunicode-Member</strong> in der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> verweist, oder über das <strong>lcid-Feld</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur).</a></p> | 
| <p>JET_errInvalidParameter</p> | <p>Ein ungültiger Parameter wurde angegeben. Folgende Gründe sind möglich:</p><ul><li><p>Der <strong>rgcolumncreate-Member</strong> der <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3-Struktur</a> ist NULL.</p></li><li><p>Der <strong>cbStruct-Member</strong> einer der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE-Strukturen,</a> die im <strong>rgcolumncreate-Member</strong> der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> -Struktur angegeben sind, wurde nicht auf sizeof( JET_COLUMNCREATE ) festgelegt.</p></li><li><p>Der <strong>cbKey-Member</strong> einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> ist auf 0 (null) festgelegt.</p></li><li><p>Der <strong>cbStruct-Member</strong> einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> ist nicht auf sizeof( JET_INDEXCREATE2 ) festgelegt.</p></li></ul> | 
| <p>JET_errRecordTooBig</p> | <p>Der Datensatz ist zu groß. Die Summe des <strong>cbMax-Elements</strong> der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE-Struktur</a> für alle festen Spalten darf einen bestimmten Wert nicht überschreiten.</p> | 
| <p>JET_errTableDuplicate</p> | <p>Die Tabelle ist bereits vorhanden.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen. Eine Tabelle darf nicht mehr als <strong>JET_ccolFixedMost</strong> festen Spalten, nicht mehr als <strong>JET_ccolVarMost</strong> Spalten variabler Länge und nicht mehr als <strong>JET_ccolTaggedMost</strong> markierten Spalten enthalten.</p> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Fehler beim Versuch, eine Unicode-Spalte zu normalisieren. Dies kann dadurch verursacht werden, dass nicht mehr die Systemressourcen verfügbar sind.</p> | 
| <p>JET_errSpaceHintsInvalid</p> | <p>Ein Element der JET-Raumhinweisstruktur war nicht richtig oder veranstellbar.</p> | 



#### <a name="remarks"></a>Hinweise

Die **JetCreateTableColumnIndex4W-Funktion** erstellt eine Tabelle mit einem anfänglichen Satz von Spalten und Indizes. Zusätzliche Spalten und Indizes können dynamisch mithilfe der Funktionen [JetAddColumn,](./jetaddcolumn-function.md) [JetDeleteColumn,](./jetdeletecolumn-function.md) [JetDeleteColumn2,](./jetdeletecolumn2-function.md) [JetCreateIndex,](./jetcreateindex-function.md) [JetCreateIndex2,](./jetcreateindex2-function.md) [JetCreateIndex3,](./jetcreateindex3-function.md) [JetCreateIndex4W](./jetcreateindex4w-function.md)und [JetDeleteIndex](./jetdeleteindex-function.md) hinzugefügt und entfernt werden.

Wie bei der [JetOpenTable-Funktion](./jetopentable-function.md) sollte die [JetCloseTable-Funktion](./jetclosetable-function.md) die Anwendung schließen, wenn die Anwendung mit der zurückgegebenen *tableid* abgeschlossen ist.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows 8.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2012.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



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
