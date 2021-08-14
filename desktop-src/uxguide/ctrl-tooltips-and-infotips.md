---
title: QuickInfos und Infotips
description: Eine QuickInfo ist ein kleines Popupfenster, das das steuerelement ohne Bezeichnung bezeichnet, auf das verwiesen wird, z. B. Symbolleistensteuerelemente ohne Bezeichnung oder Befehlsschaltflächen.
ms.assetid: 80979281-eefb-485a-b42f-7f9e05665357
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 4df7950529b2ac78c9d9bbf51c8996f17bcd985898a286f8d58e05db3b94d27e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041136"
---
# <a name="tooltips-and-infotips"></a>QuickInfos und Infotips

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Eine QuickInfo ist ein kleines Popupfenster, das das steuerelement ohne Bezeichnung bezeichnet, auf das verwiesen wird, z. B. Symbolleistensteuerelemente ohne Bezeichnung oder Befehlsschaltflächen.

![Screenshot: Schaltfläche "Drucken" mit der QuickInfo "Drucken (STRG+P)"](images/ctrl-tooltips-and-infotips-image1.png)

Eine typische QuickInfo für eine Symbolleistenschaltfläche.

Da quicktips sich als so nützlich erwiesen haben, ist ein verwandtes Steuerelement namens infotips vorhanden, das aussagekräftigeren Text bietet, als mit QuickInfos möglich ist.

Ein Infotip ist ein kleines Popupfenster, in dem das Objekt, auf das verwiesen wird, präzise beschrieben wird, z. B. Beschreibungen von Symbolleisten-Steuerelementen, Symbolen, Grafiken, Links, Windows Explorer-Objekten, Startmenü-Elementen und Taskleistenschaltflächen. Infotips sind eine Form von progressiven [Offenlegungssteuerelementen,](ctrl-progressive-disclosure-controls.md)wodurch es nicht mehr notwendig ist, immer beschreibenden Text auf dem Bildschirm zu haben.

![Screenshot der Schaltfläche "Freigeben" mit Infotip ](images/ctrl-tooltips-and-infotips-image2.png)

Ein typischer Infotip.

Im Rahmen dieses Artikels werden QuickInfos und Infotips zusammen als Tipps bezeichnet.

Tipps können Benutzer unbekannte oder unbekannte Objekte verstehen, die nicht direkt in der Benutzeroberfläche beschrieben werden. Sie werden automatisch angezeigt, wenn Benutzer mit dem Mauszeiger auf ein Objekt zeigen, und werden entfernt, wenn Benutzer auf das Steuerelement klicken oder die Maus bewegen oder wenn das Trinkgeld ausbiert.

**Entwickler:** Es gibt kein Infotip-Steuerelement. Infotips werden mit dem QuickInfo-Steuerelement implementiert. Der Unterschied besteht in der Verwendung, nicht in der Implementierung.

> [!Note]  
> Richtlinien im Zusammenhang [mit Sprechblasen,](ctrl-balloons.md) [Symbolleisten](cmd-toolbars.md)und [Hilfe](winenv-help.md) werden in separaten Artikeln vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Werden die Informationen basierend auf dem Zeigerzeigerzeiger angezeigt?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Zeigen Sie Tipps nur als Ergebnis der Benutzerinteraktion an, und zeigen Sie sie nie selbst an. Im Gegensatz dazu [können Sprechblasen](ctrl-balloons.md) selbst angezeigt werden (wie bei Benachrichtigungen), sodass sie über ein Ende verfügen, das ihre Quelle identifiziert.
-   **Ist das Steuerelement mit Text beschriftet?** Wenn dies nicht der Fall ist, fügen Sie die Beschriftung als QuickInfo hinzu. Beachten Sie, dass die meisten Steuerelemente beschriftet sein sollten und daher keine QuickInfos haben. Symbolleisten-Steuerelemente und Befehlsschaltflächen mit Grafischen Bezeichnungen sollten QuickInfos enthalten.
-   **Profitiert ein Objekt von einer zusätzlichen Beschreibung oder weiteren Informationen?** Verwenden Sie in diesem Beispiel einen Infotip. Der Text muss jedoch ergänzend sein, das heißt, er ist für die primären Aufgaben nicht von entscheidender Bedeutung. Fügen Sie wichtige Informationen direkt in die Benutzeroberfläche ein, damit Benutzer nicht erst danach suchen müssen.
-   **Handelt es sich bei den zusätzlichen Informationen um einen Fehler, eine Warnung oder einen Status?** Verwenden Sie in diesem Beispiel ein anderes Benutzeroberflächenelement, z. B. eine Sprechblase, [eine Fehlermeldung](mess-error.md)oder [eine Statusleiste.](ctrl-status-bars.md) Infotips für Infotips im Infobereich sind eine Ausnahme, da sie zum Anzeigen von Statusinformationen verwendet werden können.
-   **Müssen die Benutzer mit den Informationen interagieren?** Verwenden Sie in diesem Beispiel ein anderes Steuerelement, z. B. eine Sprechblase. Eine Benutzerinteraktion mit QuickInfo ist nicht möglich, da die Informationen beim Bewegen der Maus ausgeblendet werden.
-   **Müssen Benutzer die zusätzlichen Informationen drucken?** Verwenden Sie in diesem Beispiel ein anderes Steuerelement, z. B. ein statisches Kommentarfeld. Sie können jedoch auch Infotips verwenden, um einen direkteren Zugriff auf diese Informationen zu ermöglichen.

    ![Screenshot des Kommentarsprechblasens ](images/ctrl-tooltips-and-infotips-image3.png)

    In diesem Beispiel ermöglicht ein statisches Kommentarfeld in Microsoft Word Benutzern das Drucken von Kommentaren.

