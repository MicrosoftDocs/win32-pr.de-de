---
description: 'Weitere Informationen finden Sie hier: JetCreateTableColumnIndex4W-Funktion'
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
ms.openlocfilehash: 26ebdb8cf62123febe2d44b5a638c285c180062c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366309"
---
# <a name="jetcreatetablecolumnindex4w-function"></a>JetCreateTableColumnIndex4W-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetCreateTableColumnIndex4W** -Funktion erstellt eine Tabelle in einem Extensible Storage Engine (ESE (Datenbank mit einem anfänglichen Satz von Indizes und ein ursprünglicher Satz von Spalten aus einem Array von [JET_TABLECREATE3](./jet-tablecreate3-structure.md) Strukturen). Die [JET_TABLECREATE3](./jet-tablecreate3-structure.md) -Struktur ermöglicht das Angeben einer Rückruffunktion.

Die **JetCreateTableColumnIndex4W** -Funktion wurde im Windows 8-Betriebssystem eingeführt.

``` c++
JET_ERR JET_API JetCreateTableColumnIndex4W(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in_out      JET_TABLECREATE3* ptablecreate
);
```

### <a name="parameters"></a>Parameter

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*DBID*

Der für den API-Befehl zu verwendende Daten Bank Bezeichner.

*ptablecreate*

