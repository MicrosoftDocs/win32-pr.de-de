---
title: WTSLISTENERNAME (WtsApi32.h)
description: Stellt den Namen eines Remotedesktopdienste Listeners auf einem Remotedesktop-Sitzungshost (RD-Sitzungshost) dar.
ms.assetid: 3C41F507-6A67-4244-860F-E89B0F9E33B0
ms.tgt_platform: multiple
keywords:
- WTSLISTENERNAMEW
- WTSLISTENERNAMEA
- WTSLISTENERNAME
- PWTSLISTENERNAME
- WTSLISTENERNAME
- PWTSLISTENERNAME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce0df52229670cd090dd900dda3c2284437297bedc25c69f12c980b9cc40d92c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513840"
---
# <a name="wtslistenername"></a>WTSLISTENERNAME

Stellt den Namen eines Remotedesktopdienste Listeners auf einem Remotedesktop-Sitzungshost (RD-Sitzungshost) dar.


```C++
typedef WCHAR WTSLISTENERNAMEW[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEW;
typedef CHAR WTSLISTENERNAMEA[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEA;
#if UNICODE
typedef WTSLISTENERNAMEW WTSLISTENERNAME;
typedef PWTSLISTENERNAMEW PWTSLISTENERNAME;
#else 
typedef WTSLISTENERNAMEA WTSLISTENERNAME;
typedef PWTSLISTENERNAMEA PWTSLISTENERNAME;
#endif 
```



<dl> <dt>

**WTSLISTENERNAMEW**
</dt> <dd>

Der Unicode-Name des Listeners.

</dd> <dt>

**WTSLISTENERNAMEA**
</dt> <dd>

Ein Zeiger auf den ANSI-Namen des Listeners.

</dd> <dt>

**WTSLISTENERNAME**
</dt> <dd>

Der Name des Listeners.

</dd> <dt>

**PWTSLISTENERNAME**
</dt> <dd>

Ein Zeiger auf den Namen des Listeners.

</dd> <dt>

**WTSLISTENERNAME**
</dt> <dd>

Der Name des Listeners.

</dd> <dt>

**PWTSLISTENERNAME**
</dt> <dd>

Ein Zeiger auf den Namen des Listeners.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>WtsApi32.h</dt> </dl> |



 

 