-   **Ist der Kontext so, dass Benutzer die Tipps möglicherweise störend oder störend finden?** Wenn dies der Problem ist, sollten Sie eine andere Lösung in Betracht ziehen, die auch gar nichts macht. Wenn Sie Tipps in solchen Kontexten verwenden, erlauben Sie Benutzern, sie zu deaktivieren.

Bei entsprechender Verwendung verbessern Tipps die Kommunikation mit dem Benutzer. **Verwenden Sie niemals Tipps als Ersatz für einen guten Entwurf.** Wenn eine Grafik, Schaltfläche oder ein anderes Objekt erfordert, dass Benutzer weiterhin einen Tipp überprüfen, um es zu verstehen, ist der Entwurf schlecht. Korrigieren Sie stattdessen den Entwurf.

## <a name="design-concepts"></a>Entwurfskonzepte

Tipps sind eine leistungsstarke Möglichkeit, eine Benutzeroberfläche zu vereinfachen. Sie stellen Informationen zur Verfügung, die Benutzer benötigen, wenn sie sie benötigen, mit minimalem Aufwand. Tipps können Ihnen helfen, den Bildschirmbereich effektiver zu nutzen und die Bildschirmübersicht zu reduzieren. Schlecht entworfene Tipps können jedoch störend, störend, nicht hilfreich, überforderlich oder im Weg sein. Die folgenden Entwurfskonzepte sollen den Unterschied zeigen.

### <a name="discoverability"></a>Erkennbarkeit

Tipps automatisch angezeigt, wenn Benutzer für einen bestimmten Zeitraum mit dem Zeiger auf ein Objekt zeigen. Dieser Mechanismus zur Zeitverzögerung macht Tipps sehr praktisch, verringert aber auch deren Aufholbarkeit.

Im Laufe der Zeit erfahren Benutzer, dass bestimmte Standardobjekte wie Symbolleistenschaltflächen, Grafikschaltflächen, Startmenü-Elemente und Benachrichtigungsbereichssymbole Tipps enthalten, damit Sie ihre Aufholbarkeit als selbstverständlich einsieht.

Es dauert länger, bis Benutzer Tipps an nicht standardmäßigen Stellen finden. Es gibt keinen visuellen Hinweis, z. B. eine Hot Spot- oder Zeigeränderung, die darauf hindeutet, dass ein Objekt über ein Trinkgeld verfügt. Noch schlechter ist, dass einige Benutzer die Maus viel bewegen, insbesondere wenn sie lernen, auf der Benutzeroberfläche zu navigieren. Benutzer müssen wissen, dass ein Objekt ein Trinkgeld hat, entweder durch frühere Erfahrungen oder durch Experimentieren.

Sie können die Aufholbarkeit verbessern, indem Sie Tipps konsistent verwenden, was wiederum die Vorhersagbarkeit fördert. Wenn Sie Tipps für einige Objekte bereitstellen, sollten Sie sie für alle ähnlichen Objekte bereitstellen, für die Benutzer wahrscheinlich zusätzliche Informationen wünschen. Manchmal kann dies schwierig sein, da Sie auch sicherstellen müssen, dass die Tipps hilfreich und nicht offensichtlich sind.

Wenn sich die Bereitstellung erkennbarer, durchgängig hilfreicher Tipps als Problem erweist, sollten Sie alternative Entwürfe in Betracht ziehen, z. B. selbsterklärende Steuerelementbezeichnungen oder in-place supplemental text.

### <a name="appropriate-information"></a>Geeignete Informationen

Informationen, die für Tipps geeignet sind, haben die folgenden Merkmale:

-   **Prägnant.** Die von Tipps verwendeten Popupfenster sind perfekt für kurze Sätze und Satzfragmente sowie für formatierten Text geeignet. Große, unformatierte Textblöcke sind schwer zu lesen und überfordernd.
-   **Hilfreich.** Tipptext muss informativ sein. Es sollte nicht offensichtlich sein oder einfach wiederholen, was sich bereits auf dem Bildschirm befindet.
-   **Zusätzliche.** Da Trinkgeldtext nicht immer sichtbar ist, sollten es sich um zusätzliche Informationen handelt, die Benutzer nicht lesen müssen. Wichtige Informationen sollten mit selbsterklärenden Steuerelementbezeichnungen oder direkt ergänzendem Text kommuniziert werden.
-   **Statische.** Benutzer erwarten nicht, dass sich Tipps von einer Instanz zur nächsten ändern, sodass sie wahrscheinlich keine Änderungen an dynamischen Inhalten bemerken, z. B. Statusinformationen. Symboltipps für den Infobereich sind eine wichtige Ausnahme: Benutzer werden dort eher Änderungen an Trinkgeldinformationen feststellen, da diese Symbole in erster Linie den Status kommunizieren.

