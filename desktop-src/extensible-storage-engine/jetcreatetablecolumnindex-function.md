---
description: 'Weitere Informationen zu: JetCreateTableColumnIndex-Funktion'
title: JetCreateTableColumnIndex-Funktion
TOCTitle: JetCreateTableColumnIndex Function
ms:assetid: 9192614b-20a6-40fb-906a-51fc057e7483
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269343(v=EXCHG.10)
ms:contentKeyID: 32765632
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndexA
- JetCreateTableColumnIndexW
- JetCreateTableColumnIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a95f4c5854c672f3ebd0b8b231ca6bdddbca0801
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467207"
---
# <a name="jetcreatetablecolumnindex-function"></a>JetCreateTableColumnIndex-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcreatetablecolumnindex-function"></a>JetCreateTableColumnIndex-Funktion

Die **JetCreateTableColumnIndex-Funktion** erstellt eine Tabelle in einer ESE-Datenbank mit einem anfänglichen Satz von Indizes und einem anfänglichen Satz von Spalten aus einem Array von [JET_TABLECREATE](./jet-tablecreate-structure.md) Strukturen. Der Name **JetCreateTableColumnIndex** stammt aus der Reihenfolge der Erstellung der Objekte. Zunächst werden eine Tabelle, Spalten und schließlich Indizes erstellt.

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE* ptablecreate
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*Dbid*

Der Datenbankbezeichner, der für den API-Aufruf verwendet werden soll.

*ptablecreate*

