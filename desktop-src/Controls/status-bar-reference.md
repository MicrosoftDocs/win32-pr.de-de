---
title: Statusleiste
description: Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit Statusleisten-Steuerelementen verwendet werden.
ms.assetid: 77923055-9d00-4528-bda7-b602a26b577f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1be3ea518b63118fc80b02b382943c40ba2fd13b15713488b351b5d6cc827e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696490"
---
# <a name="status-bar"></a>Statusleiste

Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit Statusleisten-Steuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                          | Inhalte                                                                                                                                                   |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Statusleisten](status-bars.md) | Eine *Statusleiste ist* ein horizontales Fenster am unteren Rand eines übergeordneten Fensters, in dem eine Anwendung verschiedene Arten von Statusinformationen anzeigen kann.<br/> |



 

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
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a></td>
<td>Erstellt ein Statusfenster, das normalerweise zum Anzeigen des Status einer Anwendung verwendet wird. Das Fenster wird im Allgemeinen am unteren Rand des übergeordneten Fensters angezeigt und enthält den angegebenen Text.
<blockquote>
[!Note]<br />
Diese Funktion ist veraltet. Verwenden <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>Sie stattdessen CreateWindow.</strong></a>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a></td>
<td>Die <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText-Funktion</strong></a> zeichnet den angegebenen Text im Stil eines Statusfensters mit Rahmen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a></td>
<td>Verarbeitet <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> und <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> Und zeigt Hilfetext zum aktuellen Menü im angegebenen Statusfenster an.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>Meldungen



| Thema                                               | Inhalte                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SB \_ GETBORDERS**](sb-getborders.md)             | Ruft die aktuelle Breite des horizontalen und vertikalen Rahmens eines Statusfensters ab. <br/>                                                                                                  |
| [**SB \_ GETICON**](sb-geticon.md)                   | Ruft das Symbol für ein Teil in einer Statusleiste ab. <br/>                                                                                                                                           |
| [**SB \_ GETPARTS**](sb-getparts.md)                 | Ruft die Anzahl der Teile in einem Statusfenster ab. Die Meldung ruft auch die Koordinate des rechten Rands der angegebenen Anzahl von Teilen ab. <br/>                                         |
| [**SB \_ GETRECT**](sb-getrect.md)                   | Ruft das umgebundene Rechteck eines Teils in einem Statusfenster ab. <br/>                                                                                                                           |
| [**SB \_ GETTEXT**](sb-gettext.md)                   | Die [**SB \_ GETTEXT-Nachricht**](sb-gettext.md) ruft den Text aus dem angegebenen Teil eines Statusfensters ab. <br/>                                                                             |
| [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md)       | Die [**SB \_ GETTEXTLENGTH-Nachricht**](sb-gettextlength.md) ruft die Länge des Texts in Zeichen aus dem angegebenen Teil eines Statusfensters ab. <br/>                                   |
| [**SB \_ GETTIPTEXT**](sb-gettiptext.md)             | Ruft den QuickInfo-Text für ein Teil in einer Statusleiste ab. Die Statusleiste muss mit dem [**SBT-QuickInfos-Format \_ erstellt**](status-bar-styles.md) werden, um QuickInfos zu aktivieren. <br/>         |
| [**SB \_ GETUNICODEFORMAT**](sb-getunicodeformat.md) | Ruft das Unicode-Zeichenformatflag für das Steuerelement ab. <br/>                                                                                                                             |
| [**SB \_ ISSIMPLE**](sb-issimple.md)                 | Überprüft ein Statusleisten-Steuerelement, um festzustellen, ob es sich im einfachen Modus befindet. <br/>                                                                                                                        |
| [**SB \_ SETBKCOLOR**](sb-setbkcolor.md)             | Legt die Hintergrundfarbe in einer Statusleiste fest. <br/>                                                                                                                                               |
| [**SB \_ SETICON**](sb-seticon.md)                   | Legt das Symbol für ein Teil in einer Statusleiste fest. <br/>                                                                                                                                                |
| [**SB \_ SETMINHEIGHT**](sb-setminheight.md)         | Legt die Mindesthöhe des Zeichnungsbereichs eines Statusfensters fest. <br/>                                                                                                                               |
| [**SB \_ SETPARTS**](sb-setparts.md)                 | Legt die Anzahl der Teile in einem Statusfenster und die Koordinate des rechten Rands jedes Teils fest. <br/>                                                                                           |
| [**SB \_ SETTEXT**](sb-settext.md)                   | Die SB \_ SETTEXT-Meldung legt den Text im angegebenen Teil eines Statusfensters fest.<br/>                                                                                                           |
| [**SB \_ SETTIPTEXT**](sb-settiptext.md)             | Legt den QuickInfo-Text für ein Teil in einer Statusleiste fest. Die Statusleiste muss mit dem [**SBT-QuickInfos-Format \_**](status-bar-styles.md) erstellt worden sein, um QuickInfos zu aktivieren.<br/>        |
| [**SB \_ SETUNICODEFORMAT**](sb-setunicodeformat.md) | Legt das Unicode-Zeichenformatflag für das Steuerelement fest. Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen. <br/> |
| [**SB \_ SIMPLE**](sb-simple.md)                     | Gibt an, ob in einem Statusfenster einfacher Text oder alle Fensterteile angezeigt werden, die durch eine vorherige [**SB \_ SETPARTS-Meldung festgelegt**](sb-setparts.md) wurden. <br/>                                       |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                 | Inhalte                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CLICK (Statusleiste)](nm-click-status-bar.md)     | Benachrichtigt das übergeordnete Fenster eines Statusleisten-Steuerelements, dass der Benutzer im Steuerelement auf die linke Maustaste geklickt hat. [NM \_ CLICK (Statusleiste)](nm-click-status-bar.md) wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/>              |
| [NM \_ DBLCLK (Statusleiste)](nm-dblclk-status-bar.md)   | Benachrichtigt das übergeordnete Fenster eines Statusleisten-Steuerelements, dass der Benutzer im Steuerelement auf die linke Maustaste doppelklickt. Diese Benachrichtigung wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/>                                       |
| [NM \_ RCLICK (Statusleiste)](nm-rclick-status-bar.md)   | Benachrichtigt das übergeordnete Fenster eines Statusleisten-Steuerelements, dass der Benutzer im Steuerelement auf die rechte Maustaste geklickt hat. Diese Benachrichtigung wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/>                                             |
| [NM \_ RDBLCLK (Statusleiste)](nm-rdblclk-status-bar.md) | Benachrichtigt die übergeordneten Fenster eines Statusleisten-Steuerelements, dass der Benutzer im Steuerelement auf die rechte Maustaste doppelklickt. [NM \_ RDBLCLK (Statusleiste)](nm-rdblclk-status-bar.md) wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/> |
| [SBN \_ SIMPLEMODECHANGE](sbn-simplemodechange.md)     | Wird von einem Statusleisten-Steuerelement gesendet, wenn sich der einfache Modus aufgrund einer [**SB \_ SIMPLE-Nachricht**](sb-simple.md) ändert. Diese Benachrichtigung wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                        |



 

### <a name="constants"></a>Konstanten



| Thema                                      | Inhalte                                                                                                              |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Statusleistenstile](status-bar-styles.md) | In diesem Abschnitt werden die Stile aufgeführt, die zusätzlich zu den Standardfensterstilen von *Statusleisten-Steuerelementen unterstützt* werden. <br/> |



 

 

