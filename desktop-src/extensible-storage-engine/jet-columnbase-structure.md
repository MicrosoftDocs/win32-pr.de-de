---
description: 'Weitere Informationen zu: JET_COLUMNBASE-Struktur'
title: JET_COLUMNBASE-Struktur
TOCTitle: JET_COLUMNBASE Structure
ms:assetid: 171275c3-966d-409d-ad20-a8f240f7500d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269194(v=EXCHG.10)
ms:contentKeyID: 32765497
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39df84e7e0dbfe150a92ebde2faade9562ad65b74fb503f6ef1ee07f74f46f22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116240"
---
# <a name="jet_columnbase-structure"></a>JET_COLUMNBASE-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_columnbase-structure"></a>JET_COLUMNBASE-Struktur

Die **JET_COLUMNBASE-Struktur** beschreibt die Parameter einer Basisspalte. Die Funktionen [JetGetColumnInfo](./jetgetcolumninfo-function.md) und [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) verwenden die **JET_COLUMNBASE** Struktur.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wFiller;
      unsigned long cbMax;
      JET_GRBIT grbit;
      tchar szBaseTableName[256];
      tchar szBaseColumnName[256];
    } JET_COLUMNBASE;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe dieser Struktur in Bytes. Legen Sie **cbStruct** auf sizeof( JET_COLUMNBASE ) fest.

**Columnid**

Reserviert. Legen Sie **columnid** auf 0 (null) fest.

**coltyp**

Der Typ der Spalte (z. B. Text, binär oder numerisch). Weitere Informationen finden Sie unter [JET_COLTYP](./jet-coltyp.md).

**wCountry**

Reserviert. Legen Sie auf 0 (null) fest.

**langid**

Reserviert. Legen Sie auf 0 (null) fest.

**cp**

Die Codepage für die Spalte. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252). Wenn die Spalte keine Textspalte ist, wird die Codepage automatisch auf 0 (null) festgelegt.

**wFiller**

Reserviert. Legen Sie auf 0 (null) fest.

**cbMax**

Die maximale Länge einer Spalte variabler Länge in Bytes oder die tatsächliche Länge einer Spalte fester Länge in Bytes.

**grbit**

