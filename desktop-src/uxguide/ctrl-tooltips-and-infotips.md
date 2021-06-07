---
title: QuickInfos und Infotips
description: Eine QuickInfo ist ein kleines Popupfenster, das das steuerelement ohne Bezeichnung beschriftet, auf das gezeigt wird, z. B. nicht bezeichnete Symbolleistensteuerelemente oder Befehlsschaltflächen.
ms.assetid: 80979281-eefb-485a-b42f-7f9e05665357
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8911c5a008d2de6cec2bd564fd786a23c670d633
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524534"
---
# <a name="tooltips-and-infotips"></a>QuickInfos und Infotips

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Eine QuickInfo ist ein kleines Popupfenster, das das steuerelement ohne Bezeichnung beschriftet, auf das gezeigt wird, z. B. nicht bezeichnete Symbolleistensteuerelemente oder Befehlsschaltflächen.

![Screenshot: Schaltfläche "Drucken" mit der QuickInfo "Drucken (STRG+P)"](images/ctrl-tooltips-and-infotips-image1.png)

Eine typische QuickInfo für eine Symbolleistenschaltfläche.

Da QuickInfos so nützlich sind, gibt es ein verwandtes Steuerelement namens Infotips, das aussagekräftigeren Text bereitstellt, als es mit QuickInfos möglich ist.

Eine Infoinfo ist ein kleines Popupfenster, in dem das Objekt, auf das gezeigt wird, präzise beschrieben wird, z. B. Beschreibungen von Symbolleistensteuerelementen, Symbolen, Grafiken, Links, Windows-Explorer Objekten, Startmenü Elementen und Taskleistenschaltflächen. Infotips sind eine Form der Steuerung der [progressiven Offenlegung,](ctrl-progressive-disclosure-controls.md)sodass kein beschreibender Text mehr auf dem Bildschirm angezeigt werden muss.

![Screenshot der Schaltfläche "Freigeben" mit Infotip ](images/ctrl-tooltips-and-infotips-image2.png)

Ein typischer Infotip.

Im Rahmen dieses Artikels werden QuickInfos und Infotips zusammen als Tipps bezeichnet.

Tipps helfen Benutzern, unbekannte oder unbekannte Objekte zu verstehen, die nicht direkt auf der Benutzeroberfläche (UI) beschrieben werden. Sie werden automatisch angezeigt, wenn Benutzer mit dem Mauszeiger auf ein Objekt zeigen, und sie werden entfernt, wenn Benutzer auf das Steuerelement klicken oder die Maus bewegen oder wenn ein Zeitüberschreitung der Trinkgeldzeit erreicht wird.

**Entwickler:** Es gibt kein InfoTip-Steuerelement. Infotips werden mit dem QuickInfo-Steuerelement implementiert. Der Unterschied liegt in der Verwendung und nicht in der Implementierung.

> [!Note]  
> Richtlinien im Zusammenhang mit [Sprechblasen,](ctrl-balloons.md) [Symbolleisten](cmd-toolbars.md)und [Hilfe](winenv-help.md) werden in separaten Artikeln vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Werden die Informationen basierend auf dem Mauszeigerzeiger angezeigt?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Tipps nur als Ergebnis der Benutzerinteraktion anzeigen, werden nie selbst angezeigt. Im Gegensatz dazu können [Sprechblasen](ctrl-balloons.md) eigenständig angezeigt werden (wie bei Benachrichtigungen), sodass sie über ein Ende verfügen, das ihre Quelle identifiziert.
-   **Ist das Steuerelement mit Text beschriftet?** Wenn dies nicht der Fall ist, fügen Sie die Beschriftung als QuickInfo hinzu. Beachten Sie, dass die meisten Steuerelemente beschriftet sein sollten und daher keine QuickInfos aufweisen. Symbolleistensteuerelemente und Befehlsschaltflächen mit grafischen Bezeichnungen sollten QuickInfos aufweisen.
-   **Profitiert ein Objekt von einer ergänzenden Beschreibung oder weiteren Informationen?** Verwenden Sie in diesem Falle eine Infoinfo. Der Text muss jedoch ergänzend sein, d. h. für die primären Aufgaben nicht wesentlich sein. Fügen Sie wichtige Informationen direkt in die Benutzeroberfläche ein, damit Benutzer nicht erst danach suchen müssen.
-   **Handelt es sich bei den ergänzenden Informationen um einen Fehler, eine Warnung oder einen Status?** Verwenden Sie in diesem Falle ein anderes Benutzeroberflächenelement, z. B. eine Sprechblase, [eine Fehlermeldung](mess-error.md)oder eine [Statusleiste.](ctrl-status-bars.md) Infotips für Infotips für Benachrichtigungsbereiche sind eine Ausnahme, da sie zum Anzeigen von Statusinformationen verwendet werden können.
-   **Müssen die Benutzer mit den Informationen interagieren?** Verwenden Sie in diesem Falle ein anderes Steuerelement, z. B. eine Sprechblase. Eine Benutzerinteraktion mit QuickInfo ist nicht möglich, da die Informationen beim Bewegen der Maus ausgeblendet werden.
-   **Müssen Benutzer die zusätzlichen Informationen drucken?** Verwenden Sie in diesem Falle ein anderes Steuerelement, z. B. ein statisches Kommentarfeld. Sie können jedoch auch Infotips verwenden, um einen direkteren Zugriff auf diese Informationen zu ermöglichen.

    ![Screenshot des Kommentarsprechblasens ](images/ctrl-tooltips-and-infotips-image3.png)

    In diesem Beispiel können Benutzer mit einem statischen Kommentarfeld in Microsoft Word Kommentare drucken.

