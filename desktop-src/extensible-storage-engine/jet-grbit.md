---
description: 'Weitere Informationen finden Sie unter: JET_GRBIT'
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
ms.openlocfilehash: 7aa3a0331244aa1f5dd07794204d5a94d57aeadb
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984173"
---
# <a name="jet_grbit"></a>JET_GRBIT


_**Gilt für:** Windows | Windows Server_

## <a name="jet_grbit"></a>JET_GRBIT

Der **JET_GRBIT** ist eine Gruppe von Bits, die Konstanten enthalten, die spezifisch für die Funktionen und Strukturen sind, in denen sie verwendet werden.

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a>Datentypen

JET_GRBIT

Im Allgemeinen spiegeln die Konstanten, die als Werte für diesen Datentyp verwendet werden, den Namen des API-Elements wider, in dem sie verwendet werden. Beispielsweise beginnen alle an [JetRetrieveColumn](./jetretrievecolumn-function.md) übergebenen Konstanten mit "JET_bitRetrieve". Ebenso beginnen alle an [JetSetColumn übergebenen](./jetsetcolumn-function.md) Konstanten mit "JET_bitSet".

Der Wert 0 (null) bewirkt, dass der Parameter ignoriert wird.

### <a name="remarks"></a>Bemerkungen

Weitere Informationen finden Sie unter der spezifischen Funktion oder Struktur. Die Optionen werden in der Regel als eine Gruppe von Flags übergeben, die kombiniert werden können.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
