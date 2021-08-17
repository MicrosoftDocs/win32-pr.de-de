---
description: 'Weitere Informationen zu: JET_GRBIT'
title: JET_GRBIT
TOCTitle: JET_GRBIT
ms:assetid: b72548cf-3ca2-4ba5-b07a-35eb7e85ed2b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294066(v=EXCHG.10)
ms:contentKeyID: 32765681
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
ms.openlocfilehash: 2b54ed8a95d81c148b68727384dd76fba3d2dc8b1f9d6452c2105bc45f015646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119362280"
---
# <a name="jet_grbit"></a>JET_GRBIT


_**Gilt für:** Windows | Windows Server_

## <a name="jet_grbit"></a>JET_GRBIT

Der **JET_GRBIT** Datentyp ist eine Gruppe von Bits, die Konstanten enthalten, die spezifisch für die Funktionen und Strukturen sind, in denen er verwendet wird.

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a>Datentypen

JET_GRBIT

Im Allgemeinen geben die Konstanten, die als Werte für diesen Datentyp verwendet werden, den Namen des API-Elements wieder, in dem sie verwendet werden. Beispielsweise beginnen alle an [JetRetrieveColumn](./jetretrievecolumn-function.md) übergebenen Konstanten mit "JET_bitRetrieve". Ebenso beginnen alle an [JetSetColumn](./jetsetcolumn-function.md) übergebenen Konstanten mit "JET_bitSet".

Der Wert 0 (null) bewirkt, dass der Parameter ignoriert wird.

### <a name="remarks"></a>Hinweise

Weitere Informationen finden Sie in der spezifischen Funktion oder Struktur. Die Optionen werden in der Regel als Gruppe von Flags übergeben, die kombiniert werden können.

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

[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
