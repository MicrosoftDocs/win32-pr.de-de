---
description: 'Weitere Informationen zu: JetCreateTable-Funktion'
title: JetCreateTable-Funktion
TOCTitle: JetCreateTable Function
ms:assetid: 28455b8b-0000-4bd5-a3ca-e1ef0446ee07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269210(v=EXCHG.10)
ms:contentKeyID: 32765513
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableW
- JetCreateTable
- JetCreateTableA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e06e4c2d0cfa55ff85279b634449fd313eb7570
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985023"
---
# <a name="jetcreatetable-function"></a>JetCreateTable-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcreatetable-function"></a>JetCreateTable-Funktion

Die **JetCreateTable-Funktion** erstellt eine leere Tabelle in einer ESE-Datenbank.

```cpp
    JET_ERR JET_API JetCreateTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          unsigned long lPages,
      __in          unsigned long lDensity,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der zu verwendende Datenbanksitzungskontext.

*Dbid*

Der zu verwendende Datenbankbezeichner.

*szTableName*

Der Name des zu erstellende Indexes.

Der Name muss gemäß den folgenden Regeln formatiert werden:

  - Ist kleiner als JET_cbNameMost, ohne den abschließenden NULL-Wert zu enthalten.

  - Aus den folgenden Zeichen bestehen: 0 bis 9, A bis Z, a bis z und alle anderen Interpunktion außer " \! " " (Ausrufezeichen), "," (Komma), \[ " " (öffnende eckige Klammer) und \] " (schließende Klammer) – das heißt, ASCII-Zeichen 0x20, 0x22 durch 0x2d, 0x2f durch 0x5a, 0x5c, 0x5d bis 0x7f.

  - Beginnen Sie nicht mit einem Leerzeichen.

  - Muss aus mindestens einem Zeichen ohne Leerzeichen bestehen.

*lPages*

Die anfängliche Anzahl der Datenbankseiten, die für die Tabelle zugeordnet werden sollen. Wenn Sie eine Zahl angeben, die größer als 1 ist, kann die Fragmentierung reduziert werden, wenn viele Zeilen in diese Tabelle eingefügt werden.

*lDensity*

Die Tabellendichte in Prozent. Die Zahl muss entweder 0 oder im Bereich von 20 bis 100 liegen. Die Übergabe von 0 bedeutet, dass der Standardwert verwendet werden soll. Der Standardwert beträgt 80.

*Ptableid*

Bei Erfolg wird der Tabellenbezeichner in diesem Feld zurückgegeben. Der Wert ist nicht definiert, wenn die API keine JET_errSuccess zurückgibt.

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
| <p>JET_errDensityInvalid</p> | <p>Im <em>ulDensity-Member</em> in der <a href="gg294146(v=exchg.10).md">JET_TABLECREATE-</a> oder <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2-Struktur</a> wurde eine ungültige Dichte übergeben.</p> | 
| <p>JET_errDDLNotInheritable</p> | <p>Gibt an, dass die Im <strong>szTemplateTableName-Element</strong> der <a href="gg294146(v=exchg.10).md">JET_TABLECREATE-Struktur</a> benannte Tabelle kein als Vorlagentabelle markierter war (d.b. diese Tabelle hat nicht JET_bitTableCreateTemplateTable festgelegt).</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Es wurde versucht, zwei identische Indizes zu definieren.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Es wurde versucht, mehr als einen primären Index für eine Tabelle anzugeben. Eine Tabelle muss genau einen primären Index aufweisen. Wenn kein primärer Index angegeben wird, erstellt die Datenbank-Engine transparent einen.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Es wurde eine ungültige Indexdefinition angegeben. Einige der möglichen Gründe für den Empfang dieses Fehlers sind:</p><ul><li><p>Ein primärer Index ist bedingt (d.amp;#160;B. der <strong>grbit-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> hat JET_bitIndexPrimary festgelegt, und <strong>cConditionalColumn-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> ist größer als 0 (null).</p></li><li><p>Windows Server 2003 und höher. Es wurde versucht, einen Tupelindex mit Tupelgrenzwerten zu erstellen, ohne jedoch den <strong>Ptuplelimits-Member</strong> in der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur zu übergeben (d. b. das <strong>Grbit-Element</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> hat JET_bitIndexTupleLimits festgelegt, aber der <strong>Ptuplelimitzeiger</strong> ist NULL).</p></li><li><p>Übergeben einer ungültigen Schlüsseldefinition im <strong>szKey-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur.</a> Eine Erläuterung gültiger Definitionen finden Sie unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE.</a></p></li><li><p>Legen Sie das <strong>element cbVarSegMac</strong> in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> auf größer als JET_cbPrimaryKeyMost (für einen primären Index) oder größer als JET_cbSecondaryKeyMost (für einen sekundären Index) fest.</p></li><li><p>Übergeben einer ungültigen Kombination für einen benutzerdefinierten Unicode-Index (einer, für den das JET_bitIndexUnicode Bit im <strong>grbit-Member</strong> von <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>festgelegt ist). Einige häufige Ursachen sind der <strong>pidxunicode-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur NULL ist, oder die in der <strong>pidxunicode-Struktur</strong> angegebene LCID ist ungültig.</p></li><li><p>Angeben einer mehrwertigen Spalte für einen primären Index.</p></li><li><p>Versuch, zu viele bedingte Spalten zu indizierung. Der <strong>cConditionalColumn-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> darf nicht größer als JET_ccolKeyMost sein.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP und höher. Es wurde <a href="gg269207(v=exchg.10).md">eine JET_TUPLELIMITS</a> -Struktur angegeben, und ihre Grenzwerte werden nicht unterstützt. Weitere Informationen finden Sie <a href="gg269207(v=exchg.10).md"></a> im Abschnitt "Hinweise" der JET_TUPLELIMITS-Struktur.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP und höher. Ein Tupelindex kann nicht eindeutig sein (das heißt, das <em>Grbit-Element</em> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexUnique festgelegt sein).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP und höher. Ein Tupelindex kann sich nur über einer einzelnen Spalte befinden (d.amp;quot;, wenn das <strong>grbit-Element</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> JET_bitIndexTuples festgelegt ist und das <strong>szKey-Element</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur mehr als eine Spalte angibt).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP und höher. Ein Tupelindex kann kein primärer Index sein (d.amp;quot;das <strong>grbit-Element</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexTuples festgelegt sein).</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP und höher. Ein Tupelindex lässt nicht zu, dass der <strong>cbVarSegMac-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> festgelegt wird.</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP und höher. Ein Tupelindex kann sich nur in einer Text- oder Unicode-Spalte befinden. Der Versuch, andere Spalten (z. B. binäre Spalten) zu indizieren, führt zu JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errInTransaction</p> | <p>Es wurde versucht, während einer Transaktion einen Index ohne Versionsinformationen zu erstellen.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>Der <strong>cp-Member</strong> der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE-Struktur</a> wurde nicht auf eine gültige Codepage festgelegt. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Der <strong>Coltypmember</strong> der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Struktur wurde nicht auf einen gültigen Spaltentyp festgelegt.</p> | 
| <p>JET_errInvalidCreateIndex</p> | <p>Einige der Gründe für diesen Fehler können auftreten:</p><ul><li><p>Der <strong>rgindexcreate-Member</strong> der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2-Struktur</a> wurde auf NULL festgelegt.</p></li><li><p>Der <strong>rgcolumncreate-Member</strong> der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2-Struktur</a> wurde auf NULL festgelegt.</p></li><li><p>Der <strong>cbStruct-Member</strong> einer <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> wurde nicht auf einen gültigen Wert festgelegt.</p></li></ul> | 
| <p>JET_errInvalidgrbit</p> | <p>Eine ungültige Kombination von <strong>grbit-Membern</strong> wurde in <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> oder <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>angegeben.</p><p>Die Indexdefinition ist ungültig, da der <strong>grbit-Member</strong> inkonsistente Werte enthält. Mögliche Gründe:</p><ul><li><p>Für einen primären Index wurde ein Ignore-Bit angegeben (d. b. JET_bitIndexPrimary wurde mit JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull oder JET_bitIndexIgnoreFirstNull übergeben).</p></li><li><p>Ein leerer Index ignoriert keine NULL-Member (das heißt, der <strong>grbit-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> hat JET_bitIndexEmpty festgelegt, verfügt jedoch nicht über JET_bitIndexIgnoreAnyNull).</p></li><li><p>Übergeben einer <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN-Struktur</a> mit einem ungültigen <strong>Grbitmember.</strong></p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Eine ungültige Gebietsschema-ID (LCID) wurde übergeben (entweder über den <strong>lcid-Member</strong> der <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX-Struktur,</a> auf den der <strong>Pidxunicode-Member</strong> in der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> zeigt, oder über das <strong>lcid-Feld</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur).</a></p> | 
| <p>JET_errInvalidParameter</p> | <p>Ein ungültiger Parameter wurde angegeben. Mögliche Gründe:</p><ul><li><p>Der <strong>rgcolumncreate-Member</strong> der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2-Struktur</a> ist NULL.</p></li><li><p>Der <strong>cbStruct-Member</strong> einer der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE-Strukturen,</a> die im <strong>rgcolumncreate-Member</strong> der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2-Struktur</a> angegeben sind, wurde nicht auf sizeof( JET_COLUMNCREATE ) festgelegt.</p></li><li><p>Der <strong>cbKey-Member</strong> einer <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> ist auf 0 (null) festgelegt.</p></li><li><p>Der <strong>cbStruct-Member</strong> einer <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> ist nicht auf sizeof( JET_INDEXCREATE ) festgelegt.</p></li></ul> | 
| <p>JET_errRecordTooBig</p> | <p>Der Datensatz ist zu groß. Die Summe des <strong>cbMax-Elements</strong> der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE-Struktur</a> für alle festen Spalten darf einen bestimmten Wert nicht überschreiten.</p> | 
| <p>JET_errTableDuplicate</p> | <p>Die Tabelle ist bereits vorhanden.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen. Eine Tabelle darf nicht mehr als JET_ccolFixedMost festen Spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost markierten Spalten enthalten.</p> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Fehler beim Normalisieren einer Unicode-Spalte. Dies kann dadurch verursacht werden, dass nicht mehr die Systemressourcen verfügbar sind.</p> | 



#### <a name="remarks"></a>Bemerkungen

**JetCreateTable** erstellt eine Tabelle, die keine Spalten enthält. Informationen zum Hinzufügen von Spalten finden Sie unter [JetAddColumn](./jetaddcolumn-function.md).

Intern ruft **JetCreateTable** [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)auf und füllt eine [JET_TABLECREATE2-Struktur](./jet-tablecreate2-structure.md) mit:

  - JET_TABLECREATE2.cbStruct = sizeof( JET_TABLECREATE2 )

  - JET_TABLECREATE2.szTableName = szTableName

  - JET_TABLECREATE2.ulPages = lPage

  - JET_TABLECREATE2.ulDensity = lDensity

  - JET_TABLECREATE2.tableid = JET_tableidNil

Alle anderen Felder der internen [JET_TABLECREATE2-Struktur](./jet-tablecreate2-structure.md) werden auf 0 (null) oder NULL festgelegt. Bei der Ausgabe wird *ptableid* auf JET_TABLECREATE2.tableid festgelegt.

Weitere Informationen finden Sie unter [JetCreateTableColumnIndex2.](./jetcreatetablecolumnindex2-function.md)

Wenn die Anwendung wie [JetOpenTable](./jetopentable-function.md)den zurückgegebenen **tableid-Member** aus der [JET_TABLECREATE2](./jet-tablecreate2-structure.md) Struktur verwendet, sollte sie in der Regel mit [JetCloseTable](./jetclosetable-function.md)geschlossen werden.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetCreateTableW</strong> (Unicode) und <strong>JetCreateTableA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
