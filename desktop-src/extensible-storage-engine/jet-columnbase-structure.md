---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNBASE Struktur'
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
ms.openlocfilehash: 9276c36a08a429f44568b3a909af77f5ae038c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352594"
---
# <a name="jet_columnbase-structure"></a>JET_COLUMNBASE-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_columnbase-structure"></a>JET_COLUMNBASE-Struktur

Die **JET_COLUMNBASE** -Struktur beschreibt die Parameter einer Basis Spalte. Die [jetgetcolumninfo](./jetgetcolumninfo-function.md) -und [jetgettablecolumninfo](./jetgettablecolumninfo-function.md) -Funktionen verwenden die **JET_COLUMNBASE** Struktur.

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

Die Größe der-Struktur in Bytes. Legen Sie **cbStruct** auf sizeof (JET_COLUMNBASE) fest.

**ColumnID**

Reserviert. Legen Sie **ColumnID** auf 0 (null) fest.

**colyp**

Der Typ der Spalte (z. b. "Text", "Binary" oder "Numerisch"). Weitere Informationen finden Sie unter [JET_COLTYP](./jet-coltyp.md).

**wcountry**

Reserviert. Legen Sie den Wert auf 0 (null) fest.

**langid**

Reserviert. Legen Sie den Wert auf 0 (null) fest.

**cp**

Die Codepage für die Spalte. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 (null) bedeutet, dass der Standardwert verwendet wird (English, 1252). Handelt es sich bei der Spalte nicht um eine Text Spalte, wird die Codepage automatisch auf 0 (null) festgelegt.

**wfiller**

Reserviert. Legen Sie den Wert auf 0 (null) fest.

**cbmax**

Die maximale Länge (in Byte) einer Spalte variabler Länge oder die tatsächliche Länge einer Spalte fester Länge in Bytes.

**grbit**

