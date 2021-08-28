---
title: Symbolleisten
description: Symbolleisten sind eine Möglichkeit, Befehle für effizienten Zugriff zu gruppieren.
ms.assetid: 8f36307c-54fc-493d-a2ff-57db29e3508d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 461b9045716ed6cc894a88079e4626107f954a99
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884429"
---
# <a name="toolbars"></a>Symbolleisten

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Symbolleisten sind eine Möglichkeit, Befehle für effizienten Zugriff zu gruppieren.

![Screenshot von zwei Symbolleisten mit beschrifteten Elementen ](images/cmd-toolbars-image1.png)

Einige typische Symbolleisten.

**Verwenden Sie Zusätzlich zu oder anstelle von Menüleisten Symbolleisten.** Symbolleisten können effizienter sein als Menüleisten, da sie direkt sind (immer statt mit dem Mausklick angezeigt werden), direkt (anstatt zusätzliche Eingaben zu erfordern) und die am häufigsten verwendeten Befehle (anstelle einer umfassenden Liste) enthalten. Im Gegensatz zu Menüleisten müssen Symbolleisten nicht umfassend oder selbsterklärend sein, nur schnell, bequem und effizient.

Einige Symbolleisten sind anpassbar, sodass Benutzer Symbolleisten hinzufügen oder entfernen, ihre Größe und Position ändern und sogar ihren Inhalt ändern können. Einige Arten von Symbolleisten können abgedockt werden, was zu einem Palettenfenster führt. Weitere Informationen zu Symbolleistenvarianten finden Sie unter [Verwendungsmuster](#usage-patterns) in diesem Artikel.

> [!Note]  
> Richtlinien im Zusammenhang mit [Menüs,](cmd-menus.md) [Befehlsschaltflächen](ctrl-command-buttons.md)und [Symbolen](vis-icons.md) werden in separaten Artikeln dargestellt.

 

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Ist das Fenster ein primäres Fenster?** Symbolleisten funktionieren gut für primäre Fenster, sind aber in der Regel für sekundäre Fenster überwältigend. Verwenden Sie für sekundäre Fenster stattdessen [Befehlsschaltflächen,](ctrl-command-buttons.md) [Menüschaltflächen](ctrl-command-buttons.md)und [Links.](ctrl-command-links.md)
-   **Gibt es eine kleine Anzahl häufig verwendeter Befehle?** Da Symbolleisten nicht so viele Befehle verarbeiten können wie Menüleisten, funktionieren sie am besten als Möglichkeit, effizient auf eine kleine Anzahl häufig verwendeter Befehle zuzugreifen.
-   **Sind die meisten Befehle sofort?** Das heißt, sind dies größtenteils Befehle, die keine zusätzliche Eingabe erfordern? Um effizient zu sein, müssen Symbolleisten ein direktes und sofortiges Gefühl haben. Andernfalls eignen sich Menüleisten besser für Befehle, die zusätzliche Eingaben erfordern.
-   **Können die meisten Befehle direkt angezeigt werden?** Das heißt, Benutzer interagieren mit ihnen mit einem einzigen Klick? Einige Befehle können zwar mithilfe von Menüschaltflächen dargestellt werden, aber die Darstellung der meisten Befehle auf diese Weise beeinträchtigt die Effizienz der Symbolleiste und macht eine Menüleiste zu einer besseren Wahl.
-   **Werden die Befehle durch Symbole gut dargestellt?** Symbolleistenschaltflächen werden in der Regel durch Symbole anstelle von Textbeschriftungen dargestellt (obwohl einige Symbolleistenschaltflächen beide verwenden), während Menübefehle durch ihren Text dargestellt werden. Wenn die Befehlssymbole nicht von hoher Qualität sind und nicht selbsterklärend sind, ist eine Menüleiste möglicherweise eine bessere Wahl.

Wenn Ihr Programm über eine Symbolleiste ohne Menüleiste verfügt und die meisten Befehle indirekt über Menüschaltflächen und [unterteilte Schaltflächen](ctrl-command-buttons.md)zugänglich sind, ist diese Symbolleiste im Wesentlichen eine Menüleiste. Wenden Sie stattdessen das [Symbolleistenmenümuster](cmd-menus.md) in den Menürichtlinien an.

## <a name="design-concepts"></a>Entwurfskonzepte

Eine gute Menüleiste ist ein umfassender Katalog mit allen verfügbaren Befehlen der obersten Ebene, während eine gute Symbolleiste schnellen, komfortablen Zugriff auf häufig verwendete Befehle bietet. Eine Symbolleiste versucht nicht, Benutzer zu trainieren, um sie einfach produktiv zu machen. Sobald Benutzer erfahren, wie sie auf einen Befehl auf einer Symbolleiste zugreifen, greifen sie nur selten über die Menüleiste auf den Befehl zu. Aus diesen Gründen müssen die Menüleiste und die Symbolleiste eines Programms nicht direkt übereinstimmen.

### <a name="toolbars-vs-menu-bars"></a>Symbolleisten im Vergleich zu Menüleisten

In der Regel unterscheiden sich Symbolleisten wie folgt von Menüleisten:

-   **Frequenz.** Symbolleisten stellen nur die am häufigsten verwendeten Befehle dar, während Menüleisten alle verfügbaren Befehle der obersten Ebene innerhalb eines Programms katalogisieren.
-   **Unmittelbarkeit.** Das Klicken auf einen Symbolleistenbefehl wird sofort wirksam, während ein Menübefehl möglicherweise zusätzliche Eingaben erfordert. Beispielsweise zeigt ein Befehl Drucken in einer Menüleiste zuerst das Dialogfeld Drucken an, während eine Symbolleistenschaltfläche Drucken sofort eine einzelne Kopie eines Dokuments auf dem Standarddrucker druckt.

    ![Screenshot der ausgewählten Druckerschaltfläche der Symbolleiste ](images/cmd-toolbars-image2.png)

    In diesem Beispiel wird durch Klicken auf die Symbolleistenschaltfläche Drucken sofort eine einzelne Kopie eines Dokuments auf dem Standarddrucker gedruckt.

-   **Direktheit.** Symbolleistenbefehle werden mit einem einzigen Klick aufgerufen, während Menüleistenbefehle durch das Menü navigieren müssen.
-   **Anzahl und Dichte.** Der für eine Symbolleiste erforderliche Bildschirmbereich ist proportional zur Anzahl der Befehle, und dieser Speicherplatz wird immer verwendet, auch wenn dies nicht der Der-Befehl ist. Folglich müssen Symbolleisten ihren Platz effizient verwenden. Im Gegensatz dazu werden Menüleistenbefehle normalerweise in der Ansicht ausgeblendet, und ihre hierarchische Struktur ermöglicht eine beliebige Anzahl von Befehlen.
-   **Größe und Darstellung.** Um viele Befehle in einem kleinen Bereich zu packen, verwenden Symbolleisten in der Regel symbolbasierte Befehle (mit QuickInfo-basierten Bezeichnungen), während Menüleisten textbasierte Befehle (mit optionalen Symbolen) verwenden. Symbolleistenschaltflächen können zwar Standardtextbezeichnungen aufweisen, diese verwenden jedoch deutlich mehr Platz.

    ![Screenshot der Symbolleiste mit Sende-/Empfangsbezeichnung ](images/cmd-toolbars-image3.png)

    Beschriftete Symbolleistenschaltflächen nehmen mindestens dreimal so viel Speicherplatz ein wie nicht bezeichnete Schaltflächen.

-   **Selbsterklärend** Gut entworfene Symbolleisten benötigen Symbole, die größtenteils selbsterklärend sind, da Benutzer Befehle nicht effizient mithilfe von QuickInfos finden können. Symbolleisten funktionieren jedoch weiterhin gut, wenn einige weniger häufig verwendete Befehle nicht selbsterklärend sind.

    ![Screenshot der Symbolleiste mit vertrauten Symbolen ](images/cmd-toolbars-image4.png)

    In diesem Beispiel sind die am häufigsten verwendeten Symbole selbsterklärend.

-   **Erkennbar und unterscheidbar.** Bei häufig verwendeten Befehlen merken sich Benutzer Symbolleisten-Schaltflächenattribute wie Position, Form und Farbe. Mit gut entworfenen Symbolleisten können Benutzer die Befehle schnell finden, auch wenn sie sich das genaue Symbol nicht merken. Im Gegensatz dazu merken sich Benutzer häufig verwendete Befehlsspeicherorte in der Menüleiste, verlassen sich jedoch auf die Befehlsbezeichnungen, um Auswahlmöglichkeiten zu treffen.

    ![Screenshot des Dialogfelds "Optionen des Snippingtools" ](images/cmd-toolbars-image5.png)

    Bei Symbolleistenbefehlen können Symbole durch eine unterschiedliche Position, Form und Farbe erkennbar und unterscheidbar werden.

    ![Screenshot der Menüleiste mit ausgewähltem Dateibefehl ](images/cmd-toolbars-image6.png)

    Bei Menüleistenbefehlen sind Benutzer letztendlich von ihren Bezeichnungen abhängig.

### <a name="efficiency"></a>Effizienz

Angesichts ihrer Merkmale müssen Symbolleisten in erster Linie aus Effizienzgründen entworfen werden. Eine ineffiziente Symbolleiste ist einfach nicht sinnvoll.

**Wenn Sie nur eine Sache durchführen...**

Stellen Sie sicher, dass Ihre Symbolleisten in erster Linie auf Effizienz ausgelegt sind. Fokussymbolleisten auf Befehlen, die häufig verwendet werden, sofort, direkt und schnell erkennbar sind.

### <a name="hiding-menu-bars"></a>Ausblenden von Menüleisten

Im Allgemeinen funktionieren Symbolleisten hervorragend mit Menüleisten: Gute Symbolleisten bieten Effizienz und gute Menüleisten bieten Übersichtlichkeit. **Wenn sowohl Menüleisten als auch Symbolleisten vorhanden sind, kann sich jede auf ihre Stärken konzentrieren, ohne kompromittiert zu werden.**

Dieses Modell ist überraschenderweise in einfache Programme zerlegt. Bei Programmen mit nur wenigen Befehlen ist es nicht sinnvoll, sowohl eine Menüleiste als auch eine Symbolleiste zu verwenden, da die Menüleiste eine redundante, ineffiziente Version der Symbolleiste ist.

Um diese Redundanz zu vermeiden, konzentrieren sich viele einfache Programme in Windows Vista darauf, Befehle ausschließlich über die Symbolleiste bereitzustellen und die Menüleiste standardmäßig auszublenden. Zu diesen Programmen gehören Windows Explorer, Windows Internet Explorer, Windows Media Player und Windows Fotogalerie.

Dies ist keine kleine Änderung. Das Entfernen der Menüleiste ändert grundlegend die Art der Symbolleisten, da solche Symbolleisten umfassend sein und sich auf folgende Weise ändern müssen:

-   **Frequenz.** Das Entfernen der Menüleiste bedeutet, dass auf alle Befehle, die nicht direkt über ein Fenster oder die Kontextmenüs verfügbar sind, über die Symbolleiste zugegriffen werden muss, unabhängig von der Häufigkeit der Verwendung.
-   **Unmittelbarkeit.** Wenn Sie die Menüleiste entfernen, ist die Symbolleiste der einzige sichtbare Zugriffspunkt für Befehle, sodass die Symbolleiste über voll funktionsfähige Versionen verfügt. Wenn z. B. keine Menüleiste vorhanden ist, muss ein Befehl Drucken auf einer Symbolleiste das Dialogfeld Drucken anzeigen, anstatt sofort zu drucken. (Obwohl die Verwendung einer unterteilten Schaltfläche in diesem Fall ein hervorragender Kompromiss ist. Informationen zur Standardschaltfläche "Teilen" finden Sie unter [Standardmenü und Unterteilte Schaltflächen.)](#standard-menu-and-split-buttons)

    ![Screenshot der Optionen der Symbolleiste und des Druckbefehls ](images/cmd-toolbars-image7.png)

    In diesem Beispiel verfügt die Symbolleistenschaltfläche Drucken in Windows Fotogalerie über einen Befehl Drucken, der das Dialogfeld Drucken anzeigt.

-   **Direktheit.** Um Platz zu sparen und Unübersichtlich zu vermeiden, können weniger häufig verwendete Befehle in Menüschaltflächen verschoben werden, sodass sie weniger direkt sind.

Symbolleisten, die zur Ergänzung einer Menüleiste verwendet werden, sind anders konzipiert als Symbolleisten, die für die Verwendung mit einer entfernten oder ausgeblendeten Menüleiste entworfen wurden. Und da Sie nicht davon ausgehen können, dass Benutzer eine ausgeblendete Menüleiste anzeigen, um einen einzelnen Befehl auszuführen, sollte das Ausblenden einer Menüleiste genauso behandelt werden wie das vollständige Entfernen, wenn Entwurfsentscheidungen getroffen werden. (Wenn Sie die Menüleiste standardmäßig ausblenden, gehen Sie nicht davon aus, dass Benutzer an die Anzeige der Menüleiste denken, um einen Befehl zu finden, oder sogar herausfinden, wie er angezeigt wird.)

Das Entwerfen einer Symbolleiste für die Arbeit ohne Menüleiste bringt häufig einige Kompromisse mit sich. Um die Effizienz zu erhöhen, sollten Sie jedoch nicht zu viele Kompromisse eingehen. Wenn das Ausblenden der Menüleiste zu einer ineffizienten Symbolleiste führt, blenden Sie die Menüleiste nicht aus!

### <a name="keyboard-accessibility"></a>Barrierefreiheit der Tastaturnavigation

Der Zugriff auf Symbolleisten über die Tastatur ist ein ganz anderer als der Zugriff auf Menüleisten. Menüleisten erhalten den Eingabefokus, wenn Benutzer die ALT-TASTE drücken und sie den Eingabefokus mit der ESC-Taste verlieren. Sobald eine Menüleiste den Eingabefokus besitzt, wird sie unabhängig vom Rest des Fensters navigiert, und alle Pfeiltasten sowie die Tasten Start, Ende und TAB werden verwendet. Im Gegensatz dazu erhalten Symbolleisten den Eingabefokus, wenn Benutzer die TAB-TASTE durch den gesamten Inhalt des Fensters drücken. Da Symbolleisten zuletzt in der Aktiva-Reihenfolge angezeigt werden, kann die Aktivierung auf einer ausgelastet seite erheblich sein (es sei denn, Benutzer wissen, dass sie UMSCHALT+TAB verwenden, um sich rückwärts zu bewegen).

Die Barrierefreiheit ist hier ein Großes: Während Symbolleisten für Mausbenutzer einfacher sind, sind sie für Tastaturbenutzer weniger zugänglich. Dies ist kein Problem, wenn es sowohl eine Menüleiste als auch eine Symbolleiste gibt, aber wenn die Menüleiste entfernt oder ausgeblendet wird.

Aus Gründen der Barrierefreiheit sollten Sie die Menüleiste beibehalten, anstatt sie vollständig zugunsten einer Symbolleiste zu entfernen. Wenn Sie zwischen dem Entfernen der Menüleiste und dem einfachen Ausblenden wählen müssen, sollten Sie sie lieber ausblenden.

## <a name="usage-patterns"></a>Verwendungsmuster

Symbolleisten verfügen über mehrere Verwendungsmuster:



|     Verwendung                                                                                                                 |     Beispiel                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Primäre Symbolleisten**<br/> Eine Symbolleiste, die für die Arbeit ohne Menüleiste konzipiert ist, entweder ausgeblendet oder entfernt. <br/> | Primäre Symbolleisten müssen den Bedarf an Effizienz und Umfassendem ausgleichen, damit sie am besten für einfache Programme funktionieren. <br/> ![Screenshot der Windows-Explorer-Symbolleiste ](images/cmd-toolbars-image8.png)<br/> Eine primäre Symbolleiste aus Windows Explorer.<br/>                                                                        |
| **Zusätzliche Symbolleisten**<br/> Eine Symbolleiste, die für die Arbeit mit einer Menüleiste konzipiert ist. <br/>                         | Zusätzliche Symbolleisten können sich ohne Kompromittierung auf Effizienz konzentrieren. <br/> ![Screenshot einer Menüleiste über einer Symbolleiste ](images/cmd-toolbars-image9.png)<br/> Eine zusätzliche Symbolleiste aus Windows Movie Maker.<br/>                                                                                                                  |
| **Symbolleistenmenüs**<br/> eine Als Symbolleiste implementierte Menüleiste. <br/>                                        | Symbolleistenmenüs sind Symbolleisten, die in erster Linie aus Befehlen [in](ctrl-command-buttons.md) Menüschaltflächen und geteilten Schaltflächen bestehen, mit nur wenigen direkten Befehlen(sofern verfügbar). <br/> ![Screenshot der Menüleiste mit Symbolen und Befehlen ](images/cmd-toolbars-image10.png)<br/> Ein Symbolleistenmenü in Windows Fotogalerie.<br/> |
| **Anpassbare Symbolleisten**<br/> eine Symbolleiste, die von Benutzern angepasst werden kann. <br/>                          | Anpassbare Symbolleisten ermöglichen Es Benutzern, Symbolleisten hinzuzufügen oder zu entfernen, ihre Größe und Position zu ändern und sogar ihre Inhalte zu ändern. <br/> ![Screenshot einer Symbolleiste mit Dutzenden von Symbolen ](images/cmd-toolbars-image11.png)<br/> Eine anpassbare Symbolleiste aus Microsoft Visual Studio.<br/>                                             |
| **Palettenfenster**<br/> ein modusloses Dialogfeld, in dem ein Array von Befehlen angezeigt wird. <br/>                 | Palettenfenster sind ungedoppelte Symbolleisten. <br/> ![Screenshot eines Dialogfelds "Farben" ](images/cmd-toolbars-image12.png)<br/> ![Screenshot eines Schriftartdialogfelds ](images/cmd-toolbars-image13.png)<br/> Palettenfenster aus Windows Paint.<br/>                                                                             |



 

Symbolleisten verfügen über die folgenden Stile:



|   Style                                                                                                                                     | Beispiel                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nicht gekennzeichnete Symbole**<br/> eine oder mehrere Zeilen mit kleinen Symbolschaltflächen ohne Beschriftung. <br/>                                           | verwenden Sie diesen Stil, wenn zu viele Schaltflächen zum Beschriften enthalten sind oder das Programm häufig verwendet wird. Bei diesem Stil können Programme mit komplexer Funktionalität mehrere Zeilen enthalten. Daher ist dies der einzige Stil, der angepasst werden muss. Mit diesem Stil können einige Befehlsschaltflächen beschriftet werden, wenn sie häufig verwendet werden. <br/> ![Screenshot der Symbolleiste mit kleinen, nicht gekennzeichneten Symbolen ](images/cmd-toolbars-image14.png)<br/> Eine Symbolleiste ohne Beschriftung von WordPad.<br/> |
| **Große Symbole ohne Beschriftung**<br/> eine einzelne Zeile mit großen Symbolschaltflächen ohne Beschriftung. <br/>                                         | Verwenden Sie diesen Stil für einfache Hilfsprogramme, die leicht erkennbare Symbole haben und in der Regel in kleinen Fenstern ausgeführt werden. <br/> ![Screenshot der Symbolleiste mit großen Symbolen ohne Beschriftung ](images/cmd-toolbars-image15.png)<br/> ![Screenshot der Symbolleiste mit großen Symbolen ](images/cmd-toolbars-image16.png)<br/> Große Symbolleisten ohne Beschriftung von Windows Live Messenger symbolleisten und Windows Snipping Tool.<br/>                                                                       |
| **Bezeichnete Symbole**<br/> eine einzelne Zeile mit kleinen Symbolen mit Bezeichnungen. <br/>                                                          | verwenden Sie diesen Stil, wenn es nur wenige Befehle gibt oder das Programm nicht häufig verwendet wird. dieses Format hat immer eine einzelne Zeile. <br/> ![Screenshot der Symbolleiste mit bezeichneten Symbolen ](images/cmd-toolbars-image8.png)<br/> Eine Symbolleiste mit Beschriftung aus Windows Explorer.<br/>                                                                                                                                                                                                               |
| **Teilsymbolleisten**<br/> eine teilielle Zeile mit kleinen Symbolen, die verwendet wird, um Speicherplatz zu sparen, wenn keine vollständige Symbolleiste erforderlich ist. <br/>       | Verwenden Sie diesen Stil für Fenster mit Navigationsschaltflächen, einem Suchfeld oder Registerkarten, um unnötige Gewichtung am oberen Fensterrand zu vermeiden. <br/> ![Screenshot von Menüleiste, Symbolleiste und Favoritenleiste ](images/cmd-toolbars-image17.png)<br/> Teilsymbolleisten können mit Navigationsschaltflächen, einem Suchfeld oder Registerkarten kombiniert werden.<br/>                                                                                                                                                  |
| **Große Teilsymbolleisten**<br/> eine Teilzeile großer Symbole, die verwendet wird, um Speicherplatz zu sparen, wenn keine vollständige Symbolleiste erforderlich ist. <br/> | Verwenden Sie diesen Stil für einfache Hilfsprogramme, die über Navigationsschaltflächen oder ein Suchfeld verfügen, um unnötige Gewichtung am oberen Fensterrand zu vermeiden. <br/> ![Screenshot einer großen teiliellen Symbolleiste ](images/cmd-toolbars-image18.png)<br/> Eine große Teilsymbolleiste aus Windows Defender.<br/>                                                                                                                                                                                         |



 

Schließlich haben Symbolleisten-Steuerelemente mehrere Verwendungsmuster:



|     Verwendung                                                                                                                 |     Beispiel                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Schaltflächen des Befehlssymbols**<br/> Durch Klicken auf eine Befehlsschaltfläche wird eine sofortige Aktion initiiert. <br/>                                                                                                 | ![Screenshot einer Symbolleiste mit Beschriftung ](images/cmd-toolbars-image19.png)<br/> Beispiele für Symbolbefehlsschaltflächen aus Windows Fax und Scan.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Schaltflächen des Modussymbols**<br/> Wenn Sie auf eine Modusschaltfläche klicken, wird der ausgewählte Modus aktiviert. <br/>                                                                                                            | ![Screenshot einer vertikalen Symbolleiste ](images/cmd-toolbars-image20.png)<br/> Beispiele für Modusschaltflächen aus Windows Paint.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Schaltflächen des Eigenschaftensymbols**<br/> Der Zustand einer Eigenschaftenschaltfläche spiegelt den Zustand der aktuell ausgewählten Objekte wider( sofern verfügbar). Durch Klicken auf die Schaltfläche wird die Änderung auf die ausgewählten Objekte angewendet. <br/> | ![Screenshot von Formatierungssymbolen und ausgewähltem Text ](images/cmd-toolbars-image21.png)<br/> Beispiele für Eigenschaftenschaltflächen aus Microsoft Word.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Beschriftete Symbolschaltflächen**<br/> eine Befehlsschaltfläche oder Eigenschaftenschaltfläche, die mit einem Symbol und einer Textbezeichnung gekennzeichnet ist. <br/>                                                                               | diese Schaltflächen werden für häufig verwendete Symbolleistenschaltflächen verwendet, deren Symbol nicht ausreichend selbsterklärend ist. Sie werden auch in Symbolleisten verwendet, die so wenige Schaltflächen enthalten, dass jede Schaltfläche eine Textbezeichnung haben kann. <br/> ![Screenshot: Symbolleiste mit Symbolen, die für die am häufigsten verwendeten Schaltflächen bezeichnet sind ](images/cmd-toolbars-image22.png)<br/> Eine Symbolleiste mit den am häufigsten verwendeten Schaltflächen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Menüschaltflächen**<br/> Eine Befehlsschaltfläche, die verwendet wird, um einen kleinen Satz verwandter Befehle anzuzeigen. <br/>                                                                                                | Ein einzelnes nach unten zeigendes Dreieck gibt an, dass durch Klicken auf die Schaltfläche ein Menü angezeigt wird. <br/> ![Screenshot der Symbolleiste und dropdown-Befehlsliste ](images/cmd-toolbars-image23.png)<br/> Eine Menüschaltfläche mit einem kleinen Satz verwandter Befehle.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Unterteilte Schaltflächen**<br/> Eine Befehlsschaltfläche, die verwendet wird, um Variationen eines Befehls zu konsolidieren, insbesondere wenn einer der Befehle meistens verwendet wird. <br/>                                     | ![Screenshot der Schaltfläche zum Teilen des Drucks ](images/cmd-toolbars-image24.png)<br/> eine unterteilte Schaltfläche im normalen Zustand.<br/> Wie bei einer Menüschaltfläche zeigt ein einzelnes nach unten zeigendes Dreieck an, dass beim Klicken auf den rechten Teil der Schaltfläche ein Menü angezeigt wird. <br/> ![Screenshot der Befehle für geteilte Druckschaltflächen ](images/cmd-toolbars-image25.png)<br/> eine gelöschte unterteilte Schaltfläche.<br/> In diesem Beispiel wird eine unterteilte Schaltfläche verwendet, um alle druckbezogenen Befehle zu konsolidieren. Der Befehl "immediate print" wird meistens verwendet, sodass Benutzer normalerweise die anderen Befehle nicht sehen müssen. <br/> Im Gegensatz zu einer Menüschaltfläche führt das Klicken auf den linken Teil der Schaltfläche die Aktion direkt auf der Bezeichnung aus. Unterteilte Schaltflächen sind in Situationen effektiv, in denen der nächste Befehl wahrscheinlich mit dem letzten Befehl identisch ist. In diesem Fall wird die Bezeichnung wie bei einer Farbauswahl in den letzten Befehl geändert:<br/> ![Screenshot des Bucketsymbols mit Farbgebung ](images/cmd-toolbars-image26.png)<br/> In diesem Beispiel wird die Bezeichnung in den letzten Befehl geändert.<br/> |
| **Dropdownlisten**<br/> Eine Dropdownliste (bearbeitbar oder schreibgeschützt), die zum Anzeigen oder Ändern einer Eigenschaft verwendet wird. <br/>                                                                                   | ![Screenshot der Dropdownliste der Schriftarten ](images/cmd-toolbars-image27.png)<br/> In diesem Beispiel werden Dropdownlisten verwendet, um Schriftartattribute anzuzeigen und festzulegen.<br/> Eine Dropdownliste in einer Symbolleiste gibt ggf. den Status des aktuell ausgewählten Objekts wieder. Durch ändern der Liste wird der Zustand des ausgewählten Objekts geändert. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="guidelines"></a>Richtlinien

### <a name="presentation"></a>Präsentation

-   **Wählen Sie basierend auf der Anzahl von Befehlen und deren Verwendung eine geeignete Symbolleistenart aus.** Eine Anleitung zur Auswahl finden Sie in der vorherigen Symbolleisten-Stiltabelle. Vermeiden Sie die Verwendung einer Symbolleistenkonfiguration, die zu viel Platz aus dem Programmarbeitsbereich beansprucht.
-   **Platzieren Sie Symbolleisten direkt über dem Inhaltsbereich unterhalb** der Menüleiste und Adressleiste, sofern vorhanden.
-   **Wenn speicherplatz auf Premium-Ebene liegt, sparen Sie Speicherplatz wie folgt:**

    -   Weglassen der Bezeichnungen bekannter Symbole und weniger häufig verwendeter Befehle.
    -   Verwenden Sie nur eine partielle Symbolleiste anstelle der gesamten Fensterbreite.
    -   Konsolidieren verwandter Befehle mit einer Menüschaltfläche oder einer geteilten Schaltfläche.
    -   Verwenden eines [Überlauf-Chevrons,](glossary.md) um weniger häufig verwendete Befehle aufzudecken.
    -   Anzeigen von Befehlen nur, wenn sie für den aktuellen Kontext gelten.

    ![Screenshot der allgemeinen Symbole der Symbolleiste ohne Bezeichnung ](images/cmd-toolbars-image28.png)

    Die Windows Internet Explorer-Symbolleiste spart Speicherplatz, indem Bezeichnungen bekannter Symbole weggelassen werden, eine partielle Symbolleiste verwendet wird und ein Überlauf-Chevron für weniger häufig verwendete Befehle verwendet wird.

-   **Verwenden Sie für das Symbolleistenmuster ohne Bezeichnung eine Standardkonfiguration mit maximal zwei Symbolleistenzeilen.** Wenn mehr als zwei Zeilen nützlich sein können, machen Sie die Symbolleisten anpassbar. Wenn Sie mit mehr als zwei Zeilen beginnen, können Benutzer überlasten und zu viel Platz aus dem Programmarbeitsbereich nehmen.

    **Falsch:**

    ![Screenshot der Menüleiste und drei Zeilen mit Symbolleisten ](images/cmd-toolbars-image29.png)

    Eine Standardkonfiguration mit mehr als zwei Symbolleistenzeilen führt zu zu viel visueller Überordnung.

-   **Deaktivieren Sie einzelne Symbolleistenschaltflächen, die nicht für den aktuellen Kontext gelten,** anstatt sie zu entfernen. Dadurch wird der Inhalt der Symbolleiste stabil und leichter zu finden.
-   **Deaktivieren Sie einzelne Symbolleistenschaltflächen, wenn ein Klick direkt zu einem Fehler führen würde.** Dies ist erforderlich, um ein direktes Gefühl zu erhalten.
-   **Entfernen Sie für das Symbolleistenmuster ohne Bezeichnung ganze Symbolleisten, wenn sie nicht für den aktuellen Kontext gelten.** Zeigen Sie sie nur in den entsprechenden Modi an.

    ![Screenshot der Debugsymbolleiste ](images/cmd-toolbars-image30.png)

    In diesem Beispiel wird die Debugsymbolleiste nur angezeigt, wenn das Programm ausgeführt wird.

-   **Symbolleistenschaltflächen linksbündig anzeigen.** Das Hilfesymbol ist rechtsbündig ausgerichtet.

    ![Screenshot der Symbolleiste, Hilfesymbol rechtsbündig ausgerichtet ](images/cmd-toolbars-image31.png)

    Alle Symbolleistenschaltflächen werden mit Ausnahme der Hilfe linksbündig ausgerichtet.

    **Ausnahme:** Windows Symbolleisten im 7-Stil richten programmspezifische Befehle links aus, aber rechts ausgerichtete, bekannte Standardbefehle wie Optionen, Ansicht und Hilfe.

-   **Ändern Sie symbolleisten-Schaltflächenbezeichnungen nicht dynamisch.** Dies ist verwirrend und unerwartet. Sie können das Symbol jedoch ändern, um den aktuellen Zustand widerzuspiegeln.

    ![Screenshot des Bucketsymbols mit Farbgebung ](images/cmd-toolbars-image26.png)

    In diesem Beispiel wird das Symbol geändert, um den Standardbefehl anzugeben.

### <a name="controls-and-commands"></a>Steuerelemente und Befehle

-   **Bevorzugen Sie die am häufigsten verwendeten Befehle.**
    -   **Stellen Sie für primäre Symbolleisten umfassende Befehle bereit.** Primäre Symbolleisten müssen nicht so umfassend sein wie Menüleisten, aber sie müssen alle Befehle bereitstellen, die an anderer Stelle nicht leicht erkennbar sind. Primäre Symbolleisten müssen keine Befehle für:
        -   Befehle, die sich direkt auf der Benutzeroberfläche selbst befinden.
        -   Auf Befehle wird in der Regel über Kontextmenüs zugegriffen.
        -   Bekannte Standardbefehle wie Ausschneiden, Kopieren und Einfügen.
    -   **Stellen Sie für zusätzliche Symbolleisten Befehle bereit, die am häufigsten verwendet werden.** Menüleistenbefehle sind eine Obermenge der Symbolleistenbefehle, sodass Sie nicht alles bereitstellen müssen. Konzentrieren Sie sich auf den schnellen, komfortablen Befehlszugriff, und überspringen Sie den Rest.
-   **Direkte Steuerelemente bevorzugen.** Verwenden Sie Symbolleistenschaltflächen in der folgenden Reihenfolge:
    -   **Symbolschaltfläche.** Direkt und nimmt minimalen Speicherplatz in Anspruch.
    -   **Beschriftete Symbolschaltfläche.** Direkt, nimmt aber mehr Speicherplatz in Anspruch.
    -   **Schaltfläche "Teilen".** Direkt für den gängigsten Befehl, verarbeitet aber Befehlsvariationen.
    -   **Menüschaltfläche.** Indirekt, stellt aber viele Befehle dar.
-   **Sofortige Befehle bevorzugen.** Für Befehle, die entweder direkt sein können oder zusätzliche Eingaben zur Flexibilität haben können:
    -   Verwenden Sie für primäre Symbolleisten die flexiblen Versionen von Befehlen (z. B. Drucken...).
    -   Verwenden Sie für zusätzliche Symbolleisten die unmittelbaren Versionen in der Symbolleiste (z. B. Drucken) und flexible Versionen in der Menüleiste (z. B. Drucken...).
-   **Stellen Sie Bezeichnungen für häufig verwendete Befehle bereit,** insbesondere, wenn ihre Symbole keine bekannten Symbole sind.

    **Annehmbar:**

    ![Screenshot der Symbolleiste ohne Beschriftung von Symbolen ](images/cmd-toolbars-image32.png)

    **Besser:**

    ![Screenshot der Symbolleiste mit einigen symbolbeschrifteten Symbolen ](images/cmd-toolbars-image33.png)

    Die Symbolleiste Windows Fax und Scan enthält nur wenige Befehle, sodass die besseren Versionsbezeichnungen die wichtigsten sind.

-   Legen Sie Befehle nicht in Symbolleistenmenüs ab, die sich auch direkt auf der Symbolleiste befinden.

    **Falsch:**

    ![Screenshot des Druckbefehls auf der Symbolleiste und im Menü ](images/cmd-toolbars-image34.png)

    In diesem Beispiel befindet sich Drucken direkt auf der Symbolleiste, sodass es sich nicht im Menü befinden muss.

### <a name="organization-and-order"></a>Organisation und Bestellung

-   **Organisieren Sie die Befehle in einer Symbolleiste in verknüpften Gruppen.**
-   **Platzieren Sie zuerst die am häufigsten verwendeten Gruppen. Legen Sie innerhalb einer Gruppe die Befehle in ihrer logischen Reihenfolge ab.** Insgesamt sollten die Befehle über einen logischen Flow verfügen, damit sie leicht zu finden sind, während immer noch die am häufigsten verwendeten Befehle zuerst angezeigt werden. Dies ist besonders effizient, wenn ein Überlauf vorliegt.
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
Schließen  
&lt;Trennzeichen&gt;  
SaveCtrl+S  
Speichern unter...  
&lt;Trennzeichen&gt;  
Senden an  
&lt;Trennzeichen&gt;  
Drucken... STRG+P  
Seitenansicht  
Seiteneinrichtung  
&lt;Trennzeichen&gt;  
ExitAlt+F4 (Verknüpfung in der Regel nicht angegeben)
</dl> </dd> Edit(menu button) <dl> UndoCtrl+Z  
RedoCtrl+Y  
&lt;Trennzeichen&gt;  
CutCtrl+X  
CopyCtrl+C  
PasteCtrl+V  
&lt;Trennzeichen&gt;  
Wählen Sie allCtrl+A aus.  
&lt;Trennzeichen&gt;  
DeleteDel(shortcut normalerweise nicht angegeben)  
Umbenennen...  
&lt;Trennzeichen&gt;  
Finden... STRG+F  
Find nextF3 (Befehl in der Regel nicht angegeben)  
Ersetzen... STRG+H  
Gehe zu... STRG+G
</dl> </dd> <dd>Print(split button) <dl> Drucken... STRG+P  
Seitenansicht  
&lt;Trennzeichen&gt;  
Seiteneinrichtung
</dl> </dd> Ansicht (Menüschaltfläche) <dl> Menüleiste (überprüfen, ob sichtbar)  
Detailbereich (überprüfen, ob sichtbar)  
Vorschaubereich (überprüfen, ob sichtbar)  
Statusleiste (überprüfen, ob sichtbar)  
&lt;Trennzeichen&gt;  
Zoom  
VergrößernCtrl++  
VerkleinernCtrl+-  
&lt;Trennzeichen&gt;  
Textgröße (ausgewählte Einstellung hat Aufzählungszeichen) <dl> Größte  
Größer  
Medium  
Kleiner  
Kleinste
</dl> </dd> &lt;separator&gt;  
Full screenF11  
RefreshF5  
</dl> </dd> Tools(menu button) <dl> ...  
&lt;Trennzeichen&gt;  
Optionen
</dl>> </dd> Help(split button, use the Help icon) <dl> <program name> helpF1  
&lt;Trennzeichen&gt;  
Über <program name>  
</dl> </dd> </dl>

**Zusätzliche Symbolleisten**

Diese Befehle ergänzen Standardmenüleisten. Diese Liste zeigt die Schaltflächenbezeichnungen (und den Typ) mit deren Reihenfolge und Trennzeichen, Tastenkombinationen und Ellipsen an. **Beachten Sie, dass sich der Befehl zum Anzeigen und Ausblenden der Menüleiste im Menü Extras befindet.**

Die zusätzlichen Symbolleistenkategorienamen unterscheiden sich von den Standardmenükategorienamen, da sie umfassender sein müssen. Beispielsweise wird die Kategorie Organisieren anstelle von Bearbeiten verwendet, da sie Befehle enthält, die sich nicht auf die Bearbeitung beziehen. **Um die Konsistenz zwischen Menüleisten und Symbolleisten zu gewährleisten, verwenden Sie die Standardnamen der Menükategorie, wenn dies nicht irreführend wäre.**

**Falsch:**

![Screenshot der gleichen Optionen für verschiedene Befehle ](images/cmd-toolbars-image44.png)

In diesem Beispiel sollte die Symbolleiste aus Konsistenzgründen Bearbeiten anstelle von Organisieren verwenden, da sie über die Standardbefehle im Menü Bearbeiten verfügt.

### <a name="palette-windows"></a>Palettenfenster

-   **Palettenfenster verwenden kürzere Titelleisten, um den Bildschirmbereich zu minimieren.** Klicken Sie auf der Titelleiste auf die Schaltfläche Schließen.
-   **Legen Sie den Titelleistentext auf den Befehl fest, der das Palettenfenster angezeigt hat.**
-   **Verwenden Sie die Groß-/Großschreibung im Satzformat, ohne die Interpunktion zu beenden.**
-   **Geben Sie ein Kontextmenü für Fensterverwaltungsbefehle an.** Dieses Kontextmenü wird angezeigt, wenn Benutzer mit der rechten Maustaste auf die Titelleiste klicken.

    ![Screenshot der Toolbox mit Kontextmenü ](images/cmd-toolbars-image45.png)

    In diesem Beispiel können Benutzer mit der rechten Maustaste auf die Titelleiste klicken, um das Kontextmenü anzuzeigen.

-   **Machen Sie die Größenänderung von Palettenfenstern nach Möglichkeit und nützlich.** Geben Sie an, dass die Größe des Fensters mithilfe von Größenänderungszeigern über dem Fensterrahmen geändert werden kann.
-   **Wenn ein Palettenfenster erneut angezeigt wird, zeigen Sie es im gleichen Zustand an wie beim letzten Zugriff.** Speichern Sie beim Schließen die Fenstergröße und den Speicherort. Stellen Sie beim erneuten Anzeigen die gespeicherte Fenstergröße und den Speicherort wieder her. Erwägen Sie außerdem, diese Attribute pro Benutzer über Programminstanzen hinweg persistent zu machen.

### <a name="customization"></a>Anpassung

-   **Stellen Sie Anpassungen für Symbolleisten bereit, die aus mindestens zwei Zeilen bestehen.** Nur der Stil mit nicht bezeichneten Symbolen muss angepasst werden. Einfache Symbolleisten mit wenigen Befehlen müssen nicht angepasst werden.
-   **Stellen Sie eine gute Standardkonfiguration bereit.** Benutzer sollten ihre Symbolleisten nicht für gängige Szenarien anpassen müssen. Verlassen Sie sich nicht darauf, dass Benutzer ihren Weg aus einer fehlerhaften Anfangskonfiguration anpassen. Angenommen, die meisten Benutzer passen ihre Symbolleisten nicht an.
-   **Geben Sie ein Kontextmenü mit den folgenden Befehlen an:**
    -   Eine Kontrollkästchenliste zum Anzeigen der verfügbaren Symbolleisten
    -   Symbolleisten zum Sperren/Entsperren
    -   Anpassen...
-   **Sperren Sie anpassbare Symbolleisten standardmäßig,** um versehentliche Änderungen zu verhindern.
-   **Zeigen Sie für den Befehl Anpassen ein Optionsdialogfeld an,** in dem Sie auswählen können, welche Symbolleisten angezeigt werden und welche Befehle auf jeder Symbolleiste angezeigt werden.

    ![Screenshot des Dialogfelds "Anpassen" und der Optionen ](images/cmd-toolbars-image46.png)

    In diesem Beispiel stellt Visual Studio ein Optionsdialogfeld zum Anpassen der Symbolleisten bereit.

-   Geben Sie einen Reset-Befehl an, um zur ursprünglichen Symbolleistenkonfiguration im Dialogfeld Optionen anpassen zurückzukehren.
-   **Provide the ability to customize the toolbars using drag-and-drop in the following ways:**

    -   Legen Sie die Reihenfolge und Positionen der Symbolleiste fest.
    -   Legen Sie Symbolleistenlängen fest, und zeigen Sie alle Symbolleisten an, die zu klein sind, um ihren Inhalt mit einem Überlauf-Chevron anzuzeigen.
    -   Wenn dies unterstützt wird, können Sie Symbolleisten abdocken, um Palettenfenster zu werden und umgekehrt.

    Wenn das Dialogfeld Optionen anpassen angezeigt wird:

    -   Legen Sie den Inhalt der Symbolleiste fest.
    -   Legen Sie die Reihenfolge des Symbolleisteninhalts fest.

    Auf diese Weise können Benutzer Änderungen direkt und effizienter vornehmen.

-   **Speichern Sie alle Anpassungen** der Symbolleiste pro Benutzer.

### <a name="using-ellipses"></a>Verwenden von Ellipsen

Während Symbolleistenbefehle für sofortige Aktionen verwendet werden, sind manchmal weitere Informationen erforderlich, um die Aktion auszuführen. Verwenden Sie eine Auslassungszeichen, um anzugeben, dass ein Befehl weitere Informationen erfordert, bevor er wirksam werden kann. Setzen Sie die Auslassungszeichen am Ende der QuickInfo und der Bezeichnung, sofern vorhanden.

![Screenshot des QuickInfo-Drucktexts mit Auslassungszeichen ](images/cmd-toolbars-image47.png)

In diesem Beispiel wird der Druck... -Befehl zeigt ein Dialogfeld Drucken an, um weitere Informationen zu sammeln.

Wenn ein Befehl jedoch nicht sofort wirksam werden kann, sind keine Auslassungszeichen erforderlich. Freigabeeinstellungen haben also beispielsweise keine Auslassungszeichen, obwohl sie zusätzliche Informationen benötigen, da der Befehl möglicherweise nicht sofort wirksam wird.

![Screenshot der Symbolleiste, des Befehls und der QuickInfo ](images/cmd-toolbars-image48.png)

Der Befehl Freigabe Einstellungen hat keine Auslassungszeichen, da er nicht sofort wirksam werden kann.

Da Symbolleisten ständig angezeigt werden und der Speicherplatz premium ist, **sollten Ellipsen selten verwendet werden.**

> [!Note]  
> Wenden Sie für Menüs, die auf einer Symbolleiste angezeigt werden, die Richtlinien für [die Menüausellipse](cmd-menus.md)an.

 

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größen- und Abstände

![Screenshot von Symbolleisten mit Abstandsinformationen ](images/cmd-toolbars-image49.png)

Empfohlene Größen- und Abstandstaste für Standardsymbolleisten.

## <a name="labels"></a>Bezeichnungen

### <a name="general"></a>Allgemein

-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
    -   **Ausnahme:** Bei älteren Anwendungen können Sie bei Bedarf die Groß-/Formatvorlagen verwenden, um das Mischen von Groß-/Formatvorlagen zu vermeiden.

### <a name="unlabeled-icon-buttons"></a>Symbolschaltflächen ohne Beschriftung

-   **Verwenden Sie eine QuickInfo, um den Befehl zu beschriften.** Verwenden Sie für den QuickInfo-Text, wie die Bezeichnung wäre, wenn die Schaltfläche beschriftet wäre, aber schließen Sie die Tastenkombination ein, falls eine beschriftet wäre.

    ![Screenshot der Symbolleiste, des Druckersymbols und der QuickInfo ](images/cmd-toolbars-image50.png)

    Ein Beispiel für eine QuickInfo für eine Symbolschaltfläche.

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
-   **Menüelemente, die Untermenüs anzeigen, haben nie Auslassungspunkte auf ihrer Bezeichnung.** Der Untermenüpfeil gibt an, dass eine weitere Auswahl erforderlich ist.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Symbolleisten:

-   Wenn nur eine Symbolleiste verfügbar ist, verweisen Sie darauf als Symbolleiste.
-   Wenn mehrere Symbolleisten verfügbar sind, verweisen Sie auf diese nach Namen, gefolgt von der Wortsymbolleiste. Verwenden Sie die Standardmäßig aktivierte Hauptsymbolleiste, die Schaltflächen für grundlegende Aufgaben wie das Öffnen und Drucken einer Datei als Standardsymbolleiste enthält.
-   Die Symbolleiste ist ein einzelnes, nicht lokalisiertes Wort. (Im Gegensatz dazu besteht die Menüleiste aus zwei Wörtern.)
-   Verweisen Sie auf Symbolleistenschaltflächen über ihre QuickInfo-Bezeichnungen. Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Unterschrift, aber schließen Sie keine Auslassungszeichen ein.
-   Verweisen Sie auf Symbolleistenmenüschaltflächen nach ihren Bezeichnungen und dem Wortmenü. Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Groß-/Groß-/A-
-   Symbolleisten-Steuerelemente werden im Allgemeinen als Symbolleistenschaltflächen bezeichnet.
-   Um die Benutzerinteraktion zu beschreiben, klicken Sie auf symbolleistenschaltflächen und schreibgeschützte Dropdownlisten, und geben Sie für bearbeitbare Dropdownlisten ein. Verwenden Sie nicht auswählen, auswählen oder auswählen.
-   Verwenden Sie keine Cascading-, Pull-Down-, Dropdown- oder Popupmenüs, um Menüschaltflächen zu beschreiben, außer in der Programmierdokumentation.
-   Verweisen Sie auf nicht verfügbare Elemente als nicht verfügbar, nicht als abgeblendet, deaktiviert oder grau. Verwenden Sie deaktiviert in der Programmierdokumentation.
-   Formatieren Sie die Bezeichnungen nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnungen nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiele:

-   Klicken Sie **im Menü** Seite auf der Symbolleiste auf Seite **per E-Mail senden.**
-   Geben Sie **im Feld** Schriftarten auf der Symbolleiste "Segoe UI" ein.
-   Zeigen Sie **auf der Symbolleiste** Formatierung auf **Anzeigen,** und klicken Sie dann auf **Kommentare.**

 

