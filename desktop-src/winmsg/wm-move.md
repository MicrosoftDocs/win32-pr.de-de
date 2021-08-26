---
description: Wird gesendet, nachdem ein Fenster verschoben wurde.
ms.assetid: 552ddc26-fe63-449b-8c82-bb927a2c1c41
title: WM_MOVE (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84c18d7a4f4411f45a3338a057a60942d01905ccefd25b40ee511d3b8a5d915d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810470"
---
# <a name="wm_move-message"></a>WM \_ MOVE-Nachricht

Wird gesendet, nachdem ein Fenster verschoben wurde.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/windows/win32/api/winuser/nf-winuser-defwindowproca)


```C++
#define WM_MOVE                         0x0003
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Die x- und y-Koordinaten der oberen linken Ecke des Clientbereichs des Fensters. Das niedrige Wort enthält die x-Koordinate, während das obere Wort die y-Koordinate enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Die Parameter werden in Bildschirmkoordinaten für überlappende und Popupfenster und in übergeordneten Clientkoordinaten für untergeordnete Fenster angegeben.

Im folgenden Beispiel wird veranschaulicht, wie sie die Position aus dem *lParam-Parameter* abrufen.


```
xPos = (int)(short) LOWORD(lParam);   // horizontal position 
yPos = (int)(short) HIWORD(lParam);   // vertical position 
```



Sie können auch das [**MAKEPOINTS-Makro verwenden,**](/windows/win32/api/wingdi/nf-wingdi-makepoints) um den *lParam-Parameter* in eine [**POINTS-Struktur zu**](/previous-versions//dd162808(v=vs.85)) konvertieren.

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sendet die **NACHRICHTEN WM \_ SIZE** und **WM \_ MOVE,** wenn sie die [**WM \_ WINDOWPOSCHANGED-Nachricht**](wm-windowposchanged.md) verarbeitet.
Die **NACHRICHTEN WM \_ SIZE** und **WM \_ MOVE** werden nicht gesendet, wenn eine Anwendung die **WM \_ WINDOWPOSCHANGED-Nachricht** ohne Aufruf von **DefWindowProc verarbeitet.**

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_WM-FENSTERPOSCHANGED**](wm-windowposchanged.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Punkte**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

 
