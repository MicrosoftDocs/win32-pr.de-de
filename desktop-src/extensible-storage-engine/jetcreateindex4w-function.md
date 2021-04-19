---
description: 'Weitere Informationen finden Sie hier: JetCreateIndex4W-Funktion'
title: JetCreateIndex4W-Funktion
TOCTitle: JetCreateIndex4W Function
ms:assetid: 968745a2-66ce-4c7f-ab5b-43282adc5313
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835044(v=EXCHG.10)
ms:contentKeyID: 49894666
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a4c7671cbe361b6214552f4c611cd1706c0e48d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363268"
---
# <a name="jetcreateindex4w-function"></a>JetCreateIndex4W-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetCreateIndex4W** -Funktion erstellt Indizes für Daten in einer ESE-Datenbank (Extensible Storage Engine), die zum schnellen Auffinden spezifischer Daten verwendet werden kann.

Die **JetCreateIndex4W** -Funktion wurde im Windows 8-Betriebssystem eingeführt.

``` c++
JET_ERR JET_API JetCreateIndex4W(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_INDEXCREATE2* pindexcreate,
  __in          unsigned long cIndexCreate
);
```

### <a name="parameters"></a>Parameter

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*TableID*

Die Tabelle, für die der Index erstellt wird.

*pindexcreate*

Ein Array von [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) -Strukturen, von denen jede einen zu erstellenden Index definiert.

*cindexcreate*

