---
title: Pager
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit Pager-Steuerelementen verwendet werden.
ms.assetid: vs|controls|~\controls\pager\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21df98100ed649e4237c51bfcabf41420c49d004
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106340535"
---
# <a name="pager"></a>Pager

Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit Pager-Steuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                | Inhalte                                                                                                                                         |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pager-Steuerelemente](pager-controls.md) | Ein *Pager-Steuer* Element ist ein Fenster Container, der mit einem Fenster verwendet wird, das nicht über genügend Anzeigebereich verfügt, um den gesamten Inhalt anzuzeigen.<br/> |



 

### <a name="macros"></a>Makros



| Thema                                                 | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Pager- \_ forwardmaus**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse)     | Aktiviert oder deaktiviert die Maus Weiterleitung für das Pager-Steuerelement. Wenn die Maus Weiterleitung aktiviert ist, leitet das Pager-Steuerelement [**WM- \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Nachrichten an das enthaltene Fenster weiter. Sie können dieses Makro verwenden oder die [**PGM- \_ forwardmouse**](pgm-forwardmouse.md) -Nachricht explizit senden. <br/>                                                                                                                     |
| [**Pager \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor)         | Ruft die aktuelle Hintergrundfarbe für das Pager-Steuerelement ab. Sie können dieses Makro verwenden oder die [**PGM \_ GetBkColor**](pgm-getbkcolor.md) -Nachricht explizit senden. <br/>                                                                                                                                                                                                                                                                 |
| [**Pager \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder)           | Ruft die aktuelle Rahmengröße für das Pager-Steuerelement ab. Sie können dieses Makro verwenden oder die [**PGM \_ GetBorder**](pgm-getborder.md) -Nachricht explizit senden. <br/>                                                                                                                                                                                                                                                                        |
| [**Pager \_ getbuttonsize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize)   | Ruft die aktuelle Schaltflächen Größe für das Pager-Steuerelement ab. Sie können dieses Makro verwenden oder die [**PGM \_ getbuttonsize**](pgm-getbuttonsize.md) -Nachricht explizit senden. <br/>                                                                                                                                                                                                                                                                |
| [**Pager \_ GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) | Ruft den Zustand der angegebenen Schaltfläche in einem Pager-Steuerelement ab. Sie können dieses Makro verwenden oder die [**PGM \_ GetButtonState**](pgm-getbuttonstate.md) -Nachricht explizit senden. <br/>                                                                                                                                                                                                                                                       |
| [**Pager \_ getdroptarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget)   | Ruft den [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) -Schnittstellen Zeiger eines Pager-Steuer Elements ab. Sie können dieses Makro verwenden oder die [**PGM \_ getdroptarget**](pgm-getdroptarget.md) -Nachricht explizit senden. <br/>                                                                                                                                                                                                                                       |
| [**Pager- \_ GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos)                 | Ruft die aktuelle Bild Lauf Position des Pager-Steuer Elements ab. Sie können dieses Makro verwenden oder die [**PGM- \_ GetPos**](pgm-getpos.md) -Nachricht explizit senden. <br/>                                                                                                                                                                                                                                                                           |
| [**Pager \_ recalcsize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize)         | Erzwingt die Neuberechnung der Größe des enthaltenen Fensters durch das Pager-Steuerelement. Die Verwendung dieses Makros führt dazu, dass eine [PGN \_ calcsize](pgn-calcsize.md) -Benachrichtigung gesendet wird. Sie können dieses Makro verwenden oder die Nachricht " [**PGM \_ recalcsize**](pgm-recalcsize.md) " explizit senden. <br/>                                                                                                                                                        |
| [**Pager \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor)         | Legt die aktuelle Hintergrundfarbe für das Pager-Steuerelement fest. Sie können dieses Makro verwenden oder die [**PGM- \_ SetBkColor**](pgm-setbkcolor.md) -Nachricht explizit senden. <br/>                                                                                                                                                                                                                                                                      |
| [**Pager- \_ setborder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder)           | Legt die aktuelle Rahmengröße für das Pager-Steuerelement fest. Sie können dieses Makro verwenden oder die [**PGM- \_ setborder**](pgm-setborder.md) -Nachricht explizit senden. <br/>                                                                                                                                                                                                                                                                             |
| [**Pager \_ setbuttonsize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize)   | Legt die aktuelle Schaltflächen Größe für das Pager-Steuerelement fest. Sie können dieses Makro verwenden oder die [**PGM- \_ setbuttonsize**](pgm-setbuttonsize.md) -Nachricht explizit senden. <br/>                                                                                                                                                                                                                                                                     |
| [**Pager- \_ setchild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild)             | Legt das enthaltene Fenster für das Pager-Steuerelement fest. Mit diesem Makro wird das übergeordnete Element des enthaltenen Fensters nicht geändert. dem Pager-Steuerelement wird nur ein Fenster Handle für den Bildlauf zugewiesen. In den meisten Fällen ist das enthaltene Fenster ein untergeordnetes Fenster. Wenn dies der Fall ist, sollte das enthaltene Fenster dem Pager-Steuerelement untergeordnet sein. Sie können dieses Makro verwenden oder die [**PGM- \_ setchild**](pgm-setchild.md) -Nachricht explizit senden. <br/> |
| [**Pager- \_ SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos)                 | Legt die Scrollposition für das Pager-Steuerelement fest. Sie können dieses Makro verwenden oder die [**PGM- \_ SetPos**](pgm-setpos.md) -Nachricht explizit senden. <br/>                                                                                                                                                                                                                                                                                       |
| [**Pager \_ setScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)   | **Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen.**<br/> Legt die scrollparameter des Pager-Steuer Elements fest, einschließlich des Timeout Werts, der Zeilen pro Timeout und der Pixel pro Zeile. Sie können dieses Makro verwenden oder die [**PGM- \_ setsetscrollinfo**](pgm-setscrollinfo.md) -Nachricht explizit senden. <br/>                                                                                                  |



 

### <a name="messages"></a>Meldungen



| Thema                                              | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PGM \_ forwardmouse**](pgm-forwardmouse.md)      | Aktiviert oder deaktiviert die Maus Weiterleitung für das Pager-Steuerelement. Wenn die Maus Weiterleitung aktiviert ist, leitet das Pager-Steuerelement [**WM- \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Nachrichten an das enthaltene Fenster weiter. Sie können diese Nachricht explizit senden oder das [**Pager- \_ forwardmouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) -Makro verwenden. <br/>                                                                                                                       |
| [**PGM \_ GetBkColor**](pgm-getbkcolor.md)          | Ruft die aktuelle Hintergrundfarbe für das Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das [**Pager- \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) -Makro verwenden. <br/>                                                                                                                                                                                                                                                                   |
| [**PGM \_ GetBorder**](pgm-getborder.md)            | Ruft die aktuelle Rahmengröße für das Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das [**Pager- \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) -Makro verwenden. <br/>                                                                                                                                                                                                                                                                          |
| [**PGM \_ getbuttonsize**](pgm-getbuttonsize.md)    | Ruft die aktuelle Schaltflächen Größe für das Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das [**Pager- \_ getbuttonsize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) -Makro verwenden. <br/>                                                                                                                                                                                                                                                                  |
| [**PGM \_ GetButtonState**](pgm-getbuttonstate.md)  | Ruft den Zustand der angegebenen Schaltfläche in einem Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das [**Pager \_ GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) -Makro verwenden. <br/>                                                                                                                                                                                                                                                         |
| [**PGM \_ getdroptarget**](pgm-getdroptarget.md)    | Ruft den [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) -Schnittstellen Zeiger eines Pager-Steuer Elements ab. Sie können diese Nachricht explizit senden oder das [**Pager \_ getdroptarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) -Makro verwenden. <br/>                                                                                                                                                                                                                                         |
| [**PGM- \_ GetPos**](pgm-getpos.md)                  | Ruft die aktuelle Bild Lauf Position des Pager-Steuer Elements ab. Sie können diese Nachricht explizit senden oder das [**Pager- \_ GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) -Makro verwenden. <br/>                                                                                                                                                                                                                                                                             |
| [**PGM \_ recalcsize**](pgm-recalcsize.md)          | Erzwingt die Neuberechnung der Größe des enthaltenen Fensters durch das Pager-Steuerelement. Das Senden dieser Nachricht führt dazu, dass eine [PGN \_ calcsize](pgn-calcsize.md) -Benachrichtigung gesendet wird. Sie können diese Nachricht explizit senden oder das [**Pager \_ recalcsize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) -Makro verwenden. <br/>                                                                                                                                                      |
| [**PGM \_ SetBkColor**](pgm-setbkcolor.md)          | Legt die aktuelle Hintergrundfarbe für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das [**Pager- \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) -Makro verwenden. <br/>                                                                                                                                                                                                                                                                        |
| [**PGM- \_ setborder**](pgm-setborder.md)            | Legt die aktuelle Rahmengröße für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das [**Pager- \_ setborder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) -Makro verwenden. <br/>                                                                                                                                                                                                                                                                               |
| [**PGM \_ setbuttonsize**](pgm-setbuttonsize.md)    | Legt die aktuelle Schaltflächen Größe für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das [**Pager- \_ setbuttonsize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) -Makro verwenden. <br/>                                                                                                                                                                                                                                                                       |
| [**PGM- \_ setchild**](pgm-setchild.md)              | Legt das enthaltene Fenster für das Pager-Steuerelement fest. Mit dieser Meldung wird das übergeordnete Element des enthaltenen Fensters nicht geändert. dem Pager-Steuerelement wird nur ein Fenster Handle für den Bildlauf zugewiesen. In den meisten Fällen ist das enthaltene Fenster ein untergeordnetes Fenster. Wenn dies der Fall ist, sollte das enthaltene Fenster dem Pager-Steuerelement untergeordnet sein. Sie können diese Nachricht explizit senden oder das [**Pager-Element \_ setchild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) verwenden. <br/> |
| [**PGM- \_ SetPos**](pgm-setpos.md)                  | Legt die aktuelle Bild Lauf Position für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das [**Pager- \_ SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) -Makro verwenden. <br/>                                                                                                                                                                                                                                                                                 |
| [**PGM \_ setsetscrollinfo**](pgm-setscrollinfo.md) | **Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen.**<br/> Legt die scrollparameter des Pager-Steuer Elements fest, einschließlich des Timeout Werts, der Zeilen pro Timeout und der Pixel pro Zeile. Sie können diese Nachricht explizit oder mithilfe des [**Pager-Makros \_ setScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) senden. <br/>                                                                                                  |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                        | Inhalte                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ releasedcapture (Pager)](nm-releasedcapture-pager-.md) | Benachrichtigt das übergeordnete Fenster eines Pager-Steuer Elements, dass das Steuerelement die Maus Aufzeichnung freigegeben hat. NM \_ releasedcapture wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                |
| [PGN \_ calcsize](pgn-calcsize.md)                            | Benachrichtigung, die von einem Pager-Steuerelement gesendet wird, um die scrollbaren Dimensionen des enthaltenen Fensters abzurufen. Diese Dimensionen werden vom Pager-Steuerelement zum Bestimmen der scrollbaren Größe des enthaltenen Fensters verwendet. Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md) <br/> |
| [PGN- \_ hubänderung](pgn-hotitemchange.md)                  | Wird von einem Pager-Steuerelement gesendet, wenn sich das heiße (hervorgehobene) Element ändert. <br/>                                                                                                                                                                                                                               |
| [PGN- \_ Scroll](pgn-scroll.md)                                | Benachrichtigung, die von einem Pager-Steuerelement vor dem Rollup des enthaltenen Fensters gesendet wurde. Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md) <br/>                                                                                                                         |



 

### <a name="structures"></a>Strukturen



| Thema                                | Inhalte                                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nmpgcalcsize**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) | Enthält und empfängt Informationen, die das Pager-Steuerelement verwendet, um den scrollbaren Bereich des enthaltenen Fensters zu berechnen. Sie wird mit der [PGN \_ calcsize](pgn-calcsize.md) -Benachrichtigung verwendet. <br/> |
| [**Nmpghotitem**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem)   | Enthält Informationen, die mit der [PGN \_ ](pgn-hotitemchange.md) -Meldung "" angezeigt werden. <br/>                                                                                                |
| [**Nmpgscroll**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll)     | Enthält und empfängt Informationen, die das Pager-Steuerelement verwendet, wenn ein Bildlauf im enthaltenen Fenster erfolgt. Sie wird mit der [PGN- \_ scrollbenachrichtigung](pgn-scroll.md) verwendet. <br/>                          |



 

### <a name="constants"></a>Konstanten



| Thema                                            | Inhalte                                                                            |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [Pager-Steuerelement Stile](pager-control-styles.md) | In diesem Abschnitt werden die zum Erstellen von Pager-Steuerelementen verwendeten Fenster Stile aufgelistet. <br/> |



 

 

