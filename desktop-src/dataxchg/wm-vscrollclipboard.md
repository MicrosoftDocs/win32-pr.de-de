---
title: WM_VSCROLLCLIPBOARD Meldung (Winuser. h)
description: Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet, wenn die Zwischenablage Daten im CF \_ -Besitzer Anzeige Format enthält und ein Ereignis auf der vertikalen Schiebe Leiste der Zwischenablage Anzeige auftritt.
ms.assetid: 17bd32c4-1b07-42b7-b269-f517e3ec13f3
keywords:
- WM_VSCROLLCLIPBOARD Nachrichten Datenaustausch
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
ms.openlocfilehash: 87a9e80aa342065ee88c8e1d7aa44c1fd598e411
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477175"
---
# <a name="wm_vscrollclipboard-message"></a>WM \_ vscrollclipboard-Nachricht

Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet, wenn die Zwischenablage Daten im CF-Besitzer Anzeige Format enthält und ein Ereignis auf der vertikalen Schiebe Leiste der Zwischenablage [**\_ Anzeige**](standard-clipboard-formats.md) auftritt. Der Besitzer sollte das Zwischenablage Bild scrollen und die ScrollBar-Werte aktualisieren.


```C++
#define WM_VSCROLLCLIPBOARD             0x030A
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Fenster der Zwischenablage Anzeige.

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort von *LPARAM* gibt ein ScrollBar-Ereignis an. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                         | Bedeutung                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**SB \_ Unten**</dt> <dt>7</dt> </dl>                      | Scrollen Sie nach unten rechts.<br/>                                                                 |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ Endscroll**</dt> <dt>8</dt> </dl>             | Scrollvorgang beenden.<br/>                                                                            |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LineDown**</dt> <dt>1</dt> </dl>                | Scrollen Sie in eine Zeile nach unten.<br/>                                                                  |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_ Lineup**</dt> <dt>0</dt> </dl>                      | Scrollen Sie in einer Zeile nach oben.<br/>                                                                    |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PageDown**</dt> <dt>3</dt> </dl>                | Scrollen Sie eine Seite nach unten.<br/>                                                                  |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PageUp**</dt> <dt>2</dt> </dl>                      | Scrollen Sie eine Seite nach oben.<br/>                                                                    |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ Fingerposition**</dt> <dt>4</dt> </dl> | Scrollen Sie zur absoluten Position. Die aktuelle Position wird durch das höchst wertige Wort angegeben.<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**SB \_ Top**</dt> <dt>6</dt> </dl>                               | Scrollen Sie nach oben links.<br/>                                                                  |



 

Das aktuellste Wort von *LPARAM* gibt die aktuelle Position des Bild Lauf Felds an, wenn es sich bei dem nieder wertigen Wort von *LPARAM* um **SB- \_ Fingerposition** handelt. andernfalls wird das höherwertige Wort von *LPARAM* nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Der Besitzer der Zwischenablage kann mit der [**scrollwindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) -Funktion im Fenster der Zwischenablage Anzeige einen Bildlauf durchführen und den entsprechenden Bereich für ungültig erklären.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Licher**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Scrollwindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)
</dt> </dl>

 