### <a name="appropriate-timeouts"></a>Geeignete Timeouts

Die entsprechende automatische Anzeige und Entfernung von Tipps ist entscheidend für das Ziel, dass Benutzer die Kontrolle über ihre Benutzeroberflächenumgebung aufrechterhalten. Tipps drei Timeoutwerte:

-   **Ersten.** Die Zeit, in der der Zeiger fest bleiben muss, damit das Trinkgeld angezeigt wird. Die Standardzeit beträgt 0,5 Sekunden.
-   **Erneutes Anzeigen.** Die Zeit, zu der der Zeiger bei der Bewegung des Zeigers von einem Ziel zu einem anderen unverändert bleiben muss. Die Standardzeit beträgt 0,1 Sekunden.
-   **Entfernung.** Die Zeit, nach der das Trinkgeld automatisch entfernt wird. Die Standardzeit beträgt 5 Sekunden.

Zu kurze Anfangs- und Neuinszenswerte führen zu einer lästig und störenden Erfahrung, da sie häufig versehentlich angezeigt werden, während zu lange Tipps dazu führen, dass sie nicht reagieren oder nicht entdeckt werden. Die Standardentfernungszeit funktioniert gut für kurzen Trinkgeldtext, wie er in QuickInfos verwendet wird. Infotips haben längeren Text, sodass sie längere Anzeigezeiten benötigen.

### <a name="appropriate-placement"></a>Geeignete Platzierung

Tipps sollte in der Nähe des Objekts platziert werden, auf das zeigen wird, in der Regel am Ende oder Kopf des Zeigers, wenn möglich. Sie sollten jedoch nie auf eine Weise platziert werden, die das Verhalten des Benutzers beeinträchtigt, indem das objekt von Interesse verdeckt wird. Um dieses Problem zu verhindern, müssen Sie möglicherweise die Spitze vom Zeiger weg bewegen, aber angrenzend an das Objekt. Dies ist kein Problem, solange die Beziehung zwischen dem Objekt und dessen Trinkgeld klar ist. Stellen Sie sicher, dass Benutzer den Zeiger nicht nur bewegen, um die Tipps Ihres Programms zu erhalten, um fortzugehen.

### <a name="accessibility"></a>Zugriff

Tipps haben ungewöhnliche Auswirkungen auf die Barrierefreiheit. Während sie normalerweise ausgelöst werden, indem sie mit dem Mauszeiger auf ein Objekt zeigen, werden Tipps von [Sprachausgaben](inter-accessibility.md) für Steuerelemente mit Tastaturzugriff behandelt. Bei geeigneter Verwendung für präzise, hilfreiche, statische, ergänzende Informationen können Tipps die allgemeine Barrierefreiheit verbessern. Tatsächlich ist das Alttexttippmuster die bevorzugte Methode, um Grafiken zugänglich zu machen. Wenn sie jedoch nicht angemessen verwendet werden, beeinträchtigen sie die Barrierefreiheit, da wichtige oder dynamische Informationen schwieriger zu erhalten sind.

Stellen Sie mehr als eine Möglichkeit bereit, auf ein Steuerelement zuzugreifen, wenn für dieses Steuerelement ein Tipp ohne Tastaturzugriff erforderlich ist.

![Screenshot der Druckschaltfläche mit QuickInfo ](images/ctrl-tooltips-and-infotips-image4.png)

In diesem Beispiel können Benutzer mithilfe der Symbolleistenschaltfläche (auf die nicht über die Tastatur zugegriffen werden kann) oder der Tastenkombination Befehl drucken drucken drucken.

**Wenn Sie nur eine Sache durchführen...**

Entwerfen Sie erkennbare Tipps, die präzise, hilfreiche, statische, ergänzende Informationen zum richtigen Zeitpunkt an der entsprechenden Stelle anzeigen.

## <a name="usage-patterns"></a>Verwendungsmuster

Tipps haben mehrere Verwendungsmuster:



|    Verwendung                                                                                                                             |    Beispiel                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **QuickInfos**<br/> zeigt die Bezeichnung eines Steuerelements oder Glyphens ohne Bezeichnung an. <br/>                                         | Da diese Tipps als Bezeichnungen dienen, folgt ihr Text den Bezeichnungsrichtlinien für das zugrunde liegende Steuerelement. <br/> ![Screenshot der Schaltfläche "Liste exportieren" mit QuickInfo ](images/ctrl-tooltips-and-infotips-image5.png)<br/> In diesem Beispiel gibt die QuickInfo die Befehlsbezeichnung an.<br/> ![Screenshot der Schaltfläche "Schließen" mit QuickInfo ](images/ctrl-tooltips-and-infotips-image6.png)![Screenshot der Wiedergabeschaltfläche mit QuickInfo ](images/ctrl-tooltips-and-infotips-image7.png)<br/> In diesen Beispielen bezeichnen QuickInfos grafische Schaltflächen.<br/> ![Screenshot des Menüglyphens "Show" mit QuickInfo ](images/ctrl-tooltips-and-infotips-image8.png)<br/> In diesem Beispiel bezeichnet die QuickInfo ein Glyphen.<br/> |
| **Infotips**<br/> Geben Sie eine ergänzende Beschreibung oder Erklärung eines Objekts oder Steuerelements an. <br/>                  | Verwenden Sie Infotips, um Objekte und Steuerelemente wie [Symbolleistensteuerelemente,](cmd-toolbars.md) [Symbole](vis-icons.md) (einschließlich Symbolüberlagerungen), [Links,](ctrl-links.md) [Registerkarten,](ctrl-tabs.md)Steuerelemente für die progressive [Offenlegung](ctrl-progressive-disclosure-controls.md)und benutzerdefinierte Steuerelemente zu beschreiben oder zu erklären. <br/> ![Screenshot der E-Mail-Schaltfläche mit Infotip ](images/ctrl-tooltips-and-infotips-image9.png)<br/> ![Screenshot der Schaltfläche "Burn" mit Infotip ](images/ctrl-tooltips-and-infotips-image10.png)<br/> In diesen Beispielen bieten Infotips zusätzliche Informationen zu Steuerelementen und Objekten.<br/>                                                                                        |
| **Alttextinfotips**<br/> beschreiben sie eine Grafik für die Barrierefreiheit. <br/>                                              | Dieses Muster ist in erster Linie für Benutzer vorgesehen, die eine Sehbehinderung haben und möglicherweise eine Sprachausgabe verwenden. <br/> ![Screenshot der Windows-Startschaltfläche mit Infotip ](images/ctrl-tooltips-and-infotips-image11.png)<br/> In diesem Beispiel beschreibt die Infotip die Startmenü Grafik.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Miniaturansicht**<br/> zeigt ein kleines Bild eines Elements an. <br/>                                                         | Miniaturansichten bieten eine leicht erkennbare grafische Darstellung eines Fensters oder Dokuments. <br/> ![Screenshot der Miniaturansicht der Systemsteuerungskategorien ](images/ctrl-tooltips-and-infotips-image12.png)<br/> In diesem Beispiel gibt die Windows-Taskleiste Miniaturansichttipps für ihre Elemente.<br/> ![Screenshot der Miniaturansicht des Fotos und der zugehörigen Daten ](images/ctrl-tooltips-and-infotips-image13.png)<br/> In diesem Beispiel gibt Windows Fotogalerie Miniaturansichttipps für seine Elemente.<br/>                                                                                                                                                                                                                      |
| **Infotips für Details**<br/> zeigt detaillierte Informationen zu einem Objekt an. <br/>                                        | Infotips sind eine effektive Möglichkeit, detaillierte Informationen zu einem Objekt anzuzeigen oder Daten bereitzustellen. <br/> ![Screenshot der Infotipinfo des Fotos mit Dateityp ](images/ctrl-tooltips-and-infotips-image14.png)![Screenshot des Diagramms mit Infotip-Detailwerten ](images/ctrl-tooltips-and-infotips-image15.png)<br/> In diesen Beispielen enthalten Infotips ausführliche Informationen zu einem Objekt oder zu Daten.<br/>                                                                                                                                                                                                                                                                                                      |
| **Infotips im Startmenü**<br/> beschreiben sie ein Element im Startmenü. <br/>                                              | Das Startmenü besteht aus Programmnamen und wichtigen Windows-Zielen wie Dokumenten, Bildern und Systemsteuerung. Diese Tipps beschreiben Startmenüelemente, in der Regel durch eine kurze Beschreibung des Programms oder Ziels sowie der primären Aufgaben, die Benutzer damit ausführen können. Diese Beschreibungen werden auch über das Suchfeld des Startmenüs indiziert, um Benutzern die Suche nach den programmen zu ermöglichen, die sie benötigen. <br/> ![Screenshot der Infotip zum Welcome Center ](images/ctrl-tooltips-and-infotips-image16.png)<br/> In diesem Beispiel wird in der Infotip beschrieben, welche Möglichkeiten Benutzer mit einem Programm im Startmenü haben.<br/>                                                                                    |
| **Systemsteuerung Infotips**<br/> beschreiben eine Systemsteuerungskategorie oder -aufgabe. <br/>                                    | Diese Tipps enthalten zusätzliche Informationen, mit denen Benutzer die richtige Systemsteuerungskategorie und das richtige Element auswählen können. <br/> ![Screenshot der Kategorie "Benutzerkonten" mit Infotip ](images/ctrl-tooltips-and-infotips-image17.png)<br/> In diesem Beispiel beschreibt die Infotip die Kategorie Benutzerkonten Systemsteuerung.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| **Infotips für vollständige Namen**<br/> zeigt den vollständigen Namen eines Elements an, wenn der Name abgeschnitten oder nicht vollständig sichtbar ist. <br/> | Mit diesen Tipps können Sie Elemente in einem kompakteren Bereich anzeigen und gleichzeitig den Bedarf an horizontalem Scrollen reduzieren. dies ist besonders wichtig, wenn die Inhaltslänge unbekannt ist, da sie dynamisch ist. Im Gegensatz zu den anderen Mustern werden diese Tipps bei Verwendung in Listen und Strukturen direkt über dem Quellobjekt angezeigt. <br/> ![Screenshot der Infotip zum Gruppentitel des Optionsfelds ](images/ctrl-tooltips-and-infotips-image18.png)<br/> In diesem Beispiel wird ein Infotip verwendet, um den vollständigen Elementnamen beim Zeigen anzuzeigen.<br/>                                                                                                                                                                                     |
| **Statusinfos**<br/> Anzeigen von Statusinformationen für Benachrichtigungsbereichssymbole. <br/>                              | Normalerweise sollten Tipps statisch sein, da Benutzer nicht erwarten, dass sie von einer Instanz zur nächsten wechseln. **Symbole im Infobereich stellen eine Ausnahme** dar, da diese Symbole den Status kommunizieren und kein anderer Bildschirmbereich für Statustext verfügbar ist. <br/> ![Screenshot der Infoinfo "Messenger nicht angemeldet" ](images/ctrl-tooltips-and-infotips-image19.png)<br/> ![Screenshot des Infotips "Messenger signed in" ](images/ctrl-tooltips-and-infotips-image20.png)<br/> In diesen Beispielen enthalten Infotips Statusinformationen für Symbole im Benachrichtigungsbereich.<br/>                                                                                                                                  |



 

