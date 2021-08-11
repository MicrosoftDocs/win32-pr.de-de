---
title: WM_CHAR (Winuser.h)
description: Wird im Fenster mit dem Tastaturfokus veröffentlicht, wenn eine WM \_ KEYDOWN-Nachricht von der TranslateMessage-Funktion übersetzt wird. Die WM \_ CHAR-Meldung enthält den Zeichencode der gedrückten Taste.
ms.assetid: 7e45dc6f-ff68-4534-9e52-46e5f4110532
keywords:
- WM_CHAR der Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_CHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/28/2020
ms.openlocfilehash: 16f9f1160f9766bd6284f62f2203b940ab6336f326aa31a0d9fa2894d243cf59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247949"
---
# <a name="wm_char-message"></a>WM \_ CHAR-Meldung

Wird im Fenster mit dem Tastaturfokus veröffentlicht, wenn eine [**WM \_ KEYDOWN-Nachricht**](wm-keydown.md) von der [**TranslateMessage-Funktion übersetzt**](/windows/desktop/api/winuser/nf-winuser-translatemessage) wird. Die **WM \_ CHAR-Meldung** enthält den Zeichencode der gedrückten Taste.


```C++
#define WM_CHAR                         0x0102
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Zeichencode des Schlüssels.

</dd> <dt>

*lParam* 
</dt> <dd>

Anzahl der Wiederholungen, Überprüfungscode, Flag für erweiterte Schlüssel, Kontextcode, vorheriges Schlüsselzustandsflag und Übergangszustandsflag, wie in der folgenden Tabelle dargestellt.



| Bits  | Bedeutung                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Die Wiederholungsanzahl für die aktuelle Nachricht. Der Wert gibt an, wie oft die Tastatureingabe automatisch angezeigt wird, wenn der Benutzer den Schlüssel hält. Wenn die Tastatureingabe lange genug gehalten wird, werden mehrere Nachrichten gesendet. Die Wiederholungsanzahl ist jedoch nicht kumulativ. |
| 16-23 | Der Scancode. Der Wert hängt vom OEM ab.                                                                                                                                                                                                                          |
| 24    | Gibt an, ob es sich bei der Taste um eine erweiterte Taste handelt, z. B. die rechte ALT- und STRG-Taste, die auf einer erweiterten Tastatur mit 101 oder 102 Tasten angezeigt werden. Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. andernfalls ist es 0.                                                              |
| 25-28 | Reserviert; nicht verwenden.                                                                                                                                                                                                                                                 |
| 29    | Der Kontextcode. Der Wert ist 1, wenn die ALT-TASTE gedrückt gehalten wird, während die Taste gedrückt wird. andernfalls ist der Wert 0.                                                                                                                                                     |
| 30    | Der vorherige Schlüsselzustand. Der Wert ist 1, wenn der Schlüssel vor dem Senden der Nachricht heruntergefahren ist, oder 0, wenn der Schlüssel hoch ist.                                                                                                                                                    |
| 31    | Der Übergangszustand. Der Wert ist 1, wenn die Taste freigegeben wird, oder 0, wenn die Taste gedrückt wird.                                                                                                                                                            |

Weitere Informationen finden Sie unter [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).
 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="example"></a>Beispiel

```cpp
LRESULT CALLBACK WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
   
    // ...

    case WM_CHAR:
        OnKeyPress(wParam);
        break;

    default:
        return DefWindowProc(hwnd, message, wParam, lParam);
    }
    return 0;
}
```
Beispiel aus [Windows klassischen Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) auf GitHub.

## <a name="remarks"></a>Hinweise

Die **WM \_ CHAR-Nachricht** verwendet das Unicode Transformation Format (UTF)-16.

Es gibt nicht notwendigerweise eine 1:1-Entsprechung zwischen gedrückten Tasten und generierten Zeichenmeldungen, sodass die Informationen im hohen Wort des *lParam-Parameters* in der Regel für Anwendungen nicht nützlich sind. Die Informationen im hoch geordneten Wort gelten nur für die letzte [**WM \_ KEYDOWN-Nachricht,**](wm-keydown.md) die der Veröffentlichung der **WM \_ CHAR-Nachricht vorausgegangen** ist.

Für erweiterte Tastaturen mit 101 und 102 Tasten sind erweiterte Tasten die rechte ALT-Taste und die rechte STRG-Taste im Hauptteil der Tastatur. DIE TASTEN INS, DEL, HOME, END, PAGE UP, PAGE DOWN und die Pfeiltasten in den Clustern links neben der numerischen Tastatur; und die Division (/) und die EINGABETASTEn in der numerischen Tastatur. Einige andere Tastaturen unterstützen möglicherweise das Bit mit erweiterter Taste im *lParam-Parameter.*

Die [**WM \_ UNICHAR-Nachricht**](wm-unichar.md) ist identisch mit **WM \_ CHAR,** mit der Ausnahme, dass UTF-32 verwendet wird. Sie ist für das Senden oder Posten von Unicode-Zeichen an ANSI-Fenster konzipiert und kann Zeichen der ergänzenden Unicode-Ebene verarbeiten.

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ KEYDOWN**](wm-keydown.md)
</dt> <dt>

[**WM \_ UNICHAR**](wm-unichar.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastatureingaben](keyboard-input.md)
</dt> </dl>

 

