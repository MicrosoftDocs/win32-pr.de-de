---
title: Layout
description: Layout ist die Größe, der Abstand und die Platzierung von Inhalten innerhalb eines Fensters oder einer Seite.
ms.assetid: 39cd896f-d3cc-4768-a20c-a7f598da7136
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8577843f3e54744cabe970e3b9132df1d9fb45df
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444881"
---
# <a name="layout"></a>Layout

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere aktuelle [Entwurfsanleitung wider.](/windows/uwp/design/)

Layout ist die Größe, der Abstand und die Platzierung von Inhalten innerhalb eines Fensters oder einer Seite. Effektives Layout ist entscheidend, um Benutzern dabei zu helfen, schnell zu finden, was sie suchen, und die Darstellung visuell ansprechender zu gestalten. Ein effektives Layout kann den Unterschied zwischen Entwürfen, die Benutzer sofort verstehen, und Entwürfen, bei denen benutzer sich überfordert und überfordert fühlen.

**Hinweis:** Richtlinien im Zusammenhang [mit der Fensterverwaltung](win-window-mgt.md) werden in einem separaten Artikel vorgestellt. Empfohlene spezifische Größen- und Abstandswerte für Steuerelementen finden Sie in den entsprechenden Richtlinienartikeln.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="visual-hierarchy"></a>Visuelle Hierarchie

Ein Fenster oder eine Seite verfügt über eine klare visuelle Hierarchie, wenn ihre Darstellung die Beziehung und Priorität ihrer Elemente angibt. Ohne eine visuelle Hierarchie müssten Benutzer diese Beziehungen und Prioritäten selbst herausfinden.

Die visuelle Hierarchie wird erreicht, indem die folgenden Attribute gekonnt kombiniert werden:

-   **Fokus.** Das Layout gibt an, wo Benutzer zuerst suchen müssen.
-   **Fluss.** Das Auge fließt reibungslos und natürlich durch einen klaren Pfad durch die Oberfläche und findet Benutzeroberflächenelemente in der für ihre Verwendung geeigneten Reihenfolge.
-   **Gruppierung.** Logisch verknüpfte Benutzeroberflächenelemente haben eine klare visuelle Beziehung. Verknüpfte Elemente werden miteinander verbunden. Nicht verknüpfte Elemente sind getrennt.
-   **Schwerpunkt.** Benutzeroberflächenelemente werden basierend auf ihrer relativen Wichtigkeit hervorgehoben.
-   **Ausrichtung.** Die Benutzeroberflächenelemente verfügen über eine koordinierte Platzierung, sodass sie leicht gescannt und geordnet angezeigt werden können.

Darüber hinaus verfügt das effektive Layout über die folgenden Attribute:

-   **Geräteunabhängigkeit.** Das Layout wird wie beabsichtigt angezeigt, unabhängig von Schriftart oder Schriftgrad, Punkt pro Zoll (DPI), Anzeige oder Grafikadapter.
-   **Einfach zu scannen.** Benutzer finden die gesuchten Inhalte auf einen Blick.
-   **Effizienz.** Benutzeroberflächenelemente, die groß sind, müssen groß sein, und kleine Elemente sind sehr klein.
-   **Größe der Größe.** Wenn dies hilfreich ist, kann die Größe eines Fensters geändert werden, und sein Inhaltslayout ist unabhängig davon, wie groß oder klein die Oberfläche ist, effektiv.
-   **Gleichgewicht.** Der Inhalt wird gleichmäßig auf die Oberfläche verteilt angezeigt.
-   **Visuelle Einfachheit.** Die Wahrnehmung, dass ein Layout nicht komplizierter ist, als es sein muss. Benutzer sind von der Darstellung des Layouts nicht überfordert.
-   **Konsistenz.** Ähnliche Fenster oder Seiten verwenden ein ähnliches Layout, sodass benutzer sich immer orientieren.

Während Größe, Abstand und Platzierung einfache Konzepte sind, besteht die Herausforderung beim Layout darin, die richtige Mischung dieser Attribute zu erreichen.

Unter Windows wird das Layout mit geräteunabhängigen Metriken wie Dialogeinheiten (DLUs) und relativen Pixeln kommuniziert.

### <a name="a-design-model-for-reading"></a>Ein Entwurfsmodell zum Lesen

**Benutzer wählen aus, was sie nach Darstellung und Organisation des Inhalts lesen.** Um ein effektives Layout zu erstellen, müssen Sie verstehen, was Benutzer tendenziell lesen und warum.

Sie können Layoutentscheidungen treffen, indem Sie dieses Entwurfsmodell zum Lesen verwenden:

-   Die Menschen lesen in der Reihenfolge von links nach rechts, von oben nach unten (in den Kulturen des Westens).
-   Es gibt zwei Lesemodi: immersives Lesen und Scannen. Das Ziel des immersiven Lesens ist das Verständnis.

    ![Abbildung des roten Pfeils im Zickzack-Lesemuster ](images/vis-layout-image1.png)

    Dieses Diagramm modelliert immersives Lesen.

    Im Gegensatz dazu besteht das Ziel der Überprüfung in der Suche nach Dingen. Der gesamte Scanpfad sieht wie hier aus:

    ![Abbildung des roten Pfeils im diagonalen Lesemuster ](images/vis-layout-image2.png)

    In diesem Diagramm wird die Überprüfung modelliert.

    ![Abbildung eines roten Pfeils in einem Ab- und Bogenmuster ](images/vis-layout-image3.png)

    Wenn text am linken Rand einer Seite ausgeführt wird, scannen Benutzer zuerst den linken Rand.

-   Bei der Verwendung von Software werden Benutzer nicht in der Benutzeroberfläche selbst, sondern in ihrer Arbeit versunken. Daher lesen Benutzer in der Regel keinen Text der Benutzeroberfläche, den sie scannen. Anschließend lesen sie Textteile nur dann umfassend, wenn sie der Meinung sind, dass sie dies benötigen.
-   Benutzer überspringen in der Regel Navigationsbereich auf der linken oder rechten Seite einer Seite. Benutzer erkennen, dass sie dort sind, sehen sich navigationsfenster jedoch nur an, wenn sie navigieren möchten.
-   Benutzer neigen dazu, große Blöcke von unformatiertem Text zu überspringen, ohne sie überhaupt zu lesen.

    ![Abbildung von Text mit Pfeilen, die Scantext anzeigen ](images/vis-layout-image4.png)

    Benutzer überspringen bei der Überprüfung tendenziell große Text- und Navigationsbereichsblöcke.

-   Alle Dinge sind gleich: Benutzer sehen sich zuerst in der oberen linken Ecke eines Fensters an, überprüfen die Seite und beenden ihren Scan in der unteren rechten Ecke. Sie ignorieren in der Regel die untere linke Ecke.

    ![Abbildung der Seite und des Pfeils von oben links nach unten nach rechts ](images/vis-layout-image5.png)

    Wenn alles gleich ist, lesen Benutzer diese Zahlen in der folgenden Reihenfolge: 1, 2, 4 und 3.

-   Aber in der interaktiven Benutzeroberfläche sind nicht alle Dinge gleich, sodass verschiedene Benutzeroberflächenelemente unterschiedliche Aufmerksamkeit erhalten. Benutzer tendieren dazu, interaktive Steuerelemente zu betrachten, insbesondere Steuerelemente in der oberen linken und mitte des Fensters und zuerst den prominenten Text.

![Abbildung des Bildschirms mit spitzem und unscharfem Text ](images/vis-layout-image6.png)

Benutzer konzentrieren sich auf die wichtigsten interaktiven Steuerelemente und die prominente Hauptanweisung und sehen sich andere Dinge nur an, wenn sie dies benötigen.

-   Benutzer tendieren dazu, interaktive Steuerelementbezeichnungen zu lesen, insbesondere solche, die für die Durchführung der jeweiligen Aufgabe relevant erscheinen. Im Gegensatz dazu tendieren Benutzer dazu, statischen Text nur zu lesen, wenn sie der Meinung sind, dass sie dies benötigen.
-   Elemente, die anders angezeigt werden, ziehen Aufmerksamkeit auf sich. Fetter Text und großer Text hebt sich von normalem Text ab. Benutzeroberflächenelemente mit Farbe oder farbigem Hintergrund zeichnen sich aus. Elemente mit Symbolen zeichnen sich durch Elemente ohne Symbole aus.
-   Benutzer scrollen nur, wenn sie einen Grund dafür haben. Wenn der Inhalt [über dem Fold](glossary.md) keinen Grund für einen Bildlauf bietet, ist dies nicht der Grund.
-   Nachdem benutzer sich entschieden haben, was sie tun möchten, beenden sie sofort die Überprüfung und tun dies.
-   Da Benutzer die Überprüfung beenden, wenn sie der Meinung sind, dass sie fertig sind, ignorieren sie in der Regel alles, was als Abschlusspunkt erscheint.

![Screenshot der Tastaturoptionen ](images/vis-layout-image7.png)

Benutzer beenden die Überprüfung, wenn sie der Meinung sind, dass sie fertig sind.

