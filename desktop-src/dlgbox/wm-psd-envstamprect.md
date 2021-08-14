---
title: WM_PSD_ENVSTAMPRECT Nachricht (Commdlg.h)
description: Benachrichtigt die Hookprozedur eines Page Setup-Dialogfelds PagePaintHook, dass das Dialogfeld das Umschlagstempelrechteck der Beispielseite zeichnen soll.
ms.assetid: f193baa0-a084-416e-90c9-9c838758a3d3
keywords:
- Dialogfelder für WM_PSD_ENVSTAMPRECT Meldung
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
ms.openlocfilehash: 3bf846779f2fba5c2b2ac85d806c794d3e88aa6dcac0ce906ad82332e2ca2bee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720707"
---
# <a name="wm_psd_envstamprect-message"></a>WM \_ PSD \_ ENVSTAMPRECT-Nachricht

Benachrichtigt die Hookprozedur eines Dialogfelds **"Seiteneinrichtung",** [*PagePaintHook,*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)dass das Dialogfeld das Umschlagstempelrechteck der Beispielseite zeichnen soll.


```C++
#define WM_USER                  0x0400
#define WM_PSD_ENVSTAMPRECT     (WM_USER+5)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für den Gerätekontext für die Beispielseite.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die die Koordinaten des Umschlagsstempelrechtecks in Pixel enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Hookprozedur **TRUE** zurückgibt, zeichnet das Dialogfeld den Umschlagsstempelteil der Beispielseite nicht.

Wenn die Hookprozedur **FALSE** zurückgibt, zeichnet das Dialogfeld den Umschlagstempelteil der Beispielseite.

## <a name="remarks"></a>Hinweise

Das Dialogfeld **Seiteneinrichtung** enthält ein Bild einer Beispielseite, die zeigt, wie sich die Auswahl des Benutzers auf die Darstellung der gedruckten Ausgabe auswirkt. Wenn Sie die [**PageSetupDlg-Funktion**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) aufrufen, können Sie eine [*PagePaintHook-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) bereitstellen, um die Darstellung der Beispielseite anzupassen. Wenn das Dialogfeld den Inhalt der Beispielseite zeichnen soll, sendet das Dialogfeld eine Sequenz von Nachrichten an die Hookprozedur.

Eine Hookprozedur empfängt diese Meldung nur, wenn der ausgewählte Papiertyp ein Umschlag ist.

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

 

