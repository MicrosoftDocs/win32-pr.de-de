---
title: CDN_TYPECHANGE Benachrichtigungscode (Commdlg.h)
description: Wird über das Dialogfeld Öffnen oder Speichern unter im Explorer-Stil gesendet, wenn der Benutzer im Kombinationsfeld Dateitypen einen neuen Dateityp auswählt.
ms.assetid: fb8324db-e435-4ef2-aac5-506a6b7adb2c
keywords:
- CDN_TYPECHANGE Benachrichtigungscode (Dialogfelder)
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
ms.openlocfilehash: 180a16c32fb6e83ea0b17e38b42ce8c729f7685a
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590807"
---
# <a name="cdn_typechange-notification-code"></a>CDN \_ TYPECHANGE-Benachrichtigungscode

\[Ab Windows Vista wurden  **die** allgemeinen Dialogfelder Öffnen und Speichern unter durch den Allgemeinen [Elementdialog ersetzt.](/windows/win32/shell/common-file-dialog) Es wird empfohlen, anstelle dieser Dialogfelder aus der Common Dialog Box Library die API für den Allgemeinen Elementdialog zu verwenden.\]

Wird über das  Dialogfeld  Öffnen oder Speichern unter im Explorer-Stil gesendet, wenn der Benutzer im Kombinationsfeld Dateitypen einen neuen Dateityp auswählt.

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

Die [**OFNOTIFY-Struktur**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) enthält eine [**NMHDR-Struktur,**](/windows/win32/api/richedit/ns-richedit-nmhdr) deren **Code** member die **CDN \_ TYPECHANGE-Benachrichtigungsmeldung** angibt.

Die [**OFNOTIFY-Struktur**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) enthält auch einen Zeiger auf eine [**OPENFILENAME-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) deren **nFilterIndex-Member** den einbasierten Index des neu ausgewählten Dateitypfilters angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung hat keinen Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mithilfe des **\_ OFN-EXPLORER-Werts erstellt** wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Commdlg.h (einschließlich Windows.h)</dt> </dl> |



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

**Konzeptionellen**
</dt> <dt>

[Allgemeine Dialogfeldbibliothek](common-dialog-box-library.md)
</dt> </dl>

 

