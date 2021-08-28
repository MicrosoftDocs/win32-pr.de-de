---
description: Weitere Informationen finden Sie unter JetCreateIndex2-Funktion.
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
ms.openlocfilehash: fc11fe1e5d2b4d6f14ad77cb98434b0daf6b81f1
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987453"
---
# <a name="jetcreateindex2-function"></a>JetCreateIndex2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcreateindex2-function"></a>JetCreateIndex2-Funktion

Die **JetCreateIndex2-Funktion** erstellt Indizes für Daten in einer ESE-Datenbank, mit denen bestimmte Daten schnell gefunden werden können.

```cpp
    JET_ERR JET_API JetCreateIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*tableid*

Die Tabelle, für die der Index erstellt wird.

*pindexcreate*

Ein Array von [JET_INDEXCREATE](./jet-indexcreate-structure.md) Strukturen, von denen jede einen zu erstellenden Index definiert.

*cIndexCreate*

Die Anzahl der Elemente im *Array pindexcreate.*

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errCannotIndex</p> | <p>Es wurde versucht, eine Escrow-Update- oder SLV-Spalte zu indizieren (beachten Sie, dass SLV-Spalten veraltet sind).</p> | 
| <p>JET_errColumnNotFound</p> | <p>Es wurde versucht, eine Indizierung über eine nicht vorhandene Spalte zu erstellen. Der Versuch, eine nicht vorhandene Spalte bedingt zu indizieren, kann ebenfalls zu diesem Fehler führen.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Dieser Fehler wird zurückgegeben, wenn der <strong>ulDensity-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> auf eine Zahl kleiner als 20 oder mehr als 100 festgelegt ist.</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Es wurde versucht, zwei identische Indizes zu definieren.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Es wurde versucht, mehrere primäre Indizes für eine Tabelle anzugeben. Eine Tabelle muss genau einen primären Index haben. Wenn kein primärer Index angegeben wird, erstellt die Datenbank-Engine transparent einen.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Es wurde eine ungültige Indexdefinition angegeben. Einige der möglichen Gründe für den Empfang dieses Fehlers sind:</p><ul><li><p>Ein primärer Index ist bedingt (<strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> has JET_bitIndexPrimary set, and the <strong>cConditionalColumn</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> is greater than zero).</p></li><li><p>Windows Server 2003 und höher. Es wurde versucht, einen Tupelindex mit Tupelgrenzwerten zu erstellen, ohne jedoch Informationen im <strong>ptuplelimits-Member</strong> in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> zu übergeben (das heißt, <em>grbit</em> hat JET_bitIndexTupleLimits festgelegt, aber der <strong>ptuplelimits-Zeiger</strong> ist NULL).</p></li><li><p>Übergeben einer ungültigen Schlüsseldefinition im <strong>szKey-Member</strong> <a href="gg269186(v=exchg.10).md">der</a> JET_INDEXCREATE Struktur. Unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> finden Sie eine Erörterung gültiger Definitionen.</p></li><li><p>Festlegen des <strong>cbVarSegMac-Mitglieds</strong> <a href="gg269186(v=exchg.10).md">in</a> JET_INDEXCREATE auf größer als JET_cbPrimaryKeyMost (für einen primären Index) oder größer als JET_cbSecondaryKeyMost (für einen sekundären Index).</p></li><li><p>Übergeben einer ungültigen Kombination für einen benutzerdefinierten Unicode-Index (einer, bei dem das JET_bitIndexUnicode-Bit im <strong>Grbit-Member</strong> von <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE.</a> Einige häufige Ursachen können sein, dass das Pidxunicode-Feld der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> NULL ist oder die in der pidxunicode-Struktur angegebene LCID ungültig ist.</p></li><li><p>Angeben einer mehrwertigen Spalte für einen primären Index.</p></li><li><p>Es wird versucht, zu viele bedingte Spalten zu indizieren. Das <strong>cConditionalColumn-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> darf nicht größer als JET_ccolKeyMost.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP und höher. Eine <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS-Struktur</a> wurde angegeben, und ihre Grenzwerte werden nicht unterstützt. Weitere Informationen finden Sie im Abschnitt "Hinweise" <a href="gg269207(v=exchg.10).md">der JET_TUPLELIMITS</a> Struktur.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP und höher. Ein Tupelindex kann nicht eindeutig sein (<em>grbit</em> darf nicht sowohl über JET_bitIndexTuples als auch JET_bitIndexUnique verfügen).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP und höher. Ein Tupelindex kann sich nur über einer einzelnen Spalte (d. h. das <strong>Grbit-Element</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> hat JET_bitIndexTuples festgelegt, und das <strong>szKey-Element</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> gibt mehr als eine Spalte an).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP und höher. Ein Tupelindex kann kein primärer Index sein (d. h. das <strong>Grbit-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexTuples haben).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP und höher. Ein Tupelindex kann nur für eine Text- oder Unicode-Spalte verwendet werden. Der Versuch, andere Spalten (z. B. binäre Spalten) zu indizieren, führt zu JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP und höher. Ein Tupelindex lässt das Festlegen des <strong>cbVarSegMac-JET_INDEXCREATE</strong> <a href="gg269186(v=exchg.10).md">der</a> Struktur nicht zu.</p> | 
| <p>JET_errInTransaction</p> | <p>Es wurde versucht, während einer Transaktion einen Index ohne Versionsinformationen zu erstellen.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Die Indexdefinition ist ungültig, <strong>da das grbit-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> inkonsistente Werte enthält. Mögliche Gründe:</p><ul><li><p>Für einen primären Index wurde ein Ignore-Bit angegeben (JET_bitIndexPrimary wurde mit einem der JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull oder JET_bitIndexIgnoreFirstNull).</p></li><li><p>Ein leerer Index ignoriert keine NULL-Felder (d. h., das <strong>Grbit-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> JET_bitIndexEmpty festgelegt, aber nicht JET_bitIndexIgnoreAnyNull festgelegt).</p></li><li><p>Übergeben einer <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> struktur mit einem ungültigen <strong>Grbit-Member.</strong> Siehe <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li></ul><p>Wenn mehrere Indizes gleichzeitig erstellt werden (d. h., wenn der <em>cIndexCreate-Parameter</em> größer als eins ist), darf keiner der Indizes eines der folgenden Bits enthalten:</p><ul><li><p>JET_bitIndexPrimary</p></li><li><p>JET_bitIndexUnversioned</p></li><li><p>JET_bitIndexEmpty</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Eine ungültige Locale ID (LCID) wurde übergeben (entweder über das <strong>lcid-Member</strong> in der <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX-Struktur,</a> auf das das <strong>pidxunicode-Member</strong> in der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> einen Zeiger enthält, oder über den <strong>lcid-Member</strong> der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur).</a></p> | 
| <p>JET_errInvalidName</p> | <p>Es wurde ein ungültiger Indexname angegeben. Weitere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> sie unter .</p> | 
| <p>JET_errInvalidParameter</p> | <p>Ein ungültiger Parameter wurde an die API übergeben. Dieser Fehler kann unter anderem aus folgenden Gründen zurückgegeben werden:</p><ul><li><p>Das <strong>cbKey-Feld</strong> einer <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ist auf 0 (null) festgelegt.</p></li><li><p>Der <strong>cbStruct-Member</strong> <a href="gg269186(v=exchg.10).md">einer</a> JET_INDEXCREATE ist nicht auf sizeof( JET_INDEXCREATE )<a href="gg269186(v=exchg.10).md">festgelegt.</a></p></li></ul> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Beim Versuch, eine Unicode-Spalte zu normalisieren, ist ein Fehler aufgetreten. Dies kann dadurch verursacht werden, dass nicht mehr alle Systemressourcen verfügbar sind.</p> | 



#### <a name="remarks"></a>Bemerkungen

Der Rückgabewert wird JET_errSuccess erfolgreichen Abschluss aller angegebenen Indizes angegeben.

**JetCreateIndex2** durch iteriert die in **pindexcreate** angegebenen Indizes und wird manchmal beim ersten Fehler abgebrochen. Alle Indizes nach dem ersten Index mit einem Fehler wurden möglicherweise nicht versucht, obwohl der **err-Member** der JET_INDEXCREATE -Struktur JET_errSuccess. [](./jet-indexcreate-structure.md)

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetCreateIndex2W</strong> (Unicode) und <strong>JetCreateIndex2A</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
