---
title: Quick Infos und infotips
description: Eine QuickInfo ist ein kleines Popup Fenster, das das nicht beschriftete Steuerelement bezeichnet, auf das verwiesen wird, z. b. nicht gekennzeichnete Symbolleisten-Steuerelemente oder Befehlszeilen.
ms.assetid: 80979281-eefb-485a-b42f-7f9e05665357
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ddccf694b51bf8357dd779bd70146bebf4f14345
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103869372"
---
# <a name="tooltips-and-infotips"></a>Quick Infos und infotips

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Eine QuickInfo ist ein kleines Popup Fenster, das das nicht beschriftete Steuerelement bezeichnet, auf das verwiesen wird, z. b. nicht gekennzeichnete Symbolleisten-Steuerelemente oder Befehlszeilen.

![Screenshot, der die Schaltfläche "Drucken" mit der angezeigten QuickInfo "Print (STRG + P)" anzeigt.](images/ctrl-tooltips-and-infotips-image1.png)

Eine typische QuickInfo für eine Symbolleisten-Schaltfläche.

Da Quick Infos sich als nützlich erwiesen haben, ist ein zugehöriges Steuerelement mit dem Namen "Infotipps" vorhanden, das aussagekräftigeren Text bietet, als mit Quick Infos möglich ist.

Ein Infotipp ist ein kleines Popup Fenster, in dem das Objekt, auf das verwiesen wird, kurz beschrieben wird, z. b. Beschreibungen von Symbolleisten-Steuerelementen, Symbolen, Grafiken, Links, Windows-Explorer-Objekte, Startmenü Elemente und Task leisten Schaltflächen. Infotips sind eine Form von [progressives Offenlegung](ctrl-progressive-disclosure-controls.md)von Steuerelementen, sodass Sie nicht immer beschreibenden Text auf dem Bildschirm haben müssen.

![Screenshot der Freigabe Schaltfläche mit Infotipp ](images/ctrl-tooltips-and-infotips-image2.png)

Ein typischer infotip.

Für den Zweck dieses Artikels werden Quick Infos und Infotipps zusammen als Tipps bezeichnet.

Tipps helfen Benutzern dabei, unbekannte oder unbekannte Objekte zu verstehen, die nicht direkt in der Benutzeroberfläche beschrieben werden. Sie werden automatisch angezeigt, wenn Benutzer den Mauszeiger über ein Objekt bewegen und entfernt werden, wenn Benutzer auf das Steuerelement klicken oder die Maus bewegen, oder wenn die Spitze ein Timeout hat.

**Entwickler:** Es ist kein Infotipp-Steuerelement vorhanden. Infotipps werden mit dem QuickInfo-Steuerelement implementiert. Die Unterscheidung erfolgt in Verwendung und nicht in der Implementierung.

> [!Note]  
> Richtlinien, die sich auf [Luftballons](ctrl-balloons.md), [Symbolleisten](cmd-toolbars.md)und [Hilfe](winenv-help.md) beziehen, werden in separaten Artikeln dargestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Werden die angezeigten Informationen auf der Grundlage des Mauszeigers angezeigt?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Anzeigen von Tipps nur dann, wenn das Ergebnis der Benutzerinteraktion Sie niemals alleine anzeigt. Im Gegensatz dazu können [Luftballons](ctrl-balloons.md) eigenständig (wie bei Benachrichtigungen) angezeigt werden, sodass Sie über ein Fragment verfügen, das Ihre Quelle identifiziert.
-   **Ist das Steuerelement mit Text beschriftet?** Wenn dies nicht der Fall ist, fügen Sie die Beschriftung als QuickInfo hinzu. Beachten Sie, dass die meisten Steuerelemente beschriftet werden und daher keine Quick Infos aufweisen sollten. Symbolleisten-Steuerelemente und Befehls Schaltflächen mit Grafik Bezeichnungen sollten Quick Infos enthalten.
-   **Profitiert ein Objekt von einer ergänzenden Beschreibung oder weiteren Informationen?** Wenn dies der Fall ist, verwenden Sie einen infotip. Der Text muss jedoch ergänzend sein, was für die primären Aufgaben nicht erforderlich ist. Fügen Sie wichtige Informationen direkt in die Benutzeroberfläche ein, damit Benutzer nicht erst danach suchen müssen.
-   **Handelt es sich bei den ergänzenden Informationen um einen Fehler, eine Warnung oder einen Status?** Wenn dies der Fall ist, verwenden Sie ein anderes UI-Element, z. b. eine Sprechblase, eine [Fehlermeldung](mess-error.md)oder eine [Status](ctrl-status-bars.md) Infotipps für Benachrichtigungsbereich sind eine Ausnahme, da Sie zum Anzeigen von Statusinformationen verwendet werden können.
-   **Müssen die Benutzer mit den Informationen interagieren?** Wenn dies der Fall ist, verwenden Sie ein anderes Steuerelement, beispielsweise eine Sprechblase Eine Benutzerinteraktion mit QuickInfo ist nicht möglich, da die Informationen beim Bewegen der Maus ausgeblendet werden.
-   **Müssen Benutzer die ergänzenden Informationen drucken?** Verwenden Sie in diesem Fall ein anderes Steuerelement, z. b. ein statisches Kommentarfeld. Sie können jedoch auch Infotipps verwenden, um den direkten Zugriff auf diese Informationen zu ermöglichen.

    ![Screenshot der Kommentar Sprechblase ](images/ctrl-tooltips-and-infotips-image3.png)

    In diesem Beispiel ermöglicht ein statisches Kommentarfeld in Microsoft Word Benutzern, Kommentare zu drucken.

