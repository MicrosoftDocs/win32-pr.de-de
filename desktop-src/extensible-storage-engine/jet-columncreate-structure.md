---
description: 'Weitere Informationen finden Sie unter: JET_COLUMNCREATE Struktur'
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
ms.openlocfilehash: 1b14388f26e21550319b910ac01d9ee0dde4d5890336c91e1fca76bc68cce93f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118254980"
---
# <a name="jet_columncreate-structure"></a>JET_COLUMNCREATE-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_columncreate-structure"></a>JET_COLUMNCREATE-Struktur

Die **JET_COLUMNCREATE** beschreibt eine Spalte, die in einer Datenbank erstellt werden soll.

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

Die Größe der -Struktur in Bytes. Dieses Feld muss mit **sizeof( JET_COLUMNCREATE ) initialisiert werden.**

**szColumnName**

Der Name der zu erstellenden Spalte. Der Name muss die folgenden Kriterien erfüllen:

  - Es muss weniger als JET_cbNameMost Zeichen lang sein, ohne den beendenden NULL-Wert.

<!-- end list -->

  - Sie darf nur Zeichen aus den folgenden Sätzen enthalten: 0 bis 9, A bis Z, a bis z und alle anderen Interpunktionen mit Ausnahme von Ausrufezeichen ( ), Komma (,), öffnenden Klammern () und schließenden Klammern ( ), d. h. ASCII-Zeichen 0x20, 0x22 bis \! \[ \] 0x2d, 0x2f bis 0x5a, 0x5c, 0x5d bis 0x7f.

<!-- end list -->

  - Er kann nicht mit einem Leerzeichen beginnen.

<!-- end list -->

  - Sie muss mindestens ein Zeichen enthalten, das kein Leerzeichen ist.

**coltyp**

Der Typ der Spalte (z. B. Text, binär oder numerisch). Weitere Informationen finden Sie unter [JET_COLTYP](./jet-coltyp.md).

**cbMax**

Die maximale Länge einer Spalte variabler Länge in Bytes. Die Länge der Spalte für Spalten fester Länge.

**grbit**