-   **Ist der Kontext so, dass Benutzer die Tipps möglicherweise ungärrlich oder ablenkend finden?** Falls ja, sollten Sie erwägen, eine andere Lösung zu verwenden, einschließlich überhaupt nichts zu tun. Wenn Sie Tipps in solchen Kontexten verwenden, erlauben Sie Benutzern, sie zu deaktivieren.

Bei entsprechender Verwendung verbessern Tipps die Kommunikation mit dem Benutzer. **Verwenden Sie niemals Tipps als Ersatz für ein gutes Design.** Wenn eine Grafik, Schaltfläche oder ein anderes Objekt erfordert, dass Benutzer weiterhin einen Tipp überprüfen, um sie zu verstehen, ist der Entwurf schlecht. Korrigieren Sie stattdessen den Entwurf.

## <a name="design-concepts"></a>Entwurfskonzepte

Tipps sind eine leistungsstarke Möglichkeit, eine Benutzeroberfläche zu vereinfachen. Sie stellen Informationen bereit, die Benutzer benötigen, wenn sie sie benötigen, mit minimalem Aufwand. Tipps können Ihnen helfen, den Bildschirmbereich effektiver zu nutzen und die Bildschirmübersicht zu reduzieren. Schlecht entworfene Tipps können jedoch heiter, ablenkend, nicht hilfreich, überwältigend oder im Weg stehen. Die folgenden Entwurfskonzepte sollen den Unterschied verdeutlichen.

### <a name="discoverability"></a>Erkennbarkeit

Tipps werden automatisch angezeigt, wenn Benutzer über einen bestimmten Zeitraum mit dem Mauszeiger auf ein Objekt zeigen. Dieser Zeitverzögerungsmechanismus macht Tipps sehr praktisch, verringert aber auch deren Auffindbarkeit.

Im Laufe der Zeit lernen Benutzer, dass bestimmte Standardobjekte wie Symbolleistenschaltflächen, Grafische Schaltflächen, Startmenü Elemente und Symbole für den Benachrichtigungsbereich Tipps enthalten, sodass Sie ihre Auffindbarkeit als selbstverständlich betrachten können.

Es dauert länger, bis Benutzer Tipps an stellen, die nicht dem Standard entsprechen. Es gibt keinen visuellen Hinweis, z. B. eine Hotspots- oder Zeigeränderung, die angibt, dass ein Objekt über einen Trinkgeld verfügt. Noch schlechter ist es, dass einige Benutzer ihre Maus sehr bewegen, insbesondere wenn sie lernen, auf der Benutzeroberfläche zu navigieren. Benutzer müssen wissen, dass ein Objekt einen Tipp hat, entweder durch erfahrungsgemäße Erfahrung oder durch Experimentieren.

Sie können die Auffindbarkeit verbessern, indem Sie tipps konsistent verwenden, was wiederum die Vorhersagbarkeit fördert. Wenn Sie Tipps für einige Objekte bereitstellen, sollten Sie diese für alle ähnlichen Objekte bereitstellen, für die Benutzer wahrscheinlich zusätzliche Informationen benötigen. Manchmal kann dies schwierig sein, da Sie auch sicherstellen müssen, dass die Tipps hilfreich und nicht offensichtlich sind.

Wenn sich die Bereitstellung erkennbarer, konsistent hilfreicher Tipps als Problem erweist, sollten Sie alternative Entwürfe wie selbsterklärende Steuerelementbezeichnungen oder ergänzenden Text in Betracht ziehen.

### <a name="appropriate-information"></a>Geeignete Informationen

Informationen, die für Tipps geeignet sind, haben die folgenden Merkmale:

-   **Prägnant.** Die von Tipps verwendeten Popupfenster eignen sich perfekt für kurze Sätze und Satzfragmente sowie für formatierten Text. Große, unformatierte Textblöcke sind schwer zu lesen und überwältigend.
-   **Hilfreich.** Tipptext muss informativ sein. Es sollte nicht offensichtlich sein oder einfach wiederholen, was bereits auf dem Bildschirm vorhanden ist.
-   **Zusätzliche.** Da Trinkgeldtext nicht immer sichtbar ist, sollten es zusätzliche Informationen sein, die Benutzer nicht lesen müssen. Wichtige Informationen sollten mithilfe von selbsterklärenden Steuerelementbezeichnungen oder ergänzendem Text übermittelt werden.
-   **Statische.** Benutzer erwarten nicht, dass sich Tipps von einer Instanz zur nächsten ändern, sodass sie wahrscheinlich keine Änderungen an dynamischen Inhalten bemerken, z. B. Statusinformationen. Tipps zum Symbol für den Benachrichtigungsbereich sind eine wichtige Ausnahme: Benutzer werden dort eher Änderungen an Trinkgeldinformationen feststellen, da diese Symbole in erster Linie den Status kommunizieren.

