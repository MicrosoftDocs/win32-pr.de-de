---
description: 'Weitere Informationen zu: JET_RETINFO-Struktur'
title: JET_RETINFO-Struktur
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
ms.openlocfilehash: a04ee087f036bf0d6a9e0bb4c9c558dbfe3ae5a8fc8e875973ef2930e7ba911a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038728"
---
# <a name="jet_retinfo-structure"></a>JET_RETINFO-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_retinfo-structure"></a>JET_RETINFO-Struktur

Die **JET_RETINFO-Struktur** enthält optionale Eingabe- und Ausgabeparameter für [JetRetrieveColumn.](./jetretrievecolumn-function.md) Ein NULL-Zeiger kann übergeben werden, wenn andernfalls ein Zeiger auf diese Struktur übergeben würde. Das Übergeben eines NULL-Zeigers entspricht der Übergabe **von JET_RETINFO,** wobei **cbStruct** auf sizeof(JET_RETINFO), **ibLongValue** auf 0 (null) und **itagSequence** auf 1 festgelegt ist.

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

Muss auf die Größe der **JET_RETINFO-Struktur** in Bytes festgelegt werden und dient zur Bestätigung des Vorhandenseins der folgenden Felder.

**ibLongValue**

Der Offset zum ersten Byte, das aus einer Spalte vom Typ [JET_coltypLongBinary](./jet-coltyp.md)oder [JET_coltypLongText](./jet-coltyp.md)abgerufen werden soll. Beachten Sie, dass die Menge der aus diesem Offset abgerufenen Daten die niedrigere Größe des Ausgabepuffers und die Größe der Daten im tatsächlichen Wert nach diesem Offset ist.

**itagSequence**

Beschreibt die Sequenznummer des Werts in einer mehrwertigen Spalte. Beachten Sie, dass das Array von Werten einsbasiert ist. Der erste Wert ist Sequenz 1, nicht 0. Wenn die Datensatzspalte nur über einen Wert verfügt, sollte 1 als **itagSequence** übergeben werden.

Bei einer Spalte, die mehrere Werte enthalten kann, ist es nur möglich, eine Sequenznummer größer als 1 in [JetSetColumn](./jetsetcolumn-function.md) und [JetRetrieveColumn](./jetretrievecolumn-function.md) oder 0 in [JetSetColumn](./jetsetcolumn-function.md)zu verwenden. In der aktuellen Implementierung der Engine kann jede Spalte, die mit JET_bitColumnTagged erstellt wurde, mehrere Werte enthalten. Spalten, die mit JET_bitColumnMultiValued erstellt wurden, unterscheiden sich von mehrwertigen markierten Spalten nur in der Weise, wie sie indiziert werden. Weitere Informationen finden Sie [unter JET_INDEXCREATE.](./jet-indexcreate-structure.md)

**columnidNextTagged**

Gibt die columnid der abgerufenen markierten, mehrwertigen oder sparsebasierten Spalte zurück, wenn alle markierten Spalten abgerufen werden, indem 0 als columnid an [JetRetrieveColumn](./jetretrievecolumn-function.md)übergeben wird.

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
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_RETINFO]()  
[JetRetrieveColumn](./jetretrievecolumn-function.md)
