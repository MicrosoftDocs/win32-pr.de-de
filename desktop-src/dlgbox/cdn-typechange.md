---
title: CDN_TYPECHANGE Benachrichtigungs Code (kommdlg. h)
description: Wird von einem Explorer-Dialogfeld "Öffnen" oder "Speichern unter" gesendet, wenn der Benutzer einen neuen Dateityp aus dem Kombinations Feld "Dateitypen" auswählt.
ms.assetid: fb8324db-e435-4ef2-aac5-506a6b7adb2c
keywords:
- Dialog Felder für CDN_TYPECHANGE Benachrichtigungs Code
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
ms.openlocfilehash: 64226c1ac15cb6b55c6c2e2de7264d726e6f3a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476674"
---
# <a name="cdn_typechange-notification-code"></a>CDN \_ typechange-Benachrichtigungs Code

\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt. Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]

Wird von einem Explorer-Dialogfeld " **Öffnen** " oder " **Speichern** unter" gesendet, wenn der Benutzer einen neuen Dateityp aus dem Kombinations Feld "Dateitypen" auswählt.

Die [*ofnhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) -Hook-Prozedur empfängt diese Nachricht in Form einer [**WM- \_ Benachrichtigungs**](../controls/wm-notify.md) Meldung.


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

Ein Zeiger auf eine [**ofnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) -Struktur.

Die [**ofnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) -Struktur enthält eine [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) -Struktur, deren **Codemember** die **CDN- \_ typechange** -Benachrichtigungs Meldung angibt.

Die [**ofnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) -Struktur enthält auch einen Zeiger auf eine [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur, deren **nfilterindex** -Member den 1-basierten Index des neu ausgewählten Dateityp Filters angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mit dem Wert des **ofn- \_ Explorers** erstellt wurde.

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

**Licher**
</dt> <dt>

[Allgemeine Dialog Feld Bibliothek](common-dialog-box-library.md)
</dt> </dl>

 

