---
title: WM_KEYDOWN Meldung (Winuser. h)
description: Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine nicht-System Taste gedrückt wird. Eine nicht-System Taste ist ein Schlüssel, der gedrückt wird, wenn die Alt-Taste nicht gedrückt wird.
ms.assetid: 0e37149f-445c-4b20-ad68-fdf39428ac91
keywords:
- Tastatur-und Maus Eingaben für WM_KEYDOWN Nachricht
topic_type:
- apiref
api_name:
- WM_KEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: ee6dc21b4fb90f0d02e80fce8ce6cc17099a0547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359791"
---
# <a name="wm_keydown-message"></a>WM- \_ KeyDown-Meldung

Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine nicht-System Taste gedrückt wird. Eine nicht-System Taste ist ein Schlüssel, der gedrückt wird, wenn die Alt-Taste nicht gedrückt wird.


```C++
#define WM_KEYDOWN                      0x0100
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Code des virtuellen Schlüssels des nicht System Schlüssels. Siehe [virtuelle Schlüssel Codes](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Die Wiederholungs Anzahl, der Überprüfungs Code, das erweiterte schlüsselflag, der Kontext Code, das vorherige schlüsselstatusflag und das Flag für den Übergangszustand, wie im folgenden gezeigt.



| Bits  | Bedeutung                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Die Wiederholungs Anzahl für die aktuelle Nachricht. Der Wert gibt an, wie oft der Tastatur Schlag automatisch durchgeführt wird, wenn der Benutzer die Taste gedrückt hält. Wenn die Tastatureingabe lang genug gehalten wird, werden mehrere Nachrichten gesendet. Die Wiederholungs Anzahl ist jedoch nicht kumulativ. |
| 16-23 | Der Überprüfungs Code. Der Wert hängt vom OEM ab.                                                                                                                                                                                                                          |
| 24    | Gibt an, ob der Schlüssel ein erweiterter Schlüssel ist, z. b. die Rechte ALT-Taste und die STRG-Taste, die auf einer erweiterten 101-oder 102-Tastatur-Tastatur angezeigt werden. Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist der Wert 0.                                                              |
| 25-28 | Bleiben Verwenden Sie nicht.                                                                                                                                                                                                                                                 |
| 29    | Der Kontext Code. Der Wert für eine **WM- \_ KeyDown** -Nachricht ist immer 0.                                                                                                                                                                                                |
| 30    | Der vorherige Schlüssel Zustand. Der Wert ist 1, wenn der Schlüssel vor dem Senden der Nachricht nicht angezeigt wird, oder 0 (null), wenn der Schlüssel auf dem neuesten Stand ist.                                                                                                                                                 |
| 31    | Der Übergangszustand. Der Wert für eine **WM- \_ KeyDown** -Nachricht ist immer 0.                                                                                                                                                                                            |

Weitere Details finden Sie unter [KeyStroke-Nachrichtenflags](about-keyboard-input.md#keystroke-message-flags).
 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="example"></a>Beispiel

```cpp
LRESULT CALLBACK HostWndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message) 
    {
    case WM_KEYDOWN:
        if (wParam == VK_ESCAPE)
        {
            if (isFullScreen) 
            {
                GoPartialScreen();
            }
        }
        break;

    // ...
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;  
}

```

Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) auf GitHub.


## <a name="remarks"></a>Bemerkungen

Wenn die F10-Taste gedrückt wird, legt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion ein internes Flag fest. Wenn **defwindowproc** die [**WM- \_ KeyUp**](wm-keyup.md) -Nachricht empfängt, überprüft die Funktion, ob das interne Flag festgelegt ist, und sendet, wenn dies der Fall ist, eine [**WM- \_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Meldung an das Fenster der obersten Ebene. Der **WM \_ syscommand** -Parameter der Nachricht ist auf SC \_ keymenu festgelegt.

Aufgrund der autoretorf-Funktion werden möglicherweise mehr als eine **WM- \_ KeyDown** -Nachricht gesendet, bevor eine [**WM- \_ KeyUp**](wm-keyup.md) -Nachricht gepostet wird. Der vorherige Schlüssel Zustand (Bit 30) kann verwendet werden, um zu bestimmen, ob die **WM- \_ KeyDown** -Meldung den ersten nach-unten-Übergang oder einen wiederholten Down-Übergang angibt.

Für erweiterte 101-und 102-Key-Tastaturen sind erweiterte Schlüssel die Rechte ALT-Taste und die STRG-Taste im Hauptabschnitt der Tastatur. die Tasten "ins", "Entf", "Start", "Ende", "Bild-ab" und "Pfeil" in den Clustern auf der linken Seite der numerischen Keypad. und die Unterteilung (/) und EINGABETASTE in der numerischen Tastatur. Andere Tastaturen unterstützen möglicherweise das Extended-Key-Bit im *LPARAM* -Parameter.

Anwendungen müssen *wParam* an [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) übergeben, ohne Sie zu ändern.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ -Zeichen**](wm-char.md)
</dt> <dt>

[**WM- \_ KeyUp**](wm-keyup.md)
</dt> <dt>

[**WM ( \_ syscommand)**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastatureingabe](keyboard-input.md)
</dt> </dl>

 