-   **Ist der Kontext so, dass Benutzer möglicherweise die Tipps lästig oder ablenkend finden?** Wenn dies der Fall ist, sollten Sie die Verwendung einer anderen Lösung in Erwägung gezogen. Wenn Sie in solchen Kontexten Tipps verwenden, gestatten Sie es Benutzern, diese zu deaktivieren.

Bei entsprechender Verwendung verbessern Tipps die Kommunikation mit dem Benutzer. **Verwenden Sie niemals Tipps als Ersatz für einen guten Entwurf.** Wenn eine Grafik, Schaltfläche oder ein anderes Objekt erfordert, dass die Benutzer einen Tipp behalten, um dies zu verstehen, ist der Entwurf schlecht. Korrigieren Sie stattdessen den Entwurf.

## <a name="design-concepts"></a>Entwurfskonzepte

Tipps sind eine leistungsstarke Möglichkeit, eine Benutzeroberfläche zu vereinfachen. Sie stellen Informationen bereit, die Benutzer benötigen, wenn Sie Sie benötigen, mit minimalem Aufwand. Tipps können Ihnen helfen, den Bildschirmbereich effektiver zu verwenden und die Bildschirm Übersichtlichkeit zu verringern. Allerdings können schlecht gestaltete Tipps lästig, ablenkend, nicht hilfreich, überwältigend oder im Weg sein. Die folgenden Entwurfskonzepte sollen den Unterschied zeigen.

### <a name="discoverability"></a>Erkennbarkeit

Tipps werden automatisch angezeigt, wenn Benutzer den Mauszeiger über ein Objekt über einen bestimmten Zeitraum bewegen. Dieser Zeit Verzögerungs Mechanismus macht Tipps sehr praktisch, aber auch die Auffindbarkeit wird reduziert.

Im Laufe der Zeit lernen Benutzer, dass bestimmte Standardobjekte wie Symbolleisten Schaltflächen, Grafik Schaltflächen, Startmenü Elemente und Benachrichtigungs Bereichs Symbole über Tipps verfügen, sodass Sie Ihre Auffindbarkeit für den gewährten nutzen können.

Es dauert länger, bis Benutzer Tipps an nicht standardmäßigen Orten finden. Es gibt keinen visuellen Hinweis, z. b. einen Hotspot oder eine Zeiger Änderung, der angibt, dass ein Objekt über einen Tipp verfügt. Noch schlimmer ist, dass einige Benutzer den Mauszeiger herum bewegen, vor allem, wenn Sie lernen, die Benutzeroberfläche zu navigieren. Benutzer müssen wissen, dass ein Objekt einen Trinkgeld hat, entweder in der Vergangenheit oder durch experimentieren.

Sie können die Auffindbarkeit durch konsistente Verwendung von Tipps verbessern, was wiederum die Vorhersagbarkeit fördert. Wenn Sie Tipps für einige Objekte bereitstellen, sollten Sie diese für alle ähnlichen Objekte bereitstellen, für die Benutzer wahrscheinlich zusätzliche Informationen benötigen. Manchmal kann es eine Herausforderung darstellen, da Sie außerdem sicherstellen müssen, dass die Tipps hilfreich und nicht offensichtlich sind.

Wenn die Bereitstellung erkennbarer, konsistent hilfreicher Tipps ein Problem darstellt, sollten Sie alternative Entwürfe wie z. b. selbsterklärende Steuerelement Bezeichnungen oder direkten ergänzenden Text in Erwägung gezogen.

### <a name="appropriate-information"></a>Entsprechende Informationen

Die für Tipps geeigneten Informationen haben die folgenden Eigenschaften:

-   **Knapp.** Die von Tipps verwendeten Popup Fenster eignen sich perfekt für kurze Sätze und Satzfragmente sowie für formatierten Text. Große, unformatierte Textblöcke sind schwer zu lesen und zu überwältigend.
-   **Bereiten.** Tipp Text muss informativ sein. Es sollte nicht offensichtlich sein oder einfach wiederholen, was sich bereits auf dem Bildschirm befindet.
-   **Zusätzliche.** Da Tip-Text nicht immer sichtbar ist, sollten zusätzliche Informationen vorliegen, die Benutzer nicht lesen müssen. Wichtige Informationen sollten mithilfe von selbsterklärenden Steuerelement Bezeichnungen oder direkten ergänzenden Text kommuniziert werden.
-   **Kum.** Benutzer erwarten nicht, dass Tipps von einer Instanz in die nächste geändert werden, sodass Sie wahrscheinlich keine Änderungen an dynamischen Inhalten bemerken, wie z. b. Statusinformationen. Benachrichtigungsbereich-Symbol Tipps stellen eine wichtige Ausnahme dar: Benutzer sind wahrscheinlicher, dass Sie Änderungen an Tip-Informationen finden, da diese Symbole hauptsächlich den Status übermitteln.

