---
title: Layout
description: Layout ist die Größe, der Abstand und die Platzierung von Inhalten innerhalb eines Fensters oder einer Seite.
ms.assetid: 39cd896f-d3cc-4768-a20c-a7f598da7136
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2bd705346f979a44cc2a8c7917f81b9e918ce5277893b5a377ab1ede4b945bb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816899"
---
# <a name="layout"></a>Layout

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Layout ist die Größe, der Abstand und die Platzierung von Inhalten innerhalb eines Fensters oder einer Seite. Ein effektives Layout ist entscheidend, um Benutzern zu helfen, schnell zu finden, was sie suchen, und die Darstellung visuell ansprechender zu gestalten. Ein effektives Layout kann den Unterschied zwischen designs machen, die Benutzer sofort verstehen, und den Entwürfen, bei denen sich Benutzer verunsichert und überfordert fühlen.

**Hinweis:** Richtlinien im Zusammenhang mit der [Fensterverwaltung](win-window-mgt.md) werden in einem separaten Artikel vorgestellt. Empfohlene spezifische Größen- und Abstandssteuerelements werden in den jeweiligen Richtlinienartikeln vorgestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="visual-hierarchy"></a>Visuelle Hierarchie

Ein Fenster oder eine Seite verfügt über eine klare visuelle Hierarchie, wenn ihre Darstellung die Beziehung und Priorität ihrer Elemente angibt. Ohne eine visuelle Hierarchie müssten Benutzer diese Beziehungen und Prioritäten selbst herausfinden.

Die visuelle Hierarchie wird erreicht, indem die folgenden Attribute gekonnt kombiniert werden:

-   **Fokus.** Das Layout gibt an, wo Benutzer zuerst suchen müssen.
-   **Flow.** Das Auge verläuft reibungslos und natürlich durch einen klaren Pfad durch die Oberfläche und sucht nach Elementen der Benutzeroberfläche (UI) in der reihenfolge, die für ihre Verwendung geeignet ist.
-   **Gruppierung.** Logisch verknüpfte Benutzeroberflächenelemente haben eine klare visuelle Beziehung. Verwandte Elemente werden gruppiert. Nicht verknüpfte Elemente sind getrennt.
-   **Schwerpunkt.** Benutzeroberflächenelemente werden basierend auf ihrer relativen Wichtigkeit hervorgehoben.
-   **Ausrichtung.** Die Benutzeroberflächenelemente verfügen über eine koordinierte Platzierung, sodass sie leicht überprüft werden können und ordnungsgemäß angezeigt werden.

Darüber hinaus weist das effektive Layout folgende Attribute auf:

-   **Geräteunabhängigkeit.** Das Layout wird unabhängig von der Schriftart oder Schriftgröße, den DPI-Punkten (Dots per Inch), der Anzeige oder dem Grafikadapter wie beabsichtigt angezeigt.
-   **Einfach zu überprüfen.** Benutzer können den gesuchten Inhalt auf einen Blick finden.
-   **Effizienz.** Benutzeroberflächenelemente, die groß sind, müssen groß sein, und elemente, die klein sind, funktionieren gut klein.
-   **Größenänderung.** Wenn hilfreich, kann die Größe eines Fensters geändert werden, und das Inhaltslayout ist unabhängig davon effektiv, wie groß oder klein die Oberfläche ist.
-   **Gleichgewicht.** Der Inhalt wird gleichmäßig über die Oberfläche verteilt angezeigt.
-   **Visuelle Einfachheit.** Die Wahrnehmung, dass ein Layout nicht komplizierter ist, als es sein muss. Benutzer werden durch die Darstellung des Layouts nicht überfordert.
-   **Konsistenz.** Ähnliche Fenster oder Seiten verwenden ein ähnliches Layout, sodass benutzer sich immer orientiert fühlen.

Obwohl Größe, Abstand und Platzierung einfache Konzepte sind, besteht die Herausforderung beim Layout darin, die richtige Mischung dieser Attribute zu erreichen.

In Windows wird das Layout mit geräteunabhängigen Metriken wie Dialogeinheiten (DLUs) und relativen Pixeln kommuniziert.

### <a name="a-design-model-for-reading"></a>Ein Entwurfsmodell zum Lesen

**Benutzer wählen aus, was sie anhand der Darstellung und Organisation des Inhalts lesen.** Um ein effektives Layout zu erstellen, müssen Sie verstehen, was Benutzer tendenziell lesen und warum.

Sie können Layoutentscheidungen treffen, indem Sie dieses Entwurfsmodell zum Lesen verwenden:

-   Personen lesen in einer Reihenfolge von links nach rechts von oben nach unten (in älteren Kulturen).
-   Es gibt zwei Lesemodi: immersives Lesen und Scannen. Das Ziel des immersiven Lesens ist das Verständnis.

    ![Abbildung des roten Pfeils im ickzung-Lesemuster ](images/vis-layout-image1.png)

    In diesem Diagramm wird das immersive Lesen modelliert.

    Im Gegensatz dazu besteht das Ziel der Überprüfung darin, Dinge zu finden. Der gesamte Scanpfad sieht wie folgt aus:

    ![Abbildung des roten Pfeils im diagonalen Lesemuster ](images/vis-layout-image2.png)

    In diesem Diagramm wird die Überprüfung modelliert.

    ![Abbildung eines roten Pfeils in einem Nach-unten- und Einem Bogenmuster ](images/vis-layout-image3.png)

    Wenn am linken Rand einer Seite Text ausgeführt wird, scannen Benutzer zuerst den linken Rand.

-   Bei der Verwendung von Software werden Benutzer nicht in der Benutzeroberfläche selbst, sondern in ihrer Arbeit unterstützt. Daher lesen Benutzer in der Regel keinen Benutzeroberflächentext, den sie scannen. Anschließend lesen sie Textbits nur dann umfassend, wenn sie der Meinung sind, dass sie dies benötigen.
-   Benutzer tendieren dazu, Navigationsfenster auf der linken oder rechten Seite einer Seite zu überspringen. Benutzer erkennen, dass sie vorhanden sind, sehen sich die Navigationsfenster jedoch nur an, wenn sie navigieren möchten.
-   Benutzer neigen dazu, große Blöcke von unformatiertem Text zu überspringen, ohne sie überhaupt zu lesen.

    ![Abbildung von Text mit Pfeilen zum Scannen von Text ](images/vis-layout-image4.png)

    Benutzer überspringen beim Scannen häufig große Textblöcke und Navigationsfenster.

-   Alles, was gleich ist, sehen Benutzer zuerst in der oberen linken Ecke eines Fensters, scannen über die Seite und beenden ihre Überprüfung in der unteren rechten Ecke. Sie ignorieren tendenziell die untere linke Ecke.

    ![Abbildung der Seite und des Pfeils von oben links nach unten nach rechts ](images/vis-layout-image5.png)

    Wenn alles gleich ist, lesen Benutzer diese Zahlen in der folgenden Reihenfolge: 1, 2, 4 und 3.

-   In der interaktiven Benutzeroberfläche sind jedoch nicht alle Elemente gleich, sodass verschiedene Benutzeroberflächenelemente unterschiedliche Aufmerksamkeitsebenen erhalten. Benutzer sehen sich interaktive Steuerelemente an, insbesondere Steuerelemente oben links und in der Mitte des Fensters sowie hervorgehobenen Text.

![Abbildung des Bildschirms mit spitzem und unscharfem Text ](images/vis-layout-image6.png)

