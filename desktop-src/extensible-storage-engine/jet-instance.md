---
description: 'Weitere Informationen finden Sie hier: JET_INSTANCE'
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
ms.openlocfilehash: 6e1fde3e01c8328d2fdaf6609c6772fda9cd1428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960299"
---
# <a name="jet_instance"></a>JET_INSTANCE


_**Gilt für:** Windows | Windows Server_

## <a name="jet_instance"></a>JET_INSTANCE

Der **JET_INSTANCE** -Datentyp enthält ein Handle für die Instanz der-Datenbank, die für einen aufzurufenden Jet-API-Befehl verwendet werden soll.

```cpp
    typedef JET_API_PTR JET_INSTANCE;
```

### <a name="data-types"></a>Datentypen

JET_INSTANCE

Entweder **null** oder [JET_instanceNil](./invalid-handle-constants.md) kann verwendet werden, um ein ungültiges Instanzhandle anzugeben.

### <a name="remarks"></a>Bemerkungen

Dieses Handle wird abgerufen, wenn Sie eine Instanz der Datenbank erstellen, indem Sie die [jetcreateinstance](./jetcreateinstance-function.md)-, [JetCreateInstance2](./jetcreateinstance2-function.md)-, [jetinit](./jetinit-function.md)-oder [JetInit2](./jetinit2-function.md) -Funktion aufrufen.

**Windows XP:**  Die explizite Verwendung von-Instanzen wird nur unter Windows XP und höheren Versionen unterstützt.

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
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[Jetkreateingestance](./jetcreateinstance-function.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)
