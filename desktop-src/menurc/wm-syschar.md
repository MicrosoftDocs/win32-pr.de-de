---
title: WM_SYSCHAR (Winuser.h)
description: Wird im Fenster mit dem Tastaturfokus veröffentlicht, wenn eine WM SYSKEYDOWN-Nachricht von der \_ TranslateMessage-Funktion übersetzt wird.
ms.assetid: 55987105-3c53-42e5-8fab-a3c9f2ca7273
keywords:
- WM_SYSCHAR von Nachrichtenmenüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_SYSCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b42d88d5ae1346032da2c663dd8c9189c030d5bb7d538ab7ef84403d42fba76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472088"
---
# <a name="wm_syschar-message"></a>WM \_ SYSCHAR-Meldung

Wird im Fenster mit dem Tastaturfokus veröffentlicht, wenn eine [**WM \_ SYSKEYDOWN-Nachricht**](/windows/desktop/inputdev/wm-syskeydown) von der [**TranslateMessage-Funktion übersetzt**](/windows/desktop/api/winuser/nf-winuser-translatemessage) wird. Sie gibt den Zeichencode einer Systemzeichentaste an, d. &a. eine Zeichentaste, die gedrückt wird, während die ALT-TASTE gedrückt ist.


```C++
#define WM_SYSCHAR                      0x0106
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Zeichencode der Menütaste des Fensters.

</dd> <dt>

*lParam* 
</dt> <dd>

Anzahl der Wiederholungen, Überprüfungscode, Flag für erweiterte Schlüssel, Kontextcode, vorheriges Schlüsselzustandsflag und Übergangszustandsflag, wie in der folgenden Tabelle dargestellt.



| Bits                                                                             | Bedeutung                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 15</dt> </dl>  | Die Wiederholungsanzahl für die aktuelle Meldung. Der Wert gibt an, wie oft die Tastatureingabe automatisch wiederholt wurde, weil der Benutzer die Taste hält. Wenn die Tastatureingabe lang genug gehalten wird, werden mehrere Nachrichten gesendet. Die Wiederholungsanzahl ist jedoch nicht kumulativ.<br/> |
| <dl> <dt>16 23</dt> </dl> | Der Scancode. Der Wert hängt vom Originalgerätehersteller (Original Equipment Manufacturer, OEM) ab.<br/>                                                                                                                                                                                          |
| <dl> <dt>24</dt> </dl>    | Gibt an, ob es sich bei der Taste um eine erweiterte Taste handelt, z. B. die rechte ALT- und STRG-Taste, die auf einer erweiterten Tastatur mit 101 oder 102 Tasten angezeigt werden. Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. andernfalls ist es 0.<br/>                                                                |
| <dl> <dt>25 28</dt> </dl> | Reserviert; nicht verwenden.<br/>                                                                                                                                                                                                                                                   |
| <dl> <dt>29</dt> </dl>    | Der Kontextcode. Der Wert ist 1, wenn die ALT-TASTE gedrückt gehalten wird, während die Taste gedrückt wird. andernfalls ist der Wert 0.<br/>                                                                                                                                                       |
| <dl> <dt>30</dt> </dl>    | Der vorherige Schlüsselzustand. Der Wert ist 1, wenn der Schlüssel vor dem Senden der Nachricht heruntergefahren ist, oder 0, wenn der Schlüssel hoch ist.<br/>                                                                                                                                                      |
| <dl> <dt>31</dt> </dl>    | Der Übergangszustand. Der Wert ist 1, wenn die Taste freigegeben wird, oder 0, wenn die Taste gedrückt wird.<br/>                                                                                                                                                              |

Weitere Informationen finden Sie unter [Keystroke Message Flags](../inputdev/about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Hinweise

Wenn der Kontextcode 0 (null) ist, kann die Nachricht an die [**TranslateAccelerator-Funktion**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) übergeben werden, die sie so behandelt, als wäre sie eine Standardschlüsselmeldung anstelle einer Systemzeichenschlüsselnachricht. Dadurch können Zugriffstasten auch dann mit dem aktiven Fenster verwendet werden, wenn das aktive Fenster nicht über den Tastaturfokus verfügt.

Für erweiterte Tastaturen mit 101 und 102 Tasten sind erweiterte Tasten die rechte ALT- und STRG-Taste im Hauptteil der Tastatur. DIE TASTEN INS, DEL, HOME, END, PAGE UP, PAGE DOWN und die Pfeiltasten in den Clustern links neben der numerischen Tastatur; PRINT PRINTN-Taste; DIE BREAK-TASTE; NUMLOCK-TASTE; und die Division (/) und die EINGABETASTEn in der numerischen Tastatur. Andere Tastaturen unterstützen möglicherweise das Bit mit erweiterter Taste im -Parameter.

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

[**Translateaccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