### <a name="appropriate-timeouts"></a>Entsprechende Timeouts

Die entsprechende automatische Anzeige und Löschung von Tipps ist entscheidend für das Ziel der Benutzer, die die Kontrolle über die Benutzeroberflächen Umgebung behalten. Tipps haben drei Timeout Werte:

-   **Anfangs.** Der Zeitpunkt, zu dem der Zeiger stationär bleiben muss, damit der Tipp angezeigt wird. Die Standardzeit beträgt 0,5 Sekunden.
-   **Neu anzeigen.** Die Zeit, während der der Zeiger stationär bleiben muss, wenn der Zeiger von einem Ziel zu einem anderen verschoben wird. Die Standardzeit beträgt 0,1 Sekunden.
-   **Umbau.** Die Zeit, nach der der Tipp automatisch entfernt wird. Die Standardzeit beträgt 5 Sekunden.

Eine zu kurze Anfangs-und reshow-Werte führt zu einer lästigen, Unterbrechung, da Sie oft versehentlich angezeigt werden, wohingegen zu lange die Tipps nicht reaktionsfähig sind oder nicht gefunden werden. Die Standard Entfernungs Zeit eignet sich gut für Kurztext, wie Sie in Quick Infos verwendet werden. Infotips haben längeren Text, sodass Sie längere Anzeige Zeiten benötigen.

### <a name="appropriate-placement"></a>Geeignete Platzierung

Wenn möglich, sollten Sie sich in der Nähe des Objekts befinden, das mit dem Mauszeiger verknüpft ist. Sie sollten jedoch nie auf eine Weise platziert werden, die die Vorgänge des Benutzers beeinträchtigt, indem das relevante Objekt verdeckt wird. Um dieses Problem zu vermeiden, müssen Sie möglicherweise den Tipp vom Zeiger entfernen, aber neben dem Objekt. Dies stellt kein Problem dar, solange die Beziehung zwischen dem Objekt und dem Tip eindeutig ist. Stellen Sie sicher, dass Benutzer den Zeiger nicht verschieben, um die Tipps Ihres Programms zu entfernen.

### <a name="accessibility"></a>Eingabehilfen

Tipps haben eine ungewöhnliche Auswirkung auf die Barrierefreiheit. Obwohl Sie normalerweise durch zeigen des Zeigers auf ein Objekt ausgelöst werden, werden Tipps von [Bildschirmlesern](inter-accessibility.md) für Steuerelemente mit Tastatur Zugriff behandelt. Bei der passenden Verwendung für präzise, hilfreiche, statische, ergänzende Informationen können Tipps die allgemeine Barrierefreiheit verbessern. Tatsächlich ist das alt-texttip-Muster die bevorzugte Methode, um Grafiken zugänglich zu machen. Wenn Sie jedoch nicht ordnungsgemäß verwendet werden, wird die Barrierefreiheit beeinträchtigt, da wichtige oder dynamische Informationen schwerer zu erreichen sind.

Geben Sie mehr als eine Möglichkeit für den Zugriff auf ein Steuerelement an, wenn dieses Steuerelement einen Tipp erfordert, der keinen Tastatur Zugriff hat.

![Screenshot der Schaltfläche "Drucken" mit QuickInfo ](images/ctrl-tooltips-and-infotips-image4.png)

In diesem Beispiel können Benutzer mithilfe der Symbolleisten Schaltfläche (auf die keine Tastatur zugänglich ist) oder über die Tastenkombination "Druckbefehl" Drucken.

**Wenn Sie nur eine Aktion ausführen...**

Entwerfen Sie ermittelbare Tipps, die präzise, hilfreiche, statische, ergänzende Informationen an geeigneter Stelle zum richtigen Zeitpunkt anzeigen.

## <a name="usage-patterns"></a>Verwendungsmuster

Tipps haben mehrere Verwendungs Muster:



|                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **QuickInfos**<br/> zeigt die Bezeichnung eines Steuer Elements oder Symbols ohne Bezeichnung an. <br/>                                         | Da diese Tipps als Bezeichnungen fungieren, folgt ihr Text den Beschriftungs Richtlinien für das zugrunde liegende Steuerelement. <br/> ![Screenshot der Schaltfläche "Liste exportieren" mit QuickInfo ](images/ctrl-tooltips-and-infotips-image5.png)<br/> in diesem Beispiel gibt die QuickInfo die Befehls Bezeichnung an.<br/> ![Screenshot der Schaltfläche "Schließen" mit QuickInfo ](images/ctrl-tooltips-and-infotips-image6.png)![Screenshot der Wiedergabe Schaltfläche mit QuickInfo ](images/ctrl-tooltips-and-infotips-image7.png)<br/> in diesen Beispielen bezeichnen die QuickInfo-Grafik Schaltflächen.<br/> ![Screenshot des Menüs "Menü anzeigen" mit QuickInfo ](images/ctrl-tooltips-and-infotips-image8.png)<br/> In diesem Beispiel bezeichnet die QuickInfo ein Symbol.<br/> |
| **Infotipps**<br/> Bereitstellen einer ergänzenden Beschreibung oder Erläuterung eines Objekts oder Steuer Elements. <br/>                  | Verwenden Sie Infotipps zum beschreiben oder erläutern von Objekten und Steuerelementen, z. b. [Symbol](cmd-toolbars.md) leisten-Steuerelemente, [Symbolen](vis-icons.md) (einschließlich Symbol Überlagerungen), [Verknüpfungen](ctrl-links.md), [Registerkarten](ctrl-tabs.md), [Progressive Offenlegung](ctrl-progressive-disclosure-controls.md)von Steuerelementen <br/> ![Screenshot der Schaltfläche "e-Mail" mit Infotipp ](images/ctrl-tooltips-and-infotips-image9.png)<br/> ![Screenshot der Verbrauchs Schaltfläche mit Infotipp ](images/ctrl-tooltips-and-infotips-image10.png)<br/> In diesen Beispielen bieten Infotipps ergänzende Informationen zu Steuerelementen und Objekten.<br/>                                                                                        |
| **Info Tipps für alt-Text**<br/> Beschreibt eine Grafik für Barrierefreiheit. <br/>                                              | Dieses Muster richtet sich hauptsächlich an Benutzer, die über eine Form der Sehbehinderung verfügen und möglicherweise eine Sprachausgabe verwenden. <br/> ![Screenshot der Windows-Schaltfläche "Start" mit Infotipp ](images/ctrl-tooltips-and-infotips-image11.png)<br/> In diesem Beispiel wird in der Infotipp-Grafik die Start Menü Grafik beschrieben.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Miniaturansicht**<br/> Anzeigen eines kleinen Bilds eines Elements. <br/>                                                         | Miniaturansichten verfügen über eine leicht erkennbare grafische Darstellung eines Fensters oder Dokuments. <br/> ![Screenshot der System Steuerungs Kategorien-Miniaturansicht ](images/ctrl-tooltips-and-infotips-image12.png)<br/> in diesem Beispiel gibt die Windows-Taskleiste Miniatur Ansichts Tipps für ihre Elemente an.<br/> ![Screenshot der Miniaturansicht des Fotos und der zugehörigen Daten ](images/ctrl-tooltips-and-infotips-image13.png)<br/> In diesem Beispiel gibt die Windows-Fotogalerie Tipps für die Miniaturansicht an.<br/>                                                                                                                                                                                                                      |
| **Infotipps für Details**<br/> zeigen Sie ausführliche Informationen zu einem Objekt an. <br/>                                        | Infotips sind eine effektive Möglichkeit, um ausführliche Informationen zu einem Objekt anzuzeigen oder um Daten bereitzustellen. <br/> ![Screenshot des Fotos Infotipp mit Dateityp ](images/ctrl-tooltips-and-infotips-image14.png)![Screenshot des Diagramms mit Infotipp mit Detail Werten ](images/ctrl-tooltips-and-infotips-image15.png)<br/> In diesen Beispielen erhalten Sie mit Infotipps ausführliche Informationen zu einem Objekt oder zu Daten.<br/>                                                                                                                                                                                                                                                                                                      |
| **Info Tipps für Startmenü**<br/> beschreiben Sie ein Element im Startmenü. <br/>                                              | Das Startmenü umfasst Programmnamen und wichtige Windows-Ziele, z. b. Dokumente, Bilder und die Systemsteuerung. Diese Tipps beschreiben Start Menü Elemente, in der Regel durch die Angabe einer kurzen Beschreibung des Programms oder des Ziels sowie der primären Aufgaben, die Benutzer damit ausführen können. Diese Beschreibungen werden auch über das Suchfeld Startmenü indiziert, um Benutzern das Auffinden der benötigten Programme zu erleichtern. <br/> ![Screenshot des Willkommens Center-Infotipps ](images/ctrl-tooltips-and-infotips-image16.png)<br/> In diesem Beispiel wird im Infotipp beschrieben, welche Aktionen Benutzer mit einem Programm im Startmenü ausführen können.<br/>                                                                                    |
| **Info Tipps für die Systemsteuerung**<br/> Beschreibt eine System Steuerungs Kategorie oder einen Task. <br/>                                    | Diese Tipps bieten zusätzliche Informationen, die Benutzern helfen, die richtige Kategorie und das Element der Systemsteuerung auszuwählen. <br/> ![Screenshot der Kategorie "Benutzerkonten" mit Infotipp ](images/ctrl-tooltips-and-infotips-image17.png)<br/> In diesem Beispiel beschreibt der Infotipp die Kategorie Benutzerkonten-Systemsteuerung.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| **Infotipps mit vollständigem Namen**<br/> zeigt den vollständigen Namen eines Elements an, wenn der Name abgeschnitten oder nicht vollständig sichtbar ist. <br/> | Diese Tipps ermöglichen es Ihnen, Elemente in einem kompakteren Bereich anzuzeigen und gleichzeitig den Bedarf an horizontaler Bildlauf zu verringern. Dies ist besonders wichtig, wenn die Inhalts Länge unbekannt ist, weil Sie dynamisch ist. anders als bei den anderen Mustern werden diese Tipps, wenn Sie in Listen und Strukturen verwendet werden, direkt über das Quell Objekt angezeigt. <br/> ![Screenshot der Optionsfeld Gruppe-Titel Infotipp ](images/ctrl-tooltips-and-infotips-image18.png)<br/> In diesem Beispiel wird ein Infotipp verwendet, um den vollständigen Elementnamen bei Hover anzuzeigen.<br/>                                                                                                                                                                                     |
| **Info Tipps für Status**<br/> zeigt Statusinformationen für Benachrichtigungs Bereichs Symbole an. <br/>                              | Normalerweise sollten die Tipps statisch sein, da Benutzer nicht erwarten, dass Sie von einer Instanz in die nächste geändert werden. **Benachrichtigungs Bereichs Symbole stellen eine Ausnahme** dar, da diese Symbole den Status übermitteln und kein anderer Bildschirmbereich für den Status Text verfügbar ist. <br/> ![Screenshot von "Messenger nicht signiert" Infotipp ](images/ctrl-tooltips-and-infotips-image19.png)<br/> ![Screenshot des InfoTipps "Messenger signiert" ](images/ctrl-tooltips-and-infotips-image20.png)<br/> In diesen Beispielen erhalten Infotipps Statusinformationen für Benachrichtigungs Bereichs Symbole.<br/>                                                                                                                                  |



 

