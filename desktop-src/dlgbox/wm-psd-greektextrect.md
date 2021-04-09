---
title: WM_PSD_GREEKTEXTRECT Meldung (kommdlg. h)
description: Benachrichtigt die Hook-Prozedur über das Dialogfeld "Seite einrichten" (pagepainthook), dass das Dialogfeld im Begriff ist, griechischen Text innerhalb des Rand Rechtecks der Beispielseite zu zeichnen.
ms.assetid: ad0a200d-5626-4768-b3bd-73d4e3f0d548
keywords:
- Dialog Felder WM_PSD_GREEKTEXTRECT Meldung
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
ms.openlocfilehash: fd0853720bea8cadc8df40d8fa649f644fd00694
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040811"
---
# <a name="wm_psd_greektextrect-message"></a>WM- \_ PSD- \_ Meldung "greektextrect"

Benachrichtigt die Hook-Prozedur über das Dialogfeld " **Seite einrichten** " ( [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)), dass das Dialogfeld im Begriff ist, griechischen Text innerhalb des Rand Rechtecks der Beispielseite zu zeichnen.


```C++
#define WM_USER                  0x0400
#define WM_PSD_GREEKTEXTRECT    (WM_USER+4)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für den Gerätekontext der Beispielseite.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Koordinaten des griechischen Text Rechtecks in Pixel enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Hook-Prozedur **true** zurückgibt, wird der griechische Textteil der Beispielseite nicht im Dialogfeld gezeichnet.

Wenn die Hook-Prozedur **false** zurückgibt, zeichnet das Dialogfeld den griechischen Textteil der Beispielseite.

## <a name="remarks"></a>Bemerkungen

Das Dialogfeld **Seite einrichten** enthält ein Bild einer Beispielseite, das zeigt, wie sich die Auswahl des Benutzers auf die Darstellung der gedruckten Ausgabe auswirkt. Wenn Sie die [**pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) -Funktion aufrufen, können Sie eine [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur bereitstellen, um die Darstellung der Beispielseite anzupassen. Wenn im Dialogfeld der Inhalt der Beispielseite gezeichnet wird, sendet das Dialogfeld eine Sequenz von Meldungen an die Hook-Prozedur.

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

[*Pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

[**Pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))
</dt> <dt>

[**WM- \_ PSD \_ pagesetupdlg**](wm-psd-pagesetupdlg.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Allgemeine Dialog Feld Bibliothek](common-dialog-box-library.md)
</dt> </dl>

 

