---
title: WM_PSD_GREEKTEXTRECT Nachricht (Commdlg.h)
description: Benachrichtigt die Hookprozedur eines Page Setup-Dialogfelds PagePaintHook, dass das Dialogfeld nun griechisch-Text innerhalb des Randrechtecks der Beispielseite zeichnen soll.
ms.assetid: ad0a200d-5626-4768-b3bd-73d4e3f0d548
keywords:
- Dialogfelder für WM_PSD_GREEKTEXTRECT Meldung
topic_type:
- apiref
api_name:
- WM_PSD_GREEKTEXTRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c30e4873255a59a86da91b3145d0675f6940ce35081273696ce6c68b70a1560
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726050"
---
# <a name="wm_psd_greektextrect-message"></a>WM \_ PSD \_ GREEKTEXTRECT-Nachricht

Benachrichtigt die Hookprozedur eines Dialogfelds **"Seiteneinrichtung",** [*PagePaintHook,*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)darüber, dass im Dialogfeld griechischer Text innerhalb des Randrechtecks der Beispielseite gezeichnet werden soll.


```C++
#define WM_USER                  0x0400
#define WM_PSD_GREEKTEXTRECT    (WM_USER+4)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für den Gerätekontext für die Beispielseite.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die die Koordinaten des griechisch-Textrechtecks in Pixel enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Hookprozedur **TRUE** zurückgibt, zeichnet das Dialogfeld den griechisch-Textteil der Beispielseite nicht.

Wenn die Hookprozedur **FALSE** zurückgibt, zeichnet das Dialogfeld den griechisch-Textteil der Beispielseite.

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

 

