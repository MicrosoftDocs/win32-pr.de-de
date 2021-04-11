---
description: Führt keinen Vorgang aus. Eine Anwendung sendet die WM- \_ null-Nachricht, wenn Sie eine Nachricht veröffentlichen möchte, die vom Empfänger Fenster ignoriert wird.
ms.assetid: edbcfba6-7b79-4d53-84e3-2e4227e17369
title: WM_NULL Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b445e13200bdeb2947e4d8fd363a1a39f0c86db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216043"
---
# <a name="wm_null-message"></a>WM- \_ null Meldung

Führt keinen Vorgang aus. Eine Anwendung sendet die **WM- \_ null** -Nachricht, wenn Sie eine Nachricht veröffentlichen möchte, die vom Empfänger Fenster ignoriert wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


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

Eine Anwendung gibt 0 (null) zurück, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Wenn eine Anwendung z. b. einen " **WH \_ GetMessage** "-Hook installiert hat und verhindern möchte, dass eine Nachricht verarbeitet wird, kann die [**getmsgproc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) -Rückruffunktion die Nachrichtennummer in **WM \_ null** ändern, sodass der Empfänger Sie ignoriert.

Ein weiteres Beispiel ist, dass eine Anwendung überprüfen kann, ob ein Fenster auf Nachrichten reagiert, indem die **WM- \_ null** -Nachricht mit der [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) -Funktion gesendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über Windows](windows.md)
</dt> </dl>

 

 
