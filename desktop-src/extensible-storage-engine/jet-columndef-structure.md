---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNDEF Struktur'
title: JET_COLUMNDEF-Struktur
TOCTitle: JET_COLUMNDEF Structure
ms:assetid: ee1fc473-bff5-438e-98ae-247de12e76f9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294130(v=EXCHG.10)
ms:contentKeyID: 32765744
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
ms.openlocfilehash: c541b5801c95f4b269e33360f5ffa2404ff8fc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960869"
---
# <a name="jet_columndef-structure"></a>JET_COLUMNDEF-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_columndef-structure"></a>JET_COLUMNDEF-Struktur

Die **JET_COLUMNDEF** -Struktur definiert die Daten, die in einer-Spalte gespeichert werden können.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wCollate;
      unsigned long cbMax;
      JET_GRBIT grbit;
    } JET_COLUMNDEF;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe der-Struktur in Bytes. Er muss auf sizeof (JET_COLUMNDEF) festgelegt werden.

**ColumnID**

Reserviert. **ColumnID** muss auf 0 (null) festgelegt werden.

**colyp**

Der Typ der Spalte (z. b. "Text", "Binary" oder "Numerisch"). Weitere Informationen finden Sie unter [JET_COLTYP](./jet-coltyp.md).

**wcountry**

Reserviert. **wcountry** muss auf 0 (null) festgelegt werden.

**langid**

Veraltet. **LangID** muss auf 0 (null) festgelegt werden.

**cp**

Die Codepage für die Spalte. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 (null) bedeutet, dass der Standardwert verwendet wird (English, 1252). Handelt es sich bei der Spalte nicht um eine Text Spalte, wird die Codepage automatisch auf 0 (null) festgelegt.

**wcollate**

Reserviert. **wcollate** muss auf 0 (null) festgelegt werden.

**cbmax**

Die maximale Länge (in Byte) einer Spalte variabler Länge oder die Länge einer Spalte mit fester Länge.