### <a name="appropriate-timeouts"></a>Geeignete Timeouts

Die entsprechende automatische Anzeige und Entfernung von Tipps ist entscheidend für das Ziel der Benutzer, die Kontrolle über ihre Benutzeroberflächenumgebung zu behalten. Tipps haben drei Timeoutwerte:

-   **Ersten.** Die Zeit, zu der der Zeiger stationär bleiben muss, damit der Trinkgeld angezeigt wird. Die Standardzeit beträgt 0,5 Sekunden.
-   **Erneutes Zeigen.** Die Zeit, zu der der Zeiger stationär bleiben muss, während der Zeiger von einem Ziel zu einem anderen bewegt wird. Die Standardzeit beträgt 0,1 Sekunden.
-   **Entfernung.** Die Zeit, nach der der Trinkgeld automatisch entfernt wird. Die Standardzeit beträgt 5 Sekunden.

Zu kurze Anfänglichkeit und erneutes Anzeigen von Werten führen zu einer mäßigen, störenden Erfahrung, da sie häufig versehentlich angezeigt werden, während zu lange Dazu führen, dass Tipps nicht reagieren oder nicht erkannt werden. Die Standardentfernungszeit funktioniert gut für kurzen Trinkgeldtext, wie in QuickInfos verwendet. Infotips weisen längeren Text auf, sodass sie längere Anzeigezeiten benötigen.

### <a name="appropriate-placement"></a>Geeignete Platzierung

Tipps sollten in der Nähe des Objekts platziert werden, auf das der Mauszeiger zeigt, in der Regel am Ende oder Kopf des Zeigers, wenn möglich. Sie sollten jedoch nie auf eine Weise platziert werden, die das Verhalten des Benutzers beeinträchtigt, indem das objekt von Interesse verdeckt wird. Um dieses Problem zu verhindern, müssen Sie möglicherweise die Spitze vom Zeiger weg, aber neben dem -Objekt verschieben. Dies ist kein Problem, solange die Beziehung zwischen dem Objekt und dessen Trinkgeld klar ist. Stellen Sie sicher, dass Benutzer den Zeiger nicht nur bewegen, um die Tipps Ihres Programms zu erhalten, um fortzugehen.

### <a name="accessibility"></a>Zugriff

Tipps haben ungewöhnliche Auswirkungen auf die Barrierefreiheit. Während sie normalerweise ausgelöst werden, indem sie mit dem Mauszeiger auf ein Objekt zeigen, werden Tipps von [Sprachausgaben](inter-accessibility.md) für Steuerelemente mit Tastaturzugriff behandelt. Bei geeigneter Verwendung für präzise, hilfreiche, statische, ergänzende Informationen können Tipps die allgemeine Barrierefreiheit verbessern. Tatsächlich ist das Alttexttippmuster die bevorzugte Methode, um Grafiken zugänglich zu machen. Wenn sie jedoch nicht angemessen verwendet werden, beeinträchtigen sie die Barrierefreiheit, da wichtige oder dynamische Informationen schwieriger zu erhalten sind.

Stellen Sie mehr als eine Möglichkeit bereit, auf ein Steuerelement zuzugreifen, wenn für dieses Steuerelement ein Tipp ohne Tastaturzugriff erforderlich ist.

![Screenshot der Druckschaltfläche mit QuickInfo ](images/ctrl-tooltips-and-infotips-image4.png)

In diesem Beispiel können Benutzer mithilfe der Symbolleistenschaltfläche (auf die nicht über die Tastatur zugegriffen werden kann) oder der Tastenkombination Befehl drucken drucken drucken.

**Wenn Sie nur eine Sache tun...**

Entwerfen Sie erkennbare Tipps, die präzise, hilfreiche, statische, ergänzende Informationen zum richtigen Zeitpunkt an der entsprechenden Stelle anzeigen.

## <a name="usage-patterns"></a>Verwendungsmuster

Tipps weisen mehrere Verwendungsmuster auf:



|    Verwendung                                                                                                                             |    Beispiel                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **QuickInfos**<br/> zeigt die Bezeichnung eines Steuerelements oder Glyphens ohne Bezeichnung an. <br/>                                         | Da diese Tipps als Bezeichnungen dienen, folgt ihr Text den Bezeichnungsrichtlinien für das zugrunde liegende Steuerelement. <br/> ![Screenshot der Schaltfläche "Liste exportieren" mit QuickInfo ](images/ctrl-tooltips-and-infotips-image5.png)<br/> In diesem Beispiel gibt die QuickInfo die Befehlsbezeichnung an.<br/> ![Screenshot der Schaltfläche "Schließen" mit QuickInfo ](images/ctrl-tooltips-and-infotips-image6.png)![Screenshot der Wiedergabeschaltfläche mit QuickInfo ](images/ctrl-tooltips-and-infotips-image7.png)<br/> In diesen Beispielen bezeichnen QuickInfos grafische Schaltflächen.<br/> ![Screenshot des Menüglyphens "Show" mit QuickInfo ](images/ctrl-tooltips-and-infotips-image8.png)<br/> In diesem Beispiel bezeichnet die QuickInfo ein Glyphen.<br/> |
| **Infotips**<br/> Geben Sie eine ergänzende Beschreibung oder Erklärung eines Objekts oder Steuerelements an. <br/>                  | Verwenden Sie Infotips, um Objekte und Steuerelemente wie [Symbolleistensteuerelemente,](cmd-toolbars.md) [Symbole](vis-icons.md) (einschließlich Symbolüberlagerungen), [Links,](ctrl-links.md) [Registerkarten,](ctrl-tabs.md)Steuerelemente für die progressive [Offenlegung](ctrl-progressive-disclosure-controls.md)und benutzerdefinierte Steuerelemente zu beschreiben oder zu erklären. <br/> ![Screenshot der E-Mail-Schaltfläche mit Infotip ](images/ctrl-tooltips-and-infotips-image9.png)<br/> ![Screenshot der Schaltfläche "Burn" mit Infotip ](images/ctrl-tooltips-and-infotips-image10.png)<br/> In diesen Beispielen stellen Infotips zusätzliche Informationen zu Steuerelementen und Objekten bereit.<br/>                                                                                        |
| **Alttextinfotips**<br/> beschreiben sie eine Grafik für die Barrierefreiheit. <br/>                                              | Dieses Muster ist in erster Linie für Benutzer vorgesehen, die eine Sehbehinderung haben und möglicherweise eine Sprachausgabe verwenden. <br/> ![Screenshot der Windows-Startschaltfläche mit Infotip ](images/ctrl-tooltips-and-infotips-image11.png)<br/> In diesem Beispiel beschreibt die Infotip die Startmenü Grafik.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Miniaturansicht**<br/> zeigt ein kleines Bild eines Elements an. <br/>                                                         | Miniaturansichten bieten eine leicht erkennbare grafische Darstellung eines Fensters oder Dokuments. <br/> ![Screenshot der Miniaturansicht der Systemsteuerungskategorien ](images/ctrl-tooltips-and-infotips-image12.png)<br/> In diesem Beispiel gibt die Windows-Taskleiste Miniaturansichttipps für ihre Elemente.<br/> ![Screenshot der Miniaturansicht des Fotos und der zugehörigen Daten ](images/ctrl-tooltips-and-infotips-image13.png)<br/> In diesem Beispiel gibt Windows Fotogalerie Miniaturansichttipps für seine Elemente.<br/>                                                                                                                                                                                                                      |
| **Infotips für Details**<br/> zeigt detaillierte Informationen zu einem Objekt an. <br/>                                        | Infotips sind eine effektive Möglichkeit, detaillierte Informationen zu einem Objekt anzuzeigen oder Daten bereitzustellen. <br/> ![Screenshot der Infotipinfo des Fotos mit Dateityp ](images/ctrl-tooltips-and-infotips-image14.png)![Screenshot des Diagramms mit Infotip-Detailwerten ](images/ctrl-tooltips-and-infotips-image15.png)<br/> In diesen Beispielen enthalten Infotips ausführliche Informationen zu einem Objekt oder zu Daten.<br/>                                                                                                                                                                                                                                                                                                      |
| **Infotips im Startmenü**<br/> beschreiben sie ein Element im Startmenü. <br/>                                              | Das Startmenü besteht aus Programmnamen und wichtigen Windows-Zielen wie Dokumenten, Bildern und Systemsteuerung. Diese Tipps beschreiben Startmenüelemente, in der Regel durch eine kurze Beschreibung des Programms oder Ziels sowie der primären Aufgaben, die Benutzer damit ausführen können. Diese Beschreibungen werden auch über das Suchfeld des Startmenüs indiziert, um Benutzern die Suche nach den programmen zu ermöglichen, die sie benötigen. <br/> ![Screenshot der Infotip zum Welcome Center ](images/ctrl-tooltips-and-infotips-image16.png)<br/> In diesem Beispiel wird in der Infotip beschrieben, welche Möglichkeiten Benutzer mit einem Programm im Startmenü haben.<br/>                                                                                    |
| **Systemsteuerung Infotips**<br/> beschreiben eine Systemsteuerungskategorie oder -aufgabe. <br/>                                    | Diese Tipps enthalten zusätzliche Informationen, mit denen Benutzer die richtige Systemsteuerungskategorie und das richtige Element auswählen können. <br/> ![Screenshot der Kategorie "Benutzerkonten" mit Infotip ](images/ctrl-tooltips-and-infotips-image17.png)<br/> In diesem Beispiel beschreibt der Infotip die Kategorie Benutzerkonten Systemsteuerung.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| **Infotips für vollständige Namen**<br/> zeigt den vollständigen Namen eines Elements an, wenn der Name abgeschnitten oder nicht vollständig sichtbar ist. <br/> | Mit diesen Tipps können Sie Elemente in einem kompakteren Bereich anzeigen und gleichzeitig den Bedarf an horizontalem Scrollen reduzieren. dies ist besonders wichtig, wenn die Inhaltslänge unbekannt ist, da sie dynamisch ist. Im Gegensatz zu den anderen Mustern werden diese Tipps bei Verwendung in Listen und Strukturen direkt über dem Quellobjekt angezeigt. <br/> ![Screenshot der Infotip zum Gruppentitel des Optionsfelds ](images/ctrl-tooltips-and-infotips-image18.png)<br/> In diesem Beispiel wird ein Infotip verwendet, um den vollständigen Elementnamen beim Zeigen anzuzeigen.<br/>                                                                                                                                                                                     |
| **Statusinfos**<br/> Anzeigen von Statusinformationen für Benachrichtigungsbereichssymbole. <br/>                              | Normalerweise sollten Tipps statisch sein, da Benutzer nicht erwarten, dass sie von einer Instanz zur nächsten wechseln. **Symbole im Infobereich stellen eine Ausnahme** dar, da diese Symbole den Status kommunizieren und kein anderer Bildschirmbereich für Statustext verfügbar ist. <br/> ![Screenshot der Infoinfo "Messenger nicht angemeldet" ](images/ctrl-tooltips-and-infotips-image19.png)<br/> ![Screenshot des Infotips "Messenger signed in" ](images/ctrl-tooltips-and-infotips-image20.png)<br/> In diesen Beispielen enthalten Infotips Statusinformationen für Symbole im Benachrichtigungsbereich.<br/>                                                                                                                                  |



 

