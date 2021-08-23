---
title: SETRGBSTRING-Nachricht (Commdlg.h)
description: Die Hookprozedur eines Farbdialogfelds, CCHookProc, kann die registrierte SETRGBSTRING-Nachricht an das Dialogfeld senden, um die aktuelle Farbauswahl festzulegen.
ms.assetid: 02d36248-be75-4552-853f-6ac3ec034ebe
keywords:
- DIALOGFELDER FÜR SETRGBSTRING-Meldung
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
ms.openlocfilehash: 8322bb07300ce188684f5097232563e80721fadf0f614c24ac5f7b2d034c1fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985310"
---
# <a name="setrgbstring-message"></a>SETRGBSTRING-Meldung

Die Hookprozedur eines Farbdialogfelds, [*CCHookProc,*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)kann die registrierte **SETRGBSTRING-Nachricht** an das Dialogfeld senden, um die aktuelle Farbauswahl festzulegen. 


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

Der RGB-Wert der Farbe, die im Dialogfeld **Farbe** ausgewählt werden soll. Sie können das [**RGB-Makro**](/windows/desktop/api/wingdi/nf-wingdi-rgb) verwenden, um die Rot-, Grün- und Blau-Intensitäten eines RGB-Farbwerts anzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Hinweise

Wenn *lParam* mit einer der Grundfarben oder einer der 16 benutzerdefinierten Farben übereinstimmt, wählt die Dialogfeldprozedur diese Farbe aus. Die Dialogfeldprozedur aktualisiert auch alle Steuerelemente in der benutzerdefinierten Farberweiterung des Dialogfelds **Farbe,** wenn es geöffnet ist.

Wenn *lParam* nicht mit einer einfachen oder benutzerdefinierten Farbe übereinstimmt, ändert die Dialogfeldprozedur die aktuelle Farbauswahl nicht, aktualisiert jedoch die benutzerdefinierten Farbsteuerelemente, wenn sie sichtbar sind.

## <a name="examples"></a>Beispiele

Der folgende Beispielcode ruft den **SETRGBSTRING-Nachrichtenbezeichner** ab und legt dann die Farbauswahl auf Blau fest.


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
| Header<br/>                   | <dl> <dt>Commdlg.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **SETRGBSTRINGW** (Unicode) und **SETRGBSTRINGA** (ANSI)<br/>                                      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Allgemeine Dialogfeldbibliothek](common-dialog-box-library.md)
</dt> </dl>

 

