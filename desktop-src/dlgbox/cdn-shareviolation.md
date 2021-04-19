---
title: CDN_SHAREVIOLATION Benachrichtigungs Code (kommdlg. h)
description: Wird von einem Explorer-Dialogfeld "Öffnen" oder "Speichern unter" gesendet, wenn der Benutzer auf die Schaltfläche "OK" klickt und eine Netzwerkfreigabe Verletzung für die ausgewählte Datei auftritt.
ms.assetid: a62ca550-0997-4379-aaaf-a5bc9414bd69
keywords:
- Dialog Felder für CDN_SHAREVIOLATION Benachrichtigungs Code
topic_type:
- apiref
api_name:
- CDN_SHAREVIOLATION
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acfa3a91e9c84f15984285f99d071fcde24a4d66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339967"
---
# <a name="cdn_shareviolation-notification-code"></a>CDN- \_ shareverletzungs-Benachrichtigungs Code

\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt. Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]

Wird von einem Explorer-Dialogfeld " **Öffnen** " oder " **Speichern** unter" gesendet, wenn der Benutzer auf die Schaltfläche " **OK** " klickt und eine Netzwerkfreigabe Verletzung für die ausgewählte Datei auftritt.

Die [*ofnhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) -Hook-Prozedur empfängt diese Nachricht in Form einer [**WM- \_ Benachrichtigungs**](../controls/wm-notify.md) Meldung.


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_SHAREVIOLATION      (CDN_FIRST - 0x0003)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**ofnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) -Struktur. Der **pszFile** -Member dieser Struktur ist ein Zeiger auf den Namen der Datei mit der Freigabe Verletzung. Die **ofnotify** -Struktur enthält eine [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) -Struktur, deren **Codemember** die **CDN \_ shareverletzungs** -Benachrichtigungs Meldung angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert gibt an, wie das Dialogfeld die Freigabe Verletzung behandeln soll.

Wenn die Hook-Prozedur NULL zurückgibt, wird im Dialogfeld die Standard Warnmeldung für eine Freigabe Verletzung angezeigt.

Wenn Sie die Anzeige der Standard Warnmeldung verhindern möchten, geben Sie einen Wert ungleich 0 (null) von der Hookprozedur zurück, und geben Sie die Funktion [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) an, um einen der folgenden **DWL- \_ msgresult** -Werte festzulegen.



| Rückgabecode/-wert                                                                                                                                           | BESCHREIBUNG                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Ofn \_ Sharefallthrough**</dt> <dt>2</dt> </dl> | Bewirkt, dass im Dialogfeld der Dateiname zurückgegeben wird, ohne dass der Benutzer die Freigabe Verletzung warnt.<br/>  |
| <dl> <dt>**Ofn \_ Sharenowarn**</dt> <dt>1</dt> </dl>      | Bewirkt, dass im Dialogfeld der Dateiname abgelehnt wird, ohne dass der Benutzer über die Freigabe Verletzung gewarnt werden muss. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mit dem Wert des **ofn- \_ Explorers** erstellt wurde.

Das System sendet diese Benachrichtigung nur dann, wenn beim Erstellen des Dialog Felds kein Wert für " **\_ shareaware** " angegeben wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommdlg. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*Ofnhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**Ofnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**Licher**
</dt> <dt>

[Allgemeine Dialog Feld Bibliothek](common-dialog-box-library.md)
</dt> </dl>

 

