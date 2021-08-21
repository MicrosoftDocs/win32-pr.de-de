---
title: WM_SYSDEADCHAR (Winuser.h)
description: Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine WM \_ SYSKEYDOWN-Nachricht von der TranslateMessage-Funktion übersetzt wird.
ms.assetid: cf9a1171-a47c-4d7b-b351-31f41a893b20
keywords:
- WM_SYSDEADCHAR der Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_SYSDEADCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e7ddf63ab4643ef59e45a4850a18a9823753c16a59b4519fe099326fe071704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757222"
---
# <a name="wm_sysdeadchar-message"></a>WM \_ SYSDEADCHAR-Meldung

Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine [**WM \_ SYSKEYDOWN-Nachricht**](wm-syskeydown.md) von der [**TranslateMessage-Funktion übersetzt**](/windows/desktop/api/winuser/nf-winuser-translatemessage) wird. **WM \_ SYSDEADCHAR gibt** den Zeichencode eines in dead-Schlüssels des Systems an, d. b. eine in dead-Taste, die gedrückt wird, während die ALT-TASTE gedrückt wird.


```C++
#define WM_SYSDEADCHAR                  0x0107
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der zeichencode, der von der systemin dead-Taste generiert wird, d.&a; eine in dead-Taste, die gedrückt wird, während die ALT-TASTE gedrückt wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Anzahl der Wiederholungen, Überprüfungscode, Flag für erweiterte Schlüssel, Kontextcode, vorheriges Schlüsselzustandsflag und Übergangszustandsflag, wie in der folgenden Tabelle dargestellt.



| Bits  | Bedeutung                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Die Wiederholungsanzahl für die aktuelle Meldung. Der Wert gibt an, wie oft die Tastatureingabe automatisch angezeigt wird, wenn der Benutzer den Schlüssel hält. Wenn die Tastatureingabe lang genug gehalten wird, werden mehrere Nachrichten gesendet. Die Wiederholungsanzahl ist jedoch nicht kumulativ. |
| 16-23 | Der Scancode. Der Wert hängt vom OEM ab.                                                                                                                                                                                                                          |
| 24    | Gibt an, ob es sich bei der Taste um eine erweiterte Taste handelt, z. B. die rechte ALT- und STRG-Taste, die auf einer erweiterten Tastatur mit 101 oder 102 Tasten angezeigt werden. Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. andernfalls ist es 0.                                                              |
| 25-28 | Reserviert; nicht verwenden.                                                                                                                                                                                                                                                 |
| 29    | Der Kontextcode. Der Wert ist 1, wenn die ALT-TASTE gedrückt gehalten wird, während die Taste gedrückt wird. andernfalls ist der Wert 0.                                                                                                                                                     |
| 30    | Der vorherige Schlüsselzustand. Der Wert ist 1, wenn der Schlüssel vor dem Senden der Nachricht heruntergefahren ist, oder 0, wenn der Schlüssel hoch ist.                                                                                                                                                    |
| 31    | Übergangsstatus. Der Wert ist 1, wenn die Taste freigegeben wird, oder 0, wenn die Taste gedrückt wird.                                                                                                                                                                |

Weitere Informationen finden Sie unter [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Hinweise

Für erweiterte Tastaturen mit 101 und 102 Tasten sind erweiterte Tasten die rechte ALT- und STRG-Taste im Hauptteil der Tastatur. DIE INS-, DEL-, HOME-, END-, PAGE UP-, PAGE DOWN- und Pfeiltasten in den Clustern links neben der numerischen Tastatur; und die Division (/) und die EINGABETASTEn in der numerischen Tastatur. Andere Tastaturen unterstützen möglicherweise das Bit mit erweiterter Taste im *lParam-Parameter.*

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ DEADCHAR**](wm-deadchar.md)
</dt> <dt>

[**WM \_ SYSKEYDOWN**](wm-syskeydown.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastatureingaben](keyboard-input.md)
</dt> </dl>

 

