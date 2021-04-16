---
title: Sharevistring-Nachricht (kommdlg. h)
description: Ein Dialogfeld zum Öffnen oder speichern unter sendet die registrierte sharevistring-Nachricht an die Hook-Prozedur ofnhuokproc, wenn eine Freigabe Verletzung für die ausgewählte Datei auftritt, wenn der Benutzer auf die Schaltfläche OK klickt.
ms.assetid: 53884497-4872-4aa8-b56e-2bb98df58fed
keywords:
- Share Message String-Meldungs Dialogfelder
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
ms.openlocfilehash: c23c17280ad1156e35f7e0f503816c07645cf4f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477979"
---
# <a name="sharevistring-message"></a>Sharevistring-Meldung

\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt. Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]

Ein Dialogfeld zum **Öffnen** oder **Speichern** unter sendet die registrierte **sharevistring** -Nachricht an die Hook-Prozedur [*ofnhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), wenn eine Freigabe Verletzung für die ausgewählte Datei auftritt, wenn der Benutzer auf die Schaltfläche **OK** klickt.


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

Ein Zeiger auf eine [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur. Der **lpstraufile** -Member dieser Struktur enthält den Dateinamen, der die Freigabe Verletzung verursacht hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Hook-Prozedur muss einen der folgenden Werte zurückgeben, um anzugeben, wie das Dialogfeld die Freigabe Verletzung behandeln soll.



| Rückgabecode/-wert                                                                                                                                           | BESCHREIBUNG                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Ofn \_ Sharefallthrough**</dt> <dt>2</dt> </dl> | Dateiname akzeptieren<br/>                                                                                            |
| <dl> <dt>**Ofn \_ Sharenowarn**</dt> <dt>1</dt> </dl>      | Ablehnen Sie den Dateinamen, aber warnen Sie den Benutzer nicht. Die Anwendung ist dafür verantwortlich, eine Warnmeldung anzuzeigen.<br/> |
| <dl> <dt>**Ofn \_ Sharewarn**</dt> <dt>0</dt> </dl>        | Ablehnen Sie den Dateinamen, und zeigt eine Warnmeldung an (das gleiche Ergebnis wie bei keiner Hook-Prozedur).<br/>       |



 

## <a name="remarks"></a>Bemerkungen

Die Hook-Prozedur muss die **sharevistring** -Konstante in einem Aufrufen der [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion angeben, um den Bezeichner für die vom Dialogfeld gesendete Nachricht abzurufen.

Das Dialogfeld sendet die registrierte **sharevistring** -Nachricht nur dann, wenn Sie beim Erstellen des Dialog Felds nicht das **ofn \_ shareaware** -Flag im **Flags** -Member der [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur angegeben haben.

Wenn die Hook-Prozedur einen nicht definierten Wert zurückgibt, antwortet das Dialogfeld so, als ob **ofn \_ sharewarn** zurückgegeben wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommdlg. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Sharevistringw** (Unicode) und **shareviampinga** (ANSI)<br/>                                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**CDN- \_ share-Verletzung**](cdn-shareviolation.md)
</dt> <dt>

[**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Licher**
</dt> <dt>

[Allgemeine Dialog Feld Bibliothek](common-dialog-box-library.md)
</dt> </dl>

 

