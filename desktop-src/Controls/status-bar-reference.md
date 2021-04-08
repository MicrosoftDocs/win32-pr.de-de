---
title: Statusleiste
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit StatusBar-Steuerelementen verwendet werden.
ms.assetid: 77923055-9d00-4528-bda7-b602a26b577f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6e46f1c573b75439cc10aa27ae3245e47e3de9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103731489"
---
# <a name="status-bar"></a>Statusleiste

Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit StatusBar-Steuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                          | Inhalte                                                                                                                                                   |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Status leisten](status-bars.md) | Eine *Statusleiste* ist ein horizontales Fenster am unteren Rand eines übergeordneten Fensters, in dem eine Anwendung verschiedene Arten von Statusinformationen anzeigen kann.<br/> |



 

### <a name="functions"></a>Functions



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>Inhalte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>"Kreatestatus Window"</strong></a></td>
<td>Erstellt ein Statusfenster, das in der Regel verwendet wird, um den Status einer Anwendung anzuzeigen. Das Fenster wird in der Regel am unteren Rand des übergeordneten Fensters angezeigt und enthält den angegebenen Text.
<blockquote>
[!Note]<br />
Diese Funktion ist veraltet. Verwenden Sie stattdessen "up <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>Window</strong></a> ".
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>Drawstatustext</strong></a></td>
<td>Die <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>drawstatustext</strong></a> -Funktion zeichnet den angegebenen Text im Stil eines Status Fensters mit Rändern.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>Menuhelp</strong></a></td>
<td>Verarbeitet <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> und <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> Meldungen und zeigt Hilfe Text zum aktuellen Menü im angegebenen Statusfenster an.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>Meldungen



| Thema                                               | Inhalte                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SB \_ getrahmens**](sb-getborders.md)             | Ruft die aktuelle Breite der horizontalen und vertikalen Rahmen eines Status Fensters ab. <br/>                                                                                                  |
| [**SB- \_ getIcon**](sb-geticon.md)                   | Ruft das Symbol für einen Teil in einer Statusleiste ab. <br/>                                                                                                                                           |
| [**SB- \_ GetParts**](sb-getparts.md)                 | Ruft die Anzahl der Teile in einem Statusfenster ab. Die Meldung ruft auch die Koordinate des rechten Rands der angegebenen Anzahl von Teilen ab. <br/>                                         |
| [**SB \_ GetRect**](sb-getrect.md)                   | Ruft das umgebende Rechteck eines Teils in einem Statusfenster ab. <br/>                                                                                                                           |
| [**SB \_ gettext**](sb-gettext.md)                   | Die [**SB \_ gettext**](sb-gettext.md) -Nachricht Ruft den Text aus dem angegebenen Teil eines Status Fensters ab. <br/>                                                                             |
| [**SB \_ getTextLength**](sb-gettextlength.md)       | Die [**SB \_ getTextLength**](sb-gettextlength.md) -Nachricht Ruft die Länge des Texts aus dem angegebenen Teil eines Status Fensters in Zeichen ab. <br/>                                   |
| [**SB \_ GetTipText**](sb-gettiptext.md)             | Ruft den QuickInfo-Text für einen Teil in einer Statusleiste ab. Die Statusleiste muss mit dem [**SBT- \_ Tooltips**](status-bar-styles.md) -Stil erstellt werden, um Quick Infos zu aktivieren. <br/>         |
| [**SB \_ getunicodeformat**](sb-getunicodeformat.md) | Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab. <br/>                                                                                                                             |
| [**SB \_ IsSimple**](sb-issimple.md)                 | Überprüft ein Status leisten-Steuerelement, um zu bestimmen, ob es sich im einfachen Modus befindet. <br/>                                                                                                                        |
| [**SB \_ SetBkColor**](sb-setbkcolor.md)             | Legt die Hintergrundfarbe in einer Statusleiste fest. <br/>                                                                                                                                               |
| [**SB \_ -Ziel**](sb-seticon.md)                   | Legt das Symbol für einen Teil in einer Statusleiste fest. <br/>                                                                                                                                                |
| [**SB- \_ setMinHeight**](sb-setminheight.md)         | Legt die Mindesthöhe für den Zeichnungs Bereich eines Status Fensters fest. <br/>                                                                                                                               |
| [**SB- \_ SetParts**](sb-setparts.md)                 | Legt die Anzahl der Teile in einem Statusfenster und die Koordinate des rechten Rands der einzelnen Teile fest. <br/>                                                                                           |
| [**SB- \_ SetText**](sb-settext.md)                   | Die SB- \_ SetText-Nachricht legt den Text im angegebenen Teil eines Status Fensters fest.<br/>                                                                                                           |
| [**SB-Setup \_ Text**](sb-settiptext.md)             | Legt den QuickInfo-Text für einen Teil in einer Statusleiste fest. Die Statusleiste muss mit dem [**SBT- \_ Tooltips**](status-bar-styles.md) -Stil erstellt worden sein, um Quick Infos zu aktivieren.<br/>        |
| [**SB- \_ Code Format**](sb-setunicodeformat.md) | Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest. Mit dieser Meldung können Sie den Zeichensatz ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen. <br/> |
| [**SB \_ Simple**](sb-simple.md)                     | Gibt an, ob ein Statusfenster einfachen Text anzeigt oder alle durch eine vorherige [**SB \_ SetParts**](sb-setparts.md) -Meldung festgelegten Fensterteile anzeigt. <br/>                                       |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                 | Inhalte                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ Klick (Statusleiste)](nm-click-status-bar.md)     | Benachrichtigt das übergeordnete Fenster eines StatusBar-Steuer Elements, dass der Benutzer auf die linke Maustaste im Steuerelement geklickt hat. [Nm \_ Klicken Sie](nm-click-status-bar.md) in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung auf (Statusleiste).<br/>              |
| [NM \_ dblclk (Statusleiste)](nm-dblclk-status-bar.md)   | Benachrichtigt das übergeordnete Fenster eines Status leisten-Steuer Elements, dass der Benutzer die linke Maustaste im Steuerelement doppelt geklickt hat. Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md)<br/>                                       |
| [NM \_ rclick (Statusleiste)](nm-rclick-status-bar.md)   | Benachrichtigt das übergeordnete Fenster eines Status leisten-Steuer Elements, dass der Benutzer mit der rechten Maustaste im-Steuerelement geklickt hat. Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md)<br/>                                             |
| [NM \_ rdblclk (Statusleiste)](nm-rdblclk-status-bar.md) | Benachrichtigt die übergeordneten Fenster eines Status leisten-Steuer Elements, dass der Benutzer die Rechte Maustaste im Steuerelement doppelt geklickt hat. [Nm \_ Rdblclk (Statusleiste)](nm-rdblclk-status-bar.md) wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/> |
| [SBN \_ simplemodechange](sbn-simplemodechange.md)     | Wird von einem StatusBar-Steuerelement gesendet, wenn sich der einfache Modus aufgrund einer [**\_ einfachen SB**](sb-simple.md) -Nachricht ändert. Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md) <br/>                                                        |



 

### <a name="constants"></a>Konstanten



| Thema                                      | Inhalte                                                                                                              |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [StatusBar-Stile](status-bar-styles.md) | In diesem Abschnitt werden die Stile sowie die Standardfenster Stile aufgelistet, die von *StatusBar* -Steuerelementen unterstützt werden. <br/> |



 

 

