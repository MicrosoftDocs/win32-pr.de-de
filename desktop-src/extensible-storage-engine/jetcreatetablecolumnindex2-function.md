---
description: 'Weitere Informationen finden Sie hier: JetCreateTableColumnIndex2-Funktion'
title: JetCreateTableColumnIndex2-Funktion
TOCTitle: JetCreateTableColumnIndex2 Function
ms:assetid: ad9caaf3-8cd2-453f-894d-8ac438c50b73
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294057(v=EXCHG.10)
ms:contentKeyID: 32765672
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex2W
- JetCreateTableColumnIndex2
- JetCreateTableColumnIndex2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51a1789fe050ddd62990f6561ddeb01363d69f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050585"
---
# <a name="jetcreatetablecolumnindex2-function"></a>JetCreateTableColumnIndex2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcreatetablecolumnindex2-function"></a>JetCreateTableColumnIndex2-Funktion

Die **JetCreateTableColumnIndex2** -Funktion erstellt eine Tabelle in einer ESE-Datenbank mit einem anfänglichen Satz von Indizes und einem anfänglichen Satz von Spalten aus einem Array von [JET_TABLECREATE2](./jet-tablecreate2-structure.md) Strukturen. Die [JET_TABLECREATE2](./jet-tablecreate2-structure.md) -Struktur ermöglicht das Angeben einer Rückruffunktion.