## <a name="guidelines"></a>Richtlinien

### <a name="timeouts"></a>Timeouts

-   **Verwenden Sie die Standardeinstellung anfängliche, und zeigen Sie Zeitpunkte neu an. Distanzieren**
    -   Miniaturansichten, die nicht redundant und auf der Seite Ihres zugeordneten Objekts angezeigt werden, können sofort (ohne Verzögerung) angezeigt werden. Verwenden Sie jedoch das standardmäßige anfängliche Timeout für redundante Miniaturansichten (z. b. einen großen Miniatur Ansichts Tipp für ein kleines Grafik Objekt) oder Miniaturansichten, die das zugehörige Objekt abdecken.
-   **Verwenden Sie für Quick Infos das Standard Timeout für die trinkentfernungs Entfernung von fünf Sekunden.**
-   **Deaktivieren Sie für Infotipps das Entfernungs Entfernungs Timeout. Entwickler:** da Sie das Entfernungs Timeout technisch nicht deaktivieren können, legen Sie es auf seinen größten Wert fest.
-   Wenn Sie für Barrierefreiheit die Timeout Werte auf einen anderen Wert als den maximalen Wert festlegen müssen, machen Sie Sie zu einem Vielfachen der SPI \_ -Parameter getmousehovertime und SPI \_ getmessageduration, anstatt festgelegte Zeiten zu verwenden. Dadurch werden die Timeouts an die Geschwindigkeit des Benutzers angepasst.

### <a name="placement"></a>Platzierung

-   **Vermeiden Sie das abdecken des Objekts, mit dem der Benutzer die Anzeige oder Interaktion durchläuft.** Platzieren Sie den Tipp immer auf der Seite des Objekts, auch wenn dies eine Trennung zwischen dem Zeiger und dem Tipp erfordert. Einige Trennungen sind kein Problem, solange die Beziehung zwischen dem Objekt und dem Tip eindeutig ist.

    -   **Ausnahme:** Quick Infos für vollständige Namen, die in Listen und Strukturen verwendet werden.

    **Falsch:**

    ![Screenshot des Infotipp-verdeckt-Suchfelds ](images/ctrl-tooltips-and-infotips-image21.png)

    **Richtig:**

    ![Screenshot des Infotipp, der unterhalb des Suchfelds abgelegt ist ](images/ctrl-tooltips-and-infotips-image22.png)

    Im richtigen Beispiel wird der Infotipp aus dem Suchfeld entfernt, auch wenn dieser Platz zwischen ihm und der Einfügemarke erfordert.

    **Falsch:**

    ![Screenshot des Infotipp, der überarbeiteten Text verdeckt ](images/ctrl-tooltips-and-infotips-image23.png)

    **Richtig:**

    ![Screenshot des Infotipp, der oberhalb von überarbeitetem Text abgelegt wurde ](images/ctrl-tooltips-and-infotips-image24.png)

    Im richtigen Beispiel ist der zugrunde liegende Text sehr viel nützlicher als der Tipp, sodass der Infotipp nicht in den Weg versetzt wird.

-   **Vermeiden Sie für Auflistungen von Elementen, dass das nächste Objekt abgedeckt wird, mit dem der Benutzer wahrscheinlich die Anzeige oder Interaktion durchläuft.** Vermeiden Sie für horizontal angeordnete Elemente das Platzieren von Tipps auf der rechten Seite. vermeiden Sie bei vertikal angeordneten Elementen das Platzieren von Tipps unten.

    **Falsch:**

    ![Screenshot der Infotipp-Liste der zuletzt verwendeten Elemente ](images/ctrl-tooltips-and-infotips-image25.png)

    **Richtig:**

    ![Screenshot des Infotipp neben der Liste der zuletzt verwendeten Elemente ](images/ctrl-tooltips-and-infotips-image26.png)

    Im falschen Beispiel deckt der Tipp das Objekt ab, mit dem der Benutzer am ehesten mit der nächsten Interaktion interagiert.

