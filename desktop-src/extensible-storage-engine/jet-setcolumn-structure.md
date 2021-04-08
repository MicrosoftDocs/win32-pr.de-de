---
description: 'Weitere Informationen finden Sie hier: JET_SETCOLUMN Struktur'
title: JET_SETCOLUMN Struktur
TOCTitle: JET_SETCOLUMN Structure
ms:assetid: 3fdb8ec0-3c40-44f3-9859-72e22a504b90
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269233(v=EXCHG.10)
ms:contentKeyID: 32765535
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
ms.openlocfilehash: a170132fd4d832133e0f0bcad4a3499fa743db38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750520"
---
# <a name="jet_setcolumn-structure"></a>JET_SETCOLUMN Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_setcolumn-structure"></a>JET_SETCOLUMN Struktur

Die **JET_SETCOLUMN** -Struktur enthält Eingabe-und Ausgabeparameter für [jetsetcolumns](./jetsetcolumns-function.md). Felder in der Struktur beschreiben, welcher Spaltenwert festgelegt werden soll, wie er festgelegt wird und wo die Spalten Satz Daten zu finden sind.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      const void* pvData;
      unsigned long cbData;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_ERR err;
    } JET_SETCOLUMN;
```

### <a name="members"></a>Member

**ColumnID**

Der Spalten Bezeichner für eine Spalte, die festgelegt werden soll.

**pvData**

Ein Zeiger auf Daten, die in eine Spalte festgelegt werden sollen.

**cbData**

Die Größe der Zuordnung in Bytes, beginnend bei **pvData** (in Bytes).

**grbit**

Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten.

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
<td><p>JET_bitSetAppendLV</p></td>
<td><p>Fügt Daten an eine Spalte vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>an. Das gleiche Verhalten können Sie erreichen, indem Sie die Größe des vorhandenen Long-Werts ermitteln und <strong>iblongvalue</strong> in <strong>psetup</strong>angeben. Es ist jedoch einfacher, dieses <em>grbit</em>zu verwenden, da das Wissen der Größe des vorhandenen Spaltenwerts nicht erforderlich ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetOverwriteLV</p></td>
<td><p>Ersetzt den vorhandenen Long-Wert durch die neuen Daten. Wenn diese Option verwendet wird, ist es so, als ob der vorhandene Long-Wert auf 0 (null) festgelegt wurde, bevor die neuen Daten festgelegt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSizeLV</p></td>
<td><p>Interpretiert den Eingabepuffer als ganzzahlige Anzahl von Bytes, die als Länge des Long-Werts festgelegt werden soll, der durch das angegebene ColumnID und ggf. die Sequenznummer in psetinfo- &gt; itagsequence beschrieben wird. Wenn die angegebene Größe größer ist als der vorhandene Spaltenwert, wird die Spalte um 0s erweitert. Wenn die Größe kleiner als der vorhandene Spaltenwert ist, wird der Wert abgeschnitten.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetZeroLength</p></td>
<td><p>Legt einen Wert auf die Länge 0 (null) fest. Normalerweise wird ein Spaltenwert auf NULL festgelegt, indem ein cbmax von 0 übergeben wird. Bei manchen Typen, wie z. b. <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, kann ein Spaltenwert jedoch eine Länge von 0 (null) und nicht NULL sein, und diese Option wird verwendet, um zwischen null und 0 zu unterscheiden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSeparateLV</p></td>
<td><p>Erzwingt, dass ein langer Wert, Spalten vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>getrennt vom Rest der Daten Satz Daten gespeichert werden. Dies tritt normalerweise auf, wenn die Größe des Long-Werts verhindert, dass Sie mit den verbleibenden Daten Satz Daten gespeichert wird. Diese Option kann jedoch verwendet werden, um zu erzwingen, dass der lange Wert separat gespeichert wird. Beachten Sie, dass lange Werte, die vier Bytes groß oder kleiner sind, nicht getrennt werden können. In solchen Fällen wird die Option ignoriert.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetUniqueMultiValues</p></td>
<td><p>Erzwingt unterschiedliche Werte in einer mehrwertigen Spalte. Mit dieser Option werden die Quell Spaltendaten ohne Transformationen mit anderen vorhandenen Spaltenwerten verglichen, und es wird ein Fehler zurückgegeben, wenn ein Duplikat gefunden wird. Wenn diese Option angegeben wird, können JET_bitSetAppendLv, JET_bitSetOverwriteLV und JET_bitSetSizeLV nicht ebenfalls angegeben werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUniqueNormalizedMultiValues</p></td>
<td><p>Erzwingt unterschiedliche Werte in einer mehrwertigen Spalte. Mit dieser Option wird die normalisierte Transformation von Spaltendaten mit anderen ähnlich transformierten vorhandenen Spaltenwerten verglichen, und es wird ein Fehler zurückgegeben, wenn ein Duplikat gefunden wird. Wenn diese Option angegeben wird, können JET_bitSetAppendLv, JET_bitSetOverwriteLV und JET_bitSetSizeLV nicht ebenfalls angegeben werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetRevertToDefaultValue</p></td>
<td><p>Bewirkt, dass die Spalte für nachfolgende Vorgänge zum Abrufen von Spalten den Standard Spaltenwert zurückgibt. Alle vorhandenen Spaltenwerte werden entfernt. Diese Option gilt nur für gekennzeichnete, sparsespalten oder mehrwertige Spalten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetIntrinsicLV</p></td>
<td><p>Behält den langen Wert, Spalten vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder JET_coltypeLongBinary bei Bedarf mit den verbleibenden Daten Satz Daten. Normalerweise werden lange Spalten separat gespeichert, wenn Ihre Länge 1024 Bytes überschreitet oder andernfalls die Daten Satz Länge die Größe der Größenbeschränkung auf Seitengröße überschreiten würde. Wenn diese Option festgelegt ist, schlägt der Vorgang zum Festlegen von Spalten jedoch mit einem Fehler JET_errColumnTooBig fehl, anstatt diesen Spaltenwert getrennt von den verbleibenden Daten Satz Daten zu speichern.</p></td>
</tr>
</tbody>
</table>


**iblongvalue**

Der Offset zum ersten Byte, der aus einer Spalte vom Typ [JET_coltypLongBinary](./jet-coltyp.md)abgerufen werden soll, oder [JET_coltypLongText](./jet-coltyp.md).

**itagsequence**

Beschreibt die Sequenznummer des Werts in einer mehrwertigen Spalte. Eine **itagsequence** von 0 gibt an, dass der festgelegte Spaltenwert als neue Instanz einer mehrwertigen Spalte hinzugefügt werden soll.

**irre**

Fehlercodes und Warnungen, die vom Vorgang zum Festlegen der Spalte zurückgegeben werden.

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[Jetsetcolumns](./jetsetcolumns-function.md)
