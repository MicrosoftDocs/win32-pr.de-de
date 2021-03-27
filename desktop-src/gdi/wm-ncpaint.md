---
description: Die WM- \_ ncpaint-Meldung wird an ein Fenster gesendet, wenn Ihr Frame gezeichnet werden muss.
ms.assetid: d8a2a8b9-2c5d-484c-be09-67eb33de67c0
title: WM_NCPAINT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6c2e211f3dc1602821b0197d295f940606c262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864316"
---
# <a name="wm_ncpaint-message"></a>WM- \_ ncpaint-Meldung

Die **WM- \_ ncpaint** -Meldung wird an ein Fenster gesendet, wenn Ihr Frame gezeichnet werden muss.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für den Aktualisierungs Bereich des Fensters. Der Aktualisierungs Bereich wird auf den Fensterrahmen zugeschnitten.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung gibt 0 (null) zurück, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion zeichnet den Fensterrahmen.

Eine Anwendung kann die **WM- \_ ncpaint** -Nachricht abfangen und ihren eigenen benutzerdefinierten Fensterrahmen zeichnen. Der Clippingbereich für ein Fenster ist immer rechteckig, auch wenn die Form des Frames geändert wird.

Der *wParam* -Wert kann wie im folgenden Beispiel an [**getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex) übermittelt werden.


```C++
case WM_NCPAINT:
{
    HDC hdc;
    hdc = GetDCEx(hwnd, (HRGN)wParam, DCX_WINDOW|DCX_INTERSECTRGN);
    // Paint into this DC 
    ReleaseDC(hwnd, hdc);
}
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über das Zeichnen und zeichnen](painting-and-drawing.md)
</dt> <dt>

[Zeichnen und Zeichnen von Nachrichten](painting-and-drawing-messages.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[**WM- \_ Paint**](wm-paint.md)
</dt> <dt>

[**Getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> </dl>

 

 
