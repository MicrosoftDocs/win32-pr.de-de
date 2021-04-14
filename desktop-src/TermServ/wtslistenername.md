---
title: Wzlistenername (WtsApi32. h)
description: Stellt den Namen einer Remotedesktopdienste Listener auf einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server dar.
ms.assetid: 3C41F507-6A67-4244-860F-E89B0F9E33B0
ms.tgt_platform: multiple
keywords:
- Wout-listenernamew
- Wout-listenernamea
- Wzlistenername
- Pwzlistenername
- Wzlistenername
- Pwzlistenername
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a82576fc9f4490b133916852441c50dcf77e849d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392059"
---
# <a name="wtslistenername"></a>Wzlistenername

Stellt den Namen einer Remotedesktopdienste Listener auf einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server dar.


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

**Wout-listenernamew**
</dt> <dd>

Der Unicode-Name des Listener.

</dd> <dt>

**Wout-listenernamea**
</dt> <dd>

Ein Zeiger auf den ANSI-Namen des Listener.

</dd> <dt>

**Wzlistenername**
</dt> <dd>

Der Name des Listeners.

</dd> <dt>

**Pwzlistenername**
</dt> <dd>

Ein Zeiger auf den Namen des Listener.

</dd> <dt>

**Wzlistenername**
</dt> <dd>

Der Name des Listeners.

</dd> <dt>

**Pwzlistenername**
</dt> <dd>

Ein Zeiger auf den Namen des Listener.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>WtsApi32. h</dt> </dl> |



 

 





