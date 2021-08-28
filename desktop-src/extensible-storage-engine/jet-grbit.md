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
ms.openlocfilehash: 92fa6dffd94d2a1790811881fcdba86665ebb880
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482246"
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


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
