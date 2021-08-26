---
title: Pager
description: Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit Pagersteuerelementen verwendet werden.
ms.assetid: vs|controls|~\controls\pager\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bf9860c9e1dd1d565b24c7bbfc02e46480198f5bdea03717288abc83591a7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914770"
---
# <a name="pager"></a>Pager

Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit Pagersteuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                | Inhalte                                                                                                                                         |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pagersteuerelemente](pager-controls.md) | Ein *Pagersteuerelement* ist ein Fenstercontainer, der mit einem Fenster verwendet wird, das nicht über genügend Anzeigebereich verfügt, um seinen gesamten Inhalt anzuzeigen.<br/> |



 

### <a name="macros"></a>Makros



| Thema                                                 | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Pager \_ ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse)     | Aktiviert oder deaktiviert die Mausweiterleitung für das Pagersteuerelement. Wenn die Mausweiterleitung aktiviert ist, leitet das Pager-Steuerelement [**WM \_ MOUSEMOVE-Meldungen**](/windows/desktop/inputdev/wm-mousemove) an das enthaltene Fenster weiter. Sie können dieses Makro verwenden oder die [**PGM \_ FORWARDMOUSE-Nachricht**](pgm-forwardmouse.md) explizit senden. <br/>                                                                                                                     |
| [**Pager \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor)         | Ruft die aktuelle Hintergrundfarbe für das Pagersteuerelement ab. Sie können dieses Makro verwenden oder die [**PGM \_ GETBKCOLOR-Nachricht**](pgm-getbkcolor.md) explizit senden. <br/>                                                                                                                                                                                                                                                                 |
| [**Pager \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder)           | Ruft die aktuelle Rahmengröße für das Pagersteuerelement ab. Sie können dieses Makro verwenden oder die [**PGM \_ GETBORDER-Nachricht**](pgm-getborder.md) explizit senden. <br/>                                                                                                                                                                                                                                                                        |
| [**Pager \_ GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize)   | Ruft die aktuelle Schaltflächengröße für das Pagersteuerelement ab. Sie können dieses Makro verwenden oder die [**PGM \_ GETBUTTONSIZE-Nachricht**](pgm-getbuttonsize.md) explizit senden. <br/>                                                                                                                                                                                                                                                                |
| [**Pager \_ GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) | Ruft den Zustand der angegebenen Schaltfläche in einem Pagersteuerelement ab. Sie können dieses Makro verwenden oder die [**PGM \_ GETBUTTONSTATE-Nachricht**](pgm-getbuttonstate.md) explizit senden. <br/>                                                                                                                                                                                                                                                       |
| [**Pager \_ GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget)   | Ruft den [**IDropTarget-Schnittstellenzeiger**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) eines Pagersteuerelements ab. Sie können dieses Makro verwenden oder die [**PGM \_ GETDROPTARGET-Nachricht**](pgm-getdroptarget.md) explizit senden. <br/>                                                                                                                                                                                                                                       |
| [**Pager \_ GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos)                 | Ruft die aktuelle Bildlaufposition des Pagersteuerelements ab. Sie können dieses Makro verwenden oder die [**PGM \_ GETPOS-Nachricht**](pgm-getpos.md) explizit senden. <br/>                                                                                                                                                                                                                                                                           |
| [**Pager \_ RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize)         | Erzwingt, dass das Pagersteuerelement die Größe des enthaltenen Fensters neu berechnet. Die Verwendung dieses Makros führt dazu, dass eine [PGN-CALCSIZE-Benachrichtigung \_ ](pgn-calcsize.md) gesendet wird. Sie können dieses Makro verwenden oder die [**PGM \_ RECALCSIZE-Nachricht**](pgm-recalcsize.md) explizit senden. <br/>                                                                                                                                                        |
| [**Pager \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor)         | Legt die aktuelle Hintergrundfarbe für das Pagersteuerelement fest. Sie können dieses Makro verwenden oder die [**PGM \_ SETBKCOLOR-Nachricht**](pgm-setbkcolor.md) explizit senden. <br/>                                                                                                                                                                                                                                                                      |
| [**Pager \_ SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder)           | Legt die aktuelle Rahmengröße für das Pagersteuerelement fest. Sie können dieses Makro verwenden oder die [**PGM \_ SETBORDER-Nachricht**](pgm-setborder.md) explizit senden. <br/>                                                                                                                                                                                                                                                                             |
| [**Pager \_ SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize)   | Legt die aktuelle Schaltflächengröße für das Pagersteuerelement fest. Sie können dieses Makro verwenden oder die [**PGM \_ SETBUTTONSIZE-Nachricht**](pgm-setbuttonsize.md) explizit senden. <br/>                                                                                                                                                                                                                                                                     |
| [**Pager \_ SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild)             | Legt das enthaltene Fenster für das Pagersteuerelement fest. Dieses Makro ändert nicht das übergeordnete Element des enthaltenen Fensters. es weist dem Pagersteuerelement nur ein Fensterhandle für das Scrollen zu. In den meisten Fällen ist das enthaltene Fenster ein untergeordnetes Fenster. Wenn dies der Fall ist, sollte das enthaltene Fenster ein untergeordnetes Element des Pagersteuerelements sein. Sie können dieses Makro verwenden oder die [**PGM \_ SETCHILD-Nachricht**](pgm-setchild.md) explizit senden. <br/> |
| [**Pager \_ SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos)                 | Legt die Bildlaufposition für das Pagersteuerelement fest. Sie können dieses Makro verwenden oder die [**PGM \_ SETPOS-Nachricht**](pgm-setpos.md) explizit senden. <br/>                                                                                                                                                                                                                                                                                       |
| [**Pager \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)   | **Für die interne Verwendung vorgesehen; nicht für die Verwendung in Anwendungen empfohlen.**<br/> Legt die Scrollparameter des Pagersteuerelements fest, einschließlich des Timeoutwerts, der Zeilen pro Timeout und der Pixel pro Zeile. Sie können dieses Makro verwenden oder die [**PGM \_ SETSETSCROLLINFO-Nachricht**](pgm-setscrollinfo.md) explizit senden. <br/>                                                                                                  |



 

