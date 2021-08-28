---
description: Wird an die Nachrichtenwarteschlange des Installationsthreads gesendet, wenn ein Timer abläuft. Die Nachricht wird von der GetMessage- oder PeekMessage-Funktion bereitgestellt.
ms.assetid: 419e3f05-35ec-4e48-b24d-ab98df687b20
title: WM_TIMER Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d770d640b801849eeebe1c4ec86df8c41642c6149b89e00d82261f4e090f56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710030"
---
# <a name="wm_timer-message"></a>WM \_ TIMER-Meldung

Wird an die Nachrichtenwarteschlange des Installationsthreads gesendet, wenn ein Timer abläuft. Die Nachricht wird von der [**GetMessage-**](/windows/win32/api/winuser/nf-winuser-getmessage) oder [**PeekMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-peekmessagea) bereitgestellt.


```C++
#define WM_TIMER                        0x0113
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Der Timerbezeichner.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Ein Zeiger auf eine anwendungsdefinierte Rückruffunktion, die bei der Installation des Timers an die [**SetTimer-Funktion**](/windows/win32/api/winuser/nf-winuser-settimer) übergeben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Eine Anwendung sollte 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Hinweise

Sie können die Nachricht verarbeiten, indem Sie im Fensterverfahren einen **WM \_ TIMER-Fall** bereitstellen. Andernfalls ruft [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) die [*TimerProc-Rückruffunktion*](/windows/win32/api/winuser/nc-winuser-timerproc) auf, die im Aufruf der [**SetTimer-Funktion**](/windows/win32/api/winuser/nf-winuser-settimer) angegeben ist, die zum Installieren des Timers verwendet wird.

Die **WM \_ TIMER-Nachricht** ist eine Nachricht mit niedriger Priorität. Die Funktionen [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) und [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) stellen diese Nachricht nur dann bereit, wenn sich keine anderen Nachrichten mit höherer Priorität in der Nachrichtenwarteschlange des Threads befinden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)
</dt> <dt>

[**TimerProc**](/windows/win32/api/winuser/nc-winuser-timerproc)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Timer](timers.md)
</dt> </dl>

 

 
