---
title: WM_SYSKEYDOWN Meldung (Winuser. h)
description: Wird an das Fenster mit dem Tastaturfokus gesendet, wenn der Benutzer die Taste F10 drückt (wodurch die Menüleiste aktiviert wird) oder die Alt-Taste gedrückt hält und dann eine andere Taste drückt.
ms.assetid: a3c03dbf-1be7-49ff-b931-1981786b74ce
keywords:
- Tastatur-und Maus Eingaben für WM_SYSKEYDOWN Nachricht
topic_type:
- apiref
api_name:
- WM_SYSKEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3053c5933a0388e3c8522b0d7201b491aaa4fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341389"
---
# <a name="wm_syskeydown-message"></a>WM- \_ syskeydown-Meldung

Wird an das Fenster mit dem Tastaturfokus gesendet, wenn der Benutzer die Taste F10 drückt (wodurch die Menüleiste aktiviert wird) oder die Alt-Taste gedrückt hält und dann eine andere Taste drückt. Es tritt auch auf, wenn derzeit kein Fenster den Tastaturfokus besitzt. in diesem Fall wird die **WM- \_ syskeydown** -Nachricht an das aktive Fenster gesendet. Das Fenster, in dem die Meldung empfangen wird, kann durch Überprüfen des Kontext Codes im *LPARAM* -Parameter zwischen diesen beiden Kontexten unterscheiden.


```C++
#define WM_SYSKEYDOWN                   0x0104
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Code für den virtuellen Schlüssel der Taste, die gedrückt wird. Siehe [**virtuelle Schlüssel Codes**](virtual-key-codes.md).

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
| 29    | Der Kontext Code. Der Wert ist 1, wenn die Alt-Taste gedrückt ist, während die Taste gedrückt wird. der Wert ist 0, wenn die **WM- \_ syskeydown** -Nachricht im aktiven Fenster gepostet wird, da kein Fenster den Tastaturfokus besitzt.                                                                  |
| 30    | Der vorherige Schlüssel Zustand. Der Wert ist 1, wenn der Schlüssel vor dem Senden der Nachricht nicht angezeigt wird, oder wenn der Schlüssel auf "0" festgelegt ist.                                                                                                                                                    |
| 31    | Der Übergangszustand. Der Wert für eine **WM- \_ syskeydown** -Nachricht ist immer 0.                                                                                                                                                                                         |

Weitere Details finden Sie unter [KeyStroke-Nachrichtenflags](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion untersucht den angegebenen Schlüssel und generiert eine [**WM- \_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Nachricht, wenn der Schlüssel entweder Tab oder eingegeben ist.

Wenn der Kontext Code NULL ist, kann die Nachricht an die [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) -Funktion übermittelt werden, die Sie behandelt, als ob es sich um eine normale Schlüssel Nachricht anstatt um eine Zeichen Schlüssel Nachricht handelt. Dies ermöglicht das Verwenden von Zugriffstasten für das aktive Fenster, auch wenn das aktive Fenster nicht über den Tastaturfokus verfügt.

Aufgrund der automatischen Wiederholung können mehr als eine **WM- \_ syskeydown** -Meldung auftreten, bevor eine [**WM- \_ syskeyup**](wm-syskeyup.md) -Nachricht gesendet wird. Der vorherige Schlüssel Zustand (Bit 30) kann verwendet werden, um zu bestimmen, ob die **WM- \_ syskeydown** -Meldung den ersten nach-unten-Übergang oder einen wiederholten Down-Übergang angibt.

Für erweiterte 101-und 102-Schlüssel-Tastaturen sind erweiterte Schlüssel die Rechte ALT-Taste und die STRG-Taste im Hauptabschnitt der Tastatur. die Tasten "ins", "Entf", "Start", "Ende", "Bild-ab" und "Pfeil" in den Clustern auf der linken Seite der numerischen Keypad. und die Unterteilung (/) und EINGABETASTE in der numerischen Tastatur. Andere Tastaturen unterstützen möglicherweise das Extended-Key-Bit im *LPARAM* -Parameter.

Diese Meldung wird auch immer dann gesendet, wenn der Benutzer die Taste F10 ohne die Alt-Taste drückt.

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

[**WM- \_ syskeyup**](wm-syskeyup.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastatureingabe](keyboard-input.md)
</dt> </dl>

 

