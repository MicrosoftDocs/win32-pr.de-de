---
title: WM_PSD_PAGESETUPDLG Meldung (kommdlg. h)
description: Benachrichtigt eine pagepainthook-Hook-Prozedur, dass im Dialogfeld Seite einrichten der Inhalt der Beispielseite gezeichnet wird. Die Hook-Prozedur kann diese Nachricht verwenden, um Initialisierungs Aufgaben auszuführen, die sich auf das Zeichnen des Inhalts der Beispielseite beziehen.
ms.assetid: 0d95240b-7d77-4819-8e5c-cc25cd1b30f2
keywords:
- Dialog Felder WM_PSD_PAGESETUPDLG Meldung
topic_type:
- apiref
api_name:
- WM_PSD_PAGESETUPDLG
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9706eff6d015dc31332d9f757c954081f0134b2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392188"
---
# <a name="wm_psd_pagesetupdlg-message"></a>WM- \_ PSD- \_ pagesetupdlg-Nachricht

Benachrichtigt eine [**pagepainthook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur, dass im Dialogfeld **Seite einrichten** der Inhalt der Beispielseite gezeichnet wird. Die Hook-Prozedur kann diese Nachricht verwenden, um Initialisierungs Aufgaben auszuführen, die sich auf das Zeichnen des Inhalts der Beispielseite beziehen.


```C++
#define WM_USER                  0x0400
#define WM_PSD_PAGESETUPDLG     (WM_USER  )
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das nieder wertige Wort gibt einen Wert an, der das Papierformat angibt. Bei diesem Wert kann es sich um einen der **DMPAPER \_** -Werte handeln, die in der Beschreibung der Struktur aufgeführt sind. Das höchst wertige Wort gibt die Ausrichtung des Papiers oder des Umschlags an und gibt an, ob der Drucker eine Punktmatrix oder ein HPPCL-Gerät (Hewlett Packard Printer Control Language) ist. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                             | Bedeutung                                            |
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>0x0001</dt> </dl> | Papier im Querformat (Punktmatrix)<br/>    |
| <dl> <dt>0x0003</dt> </dl> | Papier im Querformat (HPPCL)<br/>         |
| <dl> <dt>0x0005</dt> </dl> | Papier im Hochformat (Punktmatrix)<br/>     |
| <dl> <dt>0x0007</dt> </dl> | Papier im Hochformat (HPPCL)<br/>          |
| <dl> <dt>0x000b</dt> </dl> | Umschlag im Querformat (HPPCL)<br/>      |
| <dl> <dt>0x000d</dt> </dl> | Umschlag im Hochformat (Punktmatrix)<br/>  |
| <dl> <dt>0x0019</dt> </dl> | Umschlag im Querformat (Punktmatrix)<br/> |
| <dl> <dt>0x001F</dt> </dl> | Umschlag im Hochformat (HPPCL)<br/>       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**pagesetupdlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) -Struktur, die Informationen enthält, die zum Initialisieren des Dialog Felds **Seite einrichten** verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Hook-Prozedur **true** zurückgibt, sendet das Dialogfeld keine weiteren Nachrichten und wird erst dann auf der Beispielseite gezeichnet, wenn das System die Beispielseite das nächste Mal neu zeichnen muss.

Wenn die Hook-Prozedur **false** zurückgibt, sendet das Dialogfeld die übrigen Nachrichten der Zeichnungs Sequenz.

## <a name="remarks"></a>Bemerkungen

Das Dialogfeld **Seite einrichten** enthält ein Bild einer Beispielseite, das zeigt, wie sich die Auswahl des Benutzers auf die Darstellung der gedruckten Ausgabe auswirkt. Wenn Sie die [**pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) -Funktion aufrufen, können Sie eine [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur bereitstellen, um die Darstellung der Beispielseite anzupassen. Wenn im Dialogfeld der Inhalt der Beispielseite gezeichnet wird, sendet das Dialogfeld eine Sequenz von Meldungen an die Hook-Prozedur.

Die ersten drei Nachrichten einer Zeichnungs Sequenz (**WM \_ PSD \_ pagesetupdlg**, [**WM \_ PSD \_ fullpagentror**](wm-psd-fullpagerect.md) [**WM \_ PSD \_ minmarginrect**](wm-psd-minmarginrect.md)) stellen Informationen bereit, die die Hook-Prozedur zum Zeichnen des Inhalts der Beispielseite verwenden kann. Die übrigen Nachrichten [**(WM \_ PSD \_ marginrect**](wm-psd-marginrect.md), [**WM \_ PSD \_ greektextrect**](wm-psd-greektextrect.md), [**WM \_ PSD \_ envstamprect**](wm-psd-envstamprect.md), [**WM \_ PSD \_ yafullpagtory**](wm-psd-yafullpagerect.md)) benachrichtigen die Hook-Prozedur, dass im Dialogfeld ein bestimmter Teil der Beispielseite gezeichnet wird. Dadurch kann die Hook-Prozedur Teile der Beispielseite selektiv zeichnen.

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

[**Pagesetupdlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[**WM- \_ PSD- \_ präct**](wm-psd-envstamprect.md)
</dt> <dt>

[**WM- \_ PSD \_ fullpagerup**](wm-psd-fullpagerect.md)
</dt> <dt>

[**WM- \_ PSD \_ greektextrect**](wm-psd-greektextrect.md)
</dt> <dt>

[**WM \_ PSD \_ marginrect**](wm-psd-marginrect.md)
</dt> <dt>

[**WM- \_ PSD \_ minmarginrect**](wm-psd-minmarginrect.md)
</dt> <dt>

[**WM- \_ PSD \_ yafullpagtory**](wm-psd-yafullpagerect.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Allgemeine Dialog Feld Bibliothek](common-dialog-box-library.md)
</dt> </dl>

 

