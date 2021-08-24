---
title: WM_KEYDOWN Meldung (Winuser.h)
description: Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine Nichtsystemtaste gedrückt wird. Eine Nichtsystemtaste ist eine Taste, die gedrückt wird, wenn die ALT-TASTE nicht gedrückt wird.
ms.assetid: 0e37149f-445c-4b20-ad68-fdf39428ac91
keywords:
- WM_KEYDOWN Meldung Tastatur- und Mauseingabe
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
ms.openlocfilehash: 9f54d0cad58a378d12247127d1ed70ab48653e18f4cceeb3c801efcf2aaae66d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717200"
---
# <a name="wm_keydown-message"></a>WM \_ KEYDOWN-Nachricht

Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine Nichtsystemtaste gedrückt wird. Eine Nichtsystemtaste ist eine Taste, die gedrückt wird, wenn die ALT-TASTE nicht gedrückt wird.


```C++
#define WM_KEYDOWN                      0x0100
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Virtuelle Schlüsselcode des Nichtsystemschlüssels. Weitere Informationen finden Sie unter [Codes für virtuelle Schlüssel.](virtual-key-codes.md)

</dd> <dt>

*lParam* 
</dt> <dd>

Wiederholungsanzahl, Scancode, Flag für erweiterte Schlüssel, Kontextcode, vorheriges Schlüsselzustandsflag und Übergangszustandsflag, wie unten dargestellt.



| Bits  | Bedeutung                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Die Wiederholungsanzahl für die aktuelle Nachricht. Der Wert gibt an, wie oft die Tastatureingabe automatisch erfolgt, weil der Benutzer den Schlüssel gedrückt hält. Wenn die Tastatureingabe lange genug gehalten wird, werden mehrere Nachrichten gesendet. Die Wiederholungsanzahl ist jedoch nicht kumulativ. |
| 16-23 | Der Scancode. Der Wert hängt vom OEM ab.                                                                                                                                                                                                                          |
| 24    | Gibt an, ob es sich bei der Taste um eine erweiterte Taste handelt, z. B. die rechte ALT- und STRG-Taste, die auf einer erweiterten Tastatur mit 101 oder 102 Tasten angezeigt wird. Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist es 0.                                                              |
| 25-28 | Reserviert; nicht verwenden.                                                                                                                                                                                                                                                 |
| 29    | Der Kontextcode. Der Wert ist immer 0 für eine **WM \_ KEYDOWN-Nachricht.**                                                                                                                                                                                                |
| 30    | Der vorherige Schlüsselzustand. Der Wert ist 1, wenn der Schlüssel ausgeschaltet ist, bevor die Nachricht gesendet wird, oder 0 (null), wenn der Schlüssel hoch ist.                                                                                                                                                 |
| 31    | Der Übergangszustand. Der Wert ist immer 0 für eine **WM \_ KEYDOWN-Nachricht.**                                                                                                                                                                                            |

Weitere Informationen finden Sie unter [Tastatureingabe-Meldungsflags.](about-keyboard-input.md#keystroke-message-flags)
 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

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

Beispiel aus [Windows klassischen Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) auf GitHub.


## <a name="remarks"></a>Hinweise

Wenn die F10-Taste gedrückt wird, legt die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ein internes Flag fest. Wenn **DefWindowProc** die [**WM \_ KEYUP-Nachricht**](wm-keyup.md) empfängt, überprüft die Funktion, ob das interne Flag festgelegt ist, und sendet, falls ja, eine [**\_ WM-SYSCOMMAND-Nachricht**](/windows/desktop/menurc/wm-syscommand) an das Fenster der obersten Ebene. Der **WM \_ SYSCOMMAND-Parameter** der Nachricht ist auf SC \_ KEYMENU festgelegt.

Aufgrund der Funktion autorepeat können mehrere **WM \_ KEYDOWN-Nachrichten** veröffentlicht werden, bevor eine [**WM \_ KEYUP-Nachricht**](wm-keyup.md) veröffentlicht wird. Der vorherige Schlüsselzustand (Bit 30) kann verwendet werden, um zu bestimmen, ob die **WM \_ KEYDOWN-Meldung** den ersten Abwärtsübergang oder einen wiederholten Abwärtsübergang angibt.

Bei erweiterten Tastaturen mit 101 und 102 Tasten sind erweiterte Tasten die rechten ALT- und STRG-Tasten im Hauptbereich der Tastatur. die INS-, DEL-, HOME-, END-, PAGE UP-, PAGE DOWN- und PFEILTASTEn in den Clustern links neben der numerischen Tastatur; und die Trenntaste (/) und die EINGABETASTE in der numerischen Tastatur. Andere Tastaturen unterstützen möglicherweise das erweiterte Tastenbit im *lParam-Parameter.*

Anwendungen müssen *wParam* an [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) übergeben, ohne es zu ändern.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ CHAR**](wm-char.md)
</dt> <dt>

[**WM \_ KEYUP**](wm-keyup.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastatureingaben](keyboard-input.md)
</dt> </dl>

 

