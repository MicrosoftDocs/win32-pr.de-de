---
title: WM_DEADCHAR Meldung (Winuser. h)
description: Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine WM- \_ KeyUp-Meldung von der translatemess-Funktion übersetzt wird.
ms.assetid: ada9a61c-dabf-447b-ae13-91803c097f0d
keywords:
- Tastatur-und Maus Eingaben für WM_DEADCHAR Nachricht
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
ms.openlocfilehash: 6053095b912360e9875fa062c2daba7cafcfd43b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476164"
---
# <a name="wm_deadchar-message"></a>WM- \_ deadchar-Nachricht

Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine [**WM- \_ KeyUp**](wm-keyup.md) -Meldung von der [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion übersetzt wird. **WM \_ Deadchar** gibt einen Zeichencode an, der von einem unzustellbaren Schlüssel generiert wird. Eine unzustellbare Taste ist ein Schlüssel, der ein Zeichen generiert, z. b. den Umschlag (Double-dot), der mit einem anderen Zeichen kombiniert wird, um ein zusammengesetztes Zeichen zu bilden. Beispielsweise wird das Zeichen "enlaut-O" () generiert, indem die unzustellbare Taste für das Zeichen "ein" eingegeben und dann der Schlüssel "O" eingegeben wird.


```C++
#define WM_DEADCHAR                     0x0103
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der von der unzustellbaren Taste generierte Zeichencode.

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

Die **WM \_ deadchar** -Nachricht wird in der Regel von Anwendungen verwendet, um dem Benutzer Feedback zu den einzelnen Schlüsseln zu geben. Beispielsweise kann eine Anwendung den Akzent an der aktuellen Zeichenposition anzeigen, ohne die Einfügemarke zu verschieben.

Da es nicht notwendigerweise eine 1:1-Entsprechung zwischen den gedrückten Schlüsseln und Zeichen Nachrichten gibt, sind die Informationen im höherwertigen Wort des *LPARAM* -Parameters für Anwendungen in der Regel nicht nützlich. Die Informationen im höherwertigen Wort gelten nur für die letzte [**WM- \_ KeyDown**](wm-keydown.md) -Nachricht, die vor der Bereitstellung der **WM \_ deadchar** -Nachricht steht.

Erweiterte Schlüssel für erweiterte 101-und 102-keytastaturen sind die Rechte ALT-Taste und die Rechte STRG-Taste im Hauptabschnitt der Tastatur. die Eingaben "ins", "Entf", "Start", "Ende", "Bild-ab" und "Pfeil" in den Clustern auf der linken Seite der numerischen Tastatur und die Unterteilung (/) und EINGABETASTE in der numerischen Tastatur. Einige andere Tastaturen unterstützen möglicherweise das Extended-Key-Bit im *LPARAM* -Parameter.

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM- \_ KeyDown**](wm-keydown.md)
</dt> <dt>

[**WM- \_ KeyUp**](wm-keyup.md)
</dt> <dt>

[**WM \_ sysdeadchar**](wm-sysdeadchar.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastatureingabe](keyboard-input.md)
</dt> </dl>

 

