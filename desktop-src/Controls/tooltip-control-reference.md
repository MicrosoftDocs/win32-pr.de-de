---
title: QuickInfo
description: Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit QuickInfo-Steuerelementen verwendet werden.
ms.assetid: vs|controls|~\controls\tooltip\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30ebe66569ede133c311168d3f3f2870dc3aeabe8eaeaa3e15d6584be2d6873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046040"
---
# <a name="tooltip"></a>QuickInfo

Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit QuickInfo-Steuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                              | Inhalte                                                                                                                          |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu QuickInfo-Steuerelementen](tooltip-controls.md)     | QuickInfos werden automatisch angezeigt oder werden angezeigt, wenn der Benutzer den Mauszeiger über ein Tool oder ein anderes Benutzeroberflächenelement hält.<br/> |
| [Verwenden von QuickInfo-Steuerelementen](using-tooltip-contro.md) | Dieser Abschnitt enthält Beispiele, die veranschaulichen, wie verschiedene Arten von QuickInfos erstellt werden.<br/>                             |



 

### <a name="messages"></a>Meldungen



| Thema                                               | Inhalte                                                                                                                                                                                                          |
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TTM \_ ACTIVATE**](ttm-activate.md)               | Aktiviert oder deaktiviert ein QuickInfo-Steuerelement. <br/>                                                                                                                                                           |
| [**TTM \_ ADDTOOL**](ttm-addtool.md)                 | Registriert ein Tool mit einem QuickInfo-Steuerelement. <br/>                                                                                                                                                              |
| [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md)           | Berechnet das Textanzeigerechteck eines QuickInfo-Steuerelements aus seinem Fensterrechteck oder das QuickInfo-Fensterrechteck, das zum Anzeigen eines angegebenen Textanzeigerechtecks benötigt wird. <br/>                                |
| [**TTM \_ DELTOOL**](ttm-deltool.md)                 | Entfernt ein Tool aus einem QuickInfo-Steuerelement. <br/>                                                                                                                                                                |
| [**\_TTM-ENUMTOOLS**](ttm-enumtools.md)             | Ruft die Informationen ab, die ein QuickInfo-Steuerelement über das aktuelle Tool verwaltet, d. h. das Tool, für das die QuickInfo derzeit Text anzeigt. <br/>                                               |
| [**TTM \_ GETBUBBLESIZE**](ttm-getbubblesize.md)     | Gibt die Breite und Höhe eines QuickInfo-Steuerelements zurück.<br/>                                                                                                                                                     |
| [**TTM \_ GETCURRENTTOOL**](ttm-getcurrenttool.md)   | Ruft die Informationen für das aktuelle Tool in einem QuickInfo-Steuerelement ab. <br/>                                                                                                                                  |
| [**TTM \_ GETDELAYTIME**](ttm-getdelaytime.md)       | Ruft die anfänglichen, Popup- und Wiederholungsdauern ab, die derzeit für ein QuickInfo-Steuerelement festgelegt sind.<br/>                                                                                                               |
| [**TTM \_ GETMARGIN**](ttm-getmargin.md)             | Ruft die oberen, linken, unteren und rechten Ränder ab, die für ein QuickInfo-Fenster festgelegt sind. Ein Rand ist der Abstand zwischen dem Rahmen des QuickInfo-Fensters und dem Im QuickInfo-Fenster enthaltenen Text in Pixel. <br/> |
| [**TTM \_ GETMAXTIPWIDTH**](ttm-getmaxtipwidth.md)   | Ruft die maximale Breite für ein QuickInfo-Fenster ab. <br/>                                                                                                                                                     |
| [**TTM \_ GETTEXT**](ttm-gettext.md)                 | Ruft die Informationen ab, die ein QuickInfo-Steuerelement über ein Tool verwaltet. <br/>                                                                                                                                   |
| [**TTM \_ GETTIPBKCOLOR**](ttm-gettipbkcolor.md)     | Ruft die Hintergrundfarbe in einem QuickInfo-Fenster ab. <br/>                                                                                                                                                   |
| [**TTM \_ GETTIPTEXTCOLOR**](ttm-gettiptextcolor.md) | Ruft die Textfarbe in einem QuickInfo-Fenster ab. <br/>                                                                                                                                                         |
| [**TTM \_ GETTITLE**](ttm-gettitle.md)               | Ruft Informationen zum Titel eines QuickInfo-Steuerelements ab.<br/>                                                                                                                                        |
| [**TTM \_ GETTOOLCOUNT**](ttm-gettoolcount.md)       | Ruft die Anzahl der Tools ab, die von einem QuickInfo-Steuerelement verwaltet werden. <br/>                                                                                                                                       |
| [**TTM \_ GETTOOLINFO**](ttm-gettoolinfo.md)         | Ruft die Informationen ab, die ein QuickInfo-Steuerelement über ein Tool verwaltet. <br/>                                                                                                                              |
| [**TTM \_ HITTEST**](ttm-hittest.md)                 | Testet einen Punkt, um zu bestimmen, ob er sich innerhalb des umgrenzten Rechtecks des angegebenen Tools befindet, und ruft ggf. Informationen zum Tool ab. <br/>                                                     |
| [**TTM \_ NEWTOOLRECT**](ttm-newtoolrect.md)         | Legt ein neues umgrenzendes Rechteck für ein Tool fest. <br/>                                                                                                                                                             |
| [**TTM \_ POP**](ttm-pop.md)                         | Entfernt ein angezeigtes QuickInfo-Fenster aus der Ansicht. <br/>                                                                                                                                                         |
| [**\_TTM-POPUP**](ttm-popup.md)                     | Bewirkt, dass die QuickInfo an den Koordinaten der letzten Mausnachricht angezeigt wird.<br/>                                                                                                                            |
| [**TTM \_ RELAYEVENT**](ttm-relayevent.md)           | Übergibt eine Mausnachricht zur Verarbeitung an ein QuickInfo-Steuerelement. <br/>                                                                                                                                           |
| [**TTM \_ SETDELAYTIME**](ttm-setdelaytime.md)       | Legt die anfänglichen, Popup- und Wiederholungsdauern für ein QuickInfo-Steuerelement fest.<br/>                                                                                                                                  |
| [**TTM \_ SETMARGIN**](ttm-setmargin.md)             | Legt die oberen, linken, unteren und rechten Ränder für ein QuickInfo-Fenster fest. Ein Rand ist der Abstand zwischen dem Rahmen des QuickInfo-Fensters und dem Im QuickInfo-Fenster enthaltenen Text in Pixel. <br/>          |
| [**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md)   | Legt die maximale Breite für ein QuickInfo-Fenster fest. <br/>                                                                                                                                                          |
| [**TTM \_ SETTIPBKCOLOR**](ttm-settipbkcolor.md)     | Legt die Hintergrundfarbe in einem QuickInfo-Fenster fest. <br/>                                                                                                                                                        |
| [**TTM \_ SETTIPTEXTCOLOR**](ttm-settiptextcolor.md) | Legt die Textfarbe in einem QuickInfo-Fenster fest. <br/>                                                                                                                                                              |
| [**TTM \_ SETTITLE**](ttm-settitle.md)               | Fügt einer QuickInfo ein Standardsymbol und eine Titelzeichenfolge hinzu.<br/>                                                                                                                                                    |
| [**TTM \_ SETTOOLINFO**](ttm-settoolinfo.md)         | Legt die Informationen fest, die ein QuickInfo-Steuerelement für ein Tool verwaltet. <br/>                                                                                                                                     |
| [**TTM \_ SETWINDOWTHEME**](ttm-setwindowtheme.md)   | Legt den visuellen Stil eines QuickInfo-Steuerelements fest.<br/>                                                                                                                                                            |
| [**TTM \_ TRACKACTIVATE**](ttm-trackactivate.md)     | Aktiviert oder deaktiviert eine Nachverfolgungs-QuickInfo.<br/>                                                                                                                                                           |
| [**TTM \_ TRACKPOSITION**](ttm-trackposition.md)     | Legt die Position einer Nachverfolgungs-QuickInfo fest.<br/>                                                                                                                                                               |
| [**TTM \_ UPDATE**](ttm-update.md)                   | Erzwingt, dass die aktuelle QuickInfo neu gezeichnet wird. <br/>                                                                                                                                                             |
| [**TTM \_ UPDATETIPTEXT**](ttm-updatetiptext.md)     | Legt den QuickInfo-Text für ein Tool fest. <br/>                                                                                                                                                                     |
| [**TTM \_ WINDOWFROMPOINT**](ttm-windowfrompoint.md) | Ermöglicht einer Unterklassenprozedur, dass eine QuickInfo Text für ein anderes Fenster als das fenster unter dem Mauscursor anzeigt. <br/>                                                                              |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                 | Inhalte                                                                                                                                                                                                                                                              |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (QuickInfo)](nm-customdraw-tooltip.md) | Wird von einem QuickInfo-Steuerelement gesendet, um die übergeordneten Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                 |
| [TTN \_ GETDISPINFO](ttn-getdispinfo.md)               | Wird von einem QuickInfo-Steuerelement gesendet, um Informationen abzurufen, die zum Anzeigen eines QuickInfo-Fensters erforderlich sind. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                            |
| [TTN \_ LINKCLICK](ttn-linkclick.md)                   | Wird gesendet, wenn auf einen Textlink in einer Sprechblasen-QuickInfo geklickt wird. <br/>                                                                                                                                                                                                |
| [TTN \_ NEEDTEXT](ttn-needtext.md)                     | Wird von einem QuickInfo-Steuerelement gesendet, um Informationen abzurufen, die zum Anzeigen eines QuickInfo-Fensters erforderlich sind. Diese Benachrichtigung ist identisch mit [TTN \_ GETDISPINFO.](ttn-getdispinfo.md) Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/> |
| [TTN \_ POP](ttn-pop.md)                               | Benachrichtigt das Besitzerfenster, dass eine QuickInfo ausgeblendet werden soll. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                  |
| [TTN \_ SHOW](ttn-show.md)                             | Benachrichtigt das Besitzerfenster, dass ein QuickInfo-Steuerelement angezeigt wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                       |



 