## <a name="guidelines"></a>Richtlinien

### <a name="timeouts"></a>Timeouts

-   **Verwenden Sie die Standardtimeouts für die Erst- und Neuanzeige. Ausnahme:**
    -   Miniaturansichten, die nicht redundant sind und auf der Seite ihres zugeordneten Objekts angezeigt werden, können sofort (ohne Verzögerung) angezeigt werden. Verwenden Sie jedoch das anfängliche Standardtimeout für redundante Miniaturansichten (z. B. einen großen Miniaturansichtstipp für ein kleines Grafikobjekt) oder Miniaturansichten, die das zugehörige Objekt abdecken.
-   **Verwenden Sie für QuickInfos das Standardmäßige Timeout für das Entfernen von Fünf-Sekunden-Tipps.**
-   Deaktivieren Sie für **Infotips das Timeout zum Entfernen von Trinkgeld. Entwickler:** Da Sie das Entfernungstimeout technisch nicht deaktivieren können, legen Sie es auf den größten Wert fest.
-   Wenn Sie für die Barrierefreiheit die Timeoutwerte auf einen anderen Wert als den Maximalwert festlegen müssen, machen Sie sie zu einem Vielfachen der Systemparameter SPI \_ GETMOUSEHOVERTIME und SPI \_ GETMESSAGEDURATION, anstatt feste Zeiten zu verwenden. Dadurch werden die Timeouts an die Geschwindigkeit des Benutzers angepasst.

### <a name="placement"></a>Platzierung

-   **Vermeiden Sie das Abdecken des Objekts, das der Benutzer anzeigen oder mit dem er interagieren möchte.** Platzieren Sie den Tipp immer auf der Seite des Objekts, auch wenn dies eine Trennung zwischen zeiger und tip erfordert. Eine Trennung ist kein Problem, solange die Beziehung zwischen dem Objekt und seinem Trinkgeld klar ist.

    -   **Ausnahme:** QuickInfos mit vollständigem Namen, die in Listen und Strukturen verwendet werden.

    **Falsch:**

    ![Screenshot der Infoinfo, die das Suchfeld verdeckt ](images/ctrl-tooltips-and-infotips-image21.png)

    **Richtig:**

    ![Screenshot der infotip unterhalb des Suchfelds ](images/ctrl-tooltips-and-infotips-image22.png)

    Im richtigen Beispiel wird die Infotip vom Suchfeld entfernt, obwohl dafür Platz zwischen dem Text und dem Caretfeld erforderlich ist.

    **Falsch:**

    ![Screenshot der Infotip, der überarbeiteten Text verdeckt ](images/ctrl-tooltips-and-infotips-image23.png)

    **Richtig:**

    ![Screenshot der Infotips oberhalb des überarbeiteten Texts ](images/ctrl-tooltips-and-infotips-image24.png)

    Im richtigen Beispiel ist der zugrunde liegende Text viel nützlicher als der Tipp, sodass der Infotip gut platziert wird.

-   **Vermeiden Sie bei Auflistungen von Elementen die Abdeckung des nächsten Objekts, das der Benutzer wahrscheinlich anzeigen oder mit dem er interagieren wird.** Vermeiden Sie bei horizontal angeordneten Elementen das Platzieren von Tipps auf der rechten Seite. Vermeiden Sie bei vertikal angeordneten Elementen das Platzieren von Tipps darunter.

    **Falsch:**

    ![Screenshot der Liste der zuletzt angezeigten Elemente mit infotip ](images/ctrl-tooltips-and-infotips-image25.png)

    **Richtig:**

    ![Screenshot der Infotip neben der Liste der zuletzt verfügbaren Elemente ](images/ctrl-tooltips-and-infotips-image26.png)

    Im falschen Beispiel deckt der Tipp das Objekt ab, mit dem der Benutzer als Nächstes höchstwahrscheinlich interagiert.

-   **Stellen Sie für potenziell ablenkende (oft große) Tipps sicher, dass die Informationen für die meisten Benutzer hilfreich sind.** Wenn dies nicht der Fall ist, machen Sie die ablenkenden Tipps optional, oder beseitigen Sie sie sogar. Andernfalls müssen die meisten Benutzer den Zeiger vom Zielobjekt weg bewegen, um den Tipp zu verwerfen.

