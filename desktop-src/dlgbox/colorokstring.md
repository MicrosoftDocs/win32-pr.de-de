---
title: COLOROKSTRING-Nachricht (Commdlg.h)
description: Ein Dialogfeld Farbe sendet die registrierte COLOROKSTRING-Nachricht an Die Hookprozedur CCHookProc, wenn der Benutzer eine Farbe auswählt und auf die Schaltfläche OK klickt.
ms.assetid: 18b28558-1262-4c88-becf-76ce799b7542
keywords:
- DIALOGFELDER FÜR DIE COLOROKSTRING-Meldung
topic_type:
- apiref
api_name:
- COLOROKSTRING
- COLOROKSTRINGA
- COLOROKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd55db4bb935880438290a83cd99c420ebcabf23ca8cb1bb238ea15f39e06247
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726280"
---
# <a name="colorokstring-message"></a>COLOROKSTRING-Nachricht

Ein **Dialogfeld Farbe** sendet die registrierte **COLOROKSTRING-Nachricht** an Die Hookprozedur [*CCHookProc,*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)wenn der Benutzer eine Farbe auswählt und auf die Schaltfläche **OK** klickt. Die Hookprozedur kann die Farbe akzeptieren und das Schließen des Dialogfelds zulassen oder die Farbe ablehnen und erzwingen, dass das Dialogfeld geöffnet bleibt.


```C++
#define COLOROKSTRING TEXT("commdlg_ColorOK")
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**CHOOSECOLOR-Struktur.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) Der **rgbResult-Member** dieser Struktur enthält den RGB-Farbwert der ausgewählten Farbe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Hookprozedur 0 (null) zurückgibt, akzeptiert das Dialogfeld **Farbe** die ausgewählte Farbe und wird geschlossen.

Wenn die Hookprozedur einen Wert ungleich 0 (null) zurückgibt, lehnt das Dialogfeld **Farbe** die ausgewählte Farbe ab und bleibt geöffnet.

## <a name="remarks"></a>Hinweise

Die Hookprozedur muss die **COLOROKSTRING-Konstante** in einem Aufruf der [**RegisterWindowMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) angeben, um den Bezeichner der vom Dialogfeld gesendeten Nachricht abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Commdlg.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **COLOROKSTRINGW** (Unicode) und **COLOROKSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Allgemeine Dialogfeldbibliothek](common-dialog-box-library.md)
</dt> </dl>

 