Natürlich gibt es Ausnahmen für dieses allgemeine Modell. Eyetrackinggeräte deuten darauf hin, dass das Verhalten der echten Benutzer recht unanst dubst. Das Ziel dieses Modells ist es, Ihnen dabei zu helfen, gute Entscheidungen und Vor- und Abschlüsse zu treffen, nicht das Benutzerverhalten genau zu modellieren. Aber wenn Sie diese Liste gelesen haben, haben Sie hoffentlich auch viele Ihrer eigenen Lesemuster erkannt.

### <a name="designing-for-scanning"></a>Entwerfen für die Überprüfung

**Benutzer lesen nicht, sie scannen, sodass Sie Benutzeroberflächenoberflächen für die Überprüfung entwerfen sollten.** Gehen Sie nicht davon aus, dass Benutzer den Text in der Reihenfolge von links nach rechts von oben nach unten lesen, sondern die Benutzeroberflächenelemente betrachten, die ihre Aufmerksamkeit auf sich ziehen.

So entwerfen Sie die Überprüfung:

-   Angenommen, Benutzer beginnen damit, das gesamte Fenster schnell zu scannen und dann die Benutzeroberflächenelemente in ungefähr der folgenden Reihenfolge zu lesen:
    -   Interaktive Steuerelemente in der Mitte
    -   Die Commitschaltflächen
    -   Interaktive Steuerelemente an anderer Stelle
    -   Main-Anweisung
    -   Ergänzende Erläuterungen
    -   Text, der mit einem Warnsymbol angezeigt wird
    -   Fenstertitel
    -   Anderer statischer Text im Haupttext
    -   Fußnoten
-   Platzieren Sie Benutzeroberflächenelemente, die eine Aufgabe initiieren, in der oberen linken Ecke oder in der oberen Mitte.
-   Platzieren Sie Benutzeroberflächenelemente, die eine Aufgabe abschließen, in der unteren rechten Ecke.
-   Legen Sie nach Möglichkeit wichtigen Text auf interaktive Steuerelemente statt auf statischen Text fest.
-   Vermeiden Sie es, wichtige Informationen in der unteren linken Ecke oder am unteren Rand eines langen bildlauffähigen Steuerelements oder einer seite zu setzen.
-   Stellen Sie keine großen Textblöcke dar. Vermeiden Sie unnötigen Text. Verwenden Sie den [invertierten](text-ui.md) Pyramidenpräsentationsstil.
-   Wenn Sie etwas unternehmen, um die Aufmerksamkeit der Benutzer zu gewinnen, stellen Sie sicher, dass die Aufmerksamkeit gerechtfertigt ist.

Arbeiten Sie nach Möglichkeit mit diesem Modell, anstatt es zu schlagen. Es gibt jedoch Zeiten, in denen Sie bestimmte Benutzeroberflächenelemente entweder hervorheben oder deren Hervor hebt.

So heben Sie primäre Benutzeroberflächenelemente hervor:

-   Legen Sie primäre Benutzeroberflächenelemente im [Scanpfad ab.](glossary.md)
-   Legen Sie eine beliebige Benutzeroberfläche ein, um eine Aufgabe in der oberen linken Ecke oder in der oberen Mitte zu initiieren.
-   Legen Sie commit-Schaltflächen in der unteren rechten Ecke ein.
-   Legen Sie die verbleibende primäre Benutzeroberfläche in den Mittelpunkt.
-   Verwenden Sie Steuerelemente, die aufmerksamkeitserregend sind, z. B. Befehlsschaltflächen, Befehlslinks und Symbole.
-   Verwenden Sie hervorgehobenen Text, einschließlich umfangreichem Text und fett formatiertem Text.
-   Legen Sie Text ein, den Benutzer in interaktiven Steuerelementen, mit Symbolen oder auf [Bannern](vis-graphic.md)lesen müssen.
-   Verwenden Sie dunklen Text auf einem hellen Hintergrund.
-   Umranden Sie die Elemente mit einem verallgemerten Raum.
-   Sie benötigen keine Interaktion, z. B. zeigend oder mit dem Mauszeiger, um das Element zu sehen, das Sie hervorheben.

    ![Screenshot der Windows-Aktivierungsoptionen ](images/vis-layout-image8.png)

    Dieses Beispiel zeigt viele Möglichkeiten, primäre Benutzeroberflächenelemente hervorzuheben.

So heben Sie die Hervorung sekundärer Benutzeroberflächenelemente auf:

-   Legen Sie sekundäre Benutzeroberflächenelemente außerhalb des Scanpfads ab.
-   Legen Sie alles, was Benutzer normalerweise nicht sehen müssen, in der unteren linken Ecke oder unteren Ecke des Fensters ab.
-   Verwenden Sie Steuerelemente, die keine Aufmerksamkeit erregen, z. B. Aufgabenlinks anstelle von Befehlsschaltflächen.
-   Verwenden Sie normalen oder grauen Text.
-   Verwenden Sie hellen Text auf einem dunklen Hintergrund. Weißer Text auf einem dunkelgrauen oder blauen Hintergrund funktioniert gut.
-   Umschließt die Elemente mit minimalem Platz.
-   Erwägen Sie die Verwendung der [progressiven Offenlegung,](ctrl-progressive-disclosure-controls.md) um sekundäre Benutzeroberflächenelemente auszublenden.

    ![Screenshot von großen und kleinen Schnittstellenelementen ](images/vis-layout-image9.png)

    Dieses Beispiel zeigt viele Möglichkeiten, sekundäre Benutzeroberflächenelemente zu deaktivieren.

### <a name="using-screen-space-effectively"></a>Effektive Verwendung des Bildschirmbereichs

Bei der effektiven Verwendung des Bildschirmraums müssen Sie mehrere Faktoren ausgleichen: Zu viel Platz zu verwenden, und ein Fenster wirkt stark und verschwenderisch und ist sogar schwer zu verwenden, basierend auf [dem Fitts-Gesetz.](inter-mouse.md)

**Falsch:**

![Screenshot mit zu viel Leerraum ](images/vis-layout-image10.png)

In diesem Beispiel ist das Fenster zu groß für seinen Inhalt.

Verwenden Sie andererseits zu wenig Platz, und ein Fenster wirkt verzeilt, mühend und beängstigend und schwierig zu verwenden, wenn scrollen und andere Bearbeitungen erforderlich sind.

**Falsch:**

![Screenshot mit zu vielen Steuerelementen ](images/vis-layout-image11.png)

In diesem Beispiel ist das Fenster zu klein für seinen Inhalt.

Obwohl die kritische Benutzeroberfläche in die minimal unterstützte [effektive Auflösung](glossary.md)passen muss, gehen Sie nicht davon aus, dass die Verwendung des Bildschirmbereichs effektiv bedeutet, dass Fenster so klein wie möglich sein sollten. **Ein effektives Layout berücksichtigt den offenen Raum und versucht nicht, alles in den kleinstmöglichen Bereich zu verzweigen.** Moderne Bildschirme verfügen über erheblichen Bildschirmbereich, und es ist sinnvoll, diesen Bereich effektiv zu verwenden, wenn Sie dies können. Daher kann es sein, dass zu viel Bildschirmraum anstelle von zu wenig verwendet wird. Auf diese Weise werden Ihre Fenster leichter und leichter erreichbar.

Sie wissen, dass ein Layout bildschirmraum effektiv verwendet, wenn:

-   Die Größe von Fenstern, Fensterbereichen und Steuerelementen muss nicht geändert werden, damit sie verwendet werden können. Wenn benutzer als Erstes die Größe eines Fensters, Bereichs oder Steuerelements ändern, ist seine Größe falsch.
-   Daten werden nicht abgeschnitten. Die meisten Daten in Listenansichten und Strukturansichten haben keine Ellipsen, und Daten in anderen Steuerelementen werden nur abgeschnitten, wenn die Datenlänge ungewöhnlich groß ist. Daten, die gelesen werden müssen, um eine Aufgabe auszuführen, sollten nicht abgeschnitten werden.
-   Die Fenster und Steuerelemente sind entsprechend dimensioniert, um unnötiges Scrollen zu vermeiden. Es gibt nur wenige horizontale Scrollleisten und keine unnötigen vertikalen Scrollleisten.
-   Steuerelemente verwenden größtenteils ihre Standardgrößen. Versuchen Sie, die Anzahl der Steuerelementgrößen zu reduzieren, indem Sie z. B. nur eine oder zwei Befehlsschaltflächenbreiten auf einer Oberfläche verwenden.
-   Die Benutzeroberflächenoberfläche ist ausgeglichen. Es gibt keine großen nicht verwendeten Bildschirmbereiche.

Wählen Sie Fenstergrößen aus, die einfach groß genug sind, um ihren Zweck zu erfüllen. (Und wenn die Größe des Fensters geändert werden kann, gilt dieses Ziel für die Standardgröße.) **Eine Kombination aus abgeschnittenen Daten oder Scrollleisten und vielem verfügbaren Bildschirmbereich ist ein klares Zeichen für ein ineffektives Layout.**

### <a name="control-sizing"></a>Größensteuerung