## <a name="guidelines"></a>Richtlinien

### <a name="timeouts"></a>Zeitlimits

-   **Verwenden Sie die Standardtimeouts für die Erst- und Neuanzeige. Ausnahme:**
    -   Miniaturansichten, die nicht redundant sind und auf der Seite ihres zugeordneten Objekts angezeigt werden, können sofort (ohne Verzögerung) angezeigt werden. Verwenden Sie jedoch das anfängliche Standardtimeout für redundante Miniaturansichten (z. B. einen großen Miniaturansichtstipp für ein kleines Grafikobjekt) oder Miniaturansichten, die das zugehörige Objekt abdecken.
-   **Verwenden Sie für QuickInfos das Standardmäßige Timeout für das Entfernen von Fünf-Sekunden-Trinkgeld.**
-   Deaktivieren Sie für **Infotips das Timeout zum Entfernen von Trinkgeld. Entwickler:** Da Sie das Entfernungstimeout technisch nicht deaktivieren können, legen Sie es auf den größten Wert fest.
-   Wenn Sie für die Barrierefreiheit die Timeoutwerte auf einen anderen Wert als den Maximalwert festlegen müssen, machen Sie sie zu einem Vielfachen der Systemparameter SPI \_ GETMOUSEHOVERTIME und SPI \_ GETMESSAGEDURATION, anstatt feste Zeiten zu verwenden. Dadurch werden die Timeouts an die Geschwindigkeit des Benutzers angepasst.

### <a name="placement"></a>Platzierung

-   **Vermeiden Sie das Abdecken des Objekts, das der Benutzer anzeigen oder mit dem er interagieren soll.** Platzieren Sie den Tipp immer auf der Seite des Objekts, auch wenn dies eine Trennung zwischen zeiger und tip erfordert. Eine Trennung ist kein Problem, solange die Beziehung zwischen dem Objekt und seinem Trinkgeld klar ist.

    -   **Ausnahme:** QuickInfos mit vollständigem Namen, die in Listen und Strukturen verwendet werden.

    **Falsch:**

    ![Screenshot der Infoinfo, die das Suchfeld verdeckt ](images/ctrl-tooltips-and-infotips-image21.png)

    **Richtig:**

    ![Screenshot der infotip unterhalb des Suchfelds ](images/ctrl-tooltips-and-infotips-image22.png)

    Im richtigen Beispiel wird die Infotip vom Suchfeld entfernt platziert, obwohl dafür Platz zwischen dem Text und dem Caretfeld erforderlich ist.

    **Falsch:**

    ![Screenshot der Infotip, der überarbeiteten Text verdeckt ](images/ctrl-tooltips-and-infotips-image23.png)

    **Richtig:**

    ![Screenshot der Infotip über dem überarbeiteten Text ](images/ctrl-tooltips-and-infotips-image24.png)

    Im richtigen Beispiel ist der zugrunde liegende Text viel nützlicher als der Tipp, sodass die Infotip weit davon entfernt ist.

-   **Vermeiden Sie bei Auflistungen von Elementen das Abdecken des nächsten Objekts, das der Benutzer wahrscheinlich anzeigen oder mit dem er interagieren wird.** Vermeiden Sie bei horizontal angeordneten Elementen das Platzieren von Tipps auf der rechten Seite. Für vertikal angeordnete Elemente vermeiden Sie das Platzieren von Tipps unten.

    **Falsch:**

    ![Screenshot der Infotip, die die Liste der zuletzt veröffentlichten Elemente verdeckt ](images/ctrl-tooltips-and-infotips-image25.png)

    **Richtig:**

    ![Screenshot der Infoinfo neben der Liste der zuletzt veröffentlichten Elemente ](images/ctrl-tooltips-and-infotips-image26.png)

    Im falschen Beispiel deckt der Tipp das Objekt ab, mit dem der Benutzer wahrscheinlich als Nächstes interagiert.

-   **Stellen Sie für potenziell ablenkende (oft große) Tipps sicher, dass die Informationen für die meisten Benutzer hilfreich sind.** Wenn dies nicht der Fall ist, machen Sie die ablenkenden Tipps optional, oder beseitigen Sie sie sogar. Andernfalls müssen die meisten Benutzer den Zeiger vom Zielobjekt weg bewegen, um das Trinkgeld zu entfernen.

