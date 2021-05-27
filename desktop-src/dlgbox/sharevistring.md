---
title: SHAREVISTRING-Nachricht (Commdlg.h)
description: Ein Dialogfeld Öffnen oder Speichern unter sendet die registrierte SHAREVISTRING-Nachricht an Ihre Hookprozedur OFNHookProc, wenn ein Freigabeverstoß für die ausgewählte Datei auftritt, wenn der Benutzer auf die Schaltfläche OK klickt.
ms.assetid: 53884497-4872-4aa8-b56e-2bb98df58fed
keywords:
- SHAREVISTRING-Meldungsdialogfelder
topic_type:
- apiref
api_name:
- SHAREVISTRING
- SHAREVISTRINGA
- SHAREVISTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 043bed9edd08269e4e030482cbd44debea3a3695
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548765"
---
# <a name="sharevistring-message"></a>SHAREVISTRING-Nachricht

\[Ab Windows Vista wurden  **die** allgemeinen Dialogfelder Öffnen und Speichern unter durch den Allgemeinen [Elementdialog ersetzt.](../shell/common-file-dialog.md) Es wird empfohlen, anstelle dieser Dialogfelder aus der Common Dialog Box Library die API für den Allgemeinen Elementdialog zu verwenden.\]

Ein **Dialogfeld** Öffnen oder Speichern unter sendet die registrierte **SHAREVISTRING-Nachricht** an Ihre Hookprozedur [*OFNHookProc,*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)wenn ein Freigabeverstoß für die ausgewählte Datei auftritt, wenn der Benutzer auf die Schaltfläche **OK** klickt. 


```C++
#define SHAREVISTRING TEXT("commdlg_ShareViolation")
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**OPENFILENAME-Struktur.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) Das **lpstrFile-Member** dieser Struktur enthält den Dateinamen, der den Freigabeverstoß verursacht hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Hookprozedur muss einen der folgenden Werte zurückgeben, um anzugeben, wie das Dialogfeld den Freigabeverstoß behandeln soll.



| Rückgabecode/-wert                                                                                                                                           | Beschreibung                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt> </dl> | Akzeptieren des Dateinamens<br/>                                                                                            |
| <dl> <dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt> </dl>      | Lehnen Sie den Dateinamen ab, aber warnen Sie den Benutzer nicht. Die Anwendung ist dafür verantwortlich, eine Warnmeldung anzuzeigen.<br/> |
| <dl> <dt>**OFN \_ SHAREWARN**</dt> <dt>0</dt> </dl>        | Lehnen Sie den Dateinamen ab, und zeigt eine Warnmeldung an (das gleiche Ergebnis wie bei einer Hookprozedur).<br/>       |



 

## <a name="remarks"></a>Hinweise

Die Hookprozedur muss die **SHAREVISTRING-Konstante** in einem Aufruf der [**RegisterWindowMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) angeben, um den Bezeichner für die vom Dialogfeld gesendete Nachricht zu erhalten.

Das Dialogfeld sendet die registrierte **SHAREVISTRING-Nachricht** nur, wenn Sie beim Erstellen des Dialogfelds das **OFN \_ SHAREAWARE-Flag** nicht im **Flags-Member** der [**OPENFILENAME-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) angegeben haben.

Wenn die Hookprozedur einen nicht definierten Wert zurückgibt, antwortet das Dialogfeld so, als ob **OFN \_ SHAREWARN** zurückgegeben würde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Commdlg.h (windows.h einschließen)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **SHAREVISTRINGW** (Unicode) und **SHAREVISTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**CDN \_ SHAREVIOLATION**](cdn-shareviolation.md)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Allgemeine Dialogfeldbibliothek](common-dialog-box-library.md)
</dt> </dl>

