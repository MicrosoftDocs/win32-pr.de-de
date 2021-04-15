---
title: Symbolleisten
description: Symbolleisten sind eine Möglichkeit zum Gruppieren von Befehlen, um einen effizienten Zugriff zu erhalten.
ms.assetid: 8f36307c-54fc-493d-a2ff-57db29e3508d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: bb32c84f6090bc25b985b8445fb351a478c24c2b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104554418"
---
# <a name="toolbars"></a>Symbolleisten

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Symbolleisten sind eine Möglichkeit zum Gruppieren von Befehlen, um einen effizienten Zugriff zu erhalten.

![Screenshot von zwei Symbolleisten mit Elementen mit der Bezeichnung ](images/cmd-toolbars-image1.png)

Einige typische Symbolleisten.

**Verwenden Sie Symbolleisten zusätzlich zu oder anstelle von Menüleisten.** Symbolleisten können effizienter als Menüleisten sein, da Sie direkt angezeigt werden (statt bei einem Mausklick angezeigt), direkt (anstelle zusätzlicher Eingaben) und die am häufigsten verwendeten Befehle (anstelle einer umfassenden Liste) enthalten. Im Gegensatz zu Menüleisten müssen Symbolleisten nicht vollständig oder selbsterklärend sein, sondern nur schnell, komfortabel und effizient.