### <a name="tooltips"></a>QuickInfos

-   **Verwenden Sie QuickInfos, um Bezeichnungen für Steuerelemente ohne Bezeichnungen zur Verfügung zu stellen.** Steuerelemente, die häufig QuickInfos enthalten, sind [Symbolleistenschaltflächen,](cmd-toolbars.md)Grafische Schaltflächen und [Steuerelemente für progressive Offenlegung.](ctrl-progressive-disclosure-controls.md) Steuerelemente mit Eingabeaufforderungen werden als bezeichnet betrachtet, z. [B. Textfelder](ctrl-text-boxes.md) [und Kombinationsfelder.](/windows/desktop/uxguide/ctrl-drop) Alle anderen Steuerelemente sollten explizite Bezeichnungen haben.
-   Verwenden Sie Satzfragmente, ohne die Interpunktion zu beenden.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
    -   **Ausnahme:** Diese Richtlinie ist neu für Windows Vista. Bei älteren Anwendungen können Sie bei Bedarf die Groß-/Formatvorlagen verwenden, um das Mischen von Groß-/Formatvorlagen zu vermeiden.
-   Fügen Sie [auslassungszeichen](ctrl-command-buttons.md) hinzu, wenn die Bezeichnung für einen Befehl gilt, der zusätzliche Informationen benötigt.
-   Wie bei normalen Bezeichnungen sollten **QuickInfos** in der Regel nur fünf Wörter oder weniger kurz halten, aber bestimmte Bezeichnungen gegenüber unübersichtlich bevorzugt werden.

    **Annehmbar:**

    ![Screenshot der QuickInfo zum Drucken ](images/ctrl-tooltips-and-infotips-image27.png)

    **Besser:**

    ![Screenshot der QuickInfo "Drucken auf Standarddrucker" ](images/ctrl-tooltips-and-infotips-image28.png)

    **Beste:**

    ![Screenshot der QuickInfo "Drucken (Dokumentschreiber)" ](images/ctrl-tooltips-and-infotips-image29.png)

    **Falsch:**

    ![Screenshot der ausführlichen QuickInfo ](images/ctrl-tooltips-and-infotips-image30.png)

    In diesen Beispielen ist das beste Beispiel präzise und spezifisch, während das falsche Beispiel unnötig ausführlich ist.

-   **QuickInfos können auch weitere Details für bezeichnete Symbolleistenschaltflächen bereitstellen, wenn dies hilfreich ist.** Wiederholen Sie nicht nur das, was bereits in der Bezeichnung vorhanden ist, oder geben Sie eine wortige Neubeschriftung.

    **Richtig:**

    ![Screenshot der QuickInfo "Alle Outlook durchsuchen" ](images/ctrl-tooltips-and-infotips-image31.png)

    In diesem Beispiel wird in der QuickInfo erläutert, was Search macht.

    **Falsch:**

    ![Screenshot der Bezeichnung der quicktip repeating button ](images/ctrl-tooltips-and-infotips-image32.png)

    In diesem Beispiel wiederholt die QuickInfo nur das, was bereits in der Bezeichnung vorhanden ist.

-   **Sie müssen aus Gründen der Konsistenz keine QuickInfos für bezeichnete Steuerelemente geben.**

    ![Screenshot von schaltflächen mit und ohne Bezeichnung ](images/ctrl-tooltips-and-infotips-image33.png)

    In diesem Beispiel verfügen die Schaltflächen der Symbolleiste ohne Bezeichnung über QuickInfos, die bezeichneten schaltflächen jedoch nicht.

-   Machen Sie QuickInfos gegebenenfalls hilfreicher, **indem Sie Tastenkombinationen und Standardwerte bereitstellen.** Setzen Sie diese zusätzlichen Informationen in Klammern. Dadurch sind QuickInfos für bezeichnete Steuerelemente hilfreich, auch wenn sie andernfalls nur die Bezeichnung wiederholen. Berücksichtigen Sie diesen zusätzlichen Text nicht, wenn Sie die Prägnanz einer QuickInfo auswerten.

    ![Screenshot der QuickInfo "Drucken (Dokumentschreiber)" ](images/ctrl-tooltips-and-infotips-image29.png)

    In diesem Beispiel zeigt Word Standardwerte und Tastenkombinationen in den QuickInfos der Symbolleiste an.

### <a name="infotips"></a>Infotips

-   **Bei Infotips an nicht standardmäßigen Stellen sollten Sie Konsistenz gegenüber Hilfreichkeit bevorzugen, um die Aufholbarkeit zu verbessern.** Geben Sie Tipps für alle Objekte an, für die Benutzer wahrscheinlich zusätzliche Informationen wünschen, auch wenn einige Infotips offensichtlich sein könnten. Dadurch wird vermieden, dass Benutzer auf eine Infotip warten müssen, die nie angezeigt wird.
    -   **Ausnahme:** Wenn nur wenige Objekte über hilfreiche Infotips verfügen, verwenden Sie überhaupt keine Infotips. Verwenden Sie stattdessen selbsterklärende Steuerelementbezeichnungen oder in-place supplemental text.