Benutzer konzentrieren sich auf die wichtigsten interaktiven Steuerelemente und die hervorgehobene Hauptanweisung und sehen sich andere Dinge nur an, wenn sie dies benötigen.

-   Benutzer lesen in der Regel interaktive Steuerelementbezeichnungen, insbesondere solche, die für die Durchführung der jeweiligen Aufgabe relevant erscheinen. Im Gegensatz dazu lesen Benutzer statischen Text nur, wenn sie denken, dass sie dies benötigen.
-   Elemente, die anders aussehen, ziehen Aufmerksamkeit auf sich. Fetter Text und großer Text hebt sich vom normalen Text ab. Benutzeroberflächenelemente mit Farbe oder einem farbigen Hintergrund zeichnen sich aus. Elemente mit Symbolen heben sich von Elementen ohne Symbole ab.
-   Benutzer scrollen nur, wenn sie einen Grund dafür haben. Wenn der Inhalt [über dem Fold](glossary.md) keinen Grund für einen Bildlauf bereitstellt, ist dies nicht der Grund.
-   Sobald Benutzer entschieden haben, was sie tun sollen, beenden sie sofort die Überprüfung und tun dies.
-   Da Benutzer die Überprüfung beenden, wenn sie denken, dass sie fertig sind, ignorieren sie in der Regel alles, was über den scheinbaren Abschlusspunkt hinausgeht.

![Screenshot der Tastaturoptionen ](images/vis-layout-image7.png)

Benutzer beenden die Überprüfung, wenn sie denken, dass sie fertig sind.

Natürlich gibt es Ausnahmen für dieses allgemeine Modell. Eyetrackinggeräte deuten darauf hin, dass das Verhalten der echten Benutzer recht unregelmäßig ist. Das Ziel dieses Modells besteht darin, Ihnen dabei zu helfen, gute Entscheidungen zu treffen und Kompromisse zu treffen, anstatt das Benutzerverhalten genau zu modellieren. Aber wenn Sie diese Liste gelesen haben, haben Sie hoffentlich auch viele Ihrer eigenen Lesemuster erkannt.

### <a name="designing-for-scanning"></a>Entwerfen für die Überprüfung

**Benutzer lesen nicht, sie scannen, sodass Sie Benutzeroberflächen für die Überprüfung entwerfen sollten.** Gehen Sie nicht davon aus, dass Benutzer den Text in einer Reihenfolge von links nach rechts von oben nach unten lesen, sondern dass sie sich die Benutzeroberflächenelemente ansehen, die ihre Aufmerksamkeit auf sich ziehen.

So entwerfen Sie die Überprüfung:

-   Angenommen, Benutzer scannen zunächst schnell das gesamte Fenster und lesen dann die Benutzeroberflächenelemente in ungefähr der folgenden Reihenfolge:
    -   Interaktive Steuerelemente in der Mitte
    -   Die Commitschaltflächen
    -   An anderer Stelle gefundene interaktive Steuerelemente
    -   Hauptanweisung
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
-   Verwenden Sie hervorgehobenen Text, z.B. großen Text und fett formatierte Text.
-   Legen Sie Text ein, den Benutzer in interaktiven Steuerelementen, mit Symbolen oder auf [Bannern](vis-graphic.md)lesen müssen.
-   Verwenden Sie dunklen Text auf einem hellen Hintergrund.
-   Umranden Sie die Elemente mit einem verallgemerten Raum.
-   Sie benötigen keine Interaktion, z. B. zeigend oder mit dem Mauszeiger, um das Element anzuzeigen, das Sie hervorheben.

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

Bei der effektiven Verwendung des Bildschirmraums müssen Sie verschiedene Faktoren ausgleichen: Zu viel Platz zu verwenden, und ein Fenster wirkt stark und verschwenderisch und ist sogar schwer zu verwenden, basierend auf [dem Fitts-Gesetz.](inter-mouse.md)

**Falsch:**

![Screenshot mit zu viel Leerraum ](images/vis-layout-image10.png)

In diesem Beispiel ist das Fenster zu groß für seinen Inhalt.

Verwenden Sie andererseits zu wenig Platz, und ein Fenster wirkt verzeilt, unvorhergesehen und schwierig zu verwenden, wenn scrollen und andere Bearbeitungen erforderlich sind.

**Falsch:**

![Screenshot mit zu vielen Steuerelementen ](images/vis-layout-image11.png)

In diesem Beispiel ist das Fenster zu klein für seinen Inhalt.

Obwohl die kritische Benutzeroberfläche in die unterstützte [Mindestauflösung](glossary.md)passen muss, sollten Sie nicht davon ausgehen, dass die Verwendung des Bildschirmbereichs effektiv bedeutet, dass Fenster so klein wie möglich sein sollten. **Ein effektives Layout berücksichtigt den offenen Raum und versucht nicht, alles in den kleinstmöglichen Bereich zu verzweigen.** Moderne Bildschirme verfügen über erheblichen Bildschirmbereich, und es ist sinnvoll, diesen Bereich effektiv zu verwenden, wenn Sie dies können. Daher kann es sein, dass zu viel Bildschirmraum anstelle von zu wenig verwendet wird. Auf diese Weise werden Ihre Fenster leichter und leichter erreichbar.

Sie wissen, dass ein Layout bildschirmraum effektiv verwendet, wenn:

-   Windows, Fensterbereiche und Steuerelemente müssen nicht geändert werden, damit sie verwendet werden können. Wenn benutzer als Erstes die Größe eines Fensters, Bereichs oder Steuerelements ändern, ist seine Größe falsch.
-   Daten werden nicht abgeschnitten. Die meisten Daten in Listenansichten und Strukturansichten haben keine Ellipsen, und Daten in anderen Steuerelementen werden nur abgeschnitten, wenn die Datenlänge ungewöhnlich groß ist. Daten, die gelesen werden müssen, um eine Aufgabe auszuführen, sollten nicht abgeschnitten werden.
-   Die Fenster und Steuerelemente sind entsprechend dimensioniert, um unnötiges Scrollen zu vermeiden. Es gibt nur wenige horizontale Scrollleisten und keine unnötigen vertikalen Scrollleisten.
-   Steuerelemente verwenden größtenteils ihre Standardgrößen. Versuchen Sie, die Anzahl der Steuerelementgrößen zu reduzieren, indem Sie z. B. nur eine oder zwei Befehlsschaltflächenbreiten auf einer Oberfläche verwenden.
-   Die Benutzeroberfläche ist ausgeglichen. Es gibt keine großen nicht verwendeten Bildschirmbereiche.

Wählen Sie Fenstergrößen aus, die einfach groß genug sind, um ihren Zweck zu erfüllen. (Und wenn die Größe des Fensters geändert werden kann, gilt dieses Ziel für die Standardgröße.) **Eine Kombination aus abgeschnittenen Daten oder Scrollleisten und viel verfügbaren Bildschirmspeicherplatz ist ein klares Zeichen für ineffektives Layout.**

### <a name="control-sizing"></a>Größen von Steuerelementen

