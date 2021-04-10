---
title: RPC_STATUS (rpcdce. h)
description: Der RPC-Status des Datentyps \_ stellt einen plattformspezifischen Status Codetyp dar.
ms.assetid: 0f929916-f3aa-477f-9c61-742f3fbbab29
keywords:
- RPC_STATUS
- RPC_STATUS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066022ce33676caadcf25a6814f3b4974701998e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040574"
---
# <a name="rpc_status"></a>RPC- \_ Status

Der RPC- **\_ Status** des Datentyps stellt einen plattformspezifischen Status Codetyp dar.


```C++
typedef long RPC_STATUS;
typedef unsigned short RPC_STATUS;
```



## <a name="remarks"></a>Bemerkungen

Der **RPC- \_ statentyp** wird von den meisten RPC-Funktionen zurückgegeben und ist Teil der [**\_ \_ INQ \_ FN**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn) -Funktionstyp Definition für das RPC-Objekt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Rpcdce. h (Include RPC. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RPC- \_ Objekt \_ INQ \_ FN**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)
</dt> </dl>

 

 





