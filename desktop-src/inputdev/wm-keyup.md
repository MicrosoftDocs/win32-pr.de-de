---
title: WM_KEYUP Meldung (Winuser. h)
description: Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine nicht-System Taste losgelassen wird. Eine nicht-System Taste ist ein Schlüssel, der gedrückt wird, wenn die Alt-Taste nicht gedrückt wird, oder eine Tastatur Taste, die gedrückt wird, wenn ein Fenster den Tastaturfokus besitzt.
ms.assetid: 67d9d82d-fab0-4aec-a337-7a9cb2b0b586
keywords:
- Tastatur-und Maus Eingaben für WM_KEYUP Nachricht
topic_type:
- apiref
api_name:
- WM_KEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28aa02dd73f1706bb12ae30825f50241be7bb0d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391792"
---
# <a name="wm_keyup-message"></a>WM- \_ keyupmeldung

Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine nicht-System Taste losgelassen wird. Eine nicht-System Taste ist ein Schlüssel, der gedrückt wird, wenn die Alt-Taste *nicht* gedrückt wird, oder eine Tastatur Taste, die gedrückt wird, wenn ein Fenster den Tastaturfokus besitzt.


```C++
#define WM_KEYUP                        0x0101
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Code des virtuellen Schlüssels des nicht System Schlüssels. Siehe [virtuelle Schlüssel Codes](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Die Wiederholungs Anzahl, der Überprüfungs Code, das erweiterte schlüsselflag, der Kontext Code, das vorherige schlüsselstatusflag und das Flag für den Übergangszustand, wie in der folgenden Tabelle gezeigt.



| Bits  | Bedeutung                                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Die Wiederholungs Anzahl für die aktuelle Nachricht. Der Wert gibt an, wie oft der Tastatur Schlag automatisch durchgeführt wird, wenn der Benutzer die Taste gedrückt hält. Die Wiederholungs Anzahl ist für eine WM- **\_ KeyUp** -Meldung immer 1. |
| 16-23 | Der Überprüfungs Code. Der Wert hängt vom OEM ab.                                                                                                                                                                     |
| 24    | Gibt an, ob der Schlüssel ein erweiterter Schlüssel ist, z. b. die Rechte ALT-Taste und die STRG-Taste, die auf einer erweiterten 101-oder 102-Tastatur-Tastatur angezeigt werden. Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist der Wert 0.         |
| 25-28 | Bleiben Verwenden Sie nicht.                                                                                                                                                                                            |
| 29    | Der Kontext Code. Der Wert für eine **WM- \_ KeyUp** -Nachricht ist immer 0.                                                                                                                                             |
| 30    | Der vorherige Schlüssel Zustand. Der Wert ist für eine WM- **\_ KeyUp** -Meldung immer 1.                                                                                                                                       |
| 31    | Der Übergangszustand. Der Wert ist für eine WM- **\_ KeyUp** -Meldung immer 1.                                                                                                                                         |

Weitere Details finden Sie unter [KeyStroke-Nachrichtenflags](about-keyboard-input.md#keystroke-message-flags).
 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion sendet eine [**WM- \_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Meldung an das Fenster der obersten Ebene, wenn die F10-Taste oder die Alt-Taste losgelassen wurde. Der *wParam* -Parameter der Nachricht ist auf SC \_ keymenu festgelegt.

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

[**WM- \_ KeyDown**](wm-keydown.md)
</dt> <dt>

[**WM ( \_ syscommand)**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastatureingabe](keyboard-input.md)
</dt> </dl>

 

