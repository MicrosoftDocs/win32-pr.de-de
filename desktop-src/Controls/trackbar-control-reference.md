---
title: Trackbar
description: Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit Trackbar-Steuerelementen verwendet werden.
ms.assetid: vs|controls|~\controls\trackbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f56c5a483340a8e77ef0df6503481d3cbc50e51a85bd07258cdf283dd563c6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060540"
---
# <a name="trackbar"></a>Trackbar

Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit Trackbar-Steuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                                  | Inhalte                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu Trackbar-Steuerelementen](trackbar-controls.md)       | Eine Trackbar ist ein Fenster, das einen Schieberegler (manchmal als Strich bezeichnet) in einem Kanal und optionale Teilstriche enthält. Wenn der Benutzer den Schieberegler mit der Maus oder den Richtungsschlüsseln bewegt, sendet die Trackleiste Benachrichtigungsmeldungen, um die Änderung anzugeben.<br/> |
| [Verwenden von Trackbar-Steuerelementen](using-trackbar-controls.md) | Dieser Abschnitt enthält Implementierungsdetails und Beispiele für Trackbar-Steuerelemente.<br/>                                                                                                                                                                               |



 

### <a name="messages"></a>Meldungen



| Thema                                                 | Inhalte                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TBM \_ CLEARSEL**](tbm-clearsel.md)                 | Löschen des aktuellen Auswahlbereichs in einer Trackleiste. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ CLEARTICS**](tbm-cleartics.md)               | Entfernt die aktuellen Teilstriche aus einer Trackleiste. Diese Meldung entfernt nicht die ersten und letzten Teilstriche, die automatisch von der Trackleiste erstellt werden. <br/>                                                                                                                                           |
| [**TBM \_ GETBUDDY**](tbm-getbuddy.md)                 | Ruft das Handle in ein Trackbar-Steuerelement-Fenster an einer bestimmten Position ab. Die angegebene Position ist relativ zur Ausrichtung des Steuerelements (horizontal oder vertikal). <br/>                                                                                                                                 |
| [**TBM \_ GETCHANNELRECT**](tbm-getchannelrect.md)     | Ruft die Größe und Position des umgebundenen Rechtecks für den Kanal einer Trackleiste ab. (Der Kanal ist der Bereich, über den sich der Schieberegler bewegt. Sie enthält die Hervorhebung, wenn ein Bereich ausgewählt wird.) <br/>                                                                                                         |
| [**TBM \_ GETLINESIZE**](tbm-getlinesize.md)           | Ruft die Anzahl der logischen Positionen ab, die der Schieberegler der Trackleiste als Reaktion auf Tastatureingaben über die Pfeiltasten bewegt, z. B. die Tasten oder . Die logischen Positionen sind die ganzzahligen Inkremente im Bereich der minimalen bis maximalen Schiebereglerpositionen der Trackleiste. <br/>                                         |
| [**TBM \_ GETNUMTICS**](tbm-getnumtics.md)             | Ruft die Anzahl der Teilstriche in einer Trackleiste ab. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ GETPAGESIZE**](tbm-getpagesize.md)           | Ruft die Anzahl logischer Positionen ab, die der Schieberegler der Trackleiste als Reaktion auf Tastatureingaben bewegt, z. B. die Tasten oder oder Mauseingaben, z. B. Klicks im Kanal der Trackleiste. Die logischen Positionen sind die ganzzahligen Inkremente im Bereich der minimalen bis maximalen Schiebereglerpositionen der Trackleiste. <br/>   |
| [**TBM \_ GETPOS**](tbm-getpos.md)                     | Ruft die aktuelle logische Position des Schiebereglers in einer Trackleiste ab. Die logischen Positionen sind die ganzzahligen Werte im Bereich von minimalen bis maximalen Schiebereglerpositionen der Trackleiste. <br/>                                                                                                                       |
| [**TBM \_ GETPTICS**](tbm-getptics.md)                 | Ruft die Adresse eines Arrays ab, das die Positionen der Teilstriche für eine Trackleiste enthält. <br/>                                                                                                                                                                                                        |
| [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md)           | Ruft die maximale Position für den Schieberegler in einer Trackleiste ab. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md)           | Ruft die Mindestposition für den Schieberegler in einer Trackleiste ab. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ GETSELEND**](tbm-getselend.md)               | Ruft die Endposition des aktuellen Auswahlbereichs in einer Trackleiste ab. <br/>                                                                                                                                                                                                                            |
| [**TBM \_ GETSELSTART**](tbm-getselstart.md)           | Ruft die Anfangsposition des aktuellen Auswahlbereichs in einer Trackleiste ab. <br/>                                                                                                                                                                                                                          |
| [**TBM \_ GETTHUMBLENGTH**](tbm-getthumblength.md)     | Ruft die Länge des Schiebereglers in einer Trackleiste ab. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ GETTHUMBRECT**](tbm-getthumbrect.md)         | Ruft die Größe und Position des umgebundenen Rechtecks für den Schieberegler in einer Trackleiste ab. <br/>                                                                                                                                                                                                                |
| [**TBM \_ GETTIC**](tbm-gettic.md)                     | Ruft die logische Position eines Teilstrichs in einer Trackleiste ab. Die logische Position kann einer der ganzzahligen Werte im Bereich von minimalen bis maximalen Schiebereglerpositionen der Trackleiste sein. <br/>                                                                                                                     |
| [**TBM \_ GETTICPOS**](tbm-getticpos.md)               | Ruft die aktuelle physische Position eines Teilstrichs in einer Trackleiste ab.<br/>                                                                                                                                                                                                                                   |
| [**TBM \_ GETTOOLTIPS**](tbm-gettooltips.md)           | Ruft das Handle für das QuickInfo-Steuerelement ab, das der Trackleiste zugewiesen ist(sofern verfügbar). <br/>                                                                                                                                                                                                                          |
| [**TBM \_ GETUNICODEFORMAT**](tbm-getunicodeformat.md) | Ruft das Unicode-Zeichenformatflag für das Steuerelement ab. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ SETBUDDY**](tbm-setbuddy.md)                 | Weist ein Fenster als Fenster für ein Trackbar-Steuerelement zu. Trackbar-Fenster werden automatisch an einer Position relativ zur Ausrichtung des Steuerelements (horizontal oder vertikal) angezeigt. <br/>                                                                                                          |
| [**TBM \_ SETLINESIZE**](tbm-setlinesize.md)           | Legt die Anzahl der logischen Positionen fest, die der Schieberegler der Trackleiste als Reaktion auf Tastatureingaben über die Pfeiltasten bewegt, z. B. die Tasten oder . Die logischen Positionen sind die ganzzahligen Inkremente im Bereich der minimalen bis maximalen Schiebereglerpositionen der Trackleiste. <br/>                                              |
| [**TBM \_ SETPAGESIZE**](tbm-setpagesize.md)           | Legt die Anzahl der logischen Positionen fest, die der Schieberegler der Trackleiste als Reaktion auf Tastatureingaben bewegt, z. B. die Tasten oder oder Mauseingaben, z. B. Klicks im Kanal der Trackleiste. Die logischen Positionen sind die ganzzahligen Inkremente im Bereich der minimalen bis maximalen Schiebereglerpositionen der Trackleiste. <br/>        |
| [**TBM \_ SETPOS**](tbm-setpos.md)                     | Legt die aktuelle logische Position des Schiebereglers in einer Trackleiste fest. <br/>                                                                                                                                                                                                                                         |
| [**TBM \_ SETPOSNOTIFY**](tbm-setposnotify.md)         | Legt die aktuelle logische Position des Schiebereglers in einer Trackleiste fest. <br/>                                                                                                                                                                                                                                         |
| [**TBM \_ SETRANGE**](tbm-setrange.md)                 | Legt den Bereich der minimalen und maximalen logischen Positionen für den Schieberegler in einer Trackleiste fest. <br/>                                                                                                                                                                                                                  |
| [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)           | Legt die maximale logische Position für den Schieberegler in einer Trackleiste fest. <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)           | Legt die minimale logische Position für den Schieberegler in einer Trackleiste fest. <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ SETSEL**](tbm-setsel.md)                     | Legt die Anfangs- und Endpositionen für den verfügbaren Auswahlbereich in einer Trackleiste fest. <br/>                                                                                                                                                                                                                |
| [**TBM \_ SETSELEND**](tbm-setselend.md)               | Legt die logische Endposition des aktuellen Auswahlbereichs in einer Trackleiste fest. Diese Meldung wird ignoriert, wenn die Trackleiste nicht über den [**TBS \_ ENABLESELRANGE-Stil**](trackbar-control-styles.md) verfügt. <br/>                                                                              |
| [**TBM \_ SETSELSTART**](tbm-setselstart.md)           | Legt die logische Anfangsposition des aktuellen Auswahlbereichs in einer Trackleiste fest. Diese Meldung wird ignoriert, wenn die Trackleiste nicht über den [**TBS \_ ENABLESELRANGE-Stil**](trackbar-control-styles.md) verfügt. <br/>                                                                            |
| [**TBM \_ SETTHUMBLENGTH**](tbm-setthumblength.md)     | Legt die Länge des Schiebereglers in einer Trackleiste fest. Diese Meldung wird ignoriert, wenn die Trackleiste nicht über das [**TBS \_ FIXEDLENGTH-Format**](trackbar-control-styles.md) verfügt. <br/>                                                                                                                      |
| [**TBM \_ SETTIC**](tbm-settic.md)                     | Legt einen Teilstrich in einer Trackleiste an der angegebenen logischen Position fest. <br/>                                                                                                                                                                                                                                      |
| [**TBM \_ SETTICFREQ**](tbm-setticfreq.md)             | Legt die Intervallhäufigkeit für Teilstriche in einer Trackleiste fest. Wenn die Häufigkeit beispielsweise auf zwei festgelegt ist, wird für jedes andere Inkrement im Bereich der Trackleiste ein Teilstrich angezeigt. Die Standardeinstellung für die Häufigkeit ist 1. Das heißt, jedes Inkrement im Bereich ist einem Teilstrich zugeordnet. <br/> |
| [**TBM \_ SETTIPSIDE**](tbm-settipside.md)             | Positioniert ein QuickInfo-Steuerelement, das von einem Trackbar-Steuerelement verwendet wird. Trackbar-Steuerelemente, die die QuickInfos zum Anzeigen des [**\_ TBS-QUICKInfos-Stils**](trackbar-control-styles.md) verwenden. <br/>                                                                                                                           |
| [**TBM \_ SETTOOLTIPS**](tbm-settooltips.md)           | Weist einem Trackbar-Steuerelement ein QuickInfo-Steuerelement zu. <br/>                                                                                                                                                                                                                                                       |
| [**TBM \_ SETUNICODEFORMAT**](tbm-setunicodeformat.md) | Legt das Unicode-Zeichenformatflag für das Steuerelement fest. Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen. <br/>                                                                                                               |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                              | Inhalte                                                                                                                                                                                      |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (Trackbar)](nm-customdraw-trackbar.md)            | Wird von einem Trackbar-Steuerelement gesendet, um seine übergeordneten Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>        |
| [NM \_ RELEASEDCAPTURE (Trackbar)](nm-releasedcapture-trackbar-.md) | Benachrichtigt das übergeordnete Fenster eines Trackbar-Steuerelements, dass das Steuerelement die Mauserfassung frei gibt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/> |
| [TRBN \_ THUMBPOSCHANGEING](trbn-thumbposchanging.md)                | Benachrichtigt, dass sich die Position des Fingerabdrucks auf einer Trackleiste ändert. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/>                               |



 

### <a name="constants"></a>Konstanten



| Thema                                                  | Inhalte                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Benutzerdefinierte Zeichnen-Werte](custom-draw-values.md)           | In diesem Abschnitt werden die Werte aufgeführt, die zum Identifizieren der Teile eines Trackbar-Steuerelements verwendet werden. <br/>      |
| [Trackbar-Steuerelementstile](trackbar-control-styles.md) | Dieser Abschnitt enthält Informationen zu den Stilen, die mit Trackbar-Steuerelementen verwendet werden. <br/> |



 

 

 