In der Regel besteht der erste Schritt bei der effektiven Verwendung des Bildschirmbereichs darin, die richtige Größe für die verschiedenen Benutzeroberflächenelemente zu bestimmen. Weitere Informationen finden Sie in den Artikeln zur Größenrichtlinie für Steuerelementen in der Tabelle control [sizing](#recommended-sizing-and-spacing) (Größe des Steuerelements) sowie in den empfohlenen Größen.

Das Fitts-Gesetz besagt, dass je kleiner ein Ziel ist, desto länger dauert es, es mit der Maus zu erhalten. Darüber hinaus kann die "Maus" bei Computern, die Windows Tablet- und Touchtechnologie verwenden, tatsächlich ein Stift oder der Finger des Benutzers sein. Daher sollten Sie alternative Eingabegeräte beim Bestimmen der Größen für kleine Steuerelemente in Betracht ziehen. **Eine Steuerelementgröße von 16 x 16 relativen Pixeln ist eine gute Mindestgröße für jedes Eingabegerät.** Im Gegensatz dazu sind die standardmäßigen 15 x 9 relativen Pixel-Drehsteuerelemente zu klein, um effektiv von Stiften verwendet zu werden.

### <a name="spacing"></a>Abstand

Durch die Bereitstellung von überflüssigen (aber nicht übermäßigen) Platz wird das Layout komfortabler und einfacher zu analysieren. Effektiver Speicherplatz ist kein ungenutzter Speicherplatz. Er spielt eine wichtige Rolle bei der Verbesserung der Scanfähigkeit für Benutzer und trägt auch zur visuellen Eignung Ihres Entwurfs bei. Richtlinien finden Sie in der [Abstandstabelle](#recommended-sizing-and-spacing).

Bei Computern, die Windows Tablet- und Touchtechnologie verwenden, ist die "Maus" möglicherweise tatsächlich ein Stift oder der Finger des Benutzers. Das Ziel ist schwieriger, wenn ein Stift oder Finger als zeigedes Gerät verwendet wird, was dazu führt, dass Benutzer außerhalb des vorgesehenen Ziels tippen. Wenn interaktive Steuerelemente sehr nah beieinander platziert werden, aber nicht tatsächlich berührt werden, können Benutzer zwischen den Steuerelementen auf den inaktiven Bereich klicken. Da das Klicken auf den inaktiven Bereich kein Ergebnis oder visuelles Feedback enthält, sind benutzer oft unsicher, was schief gelaufen ist. Wenn kleine Steuerelemente zu stark durch Leerzeichen getrennt sind, muss der Benutzer präzise tippen, um zu vermeiden, dass auf das falsche Objekt tippt. **Um diese Probleme zu beheben, sollten die Zielbereiche interaktiver Steuerelemente entweder berührt werden oder mindestens 3 DLUs (5 relative Pixel) Platz dazwischen haben.**

Sie wissen, dass ein Layout einen guten Abstand hat, wenn:

-   Insgesamt wirkt die Benutzeroberflächenoberfläche wohl und wirkt nicht überlastet.
-   Der Platz wird einheitlich und ausgeglichen angezeigt.
-   Verwandte Elemente sind nah beieinander, und nicht verknüpfte Elemente sind relativ weit voneinander entfernt.
-   Zwischen Steuerelementen, die zusammen sein sollen, wie z. B. Symbolleistenschaltflächen, ist kein leerer Speicherplatz vorhanden.

### <a name="resizable-windows"></a>Fenster mit größenveränderbarer Größe

Veränderbare Fenster sind auch ein Faktor bei der effektiven Verwendung des Bildschirmbereichs. Einige Fenster bestehen aus festem Inhalt und profitieren nicht davon, dass die Größe geändert werden kann, aber Fenster mit veränderlichem Inhalt sollten die Größe ändern können. Natürlich ist der Grund, warum Benutzer die Größe eines Fensters ändern, den zusätzlichen Bildschirmbereich zu erweitern, sodass der Inhalt entsprechend erweitert werden sollte, indem den Benutzeroberflächenelementen, die es benötigen, mehr Platz gegeben wird. Windows mit dynamischen Inhalten, Dokumenten, Bildern, Listen und Strukturen profitieren am meisten von veränderbaren Fenstern.

![Screenshot des Geänderten Steuerelements zum Abrufen der Bildlaufleiste ](images/vis-layout-image12.png)

In diesem Beispiel wird durch ändern der Größe des Fensters die Größe des Listenansicht-Steuerelements geändert.

Allerdings können Fenster zu breit gestreckt werden. Beispielsweise werden viele Systemsteuerungsseiten unhandlich, wenn der Inhalt breiter als 600 relative Pixel ist. In diesem Fall ist es besser, die Größe des Inhaltsbereichs nicht über diese maximale Breite hinaus zu ändern oder den Ursprung des Inhalts zu ändern, wenn die Größe des Fensters vergrößert wird. Behalten Sie stattdessen eine maximale Breite und einen festen linken oberen Ursprung bei.

Text wird schwierig zu lesen, wenn die Zeilenlänge zunimmt. Ziehen Sie für Textdokumente eine maximale Zeilenlänge von 80 Zeichen in Betracht, um den Text leicht lesbar zu machen. (Zeichen enthalten Buchstaben, Interpunktionszeichen und Leerzeichen.)

**Falsch:**

![Screenshot des breiten Meldungsfelds mit langem Text ](images/vis-layout-image13.png)

In diesem Beispiel erschwert die lange Textlänge das Lesen.

Schließlich müssen fensterfähige Fenster, deren Größe geändert werden kann, auch bildschirmraum effektiv verwenden, wenn sie verkleinert werden, indem sie verkleinerbare Inhalte verkleinert und Platz aus Benutzeroberflächenelementen entfernen, die ohne sie effektiv funktionieren können. Zu einem bestimmten Zeitpunkt werden das Fenster oder seine Benutzeroberflächenelemente zu klein, um verwendbar zu sein, sodass ihnen eine Mindestgröße zugewiesen oder einige Elemente vollständig entfernt werden sollten.

![Screenshot des Fensters mit einem hohen, aufdringlichen Menüband ](images/vis-layout-image14.png)

![Screenshot des Fensters ohne Menüband ](images/vis-layout-image15.png)

In diesem Beispiel hat der Bereich eine Mindestgröße.

Einige Programme profitieren von der Verwendung einer völlig anderen Darstellung, um den Inhalt in kleineren Größen nutzbar zu machen.

![Screenshot der zentrierten Media Player-Schaltflächen ](images/vis-layout-image16.png)

In diesem Beispiel ändert Windows Media Player sein Format, wenn das Fenster für das Standardformat zu klein wird.

### <a name="focus"></a>Fokus

Ein Layout hat den Fokus, wenn es einen offensichtlichen Ort gibt, an dem zuerst gesucht werden sollte. Der Fokus ist wichtig, um Benutzern zu zeigen, wo sie mit dem Scannen Ihres Fensters oder Ihrer Seite beginnen können. Ohne klaren Fokus bewegt sich das Auge des Benutzers ziellos. Der Schwerpunkt sollte etwas Wichtiges sein, das Benutzer schnell finden und verstehen müssen, und den größten visuellen Schwerpunkt haben. Die obere linke Ecke ist der natürliche Fokuspunkt für die meisten Fenster.

Es sollte nur ein Schwerpunktpunkt vorhanden sein. Genau wie in der Praxis kann sich das Auge immer nur auf eine Einzige konzentrieren, benutzer können sich nicht gleichzeitig auf mehrere Orte konzentrieren.

Um ein Benutzeroberflächenelement zum Mittelpunkt zu machen, können Sie es visuell hervorheben, indem Sie:

-   Platzieren Sie es im oberen linken oder oberen mittleren Teil der Oberfläche.
-   Verwenden von interaktiven Steuerelementen, die wichtig und leicht verständlich sind.
-   Verwenden von hervorgehobenen Texten, z. B. einer Hauptanweisung.
-   Festlegen der Standardauswahl und des anfänglichen Eingabefokus für die Steuerelemente.
-   Platzieren der Steuerelemente in einem anderen farbigen Hintergrund.

Erwägen Sie Windows Suche. Der Schwerpunkt für Windows Suchen sollte das Suchfeld sein, da es der Ausgangspunkt für die Aufgabe ist. Er befindet sich jedoch in der oberen rechten Ecke, um mit der Standardplatzierung des Suchfelds konsistent zu sein. Das Suchfeld hat den Eingabefokus, aber aufgrund seiner Position im Scanpfad reicht dieser Hinweis allein nicht aus.

Um dieses Problem zu beheben, gibt es im oberen mittleren Teil des Fensters eine hervorgehobene Anweisung, Benutzer an den richtigen Ort weiterzuleiten.

**Annehmbar:**

![Screenshot des Suchdialogfelds mit hilfreichen Text ](images/vis-layout-image17.png)

In diesem Beispiel werden Benutzer durch eine hervorgehobene Anweisung im oberen mittleren Bereich des Fensters zum Suchfeld geleitet.

Ohne die Anweisungen hätte das Fenster keinen offensichtlichen Schwerpunkt.

**Falsch:**

![Screenshot des Suchdialogfelds ohne Text ](images/vis-layout-image18.png)

Dieses Beispiel hat keinen offensichtlichen Schwerpunkt. Benutzer wissen nicht, wo sie suchen sollten.

Wenn Sie ein visuelles Element der Benutzeroberfläche hervorheben, stellen Sie sicher, dass die Aufmerksamkeit gerechtfertigt ist. Im vorherigen fehlerhaften Windows Search-Beispiel befindet sich die hervorgehobene Schaltfläche Alle in der oberen linken Ecke und hat die meisten visuellen Akzente, aber sie ist nicht der beabsichtigte Schwerpunkt. Benutzer sehen sich diese Schaltfläche möglicherweise an und versuchen herauszufinden, wie sie damit umgehen sollen.

**Falsch:**

![Screenshot der hervorgehobenen Schaltfläche "Alle" ](images/vis-layout-image19.png)

Ohne die hervorgehobene Anweisung als Fokuspunkt ist die hervorgehobene Schaltfläche Alle ein unbeabsichtigter Fokuspunkt.

### <a name="flow"></a>Flow

Ein Layout verfügt über einen Flow, wenn Benutzer reibungslos und natürlich durch einen klaren Pfad durch seine Oberfläche geführt werden, um Benutzeroberflächenelemente in der reihenfolge zu finden, die für ihre Verwendung geeignet ist. Nachdem Benutzer den Schwerpunkt identifiziert haben, müssen sie bestimmen, wie die Aufgabe abgeschlossen werden soll. Die Platzierung der Benutzeroberflächenelemente vermittelt ihre Beziehung und sollte die Schritte zum Ausführen der Aufgabe widerspiegeln. Dies bedeutet in der Regel, dass die Schritte der Aufgabe in einer Reihenfolge von links nach rechts von oben nach unten (in kulturellen Kulturen des Westens) natürlich ablaufen sollten.

Sie wissen, dass ein Layout einen guten Ablauf hat, wenn:

-   Die Platzierung der Benutzeroberflächenelemente spiegelt die Schritte wider, die Benutzer zum Ausführen der Aufgabe benötigen.
-   Benutzeroberflächenelemente, die eine Aufgabe initiieren, befinden sich in der oberen linken Ecke oder in der oberen Mitte.
-   Benutzeroberflächenelemente, die eine Aufgabe abschließen, befinden sich in der unteren rechten Ecke.
-   Verwandte Benutzeroberflächenelemente sind zusammen; Nicht verknüpfte Elemente sind getrennt.
-   Erforderliche Schritte befinden sich im Hauptablauf.
-   Optionale Schritte befinden sich außerhalb des Hauptablaufs und werden ggf. durch einen geeigneten Hintergrund oder eine progressive Offenlegung degrundiert.
-   Häufig verwendete Elemente werden vor selten verwendeten Elementen im Scanpfad angezeigt.
-   Benutzer wissen immer, was als Nächstes zu tun ist. Es gibt keine unerwarteten Sprünge oder Unterbrechungen im Taskflow.

**Falsch:**

![Screenshot des verwirrenden Dialogfeldlayouts ](images/vis-layout-image20.png)

In diesem Beispiel wissen Benutzer nicht, was als Nächstes zu tun ist. Es gibt unerwartete Sprünge und Unterbrechungen im Taskflow.

**Richtig:**

![Screenshot eines gut geplanten Dialogfelds ](images/vis-layout-image21.png)

In diesem Beispiel spiegelt die Darstellung der Benutzeroberflächenelemente die Schritte zum Ausführen der Aufgabe wider.

### <a name="grouping"></a>Gruppierung

Ein Layout verfügt über eine Gruppierung, wenn logisch verknüpfte Benutzeroberflächenelemente eine klare visuelle Beziehung aufweisen. Gruppen sind wichtig, da es für Benutzer einfacher ist, eine Gruppe verwandter Elemente zu verstehen und sich darauf zu konzentrieren, als die Elemente einzeln. Durch Gruppen wird ein Layout einfacher und einfacher zu analysieren.

Sie können die Gruppierung wie folgt anzeigen (in zunehmender Gewichtung):

-   **Layout.** Sie können verwandte Steuerelemente nebeneinander gruppieren und zusätzlichen Abstand zwischen nicht verknüpften Steuerelementen setzen.

    ![Abbildung von vier Symbolen mit vier Aufgabengruppen ](images/vis-layout-image22.png)

    In diesem Beispiel wird layout allein verwendet, um Steuerelementbeziehungen anzuzeigen.

-   **Trennzeichen.** Ein Trennzeichen ist eine horizontale oder vertikale Linie, die eine Gruppe von Steuerelementen vereinheitlicht. Trennzeichen bieten ein einfacheres, übersichtlicheres Aussehen. Im Gegensatz zu Gruppenfeldern funktionieren sie jedoch am besten, wenn sie sich über die gesamte Oberfläche erstrecken.

    ![Screenshot von drei Symbolen und drei Trennzeichen ](images/vis-layout-image23.png)

    In diesem Beispiel werden beschriftete Trennzeichen verwendet, um Steuerelementbeziehungen anzuzeigen.

-   **Aggregatoren.** Ein Aggregator ist eine Grafik, die eine visuelle Beziehung zwischen stark verknüpften Steuerelementen erstellt.

    ![Screenshot von Steuerelementen innerhalb einer elliptischen Linie ](images/vis-layout-image24.png)

    In diesem Beispiel wird ein Begrenzungsaggregator verwendet, um die Beziehung zwischen den Steuerelementen hervorzuheben und sie wie ein einzelnes Steuerelement statt acht zu gestalten.

-   **Gruppierungsfelder.** Ein Gruppenfeld ist ein beschrifteter rechteckiger Rahmen, der einen Satz verwandter Steuerelemente umgibt.

    ![Screenshot der Kontrollkästchen in einem rechteckigen Rahmen ](images/vis-layout-image25.png)

    In diesem Beispiel umschließt und bezeichnet ein Gruppenfeld einen Satz verwandter Steuerelemente.

-   **Hintergründe.** Sie können Hintergründe verwenden, um verschiedene Inhaltstypen hervorzuheben oder zu deaktivieren.

    ![Screenshot der linken Seite der Systemsteuerung ](images/vis-layout-image26.png)

    In diesem Beispiel wird der Aufgabenbereich der Systemsteuerung verwendet, um verwandte Aufgaben und Systemsteuerungselemente zu gruppieren.

    Um visuelle Überladen zu vermeiden, ist die leichteste Gewichtung, die den Auftrag gut erfüllt, die beste Wahl. Weitere Informationen finden Sie unter [Gruppenfelder,](ctrl-group-boxes.md) [Registerkarten,](ctrl-tabs.md) [Trennzeichen und Hintergründe.](vis-graphic.md)

Unabhängig vom Gruppierungsstil können Sie mithilfe von Einzug die Beziehung der Steuerelemente innerhalb einer Gruppe anzeigen. Steuerelemente, die Peers zueinander sind, sollten linksbündig ausgerichtet sein, und abhängige Steuerelemente werden mit 12 DLUs oder 18 relativen Pixeln eingerückt.

![Screenshot von drei Ebenen eingerückter Steuerelemente ](images/vis-layout-image27.png)

Abhängige Steuerelemente werden mit 12 DLUS oder 18 relativen Pixeln eingerückt. Dies ist standardmäßig der Abstand zwischen Kontrollkästchen und Optionsfeldern von ihren Bezeichnungen.

Sie wissen, dass ein Layout eine gute Gruppierung hat, wenn:

-   Das Fenster oder die Seiten umfassen höchstens 7 Gruppen.
-   Der Zweck jeder Gruppe ist offensichtlich.
-   Die Beziehung von Steuerelementen innerhalb jeder Gruppe ist offensichtlich, insbesondere die Abhängigkeit von Steuerelementen.
-   Die Gruppierung vereinfacht den Inhalt, anstatt ihn komplexer zu machen.

### <a name="alignment"></a>Ausrichtung

Ausrichtung ist die koordinierte Platzierung von Benutzeroberflächenelementen. Die Ausrichtung ist wichtig, da sie das Scannen von Inhalten vereinfacht und die Wahrnehmung der visuellen Komplexität durch die Benutzer beeinflusst.

Bei der Bestimmung der Ausrichtung müssen mehrere Ziele berücksichtigt werden:

-   **Einfaches horizontales Scannen.** Benutzer können horizontal lesen und verwandte Elemente nebeneinander ohne umständliche Lücken suchen.
-   **Einfaches vertikales Scannen.** Benutzer können Spalten verwandter Elemente scannen und mit minimaler horizontaler Augenbewegung sofort das gesuchte Element finden.
-   **Minimale visuelle Komplexität.** Benutzer betrachten ein Layout als visuell komplex, wenn es unnötige vertikale Ausrichtungsrasterlinien aufzuweisen hat.

### <a name="horizontal-alignment"></a>Horizontale Ausrichtung

**Linke Ausrichtung**

Aufgrund der Lesereihenfolge von links nach rechts funktioniert die linke Ausrichtung für die meisten Inhalte gut. Die linke Ausrichtung erleichtert das vertikale Scannen spaltenarer Daten.

**Rechtsausrichtung**

Die richtige Ausrichtung ist die beste Wahl für numerische Daten, insbesondere [für Spalten mit numerischen Daten.](ctrl-text-boxes.md) Die rechte Ausrichtung funktioniert auch gut für [Commitschaltflächen](glossary.md) sowie für Steuerelemente, die am rechten Fensterrand ausgerichtet sind.

![Screenshot der Nach-unten-Schaltfläche für die erweiterte Suche ](images/vis-layout-image28.png)

In diesem Beispiel ist die progressive Offenlegungssteuerung der erweiterten Suche rechtsbündig ausgerichtet, da sie am rechten Fensterrand platziert wird.

**Zentrierung**

Die zentrierte Ausrichtung ist am besten für Situationen reserviert, in denen die linke oder rechte Ausrichtung ungeeignet ist oder unausgewogen erscheint.

![Screenshot der zentrierten Media Player-Steuerelemente ](images/vis-layout-image29.png)

In diesem Beispiel wird das Media Player-Steuerelement zentriert, um eine ausgeglichene Darstellung zu ermöglichen.

Zentren Sie den Inhalt des Fensters nicht nur, um Platz zu füllen.

**Falsch:**

![Screenshot eines Fensters mit zu viel Leerraum ](images/vis-layout-image30.png)

In diesem Beispiel wird der Inhalt fälschlicherweise in einem Fenster mit größenveränderlicher Größe zentriert, um Platz zu füllen.

### <a name="vertical-alignment"></a>Vertikale Ausrichtung

**Elementanfangselemente**

Aufgrund der Lesereihenfolge von oben nach unten funktioniert die obere Ausrichtung für die meisten Inhalte gut. Die obere Ausrichtung erleichtert das horizontale Scannen von Benutzeroberflächenelementen.

**Textbaseline**

Wenn Steuerelemente vertikal an Text ausgerichtet werden, richten Sie die Textbaseline aus, um einen reibungslosen horizontalen Lesefluss zu ermöglichen.

**Richtig:**

![Screenshot der Schaltfläche und des ausgerichteten Bezeichnungstexts ](images/vis-layout-image31.png)

**Falsch:**

![Screenshot: Nicht ausgerichteter Schaltflächen- und Bezeichnungstext ](images/vis-layout-image32.png)

Im richtigen Beispiel werden das Steuerelement und seine Bezeichnung vertikal an ihren Textbasislinien ausgerichtet.

Sie wissen, dass ein Layout eine gute Ausrichtung hat, wenn:

-   Es ist einfach, sowohl horizontal als auch vertikal zu scannen.
-   Es hat eine einfache visuelle Darstellung.

### <a name="label-alignment"></a>Bezeichnungsausrichtung

Die allgemeinen Ausrichtungsregeln gelten für Steuerelementbezeichnungen, aber es handelt sich um ein häufiges Problem, das bestimmte Aufmerksamkeit betrifft. Die Ausrichtung von Bezeichnungen hat folgende Ziele:

-   Einfaches vertikales Scannen, um das richtige Steuerelement zu finden.
-   Einfaches horizontales Scannen, um Bezeichnungen ihren Steuerelementen zuzuordnen.
-   Einfache Lokalisierung, Behandlung von Bezeichnungen, die sich in verschiedenen Sprachen unterscheiden.
-   Funktioniert gut mit einer Mischung verschiedener Bezeichnungslängen.
-   Ermöglicht eine effiziente Nutzung des verfügbaren Speicherplatzes und vermeidet abgeschnittenen Text.

Das Allgemeine Ziel besteht darin, die Menge der Augenbewegungen zu reduzieren, die erforderlich sind, um zu ermitteln, welche Benutzer wahrscheinlich suchen, aber die Art der Steuerelemente und die Benutzer suchen, hängt vom Kontext ab.

Es gibt vier allgemeine Bezeichnungsplatzierungs- und Ausrichtungsstile mit jeweils ihren Vorteilen:

-   Linksbündige Bezeichnungen über Steuerelementen
-   Linksbündige Bezeichnungen auf der linken Seite von Steuerelementen
-   Linksbündige Bezeichnungen auf der linken Seite von Steuerelementen, Steuerelemente mit Unregelmäßigen auf der linken Seite
-   Rechtsbündige Bezeichnungen links von Steuerelementen

**Linksbündige Bezeichnungen über Steuerelementen**

Dieser Stil ist am einfachsten zu lokalisieren, da das Layout nicht von der Länge der Bezeichnungen abhängt, aber den meisten vertikalen Platz benötigt.

![list mit zwei Spalten von Bezeichnungen über Steuerelementen ](images/vis-layout-image33.png)

Dieser Stil nimmt den meisten vertikalen Platz ein, ist aber am einfachsten zu lokalisieren. Es ist eine bessere Wahl für die Bezeichnung von größtenteils interaktiven Steuerelementen.

Am besten verwendet, wenn:

-   Die bezeichneten Steuerelemente sind interaktiv (nicht nur Text).
-   Die Benutzeroberfläche wird lokalisiert. Dieser Stil bietet häufig Platz, um die Länge der Bezeichnung zu verdoppelt oder sogar zu verdreifachen.
-   Die Benutzeroberfläche verwendet eine Technologie für ein festes Layout (z.B. Win32).
-   Es gibt zehn oder weniger Steuerelemente. Mit mehr Steuerelementen sind die Bezeichnungen schwer zu überprüfen.
-   Es ist ausreichend vertikaler Platz für die Bezeichnungen vorhanden.
-   Das Layout muss frei sein, nicht nur Spalten.

**Linksbündige Bezeichnungen auf der linken Seite von Steuerelementen**

Dieser Stil ist am einfachsten vertikal zu scannen und funktioniert auch gut, wenn sich Bezeichnungen stark in der Länge unterscheiden, aber es ist schwieriger, die Bezeichnung mit ihrem Steuerelement zu verknüpfen. In diesem Stil können bei Bedarf mehrzeilige Bezeichnungen verwendet werden.

![Liste mit vier Spalten mit Bezeichnungen links von Steuerelementen ](images/vis-layout-image34.png)

Dieser Stil funktioniert gut. Es gibt jedoch zwei Spalten, aber visuell sieht es so aus, als ob es vier gibt, wodurch die Daten komplexer erscheinen.

Am besten verwendet, wenn:

-   Benutzer werden wahrscheinlich vertikal überprüfen, um bestimmte Bezeichnungen zu finden.
-   Benutzer lesen die Bezeichnungen und Steuerelemente wahrscheinlich nicht von links nach rechts, von oben nach unten.
-   Es ist ausreichend horizontaler Platz für die Bezeichnungen vorhanden.
-   Die Länge der Bezeichnungen variiert erheblich.
-   Es gibt viele Steuerelemente, z. B. mit Formularen.
-   Es gibt nur wenige Spalten. Die Bezeichnungen und Steuerelemente werden visuell als zwei einzelne Spalten angezeigt.

**Linksbündige Bezeichnungen auf der linken Seite von Steuerelementen, Steuerelemente mit Unregelmäßigen auf der linken Seite**

Dieser Stil erleichtert das vertikale Scannen der Bezeichnungen und der Bezeichnungen und Steuerelemente horizontal und ist sehr platzeffizient. es ist jedoch schwieriger, die Steuerelemente vertikal zu überprüfen. Die Steuerelemente werden rechts ausgerichtet, um den verfügbaren Speicherplatz voll zu nutzen.

![Liste mit zwei Spalten von Bezeichnungen mit unregelmäßigen Steuerelementen ](images/vis-layout-image35.png)

Dieser Stil ist kompakt und leicht zu lesen, aber es ist schwierig, Steuerelemente vertikal zu scannen.

Am besten verwendet, wenn:

-   Die Benutzeroberfläche verwendet eine Variable Layout-Technologie (z.B. Windows Presentation Foundation).
-   Benutzer werden wahrscheinlich vertikal überprüfen, um bestimmte Bezeichnungen zu finden.
-   Benutzer lesen die Bezeichnungen und Steuerelemente wahrscheinlich von links nach rechts und von oben nach unten.
-   Benutzer werden die Steuerelemente wahrscheinlich nicht vertikal scannen.
-   Der Steuerelementtext variiert in seiner Länge und wird wahrscheinlich abgeschnitten, wenn ein anderer Stil verwendet wird.
-   Die Steuerelemente sind schreibgeschützt, z. B. schreibgeschützte Textfelder. Bei anderen Steuerelementen sieht diese Ausrichtung schlampig aus. Die Steuerelemente können jedoch beim Klicken bearbeitet werden.
-   Es gibt viele Spalten, aber nur wenige Steuerelemente in einer Spalte.

**Rechtsbündige Bezeichnungen links von Steuerelementen**

Dieser Stil ist am einfachsten horizontal zu lesen, um die Bezeichnungen ihren Steuerelementen zuzuordnen. Es ist jedoch schwierig, die Bezeichnungen vertikal zu scannen, und funktioniert nicht gut, wenn labelsList mit eingerückten Bezeichnungen und Steuerelementen sich in der Länge stark unterscheidet.

![List mit eingerückten Bezeichnungen und Steuerelementen ](images/vis-layout-image36.png)

Dieser Stil ermöglicht ein einfaches vertikales Scannen der Steuerelemente, macht es jedoch schwierig, die Bezeichnungen vertikal zu scannen.

Am besten verwendet, wenn:

-   Benutzer lesen die Bezeichnungen und Steuerelemente wahrscheinlich von links nach rechts und von oben nach unten.
-   Benutzer werden wahrscheinlich nicht vertikal überprüfen, um bestimmte Bezeichnungen zu finden, möglicherweise aus folgenden Umständen:
    -   Es gibt einige Steuerelemente.
    -   Die Bezeichnungen sind bekannt.
    -   Die Steuerelemente sind größtenteils selbsterklärend und selten leer (möglicherweise mit Standardwerten, um leere Steuerelemente zu verhindern).
-   Es ist ausreichend horizontaler Platz für die Bezeichnungen vorhanden.
-   Die Länge der Bezeichnungen variiert nicht erheblich.
-   Viele Spalten vorhanden sind. Die Bezeichnungen und Steuerelemente werden visuell als einzelne Spalte angezeigt.

Bevor Sie einen dieser Stile übernehmen, sollten Sie jedoch zwei weitere Faktoren berücksichtigen:

-   Bevorzugen Sie einen Stil, den Sie konsistent im gesamten Programm verwenden können.
-   Linksbündige Bezeichnungen, die sich entweder über Steuerelementen links von Steuerelementen befinden, sind die gängigsten Stile, daher sollten sie bevorzugt werden.

### <a name="balance"></a>Balance

Ein Fenster oder eine Seite weist einen Ausgleich auf, wenn der Inhalt gleichmäßig über die Oberfläche verteilt angezeigt wird. Wenn die Oberfläche physisch die gleiche Gewichtung wie visuell hat, würde ein ausgeglichenes Layout nicht auf eine Seite springen.

Das häufigste Balanceproblem besteht darin, zu viele Inhalte auf der linken Seite eines Fensters oder einer Seite zu haben. Sie können einen Ausgleich auf folgende Weise erstellen:

-   Verwenden sie größere Ränder auf der linken Seite als die rechte.
-   Platzieren von Benutzeroberflächenelementen, die zum Ausführen einer Aufgabe verwendet werden, auf der rechten Seite.
-   Platzieren von Benutzeroberflächenelementen, die während der gesamten Aufgabe in der Mitte verwendet werden.
-   Verlängern von Größenänderungssteuerelementen oder mehrzeiligen Steuerelementen.
-   Strategische Verwendung der zentrieren Ausrichtung.

![Screenshot des Druckers auf der linken Seite und text auf der rechten Seite ](images/vis-layout-image37.png)

Dieses gut ausgeglichene Seitenlayout des Assistenten zeigt einen größeren linken Rand als rechts an, um das Gleichgewicht zu verbessern.

Wenn diese Techniken kein Gleichgewicht erreichen, sollten Sie erwägen, die Breite des Fensters oder der Seite zu verringern, um den Inhalt besser abzugleichen.

Zentrieren Sie Inhalte bei oberflächenveränderbaren Oberflächen nicht nur, um ein Gleichgewicht zu erzielen. Behalten Sie stattdessen einen festen linken oberen Ursprung bei, definieren Sie eine maximale Oberfläche, und ausgleichen Sie den Inhalt innerhalb des verwendeten Bereichs.

### <a name="grids"></a>Raster

Ein Raster ist ein unsichtbares zugrunde liegendes Ausrichtungssystem. Raster können symmetrisch sein, asymmetrische Raster funktionieren jedoch genauso gut. Bei Verwendung durch ein einzelnes Fenster oder eine Seite helfen Raster beim Organisieren von Inhalten auf einer Oberfläche. Bei der Wiederverwendung erstellen Raster ein konsistentes Layout für alle Oberflächen.

Die Anzahl der Rasterlinien wirkt sich auf die Wahrnehmung der visuellen Komplexität aus. Ein Layout mit weniger Rasterlinien erscheint einfacher als ein Layout mit mehr Rasterlinien.

**Visuell komplex:**

![Screenshot des überladenen Dialogfelds ](images/vis-layout-image38.png)

**Visuell einfach:**

![Screenshot des organisierten Dialogfelds ](images/vis-layout-image39.png)

Unnötige Rasterlinien sorgen für visuelle Komplexität.

Sie wissen, dass ein Layout Raster effektiv verwendet, wenn:

-   Windows oder Seiten mit ähnlichem Inhalt oder ähnlicher Funktion weisen ein ähnliches Layout auf.
-   Wiederholte Entwurfselemente werden an ähnlichen Stellen über Fenster und Seiten hinweg angezeigt.
-   Es gibt keine unnötigen vertikalen und horizontalen Ausrichtungsrasterlinien.

### <a name="visual-simplicity"></a>Visuelle Einfachheit

Visuelle Einfachheit ist die Wahrnehmung, dass ein Layout nicht komplizierter ist, als es sein muss.

Sie wissen, dass ein Layout visuelle Einfachheit hat, wenn es:

-   Entfernt unnötige Ebenen von Fenster chrome.
-   Stellt den Inhalt mit höchstens sieben leicht identifizierbaren Gruppen dar.
-   Verwendet einfache Gruppierung, z. B. Layout und Trennzeichen anstelle von Gruppenfeldern.
-   Verwendet einfache Steuerelemente wie Links anstelle von Befehlsschaltflächen für sekundäre Befehle und Dropdownlisten anstelle von Listen für Auswahlmöglichkeiten.
-   Reduziert die Anzahl der vertikalen und horizontalen Ausrichtungsrasterlinien.
-   Reduziert die Anzahl der Steuerelementgrößen, indem z. B. nur eine oder zwei Befehlsschaltflächenbreiten auf einer Oberfläche verwendet werden.
-   Verwendet die progressive Offenlegung, um Benutzeroberflächenelemente auszublenden, bis sie benötigt werden.
-   Verwendet ausreichend Speicherplatz, damit das Fenster oder die Seite nicht verdrängt ist.
-   Passt Fenster und Steuerelemente entsprechend an, um unnötiges Scrollen zu vermeiden.
-   Verwendet eine einzelne Schriftart mit einer kleinen Anzahl von Größen und Textfarben.

Allgemein gilt: Wenn ein Layoutelement entfernt werden kann, ohne die Effektivität der Benutzeroberfläche zu beeinträchtigen, sollte dies wahrscheinlich sein.

## <a name="guidelines"></a>Richtlinien

### <a name="screen-resolution-and-dpi"></a>Bildschirmauflösung und DPI

-   **Unterstützen Sie die minimale Windows effektive Auflösung von 800 x 600 Pixeln.** Für kritische UIs, die im abgesicherten Modus funktionieren müssen, wird eine effektive Auflösung von 640 x 480 Pixel unterstützt. Achten Sie darauf, den von der Taskleiste belegten Speicherplatz zu berücksichtigen, indem Sie 48 vertikale [relative Pixel](glossary.md) für Fenster reservieren, die mit der Taskleiste angezeigt werden.
-   **Optimieren Sie größenveränderbare Fensterlayouts für eine effektive Auflösung von 1024 x 768 Pixeln.** Ändern Sie die Größe dieser Fenster für niedrigere Bildschirmauflösungen automatisch auf eine Weise, die weiterhin funktionsfähig ist.
-   **Stellen Sie sicher, dass Sie Ihre Fenster in den Modi 96 Punkte pro Zoll (dpi) (bei 800 x 600 Pixel), 120 dpi (bei 1024 x 768 Pixel) und 144 dpi (bei 1200 x 900 Pixel) testen.** Überprüfen Sie, ob Layoutprobleme auftreten, z. B. Das Ausschneiden von Steuerelementen, Text und Fenstern und das Strecken von Symbolen und Bitmaps.
-   **Für Programme mit Toucheingabe- und mobilen Verwendungsszenarien optimieren Sie für 120 dpi.** Bildschirme mit hohem DPI-Wert sind derzeit auf Touch- und mobilen PCs weit verbreitet.

### <a name="window-size"></a>Fenstergröße

-   **Wählen Sie eine für den Inhalt geeignete Standardfenstergröße aus.** Sie sollten keine größeren Anfangsfenster verwenden, wenn Sie den Platz effektiv nutzen können.
-   **Verwenden Sie ein ausgewogenes Seitenverhältnis zwischen Höhe und Breite.** Ein Seitenverhältnis zwischen 3:5 und 5:3 wird bevorzugt, obwohl ein Seitenverhältnis von 1:3 für Meldungsdialogfelder (z. B. Fehler und Warnungen) verwendet werden kann.
-   **Verwenden Sie nach Möglichkeit fensterveränderbare Fenster, um Scrollleisten und abgeschnittene Daten zu vermeiden.** Windows mit dynamischen Inhalten, Dokumenten, Bildern, Listen und Strukturen profitieren am meisten von fensteränderbaren Fenstern.
-   **Ziehen Sie für Textdokumente eine maximale Zeilenlänge von 80 Zeichen** in Betracht, um den Text leicht lesbar zu machen. (Zeichen enthalten Buchstaben, Interpunktionszeichen und Leerzeichen.)
-   Fenster mit fester Größe:
    -   **Fenster mit fester Größe müssen vollständig sichtbar und dimensioniert sein, damit sie in den Arbeitsbereich passen.**
-   Fenster mit größenveränderbarer Größe:
    -   **Fenster mit größenveränderlicher Größe können für höhere Auflösungen optimiert werden, aber die Größe wird nach Bedarf zur Anzeigezeit auf die tatsächliche Bildschirmauflösung angepasst.**
    -   **Progressiv größere Fenster müssen progressiv mehr Informationen anzeigen.** Stellen Sie sicher, dass mindestens ein Fensterteil oder -steuerelement über inhalte verfügt, deren Größe geändert werden kann.
    -   **Behalten Sie den linken oberen Ursprung des Inhalts bei, wenn die Größe des Fensters geändert wird.** Verschieben Sie den Ursprung nicht, um den Inhalt auszugleichen, wenn sich die Fenstergröße ändert.
    -   **Legen Sie eine maximale Inhaltsgröße fest, wenn der Inhalt zu breit gestreckt werden kann.** Wenn der Inhalt unhandlich wird, sollten Sie die Größe des Inhaltsbereichs nicht über die maximale Breite hinaus ändern oder den Ursprung des Inhalts ändern, wenn die Größe des Fensters vergrößert wird. Behalten Sie stattdessen eine maximale Breite und einen festen linken oberen Ursprung bei.
    -   **Legen Sie eine minimale Fenstergröße fest, wenn eine Größe vorhanden ist, unter der der Inhalt nicht mehr verwendet werden kann.** Legen Sie bei Steuerelementen, deren Größe geändert werden kann, die minimalen Größen für größenveränderbare Elemente auf ihre kleinsten Funktionalen Größen fest, z. B. minimale Funktionale Spaltenbreiten in Listenansichten. Optionale Benutzeroberflächenelemente sollten vollständig entfernt werden.
    -   **Ändern Sie die Präsentation, um den Inhalt in kleineren Größen nutzbar zu machen.**

        ![Screenshot von Media Player-Steuerelementen ](images/vis-layout-image16.png)

        In diesem Beispiel ändert Windows Media Player sein Format, wenn das Fenster für das Standardformat zu klein wird.

### <a name="control-size"></a>Steuerelementgröße

-   **Machen Sie alle interaktiven Steuerelemente mit mindestens 16 x 16 Pixeln relativ.** Dies funktioniert gut für alle Eingabegeräte, einschließlich Windows Tablet- und Touchtechnologie.
-   **Größensteuerelemente, um abgeschnittene Daten zu vermeiden.** Abschneiden Sie keine Daten, die gelesen werden müssen, um eine Aufgabe auszuführen. Spalten der Größenlistenansicht, um abgeschnittene Daten zu vermeiden.
-   **Größensteuerelemente, um unnötiges Scrollen zu vermeiden.** Sorgen Sie dafür, dass Steuerelemente etwas größer werden, wenn dadurch eine Scrollleiste entfernt wird. Es sollten einige vertikale Scrollleisten und keine unnötigen horizontalen Scrollleisten vorhanden sein.

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

-   **Wenn Steuerelemente nicht berührt werden, befinden sich zwischen ihnen mindestens drei DLUs (5 relative Pixel).** Andernfalls können Benutzer zwischen den Steuerelementen auf inaktiven Bereich klicken. Da das Klicken auf den inaktiven Bereich kein Ergebnis oder visuelles Feedback enthält, sind benutzer oft unsicher, was schief gelaufen ist.

### <a name="placement"></a>Platzierung

-   **Ordnen Sie die Benutzeroberflächenelemente innerhalb einer Oberfläche so an, dass sie in natürlicher Reihenfolge von links nach rechts und von oben nach unten (in kulturellen Kulturen des Westens) fließen.** Die Platzierung der Benutzeroberflächenelemente vermittelt ihre Beziehung und sollte die Schritte zum Ausführen der Aufgabe widerspiegeln.
-   **Platzieren Sie Benutzeroberflächenelemente, die eine Aufgabe initiieren, in der oberen linken Ecke oder in der oberen Mitte.** Geben Sie dem Benutzeroberflächenelement, das Benutzer zuerst betrachten sollten, die größte visuelle Hervorhebung.
-   **Platzieren Sie Benutzeroberflächenelemente, die eine Aufgabe abschließen, in der unteren rechten Ecke.**
-   **Platzieren Sie verwandte Benutzeroberflächenelemente zusammen, und trennen Sie nicht verbundene Elemente.**
-   **Platzieren Sie die erforderlichen Schritte im Hauptflow.**
-   **Platzieren Sie optionale Schritte außerhalb des Hauptflusses,** möglicherweise mithilfe eines geeigneten Hintergrunds oder einer geeigneten progressiven Offenlegung.
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

    Hier wird das Textfeld hinter der Kontrollkästchenbezeichnung platziert.

-   **Machen Sie die Gruppierung zugänglich.** Gruppen, die durch Fensterbereiche, Gruppenfelder, Trennzeichen, Textbeschriftungen und Aggregatoren definiert werden, werden automatisch von Barrierefreiheitshilfen verarbeitet. Gruppen, die nur durch Platzierung und Hintergrund definiert werden, sind jedoch nicht und müssen programmgesteuert für die Barrierefreiheit definiert werden.

Weitere Richtlinien finden Sie unter [Barrierefreiheit.](inter-accessibility.md)

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größen- und Abstände

**Größen von Steuerelementen**

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
| ![Abbildung des Abstands zwischen Bezeichnungen und Steuerelementen ](images/vis_layout_image59.jpeg)<br/>  | Zwischen Textbeschriftungen und den zugehörigen Steuerelementen (z. B. Textfelder und Listenfelder)<br/> | 3<br/>                                                                              | 5<br/>                                                                              |
| ![Abbildung: Abstand zwischen verwandten Steuerelementen ](images/vis_layout_image60.jpeg)<br/>     | Zwischen verwandten Steuerelementen<br/>                                                                   | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Abbildung des Abstands zwischen nicht verknüpften Steuerelementen ](images/vis_layout_image61.jpeg)<br/>   | Zwischen nicht verknüpften Steuerelementen<br/>                                                                 | 7<br/>                                                                              | 11<br/>                                                                             |
| ![Abbildung des Abstands des ersten Steuerelements in einer Gruppe ](images/vis_layout_image62.jpeg)<br/>  | Erstes Steuerelement in einem Gruppenfeld<br/>                                                               | 11 unten im oberen Bereich des Gruppenfelds; Vertikal am Titel des Gruppenfelds ausrichten<br/> | 16 unten im oberen Bereich des Gruppenfelds; Vertikal am Titel des Gruppenfelds ausrichten<br/> |
| ![Aa511279.between-related(en-us,MSDN.10).jpg](images/vis_layout_image60.jpeg)<br/>         | Zwischen Steuerelementen in einem Gruppenfeld<br/>                                                            | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Abbildung: Abstand zwischen Schaltflächen ](images/vis_layout_image63.jpeg)<br/>              | Zwischen horizontal oder vertikal angeordneten Schaltflächen<br/>                                        | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Abbildung: Abstand des letzten Steuerelements in einer Gruppe ](images/vis_layout_image64.jpeg)<br/>   | Letztes Steuerelement in einem Gruppenfeld<br/>                                                                | 7 über dem unteren Rand des Gruppenfelds<br/>                                            | 11 über dem unteren Rand des Gruppenfelds<br/>                                           |
| ![Abbildung: Abstand vom linken Rand des Gruppenfelds ](images/vis_layout_image65.jpeg)<br/>  | Am linken Rand eines Gruppenfelds<br/>                                                          | 6<br/>                                                                              | 9<br/>                                                                              |
| ![Abbildung, die den Abstand der Textbezeichnung neben dem Steuerelement zeigt ](images/vis_layout_image66.jpeg)<br/> | Textbezeichnung neben einem Steuerelement<br/>                                                                | 3 unten vom oberen Teil des Steuerelements<br/>                                             | 5 nach unten vom oberen Ende des Steuerelements<br/>                                             |
| ![Abbildung: Abstand zwischen Textzeilen ](images/vis_layout_image67.jpeg)<br/>   | Zwischen Textzeilen<br/>                                                                 | 7<br/>                                                                              | 11<br/>                                                                             |
|                                                                                                   | Kleinster Bereich zwischen interaktiven Steuerelementen<br/>                                                | 3 oder kein Leerzeichen<br/>                                                                  | 5 oder kein Leerzeichen<br/>                                                                  |
|                                                                                                   | Kleinster Bereich zwischen einem nicht interaktiven Steuerelement und jedem anderen Steuerelement<br/>                     | 2<br/>                                                                              | 3<br/>                                                                              |



 

 

