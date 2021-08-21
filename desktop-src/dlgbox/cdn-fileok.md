---
title: CDN_FILEOK Benachrichtigungscode (Commdlg.h)
description: Wird von einem Dialogfeld Im Explorer-Stil öffnen oder speichern unter gesendet, wenn der Benutzer einen Dateinamen angibt und auf die Schaltfläche OK klickt.
ms.assetid: 7f3de96f-68d8-4f40-b74f-304835f9def2
keywords:
- CDN_FILEOK Benachrichtigungscode (Dialogfelder)
topic_type:
- apiref
api_name:
- CDN_FILEOK
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e32e9b4abbae65c2c29020bdab191272921ee601eebff1e7b07e0c674c783dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787420"
---
# <a name="cdn_fileok-notification-code"></a>\_CDN FILEOK-Benachrichtigungscode

Wird von einem  Dialogfeld Im Explorer-Stil öffnen oder speichern **unter** gesendet, wenn der Benutzer einen Dateinamen angibt und auf die **Schaltfläche OK** klickt.

Ihre [*OFNHookProc-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) empfängt diese Nachricht in Form einer [**WM \_ NOTIFY-Nachricht.**](../controls/wm-notify.md)


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FILEOK              (CDN_FIRST - 0x0005)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**OFNOTIFY-Struktur.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)

Die [**OFNOTIFY-Struktur**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) enthält eine [**NMHDR-Struktur,**](/windows/win32/api/richedit/ns-richedit-nmhdr) deren Code **member** die CDN **\_ FILEOK-Benachrichtigungsmeldung** angibt.

Die [**OFNOTIFY-Struktur**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) enthält auch einen Zeiger auf eine [**OPENFILENAME-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) deren **lpstrFile-Member** die Adresse des ausgewählten Dateinamens angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Hookprozedur 0 (null) zurückgibt, akzeptiert das Dialogfeld den angegebenen Dateinamen und wird geschlossen.

Um den angegebenen Dateinamen abzulehnen und zu erzwingen, dass das Dialogfeld geöffnet bleibt, geben Sie einen Wert ungleich 0 (null) aus der Hookprozedur zurück, und rufen Sie die [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) auf, um einen **\_ MSGRESULT-Wert** ungleich 0 (null) festzulegen.

## <a name="remarks"></a>Hinweise

Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mithilfe des **\_ OFN-EXPLORER-Werts erstellt** wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Commdlg.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
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
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM \_ NOTIFY**](../controls/wm-notify.md)
</dt> </dl>

 

