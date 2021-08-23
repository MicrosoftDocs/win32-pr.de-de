---
title: WM_SYSKEYDOWN Meldung (Winuser.h)
description: Wird mit dem Tastaturfokus an das Fenster gesendet, wenn der Benutzer die F10-Taste drückt (wodurch die Menüleiste aktiviert wird), oder die ALT-TASTE gedrückt hält und dann eine andere Taste drückt.
ms.assetid: a3c03dbf-1be7-49ff-b931-1981786b74ce
keywords:
- WM_SYSKEYDOWN Meldung Tastatur- und Mauseingabe
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
ms.openlocfilehash: 30b1398d843711e868a6b5b96cf6a66893bf74fef1e50bfdd61fa36f81f05c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611320"
---
# <a name="wm_syskeydown-message"></a>WM \_ SYSKEYDOWN-Meldung

Wird mit dem Tastaturfokus an das Fenster gesendet, wenn der Benutzer die F10-Taste drückt (wodurch die Menüleiste aktiviert wird), oder die ALT-TASTE gedrückt hält und dann eine andere Taste drückt. Sie tritt auch auf, wenn derzeit kein Fenster über den Tastaturfokus verfügt. In diesem Fall wird die **WM \_ SYSKEYDOWN-Nachricht** an das aktive Fenster gesendet. Das Fenster, das die Nachricht empfängt, kann zwischen diesen beiden Kontexten unterscheiden, indem der Kontextcode im *lParam-Parameter* überprüft wird.


```C++
#define WM_SYSKEYDOWN                   0x0104
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Virtuelle Schlüsselcode der Taste, die gedrückt wird. Weitere Informationen finden Sie unter [**Codes für virtuelle Schlüssel.**](virtual-key-codes.md)

</dd> <dt>

*lParam* 
</dt> <dd>

Wiederholungsanzahl, Scancode, Flag für erweiterte Schlüssel, Kontextcode, vorheriges Schlüsselzustandsflag und Übergangszustandsflag, wie in der folgenden Tabelle dargestellt.



| Bits  | Bedeutung                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Die Wiederholungsanzahl für die aktuelle Nachricht. Der Wert gibt an, wie oft die Tastatureingabe automatisch erfolgt, weil der Benutzer den Schlüssel gedrückt hält. Wenn die Tastatureingabe lange genug gehalten wird, werden mehrere Nachrichten gesendet. Die Wiederholungsanzahl ist jedoch nicht kumulativ. |
| 16-23 | Der Scancode. Der Wert hängt vom OEM ab.                                                                                                                                                                                                                          |
| 24    | Gibt an, ob es sich bei der Taste um eine erweiterte Taste handelt, z. B. die rechte ALT- und STRG-Taste, die auf einer erweiterten Tastatur mit 101 oder 102 Tasten angezeigt wird. Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist es 0.                                                              |
| 25-28 | Reserviert; nicht verwenden.                                                                                                                                                                                                                                                 |
| 29    | Der Kontextcode. Der Wert ist 1, wenn die ALT-Taste gedrückt ist, während die Taste gedrückt wird. ist 0, wenn die **WM \_ SYSKEYDOWN-Meldung** an das aktive Fenster gesendet wird, da kein Fenster den Tastaturfokus besitzt.                                                                  |
| 30    | Der vorherige Schlüsselzustand. Der Wert ist 1, wenn der Schlüssel ausgeschaltet ist, bevor die Nachricht gesendet wird, oder 0, wenn der Schlüssel hoch ist.                                                                                                                                                    |
| 31    | Der Übergangszustand. Der Wert ist immer 0 für eine **WM \_ SYSKEYDOWN-Nachricht.**                                                                                                                                                                                         |

Weitere Informationen finden Sie unter [Tastatureingabe-Meldungsflags.](about-keyboard-input.md#keystroke-message-flags)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Hinweise

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) untersucht den angegebenen Schlüssel und generiert eine [**\_ WM-SYSCOMMAND-Meldung,**](/windows/desktop/menurc/wm-syscommand) wenn der Schlüssel entweder TAB oder DIE EINGABETASTE ist.

Wenn der Kontextcode 0 (null) ist, kann die Nachricht an die [**TranslateAccelerator-Funktion**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) übergeben werden, die sie so behandelt, als wäre es eine normale Schlüsselnachricht anstelle einer Zeichenschlüsselnachricht. Dadurch können Zugriffstasten mit dem aktiven Fenster verwendet werden, auch wenn das aktive Fenster nicht über den Tastaturfokus verfügt.

Aufgrund der automatischen Wiederholung können mehrere **WM \_ SYSKEYDOWN-Meldungen** auftreten, bevor eine [**WM \_ SYSKEYUP-Nachricht**](wm-syskeyup.md) gesendet wird. Der vorherige Schlüsselzustand (Bit 30) kann verwendet werden, um zu bestimmen, ob die **WM \_ SYSKEYDOWN-Meldung** den ersten Übergang nach unten oder einen wiederholten Abwärtsübergang angibt.

Bei erweiterten Tastaturen mit 101 und 102 Tasten sind erweiterte Tasten die rechten ALT- und STRG-Tasten im Hauptbereich der Tastatur. die INS-, DEL-, HOME-, END-, PAGE UP-, PAGE DOWN- und PFEILTASTEn in den Clustern links neben der numerischen Tastatur; und die Trenntaste (/) und die EINGABETASTE in der numerischen Tastatur. Andere Tastaturen unterstützen möglicherweise das erweiterte Tastenbit im *lParam-Parameter.*

Diese Meldung wird auch gesendet, wenn der Benutzer die TASTE F10 ohne ALT drückt.

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

[**Translateaccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**WM \_ SYSKEYUP**](wm-syskeyup.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastatureingaben](keyboard-input.md)
</dt> </dl>

 