Eine Gruppe von Bits, die die Optionen für diese Struktur enthalten und null oder mehr der folgenden Werte enthalten.

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
<td><p>Die Spalte ist fest. Es wird immer die gleiche Menge an Speicherplatz in einer Zeile verwendet, unabhängig davon, wie viele Daten in der Spalte gespeichert werden. JET_bitColumnFixed kann nicht mit -JET_bitColumnTagged. Dieses Bit kann nicht mit langen Werten wie JET_coltypLongText <strong>und</strong> <strong>JET_coltypLongBinary.</strong></p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTagged</p></td>
<td><p>Die Spalte ist markiert. Markierte Spalten nehmen keinen Speicherplatz in der Datenbank ein, wenn sie keine Daten enthalten. Dieses Bit kann nicht mit -JET_bitColumnFixed.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnNotNULL</p></td>
<td><p>Die Spalte darf nie auf einen NULL-Wert festgelegt werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnAutoincrement</p></td>
<td><p>Die Spalte wird automatisch erhöht. Die Zahl ist eine steigende Zahl und innerhalb einer Tabelle garantiert eindeutig. Die Zahl ist jedoch möglicherweise nicht kontinuierlich. Wenn beispielsweise fünf Zeilen in eine Tabelle eingefügt werden, kann die Spalte für die automatische Inkrementierung die Werte { 1, 2, 6, 7, 8 } enthalten.</p>
<p><strong>Windows 2000:</strong> Dieses Bit kann nur für Spalten vom Typ <strong>JET_coltypLong.</strong></p>
<p><strong>Windows Server 2003 und höher:</strong> Dieses Bit kann nur für Spalten vom Typ JET_coltypLong <strong>oder</strong> <strong>JET_coltypCurrency.</strong></p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUpdatable</p></td>
<td><p>Dieses Bit ist nur für Aufrufe von <a href="gg269215(v=exchg.10).md">JetGetColumnInfo gültig.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Dieses Bit ist nur für Aufrufe von <a href="gg269211(v=exchg.10).md">JetOpenTempTable gültig.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Dieses Bit ist nur für Aufrufe von <a href="gg269211(v=exchg.10).md">JetOpenTempTable gültig.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnMultiValued</p></td>
<td><p>Die Spalte kann mehrere Werte haben. Einer mehrwertigen Spalte können null, ein oder mehrere Werte zugeordnet sein. Die verschiedenen Werte in einer mehrwertigen Spalte werden durch das <strong>itagSequence-Member</strong> verschiedener Strukturen identifiziert, z. B. <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">, JET_ENUMCOLUMNVALUE</a>. Mehrwertige Spalten müssen mit Tags versehen sein. Das bedeutet, dass es sich nicht um Spalten fester länge oder variabler Länge handelt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnEscrowUpdate</p></td>
<td><p>Die Spalte ist eine Spalte zum Aktualisieren der Stirnrunzeln. Eine Spalte zum Aktualisieren der Stirnrunzeln kann gleichzeitig von verschiedenen Sitzungen mit <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> aktualisiert werden und die Transaktionskonsistenz erhalten.</p>
<ul>
<li><p>Eine Spalte zum Aktualisieren der Stirnrunzeln kann nur erstellt werden, wenn die Tabelle leer ist.</p></li>
<li><p>Eine Spalte zum Aktualisieren der Stirnrunzeln muss vom Typ <strong>JET_coltypLong.</strong></p></li>
<li><p>Eine Spalte zum Aktualisieren der Stirnrunzeln muss über einen Standardwert verfügen <strong>(cbDefault muss</strong> also positiv sein).</p></li>
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
<td><p>Die Spalte wird ohne Version erstellt. Andere Transaktionen, die versuchen, eine Spalte mit dem gleichen Namen hinzuzufügen, führen zu einem Fehler. Dieses Bit ist nur bei <a href="gg294122(v=exchg.10).md">JetAddColumn nützlich.</a> Sie kann nicht innerhalb einer Transaktion verwendet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnMaybeNull</p></td>
<td><p>Für die zukünftige Verwendung reserviert.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnFinalize</p></td>
<td><p>Verwenden JET_bitColumnDeleteOnZero anstelle von JET_bitColumnFinalize. JET_bitColumnFinalize gibt an, dass eine Spalte finalisiert werden kann. Wenn eine Spalte, die finalisiert werden kann, über eine Spalte mit einer Hinterlegungsaktualisierung verfügt, die 0 (null) erreicht, wird die Zeile gelöscht. Zukünftige Versionen können stattdessen eine Rückruffunktion aufrufen. Weitere Informationen finden Sie unter <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Eine Spalte, die finalisiert werden kann, muss eine Spalte zum Aktualisieren der Stirnrunzel sein. JET_bitColumnFinalize kann nicht mit -JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUserDefinedDefault</p></td>
<td><p>Der Standardwert für eine Spalte wird von der Rückruffunktion bereitgestellt, <a href="gg294098(v=exchg.10).md">JET_CALLBACK.</a> Eine Spalte mit einem benutzerdefinierten Standardwert muss eine markierte Spalte sein. <strong>pvDefault</strong> muss auf <a href="gg269200(v=exchg.10).md"></a> eine JET_USERDEFINEDDEFAULT-Struktur verweisen, <strong>und cbDefault</strong> muss auf sizeof( JET_USERDEFINEDDEFAULT<a href="gg269200(v=exchg.10).md">) festgelegt werden.</a></p>
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
<td><p>Bei der Spalte handelt es sich um eine Spalte zum Aktualisieren der Stirnrunzeln, und wenn sie 0 (null) erreicht, wird der Datensatz gelöscht. Eine häufige Verwendung für eine Spalte, die finalisiert werden kann, ist die Verwendung als Verweiszählerfeld, und wenn das Feld 0 (null) erreicht, wird der Datensatz gelöscht. JET_bitColumnDeleteOnZero bezieht sich auf JET_bitColumnFinalize. Eine delete-on-zero-Spalte muss eine Spalte für die Aktualisierung der Stirnrunzel sein. JET_bitColumnDeleteOnZero kann nicht mit JET_bitColumnFinalize verwendet werden. JET_bitColumnDeleteOnZero können nicht mit benutzerdefinierten Standardspalten verwendet werden.</p></td>
</tr>
</tbody>
</table>


**pvDefault**

Zeigt auf einen Puffer, der der Standardwert für eine Spalte ist. Die Länge des Puffers ist **cbDefault.** Wenn kein Standardwert vorhanden ist, sollte **pvDefault** auf NULL und **cbDefault** auf 0 (null) festgelegt werden. Wenn *grbit* JET_bitColumnUserDefinedDefault festgelegt ist, wird **pvDefault** als Zeiger auf eine JET_USERDEFINEDDEFAULT-Struktur interpretiert. Standardwerte dürfen nicht größer als 255 Bytes sein. Wenn ein Standardwert größer als 255 Bytes ist, wird er automatisch abgeschnitten.

**cbDefault**

Die Größe des durch **pvDefault** angegebenen Puffers in Bytes.

**cp**

Die Codepage für die Spalte. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252). Wenn die Spalte keine Textspalte ist, wird die Codepage automatisch auf 0 (null) festgelegt.

**Columnid**

Bei Erfolg wird der Spaltenbezeichner der neu erstellten Spalte in diesem Feld wieder übergeben. Bei einem Fehler ist der Wert nicht definiert.

**Err**

Das **Err-Feld** enthält den Status der Erstellung dieser Spalte. Eine Liste der wahrscheinlichen Rückgabewerte finden Sie unter [JetAddColumn.](./jetaddcolumn-function.md)

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
<td><p>Deklariert in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>JET_COLUMNCREATE_W</strong> (Unicode) und <strong>JET_COLUMNCREATE_A</strong> (ANSI).</p></td>
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
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JetEscrowUpdate](./jetescrowupdate-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