### <a name="structures"></a>Strukturen



| Thema                                    | Inhalte                                                                                                                                                                                                                           |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) | Enthält Spezifische Informationen zu einem [NM \_ CUSTOMDRAW-Benachrichtigungscode,](nm-customdraw-tooltip.md) der von einem QuickInfo-Steuerelement gesendet wird. <br/>                                                                                           |
| [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa)     | Enthält Informationen zur Behandlung des [TTN \_ GETDISPINFO-Benachrichtigungscodes.](ttn-getdispinfo.md) Diese Struktur ersetzt die **TOOLTIPTEXT-Struktur.** <br/>                                                          |
| [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)             | Die [**TOOLINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) enthält Informationen zu einem Tool in einem QuickInfo-Steuerelement.<br/>                                                                                                                      |
| [**TTGLATTLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle)         | Stellt Informationen zum Titel eines QuickInfo-Steuerelements zur Verfügung. <br/>                                                                                                                                                             |
| [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa)   | Enthält Informationen, mit denen ein QuickInfo-Steuerelement bestimmt, ob sich ein Punkt im umgebundenen Rechteck des angegebenen Tools befindet. Wenn sich der Punkt im Rechteck befindet, empfängt die -Struktur Informationen zum Tool. <br/> |



 

### <a name="constants"></a>Konstanten



| Thema                                | Inhalte                                                                     |
|--------------------------------------|------------------------------------------------------------------------------|
| [QuickInfo-Stile](tooltip-styles.md) | In diesem Abschnitt werden die Steuerelementstile aufgeführt, die mit QuickInfo-Steuerelementen verwendet werden.<br/> |



 

 

 





