---
Description: Die WM \_ PAINT-Nachricht wird gesendet, wenn das System oder eine andere Anwendung eine Anforderung zum Zeichnen eines Teils des Fensters einer Anwendung sendet.
ms.assetid: afebaa07-cf00-47db-a919-46436f164881
title: WM_PAINT Meldung (Winuser.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: b5efec4bc92fcb3c90a8def59b2e85d98342cf641dfe959fc2a651f81ffc1f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092510"
---
# <a name="wm_paint-message"></a>WM \_ PAINT-Meldung

Die **WM \_ PAINT-Nachricht** wird gesendet, wenn das System oder eine andere Anwendung eine Anforderung zum Zeichnen eines Teils des Fensters einer Anwendung sendet. Die Nachricht wird gesendet, wenn die [**UpdateWindow-**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) oder [**RedrawWindow-Funktion**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) aufgerufen wird, oder von der [**DispatchMessage-Funktion,**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) wenn die Anwendung eine **WM \_ PAINT-Nachricht** mithilfe der [**GetMessage-**](/windows/win32/api/winuser/nf-winuser-getmessage) oder [**PeekMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-peekmessagea) erhält.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Eine Anwendung gibt 0 (null) zurück, wenn sie diese Nachricht verarbeitet.

## <a name="example"></a>Beispiel

```c
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);

            // All painting occurs here, between BeginPaint and EndPaint.
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(hwnd, &ps);
        }
        return 0;
    }

    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}

```

Beispiel aus [Windows klassischen Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) auf GitHub.

## <a name="remarks"></a>Hinweise

Die **WM \_ PAINT-Nachricht** wird vom System generiert und sollte nicht von einer Anwendung gesendet werden. Um zu erzwingen, dass ein Fenster in einen bestimmten Gerätekontext gezeichnet wird, verwenden Sie die [**WM \_ PRINT-**](wm-print.md) oder [**WM \_ PRINTCLIENT-Nachricht.**](wm-printclient.md) Beachten Sie, dass dies erfordert, dass das Zielfenster die **WM \_ PRINTCLIENT-Nachricht** unterstützt. Die gängigsten Steuerelemente unterstützen die **WM \_ PRINTCLIENT-Nachricht.**

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  überprüft die Updateregion. Die Funktion kann auch die [**WM \_ NCPAINT-Nachricht**](wm-ncpaint.md) an die Fensterprozedur senden, wenn der Fensterrahmen gezeichnet werden muss, und die [**WM \_ ERASEBKGND-Nachricht**](../winmsg/wm-erasebkgnd.md) senden, wenn der Fensterhintergrund gelöscht werden muss.

Das System sendet diese Nachricht, wenn keine anderen Nachrichten in der Nachrichtenwarteschlange der Anwendung vorhanden sind. [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) bestimmt, wohin die Nachricht gesendet werden soll. [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) bestimmt, welche Nachricht gesendet werden soll. **GetMessage** gibt die **WM \_ PAINT-Nachricht** zurück, wenn keine anderen Nachrichten in der Nachrichtenwarteschlange der Anwendung vorhanden sind und **DispatchMessage** die Nachricht an die entsprechende Fensterprozedur sendet.

Ein Fenster empfängt möglicherweise interne Paint-Meldungen als Ergebnis des Aufrufs von [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) mit festgelegtem RDW \_ INTERNALPAINT-Flag. In diesem Fall hat das Fenster möglicherweise keinen Updatebereich. Eine Anwendung kann die [**GetUpdateRect-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) aufrufen, um zu bestimmen, ob das Fenster über einen Updatebereich verfügt. Wenn **GetUpdateRect** 0 (null) zurückgibt, muss die Anwendung die Funktionen [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) und [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) nicht aufrufen.

Eine Anwendung muss alle erforderlichen internen Zeichnungen überprüfen, indem sie ihre internen Datenstrukturen für jede **WM \_ PAINT-Nachricht** untersucht, da eine **WM \_ PAINT-Nachricht** möglicherweise sowohl durch einen Nicht-NULL-Updatebereich als auch durch einen Aufruf von [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) mit festgelegtem RDW \_ INTERNALPAINT-Flag verursacht wurde.

Das System sendet nur einmal eine interne **WM \_ PAINT-Nachricht.** Nachdem eine interne **WM \_ PAINT-Nachricht** von [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) oder [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) zurückgegeben oder von [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)an ein Fenster gesendet wurde, sendet das System keine weiteren **WM \_ PAINT-Meldungen,** bis das Fenster ungültig wird oder [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) erneut aufgerufen wird und das RDW \_ INTERNALPAINT-Flag festgelegt ist.

Bei einigen gängigen Steuerelementen überprüft die **standardmäßige WM \_ PAINT-Nachrichtenverarbeitung** den *wParam-Parameter.* Wenn *wParam* ungleich NULL ist, geht das Steuerelement davon aus, dass der Wert ein HDC ist und zeichnet mit diesem Gerätekontext.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über Zeichnen und Zeichnen](painting-and-drawing.md)
</dt> <dt>

[Zeichnen und Zeichnen von Nachrichten](painting-and-drawing-messages.md)
</dt> <dt>

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)
</dt> <dt>

[**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> <dt>

[**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)
</dt> <dt>

[**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**WM \_ NCPAINT**](wm-ncpaint.md)
</dt> <dt>

[**WM \_ PRINT**](wm-print.md)
</dt> <dt>

[**WM \_ PRINTCLIENT**](wm-printclient.md)
</dt> </dl>

 

 
