---
title: Animationssteuerelement
description: Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit Animationssteuerelementen verwendet werden.
ms.assetid: 16994f93-e0fd-4c71-9c8a-15642408b8de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7241199dc92004f9b3616e2666dd96eadbf43fc6c4dfe9081369e13cca26e082
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921780"
---
# <a name="animation-control"></a>Animationssteuerelement

Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit Animationssteuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                                      | Inhalte                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu Animationssteuerelementen](animation-control-overview.md) | Ein *Animationssteuerelement* ist ein Fenster, in dem ein Audio-Video AVI-Clip (Interleaved) angezeigt wird. Ein AVI-Clip ist eine Reihe von Bitmapframes wie ein Film. Animationssteuerelemente können nur AVI-Clips anzeigen, die keine Audiodaten enthalten.<br/> |
| [Verwenden von Animationssteuerelementen](using-animation-control.md)    | Dieser Abschnitt enthält Implementierungsdetails und Beispielcode für Animationssteuerelemente.<br/>                                                                                                                                      |



 

### <a name="macros"></a>Makros



| Thema                                           | Inhalte                                                                                                                                                                                                                                                          |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Schließen animieren**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)         | Schließt einen AVI-Clip. Sie können dieses Makro verwenden oder die [**ACM \_ OPEN-Nachricht**](acm-open.md) explizit senden und **NULL-Parameter** übergeben. <br/>                                                                                                              |
| [**Animieren \_ der Erstellung**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create)       | Erstellt ein Animationssteuerelement. [**Animieren \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) ruft die [**CreateWindow-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowa) auf, um das Animationssteuerelement zu erstellen. <br/>                                                                                   |
| [**\_IsPlaying animieren**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) | Überprüft, ob ein AVI-Clip wiedergegeben wird. Sie können dieses Makro verwenden oder eine [**ACM \_ ISPLAYING-Nachricht**](acm-isplaying.md) senden.<br/>                                                                                                                            |
| [**Öffnen animieren \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open)           | Öffnet einen AVI-Clip und zeigt seinen ersten Frame in einem Animationssteuerelement an. Sie können dieses Makro verwenden oder die [**ACM \_ OPEN-Nachricht**](acm-open.md) explizit senden. <br/>                                                                                          |
| [**Animieren von \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex)       | Öffnet einen AVI-Clip aus einer Ressource in einem angegebenen Modul und zeigt seinen ersten Frame in einem Animationssteuerelement an. Sie können dieses Makro verwenden oder die [**ACM \_ OPEN-Nachricht**](acm-open.md) explizit senden. <br/>                                                    |
| [**Animieren \_ der Wiedergabe**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)           | Gibt einen AVI-Clip in einem Animationssteuerelement wieder. Das -Steuerelement gibt den Clip im Hintergrund wieder, während die Ausführung des Threads fortgesetzt wird. Sie können dieses Makro verwenden oder die [**ACM \_ PLAY-Nachricht**](acm-play.md) explizit senden. <br/>                                    |
| [**\_Animieren von Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek)           | Weist ein Animationssteuerelement an, einen bestimmten Frame eines AVI-Clips anzuzeigen. Das -Steuerelement zeigt den Clip im Hintergrund an, während der Thread weiterhin ausgeführt wird. Sie können dieses Makro verwenden oder die [**ACM \_ PLAY-Nachricht**](acm-play.md) explizit senden. <br/> |
| [**\_Animieren eines Stopps**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)           | Beendet die Wiedergabe eines AVI-Clips in einem Animationssteuerelement. Sie können dieses Makro verwenden oder die [**ACM \_ STOP-Nachricht**](acm-stop.md) explizit senden. <br/>                                                                                                               |



 

### <a name="messages"></a>Meldungen



| Thema                                   | Inhalte                                                                                                                                                                                                                                   |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACM \_ ISPLAYING**](acm-isplaying.md) | Überprüft, ob ein AVI-Clip wiedergegeben wird. Sie können diese Nachricht explizit senden oder das [**Makro \_ "IsPlaying animieren"**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) verwenden.<br/>                                                                                   |
| [**ACM \_ OPEN**](acm-open.md)           | Öffnet einen AVI-Clip und zeigt seinen ersten Frame in einem Animationssteuerelement an. Sie können diese Nachricht explizit senden oder das [**Makro "Animieren \_ öffnen"**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) oder [**\_ "Animieren von OpenEx"**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) verwenden. <br/>              |
| [**ACM \_ PLAY**](acm-play.md)           | Gibt einen AVI-Clip in einem Animationssteuerelement wieder. Das -Steuerelement gibt den Clip im Hintergrund wieder, während die Ausführung des Threads fortgesetzt wird. Sie können diese Nachricht explizit oder mithilfe des [**Makros \_ "Animieren von Wiedergabe"**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) senden.<br/> |
| [**\_ACM-BEENDIGUNG**](acm-stop.md)           | Beendet die Wiedergabe eines AVI-Clips in einem Animationssteuerelement. Sie können diese Nachricht explizit oder mithilfe des [**Makros \_ "Beenden animieren"**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) senden.<br/>                                                                            |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                           | Inhalte                                                                                                                                                                                                       |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACN \_ START**](acn-start.md) | Benachrichtigt das übergeordnete Fenster eines Animationssteuerelements, dass die Wiedergabe des zugeordneten AVI-Clips begonnen hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ COMMAND-Nachricht**](/windows/desktop/menurc/wm-command) gesendet. <br/>      |
| [**ACN \_ STOP**](acn-stop.md)   | Benachrichtigt das übergeordnete Fenster eines Animationssteuerelements, dass die Wiedergabe des zugeordneten AVI-Clips beendet wurde. Dieser Benachrichtigungscode wird in Form einer [**WM \_ COMMAND-Nachricht**](/windows/desktop/menurc/wm-command) gesendet. <br/> |



 

### <a name="constants"></a>Konstanten



| Thema                                                        | Inhalte                                                                      |
|--------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**Animationssteuerelementstile**](animation-control-styles.md) | In diesem Abschnitt werden die mit Animationssteuerelementen verwendeten Fensterstile aufgelistet.<br/> |



 

 

