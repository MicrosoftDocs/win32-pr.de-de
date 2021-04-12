---
title: WM_SYSCHAR Meldung (Winuser. h)
description: Wird im Fenster mit dem Tastaturfokus gepostet, wenn eine WM- \_ syskeydown-Meldung von der translatemess-Funktion übersetzt wird.
ms.assetid: 55987105-3c53-42e5-8fab-a3c9f2ca7273
keywords:
- WM_SYSCHAR von Meldungs Menüs und anderen Ressourcen
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
ms.openlocfilehash: 8d14d2f8829cfd199049d3a1b254065918393c18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519196"
---
# <a name="wm_syschar-message"></a>WM- \_ syschar-Nachricht

Wird im Fenster mit dem Tastaturfokus gepostet, wenn eine [**WM- \_ syskeydown**](/windows/desktop/inputdev/wm-syskeydown) -Meldung von der [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion übersetzt wird. Er gibt den Zeichencode eines System Zeichen Schlüssels an, bei dem es sich um einen Zeichen Schlüssel handelt, der gedrückt wird, während die Alt-Taste gedrückt ist.


```C++
#define WM_SYSCHAR                      0x0106
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Zeichencode der Fenstermenü Taste.

</dd> <dt>

*lParam* 
</dt> <dd>

Die Wiederholungs Anzahl, der Überprüfungs Code, das erweiterte schlüsselflag, der Kontext Code, das vorherige schlüsselstatusflag und das Flag für den Übergangszustand, wie in der folgenden Tabelle gezeigt.



| Bits                                                                             | Bedeutung                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 15</dt> </dl>  | Die Wiederholungs Anzahl für die aktuelle Nachricht. Der Wert gibt an, wie oft der Tastatur Schlag automatisch wiederholt wird, weil der Benutzer die Taste gedrückt hält. Wenn die Tastatureingabe lang genug gehalten wird, werden mehrere Nachrichten gesendet. Die Wiederholungs Anzahl ist jedoch nicht kumulativ.<br/> |
| <dl> <dt>16 23</dt> </dl> | Der Überprüfungs Code. Der Wert hängt vom Originalgerätehersteller (OEM) ab.<br/>                                                                                                                                                                                          |
| <dl> <dt>24</dt> </dl>    | Gibt an, ob der Schlüssel ein erweiterter Schlüssel ist, z. b. die Rechte ALT-Taste und die STRG-Taste, die auf einer erweiterten 101-oder 102-Tastatur-Tastatur angezeigt werden. Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist der Wert 0.<br/>                                                                |
| <dl> <dt>25 28</dt> </dl> | Bleiben Verwenden Sie nicht.<br/>                                                                                                                                                                                                                                                   |
| <dl> <dt>29</dt> </dl>    | Der Kontext Code. Der Wert ist 1, wenn die Alt-Taste gedrückt gehalten wird, während die Taste gedrückt wird. Andernfalls ist der Wert 0.<br/>                                                                                                                                                       |
| <dl> <dt>30</dt> </dl>    | Der vorherige Schlüssel Zustand. Der Wert ist 1, wenn der Schlüssel vor dem Senden der Nachricht nicht angezeigt wird, oder wenn der Schlüssel auf "0" festgelegt ist.<br/>                                                                                                                                                      |
| <dl> <dt>31</dt> </dl>    | Der Übergangszustand. Der Wert ist 1, wenn der Schlüssel freigegeben wird, oder der Wert ist 0, wenn die Taste gedrückt wird.<br/>                                                                                                                                                              |

Weitere Details finden Sie unter [KeyStroke-Nachrichtenflags](../inputdev/about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Wenn der Kontext Code 0 (null) ist, kann die Nachricht an die [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) -Funktion übermittelt werden, die Sie behandelt, als ob es sich um eine Standard Schlüsselnachricht anstelle einer System-Zeichen Schlüssel Nachricht handelt. Dies ermöglicht das Verwenden von Zugriffstasten für das aktive Fenster, auch wenn das aktive Fenster nicht über den Tastaturfokus verfügt.

Für erweiterte 101-und 102-Key-Tastaturen sind erweiterte Schlüssel die Rechte ALT-Taste und die STRG-Taste im Hauptabschnitt der Tastatur. die Eingaben "ins", "Entf", "Start", "Ende", "Bild-ab" und "Pfeil" in den Clustern auf der linken Seite der numerischen Tastatur die Druck-Scrn-Taste; die Pause-Taste. der NumLock-Schlüssel; und die Unterteilung (/) und EINGABETASTE in der numerischen Tastatur. Andere Tastaturen unterstützen möglicherweise das Extended-Key-Bit im-Parameter.

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

[**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ syskeydown**](/windows/desktop/inputdev/wm-syskeydown)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