-   **Um potenzielle (häufig große) Tipps zu erhalten, stellen Sie sicher, dass die Informationen für die meisten Benutzer hilfreich sind.** Wenn dies nicht der Fall ist, machen Sie die ablenktiontipps optional, oder entfernen Sie Sie. Andernfalls müssen die meisten Benutzer den Zeiger vom Zielobjekt entfernen, um den Tipp zu entfernen.

### <a name="tooltips"></a>QuickInfos

-   **Verwenden Sie Quick Infos, um Bezeichnungen für nicht beschriftete Steuerelemente bereitzustellen.** Steuerelemente, die häufig Quick Infos aufweisen, sind [Symbol](cmd-toolbars.md)leisten Schaltflächen, Grafik Schaltflächen und [Progressive Offenlegung](ctrl-progressive-disclosure-controls.md) Steuerelemente mit Eingabe Aufforderungen werden als bezeichnet, z. b. [Textfelder](ctrl-text-boxes.md) und Kombinations [Felder](/windows/desktop/uxguide/ctrl-drop). Alle anderen Steuerelemente sollten explizite Bezeichnungen aufweisen.
-   Verwenden Sie Satzfragmente ohne endinterpunktions Zeichen.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
    -   **Ausnahme:** Diese Richtlinie ist neu in Windows Vista. Bei älteren Anwendungen können Sie ggf. die Groß-/Kleinschreibung von Titeln verwenden, um das Mischen von Groß-/Kleinschreibung
-   Fügen Sie ein [Ellipsen](ctrl-command-buttons.md) hinzu, wenn die Bezeichnung für einen Befehl vorgesehen ist, der zusätzliche Informationen benötigt.
-   **Lassen** Sie Quick Infos wie normale Bezeichnungen in der Regel mit fünf Wörtern oder weniger, aber bevorzugen Sie bestimmte Bezeichnungen über vage Bezeichnungen.

    **Annehmbar:**

    ![Screenshot der QuickInfo ](images/ctrl-tooltips-and-infotips-image27.png)

    **Besserer**

    ![Screenshot der QuickInfo zum Drucken auf dem Standarddrucker ](images/ctrl-tooltips-and-infotips-image28.png)

    **Best**

    ![Screenshot der QuickInfo "Print (Document Writer)" ](images/ctrl-tooltips-and-infotips-image29.png)

    **Falsch:**

    ![Screenshot der ausführlichen QuickInfo ](images/ctrl-tooltips-and-infotips-image30.png)

    In diesen Beispielen ist das beste Beispiel sowohl kurz als auch spezifisch, während das falsche Beispiel unnötig ausführlich ist.

-   **Quick Infos können auch ausführlichere Informationen für Symbolleisten Schaltflächen enthalten, wenn dies hilfreich ist.** Wiederholen Sie nicht nur den Vorgang, oder geben Sie eine verfassen-Anweisung zurück, die bereits in der Bezeichnung ist.

    **Richtig:**

    ![Screenshot der QuickInfo "alle Outlook suchen" ](images/ctrl-tooltips-and-infotips-image31.png)

    In diesem Beispiel wird in der QuickInfo erläutert, was die Suche bewirkt.

    **Falsch:**

    ![Screenshot der QuickInfo-Schaltflächen Bezeichnung ](images/ctrl-tooltips-and-infotips-image32.png)

    In diesem Beispiel wiederholt die QuickInfo nur, was bereits in der Bezeichnung vorhanden ist.

-   **Sie müssen keine Quick Infos für beschriftete Steuerelemente, sondern nur aus Gründen der Konsistenz erhalten.**

    ![Screenshot der Schaltflächen mit beschrifteten und unbeschrifteten ](images/ctrl-tooltips-and-infotips-image33.png)

    In diesem Beispiel verfügen die nicht beschrifteten Symbolleisten Schaltflächen über Quick Infos, die beschrifteten aber nicht.

-   Vereinfachen Sie Quick Infos, wenn Sie **die Tastenkombinationen und Standardwerte bereitstellen.** Fügen Sie diese zusätzlichen Informationen in Klammern ein. Dadurch können Quick Infos für beschriftete Steuerelemente hilfreich sein, auch wenn Sie die Bezeichnung andernfalls einfach wiederholen. Beachten Sie diesen zusätzlichen Text nicht, wenn Sie die Genauigkeit einer QuickInfo auswerten.

    ![Screenshot der QuickInfo "Print (Document Writer)" ](images/ctrl-tooltips-and-infotips-image29.png)

    In diesem Beispiel zeigt Word die Standardwerte und Tastenkombinationen in den Quick Infos der Symbolleiste an.

### <a name="infotips"></a>Infotipps

-   **Für Infotipps an nicht standardmäßigen Orten sollten Sie die Konsistenz gegenüber heltadness bevorzugen, um die Auffindbarkeit zu verbessern.** Geben Sie Tipps für alle Objekte an, für die Benutzer wahrscheinlich zusätzliche Informationen benötigen, auch wenn einige Infotipps offensichtlich sind. Dadurch wird vermieden, dass Benutzer auf einen InfoTipp warten, der nie erscheint.
    -   **Ausnahme:** Wenn nur einige wenige Objekte hilfreiche Infotipps haben, verwenden Sie keine InfoTipps. Verwenden Sie stattdessen selbsterklärende Steuerelement Bezeichnungen oder direkten zusätzlichen Text.
