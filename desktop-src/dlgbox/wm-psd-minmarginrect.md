---
title: WM_PSD_MINMARGINRECT Nachricht (Commdlg.h)
description: Benachrichtigt eine PagePaintHook-Hookprozedur über die Koordinaten des Randrechtecks auf der Beispielseite. Ein Dialogfeld "Seiteneinrichtung" sendet diese Meldung, wenn der Inhalt der Beispielseite gezeichnet werden soll.
ms.assetid: 14977b52-7a6f-4c55-956a-716398a71613
keywords:
- Dialogfelder für WM_PSD_MINMARGINRECT Meldung
topic_type:
- apiref
api_name:
- WM_PSD_MINMARGINRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10557e3fc605fc86b1cfa1c7b44fd1e4d40ac399476c5b2c573f46db5c4103b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503315"
---
# <a name="wm_psd_minmarginrect-message"></a>WM \_ PSD \_ MINMARGINRECT-Nachricht

Benachrichtigt eine [*PagePaintHook-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) über die Koordinaten des Randrechtecks auf der Beispielseite. Ein Dialogfeld **"Seiteneinrichtung"** sendet diese Meldung, wenn der Inhalt der Beispielseite gezeichnet werden soll.


```C++
#define WM_USER                  0x0400
#define WM_PSD_MINMARGINRECT    (WM_USER+2)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für den Gerätekontext für die Beispielseite.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die die Koordinaten des minimalen Randrechtecks in Pixel enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Hookprozedur **TRUE** zurückgibt, sendet das Dialogfeld keine Nachrichten mehr und zeichnet erst dann auf der Beispielseite, wenn das System die Beispielseite das nächste Mal neu zeichnen muss.

Wenn die Hookprozedur **FALSE** zurückgibt, sendet das Dialogfeld die verbleibenden Nachrichten der Zeichnungssequenz.

## <a name="remarks"></a>Hinweise

Das Dialogfeld **Seiteneinrichtung** enthält ein Bild einer Beispielseite, die zeigt, wie sich die Auswahl des Benutzers auf die Darstellung der gedruckten Ausgabe auswirkt. Wenn Sie die [**PageSetupDlg-Funktion**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) aufrufen, können Sie eine [*PagePaintHook-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) bereitstellen, um die Darstellung der Beispielseite anzupassen. Wenn das Dialogfeld den Inhalt der Beispielseite zeichnen soll, sendet das Dialogfeld eine Sequenz von Nachrichten an die Hookprozedur.

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

[*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))
</dt> <dt>

[**WM \_ PSD \_ PAGESETUPDLG**](wm-psd-pagesetupdlg.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Allgemeine Dialogfeldbibliothek](common-dialog-box-library.md)
</dt> </dl>

 

