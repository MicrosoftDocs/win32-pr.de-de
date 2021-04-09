---
description: Gibt eine Anforderung zum Beenden einer Anwendung an und wird generiert, wenn die Anwendung die PostQuitMessage-Funktion aufruft. Diese Meldung bewirkt, dass die getMessage-Funktion 0 zurückgibt.
ms.assetid: a9bff5dc-cab8-4e08-838e-d92c87c265d6
title: WM_QUIT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e0d7413d65e9a0fb451fe63504f2ed5be02064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042289"
---
# <a name="wm_quit-message"></a>WM- \_ beendenmeldung

Gibt eine Anforderung zum Beenden einer Anwendung an und wird generiert, wenn die Anwendung die [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) -Funktion aufruft. Diese Meldung bewirkt, dass die [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -Funktion 0 zurückgibt.


```C++
#define WM_QUIT                         0x0012
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Exitcode, der in der [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) -Funktion angegeben wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Diese Nachricht weist keinen Rückgabewert auf, da Sie bewirkt, dass die Nachrichten Schleife beendet wird, bevor die Nachricht an die Fenster Prozedur der Anwendung gesendet wird.

## <a name="remarks"></a>Bemerkungen

Die **WM \_** -beendende Nachricht ist keinem Fenster zugeordnet und wird daher nie durch die Fenster Prozedur eines Fensters empfangen. Sie wird nur von den Funktionen [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) oder [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) abgerufen.

Veröffentlichen Sie die **WM- \_** beendende Nachricht nicht mithilfe der [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) -Funktion. verwenden Sie [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage).

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

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
