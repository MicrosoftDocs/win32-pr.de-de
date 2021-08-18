---
description: Wird an eine Anwendung gesendet, wenn die IME ein Zeichen des Konvertierungsergebnisses erhält. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 1e1353c3-5215-4829-a00a-2fee47a430eb
title: WM_IME_CHAR Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337ca982cbd755e01f3dfab465d8b82948dfdbf053a4a7c03417a1d508bc42d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146783"
---
# <a name="wm_ime_char-message"></a>WM \_ IME \_ CHAR-Nachricht

Wird an eine Anwendung gesendet, wenn die IME ein Zeichen des Konvertierungsergebnisses erhält. Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,
 WM_IME_CHAR,
 WPARAM wParam,
 LPARAM lParam   
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hwnd* 
</dt> <dd>

Ein Handle für fenster.

</dd> <dt>

*wParam* 
</dt> <dd>

**DBCS:** Ein Einzel-Byte- oder Doppel-Byte-Zeichenwert. Bei einem Doppel-Byte-Zeichen enthält (BYTE)(wParam >> 8) das lead-Byte. Beachten Sie, dass die Klammern erforderlich sind, da der Umwandlungsoperator eine höhere Rangfolge als der Schiebeoperator hat.

**Unicode:** Ein Unicode-Zeichenwert.

</dd> <dt>

*lParam* 
</dt> <dd>

Wiederholungsanzahl, Scancode, erweitertes Schlüsselflag, Kontextcode, vorheriges Schlüsselzustandsflag und Übergangszustandsflag mit Werten, die unten definiert sind.



| bit   | Bedeutung                                                                              |
|-------|--------------------------------------------------------------------------------------|
| 0-15  | Wiederholungsanzahl. Da das erste und das zweite Byte kontinuierlich sind, ist dies immer 1. |
| 16-23 | Scancode für ein vollständiges asiatisches Zeichen.                                            |
| 24    | Erweiterter Schlüssel.                                                                        |
| 25-28 | Wird nicht verwendet.                                                                            |
| 29    | Kontextcode.                                                                        |
| 30    | Vorheriger Schlüsselstatus.                                                                  |
| 31    | Übergangsstatus.                                                                    |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Im Gegensatz zur [**WM \_ CHAR-Nachricht**](../inputdev/wm-char.md) für ein Nicht-Unicode-Fenster kann diese Nachricht Double-Byte- und Einzel-Byte-Zeichenwerte enthalten. Bei einem Unicode-Fenster entspricht diese Meldung WM \_ CHAR.

Wenn die WM IME CHAR-Nachricht für ein \_ \_ Nicht-Unicode-Fenster ein Doppel-Byte-Zeichen enthält und die Anwendung diese Nachricht an [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergibt, konvertiert der IME diese Nachricht in zwei WM \_ CHAR-Nachrichten, die jeweils ein Byte des Doppel-Byte-Zeichens enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Eingabemethoden-Manager](input-method-manager.md)
</dt> <dt>

[Eingabemethoden-Manager-Nachrichten](input-method-manager-messages.md)
</dt> </dl>

 

 
