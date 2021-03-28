---
Description: Die WM- \_ Paint-Meldung wird gesendet, wenn das System oder eine andere Anwendung eine Anforderung zum Zeichnen eines Teils des Fensters einer Anwendung sendet.
ms.assetid: afebaa07-cf00-47db-a919-46436f164881
title: WM_PAINT Meldung (Winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: b13e1779fb54a3db7905cb8fc738ef45558400f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982956"
---
# <a name="wm_paint-message"></a>WM \_ Paint-Meldung

Die **WM- \_ Paint** -Meldung wird gesendet, wenn das System oder eine andere Anwendung eine Anforderung zum Zeichnen eines Teils des Fensters einer Anwendung sendet. Die Nachricht wird gesendet, wenn die Funktion [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) oder [**redrawwindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) aufgerufen wird, oder durch [**die DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) -Funktion, wenn die Anwendung eine WM-Zeichnungs Nachricht mithilfe der [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -Funktion oder der [**Peer-Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) -Funktion erhält. **\_**

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

Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) auf GitHub.

## <a name="remarks"></a>Bemerkungen

Die **WM- \_ Paint** -Meldung wird vom System generiert und sollte nicht von einer Anwendung gesendet werden. Um zu erzwingen, dass ein Fenster in einen bestimmten Gerätekontext gezeichnet wird, verwenden Sie die Meldung [**WM \_ Print**](wm-print.md) oder [**WM \_ printclient**](wm-printclient.md) . Beachten Sie, dass das Zielfenster die WM- **\_ printclient** -Nachricht unterstützen muss. Die meisten gängigen Steuerelemente unterstützen die **WM- \_ printclient** -Nachricht.

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  -Funktion überprüft den Update Bereich. Die Funktion kann die [**WM \_ ncpaint**](wm-ncpaint.md) -Nachricht auch an die Fenster Prozedur senden, wenn der Fensterrahmen gezeichnet werden muss, und die [**WM- \_ erasebkgnd**](../winmsg/wm-erasebkgnd.md) -Nachricht senden, wenn der Fenster Hintergrund gelöscht werden muss.

Das System sendet diese Nachricht, wenn in der Nachrichten Warteschlange der Anwendung keine weiteren Meldungen vorhanden sind. [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) legt fest, wohin die Nachricht gesendet werden soll. [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) bestimmt, welche Nachricht versendet werden soll. **GetMessage** gibt die **WM \_** -Zeichnungs Nachricht zurück, wenn keine weiteren Meldungen in der Nachrichten Warteschlange der Anwendung vorhanden sind, und **DispatchMessage** sendet die Nachricht an die entsprechende Fenster Prozedur.

Ein Fenster empfängt möglicherweise interne Paint-Meldungen als Ergebnis des Aufruf von [**redrawwindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) mit dem \_ festgelegten RDW internalpaint-Flag. In diesem Fall verfügt das Fenster möglicherweise nicht über einen Update Bereich. Eine Anwendung kann die [**getupdatererfunktion**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) aufrufen, um zu bestimmen, ob das Fenster über einen Update Bereich verfügt. Wenn **getupdatdent** NULL zurückgibt, muss die Anwendung die [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) -und [**endpaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) -Funktionen nicht aufrufen.

Eine Anwendung muss überprüfen, ob Sie über die internen Datenstrukturen für jede WM-Zeichnungs Nachricht verfügen, da eine **WM- \_** Zeichnungs Nachricht sowohl von einem Update Bereich ungleich NULL als auch von einem Rückruf von [**redrawwindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) mit dem festgelegten RDW **\_** \_ internalpaint-Flag ausgelöst werden kann.

Das System sendet eine interne **WM \_** -Zeichnungs Nachricht nur einmal. Nachdem eine interne **WM \_** -Zeichnungs Meldung von [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) oder [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) zurückgegeben oder an ein Fenster durch [**Update Window**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)gesendet wurde, sendet oder sendet das System keine weiteren **WM \_ Paint** -Meldungen, bis das Fenster ungültig gemacht wird, oder bis [**redrawwindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) erneut aufgerufen wird, wenn das RDW \_ internalpaint-Flag festgelegt ist.

Bei einigen allgemeinen Steuerelementen überprüft die standardmäßige **WM \_ Paint** -Nachrichtenverarbeitung den *wParam* -Parameter. Wenn *wParam* ungleich NULL ist, geht das Steuerelement davon aus, dass es sich bei dem Wert um einen HDC handelt und zeichnet sich mit diesem Gerätekontext aus.

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

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**DispatchMessage gesendet**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)
</dt> <dt>

[**Endpaint auf**](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**Getupdaterierten**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**Redrawwindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> <dt>

[**Update Window**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)
</dt> <dt>

[**WM- \_ erasebkgnd**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**WM- \_ ncpaint**](wm-ncpaint.md)
</dt> <dt>

[**WM- \_ Druck**](wm-print.md)
</dt> <dt>

[**WM- \_ printclient**](wm-printclient.md)
</dt> </dl>

 

 