### <a name="tooltips"></a>QuickInfos

-   **Verwenden Sie QuickInfos, um Bezeichnungen für Steuerelemente ohne Bezeichnung bereitzustellen.** Steuerelemente, die häufig QuickInfos aufweisen, sind [Symbolleistenschaltflächen,](cmd-toolbars.md)Grafikschaltflächen und Steuerelemente für [die progressive Offenlegung.](ctrl-progressive-disclosure-controls.md) Steuerelemente mit Eingabeaufforderungen werden als bezeichnet betrachtet, z. B. [Textfelder](ctrl-text-boxes.md) und [Kombinationsfelder.](/windows/desktop/uxguide/ctrl-drop) Alle anderen Steuerelemente sollten explizite Bezeichnungen aufweisen.
-   Verwenden Sie Satzfragmente ohne Beenden der Interpunktion.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
    -   **Ausnahme:** Diese Richtlinie ist für Windows Vista neu. Bei älteren Anwendungen können Sie bei Bedarf großgeschriebene Titel verwenden, um die Kombination von Groß-/Großschreibungsstilen zu vermeiden.
-   Fügen Sie eine [Auslassungszeichen](ctrl-command-buttons.md) hinzu, wenn die Bezeichnung für einen Befehl vorgesehen ist, der zusätzliche Informationen benötigt.
-   **Halten Sie QuickInfos** wie bei normalen Bezeichnungen in der Regel mindestens fünf Wörter kurz, bevorzugen sie jedoch bestimmte Bezeichnungen gegenüber ungenauen.

    **Annehmbar:**

    ![Screenshot der QuickInfo zum Drucken ](images/ctrl-tooltips-and-infotips-image27.png)

    **Besser:**

    ![Screenshot der QuickInfo "Auf Standarddrucker drucken" ](images/ctrl-tooltips-and-infotips-image28.png)

    **Beste:**

    ![Screenshot der QuickInfo "Print (Document Writer)" ](images/ctrl-tooltips-and-infotips-image29.png)

    **Falsch:**

    ![Screenshot der ausführlichen QuickInfo ](images/ctrl-tooltips-and-infotips-image30.png)

    In diesen Beispielen ist das beste Beispiel sowohl präzise als auch spezifisch, während das falsche Beispiel unnötig ausführlich ist.

-   **QuickInfos können auch ausführlichere Informationen für beschriftete Symbolleistenschaltflächen bereitstellen, wenn dies hilfreich ist.** Wiederholen Sie nicht einfach das, was bereits in der Bezeichnung vorhanden ist, oder geben Sie eine wortliche Neustellung an.

    **Richtig:**

    ![Screenshot der QuickInfo "Search all outlook" ](images/ctrl-tooltips-and-infotips-image31.png)

    In diesem Beispiel wird in der QuickInfo erläutert, was Die Suche ausführt.

    **Falsch:**

    ![Screenshot der sich wiederholenden QuickInfo-Schaltflächenbeschriftung ](images/ctrl-tooltips-and-infotips-image32.png)

    In diesem Beispiel wiederholt die QuickInfo nur, was bereits in der Bezeichnung vorhanden ist.

-   **Aus Gründen der Konsistenz müssen Sie keine QuickInfos für beschriftete Steuerelemente geben.**

    ![Screenshot von beschrifteten und nicht bezeichneten Schaltflächen ](images/ctrl-tooltips-and-infotips-image33.png)

    In diesem Beispiel verfügen die nicht bezeichneten Symbolleistenschaltflächen über QuickInfos, aber die beschrifteten Schaltflächen nicht.

-   Machen Sie QuickInfos ggf. **hilfreicher, indem Sie Tastenkombinationen und Standardwerte bereitstellen.** Setzen Sie diese zusätzlichen Informationen in Klammern. Auf diese Weise sind QuickInfos für beschriftete Steuerelemente hilfreich, auch wenn sie andernfalls nur die Bezeichnung wiederholen. Berücksichtigen Sie diesen zusätzlichen Text nicht, wenn Sie die Prägnanz einer QuickInfo auswerten.

    ![Screenshot der QuickInfo "Print (Document Writer)" ](images/ctrl-tooltips-and-infotips-image29.png)

    In diesem Beispiel zeigt Word Standardwerte und Tastenkombinationen in den QuickInfos der Symbolleiste an.

### <a name="infotips"></a>Infotips

-   **Bei Infotips an stellen, die nicht dem Standard entsprechen, bevorzugen Sie Konsistenz gegenüber Hilfreichkeit, um die Auffindbarkeit zu verbessern.** Geben Sie Tipps für alle Objekte, für die Benutzer wahrscheinlich zusätzliche Informationen benötigen, auch wenn einige Infotips offensichtlich sein können. Dadurch wird vermieden, dass Benutzer auf eine Infotip warten, die nie kommt.
    -   **Ausnahme:** Wenn nur wenige Objekte hilfreiche Infotips haben, verwenden Sie überhaupt keine Infotips. Verwenden Sie stattdessen selbsterklärende Steuerelementbezeichnungen oder ergänzenden Text.
