---
description: 'Weitere Informationen finden Sie unter: JET_INSTANCE'
title: JET_INSTANCE
TOCTitle: JET_INSTANCE
ms:assetid: a4136bec-95b3-42d7-b21b-1df09197bb11
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294048(v=EXCHG.10)
ms:contentKeyID: 32765647
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
ms.openlocfilehash: 63e621633bdc0b863a6fdabdd17738d6ef7f4e8e3b35f374aae3362379b7bdcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118980012"
---
# <a name="jet_instance"></a>JET_INSTANCE


_**Gilt für:** Windows | Windows Server_

## <a name="jet_instance"></a>JET_INSTANCE

Der **JET_INSTANCE** enthält ein Handle für die Instanz der Datenbank, das für einen Aufruf der JET-API verwendet werden soll.

```cpp
    typedef JET_API_PTR JET_INSTANCE;
```

### <a name="data-types"></a>Datentypen

JET_INSTANCE

Null  oder [JET_instanceNil](./invalid-handle-constants.md) kann verwendet werden, um ein ungültiges Instanzhand handle anzugeben.

### <a name="remarks"></a>Hinweise

Dieses Handle wird beim Erstellen einer Instanz der Datenbank durch Aufrufen der [JetCreateInstance-,](./jetcreateinstance-function.md) [JetCreateInstance2-,](./jetcreateinstance2-function.md) [JetInit-](./jetinit-function.md)oder [JetInit2-Funktionen](./jetinit2-function.md) erhalten.

**Windows XP:**  Die explizite Verwendung von -Instanzen wird nur auf Windows XP und späteren Versionen unterstützt.

**Windows 2000:**  Pro Prozess wird nur eine globale Instanz unterstützt.

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
<td><p>Wird in Esent.h deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)