In der Regel besteht der erste Schritt bei der effektiven Verwendung des Bildschirmbereichs darin, die richtige Größe für die verschiedenen Benutzeroberflächenelemente zu bestimmen. Weitere Informationen finden Sie in der [Tabelle control sizing (Größe des Steuerelements)](#recommended-sizing-and-spacing) sowie in den artikeln zu den jeweiligen Steuerelementrichtlinien.

Das Fitts-Gesetz besagt, dass je kleiner ein Ziel ist, desto länger dauert es, es mit der Maus zu erhalten. Darüber hinaus kann die "Maus" für Computer, die Windows Tablet und Touch-Technologie verwenden, tatsächlich ein Stift oder der Finger des Benutzers sein. Daher sollten Sie alternative Eingabegeräte bei der Größenermittlung für kleine Steuerelemente in Betracht ziehen. **Eine Steuerelementgröße von 16 x 16 relativen Pixeln ist eine gute Mindestgröße für jedes Eingabegerät.** Im Gegensatz dazu sind die standardmäßigen 15 x 9 relativen Pixel-Drehsteuerelemente zu klein, um effektiv von Stiften verwendet zu werden.

### <a name="spacing"></a>Abstand

Durch die Bereitstellung von überflüssigen (aber nicht übermäßigen) Platz wird das Layout komfortabler und einfacher zu analysieren. Effektiver Speicherplatz ist kein ungenutzter Speicherplatz. Er spielt eine wichtige Rolle bei der Verbesserung der Scanfähigkeit für Benutzer und trägt auch zur visuellen Eignung Ihres Entwurfs bei. Richtlinien finden Sie in der [Abstandstabelle](#recommended-sizing-and-spacing).

Bei Computern, die Windows Tablet and Touch Technology verwenden, ist die "Maus" möglicherweise tatsächlich ein Stift oder der Finger des Benutzers. Das Ziel ist schwieriger, wenn ein Stift oder Finger als zeigedes Gerät verwendet wird, was dazu führt, dass Benutzer außerhalb des vorgesehenen Ziels tippen. Wenn interaktive Steuerelemente sehr nah beieinander platziert werden, aber nicht tatsächlich berührt werden, können Benutzer zwischen den Steuerelementen auf den inaktiven Bereich klicken. Da das Klicken auf den inaktiven Bereich kein Ergebnis oder visuelles Feedback enthält, sind benutzer oft unsicher, was schief gelaufen ist. Wenn kleine Steuerelemente zu stark durch Leerzeichen getrennt sind, muss der Benutzer präzise tippen, um zu vermeiden, dass auf das falsche Objekt tippt. **Um diese Probleme zu beheben, sollten die Zielbereiche interaktiver Steuerelemente entweder touchiert werden oder mindestens 3 DLUs (5 relative Pixel) Platz dazwischen haben.**

Sie wissen, dass ein Layout einen guten Abstand hat, wenn:

-   Insgesamt wirkt die Benutzeroberflächenoberfläche wohl und wirkt nicht verdräumt.
-   Der Platz wird einheitlich und ausgeglichen angezeigt.
-   Verwandte Elemente sind nah beieinander, und nicht verknüpfte Elemente sind relativ weit voneinander entfernt.
-   Zwischen Steuerelementen, die zusammen sein sollen, wie z. B. Symbolleistenschaltflächen, ist kein leerer Speicherplatz vorhanden.

### <a name="resizable-windows"></a>Fenster mit größenveränderbarer Größe

Veränderbare Fenster sind auch ein Faktor bei der effektiven Verwendung des Bildschirmbereichs. Einige Fenster bestehen aus festem Inhalt und profitieren nicht davon, dass die Größe geändert werden kann, aber Fenster mit veränderbarem Inhalt sollten die Größe ändern können. Natürlich ist der Grund, warum Benutzer die Größe eines Fensters ändern, den zusätzlichen Bildschirmbereich zu erweitern, sodass der Inhalt entsprechend erweitert werden sollte, indem den Benutzeroberflächenelementen, die es benötigen, mehr Platz gegeben wird. Fenster mit dynamischem Inhalt, Dokumenten, Bildern, Listen und Strukturen profitieren am meisten von fensterveränderbaren Fenstern.

![Screenshot des Geänderten Steuerelements zum Abrufen der Bildlaufleiste ](images/vis-layout-image12.png)

In diesem Beispiel wird durch ändern der Größe des Fensters die Größe des Listenansicht-Steuerelements geändert.

Allerdings können Fenster zu breit gestreckt werden. Beispielsweise werden viele Systemsteuerungsseiten unhandlich, wenn der Inhalt breiter als 600 relative Pixel ist. In diesem Fall ist es besser, die Größe des Inhaltsbereichs nicht über diese maximale Breite hinaus zu ändern oder den Ursprung des Inhalts zu ändern, wenn die Größe des Fensters größer wird. Behalten Sie stattdessen eine maximale Breite und einen festen linken oberen Ursprung bei.

Text wird schwierig zu lesen, wenn die Zeilenlänge zunimmt. Ziehen Sie für Textdokumente eine maximale Zeilenlänge von 80 Zeichen in Betracht, um den Text leicht lesbar zu machen. (Zeichen enthalten Buchstaben, Interpunktion und Leerzeichen.)

**Falsch:**

![Screenshot eines breiten Meldungsfelds mit langem Text ](images/vis-layout-image13.png)

In diesem Beispiel erschwert die lange Textlänge das Lesen.

Außerdem müssen vergrößerbare Fenster den Bildschirmbereich effektiv nutzen, wenn sie kleiner werden, indem sie die Größe von Inhalt verkleinern und Speicherplatz aus Benutzeroberflächenelementen entfernen, die ohne diesen effektiv funktionieren können. An einem bestimmten Punkt wird das Fenster oder seine Benutzeroberflächenelemente zu klein, um verwendet werden zu können. Daher sollte ihnen eine Mindestgröße zugewiesen werden, oder einige Elemente sollten vollständig entfernt werden.

![Screenshot des Fensters mit einem hohen, aufdringlichen Menüband ](images/vis-layout-image14.png)

![Screenshot des Fensters ohne Menüband ](images/vis-layout-image15.png)

In diesem Beispiel hat der Bereich eine Mindestgröße.

Einige Programme profitieren von einer völlig anderen Präsentation, um den Inhalt in kleineren Größen nutzbar zu machen.

![Screenshot der zentrierten Media Player-Schaltflächen ](images/vis-layout-image16.png)

In diesem Beispiel wird Windows Media Player Format geändert, wenn das Fenster für das Standardformat zu klein wird.

### <a name="focus"></a>Fokus

Ein Layout hat den Fokus, wenn es einen offensichtlichen Ort gibt, um zuerst zu suchen. Der Fokus ist wichtig, um Benutzern zu zeigen, wo Sie mit dem Scannen Ihres Fensters oder Ihrer Seite beginnen können. Ohne klaren Fokus wird das Auge des Benutzers ziellos schweifen. Der Schwerpunkt sollte etwas Wichtiges sein, das Benutzer schnell finden und verstehen müssen, und sie sollten den größten visuellen Schwerpunkt haben. Die obere linke Ecke ist der natürliche Fokuspunkt für die meisten Fenster.

Es sollte nur einen Fokuspunkt geben. Genau wie in der Realen kann sich das Auge nur auf einen Punkt gleichzeitig konzentrieren, benutzer können sich nicht gleichzeitig auf mehrere Orte konzentrieren.

Um ein Benutzeroberflächenelement zum Schwerpunkt zu machen, können Sie es durch:

-   Platzieren Sie es in der oberen linken oder oberen Mitte der Oberfläche.
-   Verwenden interaktiver Steuerelemente, die wichtig und leicht verständlich sind.
-   Verwenden von prominenten Texten, z. B. einer Hauptanweisung.
-   Festlegen der Standardauswahl und des anfänglichen Eingabefokus für die Steuerelemente.
-   Platzieren der Steuerelemente in einem anderen farbigen Hintergrund.

Ziehen Sie Windows Search. Der Schwerpunkt für Windows Search sollte das Suchfeld sein, da es der Ausgangspunkt für die Aufgabe ist. Er befindet sich jedoch in der oberen rechten Ecke, um mit der standardmäßigen Platzierung des Suchfelds konsistent zu sein. Das Suchfeld hat den Eingabefokus, aber angesichts seiner Position im Scanpfad reicht dieser Hinweis allein nicht aus.

Um dieses Problem zu beheben, gibt es im oberen oberen Bereich des Fensters eine wichtige Anweisung, um Benutzer an den richtigen Ort weiter zu leitet.

**Annehmbar:**

![Screenshot des Suchdialogfelds mit hilfreichen Texten ](images/vis-layout-image17.png)

In diesem Beispiel leitet eine prominente Anweisung in der oberen Mitte des Fensters Benutzer zum Feld Suchen.

Ohne die Anweisungen würde das Fenster keinen offensichtlichen Schwerpunkt haben.

**Falsch:**

![Screenshot des Suchdialogfelds ohne Text ](images/vis-layout-image18.png)

Dieses Beispiel hat keinen offensichtlichen Schwerpunkt. Benutzer wissen nicht, wo sie suchen sollten.

Wenn Sie einen visuellen Fokus auf ein Benutzeroberflächenelement legen, stellen Sie sicher, dass die Aufmerksamkeit gerechtfertigt ist. Im vorherigen falschen Windows Search befindet sich die hervorgehobene Schaltfläche Alle in der oberen linken Ecke und hat die meisten visuellen Hervorhebungen, aber es ist nicht der beabsichtigte Fokuspunkt. Benutzer können beim Blick auf diese Schaltfläche hängen bleiben, um herauszufinden, wie sie damit umkommen.

**Falsch:**

![Screenshot der hervorgehobenen Schaltfläche "Alle" ](images/vis-layout-image19.png)

Ohne die hervorgehobene Anweisung als Fokuspunkt ist die hervorgehobene Schaltfläche Alle ein unbeabsichtigter Fokuspunkt.

### <a name="flow"></a>Flow

Ein Layout verfügt über einen Fluss, wenn Benutzer reibungslos und natürlich durch einen klaren Pfad durch die Oberfläche geführt werden und Benutzeroberflächenelemente in der für ihre Verwendung geeigneten Reihenfolge finden. Sobald Benutzer den Fokuspunkt identifizieren, müssen sie bestimmen, wie die Aufgabe abgeschlossen werden soll. Die Platzierung der Benutzeroberflächenelemente vermittelt ihre Beziehung und sollte die Schritte zum Ausführen der Aufgabe spiegeln. In der Regel bedeutet dies, dass die Aufgabenschritte natürlich von links nach rechts und von oben nach unten (in den Kulturen des Westens) ablaufen sollten.

Sie wissen, dass ein Layout einen guten Ablauf auf hat, wenn:

-   Die Platzierung der Benutzeroberflächenelemente spiegelt die Schritte ab, die Benutzer zum Ausführen der Aufgabe ausführen müssen.
-   Benutzeroberflächenelemente, die eine Aufgabe initiieren, befinden sich in der oberen linken Ecke oder in der oberen Mitte.
-   Benutzeroberflächenelemente, die eine Aufgabe abschließen, befinden sich in der unteren rechten Ecke.
-   Verwandte Benutzeroberflächenelemente sind zusammen. Nicht verknüpfte Elemente sind getrennt.
-   Die erforderlichen Schritte befinden sich im Hauptfluss.
-   Optionale Schritte befinden sich außerhalb des Hauptflusses und werden möglicherweise mithilfe eines geeigneten Hintergrunds oder einer progressiven Offenlegung wieder hervorgehoben.
-   Häufig verwendete Elemente werden vor selten verwendeten Elementen im Scanpfad angezeigt.
-   Benutzer wissen immer, was als Nächstes zu tun ist. Es gibt keine unerwarteten Brüche oder Unterbrechungen im Taskfluss.

**Falsch:**

![Screenshot des verwirrenden Dialogfeldlayouts ](images/vis-layout-image20.png)

In diesem Beispiel wissen Benutzer nicht, was als Nächstes zu tun ist. Es gibt unerwartete Brüche und Unterbrechungen im Taskfluss.

**Richtig:**

![Screenshot eines gut geplanten Dialogfelds ](images/vis-layout-image21.png)

In diesem Beispiel spiegelt die Darstellung der Benutzeroberflächenelemente die Schritte zum Ausführen der Aufgabe wieder.

### <a name="grouping"></a>Gruppierung

Ein Layout verfügt über Gruppierung, wenn logisch verknüpfte Benutzeroberflächenelemente eine klare visuelle Beziehung haben. Gruppen sind wichtig, da es für Benutzer einfacher ist, eine Gruppe verwandter Elemente zu verstehen und sich auf diese zu konzentrieren, als die Elemente einzeln. Gruppen machen ein Layout einfacher und einfacher zu analysieren.

Sie können die Gruppierung auf folgende Weise anzeigen (in zunehmender Größe):

-   **Layout.** Sie können verwandte Steuerelemente nebeneinander gruppieren und zusätzlichen Abstand zwischen nicht verknüpften Steuerelementen setzen.

    ![Abbildung von vier Symbolen mit vier Aufgabengruppen ](images/vis-layout-image22.png)

    In diesem Beispiel wird layout allein verwendet, um Steuerelementbeziehungen zu zeigen.

-   **Trennzeichen.** Ein Trennzeichen ist eine horizontale oder vertikale Linie, die eine Gruppe von Steuerelementen vereinheitlicht. Trennzeichen bieten ein einfacheres, klareres Aussehen. Im Gegensatz zu Gruppenfeldern funktionieren sie jedoch am besten, wenn sie die gesamte Oberfläche umfassen.

    ![Screenshot von drei Symbolen und drei Trennzeichen ](images/vis-layout-image23.png)

    In diesem Beispiel werden bezeichnete Trennzeichen verwendet, um Steuerelementbeziehungen zu zeigen.

-   **Aggregatoren.** Ein Aggregator ist eine Grafik, die eine visuelle Beziehung zwischen stark verknüpften Steuerelementen erstellt.

    ![Screenshot von Steuerelementen innerhalb einer elliptischen Linie ](images/vis-layout-image24.png)

    In diesem Beispiel wird ein Begrenzungsaggregator verwendet, um die Beziehung zwischen den Steuerelementen zu hervorheben und sie wie ein einzelnes Steuerelement anstelle von acht anfühlen zu lassen.

-   **Gruppenfelder.** Ein Gruppenfeld ist ein bezeichneter rechteckiger Rahmen, der eine Reihe verwandter Steuerelemente umgibt.

    ![Screenshot der Kontrollkästchen in einem rechteckigen Rahmen ](images/vis-layout-image25.png)

    In diesem Beispiel umschließt und bezeichnet ein Gruppenfeld einen Satz verwandter Steuerelemente.

-   **Hintergründe.** Sie können Hintergründe verwenden, um verschiedene Inhaltstypen zu hervorheben oder zu heben.

    ![Screenshot der linken Seite der Systemsteuerung ](images/vis-layout-image26.png)

    In diesem Beispiel wird der Aufgabenbereich der Systemsteuerung verwendet, um verwandte Aufgaben und Systemsteuerungselemente zu gruppen.

    Um visuelle Unübersichtlichkeit zu vermeiden, ist die leichteste Gruppierung, die die Aufgabe gut macht, die beste Wahl. Weitere Informationen finden Sie unter [Gruppenfelder](ctrl-group-boxes.md), [Registerkarten](ctrl-tabs.md), [Trennzeichen und Hintergründe](vis-graphic.md).

Unabhängig vom Gruppierungsstil können Sie den Einzug verwenden, um die Beziehung der Steuerelemente innerhalb einer Gruppe zu zeigen. Steuerelemente, bei denen es sich um Peers zueinander handelt, sollten linksbündig ausgerichtet sein, und abhängige Steuerelemente werden um 12 DLUs oder 18 relative Pixel eingezogen.

![Screenshot von drei Ebenen mit eingerückten Steuerelementen ](images/vis-layout-image27.png)

Abhängige Steuerelemente werden um 12 DLUS oder 18 relative Pixel eingerückt. Dies ist der Abstand zwischen Kontrollkästchen und Optionsfeldern von ihren Bezeichnungen.

Sie wissen, dass ein Layout eine gute Gruppierung auf hat, wenn:

-   Das Fenster oder die Seiten verfügt über mindestens 7 Gruppen.
-   Der Zweck jeder Gruppe ist offensichtlich.
-   Die Beziehung der Steuerelemente innerhalb jeder Gruppe ist offensichtlich, insbesondere die Steuerungsabhängigkeit.
-   Die Gruppierung vereinfacht den Inhalt, anstatt ihn komplexer zu machen.

### <a name="alignment"></a>Ausrichtung

Ausrichtung ist die koordinierte Platzierung von Benutzeroberflächenelementen. Die Ausrichtung ist wichtig, da sie die Überprüfung von Inhalten vereinfacht und die Wahrnehmung der visuellen Komplexität durch die Benutzer beeinflusst.

Es gibt mehrere Ziele, die bei der Bestimmung der Ausrichtung zu berücksichtigen sind:

-   **Einfaches horizontales Scannen.** Benutzer können horizontal lesen und aufeinander bezogene Elemente ohne unwendliche Lücken suchen.
-   **Einfacheres vertikales Scannen.** Benutzer können Spalten verwandter Elemente scannen und sofort finden, was sie suchen, mit minimaler horizontaler Augenbewegung.
-   **Minimale visuelle Komplexität.** Benutzer betrachten ein Layout als visuell komplex, wenn es über unnötige Rasterlinien mit vertikaler Ausrichtung verfügt.

### <a name="horizontal-alignment"></a>Horizontale Ausrichtung

**Linke Ausrichtung**

Aufgrund der Leserichtung von links nach rechts funktioniert die linke Ausrichtung für die meisten Inhalte gut. Die linke Ausrichtung vereinfacht das vertikale Scannen von spaltenaren Daten.

**Rechte Ausrichtung**

Die rechte Ausrichtung ist die beste Wahl für numerische Daten, insbesondere [Spalten mit numerischen Daten.](ctrl-text-boxes.md) Die rechte Ausrichtung funktioniert auch gut für [Commitschaltflächen](glossary.md) und Steuerelemente, die am rechten Fensterrand ausgerichtet sind.

![Screenshot der Schaltfläche "Pfeil nach unten" für die erweiterte Suche ](images/vis-layout-image28.png)

In diesem Beispiel ist das erweiterte Progressive Disclosure-Steuerelement für die Suche rechtsbündig ausgerichtet, da es am rechten Fensterrand platziert wird.

**Zentrierung**

Die zentrierte Ausrichtung ist am besten für Situationen reserviert, in denen entweder die linke oder die rechte Ausrichtung ungeeignet ist oder unausgeglichen erscheint.

![Screenshot von zentrierten Media Player-Steuerelementen ](images/vis-layout-image29.png)

In diesem Beispiel wird das Media Player-Steuerelement zentriert, um eine ausgeglichene Darstellung zu erhalten.

Zentriert den Fensterinhalt nicht nur, um Platz zu füllen.

**Falsch:**

![Screenshot eines Fensters mit zu viel Leerraum ](images/vis-layout-image30.png)

In diesem Beispiel wird inhalt fälschlicherweise in einem verstellbaren Fenster zentriert, um Platz zu füllen.

### <a name="vertical-alignment"></a>Vertikale Ausrichtung

**Elementspitzen**

Aufgrund der Leserichtung von oben nach unten funktioniert die obere Ausrichtung für die meisten Inhalte gut. Die ausrichtung oben vereinfacht das horizontale Scannen von Benutzeroberflächenelementen.

**Textbaselinen**

Wenn Sie Steuerelemente vertikal an Text ausrichten, richten Sie die Textbaselinen aus, um einen reibungslosen horizontalen Lesefluss zu ermöglichen.

**Richtig:**

![Screenshot der ausgerichteten Schaltfläche und des Bezeichnungstexts ](images/vis-layout-image31.png)

**Falsch:**

![Screenshot der nicht ausgerichteten Schaltfläche und des Bezeichnungstexts ](images/vis-layout-image32.png)

Im richtigen Beispiel werden das Steuerelement und seine Bezeichnung vertikal durch ihre Textbasislinien ausgerichtet.

Sie wissen, dass ein Layout eine gute Ausrichtung auf hat, wenn:

-   Es ist einfach, sowohl horizontal als auch vertikal zu scannen.
-   Es hat eine einfache visuelle Darstellung.

### <a name="label-alignment"></a>Bezeichnungsausrichtung

Die allgemeinen Ausrichtungsregeln gelten für Steuerelementbezeichnungen, aber es ist ein häufiges Problem, das besondere Aufmerksamkeit erfordert. Die Bezeichnungsausrichtung hat die folgenden Ziele:

-   Erleichtern Sie die vertikale Überprüfung, um das richtige Steuerelement zu finden.
-   Einfaches horizontales Scannen zum Zuordnen von Bezeichnungen zu ihren Steuerelementen.
-   Einfache Lokalisierung, Behandlung von Bezeichnungen, die sich sprachübergreifend in der Länge unterscheiden.
-   Funktioniert gut mit einer Mischung aus unterschiedlichen Bezeichnungslängen.
-   Nutzt den verfügbaren Speicherplatz effizient und vermeidet abgeschnittenen Text.

Das Gesamtziel besteht in der Reduzierung des Umfangs der Augenbewegungen, die erforderlich sind, um zu finden, nach welchen Benutzern wahrscheinlich gesucht wird, aber die Art der Steuerelemente und das, was Benutzer suchen, hängt vom Kontext ab.

Es gibt vier gängige Bezeichnungsplatzierungs- und Ausrichtungsstile mit jeweils seinen Vorteilen:

-   Linksbgelassene Bezeichnungen oberhalb von Steuerelementen
-   Linksbgelassene Bezeichnungen links von Steuerelementen
-   Linksbgelassene Bezeichnungen auf der linken Seite von Steuerelementen, Steuerelemente auf der linken Seite
-   Rechtsbierten Bezeichnungen links von Steuerelementen

**Linksbgelassene Bezeichnungen oberhalb von Steuerelementen**

Dieser Stil ist am einfachsten zu lokalisieren, da das Layout nicht von der Länge der Bezeichnungen abhängig ist, aber den vertikalsten Platz benötigt.

![Liste mit zwei Spalten von Bezeichnungen über Steuerelementen ](images/vis-layout-image33.png)

Dieser Stil nimmt den vertikalsten Platz ein, lässt sich aber am einfachsten lokalisieren. Dies ist eine bessere Wahl für die Bezeichnung größtenteils interaktiver Steuerelemente.

Die beste Verwendung ist, wenn:

-   Die bezeichneten Steuerelemente sind interaktiv (nicht nur Text).
-   Die Benutzeroberfläche wird lokalisiert. Dieser Stil bietet häufig Platz, um die Länge der Bezeichnung zu verdreifachen oder sogar zu verdreifachen.
-   Die Benutzeroberfläche verwendet eine Technologie für festes Layout (z. B. Win32).
-   Es gibt zehn oder weniger Steuerelemente. Mit mehr Steuerelementen sind die Bezeichnungen schwer zu scannen.
-   Es ist ausreichend vertikaler Platz vorhanden, um die Bezeichnungen aufnehmen zu können.
-   Das Layout muss frei sein, nicht nur Spalten.

**Linksbgelassene Bezeichnungen links von Steuerelementen**

Dieser Stil lässt sich am einfachsten vertikal scannen und funktioniert auch gut, wenn sich Bezeichnungen stark in der Länge unterscheiden, es jedoch schwieriger ist, die Bezeichnung dem Steuerelement zu zuordnen. In diesem Stil können bei Bedarf mehrzeilenbeschriftungen verwendet werden.

![Liste mit vier Spalten von Bezeichnungen, die von Steuerelementen übrig sind ](images/vis-layout-image34.png)

Dieser Stil funktioniert gut. Es gibt jedoch zwei Spalten, aber visuell sieht es so aus, als ob es vier gibt, wodurch die Daten komplexer erscheinen.

Die beste Verwendung ist, wenn:

-   Benutzer werden wahrscheinlich vertikal scannen, um bestimmte Bezeichnungen zu finden.
-   Benutzer lesen die Bezeichnungen und Steuerelemente wahrscheinlich nicht von links nach rechts, von oben nach unten.
-   Es ist ausreichend horizontaler Platz vorhanden, um die Bezeichnungen aufnehmen zu können.
-   Die Bezeichnungen unterscheiden sich erheblich in der Länge.
-   Es gibt viele Steuerelemente, z. B. mit Formularen.
-   Es gibt nur wenige Spalten. Die Bezeichnungen und Steuerelemente werden visuell als zwei einzelne Spalten angezeigt.

**Linksbgelassene Bezeichnungen auf der linken Seite von Steuerelementen, Steuerelemente auf der linken Seite**

Dieser Stil erleichtert das vertikale Scannen der Bezeichnungen sowie der Bezeichnungen und Steuerelemente und ist sehr platzeffizient. es ist jedoch schwieriger, die Steuerelemente vertikal zu scannen. Die Steuerelemente sind rechtsbiert, um den verfügbaren Speicherplatz voll zu nutzen.

![Liste von zwei Spalten von Bezeichnungen mit lappenden Steuerelementen ](images/vis-layout-image35.png)

Dieser Stil ist kompakt und einfach zu lesen, aber es ist schwierig, Steuerelemente vertikal zu scannen.

Die beste Verwendung ist, wenn:

-   Die Benutzeroberfläche verwendet eine Variable Layout-Technologie (z. B. Windows Presentation Foundation).
-   Benutzer werden wahrscheinlich vertikal scannen, um bestimmte Bezeichnungen zu finden.
-   Benutzer lesen die Bezeichnungen und Steuerelemente wahrscheinlich von links nach rechts, von oben nach unten.
-   Benutzer werden die Steuerelemente wahrscheinlich nicht vertikal scannen.
-   Der Steuerelementtext variiert in der Länge und wird wahrscheinlich abgeschnitten, wenn ein anderer Stil verwendet wird.
-   Die Steuerelemente sind schreibgeschützt, z. B. schreibgeschützte Textfelder. Bei anderen Steuerelementen sieht diese Ausrichtung schlampig aus. Die Steuerelemente können jedoch beim Klicken bearbeitet werden.
-   Es gibt viele Spalten, aber nur wenige Steuerelemente in einer Spalte.

**Rechtsbrechtbierte Bezeichnungen links von Steuerelementen**

Dieser Stil lässt sich am einfachsten horizontal lesen, um die Bezeichnungen ihren Steuerelementen zu zuordnen. Es ist jedoch schwierig, die Bezeichnungen vertikal zu scannen, und funktioniert nicht gut, wenn labelsList mit eingerückten Bezeichnungen und Steuerelementen sich stark in der Länge unterscheidet.

![Liste mit eingerückten Bezeichnungen und Steuerelementen ](images/vis-layout-image36.png)

Dieser Stil ermöglicht ein einfaches vertikales Scannen der Steuerelemente, erschwert jedoch das vertikale Scannen der Bezeichnungen.

Am besten verwendet in:

-   Benutzer lesen die Bezeichnungen und Steuerelemente wahrscheinlich von links nach rechts, von oben nach unten.
-   Benutzer werden wahrscheinlich nicht vertikal scannen, um nach bestimmten Bezeichnungen zu suchen. Dies liegt möglicherweise daran:
    -   Es gibt nur wenige Steuerelemente.
    -   Die Bezeichnungen sind bekannt.
    -   Die Steuerelemente sind größtenteils selbsterklärend und sind selten leer (möglicherweise mit Standardwerten, um leere Steuerelemente zu verhindern).
-   Es ist ausreichend horizontaler Platz vorhanden, um die Bezeichnungen aufnehmen zu können.
-   Die Bezeichnungen unterscheiden sich nicht erheblich in der Länge.
-   Viele Spalten vorhanden sind. Die Bezeichnungen und Steuerelemente werden visuell als einzelne Spalte angezeigt.

Bevor Sie einen dieser Stile übernehmen, sollten Sie jedoch zwei weitere Faktoren berücksichtigen:

-   Bevorzugen Sie einen Stil, den Sie im gesamten Programm konsistent verwenden können.
-   Linksbgelassene Bezeichnungen, die sich über Steuerelementen links von Steuerelementen befinden, sind die gängigsten Stile, daher sollten sie bevorzugt werden.

### <a name="balance"></a>Balance

Ein Fenster oder eine Seite hat ein Gleichgewicht, wenn der Inhalt gleichmäßig über die Oberfläche verteilt angezeigt wird. Wenn die Oberfläche physisch die gleiche Gewichtung wie visuell hat, würde ein ausgeglichenes Layout nicht auf eine Seite kippen.

Das häufigste Gleichgewichtsproblem besteht in zu vielem Inhalt auf der linken Seite eines Fensters oder einer Seite. Sie können ein Guthaben auf folgende Weise erstellen:

-   Verwenden von größeren Rändern auf der linken Seite als rechts.
-   Platzieren von Benutzeroberflächenelementen, die zum Abschließen einer Aufgabe verwendet werden, auf der rechten Seite.
-   Platzieren von Benutzeroberflächenelementen, die während der gesamten Aufgabe verwendet werden, in der Mitte.
-   Längen von Steuerelementen, die die Größe ändern können oder mehrzeilenfähig sind.
-   Strategische Verwendung der zentrierten Ausrichtung.

![Screenshot des Druckers auf der linken Seite und Text auf der rechten Seite ](images/vis-layout-image37.png)

Dieses ausgeglichene Seitenlayout des Assistenten zeigt einen größeren linken Rand als rechts, um das Gleichgewicht zu verbessern.

Wenn diese Techniken kein Gleichgewicht erzielen, sollten Sie erwägen, die Breite des Fensters oder der Seite zu reduzieren, um den Inhalt besser zu berücksichtigen.

Bei oberflächen, die die Größe ändern können, sollten Sie Inhalte nicht nur zentrieren, um ein Gleichgewicht zu erzielen. Behalten Sie stattdessen einen festen oberen linken Ursprung bei, definieren Sie eine maximale Oberfläche, und ausgleichen Sie den Inhalt innerhalb des verwendeten Platzes.

### <a name="grids"></a>Raster

Ein Raster ist ein unsichtbares zugrunde liegendes Ausrichtungssystem. Raster können symmetrisch sein, aber asymmetrische Raster funktionieren genauso gut. Bei Verwendung durch ein einzelnes Fenster oder eine Einzelne Seite können Raster dazu beitragen, Den Inhalt auf einer Oberfläche zu organisieren. Bei der Wiederverwendung erstellen Raster oberflächenübergreifend ein konsistentes Layout.

Die Anzahl der Rasterlinien wirkt sich auf die Wahrnehmung der visuellen Komplexität aus. Ein Layout mit weniger Rasterlinien erscheint einfacher als ein Layout mit mehr Rasterlinien.

**Visuell komplex:**

![Screenshot des unübersichtlichen Dialogfelds ](images/vis-layout-image38.png)

**Visuell einfach:**

![Screenshot des organisierten Dialogfelds ](images/vis-layout-image39.png)

Unnötige Rasterlinien sorgen für visuelle Komplexität.

Sie wissen, dass ein Layout Raster effektiv verwendet, wenn:

-   Fenster oder Seiten mit ähnlichen Inhalten oder Funktionen haben ein ähnliches Layout.
-   Wiederholte Entwurfselemente werden an ähnlichen Stellen über Fenster und Seiten hinweg angezeigt.
-   Es gibt keine unnötigen vertikalen und horizontalen Ausrichtungsrasterlinien.

### <a name="visual-simplicity"></a>Visuelle Einfachheit

Visuelle Einfachheit ist die Wahrnehmung, dass ein Layout nicht komplizierter ist, als es sein muss.

Sie wissen, dass ein Layout visuelle Einfachheit hat, wenn es:

-   Beseitigt unnötige Fensterver chrome-Ebenen.
-   Stellt den Inhalt mithilfe von mindestens sieben leicht identifizierbaren Gruppen vor.
-   Verwendet einfache Gruppierung, z. B. Layout und Trennzeichen anstelle von Gruppenfeldern.
-   Verwendet einfache Steuerelemente, z. B. Links anstelle von Befehlsschaltflächen für sekundäre Befehle, und Dropdownlisten anstelle von Listen für Auswahlmöglichkeiten.
-   Reduziert die Anzahl der Rasterlinien für vertikale und horizontale Ausrichtung.
-   Reduziert die Anzahl der Steuerelementgrößen, indem beispielsweise nur eine oder zwei Befehlsschaltflächenbreiten auf einer Oberfläche verwendet werden.
-   Verwendet progressive Offenlegung, um Benutzeroberflächenelemente auszublenden, bis sie benötigt werden.
-   Verwendet ausreichend Platz, damit sich das Fenster oder die Seite nicht anfühlt.
-   Größe von Fenstern und Steuerelementen entsprechend, um unnötiges Scrollen zu vermeiden.
-   Verwendet eine einzelne Schriftart mit einer kleinen Anzahl von Größen und Textfarben.

Allgemein gilt: Wenn ein Layoutelement entfernt werden kann, ohne die Effektivität der Benutzeroberfläche zu schaden, sollte dies wahrscheinlich der Grund sein.

## <a name="guidelines"></a>Richtlinien

### <a name="screen-resolution-and-dpi"></a>Bildschirmauflösung und DPI

-   **Unterstützt die effektive Windows-Mindestauflösung von 800 x 600 Pixel.** Für kritische Beis, die im abgesicherten Modus funktionieren müssen, unterstützen Sie eine effektive Auflösung von 640 x 480 Pixeln. Achten Sie darauf, den von der Taskleiste verwendeten Speicherplatz zu berücksichtigen, indem Sie 48 vertikale [relative](glossary.md) Pixel für Fenster reservieren, die mit der Taskleiste angezeigt werden.
-   **Optimieren Sie die Layouts von Fenstern, die die Größe ändern können, um eine effektive Auflösung von 1024 x 768 Pixel zu haben.** Ändern Sie die Größe dieser Fenster automatisch, um die Bildschirmauflösungen so zu ändern, dass sie weiterhin funktionsfähig sind.
-   **Testen Sie Ihre Fenster unbedingt in den Modi 96 Punkte pro Zoll (dpi) (bei 800 x 600 Pixeln), 120 dpi (bei 1024 x 768 Pixel) und 144 dpi (bei 1200 x 900 Pixeln).** Überprüfen Sie, ob Layoutprobleme auftreten, z. B. das Beschneiden von Steuerelementen, Text und Fenstern und das Strecken von Symbolen und Bitmaps.
-   **Für Programme mit Touch- und mobilen Verwendungsszenarien optimieren Sie für 120 dpi.** Bildschirme mit hohem DPI-Wert sind derzeit bei Touch-PCs und mobilen PCs weit verbreitet.

### <a name="window-size"></a>Fenstergröße

-   **Wählen Sie eine für den Inhalt geeignete Standardfenstergröße aus.** Sie sollten keine größeren Anfangsfenster verwenden, wenn Sie den Platz effektiv nutzen können.
-   **Verwenden Sie ein ausgewogenes Seitenverhältnis zwischen Höhe und Breite.** Ein Seitenverhältnis zwischen 3:5 und 5:3 wird bevorzugt, obwohl ein Seitenverhältnis von 1:3 für Meldungsdialogfelder (z. B. Fehler und Warnungen) verwendet werden kann.
-   **Verwenden Sie nach Möglichkeit verstellbare Fenster, um Bildlaufleisten und abgeschnittene Daten zu vermeiden.** Fenster mit dynamischem Inhalt, Dokumenten, Bildern, Listen und Strukturen profitieren am meisten von verstellbaren Fenstern.
-   **Bei Textdokumenten sollten Sie eine maximale Zeilenlänge von 80** Zeichen in Betracht ziehen, damit der Text leicht lesbar ist. (Zeichen enthalten Buchstaben, Interpunktion und Leerzeichen.)
-   Fenster mit fester Größe:
    -   **Fenster mit fester Größe müssen vollständig sichtbar sein und so dimensioniert sein, dass sie in den Arbeitsbereich passen.**
-   Fenster mit anpassbarer Größe:
    -   **Vergrößerbare Fenster können für höhere Auflösungen optimiert werden, aber bei Bedarf zur Anzeigezeit auf die tatsächliche Bildschirmauflösung herunter dimensioniert werden.**
    -   **Progressiv größere Fenster müssen progressiv mehr Informationen anzeigen.** Stellen Sie sicher, dass mindestens ein Fensterteil oder Steuerelement über inhalte verfügt, deren Größe geändert werden kann.
    -   **Behalten Sie den oberen linken Ursprung des Inhalts bei, wenn die Größe des Fensters geändert wird.** Verschieben Sie den Ursprung nicht, um den Inhalt beim Ändern der Fenstergröße zu ausgleichen.
    -   **Legen Sie eine maximale Inhaltsgröße fest, wenn der Inhalt zu breit sein kann.** Wenn der Inhalt unhandlich wird, ändern Sie die Größe des Inhaltsbereichs nicht über seine maximale Breite hinaus, oder ändern Sie den Ursprung des Inhalts, wenn die Größe des Fensters vergrößert wird. Behalten Sie stattdessen eine maximale Breite und einen festen ursprung links oben bei.
    -   **Legen Sie eine Mindestfenstergröße fest, wenn es eine Größe gibt, unter der der Inhalt nicht mehr verwendet werden kann.** Legen Sie bei Steuerelementen, die die Größe ändern können, die minimale größesfähige Elementgrößen auf die kleinsten funktionalen Größen fest, z. B. minimale funktionale Spaltenbreiten in Listenansichten. Optionale Benutzeroberflächenelemente sollten vollständig entfernt werden.
    -   **Ändern Sie die Präsentation, um den Inhalt in kleineren Größen nutzbar zu machen.**

        ![Screenshot von Media Player-Steuerelementen ](images/vis-layout-image16.png)

        In diesem Beispiel ändert Windows Media Player sein Format, wenn das Fenster für das Standardformat zu klein wird.

### <a name="control-size"></a>Steuerelementgröße

-   **Machen Sie alle interaktiven Steuerelemente mit mindestens 16 x 16 Pixeln relativ.** Dies funktioniert gut für alle Eingabegeräte, einschließlich Windows Tablet und Touch Technology.
-   **Größensteuerelemente, um abgeschnittene Daten zu vermeiden.** Abschneiden Sie keine Daten, die gelesen werden müssen, um eine Aufgabe auszuführen. Spalten der Größenlistenansicht, um abgeschnittene Daten zu vermeiden.
-   **Größensteuerelemente, um unnötiges Scrollen zu vermeiden.** Machen Sie Steuerelemente etwas größer, wenn dadurch eine Scrollleiste entfernt wird. Es sollten einige vertikale Scrollleisten und keine unnötigen horizontalen Scrollleisten vorhanden sein.

    ![Screenshot der Listengröße, um eine Scrollleiste zu vermeiden ](images/vis-layout-image40.png)

    In diesem Beispiel wird die Größe der Dropdownliste angepasst, um die Scrollleiste zu entfernen.

-   **Reduzieren Sie die Anzahl der Steuerelementgrößen auf einer Oberfläche.** Verwenden Sie bevorzugt die [empfohlenen Standardsteuerelementgrößen,](#recommended-sizing-and-spacing) und verwenden Sie bei Bedarf einige konsistente größere oder kleinere Steuerelemente. Versuchen Sie, eine einzelne Breite für Listenfelder und Strukturansichten und maximal drei Breiten für Befehlsschaltflächen und Dropdownlisten zu verwenden. Textfeld- und Kombinationsfeldbreiten sollten jedoch die Länge der längsten oder erwarteten Eingabe vorschlagen.

    ![Screenshot des Dialogfelds mit Listen und Schaltflächen ](images/vis-layout-image41.png)

    In diesem Beispiel werden ein Listenfeld und eine Befehlsschaltfläche konsistent verwendet.

-   **Schließen Sie für Steuerelemente, deren Größe auf Der Text basiert, zusätzliche 30 Prozent (bis zu 200 Prozent für kürzeren Text) für jeden Text ein, der lokalisiert wird.** In dieser Richtlinie wird davon ausgegangen, dass das Layout mit englischem Text entworfen wurde. Beachten Sie auch, dass sich diese Richtlinie auf lokalisierten Text bezieht, nicht auf Zahlen.
-   **Erweitern Sie statische Textsteuerelemente, Kontrollkästchen und Optionsfelder auf die maximale Breite, die in das Layout passt.** Auf diese Weise wird eine Kürzung von Text variabler Länge und Lokalisierung vermieden.

    **Falsch:**

    ![Screenshot des Statussteuerelements und des Teiltexts ](images/vis-layout-image42.png)

    In diesem Beispiel wird Steuertext unnötigerweise abgeschnitten.

### <a name="control-spacing"></a>Steuerelementabstand

-   **Wenn Steuerelemente nicht berührt werden, haben Sie mindestens 3 DLUs (5 relative Pixel) Platz dazwischen.** Andernfalls können Benutzer zwischen den Steuerelementen auf inaktiven Bereich klicken. Da das Klicken auf den inaktiven Bereich kein Ergebnis oder visuelles Feedback enthält, sind benutzer oft unsicher, was schief gelaufen ist.

### <a name="placement"></a>Platzierung

-   **Ordnen Sie die Benutzeroberflächenelemente innerhalb einer Oberfläche so an, dass sie in einer Reihenfolge von links nach rechts von oben nach unten (in kulturellen Kulturen des Westens) von links nach rechts fließen.** Die Platzierung der Benutzeroberflächenelemente vermittelt ihre Beziehung und sollte die Schritte zum Ausführen der Aufgabe widerspiegeln.
-   **Platzieren Sie Benutzeroberflächenelemente, die eine Aufgabe initiieren, in der oberen linken Ecke oder in der oberen Mitte.** Geben Sie dem Benutzeroberflächenelement, das Benutzer zuerst betrachten sollten, die größte visuelle Hervorhebung.
-   **Platzieren Sie Benutzeroberflächenelemente, die eine Aufgabe abschließen, in der unteren rechten Ecke.**
-   **Platzieren Sie verwandte Benutzeroberflächenelemente zusammen, und trennen Sie nicht verbundene Elemente.**
-   **Platzieren Sie die erforderlichen Schritte im Hauptflow.**
-   **Platzieren Sie optionale Schritte außerhalb des Hauptflusses,** möglicherweise durch Verwendung eines geeigneten Hintergrunds oder einer progressiven Offenlegung.
-   **Platzieren Sie häufig verwendete Elemente vor selten verwendeten Elementen** im Scanpfad.

### <a name="focus"></a>Fokus

-   **Wählen Sie ein einzelnes Benutzeroberflächenelement aus, das Benutzer zuerst betrachten müssen, um den Schwerpunkt zu bilden.** Der Schwerpunkt sollte etwas Wichtiges sein, das Benutzer schnell finden und verstehen müssen.
-   **Platzieren Sie den Fokuspunkt in der oberen linken Ecke oder in der oberen Mitte.**
-   **Weisen Sie dem Fokuspunkt die größte visuelle Hervorhebung zu,** z. B. hervorgehobener Text, Standardauswahl oder anfänglicher Eingabefokus.

### <a name="alignment"></a>Ausrichtung

-   Verwenden Sie normalerweise die linke Ausrichtung.
-   Verwenden Sie die richtige Ausrichtung für numerische Daten, insbesondere Spalten numerischer Daten.
-   Verwenden Sie die rechte Ausrichtung für Commitschaltflächen sowie Steuerelemente, die am rechten Fensterrand ausgerichtet sind.
-   Verwenden Sie die zentrierte Ausrichtung, wenn die linke oder rechte Ausrichtung ungeeignet ist oder unausgewogen erscheint.
-   Wenn Steuerelemente vertikal an Text ausgerichtet werden, richten Sie die Textbaseline aus, um einen reibungslosen horizontalen Lesefluss zu ermöglichen.
-   Informationen zur Ausrichtung von Bezeichnungen finden Sie im Abschnitt [Bezeichnungsausrichtung](#label-alignment) unter Entwurfskonzepte.

### <a name="accessibility"></a>Zugriff

-   **Verwenden Sie layout nicht als einziges Mittel, um wichtige Informationen über eine Benutzeroberfläche zu vermitteln.** Benutzer mit Sehbehinderung können diese Präsentation möglicherweise nicht interpretieren. Stellen Sie beispielsweise sicher, dass Steuerelementbezeichnungen ihre Beziehung zu anderen Elementen kommunizieren.
-   **Betten Sie keine untergeordneten Steuerelemente in Steuerelementbezeichnungen ein, um einen Satz oder Ausdruck zu erstellen.** Solche Zuordnungen basieren ausschließlich auf dem Layout und werden von Tastaturnavigations- oder Hilfstechnologien für die Barrierefreiheit nicht gut verarbeitet. Darüber hinaus ist diese Technik nicht lokalisierbar, da die Satzstruktur je nach Sprache variiert.

    **Falsch:**

    ![Screenshot eines Textfelds in der Mitte eines Satzes ](images/vis-layout-image43.png)

    In diesem Beispiel wird das Textfeld fälschlicherweise innerhalb der Kontrollkästchenbezeichnung platziert.

    **Richtig:**

    ![Screenshot eines Textfelds am Ende eines Satzes ](images/vis-layout-image44.png)

    Hier wird das Textfeld hinter der Bezeichnung des Kontrollkästchens platziert.

-   **Machen Sie die Gruppierung zugänglich.** Gruppen, die durch Fensterbereiche, Gruppenfelder, Trennzeichen, Textbeschriftungen und Aggregatoren definiert werden, werden automatisch von Barrierefreiheitshilfen verarbeitet. Gruppen, die nur durch Platzierung und Hintergrund definiert werden, sind jedoch nicht und müssen programmgesteuert für die Barrierefreiheit definiert werden.

Weitere Richtlinien finden Sie unter [Barrierefreiheit.](inter-accessibility.md)

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größen- und Abstände

**Größensteuerung**

In der folgenden Tabelle sind die empfohlenen Größen (Breite x Höhe oder Höhe bei einer einzelnen Zahl) für allgemeine Benutzeroberflächenelemente (für 9 pt) aufgeführt. Segoe UI bei 96 dpi). Die Breite, die auf dem längsten Element in Englisch basiert, addiert 30 Prozent für die Lokalisierung (bis zu 200 Prozent für kürzeren Text) für jeden Text (aber keine Zahlen), der lokalisiert wird.



| Beispiel | Control | Dialogeinheiten | Relative Pixel |
|-------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| ![Screenshot der Kontrollkästchen und deren Bezeichnungen ](images/vis-layout-image45.png)<br/>       | Kontrollkästchen<br/>     | 10<br/>                                                                                     | 17<br/>                                                                                              |
| ![Screenshot des Kombinationsfelds ](images/vis-layout-image46.png)<br/>                          | Kombinationsfelder<br/>     | Breite des längsten Elements + 30 % x 14<br/>                                                       | Breite des längsten Elements + 30 % x 23<br/>                                                                |
| ![Screenshot einer Befehlsschaltfläche ](images/vis-layout-image47.png)<br/>                   | Befehlsschaltflächen<br/> | 50 x 14<br/>                                                                                | 75 x 23<br/>                                                                                         |
| ![Screenshot eines von zwei ausgewählten Befehlslinks ](images/vis-layout-image48.png)<br/>  | Befehlslinks<br/>   | 25 (eine Zeile) oder 35 (zwei Zeilen)<br/>                                                        | 41 (eine Zeile) oder 58 (zwei Zeilen)<br/>                                                                 |
| ![Screenshot einer Dropdownliste ](images/vis-layout-image49.png)<br/>                   | Dropdownlisten<br/> | Breite der längsten gültigen Daten + 30 % x 14<br/>                                                 | Breite des längsten Elements + 30 % x 23<br/>                                                                |
| ![Screenshot eines Listenfelds ](images/vis-layout-image50.png)<br/>                         | Listenfelder<br/>      | Breite des längsten Elements + 30 % x eine ganzzahlige Anzahl von Elementen (mindestens 3 Elemente)<br/>            |                                                                                                            |
| ![Screenshot einer Liste von Bilddateien ](images/vis-layout-image51.png)<br/>            | Listenansichten<br/>      | Spaltenbreiten, die abgeschnittene Daten x eine ganzzahlische Anzahl von Elementen vermeiden<br/>                 |                                                                                                            |
| ![Screenshot einer Statusleiste ](images/vis-layout-image52.png)<br/>                     | Statusleisten<br/>   | 107 oder 237 x 8<br/>                                                                         | 160 oder 355 x 15<br/>                                                                                 |
| ![Screenshot von Optionsfeldern ](images/vis-layout-image53.png)<br/>                      | Optionsfelder<br/>   | 10<br/>                                                                                     | 17<br/>                                                                                              |
| ![Screenshot des Schieberegler-Steuerelements ](images/vis-layout-image54.png)<br/>                     | Schieberegler<br/>         | 15<br/>                                                                                     | 24<br/>                                                                                              |
| ![Screenshot des Texts: "Zeitzone auswählen" ](images/vis-layout-image55.png)<br/>           | Text (statisch)<br/>   | 8<br/>                                                                                      | 13<br/>                                                                                              |
| ![Screenshot des leeren Textfelds ](images/vis-layout-image56.png)<br/>                     | Textfelder<br/>      | Breite der längsten oder erwarteten Eingabe + 30 % x 14 (eine Zeile) + 10 für jede zusätzliche Zeile<br/> | Breite der längsten gültigen Daten + 30 % x 23 relative Pixel (eine Zeile) + 16 für jede zusätzliche Zeile<br/> |
| ![Screenshot geschachtelter Ordner im Windows-Explorer ](images/vis-layout-image57.png)<br/> | Strukturansichten<br/>      | Breite des längsten Elements + 30 % x eine ganzzahlige Anzahl von Elementen (mindestens 5 Elemente)<br/>            |                                                                                                            |



 

**Abstand**

In der folgenden Tabelle sind die empfohlenen Abstande zwischen allgemeinen Benutzeroberflächenelementen (für 9 pt. Segoe UI bei 96 dpi).



|   &nbsp; | Element | Dialogeinheiten | Relative Pixel |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| ![Abbildung des Abstands in den Rändern des Dialogfelds ](images/vis_layout_image58.jpeg)<br/>        | Dialogfeldränder<br/>                                                                         | 7 auf allen Seiten<br/>                                                                 | 11 auf allen Seiten<br/>                                                                |
| ![Abbildung des Abstands zwischen Bezeichnungen und Steuerelementen ](images/vis_layout_image59.jpeg)<br/>  | Zwischen Textbezeichnungen und den zugehörigen Steuerelementen (z. B. Textfelder und Listenfelder)<br/> | 3<br/>                                                                              | 5<br/>                                                                              |
| ![Abbildung des Abstands zwischen verwandten Steuerelementen ](images/vis_layout_image60.jpeg)<br/>     | Zwischen verwandten Steuerelementen<br/>                                                                   | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Abbildung des Abstands zwischen nicht verknüpften Steuerelementen ](images/vis_layout_image61.jpeg)<br/>   | Zwischen nicht verknüpften Steuerelementen<br/>                                                                 | 7<br/>                                                                              | 11<br/>                                                                             |
| ![Abbildung des Abstands des ersten Steuerelements in einer Gruppe ](images/vis_layout_image62.jpeg)<br/>  | Erstes Steuerelement in einem Gruppenfeld<br/>                                                               | 11 unten im oberen Bereich des Gruppenfelds; Vertikale Ausrichtung am Titel des Gruppenfelds<br/> | 16 unten im oberen Bereich des Gruppenfelds; Vertikal am Titel des Gruppenfelds ausrichten<br/> |
| ![Aa511279.between-related(en-us,MSDN.10).jpg](images/vis_layout_image60.jpeg)<br/>         | Zwischen Steuerelementen in einem Gruppenfeld<br/>                                                            | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Abbildung: Abstand zwischen Schaltflächen ](images/vis_layout_image63.jpeg)<br/>              | Zwischen horizontal oder vertikal angeordneten Schaltflächen<br/>                                        | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Abbildung des Abstands des letzten Steuerelements in einer Gruppe ](images/vis_layout_image64.jpeg)<br/>   | Letztes Steuerelement in einem Gruppenfeld<br/>                                                                | 7 über dem unteren Rand des Gruppenfelds<br/>                                            | 11 über dem unteren Rand des Gruppenfelds<br/>                                           |
| ![Abbildung: Abstand vom linken Rand des Gruppenfelds ](images/vis_layout_image65.jpeg)<br/>  | Am linken Rand eines Gruppenfelds<br/>                                                          | 6<br/>                                                                              | 9<br/>                                                                              |
| ![Abbildung, die den Abstand der Textbezeichnung neben dem Steuerelement zeigt ](images/vis_layout_image66.jpeg)<br/> | Textbezeichnung neben einem Steuerelement<br/>                                                                | 3 unten vom oberen Teil des Steuerelements<br/>                                             | 5 nach unten vom oberen Teil des Steuerelements<br/>                                             |
| ![Abbildung: Abstand zwischen Textzeilen ](images/vis_layout_image67.jpeg)<br/>   | Zwischen Textzeilen<br/>                                                                 | 7<br/>                                                                              | 11<br/>                                                                             |
|                                                                                                   | Kleinster Bereich zwischen interaktiven Steuerelementen<br/>                                                | 3 oder kein Leerzeichen<br/>                                                                  | 5 oder kein Leerzeichen<br/>                                                                  |
|                                                                                                   | Kleinster Bereich zwischen einem nicht interaktiven Steuerelement und jedem anderen Steuerelement<br/>                     | 2<br/>                                                                              | 3<br/>                                                                              |



 

 

