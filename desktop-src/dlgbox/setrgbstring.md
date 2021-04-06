---
title: Abmeldung von "sstrgbstring" (kommdlg. h)
description: Die Hook-Prozedur eines Farb Dialogfelds, cchookproc, kann die registrierte setrgbstring-Meldung an das Dialogfeld senden, um die aktuelle Farbauswahl festzulegen.
ms.assetid: 02d36248-be75-4552-853f-6ac3ec034ebe
keywords:
- Dialog Felder "mestrgbstring"
topic_type:
- apiref
api_name:
- SETRGBSTRING
- SETRGBSTRINGA
- SETRGBSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea5489aaa6fafcaa19a97a44d81fd85abb178d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742585"
---
# <a name="setrgbstring-message"></a>"Abmeldung"

Die Hook-Prozedur eines **Farb** Dialogfelds, [*cchookproc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), kann die registrierte **setrgbstring** -Meldung an das Dialogfeld senden, um die aktuelle Farbauswahl festzulegen.


```C++
#define SETRGBSTRING TEXT("commdlg_SetRGBColor")
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Der RGB-Wert der Farbe, die im Dialogfeld **Farbe** ausgewählt werden soll. Sie können das [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) -Makro verwenden, um die roten, grünen und blauen Intensitäten eines RGB-Farbwerts anzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Wenn *LPARAM* mit einer der Grundfarben oder einer der 16 benutzerdefinierten Farben übereinstimmt, wählt die Dialogfeld Prozedur diese Farbe aus. Die Dialogfeld Prozedur aktualisiert auch alle Steuerelemente in der benutzerdefinierten Farb Erweiterung des Dialog Felds **Farbe** , wenn Sie geöffnet ist.

Wenn *LPARAM* nicht mit einer einfachen oder benutzerdefinierten Farbe identisch ist, ändert die Dialogfeld Prozedur nicht die aktuelle Farbauswahl, sondern aktualisiert die benutzerdefinierten Farb Steuerelemente, wenn Sie sichtbar sind.

## <a name="examples"></a>Beispiele

Im folgenden Beispielcode wird der **setrgbstring** -Nachrichten Bezeichner abgerufen und anschließend die Farbauswahl auf Blau festgelegt.


```
UINT uiSetRGB;

uiSetRGB = RegisterWindowMessage(SETRGBSTRING);

SendMessage(hdlg, uiSetRGB, 0, (LPARAM) RGB(0, 0, 255)); 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommdlg. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | " **Btrgbstringw** (Unicode) **" und "** ABl" (ANSI)<br/>                                      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

**Licher**
</dt> <dt>

[Allgemeine Dialog Feld Bibliothek](common-dialog-box-library.md)
</dt> </dl>

 

