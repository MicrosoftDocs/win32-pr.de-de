---
description: 'Weitere Informationen finden Sie hier: JET_SETINFO Struktur'
title: JET_SETINFO Struktur
TOCTitle: JET_SETINFO Structure
ms:assetid: cbc41175-e48f-46b0-aeb1-1120fa2cd981
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294090(v=EXCHG.10)
ms:contentKeyID: 32765705
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
ms.openlocfilehash: 69602aad89142d9f5dc202074ca54cf278767892
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531118"
---
# <a name="jet_setinfo-structure"></a>JET_SETINFO Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_setinfo-structure"></a>JET_SETINFO Struktur

Die **JET_SETINFO** Struktur enthält optionale Eingabeparameter für [jetsetcolumn](./jetsetcolumn-function.md). Ein **null** -Zeiger kann an die Stelle geleitet werden, an der ein Zeiger auf diese-Struktur andernfalls passieren würde. Die Übergabe eines **null** -Werts ist identisch mit dem übergeben von **JET_SETINFO** , wobei **cbStruct** auf sizeof (JET_SETINFO) festgelegt ist, **iblongvalue** auf 0 (null) und **itagsequence** auf 1 festgelegt ist.

```cpp
typedef struct {
  unsigned long cbStruct;
  unsigned long ibLongValue;
  unsigned long itagSequence;
} JET_SETINFO;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe (in Bytes) der **JET_SETINFO**. Dieser Wert bestätigt, dass die folgenden Felder vorhanden sind.

**iblongvalue**

Der Offset zum ersten Byte, der in einer Spalte vom Typ [JET_coltypLongBinary](./jet-coltyp.md) oder [JET_coltypLongText](./jet-coltyp.md)festgelegt werden soll.

**itagsequence**

Beschreibt die Sequenznummer des Werts in einer mehrwertigen Spalte, die festgelegt werden soll. Das Array von Werten ist 1-basiert. Der erste Wert ist Sequenz 1, nicht 0 (null). Wenn die Daten Satz Spalte nur über einen Wert verfügt, sollte 1 als **itagsequence** übergeben werden, wenn dieser Wert ersetzt wird. Der Wert 0 (null) bedeutet, dass am Ende der Sequenz der Spaltenwerte eine neue Spaltenwert Instanz hinzugefügt wird.

Bei einer Spalte, die mehrere Werte enthalten kann, ist es nur möglich, eine Sequenznummer größer als 1 in [jetsetcolumn](./jetsetcolumn-function.md) und [jetretrievecolumschlag](./jetretrievecolumn-function.md) oder 0 in [jetsetcolumn](./jetsetcolumn-function.md)zu verwenden. In der aktuellen Implementierung der Engine kann jede Spalte, die mit JET_bitColumnTagged erstellt wurde, mehrere Werte enthalten. Spalten, die mit JET_bitColumnMultiValued erstellt werden, unterscheiden sich nur in der Art und Weise, in der Sie indiziert werden Weitere Informationen finden Sie unter [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

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

[Jetsetcolumn](./jetsetcolumn-function.md)
