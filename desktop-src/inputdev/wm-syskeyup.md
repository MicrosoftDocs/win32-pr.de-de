---
title: WM_SYSKEYUP-Nachricht (Winuser.h)
description: Wird an das Fenster mit dem Tastaturfokus gesendet, wenn der Benutzer eine Taste freigibt, die gedrückt wurde, während die ALT-TASTE gedrückt wurde.
ms.assetid: a4f62575-fb84-4390-a1d1-1a62629de55f
keywords:
- WM_SYSKEYUP Meldung Tastatur- und Mauseingabe
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
ms.openlocfilehash: 4e35a0267d29e473a3c2e5a6a00a0635a466f46c2917b913c3950aa6567e3cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829860"
---
# <a name="wm_syskeyup-message"></a>WM \_ SYSKEYUP-Meldung

Wird an das Fenster mit dem Tastaturfokus gesendet, wenn der Benutzer eine Taste freigibt, die gedrückt wurde, während die ALT-TASTE gedrückt wurde. Sie tritt auch auf, wenn derzeit kein Fenster über den Tastaturfokus verfügt. In diesem Fall wird die **\_ WM-SYSKEYUP-Nachricht** an das aktive Fenster gesendet. Das Fenster, das die Nachricht empfängt, kann zwischen diesen beiden Kontexten unterscheiden, indem der Kontextcode im *lParam-Parameter* überprüft wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_SYSKEYUP                     0x0105
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Code des virtuellen Schlüssels, der freigegeben wird. Weitere Informationen finden Sie unter [**Codes für virtuelle Schlüssel.**](virtual-key-codes.md)

</dd> <dt>

*lParam* 
</dt> <dd>

Die Wiederholungsanzahl, der Scancode, das Flag für erweiterte Schlüssel, der Kontextcode, das vorherige Schlüsselzustandsflag und das Übergangszustandsflag, wie in der folgenden Tabelle gezeigt.



| Bits  | Bedeutung                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Die Wiederholungsanzahl für die aktuelle Nachricht. Der Wert gibt an, wie oft die Tastatureingabe automatisch erfolgt, weil der Benutzer den Schlüssel gedrückt hält. Die Wiederholungsanzahl ist immer 1 für eine **\_ WM-SYSKEYUP-Nachricht.**         |
| 16-23 | Der Scancode. Der Wert hängt vom OEM ab.                                                                                                                                                                                  |
| 24    | Gibt an, ob es sich bei der Taste um eine erweiterte Taste handelt, z. B. die rechte ALT- und STRG-Taste, die auf einer erweiterten Tastatur mit 101 oder 102 Tasten angezeigt wird. Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist es 0 (null).                   |
| 25-28 | Reserviert; nicht verwenden.                                                                                                                                                                                                         |
| 29    | Der Kontextcode. Der Wert ist 1, wenn der ALT-Schlüssel nicht verfügbar ist, während der Schlüssel losgelassen wird. ist 0 (null), wenn die **\_ WM-SYSKEYUP-Meldung** an das aktive Fenster gesendet wird, da kein Fenster den Tastaturfokus besitzt. |
| 30    | Der vorherige Schlüsselzustand. Der Wert ist immer 1 für eine **\_ WM-SYSKEYUP-Nachricht.**                                                                                                                                                 |
| 31    | Der Übergangszustand. Der Wert ist immer 1 für eine **\_ WM-SYSKEYUP-Nachricht.**                                                                                                                                                   |

Weitere Informationen finden Sie unter [Tastatureingabe-Meldungsflags.](about-keyboard-input.md#keystroke-message-flags)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Hinweise

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sendet eine [**\_ WM-SYSCOMMAND-Nachricht**](/windows/desktop/menurc/wm-syscommand) an das Fenster der obersten Ebene, wenn die Taste F10 oder der ALT-Schlüssel freigegeben wurde. Der *wParam-Parameter* der Nachricht ist auf **SC \_ KEYMENU** festgelegt.

Wenn der Kontextcode 0 (null) ist, kann die Nachricht an die [**TranslateAccelerator-Funktion**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) übergeben werden, die sie so behandelt, als wäre es eine normale Schlüsselnachricht anstelle einer Zeichenschlüsselnachricht. Dadurch können Zugriffstasten mit dem aktiven Fenster verwendet werden, auch wenn das aktive Fenster nicht über den Tastaturfokus verfügt.

Bei erweiterten Tastaturen mit 101 und 102 Tasten sind erweiterte Tasten die rechten ALT- und STRG-Tasten im Hauptbereich der Tastatur. die INS-, DEL-, HOME-, END-, PAGE UP-, PAGE DOWN- und PFEILTASTEn in den Clustern links neben der numerischen Tastatur; und die Trenntaste (/) und die EINGABETASTE in der numerischen Tastatur. Andere Tastaturen unterstützen möglicherweise das erweiterte Tastenbit im *lParam-Parameter.*

Für Nicht-USA Erweiterte Tastaturen mit 102 Tasten, die rechte ALT-TASTE wird als STRG+ALT-TASTE behandelt. Die folgende Tabelle zeigt die Abfolge der Nachrichten, die sich ergeben, wenn der Benutzer diesen Schlüssel drückt und freigibt.



| `Message`                           | Code mit virtuellem Schlüssel |
|-----------------------------------|------------------|
| [**WM \_ KEYDOWN**](wm-keydown.md) | **\_VK-STEUERELEMENT**  |
| [**WM \_ KEYDOWN**](wm-keydown.md) | **\_VK-MENÜ**     |
| [**WM \_ KEYUP**](wm-keyup.md)     | **\_VK-STEUERELEMENT**  |
| **WM \_ SYSKEYUP**                  | **\_VK-MENÜ**     |



 

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

[**WM \_ SYSKEYDOWN**](wm-syskeydown.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastatureingaben](keyboard-input.md)
</dt> </dl>

 