Ein Zeiger auf eine [JET_TABLECREATE3](./jet-tablecreate3-structure.md) -Struktur, die die zu erstellende Tabelle definiert. Weitere Informationen finden Sie unter [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der in der folgenden Tabelle aufgelisteten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Enginge) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCallbackNotResolved</p></td>
<td><p>Die Rückruffunktion konnte nicht aufgelöst werden. Die dll wurde möglicherweise nicht gefunden, oder die Funktion in der dll wurde nicht gefunden. Wenn eine ausreichende Protokollierung aktiviert ist, werden im Ereignisprotokoll weitere Details angezeigt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotIndex</p></td>
<td><p>Es wurde versucht, über eine Spalte vom Typ "Escrow-Update" oder "SLV" zu indizieren (Beachten Sie, dass SLV-Spalten veraltet sind).</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotNestDDL</p></td>
<td><p>Wird zurückgegeben, wenn der <em>ptablecreate- &gt; grbit-</em> Parameter den JET_bitTableCreateTemplateTable Wert angibt, der <em>ptablecreate- &gt; sztemplatetablename</em> -Parameter jedoch auf NULL festgelegt ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnDuplicate</p></td>
<td><p>Eine Spalte ist bereits vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Es wurde versucht, einen Index für eine nicht vorhandene Spalte zu indizieren. Der Versuch, bedingt eine Indizierung über eine nicht vorhandene Spalte durchführen zu können, kann ebenfalls diesen Fehler verursachen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnRedundant</p></td>
<td><p>Es wurde versucht, eine redundante Spalte hinzuzufügen. Es darf nicht mehr als eine AUTOINCREMENT-Spalte vorhanden sein, und es sollte nicht mehr als eine Versions Spalte pro Tabelle vorhanden sein.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>Dieser Fehler wird zurückgegeben, wenn der <strong>uldensity</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur auf eine Zahl kleiner als 20 oder mehr als 100 festgelegt ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable</p></td>
<td><p>Gibt an, dass die Tabelle im <strong>sztemplatetablename</strong> -Member der <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> Struktur nicht als Vorlagen Tabelle gekennzeichnet ist (d. h., für diese Tabelle wurde der JET_bitTableCreateTemplateTable Parameterwert nicht festgelegt).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexDuplicate</p></td>
<td><p>Es wurde versucht, zwei identische Indizes zu definieren.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexHasPrimary</p></td>
<td><p>Es wurde versucht, mehr als einen primären Index für eine Tabelle anzugeben. Eine Tabelle muss genau einen primären Index aufweisen. Wenn kein primärer Index angegeben ist, wird von der Datenbank-Engine eine transparente Erstellung erstellt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Es wurde eine ungültige Index Definition angegeben. Im folgenden sind die möglichen Ursachen für diesen Fehler aufgeführt:</p>
<ul>
<li><p>Ein primärer Index ist bedingt (d. h., der <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur hat den JET_bitIndexPrimary Wert festgelegt, und der <strong>cconditionalcolumn</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur ist größer als 0 (null)).</p></li>
<li><p>Gilt für Versionen des Windows Server-Betriebssystems, beginnend mit Windows Server 2003. Es wurde versucht, einen Tupelindex mit tupellimits zu erstellen, ohne den <strong>ptuplelimits</strong> -Member in der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur zu übergeben (d. h., der <strong>grbit</strong> -Member der <strong>JET_INDEXCREATE2</strong> Struktur hat JET_bitIndexTupleLimits Wert festgelegt, der <strong>ptuplelimits</strong> -Zeiger ist jedoch NULL).</p></li>
<li><p>Übergeben einer ungültigen Schlüssel Definition im <strong>szkey</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur. Informationen zu gültigen Definitionen finden Sie unter <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</p></li>
<li><p>Das Festlegen des <strong>cbvarsegmac</strong> -Members in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> muss größer sein als der JET_cbPrimaryKeyMost Wert (für einen primären Index) oder größer als der JET_cbSecondaryKeyMost Wert (für einen sekundären Index).</p></li>
<li><p>Übergeben einer ungültigen Kombination für einen benutzerdefinierten Unicode-Index (einen, bei dem das JET_bitIndexUnicode-wertbit im <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur festgelegt ist). Zu den häufigsten Gründen gehören das <strong>pidxunicode</strong> -Element der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur ist NULL, oder die in der <strong>pidxunicode</strong> -Struktur angegebene LCID ist ungültig.</p></li>
<li><p>Angeben einer mehrwertigen Spalte für einen primären Index.</p></li>
<li><p>Es wird versucht, zu viele bedingte Spalten zu indizieren. Der <strong>cconditionalcolumn</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur darf nicht größer als <strong>JET_ccolKeyMost</strong>sein.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Gilt für Windows-Versionen ab Windows XP. Es wurde eine <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur angegeben, und ihre Grenzen werden nicht unterstützt. Weitere Informationen finden Sie im Abschnitt "Hinweise" in der <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> -Struktur.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>Gilt für Windows-Versionen ab Windows XP. Ein Tupelindex kann nicht eindeutig sein (d. h., für den <em>grbit</em> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur dürfen nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexUnique Werte festgelegt sein).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>Gilt für Windows-Versionen ab Windows XP. Ein Tupelindex kann nur über eine einzelne Spalte verfügen (d. h., wenn für das <strong>grbit</strong> -Element der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur JET_bitIndexTuples Wert festgelegt wurde und der <strong>szkey</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur mehr als eine Spalte angibt).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>Gilt für Windows-Versionen ab Windows XP. Bei einem Tupelindex kann es sich nicht um einen primären Index handeln (d. h., der <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexTuples festgelegt werden).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Gilt für Windows-Versionen ab Windows XP. Ein Tupelindex kann nur für eine Text-oder Unicode-Spalte gelten. Der Versuch, andere Spalten (z. b. binäre Spalten) zu indizieren, führt zu einem JET_errIndexTuplesTextColumnsOnly-Antwort Code.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Gilt für Windows-Versionen ab Windows XP. Ein Tupelindex lässt nicht zu, dass der <strong>cbvarsegmac</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur festgelegt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Es wurde versucht, einen Index ohne Versionsinformationen zu erstellen, während eine Transaktion durchgeführt wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>Der <strong>CP</strong> -Member der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Struktur wurde nicht auf eine gültige Codepage festgelegt. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Der <strong>colttmember</strong> der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Struktur wurde nicht auf einen gültigen Spaltentyp festgelegt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCreateIndex</p></td>
<td><p>Im folgenden sind einige Gründe aufgeführt, warum dieser Fehler auftreten kann:</p>
<ul>
<li><p>Der <strong>rgindexcreate</strong> -Member der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> Struktur wurde auf NULL festgelegt.</p></li>
<li><p>Der <strong>rgcolumncreate</strong> -Member der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> Struktur wurde auf NULL festgelegt.</p></li>
<li><p>Der <strong>cbStruct</strong> -Member einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur wurde nicht auf einen gültigen Wert festgelegt.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>In der <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> Struktur wurde eine ungültige Kombination von <strong>grbit</strong> -Membern angegeben.</p>
<p>Die Index Definition ist ungültig, da der <strong>grbit</strong> -Member inkonsistente Werte enthält. Folgende Ursachen sind möglich:</p>
<ul>
<li><p>Für einen primären Index wurde ein Ignore-Bit angegeben (d. h. JET_bitIndexPrimary Wert wurde mit den Werten JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull oder JET_bitIndexIgnoreFirstNull) übermittelt.</p></li>
<li><p>Ein leerer Index ignoriert keine NULL-Elemente (d. h., der <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur hat den JET_bitIndexEmpty Wert festgelegt, aber nicht JET_bitIndexIgnoreAnyNull Wert festgelegt).</p></li>
<li><p>Übergeben einer <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> -Struktur mit einem ungültigen <strong>grbit</strong> -Member.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Es wurde eine ungültige Gebiets Schema-ID (LCID) übergeben (entweder über den <strong>LCID</strong> -Member der <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> -Struktur, auf die der <strong>pidxunicode</strong> -Member in der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur verweist, oder über das <strong>LCID</strong> -Feld der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Ein ungültiger Parameter wurde angegeben. Folgende Ursachen sind möglich:</p>
<ul>
<li><p>Der <strong>rgcolumncreate</strong> -Member der <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> -Struktur ist NULL.</p></li>
<li><p>Der <strong>cbStruct</strong> -Member einer der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Strukturen, die im <strong>rgcolumncreate</strong> -Member der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> -Struktur angegeben sind, wurde nicht auf sizeof (JET_COLUMNCREATE) festgelegt.</p></li>
<li><p>Der <strong>cbkey</strong> -Member einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur ist auf 0 (null) festgelegt.</p></li>
<li><p>Der <strong>cbStruct</strong> -Member einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur ist nicht auf sizeof (JET_INDEXCREATE2) festgelegt.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errRecordTooBig</p></td>
<td><p>Der Datensatz ist zu groß. Die Summe des <strong>cbmax</strong> -Members der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Struktur für alle festgelegten Spalten darf einen bestimmten Wert nicht überschreiten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableDuplicate</p></td>
<td><p>Die Tabelle ist bereits vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen. Eine Tabelle kann nicht mehr als <strong>JET_ccolFixedMost</strong> fester Spalten, nicht mehr als <strong>JET_ccolVarMost</strong> Spalten variabler Länge und nicht mehr als <strong>JET_ccolTaggedMost</strong> markierte Spalten aufweisen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationFail</p></td>
<td><p>Fehler beim Versuch, eine Unicode-Spalte zu normalisieren. Dies kann darauf zurückzuführen sein, dass die Systemressourcen nicht mehr ausreichen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSpaceHintsInvalid</p></td>
<td><p>Ein Element der Jet-Raum Hinweise-Struktur war nicht korrekt oder kann nicht ausgeführt werden.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Die **JetCreateTableColumnIndex4W** -Funktion erstellt eine Tabelle mit einem anfänglichen Satz von Spalten und Indizes. Zusätzliche Spalten und Indizes können mithilfe der Funktionen [jetaddcolumn](./jetaddcolumn-function.md), [jetdeletecolumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [jetkreateindex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md)und [jetdeleteindex](./jetdeleteindex-function.md) dynamisch hinzugefügt und entfernt werden.

Wie bei der [jetopentable](./jetopentable-function.md) -Funktion sollte die [jetclosetable](./jetclosetable-function.md) -Funktion die Anwendung schließen, wenn die Anwendung mit der zurückgegebenen *TableID*-Funktion ausgeführt wird.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2012.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Siehe auch

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
[Jetaddcolumn](./jetaddcolumn-function.md)  
[Jetkreateingedex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateIndex3](./jetcreateindex3-function.md)  
[Jetkreatetable](./jetcreatetable-function.md)  
[Jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)  
[Jetdeletecolumn](./jetdeletecolumn-function.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
