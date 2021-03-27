---
description: Die WM \_ syncpaint-Meldung wird zum Synchronisieren der Zeichnung verwendet, während Verknüpfungen unabhängiger GUI-Threads vermieden werden.
ms.assetid: 4446be4e-e0b9-46ce-95b2-bea876348c25
title: WM_SYNCPAINT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5602e867af9b7ce467e8979c9f341758414ad287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994550"
---
# <a name="wm_syncpaint-message"></a>WM \_ syncpaint-Meldung

Die **WM \_ syncpaint** -Meldung wird zum Synchronisieren der Zeichnung verwendet, während Verknüpfungen unabhängiger GUI-Threads vermieden werden.

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

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung gibt 0 (null) zurück, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Wenn ein Fenster ausgeblendet, angezeigt, verschoben oder vergrößert wurde, kann das System feststellen, dass es erforderlich ist, eine **WM \_ syncpaint** -Meldung an die Fenster der obersten Ebene anderer Threads zu senden. Anwendungen müssen für die Verarbeitung **WM \_ syncpaint** an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  übergeben. Die **defwindowproc** -Funktion sendet eine [**WM \_ ncpaint**](wm-ncpaint.md) -Meldung an die Fenster Prozedur, wenn der Fensterrahmen gezeichnet werden muss, und sendet eine [**WM \_ erasebkgnd**](../winmsg/wm-erasebkgnd.md) -Meldung, wenn der Fenster Hintergrund gelöscht werden muss.

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

[**Getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> <dt>

[**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[**WM- \_ Paint**](wm-paint.md)
</dt> </dl>

 

 
