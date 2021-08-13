---
title: CDN_FOLDERCHANGE Benachrichtigungscode (Commdlg.h)
description: Wird von einem Dialogfeld im Explorer-Stil geöffnet oder speichern unter gesendet, wenn ein neuer Ordner geöffnet wird.
ms.assetid: 864ab80d-cd99-4dd6-8aff-49beed246e53
keywords:
- Dialogfelder für CDN_FOLDERCHANGE Benachrichtigungscode
topic_type:
- apiref
api_name:
- CDN_FOLDERCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 085d7d0131608ce70a1e023130159b270a679c968a548062645b32cd5cd10204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786140"
---
# <a name="cdn_folderchange-notification-code"></a>\_CDN FOLDERCHANGE-Benachrichtigungscode

\[Ab Windows Vista wurden die Dialogfelder **Öffnen** und **Speichern unter** durch das [Dialogfeld "Allgemeines Element"](../shell/common-file-dialog.md)ersetzt. Es wird empfohlen, die DIALOGFELD-API für allgemeine Elemente anstelle dieser Dialogfelder aus der Common Dialog Box Library zu verwenden.\]

Wird von einem Dialogfeld im Explorer-Stil **geöffnet** oder **speichern unter** gesendet, wenn ein neuer Ordner geöffnet wird.

Ihre [*OFNHookProc-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) empfängt diese Nachricht in Form einer [**WM \_ NOTIFY-Nachricht.**](../controls/wm-notify.md)


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FOLDERCHANGE        (CDN_FIRST - 0x0002)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**OFNOTIFY-Struktur.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) Die **OFNOTIFY-Struktur** enthält eine [**NMHDR-Struktur,**](/windows/win32/api/richedit/ns-richedit-nmhdr) deren **Codemember** die **CDN FOLDERCHANGE-Benachrichtigungsmeldung \_** angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Hinweise

Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mit dem **\_ OFN-EXPLORER-Wert** erstellt wurde.

Um den Pfad des neu geöffneten Ordners abzurufen, kann die Hookprozedur die [**CDM \_ GETFOLDERPATH-Nachricht**](cdm-getfolderpath.md) an das Dialogfeld senden.

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

[**CDM \_ GETFOLDERPATH**](cdm-getfolderpath.md)
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Allgemeine Dialogfeldbibliothek](common-dialog-box-library.md)
</dt> </dl>

