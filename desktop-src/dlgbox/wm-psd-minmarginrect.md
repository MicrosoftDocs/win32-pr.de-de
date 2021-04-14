---
title: WM_PSD_MINMARGINRECT Meldung (kommdlg. h)
description: Benachrichtigt eine pagepainthook-Hook-Prozedur über die Koordinaten des Rand Rechtecks auf der Beispielseite. Diese Meldung wird im Dialogfeld Seite einrichten gesendet, wenn der Inhalt der Beispielseite gezeichnet wird.
ms.assetid: 14977b52-7a6f-4c55-956a-716398a71613
keywords:
- Dialog Felder WM_PSD_MINMARGINRECT Meldung
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
ms.openlocfilehash: 22ec7271026ba7557fcbe3fe17cd890d62eadbca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518338"
---
# <a name="wm_psd_minmarginrect-message"></a>WM- \_ PSD- \_ minmarginrect-Meldung

Benachrichtigt eine [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur über die Koordinaten des Rand Rechtecks auf der Beispielseite. Diese Meldung wird im Dialogfeld **Seite einrichten** gesendet, wenn der Inhalt der Beispielseite gezeichnet wird.


```C++
#define WM_USER                  0x0400
#define WM_PSD_MINMARGINRECT    (WM_USER+2)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für den Gerätekontext der Beispielseite.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Koordinaten des minimalen Rand Rechtecks in Pixel enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Hook-Prozedur **true** zurückgibt, sendet das Dialogfeld keine weiteren Nachrichten und wird erst dann auf der Beispielseite gezeichnet, wenn das System die Beispielseite das nächste Mal neu zeichnen muss.

Wenn die Hook-Prozedur **false** zurückgibt, sendet das Dialogfeld die übrigen Nachrichten der Zeichnungs Sequenz.

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

 

