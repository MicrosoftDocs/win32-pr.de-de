---
title: Symbolleisten
description: Symbolleisten sind eine Möglichkeit, Befehle für effizienten Zugriff zu gruppieren.
ms.assetid: 8f36307c-54fc-493d-a2ff-57db29e3508d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8015e1dec17ad524645b474b21d42af9269ffbc8d24279c56612620f0e4bb615
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118450034"
---
# <a name="toolbars"></a>Symbolleisten

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Symbolleisten sind eine Möglichkeit, Befehle für effizienten Zugriff zu gruppieren.

![Screenshot von zwei Symbolleisten mit bezeichneten Elementen ](images/cmd-toolbars-image1.png)

Einige typische Symbolleisten.

**Verwenden Sie Zusätzlich zu oder statt Menüleisten Symbolleisten.** Symbolleisten können effizienter als Menüleisten sein, da sie direkt sind (immer angezeigt, anstatt per Mausklick angezeigt zu werden), sofort (anstatt zusätzliche Eingaben zu erfordern) und die am häufigsten verwendeten Befehle enthalten (anstelle einer umfassenden Liste). Im Gegensatz zu Menüleisten müssen Symbolleisten nicht umfassend oder selbsterklärend sein, sondern nur schnell, bequem und effizient sein.

Einige Symbolleisten sind anpassbar, sodass Benutzer Symbolleisten hinzufügen oder entfernen, ihre Größe und Position ändern und sogar ihre Inhalte ändern können. Einige Arten von Symbolleisten können rückgängig gemacht werden, was zu einem Palettenfenster führt. Weitere Informationen zu Symbolleistenvarianten finden Sie unter [Verwendungsmuster](#usage-patterns) in diesem Artikel.

> [!Note]  
> Richtlinien im Zusammenhang [mit Menüs,](cmd-menus.md) [Befehlsschaltflächen](ctrl-command-buttons.md)und [Symbolen](vis-icons.md) werden in separaten Artikeln vorgestellt.

 

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Ist das Fenster ein primäres Fenster?** Symbolleisten funktionieren gut für primäre Fenster, sind aber in der Regel für sekundäre Fenster überfordert. Verwenden Sie für sekundäre Fenster [stattdessen Befehlsschaltflächen,](ctrl-command-buttons.md) [Menüschaltflächen](ctrl-command-buttons.md) [und](ctrl-command-links.md) Links.
-   **Gibt es eine kleine Anzahl häufig verwendeter Befehle?** Symbolleisten können nicht so viele Befehle verarbeiten wie Menüleisten, daher funktionieren sie am besten als Möglichkeit, effizient auf eine kleine Anzahl häufig verwendeter Befehle zu zugreifen.
-   **Sind die meisten Befehle sofort?** Das heißt, sind sie größtenteils Befehle, die keine zusätzliche Eingabe erfordern? Um effizient zu sein, müssen Symbolleisten ein direktes und sofortiges Gefühl haben. Wenn nicht, eignen sich Menüleisten besser für Befehle, die zusätzliche Eingaben erfordern.
-   **Können die meisten Befehle direkt angezeigt werden?** Das heißt, benutzer interagieren mit ihnen mit einem einzigen Klick? Einige Befehle können zwar mithilfe von Menüschaltflächen angezeigt werden, aber die meisten Befehle auf diese Weise zu präsentieren, beeinträchtigt die Effizienz der Symbolleiste, wodurch eine Menüleiste eine bessere Wahl ist.
-   **Werden die Befehle gut durch Symbole dargestellt?** Symbolleistenschaltflächen werden in der Regel durch Symbole anstelle von Textbezeichnungen dargestellt (obwohl einige Symbolleistenschaltflächen beide verwenden), während Menübefehle durch ihren Text dargestellt werden. Wenn die Befehlssymbole keine hohe Qualität haben und nicht selbsterklärend sind, ist eine Menüleiste möglicherweise die bessere Wahl.

Wenn Ihr Programm über eine Symbolleiste ohne Menüleiste verfügt und die meisten Befehle indirekt über Menüschaltflächen und geteilte Schaltflächen zugänglich [sind,](ctrl-command-buttons.md)ist diese Symbolleiste im Wesentlichen eine Menüleiste. Wenden Sie [stattdessen das Symbolleistenmenümuster](cmd-menus.md) in den Menürichtlinien an.

## <a name="design-concepts"></a>Entwurfskonzepte

Eine gute Menüleiste ist ein umfassender Katalog aller verfügbaren Befehle der obersten Ebene, während eine gute Symbolleiste schnellen und komfortablen Zugriff auf häufig verwendete Befehle bietet. Eine Symbolleiste versucht nicht, Benutzer zu trainieren, um sie nur produktiv zu machen. Sobald Benutzer erfahren, wie sie auf einen Befehl auf einer Symbolleiste zugreifen, greifen sie selten weiterhin über die Menüleiste auf den Befehl zu. Aus diesen Gründen müssen die Menüleiste und die Symbolleiste eines Programms nicht direkt übereinstimmen.

### <a name="toolbars-vs-menu-bars"></a>Symbolleisten im Vergleich zu Menüleisten

Traditionell unterscheiden sich Symbolleisten wie folgt von Menüleisten:

-   **Frequenz.** Symbolleisten stellen nur die am häufigsten verwendeten Befehle bereit, während Menüleisten alle verfügbaren Befehle der obersten Ebene innerhalb eines Programms katalogisieren.
-   **Unmittelbarkeit.** Das Klicken auf einen Symbolleistenbefehl wird sofort wirksam, während ein Menübefehl möglicherweise zusätzliche Eingaben erfordert. Beispielsweise zeigt ein Befehl Drucken in einer Menüleiste zuerst das Dialogfeld Drucken an, während eine Schaltfläche der Symbolleiste Drucken sofort eine einzelne Kopie eines Dokuments auf dem Standarddrucker aus druckt.

    ![Screenshot der ausgewählten Druckerschaltfläche der Symbolleiste ](images/cmd-toolbars-image2.png)

    In diesem Beispiel wird durch Klicken auf die Symbolleistenschaltfläche Drucken sofort eine einzelne Kopie eines Dokuments auf dem Standarddrucker gedruckt.

-   **Direktheit.** Symbolleistenbefehle werden mit nur einem Klick aufgerufen, während Menüleistenbefehle eine Navigation durch das Menü erfordern.
-   **Anzahl und Dichte.** Der für eine Symbolleiste erforderliche Bildschirmbereich ist proportional zur Anzahl der Befehle, und dieser Platz wird immer verwendet, auch wenn die Befehle nicht verwendet werden. Folglich müssen Symbolleisten ihren Platz effizient nutzen. Im Gegensatz dazu werden Menüleistenbefehle normalerweise nicht angezeigt, und ihre hierarchische Struktur ermöglicht eine beliebige Anzahl von Befehlen.
-   **Größe und Präsentation.** Um viele Befehle in einem kleinen Bereich zu packen, verwenden Symbolleisten in der Regel symbolbasierte Befehle (mit QuickInfo-basierten Bezeichnungen), während Menüleisten textbasierte Befehle (mit optionalen Symbolen) verwenden. Symbolleistenschaltflächen können zwar Standardtextbezeichnungen haben, diese verwenden jedoch deutlich mehr Platz.

    ![Screenshot der Symbolleiste mit Sende-/Empfangsbezeichnung ](images/cmd-toolbars-image3.png)

    Beschriftete Symbolleistenschaltflächen nehmen mindestens dreimal so viel Platz ein wie nicht bezeichnete Schaltflächen.

-   **Selbsterklärend** Gut entworfene Symbolleisten benötigen Symbole, die größtenteils selbsterklärend sind, da Benutzer Befehle nur mithilfe von QuickInfos nicht effizient finden können. Symbolleisten funktionieren jedoch weiterhin gut, wenn einige weniger häufig verwendete Befehle nicht selbsterklärend sind.

    ![Screenshot der Symbolleiste mit vertrauten Symbolen ](images/cmd-toolbars-image4.png)

    In diesem Beispiel sind die am häufigsten verwendeten Symbole selbsterklärend.

-   **Erkennbar und unterscheidbar.** Bei häufig verwendeten Befehlen merken sich Benutzer Symbolleisten-Schaltflächenattribute wie Position, Form und Farbe. Mit gut entworfenen Symbolleisten können Benutzer die Befehle schnell finden, auch wenn sie sich nicht genau an das Symbolsymbol erinnern. Im Gegensatz dazu merken sich Benutzer häufig verwendete Menüleisten-Befehlspositionen, verlassen sich jedoch bei der Auswahl auf die Befehlsbezeichnungen.

    ![Screenshot des Dialogfelds "Optionen für das Snippingtool" ](images/cmd-toolbars-image5.png)

    Bei Symbolleistenbefehlen können Symbole durch charakteristische Position, Form und Farbe erkennbar und unterscheidbar werden.

    ![Screenshot der Menüleiste mit ausgewähltem Dateibefehl ](images/cmd-toolbars-image6.png)

    Bei Menüleistenbefehlen sind Benutzer letztendlich von ihren Bezeichnungen abhängig.

### <a name="efficiency"></a>Effizienz

Angesichts ihrer Merkmale müssen Symbolleisten in erster Linie für Effizienz entworfen werden. Eine ineffiziente Symbolleiste ist einfach nicht sinnvoll.

**Wenn Sie nur eins tun...**

Stellen Sie sicher, dass Ihre Symbolleisten in erster Linie auf Effizienz ausgelegt sind. Konzentrieren Sie sich auf Symbolleisten auf häufig verwendete Befehle, die sofort, direkt und schnell erkennbar sind.

### <a name="hiding-menu-bars"></a>Ausblenden von Menüleisten

Im Allgemeinen funktionieren Symbolleisten gut zusammen mit Menüleisten: Gute Symbolleisten bieten Effizienz, und gute Menüleisten bieten Umfassendes. **Sowohl Menüleisten als auch Symbolleisten ermöglichen es jedem, sich ohne Kompromittierung auf seine Stärken zu konzentrieren.**

Es ist überraschend, dass dieses Modell mit einfachen Programmen unterbricht. Für Programme mit nur wenigen Befehlen ist es nicht sinnvoll, sowohl eine Menüleiste als auch eine Symbolleiste zu verwenden, da die Menüleiste eine redundante, ineffiziente Version der Symbolleiste ist.

Um diese Redundanz zu vermeiden, konzentrieren sich viele einfache Programme in Windows Vista darauf, Befehle ausschließlich über die Symbolleiste zur Verfügung zu stellen und die Menüleiste standardmäßig zu verbergen. Zu diesen Programmen gehören Windows Explorer, Windows Internet Explorer, Windows Media Player und Windows Fotogalerie.

Dies ist keine kleine Änderung. Das Entfernen der Menüleiste ändert die Art der Symbolleisten grundlegend, da solche Symbolleisten umfassend sein müssen und sich auf folgende Weise ändern müssen:

-   **Frequenz.** Das Entfernen der Menüleiste bedeutet, dass auf alle Befehle, die nicht direkt in einem Fenster oder in den Kontextmenüs verfügbar sind, unabhängig von ihrer Verwendungshäufigkeit über die Symbolleiste zugegriffen werden muss.
-   **Unmittelbarkeit.** Wenn Sie die Menüleiste entfernen, ist die Symbolleiste der einzige sichtbare Zugriffspunkt für Befehle, der erfordert, dass die Symbolleiste über voll funktionsfähige Versionen verfügt. Wenn beispielsweise keine Menüleiste verfügbar ist, muss der Befehl Drucken auf einer Symbolleiste das Dialogfeld Drucken anzeigen, anstatt sofort zu drucken. (Obwohl die Verwendung einer geteilten Schaltfläche in diesem Fall ein hervorragender Kompromiss ist. Weitere Informationen [finden Sie unter Standardmenü und Teilungsschaltflächen](#standard-menu-and-split-buttons) für die Standardschaltfläche "Drucken teilen".)

    ![Screenshot der Optionen der Symbolleiste und des Druckbefehls ](images/cmd-toolbars-image7.png)

    In diesem Beispiel verfügt die Symbolleistenschaltfläche Drucken in Windows Fotogalerie über den Befehl Drucken, der das Dialogfeld Drucken anzeigt.

-   **Direktheit.** Um Platz zu sparen und unübersichtlich zu vermeiden, werden weniger häufig verwendete Befehle möglicherweise in Menüschaltflächen verschoben, wodurch sie weniger direkt sind.

Symbolleisten, die zum Ergänzen einer Menüleiste verwendet werden, sind anders als Symbolleisten für die Verwendung mit einer entfernten oder ausgeblendeten Menüleiste konzipiert. Und da Sie nicht davon ausgehen können, dass Benutzer eine ausgeblendete Menüleiste anzeigen, um einen einzelnen Befehl auszuführen, sollte das Ausblenden einer Menüleiste genauso behandelt werden wie das entfernen, wenn Entwurfsentscheidungen getroffen werden. (Wenn Sie die Menüleiste standardmäßig ausblenden, gehen Sie nicht davon aus, dass Benutzer die Menüleiste anzeigen möchten, um nach einem Befehl zu suchen oder sogar herauszufinden, wie sie angezeigt wird.)

Das Entwerfen einer Symbolleiste, die ohne Menüleiste funktioniert, umfasst häufig einige Kompromittierung. Aus Effizienzgründen sollte jedoch nicht zu viel kompromitt werden. Wenn das Ausblenden der Menüleiste zu einer ineffizienten Symbolleiste führt, blenden Sie die Menüleiste nicht aus!

### <a name="keyboard-accessibility"></a>Barrierefreiheit der Tastaturnavigation

Über die Tastatur unterscheidet sich der Zugriff auf Symbolleisten stark vom Zugriff auf Menüleisten. Menüleisten erhalten den Eingabefokus, wenn Benutzer die ALT-TASTE drücken und den Eingabefokus mit der ESC-TASTE verlieren. Sobald eine Menüleiste den Eingabefokus besitzt, wird sie unabhängig vom Rest des Fensters navigiert, wobei alle Pfeiltasten, Start-, End- und Tabulatortasten verarbeitet werden. Im Gegensatz dazu erhalten Symbolleisten den Eingabefokus, wenn Benutzer die TAB-TASTE durch den gesamten Inhalt des Fensters drücken. Da Symbolleisten zuletzt in der Aktivierreihenfolge angezeigt werden, kann die Aktivierung auf einer ausgelasteten Seite einen erheblichen Aufwand in Anspruch nehmen (es sei denn, Benutzer wissen, dass sie UMSCHALT+TAB verwenden, um rückwärts zu wechseln).

Die Barrierefreiheit stellt hier ein Problem dar: Obwohl Symbolleisten für Mausbenutzer einfacher sind, sind sie für Tastaturbenutzer weniger zugänglich. Dies ist kein Problem, wenn sowohl eine Menüleiste als auch eine Symbolleiste vorhanden sind, aber wenn die Menüleiste entfernt oder ausgeblendet wird.

Aus Gründen der Barrierefreiheit bevorzugen Sie es, die Menüleiste beizubehalten, anstatt sie zugunsten einer Symbolleiste vollständig zu entfernen. Wenn Sie zwischen dem Entfernen der Menüleiste und dem einfachen Ausblenden wählen müssen, sollten Sie sie ausblenden.

## <a name="usage-patterns"></a>Verwendungsmuster

Symbolleisten weisen mehrere Verwendungsmuster auf:



|     Verwendung                                                                                                                 |     Beispiel                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Primäre Symbolleisten**<br/> Eine Symbolleiste, die ohne eine Ausgeblendete oder entfernte Menüleiste funktioniert. <br/> | Primäre Symbolleisten müssen den Bedarf an Effizienz und Vollständigkeit ausgleichen, damit sie am besten für einfache Programme funktionieren. <br/> ![Screenshot der Windows-Explorer-Symbolleiste ](images/cmd-toolbars-image8.png)<br/> Eine primäre Symbolleiste aus Windows Explorer.<br/>                                                                        |
| **Zusätzliche Symbolleisten**<br/> eine Symbolleiste, die für die Arbeit mit einer Menüleiste konzipiert ist. <br/>                         | Zusätzliche Symbolleisten können sich auf Effizienz konzentrieren, ohne kompromittiert zu werden. <br/> ![Screenshot einer Menüleiste über einer Symbolleiste ](images/cmd-toolbars-image9.png)<br/> Eine zusätzliche Symbolleiste aus Windows Movie Maker.<br/>                                                                                                                  |
| **Symbolleistenmenüs**<br/> eine Menüleiste, die als Symbolleiste implementiert ist. <br/>                                        | Symbolleistenmenüs sind Symbolleisten, die in erster Linie aus Befehlen in [Menüschaltflächen](ctrl-command-buttons.md) und geteilten Schaltflächen bestehen, wobei ggf. nur wenige direkte Befehle vorhanden sind. <br/> ![Screenshot der Menüleiste mit Symbolen und Befehlen ](images/cmd-toolbars-image10.png)<br/> Ein Symbolleistenmenü in Windows Fotogalerie.<br/> |
| **Anpassbare Symbolleisten**<br/> eine Symbolleiste, die von Benutzern angepasst werden kann. <br/>                          | Anpassbare Symbolleisten ermöglichen Es Benutzern, Symbolleisten hinzuzufügen oder zu entfernen, ihre Größe und Position zu ändern und sogar ihren Inhalt zu ändern. <br/> ![Screenshot einer Symbolleiste mit Dutzenden von Symbolen ](images/cmd-toolbars-image11.png)<br/> Eine anpassbare Symbolleiste aus Microsoft Visual Studio.<br/>                                             |
| **Palettenfenster**<br/> ein modusloses Dialogfeld, das ein Array von Befehlen darstellt. <br/>                 | Palettenfenster sind abgedockte Symbolleisten. <br/> ![Screenshot eines Dialogfelds "Farben" ](images/cmd-toolbars-image12.png)<br/> ![Screenshot eines Schriftartdialogfelds ](images/cmd-toolbars-image13.png)<br/> Palettenfenster aus Windows Paint.<br/>                                                                             |



 

Symbolleisten weisen diese Stile auf:



|   Style                                                                                                                                     | Beispiel                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Symbole ohne Bezeichnung**<br/> eine oder mehrere Zeilen mit kleinen Symbolschaltflächen ohne Bezeichnung. <br/>                                           | Verwenden Sie diesen Stil, wenn zu viele Schaltflächen für die Bezeichnung vorhanden sind oder das Programm häufig verwendet wird. Mit diesem Stil können Programme mit komplexer Funktionalität mehrere Zeilen enthalten. Daher ist dies der einzige Stil, der angepasst werden muss. mit diesem Stil können einige Befehlsschaltflächen bezeichnet werden, wenn sie häufig verwendet werden. <br/> ![Screenshot der Symbolleiste mit kleinen Symbolen ohne Bezeichnung ](images/cmd-toolbars-image14.png)<br/> Eine Symbolleiste mit nicht bezeichneten Symbolen aus WordPad.<br/> |
| **Große Symbole ohne Bezeichnung**<br/> eine einzelne Zeile mit großen Symbolschaltflächen ohne Bezeichnung. <br/>                                         | Verwenden Sie diesen Stil für einfache Hilfsprogramme, die leicht erkennbare Symbole aufweisen und in der Regel in kleinen Fenstern ausgeführt werden. <br/> ![Screenshot der Symbolleiste mit großen Symbolen ohne Bezeichnung ](images/cmd-toolbars-image15.png)<br/> ![Screenshot der Symbolleiste mit großen Symbolen ](images/cmd-toolbars-image16.png)<br/> Große Symbolleisten ohne Bezeichnungen aus Windows Live Messenger und der Windows Snipping Tool.<br/>                                                                       |
| **Beschriftete Symbole**<br/> eine einzelne Zeile mit kleinen Beschriftungssymbolen. <br/>                                                          | Verwenden Sie diesen Stil, wenn nur wenige Befehle vorhanden sind oder das Programm nicht häufig verwendet wird. dieser Stil verfügt immer über eine einzelne Zeile. <br/> ![Screenshot der Symbolleiste mit beschrifteten Symbolen ](images/cmd-toolbars-image8.png)<br/> Eine symbolleiste mit Bezeichnungen aus Windows Explorer.<br/>                                                                                                                                                                                                               |
| **Partielle Symbolleisten**<br/> eine Teilzeile mit kleinen Symbolen, die verwendet wird, um Speicherplatz zu sparen, wenn keine vollständige Symbolleiste erforderlich ist. <br/>       | Verwenden Sie diesen Stil für Fenster mit Navigationsschaltflächen, einem Suchfeld oder Registerkarten, um unnötige Gewichtung am oberen Rand des Fensters zu vermeiden. <br/> ![Screenshot der Menüleiste, Symbolleiste und Favoritenleiste ](images/cmd-toolbars-image17.png)<br/> Teilsymbolleisten können mit Navigationsschaltflächen, einem Suchfeld oder Registerkarten kombiniert werden.<br/>                                                                                                                                                  |
| **Große Teilsymbolleisten**<br/> eine Teilzeile mit großen Symbolen, die verwendet wird, um Speicherplatz zu sparen, wenn keine vollständige Symbolleiste erforderlich ist. <br/> | Verwenden Sie diesen Stil für einfache Hilfsprogramme mit Navigationsschaltflächen oder einem Suchfeld, um unnötige Gewichtung am oberen Rand des Fensters zu vermeiden. <br/> ![Screenshot einer großen Teilsymbolleiste ](images/cmd-toolbars-image18.png)<br/> Eine große Teilsymbolleiste aus Windows Defender.<br/>                                                                                                                                                                                         |



 

Schließlich weisen Symbolleistensteuerelemente mehrere Verwendungsmuster auf:



|     Verwendung                                                                                                                 |     Beispiel                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Befehlssymbolschaltflächen**<br/> Durch Klicken auf eine Befehlsschaltfläche wird eine sofortige Aktion initiiert. <br/>                                                                                                 | ![Screenshot einer Symbolleiste mit Beschriftungssymbolen ](images/cmd-toolbars-image19.png)<br/> Beispiele für Symbolbefehlsschaltflächen aus Windows Fax und Scan.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Schaltflächen des Modussymbols**<br/> Wenn Sie auf eine Modusschaltfläche klicken, wird der ausgewählte Modus angezeigt. <br/>                                                                                                            | ![Screenshot einer vertikalen Symbolleiste ](images/cmd-toolbars-image20.png)<br/> Beispiele für Modusschaltflächen aus Windows Paint.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Schaltflächen für Eigenschaftensymbole**<br/> Der Zustand einer Eigenschaftenschaltfläche spiegelt ggf. den Zustand der aktuell ausgewählten Objekte wider. Durch Klicken auf die Schaltfläche wird die Änderung auf die ausgewählten Objekte angewendet. <br/> | ![Screenshot der Formatierungssymbole und des ausgewählten Texts ](images/cmd-toolbars-image21.png)<br/> Beispiele für Eigenschaftenschaltflächen aus Microsoft Word.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Beschriftete Symbolschaltflächen**<br/> eine Befehls- oder Eigenschaftenschaltfläche mit einem Symbol und einer Textbezeichnung. <br/>                                                                               | Diese Schaltflächen werden für häufig verwendete Symbolleistenschaltflächen verwendet, deren Symbol nicht ausreichend selbsterklärend ist. Sie werden auch in Symbolleisten mit so wenigen Schaltflächen verwendet, dass jede Schaltfläche eine Textbezeichnung aufweisen kann. <br/> ![Screenshot: Symbolleiste mit Symbolen, die für die am häufigsten verwendeten Schaltflächen gekennzeichnet sind ](images/cmd-toolbars-image22.png)<br/> Eine Symbolleiste mit den am häufigsten verwendeten Schaltflächen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Menüschaltflächen**<br/> eine Befehlsschaltfläche, die verwendet wird, um einen kleinen Satz verwandter Befehle darzustellen. <br/>                                                                                                | Ein einzelnes nach unten zeigende Dreieck gibt an, dass durch Klicken auf die Schaltfläche ein Menü angezeigt wird. <br/> ![Screenshot der Symbolleiste und Dropdown-Befehlsliste ](images/cmd-toolbars-image23.png)<br/> Eine Menüschaltfläche mit einem kleinen Satz verwandter Befehle.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Aufteilen von Schaltflächen**<br/> Eine Befehlsschaltfläche, die verwendet wird, um Variationen eines Befehls zu konsolidieren, insbesondere, wenn einer der Befehle die meiste Zeit verwendet wird. <br/>                                     | ![Screenshot der geteilten Druckschaltfläche ](images/cmd-toolbars-image24.png)<br/> eine geteilte Schaltfläche im normalen Zustand.<br/> Wie bei einer Menüschaltfläche gibt ein einzelnes nach unten zeigende Dreieck an, dass durch Klicken auf den äußersten rechten Teil der Schaltfläche ein Menü angezeigt wird. <br/> ![Screenshot der Befehle für geteilte Druckschaltfläche ](images/cmd-toolbars-image25.png)<br/> eine verworfene geteilte Schaltfläche.<br/> in diesem Beispiel wird eine geteilte Schaltfläche verwendet, um alle druckbezogenen Befehle zu konsolidieren. Der Befehl für den sofortigen Druck wird in den meisten Jahren verwendet, sodass Benutzer die anderen Befehle normalerweise nicht sehen müssen. <br/> Im Gegensatz zu einer Menüschaltfläche führt das Klicken auf den linken Teil der Schaltfläche die Aktion direkt auf der Bezeichnung aus. Teilungsschaltflächen sind in Situationen wirksam, in denen der nächste Befehl wahrscheinlich mit dem letzten Befehl identisch ist. In diesem Fall wird die Bezeichnung in den letzten Befehl geändert, wie bei einer Farbauswahl:<br/> ![Screenshot des Bucketsymbols mit Farbe ](images/cmd-toolbars-image26.png)<br/> In diesem Beispiel wird die Bezeichnung in den letzten Befehl geändert.<br/> |
| **Dropdownlisten**<br/> eine Dropdownliste (bearbeitbar oder schreibgeschützt), die zum Anzeigen oder Ändern einer Eigenschaft verwendet wird. <br/>                                                                                   | ![Screenshot der Dropdownliste mit Schriftarten ](images/cmd-toolbars-image27.png)<br/> In diesem Beispiel werden Dropdownlisten zum Anzeigen und Festlegen von Schriftartattributen verwendet.<br/> Eine Dropdownliste in einer Symbolleiste gibt den Status des aktuell ausgewählten Objekts an (sofern verfügbar). Wenn Sie die Liste ändern, ändert sich der Zustand des ausgewählten Objekts. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="guidelines"></a>Richtlinien

### <a name="presentation"></a>Präsentation

-   **Wählen Sie einen geeigneten Symbolleistenstil basierend auf der Anzahl der Befehle und ihrer Verwendung aus.** Eine Anleitung zur Auswahl finden Sie in der vorherigen Tabelle zum Symbolleistenformat. Vermeiden Sie die Verwendung einer Symbolleistenkonfiguration, die zu viel Speicherplatz im Programmarbeitsbereich benötigt.
-   **Platzieren Sie Symbolleisten direkt über dem Inhaltsbereich unterhalb** der Menüleiste und adressleiste, falls vorhanden.
-   **Wenn der Speicherplatz premium ist, sparen Sie Speicherplatz, indem Sie:**

    -   Weglassen der Bezeichnungen bekannter Symbole und weniger häufig verwendeter Befehle.
    -   Verwenden Sie nur eine partielle Symbolleiste anstelle der gesamten Fensterbreite.
    -   Konsolidieren verwandter Befehle mit einer Menüschaltfläche oder geteilten Schaltfläche.
    -   Verwenden eines [Überlauf-Chevrons,](glossary.md) um weniger häufig verwendete Befehle anzuzeigen.
    -   Befehle werden nur angezeigt, wenn sie für den aktuellen Kontext gelten.

    ![Screenshot der häufigen Symbole der Symbolleiste, die nicht gekennzeichnet sind ](images/cmd-toolbars-image28.png)

    Die Windows Internet Explorer-Symbolleiste spart Platz, indem Bezeichnungen bekannter Symbole weglassen, eine partielle Symbolleiste verwendet wird und ein Überlauf-Chevron für weniger häufig verwendete Befehle verwendet wird.

-   **Verwenden Sie für das Symbolleistenmuster ohne Beschriftung eine Standardkonfiguration mit nicht mehr als zwei Zeilen symbolleisten.** Wenn mehr als zwei Zeilen nützlich sein können, können Sie die Symbolleisten anpassen. Beginnend mit mehr als zwei Zeilen können Benutzer überlastet werden und zu viel Speicherplatz aus dem Programmarbeitsbereich nehmen.

    **Falsch:**

    ![Screenshot der Menüleiste und drei Zeilen mit Symbolleisten ](images/cmd-toolbars-image29.png)

    Eine Standardkonfiguration mit mehr als zwei Zeilen symbolleisten führt zu viel visueller Übersichtlichkeit.

-   **Deaktivieren Sie einzelne Symbolleistenschaltflächen, die nicht für den aktuellen** Kontext gelten, anstatt sie zu entfernen. Dadurch wird der Inhalt der Symbolleiste stabil und leichter zu finden.
-   **Deaktivieren Sie einzelne Symbolleistenschaltflächen, wenn das Klicken darauf direkt zu einem Fehler führen würde.** Dies ist erforderlich, um ein direktes Gefühl zu bewahren.
-   **Entfernen Sie für das Symbolleistenmuster ohne Beschriftung ganze Symbolleisten, wenn sie nicht für den aktuellen Kontext gelten.** Zeigen Sie sie nur in den entsprechenden Modi an.

    ![Screenshot der Debugsymbolleiste ](images/cmd-toolbars-image30.png)

    In diesem Beispiel wird die Symbolleiste Debuggen nur angezeigt, wenn das Programm ausgeführt wird.

-   **Symbolleistenschaltflächen linksbündig anzeigen.** Das Hilfesymbol (falls vorhanden) ist rechtsbündig ausgerichtet.

    ![Screenshot der Symbolleiste, Hilfesymbol rechtsbündig ausgerichtet ](images/cmd-toolbars-image31.png)

    Alle Symbolleistenschaltflächen werden mit Ausnahme der Hilfe linksbündig ausgerichtet.

    **Ausnahme:** Windows symbolleisten im 7-Stil programmspezifische Befehle nach links ausrichten, aber rechts richten Standardbefehle aus, bekannte Befehle wie Optionen, Ansicht und Hilfe.

-   **Ändern Sie die Bezeichnungen der Symbolleistenschaltfläche nicht dynamisch.** Dies ist verwirrend und unerwartet. Sie können das Symbol jedoch ändern, um den aktuellen Zustand widerzubilden.

    ![Screenshot des Bucketsymbols mit Farbe ](images/cmd-toolbars-image26.png)

    In diesem Beispiel wird das Symbol geändert, um den Standardbefehl anzugeben.

### <a name="controls-and-commands"></a>Steuerelemente und Befehle

-   **Bevorzugen Sie die am häufigsten verwendeten Befehle.**
    -   **Stellen Sie für primäre Symbolleisten umfassende Befehle zur Verfügung.** Primäre Symbolleisten müssen nicht so umfassend sein wie Menüleisten, aber sie müssen alle Befehle bereitstellen, die an anderer Stelle nicht leicht erkennbar sind. Primäre Symbolleisten benötigen keine Befehle für:
        -   Befehle, die sich direkt auf der Benutzeroberfläche befinden.
        -   Befehle, auf die in der Regel über Kontextmenüs zugegriffen wird.
        -   Bekannte Standardbefehle wie Ausschneiden, Kopieren und Einfügen.
    -   **Stellen Sie für zusätzliche Symbolleisten Befehle zur Verfügung, die am häufigsten verwendet werden.** Menüleistenbefehle sind eine Obermenge der Symbolleistenbefehle, sodass Sie nicht alles bereitstellen müssen. Konzentrieren Sie sich auf den schnellen, komfortablen Befehlszugriff, und überspringen Sie den Rest.
-   **Direkte Steuerelemente bevorzugen.** Verwenden Sie Symbolleistenschaltflächen in der folgenden Reihenfolge:
    -   **Symbolschaltfläche.** Direkt und benötigt minimalen Speicherplatz.
    -   **Symbolschaltfläche mit Bezeichnung.** Direkt, benötigt aber mehr Platz.
    -   **Schaltfläche "Teilen".** Direkt für den gängigsten Befehl, behandelt jedoch Befehlsvarianten.
    -   **Menüschaltfläche.** Indirekt, stellt aber viele Befehle vor.
-   **Direkte Befehle bevorzugen.** Für Befehle, die entweder direkt sein können oder zusätzliche Eingaben zur Flexibilität haben können:
    -   Verwenden Sie für primäre Symbolleisten die flexiblen Versionen von Befehlen (z.B. Drucken...).
    -   Verwenden Sie für zusätzliche Symbolleisten die unmittelbaren Versionen in der Symbolleiste (z. B. Drucken), und verwenden Sie flexible Versionen in der Menüleiste (z. B. Drucken...).
-   **Stellen Sie Bezeichnungen für häufig verwendete Befehle zur Verfügung,** insbesondere, wenn es sich bei ihren Symbolen nicht um bekannte Symbole handelt.

    **Annehmbar:**

    ![Screenshot der Symbolleiste ohne Beschriftung von Symbolen ](images/cmd-toolbars-image32.png)

    **Besser:**

    ![Screenshot der Symbolleiste mit einigen bezeichneten Symbolen ](images/cmd-toolbars-image33.png)

    Die Windows Fax- und Scansymbolleiste verfügt über wenige Befehle, sodass die bessere Version die wichtigsten bezeichnet.

-   Legen Sie Befehle nicht in Symbolleistenmenüs ab, die sich auch direkt auf der Symbolleiste befinden.

    **Falsch:**

    ![Screenshot des Druckbefehls auf der Symbolleiste und im Menü ](images/cmd-toolbars-image34.png)

    In diesem Beispiel befindet sich Drucken direkt auf der Symbolleiste, sodass es sich nicht im Menü befindet.

### <a name="organization-and-order"></a>Organisation und Reihenfolge

-   **Organisieren Sie die Befehle innerhalb einer Symbolleiste in verknüpfte Gruppen.**
-   **Platzieren Sie die am häufigsten verwendeten Gruppen an erster Stelle. Legen Sie die Befehle innerhalb einer Gruppe in ihrer logischen Reihenfolge ab.** Insgesamt sollten die Befehle über einen logischen Fluss verfügen, damit sie leicht zu finden sind, während weiterhin die am häufigsten verwendeten Befehle zuerst angezeigt werden. Dies ist besonders effizient, wenn ein Überlauf vorliegt.
-   **Verwenden Sie Gruppenteiler nur, wenn die Befehle gruppenübergreifend schwach gekoppelt sind.** Dadurch werden die Gruppierungen offensichtlich und die Befehle leichter zu finden.

    ![Screenshot: Symbolleiste mit gut organisierten Symbolen mithilfe von Gruppenteilern](images/cmd-toolbars-image35.png)

    ![Screenshot der Symbolleiste mit gut organisierten Symbolen ](images/cmd-toolbars-image36.png)

    Beispiele für gruppierte Symbolleisten aus Windows E-Mail.

-   **Vermeiden Sie es, destruktive Befehle neben häufig verwendeten Befehlen zu platzieren.** Verwenden Sie die Reihenfolge oder Gruppierung, um eine Trennung zu erhalten. Erwägen Sie außerdem, keine destruktiven Befehle in der Symbolleiste, sondern nur in der Menüleiste oder in Kontextmenüs zu platzieren.

    **Annehmbar:**

    ![Screenshot benachbarter Schaltflächen zum Drucken und Löschen ](images/cmd-toolbars-image37.png)

    **Besser:**

    ![Screenshot der getrennten Druck- und Löschschaltflächen ](images/cmd-toolbars-image38.png)

    Im besseren Beispiel ist der Delete-Befehl physisch von Print getrennt.

-   **Verwenden Sie das Überlauf-Chevron, um anzugeben, dass nicht alle Befehle angezeigt werden können.** Verwenden Sie den Überlauf jedoch nur, wenn nicht genügend Platz zum Anzeigen aller Befehle vorhanden ist.

    **Falsch:**

    ![Screenshot der Favoritenleiste und ausgeblendeter Befehle ](images/cmd-toolbars-image39.png)

    Das Überlauf-Chevron gibt an, dass nicht alle Befehle angezeigt werden, aber mehr davon mit einem besseren Layout sein könnten.

-   **Stellen Sie sicher, dass auf die am häufigsten verwendeten Befehle in kleinen Fenstergrößen direkt über die Symbolleiste (d. h. nicht überlaufend) zugegriffen werden kann.** Ordnen Sie die Befehle bei Bedarf neu an, verschieben Sie weniger häufig verwendete Befehle in Menüschaltflächen oder geteilte Schaltflächen, oder entfernen Sie sie sogar vollständig von der Symbolleiste. Wenn dies weiterhin ein Problem darstellt, sollten Sie ihre Auswahl des Symbolleistenstils überdenken.

### <a name="hiding-menu-bars"></a>Ausblenden von Menüleisten

Im Allgemeinen funktionieren Symbolleisten hervorragend mit Menüleisten, da sich beide auf ihre Stärken konzentrieren können, ohne kompromittiert zu werden.

-   Blenden Sie die Menüleiste standardmäßig aus, wenn das Symbolleistendesign eine Menüleiste redundant macht.
-   Blenden Sie die Menüleiste aus, anstatt sie vollständig zu entfernen, da Für Tastaturbenutzer besser auf Menüleisten zugegriffen werden kann.
-   Um die Menüleiste wiederherzustellen, geben Sie eine Menüleisten-Häkchenoption in der Menükategorie Ansicht (für primäre Symbolleisten) oder Extras (für sekundäre Symbolleisten) an. Weitere Informationen finden Sie unter [Standardmenü und unterteilte Schaltflächen.](#standard-menu-and-split-buttons)
-   Zeigen Sie die Menüleiste an, wenn Benutzer die ALT-TASTE drücken, und legen Sie den Eingabefokus auf die erste Menükategorie fest.

### <a name="interaction"></a>Interaktion

-   Zeigen Sie beim Zeigen auf die Schaltfläche [affordance](glossary.md) an, um anzugeben, dass auf das Symbol geklickt werden kann. Zeigen Sie nach dem QuickInfo-Timeout die QuickInfo oder infotip an.

    ![Screenshot einer Infotip, die eine Schaltfläche beschreibt ](images/cmd-toolbars-image40.png)

    Dieses Beispiel zeigt die verschiedenen Anzeigezustände.

-   Klicken Sie auf der linken Seite mit einem Einzigen Klick:
    -   Interagieren Sie bei Befehlsschaltflächen wie gewohnt mit dem Steuerelement.
    -   Zeigen Sie für Modusschaltflächen das Steuerelement an, um den derzeit ausgewählten Modus widerzuspiegeln. Wenn sich der Modus auf das Verhalten der Mausinteraktion auswirkt, ändern Sie auch den Zeiger.

        ![Screenshot eines Zeigers, der wie ein Farbbucket dargestellt ist ](images/cmd-toolbars-image41.png)

        In diesem Beispiel wird der Zeiger geändert, um den Mausinteraktionsmodus anzuzeigen.

    -   Zeigen Sie für Eigenschaftenschaltflächen und Dropdownlisten das Steuerelement an, um ggf. den Status der aktuell ausgewählten Objekte widerzuspiegeln. Aktualisieren Sie bei der Interaktion den Zustand des Steuerelements, und wenden Sie die Änderung auf die ausgewählten Objekte an. Wenn nichts ausgewählt ist, tun Sie nichts.

-   Führen Sie bei einem doppelklick auf der linken Seite die gleiche Aktion wie ein linker Einzelklick aus.
    -   **Ausnahme:** In seltenen Fällen kann ein Symbolleistenbefehl modaler verwendet werden. Verwenden Sie in solchen Fällen Doppelklicken, um den Modus umzuschalten.

        ![Screenshot der Infoinfo mit den Funktionen der Schaltfläche ](images/cmd-toolbars-image42.png)

        In diesem Beispiel wird durch Doppelklicken auf den Befehl Format command in einen Modus versetzt, in dem bei allen nachfolgenden Klicks das Format angewendet wird. Benutzer können den Modus verlassen, indem sie mit der linken Maustaste klicken.

-   Klicken Sie mit der rechten Maustaste auf :
    -   Zeigen Sie für anpassbare Symbolleisten das Kontextmenü zum Anpassen der Symbolleiste an. Zeigen Sie das Menü mit der rechten Maustaste nach unten an, nicht mit der Maus nach oben.
    -   Bei anderen Symbolleisten ist nichts zu tun.

### <a name="icons"></a>Symbole

-   **Stellen Sie Symbole für alle Symbolleisten-Steuerelemente außer Dropdownlisten bereit.**

    ![Screenshot der Dropdownliste "Schriftgrad" ](images/cmd-toolbars-image43.png)

    Dropdownlisten benötigen keine Symbole, aber alle anderen Symbolleistensteuerelemente.

    **Ausnahme:** Windows Symbolleisten im 7-Stil verwenden Symbole nur für Befehle, deren Symbole bekannt sind. Andernfalls verwenden sie Textbeschriftungen ohne Symbole. Dies verbessert die Übersichtlichkeit der Bezeichnungen, erfordert jedoch mehr Platz.

-   **Stellen Sie sicher, dass Symbolleistensymbole in der Hintergrundfarbe der Symbolleiste deutlich sichtbar sind.** Werten Sie Symbolleistensymbole immer im Kontext und im Modus mit hohem Kontrast aus.
-   **Wählen Sie Symbolentwürfe aus, die ihren Zweck eindeutig kommunizieren, insbesondere für die am häufigsten verwendeten Befehle.** Gut entworfene Symbolleisten benötigen Symbole, die selbsterklärend sind, da Benutzer Befehle nicht effizient mithilfe ihrer QuickInfos finden können. Symbolleisten funktionieren jedoch weiterhin gut, wenn Symbole für einige weniger häufig verwendete Befehle nicht selbsterklärend sind.
-   **Wählen Sie Symbole aus, die erkennbar und unterscheidbar sind, insbesondere für die am häufigsten verwendeten Befehle.** Stellen Sie sicher, dass die Symbole unterschiedliche Formen und Farben aufweisen. Auf diese Weise können Benutzer die Befehle schnell finden, auch wenn sie sich das Symbol nicht merken.
-   **Stellen Sie sicher, dass Symbolleistensymbole den Richtlinien für Symbole im Stil von Styles entsprechen.**

Weitere Informationen und Beispiele finden Sie unter [Symbole.](vis-icons.md)

### <a name="standard-menu-and-split-buttons"></a>Standardmenü und geteilte Schaltflächen

Wenn Sie Menüschaltflächen und unterteilte Schaltflächen in einer Symbolleiste verwenden, versuchen Sie nach Möglichkeit, die folgenden Standardmenüstrukturen und ihre relevanten Befehle zu verwenden. Im Gegensatz zu Menüleisten verwenden Symbolleistenbefehle keine Zugriffsschlüssel.

**Primäre Symbolleisten**

Diese Befehle spiegeln die Befehle in Standardmenüleisten wider, sodass sie nur für primäre Symbolleisten verwendet werden sollten. Diese Liste zeigt die Schaltflächenbezeichnungen (und den Typ) mit deren Reihenfolge und Trennzeichen, Tastenkombinationen und Ellipsen an. **Beachten Sie, dass sich der Befehl zum Anzeigen und Ausblenden der Menüleiste im Menü Ansicht befindet.**

<dl> Datei <dl> NewCtrl+N  
Öffnen... STRG+O  
Schließen <separator>  
SaveCtrl+S  
Speichern unter... <separator>  
Senden an <separator>  
Drucken... STRG+P  
Seitenansicht  
Seiteneinrichtung <separator>  
ExitAlt+F4 (Verknüpfung in der Regel nicht angegeben)
</dl> </dd> Edit(menu button) <dl> UndoCtrl+Z  
RedoCtrl+Y <separator>  
CutCtrl+X  
CopyCtrl+C  
PasteCtrl+V <separator>  
Wählen Sie allCtrl+A aus. <separator>  
DeleteDel(shortcut normalerweise nicht angegeben)  
Umbenennen... <separator>  
Finden... STRG+F  
Find nextF3 (Befehl in der Regel nicht angegeben)  
Ersetzen... STRG+H  
Gehe zu... STRG+G
</dl> </dd> <dd>Print(split button) <dl> Drucken... STRG+P  
Seitenansicht <separator>  
Seiteneinrichtung
</dl> </dd> Ansicht (Menüschaltfläche) <dl> Menüleiste (Überprüfen, ob sichtbar)  
Detailbereich (Überprüfen, ob sichtbar)  
Vorschaubereich (Überprüfen, ob sichtbar)  
Statusleiste (Überprüfen, ob sichtbar) <separator>  
Zoom  
Zoom inCtrl++  
VerkleinernCtrl+- <separator>  
Textgröße (ausgewählte Einstellung enthält Aufzählungszeichen) <dl> Größte  
Größer  
Medium  
Kleiner  
Kleinste
</dl> </dd> <separator> VollbildF11  
RefreshF5
</dl> </dd> Tools(menu button) <dl> ... <separator>  
Optionen
</dl>> </dd> Help(split button, use the Help icon) <dl> <program name> helpF1 <separator>  
Über <program name>  
</dl> </dd> </dl>

**Zusätzliche Symbolleisten**

Diese Befehle ergänzen Standardmenüleisten. Diese Liste zeigt die Schaltflächenbezeichnungen (und typ) mit ihrer Reihenfolge und Trennzeichen, Tastenkombinationen und Ausellipsen an. **Beachten Sie, dass sich der Befehl zum Anzeigen und Ausblenden der Menüleiste im Menü Extras befindet.**

Die zusätzlichen Kategorienamen der Symbolleiste unterscheiden sich von den Standardmenükategorienamen, da sie umfassender sein müssen. Beispielsweise wird die Kategorie Organisieren anstelle von Bearbeiten verwendet, da sie Befehle enthält, die sich nicht auf die Bearbeitung bezieht. **Um die Konsistenz zwischen Menüleisten und Symbolleisten zu gewährleisten, verwenden Sie die Standardmenükategorienamen, wenn dies nicht irreführend wäre.**

**Falsch:**

![Screenshot der gleichen Optionen für verschiedene Befehle ](images/cmd-toolbars-image44.png)

In diesem Beispiel sollte die Symbolleiste aus Konsistenz-Grund bearbeiten anstelle von Organisieren verwenden, da sie über die Standardbefehle des Menüs Bearbeiten verfügt.

### <a name="palette-windows"></a>Palettenfenster

-   **Palettenfenster verwenden kürzere Titelleisten, um ihren Bildschirmbereich zu minimieren.** Legen Sie auf der Titelleiste die Schaltfläche Schließen ab.
-   **Legen Sie den Text der Titelleiste auf den Befehl fest, der das Palettenfenster angezeigt hat.**
-   **Verwenden Sie die Groß-/Groß-/Formatvorlage, ohne die Interpunktion zu beenden.**
-   **Geben Sie ein Kontextmenü für Fensterverwaltungsbefehle an.** Zeigen Sie dieses Kontextmenü an, wenn Benutzer mit der rechten Maustaste auf die Titelleiste klicken.

    ![Screenshot der Toolbox mit Kontextmenü ](images/cmd-toolbars-image45.png)

    In diesem Beispiel können Benutzer mit der rechten Maustaste auf die Titelleiste klicken, um das Kontextmenü anzuzeigen.

-   **Wenn möglich und nützlich, können Sie die Größe von Palettenfenstern ändern.** Geben Sie an, dass die Größe des Fensters mithilfe von Zeigern zur Größenvergrößerung über dem Fensterrahmen geändert werden kann.
-   **Wenn ein Palettenfenster erneut angezeigt wird, zeigen Sie es mit demselben Zustand wie beim letzten Zugriff an.** Speichern Sie beim Schließen die Fenstergröße und -position. Stellen Sie bei der erneuten Anzeige die Größe und Position des gespeicherten Fensters wieder wieder auf. Erwägen Sie außerdem, diese Attribute pro Benutzer über Programminstanzen hinweg persistent zu machen.

### <a name="customization"></a>Anpassung

-   **Bereitstellen von Anpassungen für Symbolleisten, die aus zwei oder mehr Zeilen bestehen.** Nur das Symbolformat ohne Beschriftung muss angepasst werden. Einfache Symbolleisten mit wenigen Befehlen müssen nicht anpassen werden.
-   **Stellen Sie eine gute Standardkonfiguration zur Verfügung.** Benutzer sollten ihre Symbolleisten nicht für gängige Szenarien anpassen müssen. Verlassen Sie sich nicht darauf, dass Benutzer ihren Weg aus einer fehlerhaften Erstkonfiguration anpassen. Angenommen, die meisten Benutzer passen ihre Symbolleisten nicht an.
-   **Stellen Sie ein Kontextmenü mit den folgenden Befehlen zur Verfügung:**
    -   Eine Kontrollkästchenliste zum Anzeigen der verfügbaren Symbolleisten
    -   Symbolleisten zum Sperren/Entsperren
    -   Anpassen...
-   **Sperren Sie anpassbare Symbolleisten standardmäßig,** um versehentliche Änderungen zu verhindern.
-   **Zeigen Sie für den Befehl Anpassen ein** Dialogfeld mit Optionen an, in dem Sie auswählen können, welche Symbolleisten und welche Befehle auf den einzelnen Symbolleisten angezeigt werden.

    ![Screenshot des Dialogfelds "Anpassen" und der Optionen ](images/cmd-toolbars-image46.png)

    In diesem Beispiel stellt Visual Studio Ein Optionsdialogfeld zum Anpassen der Symbolleisten zur Verfügung.

-   Geben Sie im Dialogfeld Optionen anpassen den Befehl Zurücksetzen an, um zur ursprünglichen Symbolleistenkonfiguration zurückzukehren.
-   **Provide the ability to customize the toolbars using drag-and-drop in the following ways:**

    -   Legen Sie die Reihenfolge und Positionen der Symbolleiste fest.
    -   Legen Sie Symbolleistenlängen fest, und zeigen Sie alle Symbolleisten an, die zu klein sind, um ihren Inhalt mit einem Überlauf-Chevron anzuzeigen.
    -   Falls unterstützt, werden Symbolleisten zu Palettenfenstern und umgekehrt.

    Wenn das Dialogfeld Optionen anpassen angezeigt wird:

    -   Legen Sie den Inhalt der Symbolleiste fest.
    -   Legen Sie die Reihenfolge der Symbolleisteninhalte fest.

    Auf diese Weise können Benutzer Änderungen direkt und effizienter vornehmen.

-   **Speichern Sie alle Symbolleistenanpassungen** pro Benutzer.

### <a name="using-ellipses"></a>Verwenden von Ausellipsen

Während Symbolleistenbefehle für sofortige Aktionen verwendet werden, sind manchmal mehr Informationen erforderlich, um die Aktion auszuführen. Verwenden Sie Auslassungsellipsen, um anzugeben, dass ein Befehl weitere Informationen erfordert, bevor er wirksam werden kann. Legen Sie die Auslassungszeichen am Ende der QuickInfo und der Bezeichnung ab, falls eins verfügbar ist.

![Screenshot des Druckens von QuickInfo-Text mit Auslassungsellipsen ](images/cmd-toolbars-image47.png)

In diesem Beispiel wird die Druck-... -Befehl zeigt ein Dialogfeld Drucken an, um weitere Informationen zu sammeln.

Wenn ein Befehl jedoch nicht sofort wirksam werden kann, sind keine Auslassungsellipsen erforderlich. Freigabeeinstellungen haben also beispielsweise keine Auslassungsellipse, obwohl sie zusätzliche Informationen benötigt, da der Befehl möglicherweise nicht sofort wirksam werden kann.

![Screenshot der Symbolleiste, des Befehls und der QuickInfo ](images/cmd-toolbars-image48.png)

Der Befehl Einstellungen freigaben hat keine Auslassungsellipse, da er nicht sofort wirksam werden kann.

Da Symbolleisten ständig angezeigt werden und der Platz in einem Premium-Bereich liegt, sollten **Ellipsen selten verwendet werden.**

> [!Note]  
> Wenden Sie für Menüs, die auf einer Symbolleiste angezeigt werden, die Richtlinien [für Menüellipsen an.](cmd-menus.md)

 

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstand

![Screenshot von Symbolleisten mit Abstandsinformationen ](images/cmd-toolbars-image49.png)

Empfohlene Größe und Abstand für Standardsymbolleisten.

## <a name="labels"></a>Bezeichnungen

### <a name="general"></a>Allgemein

-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
    -   **Ausnahme:** Bei älteren Anwendungen können Sie bei Bedarf die Groß-/Formatvorlagen verwenden, um das Mischen von Groß-/Formatvorlagen zu vermeiden.

### <a name="unlabeled-icon-buttons"></a>Symbolschaltflächen ohne Beschriftung

-   **Verwenden Sie eine QuickInfo, um den Befehl zu beschriften.** Verwenden Sie für den QuickInfo-Text, wie die Bezeichnung wäre, wenn die Schaltfläche beschriftet wäre, aber schließen Sie die Tastenkombination ein, falls eine beschriftet wäre.

    ![Screenshot der Symbolleiste, des Druckersymbols und der QuickInfo ](images/cmd-toolbars-image50.png)

    Ein Beispiel für eine QuickInfo für symbolschaltfläche.

### <a name="labeled-icon-buttons"></a>Beschriftete Symbolschaltflächen

-   **Verwenden Sie eine präzise Bezeichnung.** Verwenden Sie nach Möglichkeit ein einzelnes Wort, maximal vier Wörter.
-   **Platzieren Sie die Bezeichnung rechts neben dem Symbol.**
-   **Verwenden Sie einen Infotip, um den Befehl zu beschreiben.** Da die Schaltflächen beschriftet sind, wäre die Verwendung einer QuickInfo anstelle einer Infotip redundant.

    ![Screenshot der bezeichneten Schaltfläche mit Infotip ](images/cmd-toolbars-image51.png)

    Ein Beispiel für eine Infotip für eine Schaltfläche mit bezeichnungsbeschrifteter Schaltfläche.

### <a name="drop-down-lists"></a>Dropdownlisten

-   **Wenn die Liste immer über einen Wert verfügt, verwenden Sie den aktuellen Wert als Bezeichnung.**

    ![Screenshot der Symbolleiste mit Schriftartoptionen ](images/cmd-toolbars-image52.png)

    In diesem Beispiel fungiert der aktuell ausgewählte Schriftartname als Bezeichnung.

-   Wenn eine bearbeitbare Dropdownliste keinen Wert hat, verwenden Sie eine [Eingabeaufforderung.](glossary.md)

    ![Screenshot der Adressbücher für die Listenbezeichnungssuche ](images/cmd-toolbars-image53.png)

    In diesem Beispiel wird eine Eingabeaufforderung für die Bezeichnung der Dropdownliste verwendet.

### <a name="menu-buttons-and-split-buttons"></a>Menüschaltflächen und geteilte Schaltflächen

-   **Bevorzugen Sie verbbasierte Menüschaltflächennamen.** Lässt das Verb jedoch weg, wenn es "Create", "Show", "View" oder "Manage" ist. Die **Menüschaltflächen Extras** **und** Seite enthalten beispielsweise keine Verben.
-   **Verwenden Sie ein einzelnes, spezifisches Wort, das den Menüinhalt eindeutig und genau beschreibt.** Obwohl die Namen nicht so allgemein sein müssen, dass sie alles im Menü beschreiben, sollten sie vorhersagbar genug sein, damit Benutzer nicht von dem, was sie im Menü finden, nicht überraschend sind.
-   **Geben Sie zwar keine Infotipbeschreibungen an, wenn sie hilfreich sind.**

### <a name="menu-items"></a>Menüelemente

-   **Verwenden Sie Menüelementnamen, die mit einem Verb, Nomen oder Nomenphrasen beginnen.**
-   **Bevorzugen Sie verbbasierte Menünamen.** Lässt das Verb jedoch weg, wenn es "Create", "Show", "View" oder "Manage" ist. Die folgenden Befehle verwenden beispielsweise keine Verben:
    -   Info
    -   Fortgeschrittene
    -   Vollbildmodus
    -   Neu
    -   Optionen
    -   Eigenschaften
-   **Verwenden Sie bestimmte Verben.** Vermeiden Sie generische, nicht hilfreiche Verben wie Change und Manage.
-   **Verwenden Sie singulare Nomen für Befehle, die für ein einzelnes Objekt gelten, andernfalls** Pluralnunen.
-   **Wählen Sie für Paare von ergänzenden Befehlen eindeutig ergänzende Namen aus.** Beispiele: Hinzufügen, Entfernen; Anzeigen, Ausblenden; Einfügen, Löschen.
-   **Wählen Sie Menüelementnamen basierend auf Benutzerzielen und Aufgaben und nicht nach Technologie aus.**
-   Verwenden Sie die folgenden Menüelementnamen für den angegebenen Zweck:
    -   **Optionen:** So zeigen Sie Programmoptionen an.
    -   **Anpassen:** So zeigen Sie die Programmoptionen an, die sich speziell auf die Konfiguration der maschinellen Benutzeroberfläche bezieht.
    -   **Personalisieren:** So zeigen Sie eine Zusammenfassung der häufig verwendeten [Personalisierungseinstellungen](glossary.md) an.
    -   **Einstellungen:** Verwenden Sie nicht. Verwenden Sie stattdessen Optionen.
    -   **Eigenschaften:** So zeigen Sie das Eigenschaftenfenster eines Objekts an.
    -   **Einstellungen:** Verwenden Sie nicht als Menübezeichnung. Verwenden Sie stattdessen Optionen.
-   **Menüelemente, die Untermenüs anzeigen, haben nie auslassungszeichen auf ihrer Bezeichnung.** Der Untermenüpfeil gibt an, dass eine weitere Auswahl erforderlich ist.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Symbolleisten:

-   Wenn nur eine Symbolleiste verfügbar ist, verweisen Sie darauf als Symbolleiste.
-   Wenn mehrere Symbolleisten verfügbar sind, verweisen Sie auf diese nach Namen, gefolgt von der Wortsymbolleiste. Verwenden Sie die Standardmäßig aktivierte Hauptsymbolleiste, die Schaltflächen für grundlegende Aufgaben wie das Öffnen und Drucken einer Datei als Standardsymbolleiste enthält.
-   Die Symbolleiste ist ein einzelnes, nicht lokalisiertes Wort. (Im Gegensatz dazu besteht die Menüleiste aus zwei Wörtern.)
-   Verweisen Sie auf Symbolleistenschaltflächen über ihre QuickInfo-Bezeichnungen. Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Unterschrift, aber schließen Sie keine Auslassungszeichen ein.
-   Verweisen Sie auf Symbolleistenmenüschaltflächen nach ihren Bezeichnungen und dem Wortmenü. Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Groß-/Groß-/A-
-   Symbolleisten-Steuerelemente werden im Allgemeinen als Symbolleistenschaltflächen bezeichnet.
-   Klicken Sie zum Beschreiben der Benutzerinteraktion für Symbolleistenschaltflächen und schreibgeschützte Dropdownlisten, und geben Sie für bearbeitbare Dropdownlisten ein. Verwenden Sie nicht auswählen, auswählen oder auswählen.
-   Verwenden Sie keine Cascading-, Pull-Down-, Dropdown- oder Popupmenüs, um Menüschaltflächen zu beschreiben, außer in der Programmierdokumentation.
-   Verweisen Sie auf nicht verfügbare Elemente als nicht verfügbar, nicht als abgeblendet, deaktiviert oder abgeblendet. Verwenden Sie deaktiviert in der Programmierdokumentation.
-   Formatieren Sie die Bezeichnungen nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnungen nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiele:

-   Klicken Sie **im Menü** Seite auf der Symbolleiste auf Seite **per E-Mail senden.**
-   Geben Sie **im Feld** Schriftarten auf der Symbolleiste "Segoe UI" ein.
-   Zeigen Sie **auf der Symbolleiste** Formatierung auf **Anzeigen,** und klicken Sie dann auf **Kommentare.**

 

