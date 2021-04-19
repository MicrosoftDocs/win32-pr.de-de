---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNCREATE Struktur'
title: JET_COLUMNCREATE-Struktur
TOCTitle: JET_COLUMNCREATE Structure
ms:assetid: 553263a9-7d2c-4bd7-ad77-1dfb6d21ef2c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269252(v=EXCHG.10)
ms:contentKeyID: 32765554
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
ms.openlocfilehash: ee2d9d194a03cf575eb0296163526c1c50301cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363609"
---
# <a name="jet_columncreate-structure"></a>JET_COLUMNCREATE-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_columncreate-structure"></a>JET_COLUMNCREATE-Struktur

Die **JET_COLUMNCREATE** -Struktur beschreibt eine Spalte, die in einer Datenbank erstellt werden soll.

```cpp
    typedef struct tag_JET_COLUMNCREATE {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_COLTYP coltyp;
      unsigned long cbMax;
      JET_GRBIT grbit;
      void* pvDefault;
      unsigned long cbDefault;
      unsigned long cp;
      JET_COLUMNID columnid;
      JET_ERR err;
    } JET_COLUMNCREATE;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe der-Struktur in Bytes. Dieses Feld muss mit **sizeof (JET_COLUMNCREATE)** initialisiert werden.

**szcolumnname**

Der Name der zu erstellenden Spalte. Der Name muss die folgenden Kriterien erfüllen:

  - Es muss weniger als JET_cbNameMost Zeichen lang sein, ohne das abschließende Null-Zeichen.

<!-- end list -->

  - Sie darf nur Zeichen aus den folgenden Sätzen enthalten: 0 bis 9, A bis Z, A bis Z und alle anderen Interpunktions Punkte außer Ausrufezeichen ( \! ), Komma (,), öffnende eckige Klammer ( \[ ) und schließende Klammer ( \] ), d. h. ASCII-Zeichen 0x20, 0x22 bis 0x2D, 0x2F bis 0x5A, 0x5c, 0x5d bis 0x7F.

<!-- end list -->

  - Er darf nicht mit einem Leerzeichen beginnen.

<!-- end list -->

  - Sie muss mindestens ein Zeichen enthalten, das kein Leerzeichen ist.

**colyp**

Der Typ der Spalte (z. b. "Text", "Binary" oder "Numerisch"). Weitere Informationen finden Sie unter [JET_COLTYP](./jet-coltyp.md).

**cbmax**

Die maximale Länge einer Spalte variabler Länge in Bytes. Die Länge der Spalte für Spalten mit fester Länge.

**grbit**

Eine Gruppe von Bits, die die Optionen für diese-Struktur enthalten und die 0 (null) oder mehrere der folgenden Werte enthalten.

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
<td><p>Die Spalte ist korrigiert. Es wird immer die gleiche Menge an Speicherplatz in einer Zeile verwendet, unabhängig davon, wie viele Daten in der Spalte gespeichert werden. JET_bitColumnFixed können nicht mit JET_bitColumnTagged verwendet werden. Dieses Bit kann nicht mit langen Werten wie <strong>JET_coltypLongText</strong> und <strong>JET_coltypLongBinary</strong>verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTagged</p></td>
<td><p>Die Spalte ist gekennzeichnet. Markierte Spalten beanspruchen keinen Speicherplatz in der Datenbank, wenn Sie keine Daten enthalten. Dieses Bit kann nicht mit JET_bitColumnFixed verwendet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnNotNULL</p></td>
<td><p>Die Spalte darf nie auf einen NULL-Wert festgelegt werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnAutoincrement</p></td>
<td><p>Die Spalte wird automatisch inkrementiert. Die Zahl ist eine steigende Zahl, die in einer Tabelle garantiert eindeutig ist. Die Zahl ist jedoch möglicherweise nicht kontinuierlich. Wenn z. b. fünf Zeilen in eine Tabelle eingefügt werden, kann die AutoIncrement-Spalte die Werte {1, 2, 6, 7, 8} enthalten.</p>
<p><strong>Windows 2000:  </strong> Dieses Bit kann nur für Spalten vom Typ <strong>JET_coltypLong</strong>verwendet werden.</p>
<p><strong>Windows Server 2003 und höher:  </strong> Dieses Bit kann nur für Spalten vom Typ <strong>JET_coltypLong</strong> oder <strong>JET_coltypCurrency</strong>verwendet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUpdatable</p></td>
<td><p>Dieses Bit ist nur bei Aufrufen von <a href="gg269215(v=exchg.10).md">jetgetcolumninfo</a>gültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Dieses Bit ist nur bei Aufrufen von <a href="gg269211(v=exchg.10).md">jetopentemptable</a>gültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Dieses Bit ist nur bei Aufrufen von <a href="gg269211(v=exchg.10).md">jetopentemptable</a>gültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnMultiValued</p></td>
<td><p>Die Spalte kann mehr wertig sein. Für eine mehrwertige Spalte können NULL, ein oder mehrere Werte zugeordnet werden. Die verschiedenen Werte in einer mehrwertigen Spalte werden durch den <strong>itagsequence</strong> -Member verschiedener Strukturen identifiziert, z. b. <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Mehrwertige Spalten müssen markierte Spalten sein. Das heißt, Sie können keine Spalten fester Länge oder Spalten mit variabler Länge aufweisen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnEscrowUpdate</p></td>
<td><p>Die Spalte ist eine Spalte zum Aktualisieren von Spalten. Eine Spalte für das Hinterlegungs Update kann gleichzeitig von verschiedenen Sitzungen mit <a href="gg294125(v=exchg.10).md">jetescrowupdate</a> aktualisiert werden und die Transaktions Konsistenz beibehalten.</p>
<ul>
<li><p>Eine Spalte für das Hinterlegungs Update kann nur erstellt werden, wenn die Tabelle leer ist.</p></li>
<li><p>Eine Spalte vom Typ "hinterlegter" muss vom Typ "JET_coltypLong" sein <strong>.</strong></p></li>
<li><p>Eine Spalte für das Hinterlegungs Update muss über einen Standardwert verfügen (" <strong>cbdefault</strong> " muss positiv sein).</p></li>
<li><p>JET_bitColumnEscrowUpdate kann nicht in Verbindung mit den folgenden Konstanten verwendet werden:</p>
<ul>
<li><p>JET_bitColumnTagged</p></li>
<li><p>JET_bitColumnVersion</p></li>
<li><p>JET_bitColumnAutoincrement</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUnversioned</p></td>
<td><p>Die Spalte wird ohne eine Version erstellt. Bei anderen Transaktionen, die versuchen, eine Spalte mit demselben Namen hinzuzufügen, tritt ein Fehler auf. Dieses Bit ist nur bei <a href="gg294122(v=exchg.10).md">jetaddcolumn</a>nützlich. Sie kann nicht innerhalb einer Transaktion verwendet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnMaybeNull</p></td>
<td><p>Für die zukünftige Verwendung reserviert.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnFinalize</p></td>
<td><p>Verwenden Sie JET_bitColumnDeleteOnZero anstelle von JET_bitColumnFinalize. JET_bitColumnFinalize gibt an, dass eine Spalte fertiggestellt werden kann. Wenn eine Spalte, die abgeschlossen werden kann, eine Spalte mit dem Wert "hinterlegter Update" aufweist, die Null erreicht, wird die Zeile gelöscht. Zukünftige Versionen können stattdessen eine Rückruffunktion aufrufen. Weitere Informationen finden Sie unter <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Eine Spalte, die abgeschlossen werden kann, muss eine Spalte für die hinterlegte Aktualisierung sein. JET_bitColumnFinalize können nicht mit JET_bitColumnUserDefinedDefault verwendet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUserDefinedDefault</p></td>
<td><p>Der Standardwert für eine Spalte wird von der Rückruffunktion <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>bereitgestellt. Eine Spalte, die über einen benutzerdefinierten Standardwert verfügt, muss eine markierte Spalte sein. <strong>pvdefault</strong> muss auf eine <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> Struktur verweisen, und <strong>cbdefault</strong> muss auf sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>) festgelegt werden.</p>
<p>JET_bitColumnUserDefinedDefault kann nicht in Verbindung mit den folgenden Konstanten verwendet werden:</p>
<ul>
<li><p>JET_bitColumnFixed</p></li>
<li><p>JET_bitColumnNotNULL</p></li>
<li><p>JET_bitColumnVersion</p></li>
<li><p>JET_bitColumnAutoincrement</p></li>
<li><p>JET_bitColumnUpdatable</p></li>
<li><p>JET_bitColumnEscrowUpdate</p></li>
<li><p>JET_bitColumnFinalize</p></li>
<li><p>JET_bitColumnDeleteOnZero</p></li>
<li><p>JET_bitColumnMaybeNull</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnDeleteOnZero</p></td>
<td><p>Bei der Spalte handelt es sich um eine Spalte zum Löschen von Spalten. Wenn Sie 0 (null) erreicht, wird der Datensatz gelöscht. Eine gängige Verwendung für eine Spalte, die fertiggestellt werden kann, ist die Verwendung als Verweis Zähler Feld. wenn das Feld Null erreicht, wird der Datensatz gelöscht. JET_bitColumnDeleteOnZero bezieht sich auf JET_bitColumnFinalize. Eine DELETE-on-Zero-Spalte muss eine Spalte für die hinterlegte Aktualisierung sein. JET_bitColumnDeleteOnZero können nicht mit JET_bitColumnFinalize verwendet werden. JET_bitColumnDeleteOnZero kann nicht mit benutzerdefinierten Standard Spalten verwendet werden.</p></td>
</tr>
</tbody>
</table>


**pvdefault**

Verweist auf einen Puffer, bei dem es sich um den Standardwert für eine Spalte handelt. Die Länge des Puffers ist **cbdefault**. Wenn kein Standardwert vorhanden ist, sollte **pvdefault** auf NULL festgelegt werden, und **cbdefault** sollte auf NULL festgelegt werden. Wenn *grbit* JET_bitColumnUserDefinedDefault festgelegt ist, wird **pvdefault** als Zeiger auf eine JET_USERDEFINEDDEFAULT Struktur interpretiert. Standardwerte dürfen nicht größer als 255 Bytes sein. Wenn ein Standardwert größer als 255 Bytes ist, wird er automatisch abgeschnitten.

**cbdefault**

Die Größe (in Bytes) des Puffers, der von **pvdefault** angegeben wird.

**cp**

Die Codepage für die Spalte. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 (null) bedeutet, dass der Standardwert verwendet wird (English, 1252). Handelt es sich bei der Spalte nicht um eine Text Spalte, wird die Codepage automatisch auf 0 (null) festgelegt.

**ColumnID**

Bei Erfolg wird der Spalten Bezeichner der neu erstellten Spalte in diesem Feld zurückgegeben. Bei einem Fehler ist der Wert nicht definiert.

**irre**

Das **Err** -Feld enthält den Status, in dem diese Spalte erstellt wird. Eine Liste der wahrscheinlichen Rückgabewerte finden Sie unter [jetaddcolumn](./jetaddcolumn-function.md) .

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
<td><p>Wird als <strong>JET_COLUMNCREATE_W</strong> (Unicode) und <strong>JET_COLUMNCREATE_A</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RETINFO](./jet-retinfo-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JET_SETCOLUMN](./jet-setcolumn-structure.md)  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[Jetaddcolumn](./jetaddcolumn-function.md)  
[Jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[Jetescrowupdate](./jetescrowupdate-function.md)  
[Jetrenamecolumschlag](./jetrenamecolumn-function.md)  
[Jetsetcolumns](./jetsetcolumns-function.md)