-   Verwenden Sie vollständige Sätze mit endinterpunktions Zeichen.
    -   **Ausnahme:** Benachrichtigungs Bereichs [Symbol Infotipps](winenv-notification.md) verwenden keine endpunktierungen.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Verwenden Sie die aktuelle und nicht die Zukunft.
-   Verwenden paralleler Grammatiken. Parallelität erfordert, dass Wörter und Ausdrücke, die dieselbe Funktion aufweisen, dieselbe Form aufweisen.
    -   **Ausnahme:** Beim Infotipp-Muster Full Name entspricht der Infotipp-Text exakt dem Ausdruck, der Groß-und Kleinschreibung und der Interpunktions Zeichen des zugrunde liegenden Steuer Elements.
-   **Vermeiden Sie große InfoTipps.** Große Infotipps sind schwer zu lesen und schwer zu positionieren, ohne das zugrunde liegende Objekt zu beeinträchtigen.
-   **Formatieren Sie Infotipps, damit Ihre Inhalte leichter lesbar und zu scannen sind.** Große Blöcke von unformatiertem Text können schwer zu lesen sein.

    **Falsch:**

    ![Screenshot der langen, unstrukturierten, QuickInfo ](images/ctrl-tooltips-and-infotips-image34.png)

    **Richtig:**

    ![Screenshot der gleichen QuickInfo mit einer Zeile pro Element ](images/ctrl-tooltips-and-infotips-image35.png)

    Im richtigen Beispiel ist der formatierte Text viel leichter zu lesen und zu scannen.

-   Benennen Sie bei der ersten Verwendung innerhalb eines infotip die Namen von Akronymen, gefolgt vom Akronym in Klammern. Beispiel: "Dynamic Host Configuration-Protokoll (DHCP)".

### <a name="start-menu-infotips"></a>Info Tipps für Startmenü

-   Verwenden Sie das Startmenü-Infotipps, um **das Element kurz zu beschreiben und die Hauptaufgaben aufzulisten, die Benutzer mit dem Element ausführen können.**
-   **Es ist hilfreich.** Konzentrieren Sie sich darauf, was Benutzer tun können. Wiederholen Sie einfach den Elementnamen, oder verwenden Sie ihn überhaupt nicht in der Beschreibung.
-   **Sie sollten spezifisch sein.** Vermeiden Sie generische Verben und Catch-All-Ausdrücke wie und andere Tasks. Wenn die Informationen wichtig sind, können Sie Sie explizit auflisten. nehmen Sie andernfalls an, dass die Benutzer wissen, dass nicht alles in den infotips aufgeführt ist.
-   **Seien Sie präzise.** Verwenden Sie 25 Wörter oder weniger. Längere Info Tipps verhindern das lesen.
-   **Beginnen Sie mit einem aktuellen, imperativen Verb,** wie z. b. erstellen, bearbeiten, anzeigen und senden. Bevorzugen spezifischer Verben gegenüber generischen Verben wie z. b. Manage und Open, die für die meisten Startmenü Elemente gelten. Gelangen Sie direkt zu dem Punkt.

    **Falsch:**

    ![Screenshot der QuickInfo: öffnet den Ordner "Musik" ](images/ctrl-tooltips-and-infotips-image36.png)

    **Besserer**

    ![Screenshot der QuickInfo: Speichern und Wiedergeben von Musik ](images/ctrl-tooltips-and-infotips-image37.png)

    Im falschen Beispiel beginnt der Infotipp mit einem generischen Verb. Das bessere Beispiel geht direkt bis zu dem Punkt mit bestimmten Verben, verwendet jedoch weiterhin die unnötige "und andere" Formulierung am Ende des Tipps.

-   **Verwenden Sie keine Programmiersprache, die wie Marketing aussieht.**

    **Falsch:**

    ![Bildschirm Abbildung von "One-Break Start Point" Infotipp ](images/ctrl-tooltips-and-infotips-image38.png)

    In diesem Beispiel klingt der Infotipp wie Marketing.

-   Da diese Infotipps für das Suchfeld Startmenü indiziert sind, **beschreiben Sie die wichtigen Aufgaben Ihres Programms mithilfe der Bedingungen, für die Benutzer am wahrscheinlichsten suchen. Verwenden Sie Schlüsselwörter und allgemeine Synonyme.**

    **Falsch:**

    ![Screenshot der QuickInfo: Erstellen von DVDs ](images/ctrl-tooltips-and-infotips-image39.png)

    **Richtig:**

    ![Screenshot der QuickInfo: Create (Burn) CDs, DVDs ](images/ctrl-tooltips-and-infotips-image40.png)

    Im richtigen Beispiel hat der Infotipp allgemeine Synonyme.

-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   **Entwickler:** Der Infotipp-Text des Startmenüs stammt aus dem Kommentarfeld des Elements.

### <a name="quick-launch-tooltips"></a>Quick Start-Quick Infos

-   **Verwenden Sie eine QuickInfo mit dem folgenden Format:** Starten (vollständiger Programmname)
-   Verwenden Sie keine Interpunktion am Ende.
-   Verwenden Sie keinen zusätzlichen Text, um das Programm zu beschreiben, oder was es tut. Da Benutzer die Programme auswählen, die in der Schnellstartleiste angezeigt werden, wissen Sie bereits ihren Zweck.

