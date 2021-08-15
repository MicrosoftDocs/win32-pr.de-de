---
title: WM_KEYUP Meldung (Winuser.h)
description: Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine Nichtsystemtaste losgelassen wird. Eine Nichtsystemtaste ist eine Taste, die gedrückt wird, wenn die ALT-Taste nicht gedrückt wird, oder eine Tastaturtaste, die gedrückt wird, wenn ein Fenster den Tastaturfokus besitzt.
ms.assetid: 67d9d82d-fab0-4aec-a337-7a9cb2b0b586
keywords:
- WM_KEYUP Meldung Tastatur- und Mauseingabe
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
ms.openlocfilehash: fc23b941f232007a781ca160538f28d864f818639df47a180de472f54cd89a8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247822"
---
# <a name="wm_keyup-message"></a>WM \_ KEYUP-Nachricht

Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine Nichtsystemtaste losgelassen wird. Eine Nichtsystemtaste ist eine Taste, die gedrückt wird, wenn die ALT-Taste *nicht* gedrückt wird, oder eine Tastaturtaste, die gedrückt wird, wenn ein Fenster den Tastaturfokus besitzt.


```C++
#define WM_KEYUP                        0x0101
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Virtuelle Schlüsselcode des Nichtsystemschlüssels. Weitere Informationen finden Sie unter [Codes für virtuelle Schlüssel.](virtual-key-codes.md)

</dd> <dt>

*lParam* 
</dt> <dd>

Die Wiederholungsanzahl, der Scancode, das Flag für erweiterte Schlüssel, der Kontextcode, das vorherige Schlüsselzustandsflag und das Übergangszustandsflag, wie in der folgenden Tabelle gezeigt.



| Bits  | Bedeutung                                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Die Wiederholungsanzahl für die aktuelle Nachricht. Der Wert gibt an, wie oft die Tastatureingabe automatisch erfolgt, weil der Benutzer den Schlüssel gedrückt hält. Die Wiederholungsanzahl beträgt immer 1 für eine **WM \_ KEYUP-Nachricht.** |
| 16-23 | Der Scancode. Der Wert hängt vom OEM ab.                                                                                                                                                                     |
| 24    | Gibt an, ob es sich bei der Taste um eine erweiterte Taste handelt, z. B. die rechte ALT- und STRG-Taste, die auf einer erweiterten Tastatur mit 101 oder 102 Tasten angezeigt wird. Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist es 0.         |
| 25-28 | Reserviert; nicht verwenden.                                                                                                                                                                                            |
| 29    | Der Kontextcode. Der Wert ist immer 0 für eine **WM \_ KEYUP-Nachricht.**                                                                                                                                             |
| 30    | Der vorherige Schlüsselzustand. Der Wert ist immer 1 für eine **WM \_ KEYUP-Nachricht.**                                                                                                                                       |
| 31    | Der Übergangszustand. Der Wert ist immer 1 für eine **WM \_ KEYUP-Nachricht.**                                                                                                                                         |

Weitere Informationen finden Sie unter [Tastatureingabe-Meldungsflags.](about-keyboard-input.md#keystroke-message-flags)
 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Hinweise

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sendet eine [**\_ WM-SYSCOMMAND-Nachricht**](/windows/desktop/menurc/wm-syscommand) an das Fenster der obersten Ebene, wenn die Taste F10 oder der ALT-Schlüssel freigegeben wurde. Der *wParam-Parameter* der Nachricht ist auf SC \_ KEYMENU festgelegt.

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

[**WM \_ KEYDOWN**](wm-keydown.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastatureingaben](keyboard-input.md)
</dt> </dl>

 

