---
description: Wird an eine Anwendung gesendet, wenn das IME ein Zeichen des Konvertierungs Ergebnisses erhält. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 1e1353c3-5215-4829-a00a-2fee47a430eb
title: WM_IME_CHAR Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0e2df06d9d837b0c1fbc0f9c9d9eb852252c47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393777"
---
# <a name="wm_ime_char-message"></a>WM- \_ IME- \_ char-Nachricht

Wird an eine Anwendung gesendet, wenn das IME ein Zeichen des Konvertierungs Ergebnisses erhält. Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


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

*HWND* 
</dt> <dd>

Ein Handle für Fenster.

</dd> <dt>

*wParam* 
</dt> <dd>

**DBCS:** Ein Einzel Byte-oder Doppelbyte-Zeichen Wert. Bei einem Double-Byte-Zeichen enthält (Byte) (wParam >> 8) das führende Byte. Beachten Sie, dass die Klammern erforderlich sind, da der Umwandlungs Operator eine höhere Rangfolge aufweist als der Shift-Operator.

**Unicode:** Ein Unicode-Zeichen Wert.

</dd> <dt>

*lParam* 
</dt> <dd>

Die Wiederholungs Anzahl, der Scan Code, das erweiterte schlüsselflag, der Kontext Code, das vorherige schlüsselstatusflag und das Übergangs Zustands Kennzeichen mit den unten definierten Werten.



| bit   | Bedeutung                                                                              |
|-------|--------------------------------------------------------------------------------------|
| 0-15  | Wiederholungs Anzahl. Da das erste Byte und das zweite Byte fortlaufend sind, ist dies immer 1. |
| 16-23 | Scannen Sie Code nach einem kompletten asiatischen Zeichen.                                            |
| 24    | Erweiterter Schlüssel.                                                                        |
| 25-28 | Nicht verwendet.                                                                            |
| 29    | Kontext Code.                                                                        |
| 30    | Vorheriger Schlüssel Zustand.                                                                  |
| 31    | Übergangsstatus.                                                                    |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Anders als bei der " [**WM \_ char**](../inputdev/wm-char.md) "-Meldung für ein nicht-Unicode-Fenster kann diese Meldung Doppelbyte-und Einzel Byte-Zeichen Werte enthalten. Bei einem Unicode-Fenster ist diese Meldung mit WM char identisch \_ .

Wenn bei einem nicht-Unicode-Fenster die "WM \_ IME \_ char"-Nachricht ein Doppelbyte Zeichen enthält und die Anwendung diese Nachricht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergibt, konvertiert der IME diese Nachricht in zwei WM- \_ char-Nachrichten, die jeweils ein Byte des Doppelbyte Zeichens enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eingabemethoden-Manager](input-method-manager.md)
</dt> <dt>

[Eingabemethoden-Manager-Meldungen](input-method-manager-messages.md)
</dt> </dl>

 

 
