---
title: CDN_SHAREVIOLATION Benachrichtigungscode (Commdlg.h)
description: Wird von einem Dialogfeld Im Explorer-Stil öffnen oder speichern unter gesendet, wenn der Benutzer auf die Schaltfläche OK klickt und für die ausgewählte Datei ein Verstoß gegen die Netzwerkfreigabe auftritt.
ms.assetid: a62ca550-0997-4379-aaaf-a5bc9414bd69
keywords:
- CDN_SHAREVIOLATION Benachrichtigungscode (Dialogfelder)
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
ms.openlocfilehash: 6e79d9c48d3e80d14d83de07c03f7db119ea8e78
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590697"
---
# <a name="cdn_shareviolation-notification-code"></a>CDN \_ SHAREVIOLATION-Benachrichtigungscode

\[Ab Windows Vista wurden  **die** allgemeinen Dialogfelder Öffnen und Speichern unter durch den Allgemeinen [Elementdialog ersetzt.](/windows/win32/shell/common-file-dialog) Es wird empfohlen, anstelle dieser Dialogfelder aus der Common Dialog Box Library die API für den Allgemeinen Elementdialog zu verwenden.\]

Wird über das  Dialogfeld  Öffnen oder Speichern unter im Explorer-Stil gesendet, wenn der Benutzer auf die Schaltfläche **OK** klickt und für die ausgewählte Datei ein Verstoß gegen die Netzwerkfreigabe auftritt.

Ihre [*OFNHookProc-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) empfängt diese Nachricht in Form einer [**WM \_ NOTIFY-Nachricht.**](../controls/wm-notify.md)


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

Ein Zeiger auf eine [**OFNOTIFY-Struktur.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) Der **pszFile-Member** dieser -Struktur ist ein Zeiger auf den Namen der Datei, die den Freigabeverstoß hatte. Die **OFNOTIFY-Struktur** enthält eine [**NMHDR-Struktur,**](/windows/win32/api/richedit/ns-richedit-nmhdr) deren **Code** member die **CDN \_ SHAREVIOLATION-Benachrichtigungsmeldung** angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert gibt an, wie das Dialogfeld den Freigabeverstoß behandeln soll.

Wenn die Hookprozedur 0 (null) zurückgibt, wird im Dialogfeld die Standardwarnmeldung für einen Freigabeverstoß angezeigt.

Um die Anzeige der Standardwarnmeldung zu verhindern, geben Sie einen Wert ungleich 0 (null) aus der Hookprozedur zurück, und rufen Sie die [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) auf, um einen der folgenden **\_ MSGRESULT-DWL-Werte** zu setzen.



| Rückgabecode/-wert                                                                                                                                           | Beschreibung                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt> </dl> | Bewirkt, dass das Dialogfeld den Dateinamen zurück gibt, ohne den Benutzer vor dem Freigabeverstoß zu warnen.<br/>  |
| <dl> <dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt> </dl>      | Bewirkt, dass das Dialogfeld den Dateinamen zurückweisen kann, ohne den Benutzer vor dem Freigabeverstoß zu warnen. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mit dem **\_ OFN-EXPLORER-Wert** erstellt wurde.

Das System sendet diese Benachrichtigung nur, wenn der **OFN \_ SHAREAWARE-Wert** beim Erstellen des Dialogfelds nicht angegeben wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Commdlg.h (windows.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Verweis**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Allgemeine Dialogfeldbibliothek](common-dialog-box-library.md)
</dt> </dl>

 

