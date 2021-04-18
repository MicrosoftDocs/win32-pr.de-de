---
description: 'Weitere Informationen finden Sie hier: JET_GRBIT'
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
ms.openlocfilehash: b050aaa844ea814c0c24a62ccfb5ab332c611107
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106365876"
---
# <a name="jet_grbit"></a>JET_GRBIT


_**Gilt für:** Windows | Windows Server_

## <a name="jet_grbit"></a>JET_GRBIT

Der **JET_GRBIT** -Datentyp ist eine Gruppe von Bits, die Konstanten enthalten, die für die Funktionen und Strukturen spezifisch sind, in denen Sie verwendet wird.

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a>Datentypen

JET_GRBIT

Im allgemeinen reflektieren die Konstanten, die als Werte für diesen Datentyp verwendet werden, den Namen des API-Elements, in dem Sie verwendet werden. Beispielsweise beginnen alle Konstanten, die an [jetretrievecolnumn](./jetretrievecolumn-function.md) übergebenen werden, mit "JET_bitRetrieve". Ebenso beginnen alle an [jetsetcolumn](./jetsetcolumn-function.md) übergebenen Konstanten mit "JET_bitSet".

Der Wert 0 (null) bewirkt, dass der-Parameter ignoriert wird.

### <a name="remarks"></a>Bemerkungen

Weitere Informationen finden Sie unter der jeweiligen Funktion oder Struktur. Die Optionen werden in der Regel als ein Satz von Flags, die kombiniert werden können, übermittelt.

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

[Jetretrievecolumschlag](./jetretrievecolumn-function.md)  
[Jetsetcolumn](./jetsetcolumn-function.md)
