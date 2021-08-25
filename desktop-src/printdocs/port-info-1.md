---
description: Die \_ PORT INFO \_ 1-Struktur identifiziert einen unterstützten Druckerport.
ms.assetid: e474fe9c-e554-406a-a5bf-de07f9a72b32
title: PORT_INFO_1-Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_1
- _PORT_INFO_1A
- _PORT_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ff6e4c3a43c35118772aede2e329a2e1e761fc0f147b5a3a9ceeef97bbf8fb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947810"
---
# <a name="port_info_1-structure"></a>PORT \_ INFO \_ 1-Struktur

Die **PORT \_ INFO \_ 1-Struktur** identifiziert einen unterstützten Druckerport.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PORT_INFO_1 {
  LPTSTR pName;
} PORT_INFO_1, *PPORT_INFO_1;
```



## <a name="members"></a>Member

<dl> <dt>

**pName**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die einen unterstützten Druckerport identifiziert (z.B. "LPT1:").

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ PORT \_ INFO \_ 1W** (Unicode) und **\_ PORT INFO \_ \_ 1A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




