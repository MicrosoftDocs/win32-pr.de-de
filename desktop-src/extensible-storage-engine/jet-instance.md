---
description: 'Weitere Informationen zu: JET_INSTANCE'
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
ms.openlocfilehash: 1fc288c17c90070d48669c7ad6f1554d52c83278
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481766"
---
# <a name="jet_instance"></a>JET_INSTANCE


_**Gilt für:** Windows | Windows Server_

## <a name="jet_instance"></a>JET_INSTANCE

Der **JET_INSTANCE** Datentyp enthält ein Handle für die Instanz der Datenbank, die für einen Aufruf der JET-API verwendet werden soll.

```cpp
    typedef JET_API_PTR JET_INSTANCE;
```

### <a name="data-types"></a>Datentypen

JET_INSTANCE

Entweder **NULL** oder [JET_instanceNil](./invalid-handle-constants.md) können verwendet werden, um ein ungültiges Instanzhandle anzugeben.

### <a name="remarks"></a>Hinweise

Dieses Handle wird abgerufen, wenn Sie eine Instanz der Datenbank erstellen, indem Sie die Funktionen [JetCreateInstance,](./jetcreateinstance-function.md) [JetCreateInstance2,](./jetcreateinstance2-function.md) [JetInit](./jetinit-function.md)oder [JetInit2](./jetinit2-function.md) aufrufen.

**Windows XP:**  Die explizite Verwendung von -Instanzen wird nur für Windows XP und höhere Versionen unterstützt.

**Windows 2000:**  Pro Prozess wird nur eine globale Instanz unterstützt.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)
