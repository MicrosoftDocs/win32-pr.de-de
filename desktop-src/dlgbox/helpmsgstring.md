---
title: HELPMSGSTRING-Nachricht (Commdlg.h)
description: Ein allgemeines Dialogfeld sendet die registrierte HELPMSGSTRING-Meldung an die Fensterprozedur des Besitzerfensters, wenn der Benutzer auf die Schaltfläche Hilfe klickt.
ms.assetid: 21c0fcf5-785b-4005-8133-e48347f991a8
keywords:
- HELPMSGSTRING-Meldungsdialogfelder
topic_type:
- apiref
api_name:
- HELPMSGSTRING
- HELPMSGSTRINGA
- HELPMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8a446164bb7ae51d36d1a89219f6c3b84eff74b9af3a40c2121b3bd205a581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741740"
---
# <a name="helpmsgstring-message"></a>HELPMSGSTRING-Meldung

Ein allgemeines Dialogfeld sendet die registrierte **HELPMSGSTRING-Meldung** an die Fensterprozedur des Besitzerfensters, wenn der Benutzer auf die Schaltfläche **Hilfe** klickt.


```C++
#define HELPMSGSTRING TEXT("commdlg_help")
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das allgemeine Dialogfeld.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die Initialisierungsstruktur für das allgemeine Dialogfeld. Diese Struktur kann eine [**CHOOSECOLOR-,**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) [**CHOOSEFONT-,**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) [**FINDREPLACE-,**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) [**OPENFILENAME-,**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) [**PRINTDLG-**](/windows/win32/api/commdlg/ns-commdlg-printdlga) oder [**PAGESETUPDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung hat keinen Rückgabewert.

## <a name="remarks"></a>Hinweise

Sie müssen die **HELPMSGSTRING-Konstante** in einem Aufruf der [**RegisterWindowMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) angeben, um den Bezeichner für die vom Dialogfeld gesendete Nachricht zu erhalten.

Verwenden Sie beim Erstellen des Dialogfelds das **hwndOwner-Member** der Initialisierungsstruktur, um das Fenster zum Empfangen von **HELPMSGSTRING-Nachrichten zu** identifizieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Commdlg.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **HELPMSGSTRINGW** (Unicode) und **HELPMSGSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**\_CDN Hilfe**](cdn-help.md)
</dt> <dt>

[**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
</dt> <dt>

[**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Allgemeine Dialogfeldbibliothek](common-dialog-box-library.md)
</dt> </dl>

 

