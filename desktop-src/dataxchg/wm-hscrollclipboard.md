---
title: WM_HSCROLLCLIPBOARD Meldung (Winuser. h)
description: Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet.
ms.assetid: 73558de6-a822-40f7-9eb2-47ea5afd4e6e
keywords:
- WM_HSCROLLCLIPBOARD Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_HSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34ee33709601b483258ae0aec4873c47fa69a00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478303"
---
# <a name="wm_hscrollclipboard-message"></a>WM- \_ hscrollclipboard-Nachricht

Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet. Dies tritt auf, wenn die Zwischenablage Daten im CF-Besitzer Anzeige Format enthält und ein Ereignis in der horizontalen Schiebe Leiste der Zwischenablage [**\_ Anzeige**](standard-clipboard-formats.md) auftritt. Der Besitzer sollte das Zwischenablage Bild scrollen und die ScrollBar-Werte aktualisieren.


```C++
#define WM_HSCROLLCLIPBOARD             0x030E
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Fenster der Zwischenablage Anzeige.

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort von *LPARAM* gibt ein ScrollBar-Ereignis an. Dieser Parameter kann einen der folgenden Werte annehmen. Das aktuellste Wort von *LPARAM* gibt die aktuelle Position des Bild Lauf Felds an, wenn es sich bei dem nieder wertigen Wort von *LPARAM* um SB-Finger **\_ Positionen** handelt. andernfalls wird das höchst wertige Wort nicht verwendet.



| Wert                                                                                                                                                                                                                         | Bedeutung                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ Endscroll**</dt> <dt>8</dt> </dl>             | Scrollvorgang beenden.<br/>                                                                            |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <dt>**SB \_ Links**</dt> <dt>6</dt> </dl>                            | Scrollen Sie nach oben links.<br/>                                                                  |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <dt>**SB \_ Recht**</dt> <dt>7</dt> </dl>                         | Scrollen Sie nach unten rechts.<br/>                                                                 |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <dt>**SB \_ LineLeft**</dt> <dt>0</dt> </dl>                | Scrollt nach links um eine Einheit.<br/>                                                              |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <dt>**SB \_ LineRight**</dt> <dt>1</dt> </dl>             | Scrollt nach rechts um eine Einheit.<br/>                                                             |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <dt>**SB \_ PageLeft**</dt> <dt>2</dt> </dl>                | Führt einen Bildlauf nach links um die Breite des Fensters aus.<br/>                                               |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <dt>**SB \_ PageRight**</dt> <dt>3</dt> </dl>             | Führt einen Bildlauf nach rechts um die Breite des Fensters aus.<br/>                                              |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ Fingerposition**</dt> <dt>4</dt> </dl> | Scrollen Sie zur absoluten Position. Die aktuelle Position wird durch das höchst wertige Wort angegeben.<br/> |



 

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

 

