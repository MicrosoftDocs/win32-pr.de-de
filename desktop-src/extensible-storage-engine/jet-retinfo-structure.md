---
description: 'Weitere Informationen finden Sie hier: JET_RETINFO Struktur'
title: JET_RETINFO Struktur
TOCTitle: JET_RETINFO Structure
ms:assetid: a47a7902-3ecd-4d42-941f-89d25d78eb4c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294049(v=EXCHG.10)
ms:contentKeyID: 32765648
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
ms.openlocfilehash: 3452c4fab7155ea33b556ac7aa2c777b11a3f954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862967"
---
# <a name="jet_retinfo-structure"></a>JET_RETINFO Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_retinfo-structure"></a>JET_RETINFO Struktur

Die **JET_RETINFO** Struktur enthält optionale Eingabe-und Ausgabeparameter für [jetretrievecolumschlag](./jetretrievecolumn-function.md). Ein NULL-Zeiger kann an die Stelle geleitet werden, an der ein Zeiger auf diese-Struktur andernfalls passieren würde. Das Übergeben eines NULL-Zeigers ist identisch mit dem übergeben von **JET_RETINFO** , wobei **cbStruct** auf sizeof (JET_RETINFO) festgelegt ist, **iblongvalue** auf 0 (null) und **itagsequence** auf 1 festgelegt ist.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
    } JET_RETINFO;
```

### <a name="members"></a>Member

**cbStruct**

Muss auf die Größe der **JET_RETINFO** Struktur in Bytes festgelegt werden und stellt sicher, dass die folgenden Felder vorhanden sind.

**iblongvalue**

Der Offset zum ersten Byte, der aus einer Spalte vom Typ [JET_coltypLongBinary](./jet-coltyp.md)abgerufen werden soll, oder [JET_coltypLongText](./jet-coltyp.md). Beachten Sie, dass die Menge der Daten, die von diesem Offset abgerufen werden, die geringere Größe des Ausgabepuffers und die Größe der Daten im tatsächlichen Wert nach diesem Offset ist.

**itagsequence**

Beschreibt die Sequenznummer des Werts in einer mehrwertigen Spalte. Beachten Sie, dass das Array von Werten einbasiert ist. Der erste Wert ist Sequenz 1, nicht 0. Wenn die Daten Satz Spalte nur über einen Wert verfügt, sollte 1 als **itagsequence** übergeben werden.

Bei einer Spalte, die mehrere Werte enthalten kann, ist es nur möglich, eine Sequenznummer größer als 1 in [jetsetcolumn](./jetsetcolumn-function.md) und [jetretrievecolumschlag](./jetretrievecolumn-function.md) oder 0 in [jetsetcolumn](./jetsetcolumn-function.md)zu verwenden. In der aktuellen Implementierung der Engine kann jede Spalte, die mit JET_bitColumnTagged erstellt wurde, mehrere Werte enthalten. Spalten, die mit JET_bitColumnMultiValued erstellt werden, unterscheiden sich nur in der Art und Weise, in der Sie indiziert werden Weitere Informationen finden Sie unter [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

**columnidnexttaging**

Gibt das ColumnID der abgerufenen Spalte mit mehreren Werten oder geringer Dichte zurück, wenn alle markierten Spalten abgerufen werden, indem 0 als ColumnID an [jetretrievecolbin](./jetretrievecolumn-function.md)übergeben wird.

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
[JET_RETINFO]()  
[Jetretrievecolumschlag](./jetretrievecolumn-function.md)
