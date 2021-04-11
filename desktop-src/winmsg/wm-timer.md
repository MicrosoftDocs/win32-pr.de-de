---
description: Wird in der Meldungs Warteschlange des Installations Threads gepostet, wenn ein Timer abläuft. Die Nachricht wird von der getMessage-Funktion oder der Peer Message-Funktion gepostet.
ms.assetid: 419e3f05-35ec-4e48-b24d-ab98df687b20
title: WM_TIMER Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c99db67c9c9b3419e477ccd0a78133df453a7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217512"
---
# <a name="wm_timer-message"></a>WM-Zeit Geber \_ Meldung

Wird in der Meldungs Warteschlange des Installations Threads gepostet, wenn ein Timer abläuft. Die Nachricht wird von der [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -Funktion oder der [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) -Funktion gepostet.


```C++
#define WM_TIMER                        0x0113
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Der timerbezeichner.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Anwendungs definierte Rückruffunktion, die bei der Installation des Timers an die [**SETTIMER**](/windows/win32/api/winuser/nf-winuser-settimer) -Funktion übermittelt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Sie können die Nachricht verarbeiten, indem Sie **einen \_ WM** -Zeit Geber Fall in der Fenster Prozedur bereitstellen. Andernfalls ruft [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) die [*timerproc*](/windows/win32/api/winuser/nc-winuser-timerproc) -Rückruffunktion auf, die im [**Aufrufen der Funktion "-Funktion"**](/windows/win32/api/winuser/nf-winuser-settimer) angegeben ist, die zum Installieren des Timers verwendet wird.

Die WM-Zeit Geber Nachricht ist eine Nachricht mit niedriger Priorität. **\_** Die Funktionen [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) und [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) stellen diese Nachricht nur dann bereit, wenn sich keine anderen Nachrichten mit höherer Priorität in der Nachrichten Warteschlange des Threads befinden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**Ziel**](/windows/win32/api/winuser/nf-winuser-settimer)
</dt> <dt>

[**Timerproc**](/windows/win32/api/winuser/nc-winuser-timerproc)
</dt> <dt>

**Licher**
</dt> <dt>

[Timer](timers.md)
</dt> </dl>

 

 
