---
title: WM_DEADCHAR Meldung (Winuser.h)
description: Wird mit dem Tastaturfokus an das Fenster gesendet, wenn eine WM \_ KEYUP-Nachricht von der TranslateMessage-Funktion übersetzt wird.
ms.assetid: ada9a61c-dabf-447b-ae13-91803c097f0d
keywords:
- WM_DEADCHAR Meldung Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_DEADCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e4921d399c4a1c7a86596bfcc907b52d9c834235d133d6455b88c5a5a40c89a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778750"
---
# <a name="wm_deadchar-message"></a>WM \_ DEADCHAR-Nachricht

Wird mit dem Tastaturfokus an das Fenster gesendet, wenn eine [**WM \_ KEYUP-Nachricht**](wm-keyup.md) von der [**TranslateMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-translatemessage) übersetzt wird. **WM \_ DEADCHAR** gibt einen Zeichencode an, der von einem in dead-Schlüssel generiert wird. Ein in dead key ist ein Schlüssel, der ein Zeichen generiert, z. B. den Umlaut (doppelter Punkt), der mit einem anderen Zeichen kombiniert wird, um ein zusammengesetztes Zeichen zu bilden. Beispielsweise wird das Umlaut-O-Zeichen ( ) generiert, indem der in dead key für das Umlaut-Zeichen und dann der O-Schlüssel eingeben wird.


```C++
#define WM_DEADCHAR                     0x0103
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der vom un toten Schlüssel generierte Zeichencode.

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
| 29    | Der Kontextcode. Der Wert ist 1, wenn die ALT-Taste gedrückt gehalten wird, während die Taste gedrückt wird. Andernfalls ist der Wert 0.                                                                                                                                                     |
| 30    | Der vorherige Schlüsselzustand. Der Wert ist 1, wenn der Schlüssel ausgeschaltet ist, bevor die Nachricht gesendet wird, oder 0, wenn der Schlüssel hoch ist.                                                                                                                                                    |
| 31    | Der Übergangszustand. Der Wert ist 1, wenn die Taste losgelassen wird, oder 0, wenn die Taste gedrückt wird.                                                                                                                                                            |

Weitere Informationen finden Sie unter [Tastatureingabe-Meldungsflags.](about-keyboard-input.md#keystroke-message-flags)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Hinweise

Die **WM \_ DEADCHAR-Nachricht** wird in der Regel von Anwendungen verwendet, um dem Benutzer Feedback zu jeder gedrückten Taste zu geben. Beispielsweise kann eine Anwendung den Akzent an der aktuellen Zeichenposition anzeigen, ohne das Caretzeichen zu verschieben.

Da es nicht notwendigerweise eine 1:1-Entsprechung zwischen gedrückten Tasten und generierten Zeichennachrichten gibt, sind die Informationen im hochwertigen Wort des *lParam-Parameters* in der Regel für Anwendungen nicht nützlich. Die Informationen im Hochreihenfolgewort gelten nur für die letzte [**WM \_ KEYDOWN-Nachricht,**](wm-keydown.md) die der Veröffentlichung der **WM \_ DEADCHAR-Nachricht** vorausgeht.

Bei erweiterten Tastaturen mit 101 und 102 Tasten sind erweiterte Tasten die rechte ALT-TASTE und die rechten STRG-Tasten im Hauptbereich der Tastatur. die TASTEN INS, DEL, HOME, END, PAGE UP, PAGE DOWN und pfeilweise in den Clustern links neben der numerischen Tastatur; und die Trenntaste (/) und die EINGABETASTE in der numerischen Tastatur. Einige andere Tastaturen unterstützen möglicherweise das erweiterte Tastenbit im *lParam-Parameter.*

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

[**WM \_ KEYDOWN**](wm-keydown.md)
</dt> <dt>

[**WM \_ KEYUP**](wm-keyup.md)
</dt> <dt>

[**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastatureingaben](keyboard-input.md)
</dt> </dl>

 

