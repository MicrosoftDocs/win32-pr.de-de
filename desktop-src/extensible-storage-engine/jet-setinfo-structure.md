---
description: 'Weitere Informationen finden Sie unter: JET_SETINFO Struktur'
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
ms.openlocfilehash: 4198598a95134291e9b9aa88eb9dcdf4ada79045
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983813"
---
# <a name="jet_setinfo-structure"></a>JET_SETINFO Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_setinfo-structure"></a>JET_SETINFO Struktur

Die **JET_SETINFO-Struktur** enthält optionale Eingabeparameter für [JetSetColumn.](./jetsetcolumn-function.md) Ein **NULL-Zeiger** kann übergeben werden, wenn andernfalls ein Zeiger auf diese Struktur übergeben würde. Die Bedeutung der Übergabe eines **NULL-Werts** ist identisch mit der Übergabe von **JET_SETINFO** mit **cbStruct,** die auf sizeof(JET_SETINFO), **ibLongValue** auf 0 (null) und **itagSequence** auf 1 festgelegt ist.

```cpp
typedef struct {
  unsigned long cbStruct;
  unsigned long ibLongValue;
  unsigned long itagSequence;
} JET_SETINFO;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe des -JET_SETINFO **.** Dieser Wert bestätigt das Vorhandensein der folgenden Felder.

**ibLongValue**

Der Offset zum ersten Byte, das in einer Spalte vom Typ JET_coltypLongBinary [oder](./jet-coltyp.md) [JET_coltypLongText.](./jet-coltyp.md)

**itagSequence**

Beschreibt die Sequenznummer des Werts in einer mehrwertigen Spalte, die festgelegt werden soll. Das Array von Werten ist 1-basiert. Der erste Wert ist Sequenz 1, nicht 0 (null). Wenn die Datensatzspalte nur einen Wert hat, sollte 1 als **itagSequence** übergeben werden, wenn dieser Wert ersetzt wird. Der Wert 0 (null) bedeutet, dass am Ende der Sequenz von Spaltenwerten eine neue Spaltenwertinstanz hinzugefügt wird.

Bei einer Spalte, die mehrere Werte enthalten kann, ist es nur möglich, eine Sequenznummer größer als 1 in [JetSetColumn](./jetsetcolumn-function.md) und [JetRetrieveColumn](./jetretrievecolumn-function.md) oder 0 in [JetSetColumn](./jetsetcolumn-function.md)zu verwenden. In der aktuellen Implementierung der Engine kann jede Spalte, die mit einem -JET_bitColumnTagged erstellt wurde, mehrere Werte enthalten. Spalten, die mit JET_bitColumnMultiValued werden, unterscheiden sich von spalten mit mehreren Tags nur in der Art und Weise, wie sie indiziert werden. Weitere [JET_INDEXCREATE](./jet-indexcreate-structure.md) finden Sie unter .

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetSetColumn](./jetsetcolumn-function.md)
