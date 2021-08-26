---
title: WM_GETDLGCODE (Winuser.h)
description: Wird an die einem -Steuerelement zugeordnete Fensterprozedur gesendet.
ms.assetid: 96d2caee-be6e-46e9-98b3-bffc3af1c003
keywords:
- WM_GETDLGCODE-Dialogfelder
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
ms.openlocfilehash: 10d9ef69c2a6e89154cd6d931e05f9e52b4c51b214319bca8dffa9f86786a3da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022190"
---
# <a name="wm_getdlgcode-message"></a>WM \_ GETDLGCODE-Nachricht

Wird an die einem -Steuerelement zugeordnete Fensterprozedur gesendet. Standardmäßig verarbeitet das System alle Tastatureingaben für das Steuerelement. das System interpretiert bestimmte Arten von Tastatureingaben als Navigationsschlüssel für Dialogfelder. Um dieses Standardverhalten zu überschreiben, kann das Steuerelement auf die **WM \_ GETDLGCODE-Nachricht** antworten, um die Eingabetypen anzugeben, die es selbst verarbeiten möchte.


```C++
#define WM_GETDLGCODE                   0x0087
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die virtuelle Taste, die vom Benutzer gedrückt wird, die Windows aufforderungt, diese Benachrichtigung aus zu geben. Der Handler muss diese Schlüssel selektiv behandeln. Beispielsweise kann der Handler **VK \_ RETURN** akzeptieren und verarbeiten, aber **die VK-TAB-Taste \_** an das Besitzerfenster delegieren. Eine Liste der Werte finden Sie unter [**Codes für virtuelle Schlüssel.**](/windows/desktop/inputdev/virtual-key-codes)

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**MSG-Struktur**](/windows/win32/api/winuser/ns-winuser-msg) (oder **NULL,** wenn das System eine Abfrage vorgibt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist mindestens einer der folgenden Werte, der angibt, welche Art von Eingabe die Anwendung verarbeitet.



| Rückgabecode/-wert                                                                                                                                                | BESCHREIBUNG                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DLGC \_ SCHALTFLÄCHE**</dt> <dt>0X2000</dt> </dl>          | Schaltfläche.<br/>                                                                                                         |
| <dl> <dt>**DLGC \_ DEFPUSHBUTTON-0x0010**</dt> <dt></dt> </dl>   | Standard-Pushschaltfläche.<br/>                                                                                            |
| <dl> <dt>**DLGC \_ HASSETSEL-0x0008**</dt> <dt></dt> </dl>       | [**EM \_ SETSEL-Meldungen.**](/windows/desktop/Controls/em-setsel)<br/>                                                           |
| <dl> <dt>**DLGC \_ RADIOBUTTON-0x0040**</dt> <dt></dt> </dl>     | Optionsfeld.<br/>                                                                                                   |
| <dl> <dt>**DLGC \_ STATIC**</dt> <dt>0x0100</dt> </dl>          | Statisches Steuerelement.<br/>                                                                                                 |
| <dl> <dt>**DLGC \_ UNDEFPUSHBUTTON-0x0020**</dt> <dt></dt> </dl> | Nicht standardmäßige Pushschaltfläche.<br/>                                                                                        |
| <dl> <dt>**DLGC \_ WANTALLKEYS**</dt> <dt>0x0004</dt> </dl>     | Alle Tastatureingaben.<br/>                                                                                             |
| <dl> <dt>**DLGC \_ WANTWS-0x0001**</dt> <dt></dt> </dl>      | Richtungsschlüssel.<br/>                                                                                                 |
| <dl> <dt>**DLGC \_ WANTCHARS-0x0080**</dt> <dt></dt> </dl>       | [**WM \_ CHAR-Meldungen.**](/windows/desktop/inputdev/wm-char)<br/>                                                                      |
| <dl> <dt>**DLGC \_ WANTMESSAGE-0x0004**</dt> <dt></dt> </dl>     | Alle Tastatureingaben (die Anwendung übergibt diese Meldung in der [**MSG-Struktur**](/windows/win32/api/winuser/ns-winuser-msg) an das Steuerelement).<br/> |
| <dl> <dt>**DLGC \_ WANTTAB-0x0002**</dt> <dt></dt> </dl>         | TAB-TASTE.<br/>                                                                                                        |



 

## <a name="remarks"></a>Hinweise

Obwohl die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) als Antwort auf die **WM \_ GETDLGCODE-Nachricht** immer 0 (null) zurückgibt, gibt die Fensterprozedur für die vordefinierten Steuerelementklassen einen Code zurück, der für jede Klasse geeignet ist.

Die **WM \_ GETDLGCODE-Nachricht** und die zurückgegebenen Werte sind nur bei benutzerdefinierten Dialogfeld-Steuerelementen oder Standardsteuerelementen nützlich, die durch Unterklassen geändert wurden.

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

[**EM \_ SETSEL**](/windows/desktop/Controls/em-setsel)
</dt> <dt>

[**Msg**](/windows/win32/api/winuser/ns-winuser-msg)
</dt> <dt>

[**WM \_ CHAR**](/windows/desktop/inputdev/wm-char)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Dialogfelder](dialog-boxes.md)
</dt> </dl>

 