**grbit**

Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die 0 (null) oder mehrere der folgenden Werte enthalten.

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
<td><p>Die Spalte wird korrigiert. Es wird immer die gleiche Menge an Speicherplatz in einer Zeile verwendet, unabhängig davon, wie viele Daten in der Spalte gespeichert werden. JET_bitColumnFixed können nicht mit JET_bitColumnTagged verwendet werden. Dieses Bit kann nicht mit langen Werten (d. h. <strong>JET_coltypLongText</strong> und <strong>JET_coltypLongBinary</strong>) verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTagged</p></td>
<td><p>Die Spalte wird gekennzeichnet. Markierte Spalten beanspruchen keinen Speicherplatz in der Datenbank, wenn Sie keine Daten enthalten. Dieses Bit kann nicht mit JET_bitColumnFixed verwendet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnNotNULL</p></td>
<td><p>Die Spalte darf nie auf einen NULL-Wert festgelegt werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnVersion</p></td>
<td><p>Die Spalte ist eine Versions Spalte, die die Version der Zeile angibt. Der Wert dieser Spalte beginnt bei Null und wird für jedes Update in der Zeile automatisch inkrementiert.</p>
<p>Dieses Bit kann nur auf <strong>JET_coltypLong</strong> Spalten angewendet werden. Dieses Bit kann nicht mit JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate oder JET_bitColumnTagged verwendet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnAutoincrement</p></td>
<td><p>Die Spalte wird automatisch inkrementiert. Die Zahl ist eine steigende Zahl, die in einer Tabelle garantiert eindeutig ist. Die Zahlen sind jedoch möglicherweise nicht kontinuierlich. Wenn z. b. fünf Zeilen in eine Tabelle eingefügt werden, &quot; kann die AutoIncrement- &quot; Spalte die Werte {1, 2, 6, 7, 8} enthalten. Dieses Bit kann nur für Spalten vom Typ <strong>JET_coltypLong</strong> oder <strong>JET_coltypCurrency</strong>verwendet werden.</p>
<p><strong>Windows 2000:  </strong> In Windows 2000 kann dieses Bit nur für Spalten vom Typ <strong>JET_coltypLong</strong>verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUpdatable</p></td>
<td><p>Dieses Bit ist nur bei Aufrufen von <a href="gg269215(v=exchg.10).md">jetgetcolumninfo</a>gültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Dieses Bit ist nur bei Aufrufen von <a href="gg294118(v=exchg.10).md">jetopentable</a>gültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Dieses Bit ist nur bei Aufrufen von <a href="gg269211(v=exchg.10).md">jetopentemptable</a>gültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnMultiValued</p></td>
<td><p>Die Spalte kann mehr wertig sein. Für eine mehrwertige Spalte können NULL, ein oder mehrere Werte zugeordnet werden. Die verschiedenen Werte in einer mehrwertigen Spalte werden durch eine Zahl gekennzeichnet, die als <strong>itagsequence</strong> -Member bezeichnet wird, der zu verschiedenen Strukturen gehört, einschließlich: <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>und <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Mehrwertige Spalten müssen markierte Spalten sein. Das heißt, Sie können keine Spalten fester Länge oder Spalten mit variabler Länge aufweisen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnEscrowUpdate</p></td>
<td><p>Gibt an, dass eine Spalte eine Spalte für die hinterlegte Aktualisierung ist. Eine Spalte für das Hinterlegungs Update kann gleichzeitig von verschiedenen Sitzungen mit <a href="gg294125(v=exchg.10).md">jetescrowupdate</a> aktualisiert werden und behält die Transaktions Konsistenz bei. Eine Spalte für das Hinterlegungs Update muss außerdem die folgenden Bedingungen erfüllen:</p>
<ul>
<li><p>Eine Spalte für das Hinterlegungs Update kann nur erstellt werden, wenn die Tabelle leer ist.</p></li>
</ul>
<ul>
<li><p>Eine Spalte vom Typ "hinterlegter" muss vom Typ " <strong>JET_coltypLong</strong>" sein.</p></li>
</ul>
<ul>
<li><p>Eine Spalte für das Hinterlegungs Update muss über einen Standardwert verfügen (" <strong>cbdefault</strong> " muss positiv sein).</p></li>
</ul>
<ul>
<li><p>JET_bitColumnEscrowUpdate kann nicht zusammen mit JET_bitColumnTagged, JET_bitColumnVersion oder JET_bitColumnAutoincrement verwendet werden.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUnversioned</p></td>
<td><p>Die Spalte wird in einem ohne Versionsinformationen erstellt. Dies bedeutet, dass andere Transaktionen, die versuchen, eine Spalte mit demselben Namen hinzuzufügen, fehlschlagen. Dieses Bit ist nur bei <a href="gg294122(v=exchg.10).md">jetaddcolumn</a>nützlich. Sie kann nicht innerhalb einer Transaktion verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnMaybeNull</p></td>
<td><p>Für die zukünftige Verwendung reserviert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnFinalize</p></td>
<td><p>Verwenden Sie JET_bitColumnDeleteOnZero anstelle von JET_bitColumnFinalize. JET_bitColumnFinalize, dass eine Spalte fertiggestellt werden kann. Wenn eine Spalte, die abgeschlossen werden kann, eine Spalte mit dem Wert "hinterlegter Update" aufweist, die Null erreicht, wird die Zeile gelöscht. In zukünftigen Versionen wird stattdessen möglicherweise eine Rückruffunktion aufgerufen (Weitere Informationen finden Sie unter <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>). Eine Spalte, die abgeschlossen werden kann, muss eine Spalte für die hinterlegte Aktualisierung sein. JET_bitColumnFinalize können nicht mit JET_bitColumnUserDefinedDefault verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUserDefinedDefault</p></td>
<td><p>Der Standardwert für eine Spalte wird von einer Rückruffunktion bereitgestellt. Siehe <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Eine Spalte, die über einen benutzerdefinierten Standardwert verfügt, muss eine markierte Spalte sein. Das Angeben von JET_bitColumnUserDefinedDefault bedeutet, dass <strong>pvdefault</strong> auf eine <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> Struktur verweisen muss und <strong>cbdefault</strong> auf sizeof ( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ) festgelegt werden muss.</p>
<ul>
<li><p>JET_bitColumnUserDefinedDefault können nicht zusammen mit JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero oder JET_bitColumnMaybeNull verwendet werden.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnDeleteOnZero</p></td>
<td><p>Bei der Spalte handelt es sich um eine Spalte zum Löschen von Spalten. Wenn Sie 0 (null) erreicht, wird der Datensatz gelöscht. Eine gängige Verwendung für eine Spalte, die fertiggestellt werden kann, ist die Verwendung als Verweis Zähler Feld. wenn das Feld Null erreicht, wird der Datensatz gelöscht. JET_bitColumnDeleteOnZero bezieht sich auf JET_bitColumnFinalize. Eine DELETE-on-Zero-Spalte muss eine Spalte für die hinterlegte Aktualisierung sein. JET_bitColumnDeleteOnZero können nicht mit JET_bitColumnFinalize verwendet werden. JET_bitColumnDeleteOnZero kann nicht mit benutzerdefinierten Standard Spalten verwendet werden.</p></td>
</tr>
</tbody>
</table>


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
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md)  
[Jetaddcolumn](./jetaddcolumn-function.md)  
[Jetescrowupdate](./jetescrowupdate-function.md)  
[Jetgettablecolumninfo](./jetgettablecolumninfo-function.md)  
[Jetopumtemptable](./jetopentemptable-function.md)  
[JetOpenTempTable2](./jetopentemptable2-function.md)  
[JetOpenTempTable3](./jetopentemptable3-function.md)  
[Jetrenamecolumschlag](./jetrenamecolumn-function.md)
