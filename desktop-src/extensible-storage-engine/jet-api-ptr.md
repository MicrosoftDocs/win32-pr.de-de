---
description: 'Weitere Informationen zu: JET_API_PTR'
title: JET_API_PTR
TOCTitle: JET_API_PTR
ms:assetid: 27b1eeec-1707-4edb-a4b2-2619190c21e7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269209(v=EXCHG.10)
ms:contentKeyID: 32765512
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
ms.openlocfilehash: 401c490c667cd8f9842a7ab0429e10a510e3b06e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466397"
---
# <a name="jet_api_ptr"></a>JET_API_PTR


_**Gilt für:** Windows | Windows Server_

## <a name="jet_api_ptr"></a>JET_API_PTR

Der **JET_API_PTR** Datentyp enthält eine ganze Zahl oder einen Zeigerwert.

```cpp
    #if defined(_WIN64)
        typedef unsigned __int64 JET_API_PTR;
    #elif !defined(__midl) && (defined(_X86_) || defined(_M_IX86)) && _MSC_VER >= 1300
        typedef __w64 unsigned long JET_API_PTR;
    #else
        typedef unsigned long JET_API_PTR;
    #endif
```

### <a name="data-types"></a>Datentypen

JET_API_PTR

Wie ein **DWORD_PTR** Datentyp wird der **JET_API_PTR** Datentyp auf einem 32-Bit-Computer als 4 Bytes und auf einem 64-Bit-Computer als 8 Bytes definiert.

### <a name="remarks"></a>Hinweise

Der **JET_API_PTR** Datentyp wird verwendet, um die folgenden Datentypen zu definieren:

  - [JET_HANDLE](./jet-handle.md)

  - [JET_INSTANCE](./jet-instance.md)

  - [JET_SESID](./jet-sesid.md)

  - [JET_TABLEID](./jet-tableid.md)

  - [JET_LS](./jet-ls.md)

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 

