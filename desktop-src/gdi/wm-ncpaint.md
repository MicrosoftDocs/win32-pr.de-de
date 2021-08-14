---
description: Die WM \_ NCPAINT-Nachricht wird an ein Fenster gesendet, wenn der Rahmen gestrichen werden muss.
ms.assetid: d8a2a8b9-2c5d-484c-be09-67eb33de67c0
title: WM_NCPAINT (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6be5fa951d50dbaf8663e34a5d9476ecb62576c203095bed9427dcef44425690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978000"
---
# <a name="wm_ncpaint-message"></a>WM \_ NCPAINT-Meldung

Die **WM \_ NCPAINT-Nachricht** wird an ein Fenster gesendet, wenn der Rahmen gestrichen werden muss.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Ein Handle für den Updatebereich des Fensters. Der Updatebereich wird an den Fensterrahmen abgeschnitten.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung gibt 0 (null) zurück, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Hinweise

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) zeichnet den Fensterrahmen.

Eine Anwendung kann die **WM \_ NCPAINT-Nachricht** abfangen und ihren eigenen benutzerdefinierten Fensterrahmen zeichnen. Der Ausschneidebereich für ein Fenster ist immer rechteckig, auch wenn die Form des Rahmens geändert wird.

Der *wParam-Wert* kann wie im folgenden Beispiel [**an GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) übergeben werden.


```C++
case WM_NCPAINT:
{
    HDC hdc;
    hdc = GetDCEx(hwnd, (HRGN)wParam, DCX_WINDOW|DCX_INTERSECTRGN);
    // Paint into this DC 
    ReleaseDC(hwnd, hdc);
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Das Zeichnen und Zeichnen](painting-and-drawing.md)
</dt> <dt>

[Zeichnen und Zeichnen von Nachrichten](painting-and-drawing-messages.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[**WM \_ PAINT**](wm-paint.md)
</dt> <dt>

[**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> </dl>

 

 
