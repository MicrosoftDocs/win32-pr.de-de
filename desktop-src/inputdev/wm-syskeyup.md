---
title: WM_SYSKEYUP Meldung (Winuser. h)
description: Wird an das Fenster mit dem Tastaturfokus gesendet, wenn der Benutzer eine Taste loslässt, die gedrückt wurde, während die Alt-Taste gedrückt gehalten wurde.
ms.assetid: a4f62575-fb84-4390-a1d1-1a62629de55f
keywords:
- Tastatur-und Maus Eingaben für WM_SYSKEYUP Nachricht
topic_type:
- apiref
api_name:
- WM_SYSKEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2139c11558eccc3fb3b225f0cc1a87bcf6fb084d
ms.sourcegitcommit: cea2889abb43350c38cd120e877d8471dae78beb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352058"
---
# <a name="wm_syskeyup-message"></a>WM- \_ syskeyup-Meldung

Wird an das Fenster mit dem Tastaturfokus gesendet, wenn der Benutzer eine Taste loslässt, die gedrückt wurde, während die Alt-Taste gedrückt gehalten wurde. Es tritt auch auf, wenn derzeit kein Fenster den Tastaturfokus besitzt. in diesem Fall wird die **WM- \_ syskeyup** -Nachricht an das aktive Fenster gesendet. Das Fenster, in dem die Meldung empfangen wird, kann durch Überprüfen des Kontext Codes im *LPARAM* -Parameter zwischen diesen beiden Kontexten unterscheiden.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_SYSKEYUP                     0x0105
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Code für den virtuellen Schlüssel des Schlüssels, der freigegeben wird. Siehe [**virtuelle Schlüssel Codes**](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Die Wiederholungs Anzahl, der Überprüfungs Code, das erweiterte schlüsselflag, der Kontext Code, das vorherige schlüsselstatusflag und das Flag für den Übergangszustand, wie in der folgenden Tabelle gezeigt.



| Bits  | Bedeutung                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Die Wiederholungs Anzahl für die aktuelle Nachricht. Der Wert gibt an, wie oft der Tastatur Schlag automatisch durchgeführt wird, wenn der Benutzer die Taste gedrückt hält. Die Wiederholungs Anzahl ist immer eine für eine **WM- \_ syskeyup** -Nachricht.         |
| 16-23 | Der Überprüfungs Code. Der Wert hängt vom OEM ab.                                                                                                                                                                                  |
| 24    | Gibt an, ob der Schlüssel ein erweiterter Schlüssel ist, z. b. die Rechte ALT-Taste und die STRG-Taste, die auf einer erweiterten 101-oder 102-Tastatur-Tastatur angezeigt werden. Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist der Wert 0 (null).                   |
| 25-28 | Bleiben Verwenden Sie nicht.                                                                                                                                                                                                         |
| 29    | Der Kontext Code. Der Wert ist 1, wenn die Alt-Taste gedrückt ist, während die Taste losgelassen wird. der Wert ist 0 (null), wenn die **WM- \_ syskeyup** -Nachricht im aktiven Fenster gepostet wird, da kein Fenster den Tastaturfokus besitzt. |
| 30    | Der vorherige Schlüssel Zustand. Der Wert für eine **WM- \_ syskeyup** -Nachricht lautet immer 1.                                                                                                                                                 |
| 31    | Der Übergangszustand. Der Wert für eine **WM- \_ syskeyup** -Nachricht lautet immer 1.                                                                                                                                                   |

Weitere Informationen finden Sie unter [KeyStroke-Nachrichtenflags](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion sendet eine [**WM- \_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Meldung an das Fenster der obersten Ebene, wenn die F10-Taste oder die Alt-Taste losgelassen wurde. Der *wParam* -Parameter der Nachricht ist auf **SC \_ keymenu** festgelegt.

Wenn der Kontext Code NULL ist, kann die Nachricht an die [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) -Funktion übermittelt werden, die Sie behandelt, als ob es sich um eine normale Schlüssel Nachricht anstatt um eine Zeichen Schlüssel Nachricht handelt. Dies ermöglicht das Verwenden von Zugriffstasten für das aktive Fenster, auch wenn das aktive Fenster nicht über den Tastaturfokus verfügt.

Für erweiterte 101-und 102-Key-Tastaturen sind erweiterte Schlüssel die Rechte ALT-Taste und die STRG-Taste im Hauptabschnitt der Tastatur. die Tasten "ins", "Entf", "Start", "Ende", "Bild-ab" und "Pfeil" in den Clustern auf der linken Seite der numerischen Keypad. und die Unterteilung (/) und EINGABETASTE in der numerischen Tastatur. Andere Tastaturen unterstützen möglicherweise das Extended-Key-Bit im *LPARAM* -Parameter.

Für nicht-U. S. Erweiterte Tastatur Tastatur mit 102-Taste, die Rechte ALT-Taste wird als STRG + ALT-Taste behandelt. In der folgenden Tabelle wird die Reihenfolge der Nachrichten angezeigt, die sich ergeben, wenn der Benutzer diesen Schlüssel drückt und freigibt.



| `Message`                           | Code des virtuellen Schlüssels |
|-----------------------------------|------------------|
| [**WM- \_ KeyDown**](wm-keydown.md) | **VK- \_ Steuerelement**  |
| [**WM- \_ KeyDown**](wm-keydown.md) | **VK- \_ Menü**     |
| [**WM- \_ KeyUp**](wm-keyup.md)     | **VK- \_ Steuerelement**  |
| **WM- \_ syskeyup**                  | **VK- \_ Menü**     |



 

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

[**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**WM ( \_ syscommand)**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**WM \_ syskeydown**](wm-syskeydown.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastatureingabe](keyboard-input.md)
</dt> </dl>

 

