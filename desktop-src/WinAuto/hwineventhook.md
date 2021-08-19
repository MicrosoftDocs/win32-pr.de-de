---
title: HWINEVENTHOOK (Windef.h)
description: Wird verwendet, um eine Hookfunktion für Fensterereignisse zu deklarieren.
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- HWINEVENTHOOK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a26a2593af7db4520248b5ee319fd4143a79ab1393cef02365d1fe3ea8cc3f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994150"
---
# <a name="hwineventhook"></a>HWINEVENTHOOK

Wird verwendet, um eine Hookfunktion für Fensterereignisse zu deklarieren.


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a>Hinweise

Dieser Datentyp wird mit der [*WinEventProc-Rückruffunktion*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) und den [**Funktionen SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) und [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                                          |
| Verteilbare Komponente<br/>          | Active Accessibility 1.3 RDK unter Windows NT 4.0 mit SP6 und höher und Windows 95<br/>                                   |
| Header<br/>                   | <dl> <dt>Windef.h (WINVER >= 0x0500) (include Windows.h)</dt> </dl> |



 

 





