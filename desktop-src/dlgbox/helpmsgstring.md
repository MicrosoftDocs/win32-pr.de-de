---
title: Helpmsgstring-Nachricht (kommdlg. h)
description: Ein häufig verwendeter Dialogfeld sendet die registrierte helpmsgstring-Meldung an die Fenster Prozedur des Besitzer Fensters, wenn der Benutzer auf die Schaltfläche Hilfe klickt.
ms.assetid: 21c0fcf5-785b-4005-8133-e48347f991a8
keywords:
- Helpmsgstring-Meldungs Dialogfelder
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
ms.openlocfilehash: ac3f7a883f50b06c8d142cb83bedf0bfa2920191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106011"
---
# <a name="helpmsgstring-message"></a>Helpmsgstring-Meldung

Ein häufig verwendeter Dialogfeld sendet die registrierte **helpmsgstring** -Meldung an die Fenster Prozedur des Besitzer Fensters, wenn der Benutzer auf die Schaltfläche **Hilfe** klickt.


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

Ein Zeiger auf die Initialisierungs Struktur für das allgemeine Dialogfeld. Bei [**dieser Struktur kann**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) es sich um eine " [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)"-, " [**choosefont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)"-, " [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)"-, " [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)"-, " [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) "-

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Sie müssen die **helpmsgstring** -Konstante in einem Aufrufen der [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion angeben, um den Bezeichner für die vom Dialogfeld gesendete Nachricht abzurufen.

Wenn Sie das Dialogfeld erstellen, verwenden Sie den **hwndOwner** -Member der Initialisierungs Struktur, um das Fenster für den Empfang von **helpmsgstring** -Nachrichten zu identifizieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommdlg. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Helpmsgstringw** (Unicode) und **helpmsgstrauinga** (ANSI)<br/>                                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**CDN- \_ Hilfe**](cdn-help.md)
</dt> <dt>

[**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
</dt> <dt>

[**Pagesetupdlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Licher**
</dt> <dt>

[Allgemeine Dialog Feld Bibliothek](common-dialog-box-library.md)
</dt> </dl>

 