Einige Symbolleisten können angepasst werden, sodass Benutzer Symbolleisten hinzufügen oder entfernen, ihre Größe und Position ändern und sogar ihren Inhalt ändern können. Einige Typen von Symbolleisten können nicht angedockt werden, was zu einem Palettenfenster führt. Weitere Informationen zu Symbolleisten-Variationen finden Sie unter [Verwendungs Muster](#usage-patterns) in diesem Artikel.

> [!Note]  
> Richtlinien, die sich auf [Menüs](cmd-menus.md), [Befehls](ctrl-command-buttons.md)Schaltflächen und [Symbole](vis-icons.md) beziehen, werden in separaten Artikeln dargestellt.

 

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Ist das Fenster ein primäres Fenster?** Symbolleisten funktionieren gut für primäre Fenster, sind aber in der Regel für sekundäre Fenster überwältigend. Verwenden Sie für sekundäre Fenster stattdessen [Befehls](ctrl-command-buttons.md)Schaltflächen, [Menü](ctrl-command-buttons.md)Schaltflächen und [Links](ctrl-command-links.md) .
-   **Gibt es eine kleine Anzahl von häufig verwendeten Befehlen?** Symbolleisten können nicht so viele Befehle wie Menüleisten verarbeiten, sodass Sie am besten als eine Möglichkeit zum effizienten Zugriff auf eine kleine Anzahl häufig verwendeter Befehle funktionieren.
-   **Sind die meisten Befehle sofort?** Das heißt, sind Sie meistens Befehle, für die keine zusätzliche Eingabe erforderlich ist? Um effizient zu sein, benötigen Symbolleisten ein direktes und unmittelbares Gefühl. Wenn dies nicht der Wert ist, eignen sich die Menüleisten besser für Befehle, die zusätzliche Eingaben erfordern.
-   **Können die meisten Befehle direkt angezeigt werden?** Das heißt, Benutzer interagieren mit Ihnen mit einem einzigen Mausklick? Obwohl einige Befehle mithilfe von Menü Schaltflächen angezeigt werden können, wird durch die Darstellung der meisten Befehle auf diese Weise die Effizienz der Symbolleiste unterdrückt, sodass eine Menüleiste besser geeignet ist.
-   **Werden die Befehle gut durch Symbole dargestellt?** Symbolleisten Schaltflächen werden in der Regel durch Symbole anstelle von Text Bezeichnungen dargestellt (obwohl einige Symbolleisten Schaltflächen beide verwenden), während Menübefehle durch Ihren Text dargestellt werden. Wenn die Befehls Symbole nicht hochwertig sind und nicht selbsterklärend sind, ist eine Menüleiste möglicherweise eine bessere Wahl.

Wenn das Programm über eine Symbolleiste ohne Menüleiste verfügt und die meisten Befehle indirekt über Menü Schaltflächen und [Trenn](ctrl-command-buttons.md)Schaltflächen zugänglich sind, handelt es sich bei dieser Symbolleiste im Grunde um eine Menüleiste. Wenden Sie stattdessen das Muster für [Symbolleisten Menüs](cmd-menus.md) in den Menüs-Richtlinien an

## <a name="design-concepts"></a>Entwurfskonzepte

Eine gute Menüleiste ist ein umfassender Katalog aller verfügbaren Befehle auf oberster Ebene, während eine gute Symbolleiste schnellen und bequemen Zugriff auf häufig verwendete Befehle ermöglicht. Eine Symbolleiste versucht nicht, Benutzer zu trainieren, sondern macht Sie einfach produktiv. Wenn Benutzer erfahren, wie Sie auf einen Befehl auf einer Symbolleiste zugreifen, greifen Sie in der Menüleiste selten auf den Befehl zu. Aus diesen Gründen müssen die Menüleiste eines Programms und seine Symbolleiste nicht direkt übereinstimmen.

### <a name="toolbars-vs-menu-bars"></a>Symbolleisten im Vergleich zu Menüleisten

In der Regel unterscheiden sich Symbolleisten von Menüleisten wie folgt:

-   **Häufig.** Symbolleisten zeigen nur die am häufigsten verwendeten Befehle an, während Menüleisten alle verfügbaren Befehle auf oberster Ebene in einem Programm katalogisieren.
-   **Unmittelbarkeit.** Das Klicken auf einen Symbolleisten Befehl wird sofort wirksam, während ein Menübefehl möglicherweise zusätzliche Eingaben erfordert. Beispielsweise zeigt ein Druckbefehl in einer Menüleiste zuerst das Dialogfeld Drucken an, während eine Schaltfläche Druck Symbolleiste sofort eine einzelne Kopie eines Dokuments auf dem Standarddrucker ausgibt.

    ![Screenshot der ausgewählten Drucker Schaltfläche der Symbolleiste ](images/cmd-toolbars-image2.png)

    Wenn Sie in diesem Beispiel auf die Schaltfläche "Drucken" klicken, wird sofort eine einzelne Kopie eines Dokuments auf dem Standarddrucker gedruckt.

-   **Die Direktheit.** Symbolleisten Befehle werden mit einem einzigen Mausklick aufgerufen, während Menüleisten Befehle im Menü navigieren müssen.
-   **Anzahl und Dichte.** Der von einer Symbolleiste benötigte Bildschirmbereich ist proportional zur Anzahl der zugehörigen Befehle, und der Speicherplatz wird immer verwendet, auch wenn es sich nicht um Befehle handelt. Folglich müssen die Symbolleisten ihren Platz auf effiziente Weise verwenden. Im Gegensatz dazu werden Menüleisten Befehle in der Ansicht normalerweise ausgeblendet, und ihre hierarchische Struktur ermöglicht eine beliebige Anzahl von Befehlen.
-   **Größe und Darstellung.** Um viele Befehle in einem kleinen Bereich zu packen, verwenden Symbolleisten normalerweise Symbol basierte Befehle (mit QuickInfo-basierten Bezeichnungen), wohingegen Menüleisten textbasierte Befehle (mit optionalen Symbolen) verwenden. Obwohl Symbolleisten Schaltflächen über Standardtext Bezeichnungen verfügen können, verwenden Sie erheblich mehr Platz.

    ![Screenshot der Symbolleiste mit der Bezeichnung "senden/empfangen" ](images/cmd-toolbars-image3.png)

    Beschriftete Symbolleisten Schaltflächen benötigen mindestens dreimal so viel Platz wie die nicht beschrifteten.

-   **Selbsterklärend** Gut gestaltete Symbolleisten benötigen Symbole, die größtenteils selbsterklärend sind, da Benutzer Befehle nicht effizient mithilfe von Quick Infos finden können. Symbolleisten funktionieren jedoch immer noch gut, wenn einige weniger häufig verwendete Befehle nicht selbsterklärend sind.

    ![Screenshot der Symbolleiste mit vertrauten Symbolen ](images/cmd-toolbars-image4.png)

    In diesem Beispiel sind die am häufigsten verwendeten Symbole selbsterklärend.

-   **Erkennbar und unterschieden.** Für häufig verwendete Befehle können sich Benutzer von Symbolleisten-Schaltflächen Attributen wie Speicherort, Form und Farbe merken. Mit gut entworfenen Symbolleisten können Benutzer die Befehle schnell finden, auch wenn Sie sich nicht das exakte symbolsymbol merken. Im Gegensatz dazu merken sich die Benutzer häufig verwendete Menüleisten-Befehls Speicherorte, verwenden jedoch die Befehls Bezeichnungen, um die Auswahl zu treffen.

    ![Screenshot des Dialog Felds "Optionen für das Ausschneiden von Tools" ](images/cmd-toolbars-image5.png)

    Bei Symbolleisten Befehlen helfen die unterschiedliche Position, Form und Farbe, Symbole zu erkennen und zu unterscheiden.

    ![Screenshot der Menüleiste mit ausgewähltem Datei Befehl ](images/cmd-toolbars-image6.png)

    Bei Menüleisten Befehlen hängen die Benutzer letztendlich von ihren Bezeichnungen ab.

### <a name="efficiency"></a>Effizienz

In Anbetracht ihrer Merkmale müssen Symbolleisten hauptsächlich für Effizienz entworfen werden. Eine ineffiziente Symbolleiste ist nicht sinnvoll.

**Wenn Sie nur eine Aktion ausführen...**

Stellen Sie sicher, dass Ihre Symbolleisten hauptsächlich auf Effizienz ausgelegt sind. Fokus Symbolleisten auf Befehle, die häufig verwendet, unmittelbar, direkt und schnell erkennbar sind.

### <a name="hiding-menu-bars"></a>Ausblenden von Menüleisten

Im Allgemeinen funktionieren Symbolleisten hervorragend zusammen mit Menüleisten: gute Symbolleisten bieten Effizienz und gute Menüleisten bieten umfassende Vorteile. **Wenn sowohl Menüleisten als auch Symbolleisten vorhanden sind, können sich alle auf die Stärken konzentrieren.**

Dieses Modell wird überraschend mit einfachen Programmen unterteilt. Für Programme mit nur wenigen Befehlen ist es nicht sinnvoll, eine Menüleiste und eine Symbolleiste zu verwenden, da die Menüleiste am Ende eine redundante, ineffiziente Version der Symbolleiste ist.

Um diese Redundanz auszuschließen, konzentrieren sich viele einfache Programme in Windows Vista darauf, Befehle ausschließlich über die Symbolleiste bereitzustellen und die Menüleiste standardmäßig zu verbergen. Zu diesen Programmen gehören Windows-Explorer, Windows Internet Explorer, Windows Media Player und Windows Photo Gallery.

Dies ist keine kleine Änderung. Wenn Sie die Menüleiste entfernen, wird die Art der Symbolleisten grundlegend geändert, da diese Symbolleisten umfassend sein müssen und sich wie folgt ändern:

-   **Häufig.** Wenn Sie die Menüleiste entfernen, bedeutet dies, dass alle Befehle, die nicht direkt aus einem Fenster oder den zugehörigen Kontextmenüs verfügbar sind, über die Symbolleiste zugänglich sein müssen, unabhängig von ihrer Verwendungs Häufigkeit.
-   **Unmittelbarkeit.** Wenn Sie die Menüleiste entfernen, ist die Symbolleiste der einzige sichtbare Zugriffspunkt für Befehle. Dies erfordert, dass die Symbolleiste über voll funktionsfähige Versionen verfügt. Wenn z. b. keine Menüleiste vorhanden ist, muss ein Druckbefehl auf einer Symbolleiste das Dialogfeld Drucken anzeigen, anstatt sofort zu drucken. (Obwohl die Verwendung einer unterteilten Schaltfläche in diesem Fall eine ausgezeichnete Gefährdung darstellt. Weitere Informationen finden Sie unter [Standardmenü und unterteilte](#standard-menu-and-split-buttons) Schaltflächen für die Standarddruck unterteilte Schaltfläche

    ![Screenshot der Optionen für die Symbolleiste und den Druckbefehl ](images/cmd-toolbars-image7.png)

    In diesem Beispiel enthält die Symbolleisten Schaltfläche Drucken in der Windows-Fotogalerie einen Befehl Drucken, der das Dialogfeld Drucken anzeigt.

-   **Die Direktheit.** Um Speicherplatz zu sparen und die Übersichtlichkeit zu verhindern, können weniger häufig verwendete Befehle in Menü Schaltflächen verschoben werden, sodass Sie weniger direkt verwendet werden.

Symbolleisten zum ergänzen einer Menüleiste sind anders konzipiert als Symbolleisten, die für die Verwendung mit einer entfernten oder ausgeblendeten Menüleiste entworfen wurden. Und da Sie nicht davon ausgehen können, dass Benutzer eine ausgeblendete Menüleiste anzeigen, um einen einzelnen Befehl auszuführen, sollte das Ausblenden einer Menüleiste genauso behandelt werden wie das vollständige entfernen, wenn Entwurfsentscheidungen getroffen werden. (Wenn Sie die Menüleiste standardmäßig ausblenden, gehen Sie nicht davon aus, dass die Benutzer die Menüleiste anzeigen, um einen Befehl zu finden, oder sogar herauszufinden, wie Sie angezeigt werden soll.)

Das Entwerfen einer Symbolleiste, die ohne Menüleiste funktioniert, umfasst häufig einige Kompromisse. Aber aus Effizienzgründen sollten Sie nicht zu viel kompromittieren. Wenn das Ausblenden der Menüleiste zu einer ineffizienten Symbolleiste führt, blenden Sie die Menüleiste nicht aus.

### <a name="keyboard-accessibility"></a>Barrierefreiheit der Tastaturnavigation

Auf der Tastatur unterscheidet sich der Zugriff auf Symbolleisten erheblich von dem Zugriff auf Menüleisten. Menüleisten erhalten den Eingabefokus, wenn Benutzer die Alt-Taste drücken und der Eingabefokus mit der ESC-Taste verloren geht. Wenn eine Menüleiste den Eingabefokus besitzt, wird Sie unabhängig vom Rest des Fensters navigiert und verarbeitet alle Pfeiltasten, Start-, End-und Tab-Taste. Im Gegensatz dazu erhalten Symbolleisten den Eingabefokus, wenn Benutzer die Tab-Taste durch den gesamten Inhalt des Fensters drücken. Da Symbolleisten zuletzt in der Aktivier Reihenfolge angezeigt werden, können Sie auf einer ausgelasteten Seite erhebliche Anstrengungen ausführen (es sei denn, Benutzer wissen, dass UMSCHALT + TAB verwendet wird, um rückwärts zu wechseln).

Barrierefreiheit stellt hier ein Problem dar: während die Symbolleisten einfacher für Maus Benutzer sind, sind Sie für Tastatur Benutzer weniger zugänglich. Dies ist kein Problem, wenn eine Menüleiste und eine Symbolleiste vorhanden sind, aber wenn die Menüleiste entfernt oder ausgeblendet wird.

Aus Gründen der Barrierefreiheit empfiehlt es sich, die Menüleiste beizubehalten, anstatt sie vollständig zugunsten einer Symbolleiste zu entfernen. Wenn Sie die Menüleiste entfernen und einfach ausblenden müssen, bevorzugen Sie Sie.

## <a name="usage-patterns"></a>Verwendungsmuster

Symbolleisten verfügen über mehrere Verwendungs Muster:



|                                                                                                                      |                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Primäre Symbolleisten**<br/> eine Symbolleiste, die ohne eine Menüleiste, die ausgeblendet oder entfernt wurde, funktioniert. <br/> | primäre Symbolleisten müssen den Bedarf an Effizienz hinsichtlich der Effizienz ausgleichen, sodass Sie für einfache Programme am besten geeignet sind. <br/> ![Screenshot der Windows-Explorer-Symbolleiste ](images/cmd-toolbars-image8.png)<br/> Eine primäre Symbolleiste aus Windows-Explorer.<br/>                                                                        |
| **Ergänzende Symbolleisten**<br/> eine Symbolleiste, die für die Arbeit mit einer Menüleiste konzipiert ist. <br/>                         | ergänzende Symbolleisten können sich ohne Kompromisse auf Effizienz konzentrieren. <br/> ![Screenshot einer Menüleiste über eine Symbolleiste ](images/cmd-toolbars-image9.png)<br/> Eine ergänzende Symbolleiste von Windows Movie Maker.<br/>                                                                                                                  |
| **Symbolleisten Menüs**<br/> eine Menüleiste, die als Symbolleiste implementiert ist. <br/>                                        | Symbolleisten Menüs sind Symbolleisten, die hauptsächlich aus Befehlen in [Menü](ctrl-command-buttons.md) Schaltflächen und Trenn Schaltflächen bestehen, bei denen es sich nur um einige direkte Befehle handelt. <br/> ![Screenshot der Menüleiste mit Symbolen und Befehlen ](images/cmd-toolbars-image10.png)<br/> Ein Symbolleisten Menü in der Windows-Fotogalerie.<br/> |
| **Anpassbare Symbolleisten**<br/> eine Symbolleiste, die von Benutzern angepasst werden kann. <br/>                          | durch anpassbare Symbolleisten können Benutzer Symbolleisten hinzufügen oder entfernen, ihre Größe und Position ändern und sogar ihren Inhalt ändern. <br/> ![Screenshot einer Symbolleiste mit Dutzenden von Symbolen ](images/cmd-toolbars-image11.png)<br/> Eine anpassbare Symbolleiste aus Microsoft Visual Studio.<br/>                                             |
| **Palettenfenster**<br/> ein nicht modalem Dialogfeld, das ein Array von Befehlen darstellt. <br/>                 | Palettenfenster sind nicht angedockte Symbolleisten. <br/> ![Screenshot eines Farben Dialogfelds ](images/cmd-toolbars-image12.png)<br/> ![Screenshot eines Schriftarten Dialogfelds ](images/cmd-toolbars-image13.png)<br/> Palette Fenster von Windows Paint.<br/>                                                                             |



 

Symbolleisten haben folgende Stile:



|                                                                                                                                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nicht gekennzeichnete Symbole**<br/> eine oder mehrere Zeilen mit kleinen Symbol Schaltflächen ohne Bezeichnung. <br/>                                           | Verwenden Sie diesen Stil, wenn zu viele Schaltflächen für die Bezeichnung vorhanden sind oder das Programm häufig verwendet wird. bei diesem Stil können Programme mit komplexer Funktionalität mehrere Zeilen enthalten. Daher ist dies der einzige Stil, der anpassbar sein muss. bei diesem Stil können einige Befehls Schaltflächen bezeichnet werden, wenn Sie häufig verwendet werden. <br/> ![Screenshot der Symbolleiste mit kleinen, nicht beschrifteten Symbolen ](images/cmd-toolbars-image14.png)<br/> Eine Symbolleiste ohne Bezeichnung von WordPad.<br/> |
| **Große nicht gekennzeichnete Symbole**<br/> eine einzelne Zeile mit großen Symbol Schaltflächen ohne Bezeichnung. <br/>                                         | Verwenden Sie dieses Format für einfache Hilfsprogramme, die leicht erkennbare Symbole aufweisen und in der Regel in kleinen Fenstern ausgeführt werden. <br/> ![Screenshot der Symbolleiste mit großen, nicht beschrifteten Symbolen ](images/cmd-toolbars-image15.png)<br/> ![Screenshot der Symbolleiste mit großen Symbolen ](images/cmd-toolbars-image16.png)<br/> Große Symbolleisten Symbolleisten von Windows Live Messenger und das Windows-Tool zum Ausschneiden von Symbolen.<br/>                                                                       |
| **Gekennzeichnete Symbole**<br/> eine einzelne Zeile mit kleinen markierten Symbolen. <br/>                                                          | Verwenden Sie diesen Stil, wenn einige Befehle vorhanden sind oder das Programm nicht häufig verwendet wird. Dieser Stil hat immer eine einzelne Zeile. <br/> ![Screenshot der Symbolleiste mit gekennzeichneten Symbolen ](images/cmd-toolbars-image8.png)<br/> Eine Symbolleiste mit beschrifteten Symbolen aus Windows-Explorer.<br/>                                                                                                                                                                                                               |
| **Partielle Symbolleisten**<br/> eine partielle Zeile kleiner Symbole, mit der Platz gespart wird, wenn keine vollständige Symbolleiste erforderlich ist. <br/>       | Verwenden Sie dieses Format für Fenster mit Navigations Schaltflächen, einem Suchfeld oder Registerkarten, um unnötige Gewichtung am oberen Rand des Fensters zu vermeiden. <br/> ![Screenshot der Menüleiste, Symbolleiste und Favoritenleiste ](images/cmd-toolbars-image17.png)<br/> Partielle Symbolleisten können mit Navigations Schaltflächen, einem Suchfeld oder Registerkarten kombiniert werden.<br/>                                                                                                                                                  |
| **Große partielle Symbolleisten**<br/> eine partielle Zeile von großen Symbolen, die verwendet wird, um Platz zu sparen, wenn keine vollständige Symbolleiste erforderlich <br/> | Verwenden Sie dieses Format für einfache Hilfsprogramme, die über Navigations Schaltflächen oder ein Suchfeld verfügen, um unnötige Gewichtung am oberen Rand des Fensters zu vermeiden. <br/> ![Screenshot einer großen partiellen Symbolleiste ](images/cmd-toolbars-image18.png)<br/> Eine große partielle Symbolleiste von Windows Defender.<br/>                                                                                                                                                                                         |



 

Zum Schluss haben Symbolleisten-Steuerelemente mehrere Verwendungs Muster:



|                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Schaltflächen für Befehls Symbol**<br/> durch Klicken auf eine Befehls Schaltfläche wird eine sofortige Aktion initiiert. <br/>                                                                                                 | ![Screenshot einer Symbolleiste mit beschrifteten Symbolen ](images/cmd-toolbars-image19.png)<br/> Beispiele für Symbol Befehls Schaltflächen aus Windows-Fax und-Scan.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Schaltflächen für Modus**<br/> das Klicken auf die Schaltfläche Modus wechselt in den ausgewählten Modus. <br/>                                                                                                            | ![Screenshot einer vertikalen Symbolleiste ](images/cmd-toolbars-image20.png)<br/> Beispiele für Modus-Schaltflächen aus Windows Paint.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Eigenschaften Symbol Schaltflächen**<br/> der Zustand einer Eigenschaften Schaltfläche gibt den Zustand der aktuell ausgewählten Objekte an (sofern vorhanden). durch Klicken auf die Schaltfläche wird die Änderung auf die ausgewählten Objekte angewendet. <br/> | ![Screenshot der Formatierung von Symbolen und ausgewähltem Text ](images/cmd-toolbars-image21.png)<br/> Beispiele für Eigenschafts Schaltflächen von Microsoft Word.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Beschriftete Symbolschaltflächen**<br/> eine Befehls Schaltfläche oder eine Eigenschaften Schaltfläche mit einem Symbol und einer Text Bezeichnung. <br/>                                                                               | Diese Schaltflächen werden für häufig verwendete Symbolleisten Schaltflächen verwendet, deren Symbol nicht selbsterklärend ist. Sie werden auch in Symbolleisten mit so wenigen Schaltflächen verwendet, dass jede Schaltfläche eine Text Bezeichnung aufweisen kann. <br/> ![Screenshot, der die Symbolleiste mit Symbolen anzeigt, die für die am häufigsten verwendeten Schaltflächen bezeichnet werden. ](images/cmd-toolbars-image22.png)<br/> Eine Symbolleiste mit den am häufigsten verwendeten Schaltflächen mit der Bezeichnung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Menü Schaltflächen**<br/> eine Befehls Schaltfläche, die verwendet wird, um einen kleinen Satz verwandter Befehle anzuzeigen. <br/>                                                                                                | ein einzelnes nach unten zeigendes Dreieck gibt an, dass durch Klicken auf die Schaltfläche ein Menü angezeigt wird. <br/> ![Screenshot der Symbolleiste und Dropdown-Befehlsliste ](images/cmd-toolbars-image23.png)<br/> Eine Menü Schaltfläche mit einem kleinen Satz verwandter Befehle.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Trenn Schaltflächen**<br/> eine Befehls Schaltfläche, die zum Konsolidieren von Variationen eines Befehls verwendet wird, vor allem, wenn einer der Befehle in der meiste Zeit verwendet wird. <br/>                                     | ![Screenshot der Schaltfläche "Split Print" ](images/cmd-toolbars-image24.png)<br/> eine Trenn Schaltfläche im normalen Zustand.<br/> wie eine Menü Schaltfläche zeigt ein einzelnes nach unten zeigendes Dreieck an, dass durch Klicken auf den rechten Teil der Schaltfläche ein Menü angezeigt wird. <br/> ![Screenshot der Schaltflächen Befehle "Split Print" ](images/cmd-toolbars-image25.png)<br/> eine aufgeteilte Trenn Schaltfläche.<br/> in diesem Beispiel wird eine unterteilte Schaltfläche verwendet, um alle druckbezogenen Befehle zu konsolidieren. in den meisten Fällen wird der Befehl für den sofortigen Druck verwendet, sodass Benutzer normalerweise nicht die anderen Befehle sehen müssen. <br/> anders als bei einer Menü Schaltfläche wird durch Klicken auf den linken Teil der Schaltfläche die Aktion direkt für die Bezeichnung ausgeführt. unterteilte Schaltflächen sind in Situationen wirksam, in denen der nächste Befehl wahrscheinlich mit dem letzten Befehl identisch ist. in diesem Fall wird die Bezeichnung wie bei einer Farbauswahl in den letzten Befehl geändert:<br/> ![Screenshot des Bucket-Symbols zum Zeichnen von Paint ](images/cmd-toolbars-image26.png)<br/> In diesem Beispiel wird die Bezeichnung in den letzten Befehl geändert.<br/> |
| **Dropdownlisten**<br/> eine Dropdown Liste (bearbeitbar oder schreibgeschützt), die verwendet wird, um eine Eigenschaft anzuzeigen oder zu ändern. <br/>                                                                                   | ![Screenshot der Dropdown Liste mit Schriftarten ](images/cmd-toolbars-image27.png)<br/> In diesem Beispiel werden die Dropdown Listen verwendet, um Schriftart Attribute anzuzeigen und festzulegen.<br/> Eine Dropdown Liste in einer Symbolleiste gibt ggf. den Zustand des aktuell ausgewählten Objekts an. Durch Ändern der Liste wird der Zustand des ausgewählten Objekts geändert. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="guidelines"></a>Richtlinien

### <a name="presentation"></a>Präsentation

-   **Wählen Sie einen geeigneten Symbolleisten Stil basierend auf der Anzahl der Befehle und deren Verwendung aus.** Eine Anleitung zum Auswählen von finden Sie in der vorherigen Symbolleiste in der Symbolleiste. Vermeiden Sie die Verwendung einer Symbolleisten Konfiguration, die zu viel Speicherplatz aus dem Programm Arbeitsbereich benötigt.
-   **Platzieren Sie Symbolleisten direkt oberhalb des Inhalts Bereichs,** und zwar unterhalb der Menüleiste und Adressleiste, falls vorhanden.
-   **Wenn der Speicherplatz auf dem Premium-Speicherplatz ist, sparen Sie Speicherplatz**

    -   Die Bezeichnungen bekannter Symbole und weniger häufig verwendete Befehle werden weggelassen.
    -   Es wird nur eine partielle Symbolleiste anstelle der gesamten Fensterbreite verwendet.
    -   Konsolidieren verwandter Befehle mit einer Menü Schaltfläche oder einer unterteilten Schaltfläche.
    -   Verwenden eines [Überlauf-Chevron](glossary.md) , um weniger häufig verwendete Befehle anzuzeigen.
    -   Anzeigen von Befehlen nur, wenn Sie auf den aktuellen Kontext angewendet werden.

    ![Screenshot der allgemeinen Symbolleisten Symbole nicht beschriftet ](images/cmd-toolbars-image28.png)

    Die Windows Internet Explorer-Symbolleiste spart Speicherplatz, indem Bezeichnungen bekannter Symbole, die Verwendung einer partiellen Symbolleiste und die Verwendung eines Überlauf-Chevron für seltener verwendete Befehle weggelassen werden.

-   **Verwenden Sie für das Symbol Toolbar-Muster ohne Bezeichnung eine Standardkonfiguration, die nicht mehr als zwei Zeilen von Symbolleisten darstellt.** Wenn mehr als zwei Zeilen nützlich sein können, können Sie die Symbolleisten anpassbar machen. Beginnend mit mehr als zwei Zeilen kann die Benutzer überfordern und zu viel Speicherplatz aus dem Programm Arbeitsbereich beanspruchen.

    **Falsch:**

    ![Screenshot der Menüleiste und drei Zeilen von Symbolleisten ](images/cmd-toolbars-image29.png)

    Eine Standardkonfiguration mit mehr als zwei Zeilen von Symbolleisten führt zu einer zu großen visuellen Übersichtlichkeit.

-   Deaktivieren Sie einzelne Symbolleisten Schaltflächen, **die nicht auf den aktuellen Kontext angewendet werden,** anstatt Sie zu entfernen. Dadurch wird die Symbolleisten Inhalte stabil und leichter zu finden.
-   **Deaktivieren Sie einzelne Symbolleisten Schaltflächen, wenn Sie auf diese Schaltflächen direkt zu einem Fehler führen.** Dies ist erforderlich, um ein direktes Verhalten zu gewährleisten.
-   **Entfernen Sie für das Symbolleisten Muster ohne Bezeichnung Symbole die gesamten Symbolleisten, wenn Sie nicht auf den aktuellen Kontext angewendet werden.** Zeigen Sie Sie nur in den entsprechenden Modi an.

    ![Screenshot der Symbolleiste "Debuggen" ](images/cmd-toolbars-image30.png)

    In diesem Beispiel wird die debugsymbolleiste nur angezeigt, wenn das Programm ausgeführt wird.

-   **Symbolleisten-Schaltflächen linksbündig ausgerichtet.** Das Hilfe Symbol (falls vorhanden) ist rechtsbündig ausgerichtet.

    ![Screenshot der Symbolleiste, Hilfe Symbol Rechtsbündig ](images/cmd-toolbars-image31.png)

    Alle Symbolleisten Schaltflächen sind linksbündig ausgerichtet, ausgenommen Hilfe.

    **Ausnahme:** Symbolleisten im Windows 7-Stil richten Links Programm spezifische Befehle aus, korrigieren jedoch standardmäßig bekannte Befehle wie Optionen, Ansicht und Hilfe.

-   **Ändern Sie die Symbolleisten-Schaltflächen Bezeichnungen nicht dynamisch.** Dies ist verwirrend und unerwartet. Allerdings können Sie das Symbol ändern, um den aktuellen Zustand widerzuspiegeln.

    ![Screenshot des Bucket-Symbols zum Zeichnen von Paint ](images/cmd-toolbars-image26.png)

    In diesem Beispiel wird das Symbol so geändert, dass es den Standardbefehl angibt.

### <a name="controls-and-commands"></a>Steuerelemente und Befehle

-   **Bevorzugen Sie die am häufigsten verwendeten Befehle.**
    -   **Stellen Sie für primäre Symbolleisten umfassende Befehle bereit.** Primäre Symbolleisten müssen nicht so umfassend wie Menüleisten sein, aber Sie müssen alle Befehle bereitstellen, die an anderer Stelle nicht auffähierbar sind. Primäre Symbolleisten benötigen keine Befehle für Folgendes:
        -   Befehle, die sich direkt auf der Benutzeroberfläche selbst befinden.
        -   Befehle, die in der Regel über Kontextmenüs aufgerufen werden.
        -   Standard mäßige, bekannte Befehle wie Ausschneiden, kopieren und einfügen.
    -   **Geben Sie für ergänzende Symbolleisten Befehle an, die am häufigsten verwendet werden.** Menüleisten Befehle sind eine supermenge der Symbolleisten Befehle, sodass Sie nicht alles angeben müssen. Konzentrieren Sie sich auf den schnellen, praktischen Befehls Zugriff, und überspringen Sie den Rest.
-   **Direkte Steuerelemente bevorzugen.** Verwenden Sie die Schaltflächen der Symbolleiste in der folgenden Reihenfolge:
    -   **Symbol Schaltfläche.** Direkt und benötigt nur wenig Speicherplatz.
    -   **Beschriftete Symbol Schaltfläche.** Direkt, benötigt jedoch mehr Platz.
    -   **Trenn Schaltfläche.** Leiten Sie den häufigsten Befehl ein, aber behandelt Befehls Variationen.
    -   **Menü Schaltfläche.** Indirekt, stellt jedoch viele Befehle dar.
-   **Sofortige Befehle bevorzugen.** Für Befehle, die entweder unmittelbar sein können oder zusätzliche Eingaben für die Flexibilität aufweisen:
    -   Verwenden Sie für primäre Symbolleisten die flexiblen Versionen von Befehlen (z. b. Drucken...).
    -   Verwenden Sie für ergänzende Symbolleisten die unmittelbaren Versionen in der Symbolleiste (z. b. Drucken), und verwenden Sie flexible Versionen in der Menüleiste (z. b. Drucken...).
-   **Stellen Sie Bezeichnungen für häufig verwendete Befehle bereit,** insbesondere dann, wenn Ihre Symbole keine bekannten Symbole sind.

    **Annehmbar:**

    ![Screenshot der Symbolleiste ohne die Bezeichnung "Symbole" ](images/cmd-toolbars-image32.png)

    **Besserer**

    ![Screenshot der Symbolleiste mit einigen Symbolen ](images/cmd-toolbars-image33.png)

    Die Symbolleiste für Windows-Fax und-Scan verfügt über einige Befehle, sodass die bessere Version die wichtigsten Bezeichnungen bezeichnet.

-   Fügen Sie Befehle nicht in Symbolleisten Menüs ein, die sich auch direkt auf der Symbolleiste befinden.

    **Falsch:**

    ![Screenshot des Befehls "Drucken" auf der Symbolleiste und im Menü ](images/cmd-toolbars-image34.png)

    In diesem Beispiel befindet sich Print direkt auf der Symbolleiste, sodass es nicht im Menü angezeigt werden muss.

### <a name="organization-and-order"></a>Organisation und Bestellung

-   **Ordnen Sie die Befehle in einer Symbolleiste in Verwandte Gruppen auf.**
-   **Platzieren Sie die am häufigsten verwendeten Gruppen zuerst. Fügen Sie die Befehle innerhalb einer Gruppe in ihre logische Reihenfolge ein.** Insgesamt sollten die Befehle einen logischen Flow aufweisen, damit Sie problemlos gefunden werden können, während die am häufigsten verwendeten Befehle zuerst angezeigt werden. Dies ist besonders effizient, insbesondere bei einem Überlauf.
-   **Verwenden Sie Gruppen Teiler nur dann, wenn die gruppenübergreifende Befehle schwach gekoppelt sind.** Dadurch sind die Gruppierungen offensichtlich, und die Befehle sind leichter zu finden.

    ![Screenshot, der eine Symbolleiste mit gut organisierten Symbolen mithilfe von Gruppen Teilern anzeigt.](images/cmd-toolbars-image35.png)

    ![Screenshot der Symbolleiste mit gut organisierten Symbolen ](images/cmd-toolbars-image36.png)

    Beispiele für gruppierte Symbolleisten aus Windows Mail.

-   **Vermeiden Sie das Platzieren von destruktiven Befehlen neben häufig verwendeten Befehlen.** Verwenden Sie entweder Order oder Gruppierung, um die Trennung zu erhalten. Erwägen Sie auch, keine destruktiven Befehle auf der Symbolleiste zu platzieren, sondern nur in der Menüleiste oder in den Kontextmenüs.

    **Annehmbar:**

    ![Screenshot der angrenzenden Schaltflächen "Drucken" und "Löschen" ](images/cmd-toolbars-image37.png)

    **Besserer**

    ![Screenshot der getrennten Schaltflächen "Drucken" und "Löschen" ](images/cmd-toolbars-image38.png)

    Im besseren Beispiel ist der Befehl Delete physisch vom Print getrennt.

-   **Verwenden Sie das Überlauf-Chevron, um anzugeben, dass nicht alle Befehle angezeigt werden können.** Verwenden Sie den Überlauf jedoch nur dann, wenn nicht genügend Platz zum Anzeigen aller Befehle vorhanden ist.

    **Falsch:**

    ![Screenshot der Favoritenleiste und der ausgeblendeten Befehle ](images/cmd-toolbars-image39.png)

    Der Überlauf-Chevron gibt an, dass nicht alle Befehle angezeigt werden, aber viele von Ihnen können ein besseres Layout aufweisen.

-   **Stellen Sie sicher, dass die am häufigsten verwendeten Befehle direkt über die Symbolleiste (d. h. nicht über einen Überlauf) in kleinen Fenstergrößen zugänglich sind.** Ordnen Sie die Befehle bei Bedarf neu an, verschieben Sie weniger häufig verwendete Befehle in Menü Schaltflächen oder unterteilte Schaltflächen, oder entfernen Sie sie vollständig aus der Symbolleiste. Wenn dies ein Problem ist, überdenken Sie die Auswahl des Toolbar-Stils.

### <a name="hiding-menu-bars"></a>Ausblenden von Menüleisten

Im Allgemeinen funktionieren Symbolleisten hervorragend zusammen mit Menüleisten, da beide die Möglichkeit haben, sich ohne Kompromisse auf ihre Stärken zu konzentrieren.

-   Blendet die Menüleiste standardmäßig aus, wenn der Symbolleisten Entwurf eine Menüleiste redundant macht.
-   Blenden Sie die Menüleiste aus, anstatt sie vollständig zu entfernen, da Menüleisten für Tastatur Benutzer besser zugänglich sind.
-   Um die Menüleiste wiederherzustellen, geben Sie eine Menüleisten-Kontrollkästchen-Option in der Ansicht (für primäre Symbolleisten) oder Tools (für sekundäre Symbolleisten) an. Weitere Informationen finden Sie unter [Standard Menü und unterteilte Schalt](#standard-menu-and-split-buttons)Flächen.
-   Zeigen Sie die Menüleiste an, wenn Benutzer die Alt-Taste drücken, und legen Sie den Eingabefokus in der ersten Menükategorie fest.

### <a name="interaction"></a>Interaktion

-   Zeigen Sie auf dem Mauszeiger [auf die](glossary.md) Schaltfläche, um anzugeben, dass das Symbol klickbar ist. Zeigen Sie nach dem QuickInfo-Timeout die QuickInfo oder den infotip an.

    ![Screenshot eines Infotipp, der eine Schaltfläche beschreibt ](images/cmd-toolbars-image40.png)

    Dieses Beispiel zeigt die verschiedenen Anzeige Zustände.

-   Bei der linken Maustaste:
    -   Interagieren Sie für Befehls Schaltflächen mit dem Steuerelement wie gewohnt.
    -   Zeigen Sie das Steuerelement für Modus-Schaltflächen an, um den derzeit ausgewählten Modus wiederzugeben. Wenn sich der Modus auf das Verhalten der Maus Interaktion auswirkt, ändern Sie auch den-Zeiger.

        ![Screenshot eines Zeigers, der wie ein Paint-Bucket geformt ist ](images/cmd-toolbars-image41.png)

        In diesem Beispiel wird der Zeiger so geändert, dass der Maus Interaktionsmodus angezeigt wird.

    -   Zeigen Sie für Eigenschafts Schaltflächen und Dropdown Listen das Steuerelement an, um den Zustand der aktuell ausgewählten Objekte (sofern vorhanden) widerzuspiegeln. Aktualisieren Sie bei der Interaktion den Zustand des Steuer Elements, und wenden Sie die Änderung auf die ausgewählten Objekte an. Wenn nichts ausgewählt ist, tun Sie nichts.

-   Führen Sie bei einem Doppelklick mit der linken Maustaste dieselbe Aktion aus wie bei einem linken Mausklick.
    -   **Ausnahme:** In seltenen Fällen kann ein Symbolleisten Befehl effizienter modale verwendet werden. Verwenden Sie in solchen Fällen doppelklicken, um den Modus zu wechseln.

        ![Screenshot des Infotipp mit den Funktionen der Schaltfläche ](images/cmd-toolbars-image42.png)

        In diesem Beispiel wechselt der Befehl zum Formatieren von Malern in einen Modus, in dem alle nachfolgenden Klicks das Format anwenden. Benutzer können den Modus verlassen, indem Sie mit der linken Maustaste klicken.

-   Klicken Sie mit der rechten Maustaste auf:
    -   Zeigen Sie für anpassbare Symbolleisten das Kontextmenü zum Anpassen der Symbolleiste an. Zeigen Sie das Menü an, und klicken Sie mit der rechten Maustaste auf den Pfeil nach unten und nicht auf die
    -   Führen Sie für andere Symbolleisten keine Aktion aus.

### <a name="icons"></a>Symbole

-   **Stellen Sie Symbole für alle Symbolleisten-Steuerelemente außer Dropdown Listen bereit.**

    ![Screenshot der Dropdown Liste "Schriftart Größe" ](images/cmd-toolbars-image43.png)

    Dropdown Listen benötigen keine Symbole, aber alle anderen Symbolleisten-Steuerelemente.

    **Ausnahme:** Symbolleisten im Windows 7-Stil verwenden Symbole nur für Befehle, deren Symbole bekannt sind. Andernfalls werden Text Beschriftungen ohne Symbole verwendet. Dies verbessert die Übersichtlichkeit der Bezeichnungen, erfordert jedoch mehr Platz.

-   **Stellen Sie sicher, dass Symbolleisten Symbole für die Hintergrundfarbe der Symbolleiste eindeutig sichtbar sind.** Wertet Symbolleisten Symbole immer im Kontext und im Modus mit hohem Kontrast aus.
-   **Wählen Sie Symbol Entwürfe aus, die ihren Zweck eindeutig vermitteln, insbesondere für die am häufigsten verwendeten Befehle.** Gut gestaltete Symbolleisten benötigen Symbole, die selbsterklärend sind, da Benutzer keine Befehle effizient mithilfe ihrer Quick Infos finden können. Symbolleisten funktionieren jedoch immer noch gut, wenn Symbole für einige weniger häufig verwendete Befehle nicht selbsterklärend sind.
-   **Wählen Sie Symbole aus, die erkennbar und unterschieden werden können, insbesondere für die am häufigsten verwendeten Befehle.** Stellen Sie sicher, dass die Symbole über unterschiedliche Formen und Farben verfügen. Auf diese Weise können Benutzer die Befehle schnell finden, auch wenn Sie das symbolsymbol nicht merken.
-   **Stellen Sie sicher, dass Symbolleisten Symbole den Richtlinien des Aero-Style-Symbols entsprechen.**

Weitere Informationen und Beispiele finden Sie unter [Symbole](vis-icons.md).

### <a name="standard-menu-and-split-buttons"></a>Standard Menü und unterteilte Schaltflächen

Wenn Sie Menü Schaltflächen und Trenn Schaltflächen in einer Symbolleiste verwenden, versuchen Sie, die folgenden Standardmenü Strukturen und ihre entsprechenden Befehle zu verwenden, wann immer dies möglich ist. Im Gegensatz zu Menüleisten werden von Symbolleisten Befehlen keine Zugriffstasten übernommen.

**Primäre Symbolleisten**

Diese Befehle spiegeln die Befehle in Standardmenü leisten wider, sodass Sie nur für primäre Symbolleisten verwendet werden sollten. Diese Liste zeigt die Schaltflächen Beschriftungen (und den Typ) mit ihrer Reihenfolge und Trennzeichen, den Tastenkombinationen und den Ellipsen an. **Beachten Sie, dass der Befehl zum Anzeigen und Ausblenden der Menüleiste im Menü Ansicht angezeigt wird.**

<dl> File <dl> Newstrg + N  
Öffnen Sie... STRG + O  
Schließen <separator>  
Savectrl + S  
Speichern unter... <separator>  
Senden an <separator>  
Drucken... STRG + P  
Seitenansicht  
Seite einrichten <separator>  
Exitalt + F4 (in der Regel nicht angegeben)
</dl> </dd> Edit(menu button) <dl> Undoctrl + Z  
Redoctrl + Y <separator>  
Schneide STRG + X  
Copystrg + C  
Pastectrl + V <separator>  
Wählen Sie allstrg + A <separator>  
Deletedel (in der Regel nicht angegeben)  
Umbenennen... <separator>  
Suchen... STRG + F  
NextF3 suchen (Befehl in der Regel nicht angegeben)  
Ersetzen... STRG + H  
Gehe zu... STRG + G
</dl> </dd> <dd>Drucken (Trenn Schaltfläche) <dl> Drucken... STRG + P  
Seitenansicht <separator>  
Seiteneinrichtung
</dl> </dd> Anzeigen (Menü Schaltfläche) <dl> Menüleiste (überprüfen, wenn sichtbar)  
Detailbereich (überprüfen, ob sichtbar)  
Vorschaubereich (überprüfen, wenn sichtbar)  
Status Leiste (überprüfen, wenn sichtbar) <separator>  
Zoom  
Zoom-inctrl + +  
Zoom-ausstrg +- <separator>  
Textgröße (ausgewählte Einstellung hat Aufzählungs Zeichen) <dl> Möglichst  
Größer  
Medium  
Kleiner  
Ster
</dl> </dd> <separator> Vollständige screenF11  
RefreshF5
</dl> </dd> Tools(menu button) <dl> ... <separator>  
Optionen
</dl>> </dd> Help(split button, use the Help icon) <dl> <program name> helpF1 <separator>  
Zu <program name>  
</dl> </dd> </dl>

**Ergänzende Symbolleisten**

Diese Befehle ergänzen Standardmenü leisten. Diese Liste zeigt die Schaltflächen Beschriftungen (und den Typ) mit ihrer Reihenfolge und Trennzeichen, den Tastenkombinationen und den Ellipsen an. **Beachten Sie, dass der Befehl zum Anzeigen und Ausblenden der Menüleiste im Menü Extras angezeigt wird.**

Die Namen der ergänzenden Symbolleisten Kategorien unterscheiden sich von den standardmäßigen Menü Kategorienamen, da Sie umfassender sein müssen. Beispielsweise wird die Kategorie organisieren anstelle von Bearbeiten verwendet, da Sie Befehle enthält, die nicht mit der Bearbeitung verknüpft sind. **Um die Konsistenz zwischen Menüleisten und Symbolleisten zu gewährleisten, verwenden Sie die Standardmenü Kategorien Amen, wenn dies nicht irreführend wäre.**

**Falsch:**

![Screenshot der gleichen Optionen für verschiedene Befehle ](images/cmd-toolbars-image44.png)

In diesem Beispiel sollte die Symbolleiste "Bearbeiten" anstelle von "organisieren" verwenden, da Sie über die Standard Befehle zum Bearbeiten des Menüs verfügt.

### <a name="palette-windows"></a>Palettenfenster

-   **Palettenfenster verwenden kürzere Titelleisten, um den Bildschirmbereich zu minimieren.** Legen Sie die Schaltfläche Schließen auf der Titelleiste ab.
-   **Legen Sie den Text der Titelleiste auf den Befehl fest, der das Palettenfenster angezeigt hat.**
-   **Verwenden Sie die Groß-/Kleinschreibung im Satz Stil ohne das Beenden der**
-   **Geben Sie ein Kontextmenü für Fenster Verwaltungs Befehle an.** Zeigen Sie dieses Kontextmenü an, wenn Benutzer mit der rechten Maustaste auf die Titelleiste klicken.

    ![Screenshot der Toolbox mit einem Kontextmenü ](images/cmd-toolbars-image45.png)

    In diesem Beispiel können Benutzer mit der rechten Maustaste auf die Titelleiste klicken, um das Kontextmenü anzuzeigen.

-   **Wenn dies möglich und nützlich ist, können Sie Palettenfenster ändern.** Geben Sie an, dass die Größe des Fensters geändert werden kann
-   **Wenn ein Palettenfenster erneut angezeigt wird, zeigen Sie es mit demselben Zustand an, auf das zuletzt zugegriffen wurde.** Wenn Sie schließen, speichern Sie die Fenstergröße und den Speicherort. Stellen Sie bei der erneuten Anzeige die Größe und den Speicherort des gespeicherten Fensters wieder her. Außerdem sollten Sie diese Attribute in den einzelnen Programm Instanzen auf Benutzerbasis beibehalten.

### <a name="customization"></a>Anpassung

-   **Stellen Sie Anpassungen für Symbolleisten bereit, die aus zwei oder mehr Zeilen bestehen.** Nur der unbezeichnete Symbol Stil muss angepasst werden. Einfache Symbolleisten mit wenigen Befehlen müssen nicht angepasst werden.
-   **Stellen Sie eine gute Standardkonfiguration bereit.** Benutzer sollten Ihre Symbolleisten nicht für gängige Szenarien anpassen. Verlassen Sie sich nicht darauf, dass Benutzer ihren Weg aus einer ungültigen anfänglichen Konfiguration anpassen. Nehmen Sie an, dass die meisten Benutzer Ihre Symbolleisten nicht anpassen.
-   **Geben Sie ein Kontextmenü mit den folgenden Befehlen an:**
    -   Eine Liste der Kontrollkästchen zum Anzeigen der verfügbaren Symbolleisten
    -   Symbolleisten sperren/entsperren
    -   Anpassen...
-   Hiermit werden **anpassbare Symbolleisten standardmäßig gesperrt**, um versehentliche Änderungen zu verhindern.
-   **Zum Anpassen des Befehls wird ein Dialogfeld mit den Optionen angezeigt** , in dem Sie auswählen können, welche Symbolleisten angezeigt werden und welche Befehle auf den einzelnen Symbolleisten angezeigt werden.

    ![Screenshot des Dialog Felds "anpassen" und der Optionen ](images/cmd-toolbars-image46.png)

    In diesem Beispiel bietet Visual Studio ein Dialogfeld "Optionen", in dem die Symbolleisten angepasst werden.

-   Stellen Sie einen Reset-Befehl bereit, um zur ursprünglichen Symbolleisten Konfiguration im Dialogfeld Optionen anpassen zurückzukehren.
-   **Mit Drag & Drop können Sie die Symbolleisten wie folgt anpassen:**

    -   Festlegen von Symbolleisten Reihenfolge und Positionen.
    -   Legen Sie Symbolleisten Längen fest, und zeigen Sie Symbolleisten an, die zu klein sind, um deren Inhalt mit einem Überlauf-Chevron anzuzeigen.
    -   Wenn unterstützt, lösen Sie Symbolleisten aus, sodass Sie zu palettenfenstern werden und umgekehrt.

    Wenn das Dialogfeld Optionen anpassen angezeigt wird:

    -   Legen Sie den Symbolleisten Inhalt fest.
    -   Legt die Reihenfolge der Symbolleisten Inhalte fest.

    Auf diese Weise können Benutzer Änderungen direkt und effizient vornehmen.

-   **Speichern Sie alle Benutzer Symbolleisten Anpassungen** auf Benutzerbasis.

### <a name="using-ellipses"></a>Verwenden von Ellipsen

Obwohl Symbolleisten Befehle für sofortige Aktionen verwendet werden, sind manchmal Weitere Informationen erforderlich, um die Aktion auszuführen. Verwenden Sie ein Auslassungs Zeichen, um anzugeben, dass ein Befehl weitere Informationen erfordert, bevor er wirksam werden kann. Fügen Sie die Auslassungs Punkte am Ende der QuickInfo und der Bezeichnung ein, sofern vorhanden.

![Screenshot des druckquickinfo-Texts mit Auslassungs Zeichen ](images/cmd-toolbars-image47.png)

In diesem Beispiel wird der Druck... Befehl zeigt ein Druck Dialogfeld an, um weitere Informationen zu sammeln.

Wenn ein Befehl nicht sofort wirksam werden kann, ist jedoch keine Auslassungs Punkte erforderlich. Beispielsweise verfügen Freigabe Einstellungen nicht über ein Ellipsen, obwohl zusätzliche Informationen erforderlich sind, da der Befehl nicht sofort wirksam werden kann.

![Screenshot der Symbolleiste, des Befehls und der QuickInfo ](images/cmd-toolbars-image48.png)

Der Befehl für die Freigabe Einstellungen weist keine Auslassungs Punkte auf, da er nicht sofort wirksam werden kann.

Da Symbolleisten ständig angezeigt werden und der Speicherplatz in einem Premium-Bereich liegt, **sollten Ellipsen nur selten verwendet werden**.

> [!Note]  
> Für Menüs, die auf einer Symbolleiste angezeigt werden, wenden Sie die [Richtlinien](cmd-menus.md)für den Menübefehl

 

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstände

![Bildschirm Abbildung von Symbolleisten mit Abstands Informationen ](images/cmd-toolbars-image49.png)

Empfohlene Größe und Abstände für Standard Symbolleisten.

## <a name="labels"></a>Bezeichnungen

### <a name="general"></a>Allgemein

-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
    -   **Ausnahme:** Bei älteren Anwendungen können Sie ggf. die Groß-/Kleinschreibung von Titeln verwenden, um das Mischen von Groß-/Kleinschreibung

### <a name="unlabeled-icon-buttons"></a>Nicht beschriftete Symbol Schaltflächen

-   **Verwenden Sie eine QuickInfo, um den Befehl zu bezeichnen.** Verwenden Sie für den QuickInfo-Text das, was die Bezeichnung wäre, wenn die Schaltfläche mit der Bezeichnung versehen wäre, und schließen Sie ggf. die Tastenkombination ein.

    ![Screenshot der Symbolleiste, des Drucker Symbols und der QuickInfo ](images/cmd-toolbars-image50.png)

    Ein Beispiel für eine Symbol Schaltflächen-QuickInfo.

### <a name="labeled-icon-buttons"></a>Beschriftete Symbolschaltflächen

-   **Verwenden Sie eine präzise Bezeichnung.** Verwenden Sie, wenn möglich, ein einzelnes Wort, höchstens vier Wörter.
-   **Platzieren Sie die Bezeichnung auf der rechten Seite des Symbols.**
-   **Verwenden Sie einen InfoTipp, um den Befehl zu beschreiben.** Da die Schaltflächen gekennzeichnet sind, wäre die Verwendung einer QuickInfo anstelle eines Infotipp redundant.

    ![Screenshot der beschrifteten Schaltfläche mit Infotipp ](images/cmd-toolbars-image51.png)

    Ein Beispiel für einen InfoTipp mit der Bezeichnung Symbol Schaltfläche.

### <a name="drop-down-lists"></a>Dropdownlisten

-   **Wenn die Liste immer über einen Wert verfügt, verwenden Sie den aktuellen Wert als Bezeichnung.**

    ![Screenshot der Symbolleiste mit Schriftart Optionen ](images/cmd-toolbars-image52.png)

    In diesem Beispiel fungiert der aktuell ausgewählte Schriftart Name als Bezeichnung.

-   Wenn eine bearbeitbare Dropdown Liste keinen Wert hat, verwenden Sie eine [Eingabeaufforderung](glossary.md).

    ![Screenshot der Such Adressbücher für die Listen Bezeichnung ](images/cmd-toolbars-image53.png)

    In diesem Beispiel wird eine Eingabeaufforderung für die Bezeichnung der Dropdown Liste verwendet.

### <a name="menu-buttons-and-split-buttons"></a>Menü-und Trenn Schaltflächen

-   **Verb-basierte Menü Schaltflächen Namen bevorzugen.** Lassen Sie jedoch das Verb aus, wenn es erstellen, anzeigen, anzeigen oder verwalten ist. Beispielsweise haben **Tools** und **Seiten** Menü Schaltflächen keine Verben.
-   **Verwenden Sie ein einzelnes, bestimmtes Wort, das den Menü Inhalt eindeutig und genau beschreibt.** Obwohl die Namen nicht so allgemein sein müssen, dass Sie alles im Menü beschreiben, sollten Sie vorhersehbar genug sein, damit die Benutzer nicht überrascht sind, was Sie im Menü finden.
-   **Wenn dies nicht erforderlich ist, geben Sie Infotipp-Beschreibungen an, wenn Sie hilfreich sind.**

### <a name="menu-items"></a>Menüelemente

-   **Verwenden Sie Menü Elementnamen, die mit einem Verb, einem Substantiv oder einem Substantiv Ausdruck beginnen.**
-   **Verb-basierte Menü Namen bevorzugen.** Lassen Sie jedoch das Verb aus, wenn es erstellen, anzeigen, anzeigen oder verwalten ist. Die folgenden Befehle verwenden z. b. keine Verben:
    -   Info
    -   Fortgeschrittene
    -   Vollbildmodus
    -   Neu
    -   Optionen
    -   Eigenschaften
-   **Verwenden Sie bestimmte Verben.** Vermeiden Sie generische, nicht hilfreiche Verben wie z. b. ändern und verwalten.
-   **Verwenden Sie Singular Nomen für Befehle, die auf ein einzelnes Objekt angewendet werden, und verwenden Sie** andernfalls Plural Nomen.
-   **Wählen Sie für Paare von ergänzenden Befehlen eindeutig ergänzende Namen aus.** Beispiele: Hinzufügen, entfernen; Anzeigen, ausblenden; Einfügen, löschen.
-   **Wählen Sie die Namen der Menü Elemente basierend auf den Benutzer Zielen und Aufgaben, nicht auf der Technologie aus.**
-   Verwenden Sie die folgenden Menü Elementnamen für den angegebenen Zweck:
    -   **Optionen:** , Um Programmoptionen anzuzeigen.
    -   **Anpassen:** Zum Anzeigen der Programmoptionen, die sich speziell auf die Konfiguration der mechanischen Benutzeroberfläche beziehen.
    -   **Personalisieren:** Um eine Zusammenfassung der häufig verwendeten [Personalisierungs](glossary.md) Einstellungen anzuzeigen.
    -   **Einstellungen:** Verwenden Sie nicht. Verwenden Sie stattdessen Optionen.
    -   **Eigenschaften:** , Wenn das Eigenschaften Fenster eines Objekts angezeigt werden soll.
    -   **Einstellungen:** Verwenden Sie nicht als Menü Bezeichnung. Verwenden Sie stattdessen Optionen.
-   **Menü Elemente, in denen Untermenüs angezeigt werden, haben nie eine Ellipse für ihre Bezeichnung.** Der unter Menü Pfeil gibt an, dass eine andere Auswahl erforderlich ist.

## <a name="documentation"></a>Dokumentation

Wenn Sie auf Symbolleisten verweisen:

-   Wenn nur eine Symbolleiste vorhanden ist, lesen Sie diese als Symbolleiste.
-   Wenn mehrere Symbolleisten vorhanden sind, können Sie diese anhand des Namens, gefolgt von der Word-Symbolleiste, anzeigen. Lesen Sie die Hauptsymbol Leiste, die standardmäßig aktiviert ist, und enthält Schaltflächen für grundlegende Aufgaben, z. b. das Öffnen und Drucken einer Datei, als Standard Symbolleiste.
-   Die Symbolleiste ist ein einzelnes, nicht groß geschrisiertes Wort. (Im Gegensatz dazu handelt es sich bei der Menüleiste um zwei Wörter.)
-   Informationen zu den Symbolleisten-Schaltflächen finden Sie unter. Verwenden Sie den genauen Bezeichnungs Text, einschließlich der Groß-/Kleinschreibung, aber keine Auslassungs Zeichen.
-   Weitere Informationen finden Sie unter den Menü Schaltflächen auf der Symbolleiste. Verwenden Sie den genauen Bezeichnungs Text, einschließlich der Groß-/Kleinschreibung
-   Verwenden Sie Symbolleisten-Steuerelemente als Symbolleisten Schaltflächen.
-   Um die Interaktion von Benutzern zu beschreiben, verwenden Sie für Symbolleisten Schaltflächen und schreibgeschützte Dropdown Listen, und geben Sie für bearbeitbare Dropdown Listen ein. Verwenden Sie SELECT, SELECT oder Pick nicht.
-   Verwenden Sie nicht Cascading, pulldowndown, Dropdown Liste oder Popup, um Menü Schaltflächen zu beschreiben, außer in der Programmier Dokumentation.
-   Verweisen Sie auf nicht verfügbare Elemente als nicht verfügbar, nicht als abgeblendet, deaktiviert oder abgeblendet. Verwenden Sie deaktivierte in der Programmier Dokumentation.
-   Formatieren Sie die Bezeichnungen nach Möglichkeit mithilfe von fettem Text. Andernfalls sollten Sie die Bezeichnungen nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiele:

-   Klicken Sie im Menü **Seite** auf der Symbolleiste auf **Seite per e-Mail senden**.
-   Geben Sie auf der Symbolleiste im Feld **Schriftarten** den Text "Segoe UI" ein.
-   Zeigen Sie auf der Symbolleiste **Formatierung** auf **anzeigen**, und klicken Sie dann auf **Kommentare**.

 