Ein Zeiger auf eine [JET_TABLECREATE](./jet-tablecreate-structure.md) Struktur, die die zu erstellende Tabelle definiert. Weitere Informationen finden [Sie unter JET_TABLECREATE.](./jet-tablecreate-structure.md)

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>Die Rückruffunktion konnte nicht aufgelöst werden. Die DLL wurde möglicherweise nicht gefunden, oder die Funktion in der DLL wurde möglicherweise nicht gefunden. Wenn eine ausreichende Protokollierung aktiviert ist, enthält das Ereignisprotokoll weitere Details.</p> | 
| <p>JET_errCannotIndex</p> | <p>Es wurde versucht, eine Indizierung über eine Escrow-Update- oder SLV-Spalte zu erstellen (beachten Sie, dass SLV-Spalten veraltet sind).</p> | 
| <p>JET_errCannotNestDDL</p> | <p>Wenn ptablecreate- &gt; grbit JET_bitTableCreateTemplateTable angibt, ptablecreate- &gt; szTemplateTableName jedoch auf NULL festgelegt ist.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Eine Spalte ist bereits vorhanden.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Es wurde versucht, eine indizierte Spalte für eine nicht vorhandene Spalte zu verwenden. Der Versuch, eine bedingte Indizierung für eine nicht vorhandene Spalte zu erstellen, kann auch diesen Fehler erzeugen.</p> | 
| <p>JET_errColumnRedundant</p> | <p>Es wurde versucht, eine redundante Spalte hinzuzufügen. Es sollte nicht mehr als eine Spalte für die automatische Inkrementierung und nicht mehr als eine Versionsspalte pro Tabelle vorhanden sein.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Dieser Fehler wird zurückgegeben, wenn der <strong>ulDensity-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> auf eine Zahl kleiner als 20 oder mehr als 100 festgelegt ist.</p> | 
| <p>JET_errDDLNotInheritable</p> | <p>Gibt an, dass die Im <strong>szTemplateTableName-Element</strong> der <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> -Struktur benannte Tabelle nicht als Vorlagentabelle markiert wurde (d.b. diese Tabelle nicht JET_bitTableCreateTemplateTable festgelegt hat).</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Es wurde versucht, zwei identische Indizes zu definieren.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Es wurde versucht, mehr als einen primären Index für eine Tabelle anzugeben. Eine Tabelle muss genau einen primären Index aufweisen. Wenn kein primärer Index angegeben wird, erstellt die Datenbank-Engine transparent einen.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Es wurde eine ungültige Indexdefinition angegeben. Einige der möglichen Gründe für den Empfang dieses Fehlers sind:</p><ul><li><p>Ein primärer Index ist bedingt (das heißt, der <strong>Grbitmember</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> hat JET_bitIndexPrimary festgelegt, und <strong>der cConditionalColumn-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> ist größer als 0 (null).</p></li><li><p>Windows Server 2003 und höher. Es wurde versucht, einen Tupelindex mit Tupelgrenzwerten zu erstellen, aber ohne das <strong>Ptuplelimits-Element</strong> in der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur zu übergeben (d.b. das <strong>Grbit-Element</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> hat JET_bitIndexTupleLimits festgelegt, aber der <strong>Ptuplelimitzeiger</strong> ist NULL).</p></li><li><p>Übergeben einer ungültigen Schlüsseldefinition im <strong>szKey-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur.</a> Eine Erläuterung gültiger Definitionen finden Sie unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE.</a></p></li><li><p>Das Festlegen des <strong>cbVarSegMac-Members</strong> in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ist größer als JET_cbPrimaryKeyMost (für einen primären Index) oder größer als JET_cbSecondaryKeyMost (für einen sekundären Index).</p></li><li><p>Übergeben einer ungültigen Kombination für einen benutzerdefinierten Unicode-Index (einer, für den das JET_bitIndexUnicode Bit im <strong>grbit-Member</strong> von <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>festgelegt ist). Einige häufige Ursachen sind der <strong>Pidxunicode-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur NULL ist oder die in der <strong>pidxunicode-Struktur</strong> angegebene LCID ungültig ist.</p></li><li><p>Angeben einer mehrwertigen Spalte für einen primären Index.</p></li><li><p>Versuch, zu viele bedingte Spalten zu indizierung. Der <strong>cConditionalColumn-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> darf nicht größer als JET_ccolKeyMost sein.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP und höher. Es wurde <a href="gg269207(v=exchg.10).md">eine JET_TUPLELIMITS</a> -Struktur angegeben, und ihre Grenzwerte werden nicht unterstützt. Weitere Informationen finden Sie <a href="gg269207(v=exchg.10).md"></a> im Abschnitt "Hinweise" der JET_TUPLELIMITS-Struktur.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP und höher. Ein Tupelindex kann nicht eindeutig sein (das heißt, das <em>Grbit-Element</em> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexUnique festgelegt sein).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP und höher. Ein Tupelindex kann sich nur über einer einzelnen Spalte befinden (d.amp;quot;, wenn das <strong>grbit-Element</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> JET_bitIndexTuples festgelegt ist und das <strong>szKey-Element</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur mehr als eine Spalte angibt).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP und höher. Ein Tupelindex kann kein primärer Index sein (d.amp;quot;das <strong>grbit-Element</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexTuples festgelegt sein).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP und höher. Ein Tupelindex kann sich nur in einer Text- oder Unicode-Spalte befinden. Der Versuch, andere Spalten (z. B. binäre Spalten) zu indizieren, führt zu JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP und höher. Ein Tupelindex lässt nicht zu, dass der <strong>cbVarSegMac-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> festgelegt wird.</p> | 
| <p>JET_errInTransaction</p> | <p>Es wurde versucht, während einer Transaktion einen Index ohne Versionsinformationen zu erstellen.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>Der <strong>cp-Member</strong> der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE-Struktur</a> wurde nicht auf eine gültige Codepage festgelegt. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Der <strong>Coltypmember</strong> der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE-Struktur</a> wurde nicht auf einen gültigen Spaltentyp festgelegt.</p> | 
| <p>JET_errInvalidCreateIndex</p> | <p>Einige der Gründe für diesen Fehler können auftreten:</p><ul><li><p>Der <strong>rgindexcreate-Member</strong> der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2-Struktur</a> wurde auf NULL festgelegt.</p></li><li><p>Der <strong>rgcolumncreate-Member</strong> der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2-Struktur</a> wurde auf NULL festgelegt.</p></li><li><p>Der <strong>cbStruct-Member</strong> einer <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> wurde nicht auf einen gültigen Wert festgelegt.</p></li></ul> | 
| <p>JET_errInvalidgrbit</p> | <p>Eine ungültige Kombination von <strong>grbit-Membern</strong> wurde in <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> oder <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>angegeben.</p><p>Die Indexdefinition ist ungültig, da der <strong>grbit-Member</strong> inkonsistente Werte enthält. Mögliche Gründe:</p><ul><li><p>Für einen primären Index wurde ein ignore-Bit angegeben (d. h. JET_bitIndexPrimary wurde mit JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull oder JET_bitIndexIgnoreFirstNull).</p></li><li><p>Ein leerer Index ignoriert keine NULL-Member (d. h., das <strong>Grbit-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> JET_bitIndexEmpty festgelegt, aber nicht JET_bitIndexIgnoreAnyNull festgelegt).</p></li><li><p>Übergeben einer <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> struktur mit einem ungültigen <strong>Grbit-Member.</strong></p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Eine ungültige Locale ID (LCID) wurde übergeben (entweder über den <strong>lcid-Member</strong> der <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX-Struktur,</a> auf den das <strong>pidxunicode-Member</strong> in der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> verweist, oder über das <strong>lcid-Feld</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur).</a></p> | 
| <p>JET_errInvalidParameter</p> | <p>Es wurde ein ungültiger Parameter angegeben. Mögliche Gründe:</p><ul><li><p>Der <strong>rgcolumncreate-Member</strong> der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> ist NULL.</p></li><li><p>Der <strong>cbStruct-Member</strong> einer der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE-Strukturen,</a> die im <strong>rgcolumncreate-Member</strong> der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2-Struktur</a> angegeben sind, wurde nicht auf sizeof( JET_COLUMNCREATE) festgelegt.</p></li><li><p>Der <strong>cbKey-Member</strong> einer <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> ist auf 0 (null) festgelegt.</p></li><li><p>Der <strong>cbStruct-Member</strong> einer <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> ist nicht auf sizeof( JET_INDEXCREATE) festgelegt.</p></li></ul> | 
| <p>JET_errRecordTooBig</p> | <p>Der Datensatz ist zu groß. Die Summe des <strong>cbMax-Members</strong> der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE-Struktur</a> für alle festen Spalten darf einen bestimmten Wert nicht überschreiten.</p> | 
| <p>JET_errTableDuplicate</p> | <p>Die Tabelle ist bereits vorhanden.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen. Eine Tabelle kann nicht mehr als JET_ccolFixedMost Spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost spalten enthalten.</p> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Beim Versuch, eine Unicode-Spalte zu normalisieren, ist ein Fehler aufgetreten. Dies kann dadurch verursacht werden, dass nicht mehr alle Systemressourcen verfügbar sind.</p> | 



#### <a name="remarks"></a>Hinweise

Der Aufruf von **JetCreateTableColumnIndex** ist identisch mit dem Aufrufen von [JetCreateTableColumnIndex2,](./jetcreatetablecolumnindex2-function.md)bei dem jedes Feld in der [JET_TABLECREATE2-Struktur](./jet-tablecreate2-structure.md) den Wert des entsprechenden Felds von JET_TABLECREATE mit den folgenden [Ausnahmen](./jet-tablecreate-structure.md)enthält:

  - JET_TABLECREATE2.cbStruct auf sizeof( JET_TABLECREATE2)

  - JET_TABLECREATE2.szCallback auf NULL festgelegt

  - JET_TABLECREATE2.cbtyp auf 0 festgelegt

Weitere [Informationen finden Sie unter JetCreateTableColumnIndex2.](./jetcreatetablecolumnindex2-function.md)

Wenn [die Anwendung wie JetOpenTable](./jetopentable-function.md)die zurückgegebene *tableid* verwendet, sollte sie in der Regel mit [JetCloseTable geschlossen werden.](./jetclosetable-function.md)

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetCreateTableColumnIndexW</strong> (Unicode) und <strong>JetCreateTableColumnIndexA</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex]()  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