Optionen für die Spalte, einschließlich null oder mehr der folgenden Werte.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitColumnFixed</p></td>
<td><p>Die Spalte ist fest und belegt die gleiche Menge an Speicherplatz in einer Zeile, unabhängig davon, wie viele Daten sie enthält. JET_bitColumnFixed können nicht mit JET_bitColumnTagged kombiniert werden und können nicht verwendet werden, wenn der <strong>Coltypmember</strong> auf <strong>JET_coltypLongText</strong> oder <strong>JET_coltypLongBinary</strong>festgelegt ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTagged</p></td>
<td><p>Die Spalte wird gekennzeichnet und belegt nur Dann Speicherplatz in der Datenbank, wenn sie Daten enthält. JET_bitColumnTagged können nicht mit JET_bitColumnFixed, JET_bitColumnVersion oder JET_bitColumnEscrowUpdate kombiniert werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnNotNULL</p></td>
<td><p>Die Spalte darf nicht auf einen <strong>NULL-Wert</strong> festgelegt werden.</p>
<p>JET_bitColumnNotNULL können nicht mit JET_bitColumnUserDefinedDefault kombiniert werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnVersion</p></td>
<td><p>Die Spalte ist eine Versionsspalte, die die Version der Zeile angibt. Der Wert dieser Spalte beginnt bei 0 (null) und wird für jedes Update der Zeile automatisch erhöht.</p>
<p>JET_bitColumnVersion können nur verwendet werden, wenn der <strong>Coltypmember</strong> auf <strong>JET_coltypLong</strong> festgelegt ist und nicht mit JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged oder JET_bitColumnUserDefinedDefault kombiniert werden kann.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnAutoincrement</p></td>
<td><p>Die Spalte wird automatisch erhöht. Die Zahl ist eine steigende Zahl und innerhalb einer Tabelle garantiert eindeutig. Die Zahlen sind jedoch möglicherweise nicht sequenziell. Wenn beispielsweise fünf Zeilen in eine Tabelle eingefügt werden, kann die automatisch inkrementierte Spalte die Werte { 1, 2, 6, 7, 8 } enthalten.</p>
<p>JET_bitColumnAutoincrement können nur verwendet werden, wenn der <strong>Coltypmember</strong> auf <strong>JET_coltypLong</strong> oder <strong>JET_coltypCurrency</strong> festgelegt ist und nicht mit JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault oder JET_bitColumnVersion kombiniert werden kann.</p>
<p><strong>Windows 2000:</strong> JET_bitColumnVersion kann nur verwendet werden, wenn der <strong>Coltypmember</strong> auf <strong>JET_coltypLong</strong>festgelegt ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUpdatable</p></td>
<td><p>Gilt nur für Aufrufe von <a href="gg269215(v=exchg.10).md">JetGetColumnInfo.</a> JET_bitColumnUpdatable können nicht mit JET_bitColumnUserDefinedDefault kombiniert werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Nur für Aufrufe von <a href="gg294118(v=exchg.10).md">JetOpenTable</a>gültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Nur für Aufrufe von <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>gültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnMultiValued</p></td>
<td><p>Die Spalte kann mehrwertige Werte aufweisen. Einer mehrwertigen Spalte können null, ein oder mehrere Werte zugeordnet sein. Die verschiedenen Werte in einer mehrwertigen Spalte werden durch eine Zahl im <strong>itagSequence-Element</strong> verschiedener Strukturen identifiziert, z. B. <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">, JET_ENUMCOLUMNVALUE</a>. Mehrwertige Spalten müssen mit Tags versehen werden. Das heißt, dass es sich möglicherweise nicht um Spalten mit fester oder variabler Länge handelt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnEscrowUpdate</p></td>
<td><p>Gibt an, dass es sich bei einer Spalte um eine Spalte für die Escrow-Aktualisierung handelt, die gleichzeitig von verschiedenen Sitzungen mit <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> aktualisiert werden kann und transaktionskonsistent ist.</p>
<ul>
<li><p>Eine Spalte für die Escrow-Aktualisierung kann nur erstellt werden, wenn die Tabelle leer ist.</p></li>
</ul>
<ul>
<li><p>Für eine Spalte mit der Spaltenauffüllungsaktualisierung muss der <strong>coltyp-Member</strong> auf JET_coltypLong festgelegt <strong>werden.</strong></p></li>
</ul>
<ul>
<li><p>Eine Spalte für die Escrow-Aktualisierung muss einen Standardwert aufweisen <strong>(cbDefault</strong> muss positiv sein).</p></li>
</ul>
<ul>
<li><p>JET_bitColumnEscrowUpdate können nicht mit JET_bitColumnTagged, JET_bitColumnVersion oder JET_bitColumnAutoincrement kombiniert werden.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUnversioned</p></td>
<td><p>Die Spalte wird ohne Versionsnummer erstellt. Dies bedeutet, dass andere Transaktionen, die versuchen, eine Spalte mit dem gleichen Namen hinzuzufügen, fehlschlagen. JET_bitColumnUnversioned wird nur mit <a href="gg294122(v=exchg.10).md">JetAddColumn</a>verwendet. Sie kann nicht innerhalb einer Transaktion verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnMaybeNull</p></td>
<td><p>Für die zukünftige Verwendung reserviert.</p>
<p>JET_bitColumnMaybeNull können nicht mit JET_bitColumnUserDefinedDefault kombiniert werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnFinalize</p></td>
<td><p>Darf nicht verwendet werden. Verwenden Sie stattdessen JET_bitColumnDeleteOnZero.</p>
<p>Die Spalte kann abgeschlossen werden. Eine Spalte, die finalisiert werden kann, ist eine Spalte zum Hinterlegungsupdate, die bewirkt, dass die Zeile gelöscht wird, wenn die Spalte 0 (null) erreicht. Zukünftige Versionen können stattdessen eine Rückruffunktion aufrufen (siehe <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>). Eine Spalte, die finalisiert werden kann, muss eine Spalte für die Escrow-Aktualisierung sein. JET_bitColumnFinalize können nicht mit JET_bitColumnUserDefinedDefault kombiniert werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUserDefinedDefault</p></td>
<td><p>Der Standardwert für eine Spalte wird von einer Rückruffunktion bereitgestellt. Siehe <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Eine Spalte mit einem benutzerdefinierten Standardwert muss eine markierte Spalte sein. Wenn JET_bitColumnUserDefinedDefault angegeben wird, muss <strong>pvDefault</strong> auf eine <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT-Struktur</a> zeigen, und <strong>cbDefault</strong> muss auf sizeof( JET_USERDEFINEDDEFAULT ) festgelegt werden.</p>
<p>JET_bitColumnUserDefinedDefault können nicht mit JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero oder JET_bitColumnMaybeNull kombiniert werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnDeleteOnZero</p></td>
<td><p>Bei der Spalte handelt es sich um eine Spalte für die Nachschubaktualisierung, und wenn sie 0 (null) erreicht, wird der Datensatz gelöscht. Eine häufige Verwendung für Delete-on-Zero-Spalten ist als Verweisanzahlfelder. Wenn die Anzahl der Verweise auf 0 (null) fällt, wird der Datensatz gelöscht. Eine Spalte mit dem Wert delete-on-zero muss eine Spalte zum Aktualisieren der Löschspalte sein.</p>
<p>JET_bitColumnDeleteOnZero ersetzt JET_bitColumnFinalize.</p>
<p>JET_bitColumnDeleteOnZero kann nicht mit JET_bitColumnFinalize oder JET_bitColumnUserDefinedDefault kombiniert und nicht mit benutzerdefinierten Standardspalten verwendet werden.</p></td>
</tr>
</tbody>
</table>


**szBaseTableName**

Die Tabelle, von der die aktuelle Tabelle ihre DDL erbt.

**szBaseColumnName**

Der Name der Spalte in der Vorlagentabelle.

### <a name="remarks"></a>Hinweise

**JET_COLUMNBASE** enthält viele der gleichen Informationen wie [JET_COLUMNDEF](./jet-columndef-structure.md), fügt jedoch Zeichenfolgenfelder hinzu, um die Basistabelle zu beschreiben (wenn eine hierarchische DDL verwendet wurde).

### <a name="requirements"></a>Anforderungen

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
<td><p>Wird in Esent.h deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Wird als <strong>JET_COLUMNBASE_W</strong> (Unicode) und JET_COLUMNBASE_A (ANSI) implementiert. <strong></strong></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md)  
[JetGetColumnInfo](./jetgetcolumninfo-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)
