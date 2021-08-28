---
description: 'Weitere Informationen zu: JetCreateIndex4W-Funktion'
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
ms.openlocfilehash: c79f1638645f0dcd7e4306f543a9ee15b9668843
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987443"
---
# <a name="jetcreateindex4w-function"></a>JetCreateIndex4W-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetCreateIndex4W-Funktion** erstellt Indizes für Daten in einer ESE-Datenbank (Extensible Storage Engine), die verwendet werden kann, um bestimmte Daten schnell zu finden.

Die **JetCreateIndex4W-Funktion** wurde im Windows 8 Betriebssystem eingeführt.

``` c++
JET_ERR JET_API JetCreateIndex4W(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_INDEXCREATE2* pindexcreate,
  __in          unsigned long cIndexCreate
);
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*tableid*

Die Tabelle, für die der Index erstellt wird.

*pindexcreate*

Ein Array von [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) Strukturen, von denen jede einen zu erstellenden Index definiert.

*cIndexCreate*

Die Anzahl der Elemente im *Array pindexcreate.*

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der in der folgenden Tabelle aufgeführten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errCannotIndex</p> | <p>Es wurde versucht, eine Indizierung über eine Escrow-Update- oder SLV-Spalte zu erstellen (beachten Sie, dass SLV-Spalten veraltet sind).</p> | 
| <p>JET_errColumnNotFound</p> | <p>Es wurde versucht, eine nicht vorhandene Spalte zu indizieren. Der Versuch, eine bedingte Indizierung für eine nicht vorhandene Spalte zu erstellen, kann auch diesen Fehler erzeugen.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Dieser Fehler wird zurückgegeben, wenn der <strong>ulDensity-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> auf eine Zahl kleiner als 20 oder größer als 100 festgelegt ist.</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Es wurde versucht, zwei identische Indizes zu definieren.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Es wurde versucht, mehr als einen primären Index für eine Tabelle anzugeben. Eine Tabelle muss genau einen primären Index aufweisen. Wenn kein primärer Index angegeben wird, erstellt die Datenbank-Engine transparent einen.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Es wurde eine ungültige Indexdefinition angegeben. Im Folgenden sind einige mögliche Gründe für diesen Fehler zu nennen:</p><ul><li><p>Ein primärer Index ist bedingt (<strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> has <strong>JET_bitIndexPrimary</strong> set, and the <strong>cConditionalColumn</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> is greater than zero).</p></li><li><p>Gilt für Versionen von Windows ab Windows Server 2003. Es wurde versucht, einen Tupelindex mit Tupelgrenzwerten zu erstellen, ohne jedoch Informationen in den <strong>Ptuplelimits-Membern</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> zu übergeben (das heißt, <em>grbit</em> hat <strong>JET_bitIndexTupleLimits</strong> festgelegt, aber der <strong>ptuplelimits-Zeiger</strong> ist NULL).</p></li><li><p>Übergeben einer ungültigen Schlüsseldefinition im <strong>szKey-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur.</a> Informationen zu gültigen Definitionen finden Sie unter <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</p></li><li><p>Festlegen des <strong>cbVarSegMac-Members</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> auf größer als <strong>JET_cbPrimaryKeyMost</strong> (für einen primären Index) oder größer als <strong>JET_cbSecondaryKeyMost</strong> (für einen sekundären Index).</p></li><li><p>Übergeben einer ungültigen Kombination für einen benutzerdefinierten Unicode-Index (einer, für den das <strong>JET_bitIndexUnicode</strong> Bit im <strong>grbit-Member</strong> von <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>festgelegt ist). Einige häufige Ursachen können darin bestehen, dass das Pidxunicode-Feld der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> NULL ist oder die in der pidxunicode-Struktur angegebene LCID ungültig ist.</p></li><li><p>Angeben einer mehrwertigen Spalte für einen primären Index.</p></li><li><p>Versuch, zu viele bedingte Spalten zu indizierung. Der <strong>cConditionalColumn-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> darf nicht größer als <strong>JET_ccolKeyMost</strong>sein.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Gilt für Versionen von Windows, die mit Windows XP beginnen. Es wurde <a href="gg269207(v=exchg.10).md">eine JET_TUPLELIMITS</a> -Struktur angegeben, und ihre Grenzwerte werden nicht unterstützt. Weitere Informationen finden Sie im Abschnitt <a href="gg269207(v=exchg.10).md"></a> "Hinweise" der JET_TUPLELIMITS-Struktur.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Gilt für Versionen von Windows, die mit Windows XP beginnen. Ein Tupelindex kann nicht eindeutig sein (<em>grbit</em> darf nicht sowohl <strong>JET_bitIndexTuples</strong> als auch <strong>JET_bitIndexUnique</strong> festgelegt sein).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Gilt für Versionen von Windows, die mit Windows XP beginnen. Ein Tupelindex kann sich nur über einer einzelnen Spalte befinden (das heißt, das <strong>grbit-Element</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> hat <strong>JET_bitIndexTuples</strong> festgelegt, und das <strong>szKey-Element</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> gibt mehr als eine Spalte an).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Gilt für Versionen von Windows, die mit Windows XP beginnen. Ein Tupelindex kann kein primärer Index sein (d.amp;n.b. darf das <strong>Grbit-Element</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> nicht sowohl <strong>JET_bitIndexPrimary</strong> als auch <strong>JET_bitIndexTuples</strong> festgelegt sein).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Gilt für Versionen von Windows, die mit Windows XP beginnen. Ein Tupelindex kann sich nur in einer Text- oder Unicode-Spalte befinden. Der Versuch, andere Spalten (z. B. binäre Spalten) zu indizieren, führt <strong>zu JET_errIndexTuplesTextColumnsOnly</strong>.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Gilt für Versionen von Windows, die mit Windows XP beginnen. Ein Tupelindex lässt nicht zu, dass der <strong>cbVarSegMac-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> festgelegt wird.</p> | 
| <p>JET_errInTransaction</p> | <p>Es wurde versucht, während einer Transaktion einen Index ohne Versionsinformationen zu erstellen.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Die Indexdefinition ist ungültig, da der <strong>grbit-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> inkonsistente Werte enthält. Folgende Gründe sind möglich:</p><ul><li><p>Für einen primären Index wurde ein Ignore-Bit angegeben (JET_bitIndexPrimary wurde mit einem der <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>oder <strong>JET_bitIndexIgnoreFirstNull</strong>) übergeben.</p></li><li><p>Ein leerer Index ignoriert keine NULL-Felder (d. b. <strong>grbit-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> hat <strong>JET_bitIndexEmpty</strong> festgelegt, verfügt jedoch nicht <strong>über JET_bitIndexIgnoreAnyNull).</strong></p></li><li><p>Übergeben einer <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN-Struktur</a> mit einem ungültigen <strong>Grbitmember.</strong> Siehe <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li></ul><p>Wenn mehrere Indizes gleichzeitig erstellt werden (d. b. wenn der <em>cIndexCreate-Parameter</em> größer als eins ist), darf keiner der Indizes eines der folgenden Bits enthalten:</p><ul><li><p><strong>JET_bitIndexPrimary</strong></p></li><li><p><strong>JET_bitIndexUnversioned</strong></p></li><li><p><strong>JET_bitIndexEmpty</strong></p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Eine ungültige Gebietsschema-ID (LCID) wurde übergeben (entweder über den <strong>lcid-Member</strong> in der <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX-Struktur,</a> auf den der <strong>pidxunicode-Member</strong> in der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> einen Zeiger auf enthält, oder über den <strong>lcid-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur).</a></p> | 
| <p>JET_errInvalidName</p> | <p>Ein ungültiger Indexname wurde angegeben. Weitere Informationen finden Sie <a href="gg294082(v=exchg.10).md">unter JET_INDEXCREATE2.</a></p> | 
| <p>JET_errInvalidParameter</p> | <p>Ein ungültiger Parameter wurde an die API übergeben. Im Folgenden finden Sie einige Gründe, warum dieser Fehler zurückgegeben werden kann:</p><ul><li><p>Das <strong>cbKey-Feld</strong> einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> ist auf 0 (null) festgelegt.</p></li><li><p>Der <strong>cbStruct-Member</strong> einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> ist nicht auf sizeof(JET_INDEXCREATE2) festgelegt.</p></li></ul> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Fehler beim Normalisieren einer Unicode-Spalte. Dies kann dadurch verursacht werden, dass nicht mehr die Systemressourcen verfügbar sind.</p> | 
| <p>JET_errSpaceHintsInvalid</p> | <p>Ein Element der JET-Raumhinweisstruktur war nicht richtig oder veranstellbar.</p> | 



#### <a name="remarks"></a>Bemerkungen

Die **JetCreateIndex4W-Funktion** durchläuft die im *pindexcreate-Parameter* angegebenen Indizes und wird manchmal beim ersten Fehler abgebrochen. Indizes nach dem ersten Index mit einem Fehler wurden möglicherweise nicht versucht, obwohl der **Err-Member** der [JET_INDEXCREATE2-Struktur](./jet-indexcreate2-structure.md) JET_errSuccess enthält.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2012.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Siehe auch

[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JET_SPACEHINTS](./jet-spacehints-structure.md)
