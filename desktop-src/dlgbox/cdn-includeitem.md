---
title: CDN_INCLUDEITEM Benachrichtigungs Code (kommdlg. h)
description: Wird von einem Dialogfeld "Öffnen" oder "Speichern unter" gesendet, um zu bestimmen, ob das Dialogfeld ein Element in der Elementliste eines shellordners anzeigen soll.
ms.assetid: 0972a78d-e058-4bac-85bd-fbd4c3885552
keywords:
- Dialog Felder für CDN_INCLUDEITEM Benachrichtigungs Code
topic_type:
- apiref
api_name:
- CDN_INCLUDEITEM
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67cbe830c644657425eb087dd64884da17a9a0c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742848"
---
# <a name="cdn_includeitem-notification-code"></a>CDN \_ includeitem-Benachrichtigungs Code

\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt. Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]

Wird von einem Dialogfeld " **Öffnen** " oder " **Speichern** unter" gesendet, um zu bestimmen, ob das Dialogfeld ein Element in der Elementliste eines shellordners anzeigen soll. Wenn der Benutzer einen Ordner öffnet, sendet das Dialogfeld für jedes Element im Ordner eine **CDN- \_ includeitem** -Benachrichtigung. Das Dialogfeld sendet diese Benachrichtigung nur dann, wenn das **ofn \_ enableinclubezeichtifisflag** beim Erstellen des Dialog Felds festgelegt wurde.

Die [*ofnhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) -Hook-Prozedur empfängt diese Nachricht in Form einer [**WM- \_ Benachrichtigungs**](../controls/wm-notify.md) Meldung.


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INCLUDEITEM         (CDN_FIRST - 0x0007)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**ofnotifyex**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) -Struktur.

Die [**ofnotifyex**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) -Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, deren **Codemember** die **CDN \_ includeitem** -Benachrichtigungs Meldung angibt.

Der **PSF** -Member der [**ofnotifyex**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) -Struktur ist ein Zeiger auf eine Schnittstelle für den Ordner, dessen Elemente aufgelistet werden. Der **PIDL** -Member ist ein Zeiger auf eine Element Bezeichner-Liste, die das Element relativ zum Ordner identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die [*ofnhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) -Hook-Prozedur NULL zurückgibt, schließt das Dialogfeld das Element aus der Liste der Elemente aus.

Um das Element einzuschließen, geben Sie einen Wert ungleich 0 (null) von der Hook-Prozedur zurück.

## <a name="remarks"></a>Bemerkungen

Das Dialogfeld enthält immer Elemente, die sowohl das **sfgao- \_ Dateisystem** als auch das **sfgao \_ filesysancestor** -Attribut aufweisen, unabhängig von dem Wert, der von **CDN \_ includeitem** zurückgegeben wird.

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

[**Ofnotifyex**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)
</dt> <dt>

**Licher**
</dt> <dt>

[Allgemeine Dialog Feld Bibliothek](common-dialog-box-library.md)
</dt> </dl>

 

