---
title: WM_PSD_MARGINRECT Meldung (Commdlg.h)
description: Benachrichtigt die Hookprozedur eines Page Setup-Dialogfelds PagePaintHook, dass das Dialogfeld das Randrechteck der Beispielseite zeichnen soll.
ms.assetid: 81c057ab-6faf-4dd8-8b0c-34a2753e572c
keywords:
- Dialogfelder für WM_PSD_MARGINRECT Meldung
topic_type:
- apiref
api_name:
- WM_PSD_MARGINRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09523258d1f67cfc4f35433a43a6b5a17db0be9dedaea87511c0c6d1327f82cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985260"
---
# <a name="wm_psd_marginrect-message"></a>WM \_ PSD \_ MARGINRECT-Nachricht

Benachrichtigt die Hookprozedur  eines Page Setup-Dialogfelds [**(PagePaintHook),**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)dass das Dialogfeld das Randrechteck der Beispielseite zeichnen soll.


```C++
#define WM_USER                  0x0400
#define WM_PSD_MARGINRECT       (WM_USER+3)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für den Gerätekontext für die Beispielseite.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die die Koordinaten des Randrechtecks in Pixel enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Hookprozedur **TRUE** zurückgibt, zeichnet das Dialogfeld das Randrechteck auf der Beispielseite nicht.

Wenn die Hookprozedur **FALSE** zurückgibt, zeichnet das Dialogfeld das Randrechteck auf der Beispielseite.

## <a name="remarks"></a>Hinweise

Das Dialogfeld **Seiteneinrichtung** enthält ein Bild einer Beispielseite, die zeigt, wie sich die Auswahl des Benutzers auf die Darstellung der gedruckten Ausgabe auswirkt. Wenn Sie die [**PageSetupDlg-Funktion**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) aufrufen, können Sie eine [*PagePaintHook-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) bereitstellen, um die Darstellung der Beispielseite anzupassen. Wenn das Dialogfeld den Inhalt der Beispielseite zeichnen soll, sendet das Dialogfeld eine Sequenz von Nachrichten an die Hookprozedur.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Commdlg.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

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

 