-   Verwenden Sie vollständige Sätze mit endender Interpunktion.
    -   **Ausnahme:** [Infotips für Infotips im](winenv-notification.md) Infobereich verwenden keine Endzeichen.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Verwenden Sie "present tense", nicht "future".
-   Verwenden Sie parallele grammatikalische Konstruktionen. Parallelität erfordert, dass Wörter und Ausdrücke, die dieselbe Funktion haben, die gleiche Form haben.
    -   **Ausnahme:** Für das Infotip-Muster mit vollständigem Namen stimmt der Infotiptext genau mit dem Ausdruck, der Groß-/Zeichensetzung des zugrunde liegenden Steuerelements ab.
-   **Vermeiden Sie große Infotips.** Große Infotips sind schwer zu lesen und schwer zu positionieren, ohne das zugrunde liegende Objekt zu stören.
-   **Formatieren Sie Infotips, um ihre Inhalte leichter zu lesen und zu scannen.** Große Blöcke von unformatiertem Text können schwierig zu lesen sein.

    **Falsch:**

    ![Screenshot einer langen, unstrukturierten, ausgeführten QuickInfo ](images/ctrl-tooltips-and-infotips-image34.png)

    **Richtig:**

    ![Screenshot der gleichen QuickInfo mit einer Zeile pro Element ](images/ctrl-tooltips-and-infotips-image35.png)

    Im richtigen Beispiel ist der formatierte Text viel einfacher zu lesen und zu scannen.

-   Geben Sie bei der ersten Verwendung in einem Infotip die Namen von Akronymen und dann das Akronym in Klammern ein. Beispiel: "Dynamic Host Configuration Protocol (DHCP)"

### <a name="start-menu-infotips"></a>Infotips im Startmenü

-   Verwenden Startmenü Infotips, um das Element präzise zu beschreiben und die primären Aufgaben auflisten, die Benutzer **mit dem Element ausführen können.**
-   **Seien Sie hilfreich.** Konzentrieren Sie sich darauf, was Benutzer tun können. Wiederholen Sie nicht einfach den Elementnamen, oder verwenden Sie ihn überhaupt in der Beschreibung.
-   **Seien Sie spezifisch.** Vermeiden Sie generische Verben und catch-all-Ausdrücke wie und andere Aufgaben. Wenn die Informationen wichtig sind, listen Sie sie speziell auf. Andernfalls wird davon ausgegangen, dass Benutzer verstehen, dass nicht alles in den Infotips aufgeführt ist.
-   **Seien Sie präzise.** Verwenden Sie 25 Wörter oder weniger. Längere Infotips raten vom Lesen ab.
-   **Beginnen Sie mit einem gegenwärtigen, imperativen Verb wie** Erstellen, Bearbeiten, Anzeigen und Senden. Bevorzugen Sie bestimmte Verben gegenüber generischen Verben wie "verwalten" und "öffnen", die tatsächlich für die meisten Startmenü gelten. Kommen Sie direkt auf den Punkt.

    **Falsch:**

    ![Screenshot der QuickInfo: Öffnet den Ordner "music". ](images/ctrl-tooltips-and-infotips-image36.png)

    **Besser:**

    ![Screenshot der QuickInfo: Speichern und Wiederspielen von Musik ](images/ctrl-tooltips-and-infotips-image37.png)

    Im falschen Beispiel beginnt der Infotip mit einem generischen Verb. Das bessere Beispiel kommt mit bestimmten Verben auf den Punkt, verwendet aber weiterhin den unnötigen Ausdruck "und andere" am Ende des Trinkgelds.

-   **Verwenden Sie keine Sprache, die wie Marketing klingt.**

    **Falsch:**

    ![Screenshot der Infoinfo "One-Stop-Startpunkt" ](images/ctrl-tooltips-and-infotips-image38.png)

    In diesem Beispiel klingt der Infotip wie Marketing.

-   Da diese Infotips für das Suchfeld Startmenü indiziert werden, beschreiben Sie die wichtigen Aufgaben Ihres Programms mithilfe von Begriffen, nach denen Benutzer am **wahrscheinlichsten suchen. Erwägen Sie die Verwendung von Schlüsselwörtern und gängigen Synonymen.**

    **Falsch:**

    ![Screenshot der QuickInfo: Erstellen von DVDs ](images/ctrl-tooltips-and-infotips-image39.png)

    **Richtig:**

    ![Screenshot der QuickInfo: Cds, DVDs erstellen (speichern) ](images/ctrl-tooltips-and-infotips-image40.png)

    Im richtigen Beispiel weist die Infotip allgemeine Synonyme auf.

-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   **Entwickler:** Der Startmenü Infotip-Text stammt aus dem Kommentarfeld des Elements.

### <a name="quick-launch-tooltips"></a>Schnellstart QuickInfos

-   **Verwenden Sie eine QuickInfo im Format :** Start (vollständiger Programmname)
-   Verwenden Sie keine Interpunktion am Ende.
-   Verwenden Sie keinen zusätzlichen Text, um das Programm oder seine Verwendungszwecke zu beschreiben. Da Benutzer die programme auswählen, die auf der Schnellstart Leiste angezeigt werden, kennen sie ihren Zweck bereits.