### <a name="control-panel-infotips"></a>Info Tipps für die Systemsteuerung

-   Verwenden Sie die Info Tipps der Systemsteuerung, um **die System Steuerungsaufgaben und die konfigurierte Hardware und Software kurz zu beschreiben.**
-   **Die Namen und Symbole der Systemsteuerung müssen infotips enthalten.** Einzelne Aufgaben haben keine Quick Infos.
-   **Es ist hilfreich.** Konzentrieren Sie sich darauf, was Benutzer tun können. Wiederholen Sie nicht einfach den Elementnamen der Systemsteuerung, oder verwenden Sie ihn überhaupt nicht in der Beschreibung.
-   **Sie sollten spezifisch sein.** Vermeiden Sie generische Verben und Catch-All-Ausdrücke wie und andere Hardware. Wenn die Informationen wichtig sind, können Sie Sie explizit auflisten. nehmen Sie andernfalls an, dass die Benutzer wissen, dass nicht alles in den infotips aufgeführt ist.

    **Falsch:**

    ![Screenshot der QuickInfo: konfiguriert die Maus ](images/ctrl-tooltips-and-infotips-image41.png)

    **Richtig:**

    ![Screenshot der detaillierten QuickInfo für die Mauseinstellungen ](images/ctrl-tooltips-and-infotips-image42.png)

    Im richtigen Beispiel werden die Typen der konfigurierten Hardware speziell aufgelistet.

-   **Seien Sie präzise.** Verwenden Sie 25 Wörter oder weniger. Längere Info Tipps verhindern das lesen.
-   **Beginnen Sie mit einem aktuellen, imperativen Verb.**

    **Richtig:**

    Konfigurieren Sie die Internet Anzeige und die Verbindungseinstellungen.

    Passen Sie die Einstellungen für maschinelles sehen, hören und Mobilität an.

-   **Gelangen Sie direkt zu dem Punkt.** Verwenden Sie die Sprache, die für die Systemsteuerung gilt, nicht, z. b. "verwenden Sie, um Einstellungen für die Darstellung und Funktionalität von..." anzuzeigen und zu konfigurieren. oder "bietet Optionen für Sie..."
-   Verwenden Sie keine Programmiersprache, die wie Marketing aussieht.

    **Falsch:**

    Ihr einziger Ausgangspunkt für alle Anforderungen an die Datenträger Konfiguration.

-   Da diese Infotipps für das Suchfeld der Systemsteuerung indiziert sind, **beschreiben Sie Elemente mit Bedingungen, für die Benutzer am wahrscheinlichsten suchen.** Verwenden Sie gängige Synonyme für beliebte Tasks und Objekte.

    ![Screenshot der QuickInfo mit Game-Controller-Aufgaben ](images/ctrl-tooltips-and-infotips-image43.png)

    In diesem Beispiel wird das Element mithilfe von Begriffen beschrieben, für die Benutzer am wahrscheinlichsten suchen.

-   Wenn ein System Steuerungselement mit anderen möglicherweise verwirrt ist, erläutern Sie, wie es sich im infotip unterscheidet.

    **Falsch:**

    ![Screenshot von Infotipp mit fehlenden Details ](images/ctrl-tooltips-and-infotips-image44.png)

    In diesem Beispiel konfigurieren beide System Steuerungselemente einen Sound, aber der Unterschied wird nicht durch den Infotipp verdeutlicht.

    **Richtig:**

    ![Screenshot des Infotipp mit bestimmten Details ](images/ctrl-tooltips-and-infotips-image45.png)

    In diesem Beispiel ist der Unterschied zwischen den beiden Elementen aufgrund des Tipps deutlicher zu erkennen.

### <a name="icons"></a>Symbole

Im Gegensatz zu früheren Versionen von Windows ermöglicht Windows Vista Tipps, Symbole zu haben.

-   Verwenden Sie für Quick Infos keine Symbole.
-   Verwenden Sie für infotips nur Symbole, wenn Sie die Erkennung oder das Verständnis unterstützen, oder stellen Sie Kontext bereit. Die meisten Infotipps sollten keine Symbole aufweisen.

    ![Screenshot des volumeinfotipps mit dem Haupt Telefonsymbol ](images/ctrl-tooltips-and-infotips-image46.png)

    In diesem Beispiel enthält der Infotipp ein Symbol, mit dem das Symbol seiner Bedeutung zugeordnet werden kann.

-   Das Symbol muss den [Aero-Stil](vis-icons.md) verwenden und eine unaufdringliche Darstellung aufweisen.

Allgemeine Symbol Richtlinien und Beispiele finden Sie unter [Symbole](vis-icons.md).

## <a name="documentation"></a>Dokumentation

Wenn Sie auf Tipps verweisen:

-   Informationen zur Programmierung und anderen technischen Dokumentationen finden Sie unter Tip (QuickInfo oder infotip). An allen anderen Stellen Sie einfach einen Tipp.
-   Die folgenden Variationen sind falsch: QuickInfo, QuickInfo und QuickInfo.
-   Verwenden Sie Hover, um die Benutzerinteraktion zu beschreiben.