Die Anzahl der Elemente im *pindexcreate* -Array.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) -Datentyp mit einem der in der folgenden Tabelle aufgelisteten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>JET_errCannotIndex</p></td>
<td><p>Es wurde versucht, über eine Spalte vom Typ "Escrow-Update" oder "SLV" zu indizieren (Beachten Sie, dass SLV-Spalten veraltet sind).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Es wurde versucht, einen Index für eine nicht vorhandene Spalte zu indizieren. Der Versuch, bedingt eine Indizierung über eine nicht vorhandene Spalte durchführen zu können, kann ebenfalls diesen Fehler verursachen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>Dieser Fehler wird zurückgegeben, wenn der <strong>uldensity</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur auf eine Zahl kleiner als 20 oder größer als 100 festgelegt ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexDuplicate</p></td>
<td><p>Es wurde versucht, zwei identische Indizes zu definieren.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexHasPrimary</p></td>
<td><p>Es wurde versucht, mehr als einen primären Index für eine Tabelle anzugeben. Eine Tabelle muss genau einen primären Index aufweisen. Wenn kein primärer Index angegeben ist, wird von der Datenbank-Engine eine transparente Erstellung erstellt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Es wurde eine ungültige Index Definition angegeben. Im folgenden sind einige mögliche Ursachen für diesen Fehler aufgeführt:</p>
<ul>
<li><p>Ein primärer Index ist bedingt (<strong>grbit</strong> -Member von <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> <strong>JET_bitIndexPrimary</strong> festgelegt haben, und der <strong>cconditionalcolumn</strong> -Member von <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ist größer als 0 (null)).</p></li>
<li><p>Gilt für Windows-Versionen ab Windows Server 2003. Es wurde versucht, einen Tupelindex mit tupellimits zu erstellen, aber ohne Informationen im <strong>ptuplelimits</strong> -Member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> zu übergeben (das heißt, dass für <em>grbit</em> <strong>JET_bitIndexTupleLimits</strong> festgelegt ist, der <strong>ptuplelimits</strong> -Zeiger aber NULL ist).</p></li>
<li><p>Übergeben einer ungültigen Schlüssel Definition im <strong>szkey</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur. Informationen zu gültigen Definitionen finden Sie unter <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</p></li>
<li><p>Das Festlegen des <strong>cbvarsegmac</strong> -Members in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> auf größer als <strong>JET_cbPrimaryKeyMost</strong> (für einen primären Index) oder größer als <strong>JET_cbSecondaryKeyMost</strong> (für einen sekundären Index).</p></li>
<li><p>Übergeben einer ungültigen Kombination für einen benutzerdefinierten Unicode-Index (einen, bei dem das <strong>JET_bitIndexUnicode</strong> Bit im <strong>grbit</strong> -Member von <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>festgelegt ist). Einige häufige Gründe können sein, dass das pidxunicode-Feld der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur NULL ist oder die in der pidxunicode-Struktur angegebene LCID ungültig ist.</p></li>
<li><p>Angeben einer mehrwertigen Spalte für einen primären Index.</p></li>
<li><p>Es wird versucht, zu viele bedingte Spalten zu indizieren. Der <strong>cconditionalcolumn</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur darf nicht größer als <strong>JET_ccolKeyMost</strong>sein.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Gilt für Windows-Versionen ab Windows XP. Es wurde eine <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur angegeben, und ihre Grenzen werden nicht unterstützt. Weitere Informationen finden Sie im Abschnitt "Hinweise" in der <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> -Struktur.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>Gilt für Windows-Versionen ab Windows XP. Ein Tupelindex kann nicht eindeutig sein (für<em>grbit</em> dürfen nicht sowohl <strong>JET_bitIndexTuples</strong> als auch <strong>JET_bitIndexUnique</strong> festgelegt sein).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>Gilt für Windows-Versionen ab Windows XP. Ein Tupelindex kann nur über eine einzelne Spalte verfügen (d. h., der <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur verfügt über <strong>JET_bitIndexTuples</strong> Menge, und der <strong>szkey</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur gibt mehr als eine Spalte an).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>Gilt für Windows-Versionen ab Windows XP. Bei einem Tupelindex kann es sich nicht um einen primären Index handeln (d. h., der <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur darf nicht sowohl <strong>JET_bitIndexPrimary</strong> als auch <strong>JET_bitIndexTuples</strong> festgelegt werden).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Gilt für Windows-Versionen ab Windows XP. Ein Tupelindex kann nur für eine Text-oder Unicode-Spalte gelten. Der Versuch, andere Spalten zu indizieren (z. b. binäre Spalten), führt zu <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Gilt für Windows-Versionen ab Windows XP. Ein Tupelindex lässt nicht zu, dass der <strong>cbvarsegmac</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur festgelegt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInTransaction</p></td>
<td><p>Es wurde versucht, einen Index ohne Versionsinformationen zu erstellen, während eine Transaktion durchgeführt wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Die Index Definition ist ungültig, da der <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur inkonsistente Werte enthält. Folgende Ursachen sind möglich:</p>
<ul>
<li><p>Für einen primären Index wurde ein Ignore-Bit angegeben (JET_bitIndexPrimary mit einem <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>oder <strong>JET_bitIndexIgnoreFirstNull</strong>).</p></li>
<li><p>Ein leerer Index ignoriert keine NULL-Felder (d. h., das <strong>grbit</strong> -Element der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur hat <strong>JET_bitIndexEmpty</strong> festgelegt, aber nicht <strong>JET_bitIndexIgnoreAnyNull</strong> festgelegt).</p></li>
<li><p>Übergeben einer <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> -Struktur mit einem ungültigen <strong>grbit</strong> -Member. Siehe <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li>
</ul>
<p>Wenn mehrere Indizes gleichzeitig erstellt werden (d. h., wenn der <em>cindexcreate</em> -Parameter größer als 1 ist), kann keiner der Indizes einen der folgenden Bits enthalten:</p>
<ul>
<li><p><strong>JET_bitIndexPrimary</strong></p></li>
<li><p><strong>JET_bitIndexUnversioned</strong></p></li>
<li><p><strong>JET_bitIndexEmpty</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Es wurde eine ungültige Gebiets Schema-ID (LCID) übergeben (entweder über den <strong>LCID</strong> -Member in der <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> -Struktur, in der das <strong>pidxunicode</strong> -Element in der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur einen Zeiger auf enthält, oder über den <strong>LCID</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName</p></td>
<td><p>Es wurde ein ungültiger Indexname angegeben. Weitere Informationen finden Sie unter <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Ein ungültiger Parameter wurde an die API übergeben. Im folgenden sind einige Gründe aufgeführt, warum dieser Fehler zurückgegeben werden kann:</p>
<ul>
<li><p>Das <strong>cbkey</strong> -Feld einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur ist auf 0 (null) festgelegt.</p></li>
<li><p>Der <strong>cbStruct</strong> -Member einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur ist nicht auf sizeof (JET_INDEXCREATE2) festgelegt.</p></li>
</ul></td>
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

Die **JetCreateIndex4W** -Funktion durchläuft die im *pindexcreate* -Parameter angegebenen Indizes und bricht bei dem ersten Fehler manchmal ab. Möglicherweise wurden keine Indizes nach dem ersten Index mit einem Fehler versucht, obwohl der **Err** -Member der [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) Struktur JET_errSuccess enthält.

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

[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)  
[Jetkreateingedex](./jetcreateindex-function.md)  
[Jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JET_SPACEHINTS](./jet-spacehints-structure.md)
