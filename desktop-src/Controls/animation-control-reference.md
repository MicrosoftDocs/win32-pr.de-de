---
title: Animations Steuerelement
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit Animations Steuerelementen verwendet werden.
ms.assetid: 16994f93-e0fd-4c71-9c8a-15642408b8de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2a3fc7377c7258ba49b5a4188e6074270b5862
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474413"
---
# <a name="animation-control"></a>Animations Steuerelement

Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit Animations Steuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                                      | Inhalte                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu Animations Steuerelementen](animation-control-overview.md) | Ein *Animations Steuer* Element ist ein Fenster, in dem ein Audio-Video Interleaved (AVI)-Clip angezeigt wird. Ein AVI-Clip ist eine Reihe von bitmapframes, wie z. b. einem Film. Von Animations Steuerelementen können nur AVI-Clips angezeigt werden, die keine Audiodaten enthalten.<br/> |
| [Verwenden von Animations Steuerelementen](using-animation-control.md)    | Dieser Abschnitt enthält Implementierungsdetails und Beispielcode für Animations Steuerelemente.<br/>                                                                                                                                      |



 

### <a name="macros"></a>Makros



| Thema                                           | Inhalte                                                                                                                                                                                                                                                          |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Schließen animieren**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)         | Schließt einen AVI-Clip. Sie können dieses Makro verwenden oder die [**\_ geöffnete ACM**](acm-open.md) -Nachricht explizit senden und dabei **null** -Parameter übergeben. <br/>                                                                                                              |
| [**Animieren \_ Erstellen**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create)       | Erstellt ein Animations Steuerelement. [**Animieren \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) Ruft die Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " auf, um das Animations Steuerelement zu erstellen. <br/>                                                                                   |
| [**Animieren von \_ isplay**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) | Prüft, ob ein AVI-Clip wiedergegeben wird. Sie können dieses Makro verwenden oder eine [**ACM- \_ isplay**](acm-isplaying.md) -Nachricht senden.<br/>                                                                                                                            |
| [**\_Geöffnetes animieren**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open)           | Öffnet einen AVI-Clip und zeigt seinen ersten Frame in einem Animations Steuerelement an. Sie können dieses Makro verwenden oder die [**\_ geöffnete ACM**](acm-open.md) -Nachricht explizit senden. <br/>                                                                                          |
| [**Animieren von \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex)       | Öffnet einen AVI-Clip aus einer Ressource in einem angegebenen Modul und zeigt seinen ersten Frame in einem Animations Steuerelement an. Sie können dieses Makro verwenden oder die [**\_ geöffnete ACM**](acm-open.md) -Nachricht explizit senden. <br/>                                                    |
| [**\_Spielen animieren**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)           | Gibt einen AVI-Clip in einem Animations Steuerelement wieder. Das-Steuerelement spielt den Clip im Hintergrund, während der Thread weiterhin ausgeführt wird. Sie können dieses Makro verwenden oder die [**ACM- \_ Wiedergabe**](acm-play.md) Nachricht explizit senden. <br/>                                    |
| [**Animieren \_ animieren**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek)           | Weist ein Animations Steuerelement an, einen bestimmten Rahmen eines AVI-Clips anzuzeigen. Das-Steuerelement zeigt den Clip im Hintergrund an, während der Thread weiterhin ausgeführt wird. Sie können dieses Makro verwenden oder die [**ACM- \_ Wiedergabe**](acm-play.md) Nachricht explizit senden. <br/> |
| [**Animation \_ animieren**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)           | Beendet die Wiedergabe eines AVI-Clips in einem Animations Steuerelement. Sie können dieses Makro verwenden oder die [**ACM- \_ Stoppnachricht**](acm-stop.md) explizit senden. <br/>                                                                                                               |



 

### <a name="messages"></a>Meldungen



| Thema                                   | Inhalte                                                                                                                                                                                                                                   |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACM \_ isplay**](acm-isplaying.md) | Überprüft, ob ein AVI-Clip wiedergegeben wird. Sie können diese Nachricht explizit senden oder das [**Animieren von \_ isplay**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) -Makro verwenden.<br/>                                                                                   |
| [**ACM \_ geöffnet**](acm-open.md)           | Öffnet einen AVI-Clip und zeigt seinen ersten Frame in einem Animations Steuerelement an. Sie können diese Nachricht explizit senden oder das Makro [**animieren \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) oder [**animieren \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) verwenden. <br/>              |
| [**ACM \_ Play**](acm-play.md)           | Gibt einen AVI-Clip in einem Animations Steuerelement wieder. Das-Steuerelement spielt den Clip im Hintergrund, während der Thread weiterhin ausgeführt wird. Sie können diese Nachricht explizit oder mit dem [**animieren \_ Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) -Makro senden.<br/> |
| [**ACM \_ anzuhalten**](acm-stop.md)           | Beendet die Wiedergabe eines AVI-Clips in einem Animations Steuerelement. Sie können diese Nachricht explizit oder mithilfe des Makros [**animieren- \_ Ende**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) senden.<br/>                                                                            |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                           | Inhalte                                                                                                                                                                                                       |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACN \_ starten**](acn-start.md) | Benachrichtigt das übergeordnete Fenster eines Animations Steuer Elements, dass der zugehörige AVI-Clip mit der Wiedergabe begonnen hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht gesendet. <br/>      |
| [**ACN \_ stoppt**](acn-stop.md)   | Benachrichtigt das übergeordnete Fenster eines Animations Steuer Elements, dass der zugehörige AVI-Clip beendet wurde. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht gesendet. <br/> |



 

### <a name="constants"></a>Konstanten



| Thema                                                        | Inhalte                                                                      |
|--------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**Animations Steuerelement Stile**](animation-control-styles.md) | In diesem Abschnitt werden die mit Animations Steuerelementen verwendeten Fenster Stile aufgelistet.<br/> |



 

 

