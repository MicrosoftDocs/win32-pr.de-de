---
title: CDN_INCLUDEITEM Benachrichtigungscode (Commdlg.h)
description: Wird über das Dialogfeld Öffnen oder Speichern unter gesendet, um zu bestimmen, ob im Dialogfeld ein Element in der Elementliste eines Shellordners angezeigt werden soll.
ms.assetid: 0972a78d-e058-4bac-85bd-fbd4c3885552
keywords:
- CDN_INCLUDEITEM Benachrichtigungscode (Dialogfelder)
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
ms.openlocfilehash: 445ea8626d7ecc6c1c72cd13eebfc9811ae229b772787eae2625224d830bc25e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721078"
---
# <a name="cdn_includeitem-notification-code"></a>\_CDN INCLUDEITEM-Benachrichtigungscode

\[Ab Windows Vista wurden **die** allgemeinen  Dialogfelder Öffnen und Speichern unter durch den Allgemeinen [Elementdialog ersetzt.](../shell/common-file-dialog.md) Es wird empfohlen, anstelle dieser Dialogfelder aus der Common Dialog Box Library die API für den Allgemeinen Elementdialog zu verwenden.\]

Wird über das **Dialogfeld Öffnen** oder Speichern **unter** gesendet, um zu bestimmen, ob im Dialogfeld ein Element in der Elementliste eines Shellordners angezeigt werden soll. Wenn der Benutzer einen Ordner öffnet, sendet das Dialogfeld eine CDN **\_ INCLUDEITEM-Benachrichtigung** für jedes Element im Ordner. Das Dialogfeld sendet diese Benachrichtigung nur, wenn das **OFN \_ ENABLEINCLUDENOTIFY-Flag** beim Erstellen des Dialogfelds festgelegt wurde.

Ihre [*OFNHookProc-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) empfängt diese Nachricht in Form einer [**WM \_ NOTIFY-Nachricht.**](../controls/wm-notify.md)


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

Ein Zeiger auf eine [**OFNOTIFYEX-Struktur.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)

Die [**OFNOTIFYEX-Struktur**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) enthält eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) deren Code member die CDN **\_ INCLUDEITEM-Benachrichtigungsmeldung** angibt. 

Der **psf-Member** der [**OFNOTIFYEX-Struktur**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) ist ein Zeiger auf eine Schnittstelle für den Ordner, dessen Elemente aufzählt werden. Das **pidl-Element** ist ein Zeiger auf eine Elementbezeichnerliste, die das Element relativ zum Ordner identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die [*OFNHookProc-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) 0 (null) zurückgibt, schließt das Dialogfeld das Element aus der Liste der Elemente aus.

Um das Element ein include zu erhalten, geben Sie einen Wert ungleich 0 (null) aus der Hookprozedur zurück.

## <a name="remarks"></a>Hinweise

Das Dialogfeld enthält immer Elemente, die sowohl über die **ATTRIBUTE SFGAO \_ FILESYSTEM** als auch **SFGAO \_ FILESYSANCESTOR** verfügen, unabhängig vom Wert, der von CDN **\_ INCLUDEITEM zurückgegeben wird.**

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

[**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Allgemeine Dialogfeldbibliothek](common-dialog-box-library.md)
</dt> </dl>