**Windows XP: JetCreateTableColumnIndex2** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex2(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE2* ptablecreate
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*DBID*

Der für den API-Befehl zu verwendende Daten Bank Bezeichner.

*ptablecreate*

Ein Zeiger auf eine [JET_TABLECREATE2](./jet-tablecreate2-structure.md) -Struktur, die die zu erstellende Tabelle definiert. Weitere Informationen finden Sie unter [JET_TABLECREATE2](./jet-tablecreate2-structure.md) .

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>, Wenn ptablecreate- &gt; grbit JET_bitTableCreateTemplateTable angibt, ptablecreate- &gt; sztemplatetablename jedoch auf NULL festgelegt ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnDuplicate</p></td>
<td><p>Eine Spalte ist bereits vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Es wurde versucht, eine nicht vorhandene Spalte zu indizieren. Der Versuch, bedingt eine Indizierung über eine nicht vorhandene Spalte durchführen zu können, kann ebenfalls diesen Fehler verursachen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnRedundant</p></td>
<td><p>Es wurde versucht, eine redundante Spalte hinzuzufügen. Es darf nicht mehr als eine AUTOINCREMENT-Spalte und höchstens eine Versions Spalte pro Tabelle vorhanden sein.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>Dieser Fehler wird zurückgegeben, wenn der <strong>uldensity</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur auf eine Zahl kleiner als 20 oder mehr als 100 festgelegt ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable</p></td>
<td><p>Gibt an, dass die Tabelle im <strong>sztemplatetablename</strong> -Member der <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> Struktur nicht als Vorlagen Tabelle gekennzeichnet ist (d. h., dass die Tabelle nicht über JET_bitTableCreateTemplateTable festgelegt wurde).</p></td>
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
<td><p>Es wurde eine ungültige Index Definition angegeben. Mögliche Ursachen für den Empfang dieses Fehlers:</p>
<ul>
<li><p>Ein primärer Index ist bedingt (d. h., das <strong>grbit</strong> -Element der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur verfügt über JET_bitIndexPrimary Menge, und der <strong>cconditionalcolumn</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur ist größer als 0 (null)).</p></li>
<li><p>Windows Server 2003 und höher. Es wurde versucht, einen Tupelindex mit tupellimits zu erstellen, ohne den <strong>ptuplelimits</strong> -Member in der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur zu übergeben (d. h., der <strong>grbit</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur hat JET_bitIndexTupleLimits festgelegt, der <strong>ptuplelimits</strong> -Zeiger ist jedoch NULL).</p></li>
<li><p>Übergeben einer ungültigen Schlüssel Definition im <strong>szkey</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur. Eine Erörterung gültiger Definitionen finden Sie unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p></li>
<li><p>Das Festlegen des <strong>cbvarsegmac</strong> -Members in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> auf größer als JET_cbPrimaryKeyMost (für einen primären Index) oder größer als JET_cbSecondaryKeyMost (für einen sekundären Index).</p></li>
<li><p>Übergeben einer ungültigen Kombination für einen benutzerdefinierten Unicode-Index (einen, bei dem das JET_bitIndexUnicode Bit im <strong>grbit</strong> -Member von <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>festgelegt ist). Zu den häufigsten Gründen gehören das <strong>pidxunicode</strong> -Element der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur ist NULL, oder die in der <strong>pidxunicode</strong> -Struktur angegebene LCID ist ungültig.</p></li>
<li><p>Angeben einer mehrwertigen Spalte für einen primären Index.</p></li>
<li><p>Es wird versucht, zu viele bedingte Spalten zu indizieren. Der <strong>cconditionalcolumn</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur darf nicht größer als JET_ccolKeyMost sein.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Windows XP und höher. Es wurde eine <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur angegeben, und ihre Grenzen werden nicht unterstützt. Weitere Informationen finden Sie im Abschnitt "Hinweise" der <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>Windows XP und höher. Ein Tupelindex kann nicht eindeutig sein (d. h., der <em>grbit</em> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexUnique festgelegt werden).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>Windows XP und höher. Ein Tupelindex kann nur über eine einzelne Spalte verfügen (d. h., wenn der <strong>grbit</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur JET_bitIndexTuples festgelegt hat und der <strong>szkey</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur mehr als eine Spalte angibt).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>Windows XP und höher. Bei einem Tupelindex kann es sich nicht um einen primären Index handeln (d. h., der <strong>grbit</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexTuples festgelegt werden).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Windows XP und höher. Ein Tupelindex kann nur für eine Text-oder Unicode-Spalte gelten. Der Versuch, andere Spalten (z. b. binäre Spalten) zu indizieren, führt zu JET_errIndexTuplesTextColumnsOnly.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Windows XP und höher. Ein Tupelindex lässt nicht zu, dass der <strong>cbvarsegmac</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur festgelegt wird.</p></td>
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
<td><p>Mögliche Ursachen für diesen Fehler:</p>
<ul>
<li><p>Der <strong>rgindexcreate</strong> -Member der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> Struktur wurde auf NULL festgelegt.</p></li>
<li><p>Der <strong>rgcolumncreate</strong> -Member der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> Struktur wurde auf NULL festgelegt.</p></li>
<li><p>Der <strong>cbStruct</strong> -Member einer <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur wurde nicht auf einen gültigen Wert festgelegt.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>In <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> oder <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>wurde eine ungültige Kombination von <strong>grbit</strong> -Membern angegeben.</p>
<p>Die Index Definition ist ungültig, da der <strong>grbit</strong> -Member inkonsistente Werte enthält. Mögliche Ursachen:</p>
<ul>
<li><p>Für einen primären Index wurde ein Ignore-Bit angegeben (d. h. JET_bitIndexPrimary mit JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull oder JET_bitIndexIgnoreFirstNull).</p></li>
<li><p>Ein leerer Index ignoriert keine NULL-Elemente (d. h., das <strong>grbit</strong> -Element der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur hat JET_bitIndexEmpty festgelegt, aber nicht JET_bitIndexIgnoreAnyNull festgelegt).</p></li>
<li><p>Übergeben einer <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> -Struktur mit einem ungültigen <strong>grbit</strong> -Member.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Es wurde eine ungültige Gebiets Schema-ID (LCID) übergeben (entweder über den <strong>LCID</strong> -Member der <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> -Struktur, auf die durch das <strong>pidxunicode</strong> -Element in der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur verwiesen wird, oder über das <strong>LCID</strong> -Feld der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Ein ungültiger Parameter wurde angegeben. Mögliche Ursachen:</p>
<ul>
<li><p>Der <strong>rgcolumncreate</strong> -Member der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> -Struktur ist NULL.</p></li>
<li><p>Der <strong>cbStruct</strong> -Member einer der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Strukturen, die im <strong>rgcolumncreate</strong> -Member der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> -Struktur angegeben sind, wurde nicht auf sizeof (JET_COLUMNCREATE) festgelegt.</p></li>
<li><p>Der <strong>cbkey</strong> -Member einer <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur ist auf 0 (null) festgelegt.</p></li>
<li><p>Der <strong>cbStruct</strong> -Member einer <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur ist nicht auf sizeof (JET_INDEXCREATE) festgelegt.</p></li>
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
<td><p>Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen. Eine Tabelle kann nicht mehr als JET_ccolFixedMost fester Spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost markierte Spalten aufweisen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationFail</p></td>
<td><p>Fehler beim Versuch, eine Unicode-Spalte zu normalisieren. Dies kann darauf zurückzuführen sein, dass die Systemressourcen nicht mehr ausreichen.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Der Name **JetCreateTableColumnIndex2** stammt aus der Reihenfolge der Erstellung der Objekte: er erstellt zuerst eine Tabelle, Spalten und schließlich Indizes. **JetCreateTableColumnIndex2** erstellt eine Tabelle mit einem anfänglichen Satz von Spalten und Indizes. Weitere Spalten und Indizes können mit [jetaddcolumn](./jetaddcolumn-function.md), [jetdeletecolumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [jetkreateindex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md)und [jetdeleteindex](./jetdeleteindex-function.md)dynamisch hinzugefügt und entfernt werden.

Wie [jetopentable](./jetopentable-function.md), wenn die Anwendung mit der zurückgegebenen *TableID* ausgeführt wird, sollte Sie in der Regel mit [jetclosetable](./jetclosetable-function.md)geschlossen werden.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista oder Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008 oder Windows Server 2003.</p></td>
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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>JetCreateTableColumnIndex2W</strong> (Unicode) und <strong>JetCreateTableColumnIndex2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_CBTYP](./jet-cbtyp.md)  
[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[Jetaddcolumn](./jetaddcolumn-function.md)  
[Jetkreateingedex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[Jetkreatetable](./jetcreatetable-function.md)  
[Jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)  
[Jetdeletecolumn](./jetdeletecolumn-function.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
