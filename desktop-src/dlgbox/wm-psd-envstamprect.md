---
title: WM_PSD_ENVSTAMPRECT Meldung (kommdlg. h)
description: Benachrichtigt die Hook-Prozedur über das Dialogfeld "Seite einrichten" (pagepainthook), dass das Dialogfeld im Begriff ist, das Umschlag Stempel Rechteck der Beispielseite zu zeichnen.
ms.assetid: f193baa0-a084-416e-90c9-9c838758a3d3
keywords:
- Dialog Felder WM_PSD_ENVSTAMPRECT Meldung
topic_type:
- apiref
api_name:
- WM_PSD_ENVSTAMPRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf13485ab75f51298ef273c7e02ea0253e4244d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477970"
---
# <a name="wm_psd_envstamprect-message"></a>WM- \_ PSD- \_ Nachricht

Benachrichtigt die Hook-Prozedur über das Dialogfeld " **Seite einrichten** " ( [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)), dass das Dialogfeld im Begriff ist, das Umschlag Stempel Rechteck der Beispielseite zu zeichnen.


```C++
#define WM_USER                  0x0400
#define WM_PSD_ENVSTAMPRECT     (WM_USER+5)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für den Gerätekontext der Beispielseite.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Koordinaten des Umschlag Stempel Rechtecks in Pixel enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Hook-Prozedur **true** zurückgibt, wird der Teil des Umschlag Stempels der Beispielseite nicht im Dialogfeld gezeichnet.

Wenn die Hook-Prozedur **false** zurückgibt, wird das Dialogfeld den Umschlag Stempel Bereich der Beispielseite gezeichnet.

## <a name="remarks"></a>Bemerkungen

Das Dialogfeld **Seite einrichten** enthält ein Bild einer Beispielseite, das zeigt, wie sich die Auswahl des Benutzers auf die Darstellung der gedruckten Ausgabe auswirkt. Wenn Sie die [**pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) -Funktion aufrufen, können Sie eine [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur bereitstellen, um die Darstellung der Beispielseite anzupassen. Wenn im Dialogfeld der Inhalt der Beispielseite gezeichnet wird, sendet das Dialogfeld eine Sequenz von Meldungen an die Hook-Prozedur.

Eine Hook-Prozedur empfängt diese Nachricht nur, wenn es sich bei dem ausgewählten Papiertyp um einen Umschlag handelt.

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

 