### <a name="control-panel-infotips"></a>Systemsteuerung Infotips

-   Verwenden Sie Systemsteuerung Infotips, um **die Systemsteuerung Tasks sowie die konfigurierte Hardware und Software präzise** zu beschreiben.
-   **Systemsteuerung Namen und Symbole müssen Infotips aufweisen.** Einzelne Aufgaben verfügen nicht über QuickInfos.
-   **Seien Sie hilfreich.** Konzentrieren Sie sich darauf, was Benutzer tun können. Wiederholen Sie nicht einfach den Systemsteuerung Elementnamen, oder verwenden Sie ihn überhaupt in der Beschreibung.
-   **Seien Sie spezifisch.** Vermeiden Sie generische Verben und catch-all-Ausdrücke wie und andere Hardware. Wenn die Informationen wichtig sind, listen Sie sie explizit auf. Gehen Sie andernfalls davon aus, dass Benutzer verstehen, dass nicht alles in den Infotips aufgeführt ist.

    **Falsch:**

    ![Screenshot der QuickInfo: Konfiguriert die Maus ](images/ctrl-tooltips-and-infotips-image41.png)

    **Richtig:**

    ![Screenshot einer ausführlichen QuickInfo für Mauseinstellungen ](images/ctrl-tooltips-and-infotips-image42.png)

    Im richtigen Beispiel werden die konfigurierten Hardwaretypen speziell aufgeführt.

-   **Seien Sie präzise.** Verwenden Sie mindestens 25 Wörter. Längere Infotips raten vom Lesen ab.
-   **Beginnen Sie mit einem imperativen Verb mit einer aktuellen Verformung.**

    **Richtig:**

    Konfigurieren sie die Einstellungen für die Internetanzeige und -verbindung.

    Passen Sie die Einstellungen für Seh-, Hör- und Mobilitätseinstellungen an.

-   **Gelangen Sie direkt zu dem Punkt.** Verwenden Sie keine Sprache, die für Systemsteuerung gilt, z. B. "Verwenden Sie zum Anzeigen und Konfigurieren von Einstellungen für die Darstellung und Funktionalität Ihrer..." oder "Stellt Optionen für Sie bereit..."
-   Verwenden Sie keine Sprache, die nach Marketing klingt.

    **Falsch:**

    Ihr One-Stop-Startpunkt für alle Anforderungen an die Datenträgerkonfiguration.

-   Da diese Infotips für das suchfeld Systemsteuerung indiziert werden, **beschreiben Sie Elemente mithilfe von Begriffen, nach denen Benutzer am wahrscheinlichsten suchen.** Erwägen Sie die Verwendung gängiger Synonyme für beliebte Aufgaben und Objekte.

    ![Screenshot der QuickInfo mit Aufgaben des Gamecontrollers ](images/ctrl-tooltips-and-infotips-image43.png)

    In diesem Beispiel wird das Element mitHilfe von Begriffen beschrieben, nach denen Benutzer höchstwahrscheinlich suchen.

-   Wenn ein Systemsteuerung Element wahrscheinlich mit anderen verwechselt wird, erläutern Sie in der Infotip, wie es sich unterscheidet.

    **Falsch:**

    ![Screenshot der Infoinfo mit fehlenden spezifischen Details ](images/ctrl-tooltips-and-infotips-image44.png)

    In diesem Beispiel konfigurieren beide Systemsteuerung Elemente Sound, aber der Infotip verdeutlicht den Unterschied nicht.

    **Richtig:**

    ![Screenshot der Infotip mit bestimmten Details ](images/ctrl-tooltips-and-infotips-image45.png)

    In diesem Beispiel ist der Unterschied zwischen den beiden Elementen aufgrund des Trinkgelds offensichtlicher.

### <a name="icons"></a>Symbole

Im Gegensatz zu früheren Versionen von Windows lässt Windows Vista Tipps zum Verwenden von Symbolen zu.

-   Verwenden Sie für QuickInfos keine Symbole.
-   Verwenden Sie für Infotips symbole nur, wenn sie bei der Erkennung oder dem Verständnis helfen oder Kontext bereitstellen. Die meisten Infotips sollten keine Symbole enthalten.

    ![Screenshot der Volume-Infoinfo mit Symbol "Symbol" ](images/ctrl-tooltips-and-infotips-image46.png)

    In diesem Beispiel verfügt die Infoinfo über ein Symbol, um das Symbol mit seiner Bedeutung zu verknüpfen.

-   Das Symbol muss den [Stil "Styles"](vis-icons.md) verwenden und eine unaufdringliche Darstellung aufweisen.

Allgemeine Richtlinien und Beispiele für Symbole finden Sie unter [Symbole.](vis-icons.md)

## <a name="documentation"></a>Dokumentation

Wenn Sie sich auf Tipps beziehen:

-   In der Programmierung und anderen technischen Dokumentationen finden Sie informationen zum Typ des Trinkgelds (QuickInfo oder Infotip). Nennen Sie es überall anders einfach als Trinkgeld.
-   Die folgenden Varianten sind falsch: QuickInfo, QuickInfo und QuickInfo.
-   Verwenden Sie den Mauszeiger, um die Benutzerinteraktion zu beschreiben.

