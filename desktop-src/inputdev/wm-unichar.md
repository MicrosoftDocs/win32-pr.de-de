---
title: WM_UNICHAR Meldung (Winuser. h)
description: Die WM \_ UNICHAR-Nachricht kann von einer Anwendung verwendet werden, um Eingaben für andere Fenster bereitzustellen.
ms.assetid: edbfcf14-0371-43ce-9676-eb10d964d0b7
keywords:
- Tastatur-und Maus Eingaben für WM_UNICHAR Nachricht
topic_type:
- apiref
api_name:
- WM_UNICHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833b5cb59095f5aecc8c0172857c8761fd92449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340335"
---
# <a name="wm_unichar-message"></a>WM \_ UNICHAR-Nachricht

Die **WM \_ UNICHAR** -Nachricht kann von einer Anwendung verwendet werden, um Eingaben für andere Fenster bereitzustellen. Diese Meldung enthält den Zeichencode der Taste, die gedrückt wurde. (Testen Sie, ob eine Ziel-APP **WM- \_ UNICHAR** -Nachrichten verarbeiten kann, indem Sie die Nachricht mit *wParam* auf **Unicode \_ nochar** senden.)


```C++
#define WM_UNICHAR                      0x0109
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Zeichencode des Schlüssels.

Wenn *wParam* eine **Unicode \_** -Datei ist und die Anwendung diese Nachricht verarbeitet, wird **true** zurückgegeben. Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion gibt **false** zurück (Standard).

Wenn *wParam* nicht der **Unicode \_**-Wert ist, wird **false** zurückgegeben. Der Unicode-  [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sendet eine [**WM \_ char**](wm-char.md) -Nachricht mit denselben Parametern, und die ANSI **defwindowproc** -Funktion postet entweder eine oder zwei **WM \_ char** -Nachrichten mit den entsprechenden ANSI-Zeichen.

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
| 29    | Der Kontext Code. Der Wert ist 1, wenn die Alt-Taste gedrückt gehalten wird, während die Taste gedrückt wird. Andernfalls ist der Wert 0.                                                                                                                                                     |
| 30    | Der vorherige Schlüssel Zustand. Der Wert ist 1, wenn der Schlüssel vor dem Senden der Nachricht nicht angezeigt wird, oder wenn der Schlüssel auf "0" festgelegt ist.                                                                                                                                                    |
| 31    | Der Übergangszustand. Der Wert ist 1, wenn der Schlüssel freigegeben wird, oder der Wert ist 0, wenn die Taste gedrückt wird.                                                                                                                                                            |

Weitere Details finden Sie unter [KeyStroke-Nachrichtenflags](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Die **WM- \_ UNICHAR** -Nachricht ähnelt [**WM \_ char**](wm-char.md), verwendet jedoch UTF (Unicode Transformation Format)-32, während **WM \_ char** UTF-16 verwendet.

Diese Nachricht dient zum Senden oder Bereitstellen von Unicode-Zeichen an ANSI-Fenster und kann zusätzliche Unicode-unikezeichen verarbeiten.

Da es nicht notwendigerweise eine 1:1-Entsprechung zwischen den gedrückten Schlüsseln und Zeichen Nachrichten gibt, sind die Informationen im höherwertigen Wort des *LPARAM* -Parameters für Anwendungen in der Regel nicht nützlich. Die Informationen im höherwertigen Wort gelten nur für die letzte [**WM- \_ KeyDown**](wm-keydown.md) -Nachricht, die vor der Bereitstellung der **WM \_ UNICHAR** -Nachricht steht.

Erweiterte Schlüssel für erweiterte 101-und 102-keytastaturen sind die Rechte ALT-Taste und die Rechte STRG-Taste im Hauptabschnitt der Tastatur. die Eingaben "ins", "Entf", "Start", "Ende", "Bild-ab" und "Pfeil" in den Clustern auf der linken Seite der numerischen Tastatur und die Unterteilung (/) und EINGABETASTE in der numerischen Tastatur. Einige andere Tastaturen unterstützen möglicherweise das Extended-Key-Bit im *LPARAM* -Parameter.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ -Zeichen**](wm-char.md)
</dt> <dt>

[**WM- \_ KeyDown**](wm-keydown.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastatureingabe](keyboard-input.md)
</dt> </dl>

 

