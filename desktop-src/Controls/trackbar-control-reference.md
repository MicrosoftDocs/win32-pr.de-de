---
title: TrackBar
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit TrackBar-Steuerelementen verwendet werden.
ms.assetid: vs|controls|~\controls\trackbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe8e58cd8db9c2811f31cac92ee3d1d31c2c02d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337362"
---
# <a name="trackbar"></a>TrackBar

Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit TrackBar-Steuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                                  | Inhalte                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu TrackBar-Steuerelementen](trackbar-controls.md)       | Eine TrackBar ist ein Fenster, das einen Schieberegler (manchmal als Ziehpunkt bezeichnet) in einem Kanal und optionale Teil Striche enthält. Wenn der Benutzer den Schieberegler mit der Maus oder der Richtungs Taste verschiebt, sendet die TrackBar Benachrichtigungs Meldungen, um die Änderung anzuzeigen.<br/> |
| [Verwenden von TrackBar-Steuerelementen](using-trackbar-controls.md) | Dieser Abschnitt enthält Implementierungsdetails und Beispiele für TrackBar-Steuerelemente.<br/>                                                                                                                                                                               |



 

### <a name="messages"></a>Meldungen



| Thema                                                 | Inhalte                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TBM- \_ ClearSEL**](tbm-clearsel.md)                 | Löscht den aktuellen Auswahlbereich in einer TrackBar. <br/>                                                                                                                                                                                                                                                      |
| [**TBM- \_ ClearTics**](tbm-cleartics.md)               | Entfernt die aktuellen Teil Striche aus einer TrackBar. Diese Meldung entfernt nicht die ersten und letzten Teil Striche, die automatisch von der TrackBar erstellt werden. <br/>                                                                                                                                           |
| [**TBM \_ GetBuddy**](tbm-getbuddy.md)                 | Ruft das Handle für ein Fenster des TrackBar-Steuerelement-Steuer Elements an einem angegebenen Speicherort ab. Der angegebene Speicherort ist relativ zur Ausrichtung des Steuer Elements (horizontal oder vertikal). <br/>                                                                                                                                 |
| [**TBM \_ GetChannelRect**](tbm-getchannelrect.md)     | Ruft die Größe und Position des umgebenden Rechtecks für den Kanal einer TrackBar ab. (Der Kanal ist der Bereich, in dem der Schieberegler verschoben wird. Sie enthält die Hervorhebung, wenn ein Bereich ausgewählt ist.) <br/>                                                                                                         |
| [**TBM \_ getlinesize**](tbm-getlinesize.md)           | Ruft die Anzahl logischer Positionen ab, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben aus den Pfeiltasten (z. b. die-oder-Taste) verschiebt. Bei den logischen Positionen handelt es sich um die ganzzahligen Inkremente in der TrackBar im Bereich der minimalen bis zum maximalen Schieberegler. <br/>                                         |
| [**TBM- \_ getnumtik**](tbm-getnumtics.md)             | Ruft die Anzahl der Teil Striche in einer TrackBar ab. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ getpagesize**](tbm-getpagesize.md)           | Ruft die Anzahl logischer Positionen ab, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben bewegt, z. b. die-Taste oder die-Taste, oder Maus Eingaben, z. b. Klicks im Kanal der Trackleiste. Bei den logischen Positionen handelt es sich um die ganzzahligen Inkremente in der TrackBar im Bereich der minimalen bis zum maximalen Schieberegler. <br/>   |
| [**TBM- \_ GetPos**](tbm-getpos.md)                     | Ruft die aktuelle logische Position des Schiebereglers in einer TrackBar ab. Die logischen Positionen sind die ganzzahligen Werte in der TrackBar-Bereich der minimalen bis maximalen Schieberegler-Positionen. <br/>                                                                                                                       |
| [**TBM- \_ getptics**](tbm-getptics.md)                 | Ruft die Adresse eines Arrays ab, das die Positionen der Teil Striche für eine TrackBar enthält. <br/>                                                                                                                                                                                                        |
| [**TBM- \_ getrangemax**](tbm-getrangemax.md)           | Ruft die maximale Position für den Schieberegler in einer TrackBar ab. <br/>                                                                                                                                                                                                                                           |
| [**TBM- \_ getrangemin**](tbm-getrangemin.md)           | Ruft die minimale Position für den Schieberegler in einer TrackBar ab. <br/>                                                                                                                                                                                                                                           |
| [**TBM- \_ getselend**](tbm-getselend.md)               | Ruft die Endposition des aktuellen Auswahl Bereichs in einer TrackBar ab. <br/>                                                                                                                                                                                                                            |
| [**TBM \_ getselstart**](tbm-getselstart.md)           | Ruft die Anfangsposition des aktuellen Auswahl Bereichs in einer TrackBar ab. <br/>                                                                                                                                                                                                                          |
| [**TBM \_ getthumblength**](tbm-getthumblength.md)     | Ruft die Länge des Schiebereglers in einer TrackBar ab. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ getthumbrect**](tbm-getthumbrect.md)         | Ruft die Größe und Position des umgebenden Rechtecks für den Schieberegler in einer TrackBar ab. <br/>                                                                                                                                                                                                                |
| [**TBM \_ GetTic**](tbm-gettic.md)                     | Ruft die logische Position eines Teil Strichs in einer TrackBar ab. Die logische Position kann ein beliebiger ganzzahliger Wert im Bereich der TrackBar sein, der den minimalen und maximalen Schieberegler-Positionen entspricht. <br/>                                                                                                                     |
| [**TBM- \_ GetTicPos**](tbm-getticpos.md)               | Ruft die aktuelle physische Position eines Teil Strichs in einer TrackBar ab.<br/>                                                                                                                                                                                                                                   |
| [**TBM \_ gettooltips**](tbm-gettooltips.md)           | Ruft das Handle für das QuickInfo-Steuerelement ab, das der TrackBar zugewiesen ist, sofern vorhanden. <br/>                                                                                                                                                                                                                          |
| [**TBM \_ getunicodeformat**](tbm-getunicodeformat.md) | Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab. <br/>                                                                                                                                                                                                                                           |
| [**TBM- \_ SetBuddy**](tbm-setbuddy.md)                 | Weist ein Fenster als Buddy-Fenster für ein TrackBar-Steuerelement zu. TrackBar-Buddy-Fenster werden automatisch an einem Speicherort relativ zur Ausrichtung des Steuer Elements angezeigt (horizontal oder vertikal). <br/>                                                                                                          |
| [**TBM \_ setlinesize**](tbm-setlinesize.md)           | Legt die Anzahl der logischen Positionen fest, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben aus den Pfeiltasten (z. b. die-oder-Taste) verschiebt. Bei den logischen Positionen handelt es sich um die ganzzahligen Inkremente in der TrackBar im Bereich der minimalen bis zum maximalen Schieberegler. <br/>                                              |
| [**TBM \_ setPageSize**](tbm-setpagesize.md)           | Legt die Anzahl der logischen Positionen fest, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben bewegt, wie z. b. die-Taste oder die-Taste oder Maus Eingaben, z. b. Klicks im Kanal der Trackleiste. Bei den logischen Positionen handelt es sich um die ganzzahligen Inkremente in der TrackBar im Bereich der minimalen bis zum maximalen Schieberegler. <br/>        |
| [**TBM- \_ SetPos**](tbm-setpos.md)                     | Legt die aktuelle logische Position des Schiebereglers in einer TrackBar fest. <br/>                                                                                                                                                                                                                                         |
| [**TBM \_ setposnotify**](tbm-setposnotify.md)         | Legt die aktuelle logische Position des Schiebereglers in einer TrackBar fest. <br/>                                                                                                                                                                                                                                         |
| [**TBM-über \_ Tragung**](tbm-setrange.md)                 | Legt den Bereich der minimalen und maximalen logischen Positionen für den Schieberegler in einer TrackBar fest. <br/>                                                                                                                                                                                                                  |
| [**TBM-Objekt- \_ Max**](tbm-setrangemax.md)           | Legt die maximale logische Position für den Schieberegler in einer TrackBar fest. <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ -Anpassung**](tbm-setrangemin.md)           | Legt die minimale logische Position für den Schieberegler in einer TrackBar fest. <br/>                                                                                                                                                                                                                                        |
| [**TBM- \_ Sekunden**](tbm-setsel.md)                     | Legt die Anfangs-und Endpositionen für den verfügbaren Auswahlbereich in einer TrackBar fest. <br/>                                                                                                                                                                                                                |
| [**TBM- \_ setselend**](tbm-setselend.md)               | Legt die logische Endposition des aktuellen Auswahl Bereichs in einer TrackBar fest. Diese Meldung wird ignoriert, wenn die TrackBar nicht über den [**\_ enableselrange**](trackbar-control-styles.md) -Stil von TB verfügt. <br/>                                                                              |
| [**TBM- \_ setselstart**](tbm-setselstart.md)           | Legt die logische Startposition des aktuellen Auswahl Bereichs in einer TrackBar fest. Diese Meldung wird ignoriert, wenn die TrackBar nicht über den [**\_ enableselrange**](trackbar-control-styles.md) -Stil von TB verfügt. <br/>                                                                            |
| [**TBM \_ setthumblength**](tbm-setthumblength.md)     | Legt die Länge des Schiebereglers in einer TrackBar fest. Diese Meldung wird ignoriert, wenn die TrackBar nicht über den [**TSB- \_ FixedLength**](trackbar-control-styles.md) -Stil verfügt. <br/>                                                                                                                      |
| [**TBM- \_ SetTic**](tbm-settic.md)                     | Legt einen Teil Strich in einer TrackBar an der angegebenen logischen Position fest. <br/>                                                                                                                                                                                                                                      |
| [**TBM-Cluster- \_ Freq**](tbm-setticfreq.md)             | Legt die Intervall Häufigkeit für Teil Striche in einer TrackBar fest. Wenn die Häufigkeit z. b. auf zwei festgelegt ist, wird für jedes andere Inkrement im Bereich der TrackBar ein Teil Strich angezeigt. Die Standardeinstellung für die Häufigkeit ist 1. Das heißt, jedes Inkrement im Bereich ist einem Teil Strich zugeordnet. <br/> |
| [**TBM- \_ Seite**](tbm-settipside.md)             | Positioniert ein QuickInfo-Steuerelement von einem TrackBar-Steuerelement. TrackBar-Steuerelemente, die den [**TSB- \_ Tooltips**](trackbar-control-styles.md) -Stil verwenden, zeigen Quick Infos an. <br/>                                                                                                                           |
| [**TBM- \_ SetToolTips**](tbm-settooltips.md)           | Weist einem TrackBar-Steuerelement ein QuickInfo-Steuerelement zu. <br/>                                                                                                                                                                                                                                                       |
| [**TBM- \_ Code Format**](tbm-setunicodeformat.md) | Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest. Mit dieser Meldung können Sie den Zeichensatz ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen. <br/>                                                                                                               |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                              | Inhalte                                                                                                                                                                                      |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ customdraw (TrackBar)](nm-customdraw-trackbar.md)            | Wird von einem TrackBar-Steuerelement gesendet, um die übergeordneten Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>        |
| [NM \_ releasedcapture (TrackBar)](nm-releasedcapture-trackbar-.md) | Benachrichtigt das übergeordnete Fenster eines TrackBar-Steuer Elements, dass das Steuerelement die Maus Aufzeichnung freigibt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/> |
| [trbn- \_ thumbposchanging](trbn-thumbposchanging.md)                | Benachrichtigt, dass sich die Position des Zieh Punkts auf einer TrackBar ändert. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                               |



 

### <a name="constants"></a>Konstanten



| Thema                                                  | Inhalte                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Benutzerdefinierte Zeichnungs Werte](custom-draw-values.md)           | In diesem Abschnitt werden die Werte aufgelistet, die zum Identifizieren der Teile eines TrackBar-Steuer Elements verwendet werden. <br/>      |
| [TrackBar-Steuerelement Stile](trackbar-control-styles.md) | Dieser Abschnitt enthält Informationen zu den Stilen, die mit TrackBar-Steuerelementen verwendet werden. <br/> |



 

 

 





