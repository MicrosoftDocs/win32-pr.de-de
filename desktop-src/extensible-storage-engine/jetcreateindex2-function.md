---
description: 'Weitere Informationen finden Sie hier: JetCreateIndex2-Funktion'
title: JetCreateIndex2-Funktion
TOCTitle: JetCreateIndex2 Function
ms:assetid: 8810eaed-40cb-4561-aafc-9a9bbdb0d05b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269324(v=EXCHG.10)
ms:contentKeyID: 32765614
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex2W
- JetCreateIndex2A
- JetCreateIndex2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42c1eb8fa1bb7fa880cf7286a1ec472ddc7ba7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373201"
---
# <a name="jetcreateindex2-function"></a>JetCreateIndex2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcreateindex2-function"></a>JetCreateIndex2-Funktion

Die **JetCreateIndex2** -Funktion erstellt Indizes für Daten in einer ESE-Datenbank, die zum schnellen Auffinden spezifischer Daten verwendet werden kann.

```cpp
    JET_ERR JET_API JetCreateIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*TableID*

Die Tabelle, für die der Index erstellt wird.

*pindexcreate*

Ein Array von [JET_INDEXCREATE](./jet-indexcreate-structure.md) -Strukturen, von denen jede einen zu erstellenden Index definiert.

*cindexcreate*

Die Anzahl der Elemente im *pindexcreate* -Array.

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
<td><p>JET_errCannotIndex</p></td>
<td><p>Es wurde versucht, über eine Spalte vom Typ "Escrow-Update" oder "SLV" zu indizieren (Beachten Sie, dass SLV-Spalten veraltet sind).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Es wurde versucht, eine nicht vorhandene Spalte zu indizieren. Der Versuch, bedingt eine Indizierung über eine nicht vorhandene Spalte durchführen zu können, kann ebenfalls diesen Fehler verursachen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>Dieser Fehler wird zurückgegeben, wenn der <strong>uldensity</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur auf eine Zahl kleiner als 20 oder mehr als 100 festgelegt ist.</p></td>
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
<td><p>Es wurde eine ungültige Index Definition angegeben. Mögliche Ursachen für den Empfang dieses Fehlers:</p>
<ul>
<li><p>Ein primärer Index ist bedingt (<strong>grbit</strong> -Member von <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> JET_bitIndexPrimary festgelegt haben, und der <strong>cconditionalcolumn</strong> -Member von <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ist größer als 0 (null)).</p></li>
<li><p>Windows Server 2003 und höher. Es wurde versucht, einen Tupelindex mit tupellimits zu erstellen, aber ohne Informationen im <strong>ptuplelimits</strong> -Member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> zu übergeben (das heißt, dass <em>grbit</em> JET_bitIndexTupleLimits festgelegt ist, der <strong>ptuplelimits</strong> -Zeiger aber NULL ist).</p></li>
<li><p>Übergeben einer ungültigen Schlüssel Definition im <strong>szkey</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur. Eine Erörterung gültiger Definitionen finden Sie unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p></li>
<li><p>Das Festlegen des <strong>cbvarsegmac</strong> -Members in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> auf größer als JET_cbPrimaryKeyMost (für einen primären Index) oder größer als JET_cbSecondaryKeyMost (für einen sekundären Index).</p></li>
<li><p>Übergeben einer ungültigen Kombination für einen benutzerdefinierten Unicode-Index (einen, bei dem das JET_bitIndexUnicode Bit im <strong>grbit</strong> -Member von <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>festgelegt ist). Einige häufige Gründe können sein, dass das pidxunicode-Feld der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur NULL ist oder die in der pidxunicode-Struktur angegebene LCID ungültig ist.</p></li>
<li><p>Angeben einer mehrwertigen Spalte für einen primären Index.</p></li>
<li><p>Es wird versucht, zu viele bedingte Spalten zu indizieren. Der <strong>cconditionalcolumn</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur darf nicht größer als JET_ccolKeyMost sein.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Windows XP und höher. Es wurde eine <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur angegeben, und ihre Grenzen werden nicht unterstützt. Weitere Informationen finden Sie im Abschnitt "Hinweise" der <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>Windows XP und höher. Ein Tupelindex kann nicht eindeutig sein (für<em>grbit</em> dürfen nicht sowohl JET_bitIndexTuples als auch JET_bitIndexUnique festgelegt sein).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>Windows XP und höher. Ein Tupelindex kann nur über eine einzelne Spalte verfügen (d. h., der <strong>grbit</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur verfügt über JET_bitIndexTuples Menge, und der <strong>szkey</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur gibt mehr als eine Spalte an).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>Windows XP und höher. Bei einem Tupelindex kann es sich nicht um einen primären Index handeln (d. h., der <strong>grbit</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexTuples festgelegt werden).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Windows XP und höher. Ein Tupelindex kann nur für eine Text-oder Unicode-Spalte gelten. Der Versuch, andere Spalten zu indizieren (z. b. binäre Spalten), führt zu JET_errIndexTuplesTextColumnsOnly.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Windows XP und höher. Ein Tupelindex lässt nicht zu, dass der <strong>cbvarsegmac</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur festgelegt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInTransaction</p></td>
<td><p>Es wurde versucht, einen Index ohne Versionsinformationen zu erstellen, während eine Transaktion durchgeführt wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Die Index Definition ist ungültig, da der <strong>grbit</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur inkonsistente Werte enthält. Mögliche Ursachen:</p>
<ul>
<li><p>Für einen primären Index wurde ein Ignore-Bit angegeben (JET_bitIndexPrimary mit einem JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull oder JET_bitIndexIgnoreFirstNull).</p></li>
<li><p>Ein leerer Index ignoriert keine NULL-Felder (d. h., das <strong>grbit</strong> -Element der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur hat JET_bitIndexEmpty festgelegt, aber nicht JET_bitIndexIgnoreAnyNull festgelegt).</p></li>
<li><p>Übergeben einer <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> -Struktur mit einem ungültigen <strong>grbit</strong> -Member. Siehe <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li>
</ul>
<p>Wenn mehrere Indizes gleichzeitig erstellt werden (d. h., wenn der <em>cindexcreate</em> -Parameter größer als 1 ist), kann keiner der Indizes einen der folgenden Bits enthalten:</p>
<ul>
<li><p>JET_bitIndexPrimary</p></li>
<li><p>JET_bitIndexUnversioned</p></li>
<li><p>JET_bitIndexEmpty</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Es wurde eine ungültige Gebiets Schema-ID (LCID) übergeben (entweder über den <strong>LCID</strong> -Member in der <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> -Struktur, in der das <strong>pidxunicode</strong> -Element in der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur einen Zeiger auf enthält, oder über den <strong>LCID</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName</p></td>
<td><p>Es wurde ein ungültiger Indexname angegeben. Weitere Informationen finden Sie unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Ein ungültiger Parameter wurde an die API übergeben. Dieser Fehler kann aus folgenden Gründen zurückgegeben werden:</p>
<ul>
<li><p>Das <strong>cbkey</strong> -Feld einer <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur ist auf 0 (null) festgelegt.</p></li>
<li><p>Der <strong>cbStruct</strong> -Member einer <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur ist nicht auf sizeof (<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ) festgelegt.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationFail</p></td>
<td><p>Fehler beim Versuch, eine Unicode-Spalte zu normalisieren. Dies kann darauf zurückzuführen sein, dass die Systemressourcen nicht mehr ausreichen.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Der Rückgabewert wird nach erfolgreichem Abschluss aller angegebenen Indizes JET_errSuccess.

**JetCreateIndex2** durchläuft die in **pindexcreate** angegebenen Indizes und bricht bei dem ersten Fehler manchmal ab. Möglicherweise wurden keine Indizes nach dem ersten Index mit einem Fehler versucht, obwohl der **Err** -Member der [JET_INDEXCREATE](./jet-indexcreate-structure.md) Struktur JET_errSuccess enthält.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
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
<td><p>Implementiert als <strong>JetCreateIndex2W</strong> (Unicode) und <strong>JetCreateIndex2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[Jetkreateingedex](./jetcreateindex-function.md)  
[Jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