Optionen für die Spalte, einschließlich NULL oder mehr der folgenden Werte.

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
<td><p>Die Spalte ist korrigiert und belegt den gleichen Speicherplatz in einer Zeile, unabhängig davon, wie viele Daten Sie enthält. JET_bitColumnFixed kann nicht mit JET_bitColumnTagged kombiniert werden und kann nicht verwendet werden, wenn das <strong>colttmember</strong> auf <strong>JET_coltypLongText</strong> oder <strong>JET_coltypLongBinary</strong>festgelegt ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTagged</p></td>
<td><p>Die Spalte ist gekennzeichnet und belegt nur dann Speicherplatz in der Datenbank, wenn Sie Daten enthält. JET_bitColumnTagged können nicht mit JET_bitColumnFixed, JET_bitColumnVersion oder JET_bitColumnEscrowUpdate kombiniert werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnNotNULL</p></td>
<td><p>Die Spalte darf nicht auf einen <strong>null</strong> -Wert festgelegt werden.</p>
<p>JET_bitColumnNotNULL können nicht mit JET_bitColumnUserDefinedDefault kombiniert werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnVersion</p></td>
<td><p>Die Spalte ist eine Versions Spalte, die die Version der Zeile angibt. Der Wert dieser Spalte beginnt bei Null und wird für jedes Update der Zeile automatisch inkrementiert.</p>
<p>JET_bitColumnVersion können nur verwendet werden, wenn das <strong>colttmember</strong> auf <strong>JET_coltypLong</strong> festgelegt ist und nicht mit JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged oder JET_bitColumnUserDefinedDefault kombiniert werden kann.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnAutoincrement</p></td>
<td><p>Die Spalte wird automatisch inkrementiert. Die Zahl ist eine steigende Zahl, die in einer Tabelle garantiert eindeutig ist. Die Zahlen sind jedoch möglicherweise nicht sequenziell. Wenn z. b. fünf Zeilen in eine Tabelle eingefügt werden, kann die automatisch inkrementierte Spalte die Werte {1, 2, 6, 7, 8} enthalten.</p>
<p>JET_bitColumnAutoincrement können nur verwendet werden, wenn das <strong>colttmember</strong> auf <strong>JET_coltypLong</strong> oder <strong>JET_coltypCurrency</strong> festgelegt ist und nicht mit JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault oder JET_bitColumnVersion kombiniert werden kann.</p>
<p><strong>Windows 2000:  </strong> JET_bitColumnVersion können nur verwendet werden, wenn das <strong>colttmember</strong> auf <strong>JET_coltypLong</strong>festgelegt ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUpdatable</p></td>
<td><p>Gilt nur für Aufrufe von <a href="gg269215(v=exchg.10).md">jetgetcolumninfo</a>. JET_bitColumnUpdatable können nicht mit JET_bitColumnUserDefinedDefault kombiniert werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Nur bei Aufrufen von <a href="gg294118(v=exchg.10).md">jetopentable</a>gültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Nur bei Aufrufen von <a href="gg269211(v=exchg.10).md">jetopumtemptable</a>gültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnMultiValued</p></td>
<td><p>Die Spalte kann mehr wertig sein. Für eine mehrwertige Spalte können NULL, ein oder mehrere Werte zugeordnet werden. Die verschiedenen Werte in einer mehrwertigen Spalte werden durch eine Zahl im <strong>itagsequence</strong> -Member verschiedener Strukturen identifiziert, z. b. <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Mehrwertige Spalten müssen markierte Spalten sein. Das heißt, Sie sind möglicherweise keine Spalten fester Länge oder Spalten variabler Länge.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnEscrowUpdate</p></td>
<td><p>Gibt an, dass eine Spalte eine Spalte für das Hinterlegungs Update ist, die gleichzeitig von verschiedenen Sitzungen mit <a href="gg294125(v=exchg.10).md">jetescrowupdate</a> aktualisiert werden kann und transaktionale Konsistenz aufweist.</p>
<ul>
<li><p>Eine Spalte für das Hinterlegungs Update kann nur erstellt werden, wenn die Tabelle leer ist.</p></li>
</ul>
<ul>
<li><p>Für eine Spalte mit einem Hinterlegungs Update muss das <strong>colttmember</strong> auf JET_coltypLong festgelegt werden <strong>.</strong></p></li>
</ul>
<ul>
<li><p>Eine Spalte für das Hinterlegungs Update muss über einen Standardwert verfügen (" <strong>cbdefault</strong> " muss positiv sein).</p></li>
</ul>
<ul>
<li><p>JET_bitColumnEscrowUpdate können nicht mit JET_bitColumnTagged, JET_bitColumnVersion oder JET_bitColumnAutoincrement kombiniert werden.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUnversioned</p></td>
<td><p>Die Spalte wird ohne Versionsnummer erstellt. Dies bedeutet, dass andere Transaktionen, die versuchen, eine Spalte mit demselben Namen hinzuzufügen, fehlschlagen. JET_bitColumnUnversioned wird nur mit <a href="gg294122(v=exchg.10).md">jetaddcolumn</a>verwendet. Sie kann nicht innerhalb einer Transaktion verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnMaybeNull</p></td>
<td><p>Für die zukünftige Verwendung reserviert.</p>
<p>JET_bitColumnMaybeNull können nicht mit JET_bitColumnUserDefinedDefault kombiniert werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnFinalize</p></td>
<td><p>Darf nicht verwendet werden. Verwenden Sie stattdessen JET_bitColumnDeleteOnZero.</p>
<p>Die Spalte kann abgeschlossen werden. Eine Spalte, die abgeschlossen werden kann, ist eine Spalte für das hinterlegen des Updates, die bewirkt, dass die Zeile gelöscht wird, wenn die Spalte NULL erreicht. In zukünftigen Versionen wird stattdessen möglicherweise eine Rückruffunktion aufgerufen (siehe <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>). Eine Spalte, die abgeschlossen werden kann, muss eine Spalte für die hinterlegte Aktualisierung sein. JET_bitColumnFinalize können nicht mit JET_bitColumnUserDefinedDefault kombiniert werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUserDefinedDefault</p></td>
<td><p>Der Standardwert für eine Spalte wird von einer Rückruffunktion bereitgestellt. Siehe <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Eine Spalte, die über einen benutzerdefinierten Standardwert verfügt, muss eine markierte Spalte sein. Wenn JET_bitColumnUserDefinedDefault angegeben wird, muss <strong>pvdefault</strong> auf eine <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> Struktur verweisen, und <strong>cbdefault</strong> muss auf sizeof (JET_USERDEFINEDDEFAULT) festgelegt werden.</p>
<p>JET_bitColumnUserDefinedDefault können nicht mit JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero oder JET_bitColumnMaybeNull kombiniert werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnDeleteOnZero</p></td>
<td><p>Bei der Spalte handelt es sich um eine Spalte zum Aktualisieren von Spalten. Wenn Sie Null erreicht, wird der Datensatz gelöscht. Eine häufige Verwendung für Spalten mit dem Wert "Delete-on-Zero" ist als Verweis Zähler Felder. Wenn die Anzahl der Verweise auf Null fällt, wird der Datensatz gelöscht. Eine DELETE-on-Zero-Spalte muss eine Spalte für die hinterlegte Aktualisierung sein.</p>
<p>JET_bitColumnDeleteOnZero ersetzt JET_bitColumnFinalize.</p>
<p>JET_bitColumnDeleteOnZero kann nicht mit JET_bitColumnFinalize oder JET_bitColumnUserDefinedDefault kombiniert werden und kann nicht mit benutzerdefinierten Standard Spalten verwendet werden.</p></td>
</tr>
</tbody>
</table>


**szbasetablename**

Die Tabelle, aus der die aktuelle Tabelle Ihre DDL erbt.

**szbasecolumschlag Name**

Der Name der Spalte in der Vorlagen Tabelle.

### <a name="remarks"></a>Bemerkungen

**JET_COLUMNBASE** enthält viele der gleichen Informationen wie [JET_COLUMNDEF](./jet-columndef-structure.md), fügt jedoch Zeichen folgen Felder hinzu, um die Basistabelle zu beschreiben (wenn eine hierarchische DDL verwendet wurde).

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
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Wird als <strong>JET_COLUMNBASE_W</strong> (Unicode) und <strong>JET_COLUMNBASE_A</strong> (ANSI) implementiert.</p></td>
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
[Jetgetcolumninfo](./jetgetcolumninfo-function.md)  
[Jetgettablecolumninfo](./jetgettablecolumninfo-function.md)  
[Jetrenamecolumschlag](./jetrenamecolumn-function.md)