-   Verwenden Sie vollständige Sätze mit endender Interpunktion.
    -   **Ausnahme:** Infotips für [Infotips](winenv-notification.md) des Infobereichs verwenden keine endende Interpunktion.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Verwenden Sie die aktuelle Tense, nicht die Zukunft.
-   Verwenden Sie parallele grammatische Konstruktionen. Parallelität erfordert, dass Wörter und Ausdrücke, die die gleiche Funktion aufweisen, die gleiche Form aufweisen.
    -   **Ausnahme:** Für das Infotipmuster mit vollständigem Namen stimmt der Infotip-Text genau mit dem Ausdruck, der Groß-/Großschreibung und der Interpunktion des zugrunde liegenden Steuerelements überein.
-   **Vermeiden Sie große Infotips.** Große Infotips sind schwer zu lesen und schwer zu positionieren, ohne das zugrunde liegende Objekt zu beeinträchtigen.
-   **Formatieren Sie Infotips, um deren Inhalt einfacher zu lesen und zu überprüfen.** Große Blöcke mit unformatiertem Text können schwierig zu lesen sein.

    **Falsch:**

    ![Screenshot einer langen, unstrukturierten, ausgeführten QuickInfo ](images/ctrl-tooltips-and-infotips-image34.png)

    **Richtig:**

    ![Screenshot der gleichen QuickInfo mit einer Zeile pro Element ](images/ctrl-tooltips-and-infotips-image35.png)

    Im richtigen Beispiel ist der formatierte Text viel einfacher zu lesen und zu scannen.

-   Notieren Sie sich bei der ersten Verwendung in einer Infotip die Namen von Akronymen, gefolgt vom Akronym in Klammern. Beispiel: "Dynamic Host Configuration Protocol (DHCP)."

### <a name="start-menu-infotips"></a>Infotips im Startmenü

-   Verwenden Sie Startmenü Infotips, um das Element präzise zu **beschreiben und die primären Aufgaben aufzulisten, die Benutzer mit dem Element ausführen können.**
-   **Seien Sie hilfreich.** Konzentrieren Sie sich darauf, was Benutzer tun können. Wiederholen Sie nicht einfach den Elementnamen, oder verwenden Sie ihn überhaupt in der Beschreibung.
-   **Seien Sie spezifisch.** Vermeiden Sie generische Verben und catch-all-Ausdrücke wie und andere Aufgaben. Wenn die Informationen wichtig sind, listen Sie sie explizit auf. Gehen Sie andernfalls davon aus, dass Benutzer verstehen, dass nicht alles in den Infotips aufgeführt ist.
-   **Seien Sie präzise.** Verwenden Sie mindestens 25 Wörter. Längere Infotips raten vom Lesen ab.
-   **Beginnen Sie mit einem imperativen Verb mit vorhandener Tense,** z. B. Erstellen, Bearbeiten, Anzeigen und Senden. Bevorzugen Sie bestimmte Verben gegenüber generischen Verben wie verwalten und öffnen, die wirklich für die meisten Startmenü Elemente gelten. Gelangen Sie direkt zu dem Punkt.

    **Falsch:**

    ![Screenshot der QuickInfo: Öffnet den Ordner "music". ](images/ctrl-tooltips-and-infotips-image36.png)

    **Besser:**

    ![Screenshot der QuickInfo: Speichern und Wiedergeben von Musik ](images/ctrl-tooltips-and-infotips-image37.png)

    Im falschen Beispiel beginnt die Infotip mit einem generischen Verb. Das bessere Beispiel kommt mit bestimmten Verben direkt auf den Punkt, verwendet aber weiterhin den unnötigen "and other"-Ausdruck am Ende des Trinkgelds.

-   **Verwenden Sie keine Sprache, die nach Marketing klingt.**

    **Falsch:**

    ![Screenshot der Infoinfo "One-Stop-Startpunkt" ](images/ctrl-tooltips-and-infotips-image38.png)

    In diesem Beispiel klingt der Infotip nach Marketing.

-   Da diese Infotips für das suchfeld Startmenü indiziert sind, beschreiben Sie die **wichtigen Aufgaben Ihres Programms mit Begriffen, nach denen Benutzer am wahrscheinlichsten suchen. Erwägen Sie die Verwendung von Schlüsselwörtern und häufig verwendeten Synonymen.**

    **Falsch:**

    ![Screenshot der QuickInfo: Erstellen von DVD-Dateien ](images/ctrl-tooltips-and-infotips-image39.png)

    **Richtig:**

    ![Screenshot der QuickInfo: Erstellen (Branden) von CDS, DVDS ](images/ctrl-tooltips-and-infotips-image40.png)

    Im richtigen Beispiel hat der Infotip allgemeine Synonyme.

-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   **Entwickler:** Der Startmenü infotip-Text stammt aus dem Kommentarfeld des Elements.

### <a name="quick-launch-tooltips"></a>Schnellstart QuickInfos

-   **Verwenden Sie eine QuickInfo im folgenden Format:** Starten (vollständiger Programmname)
-   Verwenden Sie keine Interpunktion am Ende.
-   Verwenden Sie keinen zusätzlichen Text, um das Programm oder seine Funktionen zu beschreiben. Da Benutzer die programme auswählen, die in der Schnellstart angezeigt werden, kennen sie bereits ihren Zweck.

