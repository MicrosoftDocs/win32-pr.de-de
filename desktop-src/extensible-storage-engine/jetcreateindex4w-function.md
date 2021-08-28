---
description: Weitere Informationen finden Sie unter JetCreateIndex4W-Funktion.
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
ms.openlocfilehash: cd1df48c165fa168ed9612177f5cf95f83f2069f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478406"
---
# <a name="jetcreateindex4w-function"></a>JetCreateIndex4W-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetCreateIndex4W-Funktion** erstellt Indizes für Daten in einer ESE-Datenbank (Extensible Storage Engine), mit der bestimmte Daten schnell gefunden werden können.

Die **JetCreateIndex4W-Funktion** wurde im Windows 8 eingeführt.

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

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der in der folgenden Tabelle aufgeführten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errCannotIndex</p> | <p>Es wurde versucht, eine Escrow-Update- oder SLV-Spalte zu indizieren (beachten Sie, dass SLV-Spalten veraltet sind).</p> | 
| <p>JET_errColumnNotFound</p> | <p>Es wurde versucht, eine nicht vorhandene Spalte zu indizieren. Der Versuch, eine nicht vorhandene Spalte bedingt zu indizieren, kann diesen Fehler ebenfalls erzeugen.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Dieser Fehler wird zurückgegeben, wenn der <strong>ulDensity-Member</strong> der JET_INDEXCREATE2-Struktur auf eine Zahl kleiner als 20 oder größer als 100 festgelegt ist. <a href="gg294082(v=exchg.10).md"></a></p> | 
| <p>JET_errIndexDuplicate</p> | <p>Es wurde versucht, zwei identische Indizes zu definieren.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Es wurde versucht, mehrere primäre Indizes für eine Tabelle anzugeben. Eine Tabelle muss genau einen primären Index haben. Wenn kein primärer Index angegeben wird, erstellt die Datenbank-Engine transparent einen.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Es wurde eine ungültige Indexdefinition angegeben. Im Folgenden finden Sie einige mögliche Gründe für diesen Fehler:</p><ul><li><p>Ein primärer Index ist bedingt (<strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> has <strong>JET_bitIndexPrimary</strong> set, and the <strong>cConditionalColumn</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> is greater than zero).</p></li><li><p>Gilt für Versionen von Windows ab Windows Server 2003. Es wurde versucht, einen Tupelindex mit Tupelgrenzwerten zu erstellen, ohne jedoch Informationen im <strong>ptuplelimits-Member</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> zu übergeben (das heißt, <em>grbit</em> hat <strong>JET_bitIndexTupleLimits</strong> festgelegt, aber der <strong>ptuplelimits-Zeiger</strong> ist NULL).</p></li><li><p>Übergeben einer ungültigen Schlüsseldefinition im <strong>szKey-Member</strong> <a href="gg294082(v=exchg.10).md">der</a> JET_INDEXCREATE2 Struktur. Informationen zu gültigen Definitionen finden Sie unter <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</p></li><li><p>Festlegen des <strong>cbVarSegMac-Mitglieds</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> auf größer als <strong>JET_cbPrimaryKeyMost</strong> (für einen primären Index) oder größer als JET_cbSecondaryKeyMost (für einen <strong>sekundären</strong> Index).</p></li><li><p>Übergeben einer ungültigen Kombination für einen benutzerdefinierten <strong></strong> Unicode-Index (einer, bei dem das JET_bitIndexUnicode-Bit im <strong>Grbit-Member</strong> von <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2.</a> Einige häufige Ursachen können sein, dass das Pidxunicode-Feld der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> NULL ist oder die in der pidxunicode-Struktur angegebene LCID ungültig ist.</p></li><li><p>Angeben einer mehrwertigen Spalte für einen primären Index.</p></li><li><p>Es wird versucht, zu viele bedingte Spalten zu indizieren. Der <strong>cConditionalColumn-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> darf nicht größer als <strong>JET_ccolKeyMost.</strong></p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Gilt für Versionen von Windows ab Windows XP. Eine <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS-Struktur</a> wurde angegeben, und ihre Grenzwerte werden nicht unterstützt. Weitere Informationen finden Sie im Abschnitt "Hinweise" der <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Gilt für Versionen von Windows ab Windows XP. Ein Tupelindex kann nicht eindeutig sein (<em>grbit</em> darf nicht sowohl über JET_bitIndexTuples <strong>als</strong> auch <strong>JET_bitIndexUnique</strong> verfügen).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Gilt für Versionen von Windows ab Windows XP. Ein Tupelindex kann sich nur über einer einzelnen Spalte (d. h. das <strong>Grbit-Element</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> hat <strong>JET_bitIndexTuples</strong> festgelegt, und das <strong>szKey-Element</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> gibt mehr als eine Spalte an).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Gilt für Versionen von Windows ab Windows XP. Ein Tupelindex kann kein primärer Index sein (d. h. das <strong>Grbit-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> darf nicht sowohl JET_bitIndexPrimary als auch <strong>JET_bitIndexTuples</strong> haben). <strong></strong></p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Gilt für Versionen von Windows ab Windows XP. Ein Tupelindex kann nur für eine Text- oder Unicode-Spalte verwendet werden. Der Versuch, andere Spalten (z. B. binäre Spalten) zu indizieren, führt <strong>zu JET_errIndexTuplesTextColumnsOnly.</strong></p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Gilt für Versionen von Windows ab Windows XP. Ein Tupelindex lässt das Festlegen des <strong>cbVarSegMac-JET_INDEXCREATE2</strong> struktur nicht zu. <a href="gg294082(v=exchg.10).md"></a></p> | 
| <p>JET_errInTransaction</p> | <p>Es wurde versucht, während einer Transaktion einen Index ohne Versionsinformationen zu erstellen.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Die Indexdefinition ist ungültig, <strong>da das grbit-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> inkonsistente Werte enthält. Im Folgenden finden Sie einige mögliche Gründe:</p><ul><li><p>Für einen primären Index wurde ein Ignore-Bit angegeben (JET_bitIndexPrimary wurde mit einem der JET_bitIndexIgnoreNull <strong>,</strong>JET_bitIndexIgnoreAnyNull <strong>oder</strong> <strong>JET_bitIndexIgnoreFirstNull) übergeben.</strong></p></li><li><p>Ein leerer Index ignoriert keine NULL-Felder (d. h., das <strong></strong> <strong>grbit-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> hat JET_bitIndexEmpty festgelegt, aber keine JET_bitIndexIgnoreAnyNull festgelegt). <strong></strong></p></li><li><p>Übergeben einer <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> struktur mit einem ungültigen <strong>Grbit-Member.</strong> Siehe <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li></ul><p>Wenn mehrere Indizes gleichzeitig erstellt werden (d. h., wenn der <em>cIndexCreate-Parameter</em> größer als eins ist), darf keiner der Indizes eines der folgenden Bits enthalten:</p><ul><li><p><strong>JET_bitIndexPrimary</strong></p></li><li><p><strong>JET_bitIndexUnversioned</strong></p></li><li><p><strong>JET_bitIndexEmpty</strong></p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Eine ungültige Locale ID (LCID) wurde übergeben (entweder über das <strong>lcid-Member</strong> in der <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX-Struktur,</a> auf das das <strong>pidxunicode-Member</strong> in der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> einen Zeiger enthält, oder über den <strong>lcid-Member</strong> der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur).</a></p> | 
| <p>JET_errInvalidName</p> | <p>Es wurde ein ungültiger Indexname angegeben. Weitere <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> finden Sie unter JET_INDEXCREATE2.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Ein ungültiger Parameter wurde an die API übergeben. Im Folgenden finden Sie einige Gründe, warum dieser Fehler zurückgegeben werden kann:</p><ul><li><p>Das <strong>cbKey-Feld</strong> einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ist auf 0 (null) festgelegt.</p></li><li><p>Der <strong>cbStruct-Member</strong> einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ist nicht auf sizeof(JET_INDEXCREATE2) festgelegt.</p></li></ul> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Fehler beim Versuch, eine Unicode-Spalte zu normalisieren. Dies kann dadurch verursacht werden, dass nicht mehr alle Systemressourcen verfügbar sind.</p> | 
| <p>JET_errSpaceHintsInvalid</p> | <p>Ein Element der JET-Raumhinweisstruktur war nicht richtig oder umsetzbar.</p> | 



#### <a name="remarks"></a>Hinweise

Die **JetCreateIndex4W-Funktion** durchgibt die im *pindexcreate-Parameter* angegebenen Indizes und bricht manchmal beim ersten Fehler ab. Alle Indizes nach dem ersten Index mit einem Fehler wurden möglicherweise nicht versucht, obwohl der **err-Member** der JET_INDEXCREATE2-Struktur JET_errSuccess. [](./jet-indexcreate2-structure.md)

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows 8.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2012.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

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
