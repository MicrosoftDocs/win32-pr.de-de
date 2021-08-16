---
title: WM_VSCROLLCLIPBOARD Meldung (Winuser.h)
description: Wird von einem Zwischenablage-Viewer-Fenster an den Besitzer der Zwischenablage gesendet, wenn die Zwischenablage Daten im CF \_ OWNERDISPLAY-Format enthält und ein Ereignis in der vertikalen Bildlaufleiste des Zwischenablage-Viewers auftritt.
ms.assetid: 17bd32c4-1b07-42b7-b269-f517e3ec13f3
keywords:
- WM_VSCROLLCLIPBOARD Nachricht Data Exchange
topic_type:
- apiref
api_name:
- WM_VSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbcf634870ce232543cd20ccd42c9e8ca255705810e81af39cc6e81f8e41658d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544875"
---
# <a name="wm_vscrollclipboard-message"></a>WM \_ VSCROLLCLIPBOARD-Meldung

Wird von einem Zwischenablage-Viewer-Fenster an den Besitzer der Zwischenablage gesendet, wenn die Zwischenablage Daten im [**CF \_ OWNERDISPLAY-Format**](standard-clipboard-formats.md) enthält und ein Ereignis in der vertikalen Bildlaufleiste des Zwischenablage-Viewers auftritt. Der Besitzer sollte im Bild der Zwischenablage scrollen und die Werte der Bildlaufleiste aktualisieren.


```C++
#define WM_VSCROLLCLIPBOARD             0x030A
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Zwischenablage-Viewerfenster.

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort *lParam* in niedriger Reihenfolge gibt ein Bildlaufleistenereignis an. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                         | Bedeutung                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**SB \_ BOTTOM**</dt> <dt>7</dt> </dl>                      | Scrollen Sie nach unten rechts.<br/>                                                                 |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ENDSCROLL**</dt> <dt>8</dt> </dl>             | Ende des Bildlaufs.<br/>                                                                            |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> <dt>1</dt> </dl>                | Scrollen Sie um eine Zeile nach unten.<br/>                                                                  |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_ LINEUP**</dt> <dt>0</dt> </dl>                      | Scrollen Sie eine Zeile nach oben.<br/>                                                                    |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PAGEDOWN**</dt> <dt>3</dt> </dl>                | Scrollen Sie eine Seite nach unten.<br/>                                                                  |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PAGEUP**</dt> <dt>2</dt> </dl>                      | Scrollen Sie eine Seite nach oben.<br/>                                                                    |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt> </dl> | Scrollen Sie zur absoluten Position. Die aktuelle Position wird durch das Wort in hoher Reihenfolge angegeben.<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**SB \_ TOP**</dt> <dt>6</dt> </dl>                               | Scrollen Sie nach oben links.<br/>                                                                  |



 

Das Wort in hoher Reihenfolge von *lParam* gibt die aktuelle Position des Bildlauffelds an, wenn das Wort der niedrigen Ordnung von *lParam* **SB \_ THUMBPOSITION** ist. Andernfalls wird das Wort in hoher Reihenfolge von *lParam* nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Der Besitzer der Zwischenablage kann die [**ScrollWindow-Funktion**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) verwenden, um das Bild im Zwischenablage-Viewer-Fenster zu scrollen und die entsprechende Region ungültig zu machen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)
</dt> </dl>

 