### <a name="control-panel-infotips"></a>Systemsteuerung Infos

-   Verwenden Systemsteuerung Infotips, um die Systemsteuerung aufgaben und die **konfigurierte Hardware und Software kurz zu beschreiben.**
-   **Systemsteuerung Namen und Symbole müssen Infotips enthalten.** Einzelne Aufgaben verfügen nicht über QuickInfos.
-   **Seien Sie hilfreich.** Konzentrieren Sie sich darauf, was Benutzer tun können. Wiederholen Sie nicht einfach den Systemsteuerung Elementnamen, oder verwenden Sie ihn überhaupt in der Beschreibung.
-   **Seien Sie spezifisch.** Vermeiden Sie generische Verben und catch-all-Ausdrücke wie und andere Hardware. Wenn die Informationen wichtig sind, listen Sie sie speziell auf. Andernfalls wird davon ausgegangen, dass Benutzer verstehen, dass nicht alles in den Infotips aufgeführt ist.

    **Falsch:**

    ![Screenshot der QuickInfo: Konfiguriert die Maus ](images/ctrl-tooltips-and-infotips-image41.png)

    **Richtig:**

    ![Screenshot einer detaillierten QuickInfo für Mauseinstellungen ](images/ctrl-tooltips-and-infotips-image42.png)

    Im richtigen Beispiel werden die konfigurierten Hardwaretypen speziell aufgeführt.

-   **Seien Sie präzise.** Verwenden Sie 25 Wörter oder weniger. Längere Infotips raten vom Lesen ab.
-   **Beginnen Sie mit einem gegenwärtigen, imperativen Verb.**

    **Richtig:**

    Konfigurieren Von Internetanzeige- und Verbindungseinstellungen.

    Passen Sie die Einstellungen für Sehvermögen, Hörvermögen und Mobilität an.

-   **Kommen Sie direkt auf den Punkt.** Verwenden Sie keine Sprache, die für alle Systemsteuerung gilt, z. B. "Verwenden Sie zum Anzeigen und Konfigurieren von Einstellungen für die Darstellung und Funktionalität Ihrer...". oder "Stellt Optionen für Sie zur Verfügung...".
-   Verwenden Sie keine Sprache, die wie Marketing klingt.

    **Falsch:**

    Ihr einmaliger Ausgangspunkt für alle Anforderungen an die Datenträgerkonfiguration.

-   Da diese Infotips für das Suchfeld Systemsteuerung werden, beschreiben Sie Elemente mit Begriffen, nach denen Benutzer am **wahrscheinlichsten suchen.** Erwägen Sie die Verwendung gängiger Synonyme für beliebte Aufgaben und Objekte.

    ![Screenshot der QuickInfo mit Gamecontrolleraufgaben ](images/ctrl-tooltips-and-infotips-image43.png)

    In diesem Beispiel wird das Element mithilfe von Begriffen beschrieben, nach denen Benutzer am wahrscheinlichsten suchen.

-   Wenn ein Systemsteuerung-Element wahrscheinlich mit anderen verwechselt wird, erläutern Sie, wie es sich im Infotip unterscheiden kann.

    **Falsch:**

    ![Screenshot der Infotips ohne bestimmte Details ](images/ctrl-tooltips-and-infotips-image44.png)

    In diesem Beispiel konfigurieren beide Systemsteuerung Sound, aber die Infotips verdeutlichen den Unterschied nicht.

    **Richtig:**

    ![Screenshot der Infotips mit bestimmten Details ](images/ctrl-tooltips-and-infotips-image45.png)

    In diesem Beispiel ist der Unterschied zwischen den beiden Elementen aufgrund des Trinkgelds offensichtlicher.

### <a name="icons"></a>Symbole

Im Gegensatz zu früheren Versionen von Windows ermöglicht Windows Vista, dass Tipps Symbole enthalten.

-   Verwenden Sie für QuickInfos keine Symbole.
-   Verwenden Sie Für Infotips Symbole nur, wenn sie bei der Erkennung oder beim Verständnis helfen oder Kontext bereitstellen. Die meisten Infotips sollten keine Symbole enthalten.

    ![Screenshot der Volumeinfo mit Symbol "Icon" ](images/ctrl-tooltips-and-infotips-image46.png)

    In diesem Beispiel verfügt der Infotip über ein Symbol, um das Symbol mit seiner Bedeutung zu verknüpfen.

-   Für das Symbol muss [der Stil Des-Stils verwendet](vis-icons.md) werden, und das Symbol muss unaufdringlich aussehen.

Allgemeine Symbolrichtlinien und Beispiele finden Sie unter [Symbole](vis-icons.md).

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Tipps:

-   Informationen zur Art des Trinkgelds (QuickInfo oder Infotip) finden Sie in der Programmierung und anderen technischen Dokumentationen. Überall sonst können Sie es einfach als Tipp bezeichnen.
-   Die folgenden Varianten sind falsch: QuickInfo, QuickInfo und QuickInfo.
-   Um die Benutzerinteraktion zu beschreiben, verwenden Sie den Hover.

