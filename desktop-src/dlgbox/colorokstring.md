---
title: Colorokstring-Nachricht (kommdlg. h)
description: Ein Farb Dialogfeld sendet die registrierte colorokstring-Nachricht an die Hook-Prozedur cchookproc, wenn der Benutzer eine Farbe auswählt und auf die Schaltfläche OK klickt.
ms.assetid: 18b28558-1262-4c88-becf-76ce799b7542
keywords:
- Colorokstring-Meldungs Dialogfelder
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
ms.openlocfilehash: 86229c71f1234efb4b561ac73bc8aa20f6258cdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103647"
---
# <a name="colorokstring-message"></a>Colorokstring-Meldung

Ein **Farb** Dialogfeld sendet die registrierte **colorokstring** -Nachricht an die Hook-Prozedur [*cchookproc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), wenn der Benutzer eine Farbe auswählt und auf die Schaltfläche **OK** klickt. Die Hook-Prozedur kann die Farbe annehmen und zulassen, dass das Dialogfeld geschlossen wird, oder die Farbe ablehnen und erzwingen, dass das Dialogfeld geöffnet bleibt.


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

Ein Zeiger auf eine [**chooon Color**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) -Struktur. Der **rgbresult** -Member dieser Struktur enthält den RGB-Farbwert der ausgewählten Farbe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Hook-Prozedur 0 (null) zurückgibt, wird das Dialogfeld **Farbe** die ausgewählte Farbe annehmen und geschlossen.

Wenn die Hook-Prozedur einen Wert ungleich 0 (null) zurückgibt, lehnt das Dialogfeld **Farbe** die ausgewählte Farbe ab und bleibt geöffnet.

## <a name="remarks"></a>Bemerkungen

Die Hook-Prozedur muss die **colorokstring** -Konstante in einem Aufrufen der [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion angeben, um den Bezeichner der vom Dialogfeld gesendeten Nachricht abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommdlg. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Colorokstringw** (Unicode) und **colorokstraninga** (ANSI)<br/>                                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Licher**
</dt> <dt>

[Allgemeine Dialog Feld Bibliothek](common-dialog-box-library.md)
</dt> </dl>

 

