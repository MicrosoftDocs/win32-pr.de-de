---
title: CDN_TYPECHANGE Benachrichtigungscode (Commdlg.h)
description: Wird von einem Dialogfeld im Explorer-Stil geöffnet oder speichern unter gesendet, wenn der Benutzer einen neuen Dateityp aus dem Kombinationsfeld "Dateitypen" auswählt.
ms.assetid: fb8324db-e435-4ef2-aac5-506a6b7adb2c
keywords:
- Dialogfelder für CDN_TYPECHANGE Benachrichtigungscode
topic_type:
- apiref
api_name:
- CDN_TYPECHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf55584aafd5c73ee3ec2b756b59054e8aabaaf4cf5974a09dd11d3b4f40b655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504188"
---
# <a name="cdn_typechange-notification-code"></a>\_CDN TYPECHANGE-Benachrichtigungscode

\[Ab Windows Vista wurden die Dialogfelder **Öffnen** und **Speichern unter** durch das [Dialogfeld "Allgemeines Element"](../shell/common-file-dialog.md)ersetzt. Es wird empfohlen, die DIALOGFELD-API für allgemeine Elemente anstelle dieser Dialogfelder aus der Common Dialog Box Library zu verwenden.\]

Wird von einem Dialogfeld im Explorer-Stil **geöffnet** oder **speichern unter** gesendet, wenn der Benutzer einen neuen Dateityp aus dem Kombinationsfeld "Dateitypen" auswählt.

Ihre [*OFNHookProc-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) empfängt diese Nachricht in Form einer [**WM \_ NOTIFY-Nachricht.**](../controls/wm-notify.md)


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_TYPECHANGE          (CDN_FIRST - 0x0006)
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

Die [**OFNOTIFY-Struktur**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) enthält eine [**NMHDR-Struktur,**](/windows/win32/api/richedit/ns-richedit-nmhdr) deren **Codemember** die **CDN TYPECHANGE-Benachrichtigungsmeldung \_** angibt.

Die [**OFNOTIFY-Struktur**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) enthält auch einen Zeiger auf eine [**OPENFILENAME-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) deren **nFilterIndex-Member** den einsbasierten Index des neu ausgewählten Dateitypfilters angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Hinweise

Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mit dem **\_ OFN-EXPLORER-Wert** erstellt wurde.

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

**Konzeptionellen**
</dt> <dt>

[Allgemeine Dialogfeldbibliothek](common-dialog-box-library.md)
</dt> </dl>

