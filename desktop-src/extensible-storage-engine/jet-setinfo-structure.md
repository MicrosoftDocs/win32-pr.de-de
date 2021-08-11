---
description: 'Weitere Informationen zu: JET_SETINFO-Struktur'
title: JET_SETINFO-Struktur
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
ms.openlocfilehash: 379fd60a001312152dbe181c27a3e8158ceca79b4cfa9075a530b6c73f4337cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118253441"
---
# <a name="jet_setinfo-structure"></a>JET_SETINFO-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_setinfo-structure"></a>JET_SETINFO-Struktur

Die **JET_SETINFO-Struktur** enthält optionale Eingabeparameter für [JetSetColumn.](./jetsetcolumn-function.md) Ein **NULL-Zeiger** kann übergeben werden, wenn andernfalls ein Zeiger auf diese Struktur übergeben würde. Die Bedeutung der Übergabe eines **NULL-Werts** entspricht der Übergabe **von JET_SETINFO,** wobei **cbStruct** auf sizeof(JET_SETINFO), **ibLongValue** auf 0 (null) und **itagSequence** auf 1 festgelegt ist.

```cpp
typedef struct {
  unsigned long cbStruct;
  unsigned long ibLongValue;
  unsigned long itagSequence;
} JET_SETINFO;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe des **JET_SETINFO** in Bytes. Dieser Wert bestätigt das Vorhandensein der folgenden Felder.

**ibLongValue**

Der Offset zum ersten Byte, das in einer Spalte vom Typ [JET_coltypLongBinary](./jet-coltyp.md) oder [JET_coltypLongText](./jet-coltyp.md)festgelegt werden soll.

**itagSequence**

Beschreibt die Sequenznummer des Werts in einer mehrwertigen Spalte, die festgelegt werden soll. Das Array von Werten ist einsbasiert. Der erste Wert ist sequenz 1, nicht 0 (null). Wenn die Datensatzspalte nur über einen Wert verfügt, sollte 1 als **itagSequence** übergeben werden, wenn dieser Wert ersetzt wird. Der Wert 0 (null) bedeutet, dass am Ende der Sequenz von Spaltenwerten eine neue Spaltenwertinstanz hinzugefügt wird.

Bei einer Spalte, die mehrere Werte enthalten kann, ist es nur möglich, eine Sequenznummer größer als 1 in [JetSetColumn](./jetsetcolumn-function.md) und [JetRetrieveColumn](./jetretrievecolumn-function.md) oder 0 in [JetSetColumn](./jetsetcolumn-function.md)zu verwenden. In der aktuellen Implementierung der Engine kann jede Spalte, die mit JET_bitColumnTagged erstellt wurde, mehrere Werte enthalten. Spalten, die mit JET_bitColumnMultiValued erstellt werden, unterscheiden sich von mehrwertigen markierten Spalten nur in der Weise, wie sie indiziert werden. Weitere Informationen finden [Sie unter JET_INDEXCREATE.](./jet-indexcreate-structure.md)

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

[JetSetColumn](./jetsetcolumn-function.md)
