---
description: Führt keinen Vorgang aus. Eine Anwendung sendet die WM NULL-Nachricht, wenn sie eine Nachricht veröffentlichen \_ möchte, die das Empfängerfenster ignoriert.
ms.assetid: edbcfba6-7b79-4d53-84e3-2e4227e17369
title: WM_NULL (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9ade89ee83a7d0d0b9d012248da729facbd07d269387a86cd4dfac873b76be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199946"
---
# <a name="wm_null-message"></a>WM \_ NULL-Nachricht

Führt keinen Vorgang aus. Eine Anwendung sendet die **WM \_ NULL-Nachricht,** wenn sie eine Nachricht veröffentlichen möchte, die das Empfängerfenster ignoriert.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NULL                         0x0000
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Eine Anwendung gibt 0 (null) zurück, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Hinweise

Wenn eine Anwendung beispielsweise einen **WH \_ GETMESSAGE-Hook** installiert hat und verhindern möchte, dass eine Nachricht verarbeitet wird, kann die [**GetMsgProc-Rückruffunktion**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) die Nachrichtennummer in **WM \_ NULL** ändern, damit der Empfänger sie ignoriert.

Als weiteres Beispiel kann eine Anwendung überprüfen, ob ein Fenster auf Nachrichten reagiert, indem die **WM \_ NULL-Nachricht** mit der [**SendMessageTimeout-Funktion gesendet**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Windows Übersicht](windows.md)
</dt> </dl>

 

 