### <a name="messages"></a>Meldungen



| Thema                                              | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PGM \_ FORWARDMOUSE**](pgm-forwardmouse.md)      | Aktiviert oder deaktiviert die Mausweiterleitung für das Pagersteuerelement. Wenn die Mausweiterleitung aktiviert ist, leitet das Pager-Steuerelement [**WM \_ MOUSEMOVE-Meldungen**](/windows/desktop/inputdev/wm-mousemove) an das enthaltene Fenster weiter. Sie können diese Nachricht explizit senden oder das [**Pager \_ ForwardMouse-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) verwenden. <br/>                                                                                                                       |
| [**PGM \_ GETBKCOLOR**](pgm-getbkcolor.md)          | Ruft die aktuelle Hintergrundfarbe für das Pagersteuerelement ab. Sie können diese Nachricht explizit senden oder das [**Pager-Makro \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) verwenden. <br/>                                                                                                                                                                                                                                                                   |
| [**PGM \_ GETBORDER**](pgm-getborder.md)            | Ruft die aktuelle Rahmengröße für das Pagersteuerelement ab. Sie können diese Nachricht explizit senden oder das [**Pager-Makro \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) verwenden. <br/>                                                                                                                                                                                                                                                                          |
| [**PGM \_ GETBUTTONSIZE**](pgm-getbuttonsize.md)    | Ruft die aktuelle Schaltflächengröße für das Pagersteuerelement ab. Sie können diese Nachricht explizit senden oder das [**Pager-Makro \_ GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) verwenden. <br/>                                                                                                                                                                                                                                                                  |
| [**PGM \_ GETBUTTONSTATE**](pgm-getbuttonstate.md)  | Ruft den Zustand der angegebenen Schaltfläche in einem Pagersteuerelement ab. Sie können diese Nachricht explizit senden oder das [**\_ Pager-Makro GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) verwenden. <br/>                                                                                                                                                                                                                                                         |
| [**PGM \_ GETDROPTARGET**](pgm-getdroptarget.md)    | Ruft den [**IDropTarget-Schnittstellenzeiger**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) eines Pagersteuerelements ab. Sie können diese Nachricht explizit senden oder das [**Pager-Makro \_ GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) verwenden. <br/>                                                                                                                                                                                                                                         |
| [**PGM \_ GETPOS**](pgm-getpos.md)                  | Ruft die aktuelle Bildlaufposition des Pagersteuerelements ab. Sie können diese Nachricht explizit senden oder das [**Pager \_ GetPos-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) verwenden. <br/>                                                                                                                                                                                                                                                                             |
| [**PGM \_ RECALCSIZE**](pgm-recalcsize.md)          | Erzwingt, dass das Pagersteuerelement die Größe des enthaltenen Fensters neu berechnet. Das Senden dieser Nachricht führt dazu, dass eine [PGN-CALCSIZE-Benachrichtigung \_ ](pgn-calcsize.md) gesendet wird. Sie können diese Nachricht explizit senden oder das [**Pager \_ RecalcSize-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) verwenden. <br/>                                                                                                                                                      |
| [**PGM \_ SETBKCOLOR**](pgm-setbkcolor.md)          | Legt die aktuelle Hintergrundfarbe für das Pagersteuerelement fest. Sie können diese Nachricht explizit senden oder das [**\_ Pager-Makro SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) verwenden. <br/>                                                                                                                                                                                                                                                                        |
| [**PGM \_ SETBORDER**](pgm-setborder.md)            | Legt die aktuelle Rahmengröße für das Pagersteuerelement fest. Sie können diese Nachricht explizit senden oder das [**\_ Pager-Makro SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) verwenden. <br/>                                                                                                                                                                                                                                                                               |
| [**PGM \_ SETBUTTONSIZE**](pgm-setbuttonsize.md)    | Legt die aktuelle Schaltflächengröße für das Pagersteuerelement fest. Sie können diese Nachricht explizit senden oder das [**\_ Pager-Makro SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) verwenden. <br/>                                                                                                                                                                                                                                                                       |
| [**PGM \_ SETCHILD**](pgm-setchild.md)              | Legt das enthaltene Fenster für das Pagersteuerelement fest. Diese Meldung ändert nicht das übergeordnete Element des enthaltenen Fensters. es weist dem Pagersteuerelement nur ein Fensterhandle für das Scrollen zu. In den meisten Fällen ist das enthaltene Fenster ein untergeordnetes Fenster. Wenn dies der Fall ist, sollte das enthaltene Fenster ein untergeordnetes Element des Pagersteuerelements sein. Sie können diese Nachricht explizit senden oder das [**\_ Pager-Makro SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) verwenden. <br/> |
| [**PGM \_ SETPOS**](pgm-setpos.md)                  | Legt die aktuelle Bildlaufposition für das Pagersteuerelement fest. Sie können diese Nachricht explizit senden oder das [**Pager \_ SetPos-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) verwenden. <br/>                                                                                                                                                                                                                                                                                 |
| [**PGM \_ SETSETSCROLLINFO**](pgm-setscrollinfo.md) | **Für die interne Verwendung vorgesehen; nicht für die Verwendung in Anwendungen empfohlen.**<br/> Legt die Scrollparameter des Pagersteuerelements fest, einschließlich des Timeoutwerts, der Zeilen pro Timeout und der Pixel pro Zeile. Sie können diese Nachricht explizit oder mithilfe des [**\_ Pager-Makros SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) senden. <br/>                                                                                                  |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                        | Inhalte                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ RELEASEDCAPTURE (Pager)](nm-releasedcapture-pager-.md) | Benachrichtigt das übergeordnete Fenster eines Pagersteuerelements, dass das Steuerelement die Mausaufnahme freigegeben hat. NM \_ RELEASEDCAPTURE wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                                |
| [PGN \_ CALCSIZE](pgn-calcsize.md)                            | Benachrichtigung, die von einem Pagersteuerelement gesendet wird, um die bildlauffähigen Dimensionen des enthaltenen Fensters abzurufen. Diese Dimensionen werden vom Pagersteuerelement verwendet, um die bildlauffähige Größe des enthaltenen Fensters zu bestimmen. Diese Benachrichtigung wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/> |
| [PGN \_ HOTITEMCHANGE](pgn-hotitemchange.md)                  | Wird von einem Pagersteuerelement gesendet, wenn sich das heiße (hervorgehobene) Element ändert. <br/>                                                                                                                                                                                                                               |
| [PGN \_ SCROLL](pgn-scroll.md)                                | Benachrichtigung, die von einem Pagersteuerelement gesendet wird, bevor das enthaltene Fenster gescrollt wird. Diese Benachrichtigung wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                                         |



 

### <a name="structures"></a>Strukturen



| Thema                                | Inhalte                                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) | Enthält und empfängt Informationen, die das Pagersteuerelement verwendet, um den bildlauffähigen Bereich des enthaltenen Fensters zu berechnen. Sie wird mit der [PGN-CALCSIZE-Benachrichtigung \_ ](pgn-calcsize.md) verwendet. <br/> |
| [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem)   | Enthält Informationen, die mit der [PGN \_ HOTITEMCHANGE-Benachrichtigung](pgn-hotitemchange.md) verwendet werden. <br/>                                                                                                |
| [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll)     | Enthält Und empfängt Informationen, die das Pagersteuerelement beim Scrollen im enthaltenen Fenster verwendet. Sie wird mit der [PGN \_ SCROLL-Benachrichtigung](pgn-scroll.md) verwendet. <br/>                          |



 

### <a name="constants"></a>Konstanten



| Thema                                            | Inhalte                                                                            |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [Pager-Steuerelementstile](pager-control-styles.md) | In diesem Abschnitt werden die Fensterstile aufgelistet, die beim Erstellen von Pagersteuerelementen verwendet werden. <br/> |



 

 

