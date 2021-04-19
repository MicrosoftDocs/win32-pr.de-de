---
title: WM_CHAR Meldung (Winuser. h)
description: Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine WM- \_ KeyDown-Meldung von der translatemess-Funktion übersetzt wird. Die Meldung "WM \_ char" enthält den Zeichencode der Taste, die gedrückt wurde.
ms.assetid: 7e45dc6f-ff68-4534-9e52-46e5f4110532
keywords:
- Tastatur-und Maus Eingaben für WM_CHAR Nachricht
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
ms.openlocfilehash: 8d174f64fa776b506814540d4f2c97635fba38a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354182"
---
# <a name="wm_char-message"></a>WM- \_ char-Nachricht

Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine [**WM- \_ KeyDown**](wm-keydown.md) -Meldung von der [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion übersetzt wird. Die Meldung " **WM \_ char** " enthält den Zeichencode der Taste, die gedrückt wurde.


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

Die Wiederholungs Anzahl, der Überprüfungs Code, das erweiterte schlüsselflag, der Kontext Code, das vorherige schlüsselstatusflag und das Flag für den Übergangszustand, wie in der folgenden Tabelle gezeigt.



| Bits  | Bedeutung                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Die Wiederholungs Anzahl für die aktuelle Nachricht. Der Wert gibt an, wie oft der Tastatur Schlag automatisch durchgeführt wird, wenn der Benutzer die Taste gedrückt hält. Wenn die Tastatureingabe lang genug gehalten wird, werden mehrere Nachrichten gesendet. Die Wiederholungs Anzahl ist jedoch nicht kumulativ. |
| 16-23 | Der Überprüfungs Code. Der Wert hängt vom OEM ab.                                                                                                                                                                                                                          |
| 24    | Gibt an, ob der Schlüssel ein erweiterter Schlüssel ist, z. b. die Rechte ALT-Taste und die STRG-Taste, die auf einer erweiterten 101-oder 102-Tastatur-Tastatur angezeigt werden. Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist der Wert 0.                                                              |
| 25-28 | Bleiben Verwenden Sie nicht.                                                                                                                                                                                                                                                 |
| 29    | Der Kontext Code. Der Wert ist 1, wenn die Alt-Taste gedrückt gehalten wird, während die Taste gedrückt wird. Andernfalls ist der Wert 0.                                                                                                                                                     |
| 30    | Der vorherige Schlüssel Zustand. Der Wert ist 1, wenn der Schlüssel vor dem Senden der Nachricht nicht angezeigt wird, oder wenn der Schlüssel auf "0" festgelegt ist.                                                                                                                                                    |
| 31    | Der Übergangszustand. Der Wert ist 1, wenn der Schlüssel freigegeben wird, oder der Wert ist 0, wenn die Taste gedrückt wird.                                                                                                                                                            |

Weitere Details finden Sie unter [KeyStroke-Nachrichtenflags](about-keyboard-input.md#keystroke-message-flags).
 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

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
Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) auf GitHub.

## <a name="remarks"></a>Bemerkungen

Die Meldung " **WM \_ char** " verwendet UTF (Unicode Transformation Format)-16.

Es gibt nicht notwendigerweise eine eins-zu-eins-Entsprechung zwischen den gedrückten Schlüsseln und den generierten Zeichen Meldungen. Daher sind die Informationen im höherwertigen Wort des *LPARAM* -Parameters für Anwendungen in der Regel nicht nützlich. Die Informationen im höherwertigen Wort gelten nur für die letzte [**WM- \_ KeyDown**](wm-keydown.md) -Nachricht, die vor der Bereitstellung der **WM- \_ char** -Nachricht steht.

Erweiterte Schlüssel für erweiterte 101-und 102-keytastaturen sind die Rechte ALT-Taste und die Rechte STRG-Taste im Hauptabschnitt der Tastatur. die Eingaben "ins", "Entf", "Start", "Ende", "Bild-ab" und "Pfeil" in den Clustern auf der linken Seite der numerischen Tastatur und die Unterteilung (/) und EINGABETASTE in der numerischen Tastatur. Einige andere Tastaturen unterstützen möglicherweise das Extended-Key-Bit im *LPARAM* -Parameter.

Die [**WM \_ UNICHAR**](wm-unichar.md) -Nachricht ist mit **WM \_ char** identisch, mit der Ausnahme, dass Sie UTF-32 verwendet. Er ist darauf ausgelegt, Unicode-Zeichen an ANSI-Fenster zu senden oder bereitzustellen, und er kann Unicode-Zeichen der ergänzenden Ebene verarbeiten.

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM- \_ KeyDown**](wm-keydown.md)
</dt> <dt>

[**WM \_ UNICHAR**](wm-unichar.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastatureingabe](keyboard-input.md)
</dt> </dl>

 

