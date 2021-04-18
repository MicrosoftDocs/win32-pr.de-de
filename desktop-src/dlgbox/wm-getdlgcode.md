---
title: WM_GETDLGCODE Meldung (Winuser. h)
description: Wird an die Fenster Prozedur gesendet, die einem Steuerelement zugeordnet ist.
ms.assetid: 96d2caee-be6e-46e9-98b3-bffc3af1c003
keywords:
- Dialog Felder WM_GETDLGCODE Meldung
topic_type:
- apiref
api_name:
- WM_GETDLGCODE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d6e1ddb3be21e227c4dad404a06113f5c50a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337531"
---
# <a name="wm_getdlgcode-message"></a>WM \_ getdlgcode-Meldung

Wird an die Fenster Prozedur gesendet, die einem Steuerelement zugeordnet ist. Standardmäßig verarbeitet das System alle Tastatureingaben für das Steuerelement. Das System interpretiert bestimmte Typen von Tastatureingaben als Dialogfeld-Navigationstasten. Um dieses Standardverhalten zu überschreiben, kann das-Steuerelement auf die **WM- \_ getdlgcode** -Meldung reagieren, um die Eingabetypen anzugeben, die verarbeitet werden sollen.


```C++
#define WM_GETDLGCODE                   0x0087
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der vom Benutzer gedrückte virtuelle Schlüssel, der Windows aufgefordert hat, diese Benachrichtigung auszugeben. Der Handler muss diese Schlüssel selektiv verarbeiten. Beispielsweise kann der Handler die " **VK \_ Return** "-Rückgabe, aber die **\_ Registerkarte "VK** " an das Besitzer Fenster delegieren und verarbeiten. Eine Liste der Werte finden Sie unter [**Virtual Key Codes**](/windows/desktop/inputdev/virtual-key-codes).

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**msg**](/windows/win32/api/winuser/ns-winuser-msg) -Struktur (oder **null** , wenn das System eine Abfrage ausführt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist einer oder mehrere der folgenden Werte, die angeben, welche Art von Eingabe die Anwendung verarbeitet.



| Rückgabecode/-wert                                                                                                                                                | BESCHREIBUNG                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Dlgc \_ Schaltfläche**</dt> <dt>0x2000</dt> </dl>          | Gedrückt.<br/>                                                                                                         |
| <dl> <dt>**Dlgc \_ DEFPUSHBUTTON**</dt> <dt>0x0010</dt> </dl>   | Standard Schaltfläche "Push".<br/>                                                                                            |
| <dl> <dt>**Dlgc \_ Hassetsel**</dt> <dt>0x0008</dt> </dl>       | [**EM \_ Nachrichten**](/windows/desktop/Controls/em-setsel) Nachrichten.<br/>                                                           |
| <dl> <dt>**Dlgc \_ RadioButton**</dt> <dt>0x0040</dt> </dl>     | Optionsfeld.<br/>                                                                                                   |
| <dl> <dt>**Dlgc \_ Statisch**</dt> <dt>0x0100</dt> </dl>          | Statisches Steuerelement.<br/>                                                                                                 |
| <dl> <dt>**Dlgc \_ Undefpushbutton**</dt> <dt>0x0020</dt> </dl> | Nicht standardmäßige pushschaltfläche.<br/>                                                                                        |
| <dl> <dt>**Dlgc \_ Wantallkeys**</dt> <dt>0x0004</dt> </dl>     | Alle Tastatureingaben.<br/>                                                                                             |
| <dl> <dt>**Dlgc \_ Wantpfeile**</dt> <dt>0x0001</dt> </dl>      | Richtungs Tasten.<br/>                                                                                                 |
| <dl> <dt>**Dlgc \_ Wantchars**</dt> <dt>0x0080</dt> </dl>       | [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char) -Nachrichten.<br/>                                                                      |
| <dl> <dt>**Dlgc \_ Wantmessage**</dt> <dt>0x0004</dt> </dl>     | Alle Tastatureingaben (die Anwendung übergibt diese Nachricht in der [**msg**](/windows/win32/api/winuser/ns-winuser-msg) -Struktur an das-Steuerelement).<br/> |
| <dl> <dt>**Dlgc \_ Wanttab**</dt> <dt>0x0002</dt> </dl>         | Tab-Taste.<br/>                                                                                                        |



 

## <a name="remarks"></a>Bemerkungen

Obwohl die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion immer NULL als Antwort auf die **WM- \_ getdlgcode** -Meldung zurückgibt, gibt die Fenster Prozedur für die vordefinierten Steuerelement Klassen einen für jede Klasse geeigneten Code zurück.

Die " **WM \_ getdlgcode** "-Meldung und die zurückgegebenen Werte sind nur für benutzerdefinierte Dialogfeld Steuerelemente oder Standard Steuerelemente hilfreich, die durch Unterklassen geändert werden.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**EM- \_ tsel**](/windows/desktop/Controls/em-setsel)
</dt> <dt>

[**Meldung**](/windows/win32/api/winuser/ns-winuser-msg)
</dt> <dt>

[**WM \_ -Zeichen**](/windows/desktop/inputdev/wm-char)
</dt> <dt>

**Licher**
</dt> <dt>

[Dialog Felder](dialog-boxes.md)
</dt> </dl>

 

