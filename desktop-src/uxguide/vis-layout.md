---
title: Layout
description: Layout gibt die Größe, den Abstand und die Platzierung von Inhalten in einem Fenster oder einer Seite an.
ms.assetid: 39cd896f-d3cc-4768-a20c-a7f598da7136
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: f6b33375cbb679cc7c7efdeb12e5cd30be6280c5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104218945"
---
# <a name="layout"></a>Layout

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Layout gibt die Größe, den Abstand und die Platzierung von Inhalten in einem Fenster oder einer Seite an. Das effektive Layout ist wichtig, um Benutzern zu helfen, schnell zu ermitteln, was Sie suchen, und die Darstellung visuell ansprechend zu gestalten. Das effektive Layout kann den Unterschied zwischen den Entwürfen unterscheiden, die Benutzer sofort verstehen, und der Benutzer, die das Gefühl haben, dass Benutzer verwirrt

**Hinweis:** Die Richtlinien für die [Fensterverwaltung](win-window-mgt.md) werden in einem separaten Artikel dargestellt. Empfohlene spezifische Steuerelement Größen und Abstände werden in den jeweiligen Richtlinien Artikeln angezeigt.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="visual-hierarchy"></a>Visuelle Hierarchie

Ein Fenster oder eine Seite weist eine eindeutige visuelle Hierarchie auf, wenn die Darstellung die Beziehung und die Priorität der zugehörigen Elemente angibt. Ohne eine visuelle Hierarchie müssten Benutzer diese Beziehungen und Prioritäten selbst ermitteln.

Die visuelle Hierarchie wird erzielt, indem die folgenden Attribute gekonnt kombiniert werden:

-   **Liegt.** Das Layout gibt an, wo Benutzer zuerst suchen müssen.
-   **Rom.** Das Auge fließt reibungslos und natürlich durch einen klaren Weg durch die Oberfläche, wobei Elemente der Benutzeroberfläche (UI) in der für ihre Verwendung geeigneten Reihenfolge gefunden werden.
-   **Bündelung.** Logisch verwandte Benutzeroberflächen Elemente haben eine klare visuelle Beziehung. Verwandte Elemente werden gruppiert. nicht verknüpfte Elemente sind separat.
-   **Akzente.** Elemente der Benutzeroberfläche werden basierend auf ihrer relativen Wichtigkeit hervorgehoben.
-   **Richt.** Die Benutzeroberflächen Elemente verfügen über eine koordinierte Platzierung, sodass Sie leicht zu scannen sind und ordnungsgemäß angezeigt werden.

Außerdem weist das effektive Layout folgende Attribute auf:

-   **Geräteunabhängigkeit.** Das Layout wird unabhängig von Schriftart, Größe, dpi (dpi), Display und Grafik Adaptor als beabsichtigt angezeigt.
-   **Leicht zu scannen.** Benutzer können auf einen Blick den gesuchten Inhalt finden.
-   **Leistung.** Große Benutzeroberflächen Elemente müssen groß sein, und Elemente, die klein sind, sind sehr klein.
-   **Größe der Größe.** Wenn dies hilfreich ist, kann die Größe eines Fensters geändert werden, und das Inhalts Layout ist unabhängig davon wirksam, wie groß oder klein die Oberfläche ist.
-   **Schwebe.** Der Inhalt wird gleichmäßig auf die Oberfläche verteilt angezeigt.
-   **Visuelle Einfachheit.** Der Eindruck, dass ein Layout nicht komplizierter ist als es sein muss. Benutzer fühlen sich nicht durch die Darstellung des Layouts überlastet.
-   **Konsistenz.** Ähnliche Fenster oder Seiten verwenden ein ähnliches Layout, sodass sich Benutzer immer als orientiert fühlen.

Beim Anpassen der Größe, des Abstands und der Platzierung handelt es sich um einfache Konzepte, die Herausforderung beim Layout besteht jedoch darin, die richtige Mischung dieser Attribute zu erzielen.

In Windows wird das Layout mithilfe von geräteunabhängigen Metriken wie Dialog Einheiten (DLUs) und relativen Pixeln kommuniziert.

### <a name="a-design-model-for-reading"></a>Ein Entwurfs Modell zum Lesen

**Benutzer wählen, was Sie von der Darstellung und Organisation des Inhalts gelesen haben.** Um ein effektives Layout zu erstellen, müssen Sie verstehen, was Benutzer tendenziell lesen und warum.

Mithilfe dieses Entwurfs Modells können Sie Layoutentscheidungen treffen, um Folgendes zu lesen:

-   Personen, die von links nach rechts, von oben nach unten (in westlichen Kulturen) gelesen wurden.
-   Es gibt zwei Lese-und Überprüfungs Modi: immersives lesen und scannen. Das Ziel des immersiven Lesens ist das Verständnis.

    ![Abbildung von rotem Pfeil im Muster zum Lesen von Zickzack ](images/vis-layout-image1.png)

    Dieses Diagramm modelliert das immersive lesen.

    Im Gegensatz dazu ist das Ziel der Überprüfung das Auffinden von Dingen. Der gesamte Scanpfad sieht wie folgt aus:

    ![Abbildung von rotem Pfeil im diagonalen Lese Muster ](images/vis-layout-image2.png)

    Dieses Diagramm modelliert das Scannen.

    ![Abbildung von rotem Pfeil in einem Down-und Bogen Muster ](images/vis-layout-image3.png)

    Wenn am linken Rand einer Seite Text ausgeführt wird, Scannen Benutzer den linken Rand zuerst.

-   Bei der Verwendung von Software werden Benutzer nicht in die Benutzeroberfläche übernommen, sondern in ihrer Arbeit. Folglich lesen Benutzer in der Regel nicht den UI-Text, der Sie scannt. Dann lesen Sie Bits von Text nur dann umfassend, wenn Sie der Meinung sind, dass Sie Sie benötigen.
-   Benutzer neigen dazu, Navigationsbereiche auf der linken oder rechten Seite der Seite zu überspringen. Benutzer erkennen, dass Sie vorhanden sind, sehen sich jedoch nur die Navigationsbereiche an, wenn Sie navigieren möchten.
-   Benutzer neigen dazu, große Blöcke unformatierten Texts zu überspringen, ohne Sie zu lesen.

    ![Abbildung von Text mit Pfeilen, die den Scantext zeigen ](images/vis-layout-image4.png)

    Benutzer neigen dazu, beim Scannen große Text-und Navigationsbereiche zu überspringen.

-   Alle Dinge, die gleich sind, Benutzer sehen zuerst in der oberen linken Ecke eines Fensters nach, Scannen auf der Seite und beenden den Scan in der unteren rechten Ecke. In der Regel wird die linke untere Ecke ignoriert.

    ![Abbildung der Seite und von oben links nach unten rechts ](images/vis-layout-image5.png)

    Alle Dinge, die gleich sind, werden von Benutzern in der folgenden Reihenfolge gelesen: 1, 2, 4 und 3.

-   In der interaktiven Benutzeroberfläche sind jedoch nicht alle Dinge gleich, sodass verschiedene Benutzeroberflächen Elemente unterschiedliche Ebenen der Aufmerksamkeit erhalten. Benutzer neigen dazu, interaktive Steuerelemente zu betrachten, insbesondere die Steuerelemente in der oberen linken und mittleren Ecke des Fensters und den ersten Text.

![Abbildung des Bildschirms mit scharfer und unscharf Text ](images/vis-layout-image6.png)

Die Benutzer konzentrieren sich auf die interaktiven Hauptsteuer Elemente und die Haupt Anweisung und betrachten nur andere Dinge, wenn dies erforderlich ist.

-   Benutzer neigen dazu, interaktive Steuerelement Bezeichnungen zu lesen, insbesondere diejenigen, die für das Abschließen der Aufgabe relevant sind. Im Gegensatz dazu neigen Benutzer eher zum Lesen von statischem Text, wenn Sie der Ansicht sind.
-   Elemente, die unterschiedlich aussehen, werden beachtet. Fett formatierter Text und großer Text werden aus normalem Text hervorgehoben. Elemente der Benutzeroberfläche mit Farbe oder farbiger farbiger Hintergrund. Elemente mit Symbolen sind von Elementen ohne Symbole ausgehend.
-   Benutzer Scrollen nicht, es sei denn, Sie haben einen Grund für. Wenn der Inhalt [über dem Fold](glossary.md) keinen Grund für einen Bildlauf bietet, werden diese nicht angezeigt.
-   Nachdem die Benutzer entschieden haben, was zu tun ist, wird die Überprüfung sofort beendet.
-   Da Benutzer die Überprüfung beenden, wenn Sie Ihre Meinung haben, neigen Sie dazu, etwas außer dem Zeitpunkt zu ignorieren, der zum Zeitpunkt der Vervollständigung steht.

![Screenshot der Tastatur Optionen ](images/vis-layout-image7.png)

Benutzer beenden das Scannen, wenn Sie denken, dass Sie fertig sind.

Natürlich gibt es Ausnahmen für dieses allgemeine Modell. Augen Verfolgungs Geräte zeigen an, dass das Verhalten der realen Benutzerrecht unregelmäßig ist. Dieses Modell soll Sie dabei unterstützen, gute Entscheidungen und Kompromisse zu treffen und das Benutzer Verhalten nicht genau zu modellieren. Doch wenn Sie diese Liste gelesen haben, haben Sie hoffentlich viele ihrer eigenen Lesemuster erkannt.

### <a name="designing-for-scanning"></a>Entwerfen für Scannen

**Benutzer lesen nicht, Sie scannen, sodass Sie Benutzeroberflächen Oberflächen für die Überprüfung entwerfen sollten.** Gehen Sie nicht davon aus, dass Benutzer den Text von links nach rechts und von oben nach unten in der Reihenfolge lesen, sondern die Benutzeroberflächen Elemente betrachten, die Ihre Aufmerksamkeit berücksichtigen.

Zum Entwerfen für das Scannen:

-   Nehmen Sie an, dass der Benutzer zunächst das gesamte Fenster scannt und dann die Benutzeroberflächen Elemente in ungefähr der folgenden Reihenfolge liest:
    -   Interaktive Steuerelemente im Mittelpunkt
    -   Die Commit-Schaltflächen
    -   Interaktive Steuerelemente gefunden an anderer Stelle
    -   Main-Anweisung
    -   Ergänzende Erläuterungen
    -   Text mit einem Warnsymbol
    -   Fenstertitel
    -   Anderer statischer Text im Haupttext
    -   Fußnoten
-   Platzieren Sie Benutzeroberflächen Elemente, die eine Aufgabe in der oberen linken Ecke oder der oberen Mitte initiieren.
-   Platzieren Sie Benutzeroberflächen Elemente, die eine Aufgabe in der unteren rechten Ecke vervollständigen.
-   Wenn möglich, legen Sie anstelle von statischem Text entscheidenden Text für interaktive Steuerelemente an.
-   Vermeiden Sie das Platzieren wichtiger Informationen in der unteren linken Ecke oder am unteren Rand eines langen scrollbaren Steuer Elements oder einer anderen Seite.
-   Stellen Sie keine großen Textblöcke dar. Vermeiden Sie unnötigen Text. Verwenden Sie den [umgekehrten Pyramid](text-ui.md) -Präsentationsstil.
-   Wenn Sie etwas tun, um die Benutzer Aufmerksamkeit zu berücksichtigen, stellen Sie sicher, dass die Aufmerksamkeit gewährleistet ist.

Wenn möglich, arbeiten Sie mit diesem Modell, anstatt es zu bekämpfen. Es gibt jedoch Zeiten, in denen bestimmte Benutzeroberflächen Elemente hervorgehoben oder außer hervorgehoben werden müssen.

So betonen Sie primäre Benutzeroberflächen Elemente:

-   Fügen Sie primäre Benutzeroberflächen Elemente in den [Scanpfad](glossary.md)ein.
-   Fügen Sie eine beliebige Benutzeroberfläche ein, um eine Aufgabe in der oberen linken Ecke oder der oberen Mitte zu initiieren.
-   Legen Sie die Schaltflächen "Commit" in der unteren rechten Ecke ab.
-   Legen Sie die verbleibende primäre Benutzeroberfläche in den Mittelpunkt.
-   Verwenden Sie Steuerelemente, die Aufmerksamkeit erfordern, z. b. Befehls Schaltflächen, Befehls Verknüpfungen und Symbole.
-   Verwenden Sie den hervorragenden Text, einschließlich umfangreichen Texts und fetten Text.
-   Put Text-Benutzer müssen interaktive Steuerelemente, Symbole oder [Banner](vis-graphic.md)lesen.
-   Verwenden Sie den dunklen Text auf einem hellen Hintergrund.
-   Umschließen Sie die Elemente mit großzügigem Leerraum.
-   Sie benötigen keine Interaktionen, wie z. b. das zeigen oder zeigen, um das Element anzuzeigen, das Sie betonen.

    ![Screenshot der Windows-Aktivierungs Optionen ](images/vis-layout-image8.png)

    Dieses Beispiel zeigt viele Möglichkeiten, primäre Benutzeroberflächen Elemente hervorzuheben.

So heben Sie die Betonung der sekundären Benutzeroberflächen Elemente auf

-   Fügen Sie sekundäre Benutzeroberflächen Elemente außerhalb des Überprüfungs Pfads ein.
-   Legen Sie alle Benutzer in der Regel in der unteren linken Ecke oder im unteren Fensterbereich fest.
-   Verwenden Sie Steuerelemente, die keine Aufmerksamkeit erregen, wie z. b. Aufgaben Links anstelle von Befehls Schaltflächen
-   Normalen oder grauen Text verwenden.
-   Verwenden Sie hellen Text in einem dunklen Hintergrund. Weißer Text in einem dunkelgrauen oder blauen Hintergrund funktioniert gut.
-   Umschließen Sie die Elemente mit minimalem Leerraum.
-   Verwenden Sie die [Progressive Offenlegung](ctrl-progressive-disclosure-controls.md) , um sekundäre Benutzeroberflächen Elemente auszublenden.

    ![Screenshot von großen und kleinen Schnittstellen Elementen ](images/vis-layout-image9.png)

    Dieses Beispiel zeigt viele Möglichkeiten, sekundäre Benutzeroberflächen Elemente hervorzuheben.

### <a name="using-screen-space-effectively"></a>Effektive Verwendung des Bildschirm Raums

Wenn Sie den Bildschirmbereich effektiv verwenden, müssen Sie mehrere Faktoren ausgleichen: Verwenden Sie zu viel Speicherplatz, und ein Fenster hat hohe und Verschwendung und ist sogar schwer zu verwenden, basierend auf dem [Recht von FTTS](inter-mouse.md).

**Falsch:**

![Screenshot, der zu viel Leerraum anzeigt ](images/vis-layout-image10.png)

In diesem Beispiel ist das Fenster zu groß für seinen Inhalt.

Verwenden Sie auf der anderen Seite zu wenig Platz, und ein Fenster ist umständlich, unbequem und einschüchternd und schwer zu verwenden, wenn es einen Bildlauf und eine andere Bearbeitung erfordert.

**Falsch:**

![Screenshot mit zu vielen Steuerelementen ](images/vis-layout-image11.png)

In diesem Beispiel ist das Fenster für seinen Inhalt zu klein.

Obwohl die kritische Benutzeroberfläche in die minimal unterstützte [effektive Auflösung](glossary.md)passen muss, gehen Sie nicht davon aus, dass die Verwendung des Bildschirm Raums effektiv bedeutet, dass Windows so klein wie möglich sein sollte. **Das effektive Layout wirkt sich auf den freien Speicherplatz aus und versucht nicht, alles in den kleinsten möglichen Bereich zu wiegen.** Moderne anzeigen weisen einen erheblichen Bildschirmbereich auf, und es ist sinnvoll, diesen Bereich effektiv zu verwenden, wenn dies möglich ist. Folglich ist es nicht zu klein, dass Sie sich auf der Seite mit zu viel Bildschirmfläche befinden. Dadurch wird Ihr Fenster leichter und besser zugänglich.

Sie wissen, dass ein Layout den Bildschirmbereich effektiv verwendet, wenn Folgendes gilt:

-   Fenster, Fensterbereiche und Steuerelemente müssen nicht in der Größe geändert werden, um verwendet werden zu können. Wenn ein Benutzer die Größe eines Fensters, eines Bereichs oder eines Steuer Elements ändert, ist seine Größe falsch.
-   Die Daten werden nicht abgeschnitten. Die meisten Daten in Listenansichten und Struktur Ansichten verfügen über keine Ellipsen, und Daten in anderen Steuerelementen werden nur abgeschnitten, wenn die Daten Länge ungewöhnlich groß ist. Daten, die gelesen werden müssen, um eine Aufgabe auszuführen, sollten nicht abgeschnitten werden.
-   Die Größen der Fenster und Steuerelemente werden entsprechend angepasst, um unnötigen Bildlauf auszuschließen. Es gibt nur wenige horizontale Scrollleisten und keine unnötigen vertikalen Scrollleisten.
-   Steuerelemente verwenden hauptsächlich ihre Standardgrößen. Verringern Sie die Anzahl der Steuerelement Größen, indem Sie z. b. nur eine oder zwei Befehls Schaltflächen breiten auf einer Oberfläche verwenden.
-   Die UI-Oberfläche ist ausgeglichen. Es sind keine großen, nicht verwendeten Bildschirmbereiche vorhanden.

Wählen Sie die Fenstergrößen aus, die nur groß genug sind, um ihren Zweck zu erfüllen. (Und wenn das Fenster in der Größe geändert werden kann, ist dieses Ziel auf seine Standardgröße anwendbar.) **Eine Kombination aus abgeschnittene Daten oder Scrollleisten und reichlich verfügbarem Bildschirmraum ist ein unklares Zeichen für ein ineffizientes Layout.**

### <a name="control-sizing"></a>Steuern der Größe

Normalerweise besteht der erste Schritt bei der effektiven Verwendung des Bildschirm Raums darin, die richtige Größe für die verschiedenen Benutzeroberflächen Elemente festzulegen. Weitere Informationen finden Sie in der Tabelle mit den [Steuerelement Größen](#recommended-sizing-and-spacing) und der empfohlenen Größe in den Artikeln zu den jeweiligen Steuerungs Richtlinien.

Das Recht besagt, dass der kleinere Zielwert ist, desto länger dauert es, bis es mit der Maus abgerufen wird. Für Computer, die die Tablet-und Touch-Technologie von Windows verwenden, kann es sein, dass die "Maus" tatsächlich ein Stift oder der Finger des Benutzers ist. Sie sollten also Alternative Eingabegeräte in Erwägung gezogen werden, wenn Sie Größen für kleine Steuerelemente **Eine Steuerelement Größe von 16x16 relative Pixel ist eine gute Mindestgröße für alle Eingabegeräte.** Im Gegensatz dazu sind die standardmäßigen 15x9-Pixel Dreh Steuer Schaltflächen zu klein, damit Sie von den Stiften effektiv verwendet werden können.

### <a name="spacing"></a>Abstand

Das Bereitstellen von großzügigem (aber nicht übermäßigem) Raum macht das Layout komplizierter und leichter zu analysieren. Der Speicherplatz ist nicht nicht verwendeter Speicherplatz. er spielt eine wichtige Rolle bei der Verbesserung der Benutzer Fähigkeit, Sie zu überprüfen, und fügt auch eine visuelle Anziehungs Weise des Entwurfs ein. Richtlinien finden Sie in der [Tabelle "Abstand](#recommended-sizing-and-spacing)".

Bei Computern, auf denen die Tablet-und Touch-Technologie von Windows verwendet wird, ist die "Maus" möglicherweise ein Stift oder der Finger des Benutzers. Die Ausrichtung ist schwieriger, wenn Sie einen Stift oder Finger als Zeigegerät verwenden, was dazu führt, dass Benutzer außerhalb des vorgesehenen Ziels tippen. Wenn interaktive Steuerelemente sehr nah beieinander platziert werden, aber nicht tatsächlich berühren, klicken Benutzer möglicherweise auf inaktiven Bereich zwischen den Steuerelementen. Da das Klicken auf inaktiven Speicherplatz weder Ergebnis noch visuelles Feedback hat, sind die Benutzer häufig unsicher, was schief gelaufen ist. Wenn kleine Steuerelemente zu stark voneinander entfernt sind, muss der Benutzer mit der Genauigkeit tippen, um zu vermeiden, dass auf das falsche Objekt angetippt wird. **Um diese Probleme zu beheben, sollten die Zielregionen interaktiver Steuerelemente entweder berühren oder mindestens 3 DLUs (5 relative Pixel) enthalten.**

Sie wissen, dass ein Layout in folgenden Abständen einen guten Abstand hat:

-   Insgesamt ist die Oberfläche für die Benutzeroberfläche zufrieden und ist nicht verengen.
-   Der Leerraum wird einheitlich und ausgeglichen angezeigt.
-   Verwandte Elemente sind nah beieinander, und nicht verknüpfte Elemente sind relativ weit voneinander entfernt.
-   Es gibt keinen freien Speicherplatz zwischen Steuerelementen, die verbunden werden sollen, z. b. Schaltflächen auf der Symbolleiste.

### <a name="resizable-windows"></a>Fenster mit Größenänderung

Fenster mit Größenänderung sind auch ein Faktor für die effektive Verwendung des Bildschirm Raums. Einige Fenster bestehen aus festem Inhalt und können nicht in der Größe geändert werden, aber Windows mit Inhalt, dessen Größe geändert werden kann, sollte in der Größe geändert werden können. Der Grund, warum Benutzer die Größe eines Fensters ändern, besteht natürlich darin, den zusätzlichen Bildschirmbereich erweitert zu lassen. der Inhalt sollte daher entsprechend erweitert werden, indem die Benutzeroberflächen Elemente, die Sie benötigen, mehr Platz zur Folge hat. Fenster mit dynamischem Inhalt, Dokumenten, Bildern, Listen und Strukturen profitieren am meisten von Fenstern mit Größenänderung.

![Screenshot des Steuer Elements zum Ändern der Größe der Bild Lauf Leiste ](images/vis-layout-image12.png)

In diesem Beispiel ändert die Größe des Fensters das Listenansicht-Steuerelement.

Das heißt, Windows kann zu breit gestreckten werden. Beispielsweise werden viele System Steuerungs Seiten unhandlich, wenn der Inhalt breiter als 600 relative Pixel ist. In diesem Fall ist es besser, die Größe des Inhalts Bereichs über diese maximale Breite hinaus zu ändern oder den Ursprung des Inhalts zu ändern, wenn die Größe des Fensters vergrößert wird. Behalten Sie stattdessen eine maximale Breite und einen fixierten oberen linken Ursprung bei.

Der Text wird beim Erhöhen der Zeilenlänge schwer lesbar. Bei Textdokumenten wird eine maximale Zeilenlänge von 80 Zeichen berücksichtigt, damit der Text leichter lesbar ist. (Zeichen umfassen Buchstaben, Interpunktions Zeichen und Leerzeichen.)

**Falsch:**

![Screenshot des breiten Meldungs Felds mit langem Text ](images/vis-layout-image13.png)

In diesem Beispiel ist die Länge des langen Texts schwierig zu lesen.

Und schließlich müssen in der Größe zu erstellbaren Fenstern auch Bildschirmbereiche effektiv verwendet werden, wenn Sie kleiner werden, indem die Größe des Inhalts angepasst wird und Speicherplatz von Benutzeroberflächen Elementen entfernt wird, die ohne diese Funktion effektiv funktionieren. Zu einem bestimmten Zeitpunkt werden das Fenster oder seine Benutzeroberflächen Elemente zu klein, damit es verwendet werden kann. Daher sollten Sie eine minimale Größe aufweisen, oder einige Elemente sollten vollständig entfernt werden.

![Screenshot des Fensters mit hohem, eindringlichem Menüband ](images/vis-layout-image14.png)

![Screenshot des Fensters ohne Menüband ](images/vis-layout-image15.png)

In diesem Beispiel hat der Bereich eine Mindestgröße.

Einige Programme profitieren von der Verwendung einer vollkommen anderen Präsentation, damit der Inhalt in geringerer Größe verwendet werden kann.

![Screenshot der Schaltflächen für zentrierte Medien Player ](images/vis-layout-image16.png)

In diesem Beispiel ändert Windows Media Player sein Format, wenn das Fenster für das Standardformat zu klein wird.

### <a name="focus"></a>Fokus

Ein Layout ist fokussiert, wenn es eine offensichtliche Stelle gibt, an der Sie zuerst suchen können. Der Fokus ist wichtig, um Benutzern zu zeigen, wo Sie mit dem Scannen Ihres Fensters oder Ihrer Seite beginnen. Ohne den Fokus zu haben, wird das Auge des Benutzers ohne weiteres umherbewegen. Der Schwerpunkt sollte ein wichtiger Punkt sein, den Benutzer schnell finden und verstehen müssen, und Sie sollten den größten visuellen Fokus haben. Die linke obere Ecke ist für die meisten Fenster der natürliche Fokuspunkt.

Es sollte nur ein Mittelpunkt vorhanden sein. Genau wie in der Praxis kann sich das Auge nur auf eine Sache konzentrieren, Benutzer können sich nicht gleichzeitig auf mehrere Orte konzentrieren.

Wenn Sie ein Benutzeroberflächen Element als Mittelpunkt festlegen möchten, können Sie ihm visuelle Akzente geben:

-   Platzieren des Werts in der oberen linken oder oberen Mitte der Oberfläche.
-   Verwendung interaktiver Steuerelemente, die wichtig und leicht verständlich sind.
-   Verwenden von prominentem Text, z. b. einer Haupt Anweisung.
-   Erteilen der Standardauswahl und des ersten Eingabefokus für die Steuerelemente.
-   Platzieren der Steuerelemente in einem anderen farbigen Hintergrund.

Beachten Sie Windows Search. Der Fokuspunkt für Windows Search sollte das Suchfeld sein, da es sich hierbei um den Ausgangspunkt der Aufgabe handelt. Sie befindet sich jedoch in der oberen rechten Ecke, um mit der standardmäßigen Suchfeld Platzierung konsistent zu sein. Das Suchfeld hat den Eingabefokus, aber angesichts seiner Position im Überprüfungs Pfad ist dieser Hinweis allein nicht ausreichend.

Um dieses Problem zu beheben, besteht eine deutliche Anweisung im oberen Bereich des Fensters, um Benutzer an den richtigen Speicherort weiterzuleiten.

**Annehmbar:**

![Screenshot des Such Dialogfelds mit hilfreichen Text ](images/vis-layout-image17.png)

In diesem Beispiel werden Benutzer durch eine prominente Anweisung im oberen mittleren Bereich des Fensters zum Suchfeld geleitet.

Ohne die Anweisungen hat das Fenster keinen offensichtlichen Schwerpunkt.

**Falsch:**

![Screenshot des Such Dialogfelds ohne Text ](images/vis-layout-image18.png)

Dieses Beispiel weist keinen offensichtlichen Fokuspunkt auf. Benutzer wissen nicht, wo Sie suchen müssen.

Wenn Sie einem Benutzeroberflächen Element einen visuellen Fokus geben, stellen Sie sicher, dass die Aufmerksamkeit gewährleistet ist. Im vorherigen Beispiel für eine falsche Windows-Suche befindet sich die markierte Schaltfläche Alle in der oberen linken Ecke und hat die meisten visuellen Akzente, aber Sie ist nicht der beabsichtigte Fokuspunkt. Die Benutzer können sich diese Schaltfläche ansehen, um herauszufinden, was damit zu tun ist.

**Falsch:**

![Screenshot der hervorgehobenen Schaltfläche "alle" ](images/vis-layout-image19.png)

Ohne die markante Anweisung als Mittelpunkt ist die markierte Schaltfläche alle ein unbeabsichtigter Fokuspunkt.

### <a name="flow"></a>Flow

Ein Layout weist einen Flow auf, wenn Benutzer reibungslos und natürlich über einen klaren Weg durch ihre Oberfläche geführt werden, wobei die Benutzeroberflächen Elemente in der für ihre Verwendung geeigneten Reihenfolge gefunden werden. Nachdem die Benutzer den Schwerpunkt identifiziert haben, müssen Sie bestimmen, wie die Aufgabe ausgeführt werden soll. Die Platzierung der UI-Elemente übermittelt Ihre Beziehung und sollte die Schritte zum Ausführen der Aufgabe widerspiegeln. In der Regel bedeutet dies, dass die Schritte der Aufgabe natürlich von links nach rechts, von oben nach unten (in westlichen Kulturen) durchlaufen werden sollten.

Sie wissen, dass ein Layout einen guten Ablauf hat, wenn:

-   Die Platzierung der UI-Elemente spiegelt die Schritte wider, die Benutzer zum Ausführen der Aufgabe benötigen.
-   Elemente der Benutzeroberfläche, die eine Aufgabe initiieren, befinden sich in der oberen linken Ecke oder der oberen Mitte.
-   Elemente der Benutzeroberfläche, die eine Aufgabe vervollständigen, befinden sich in der unteren rechten Ecke.
-   Verwandte Benutzeroberflächen Elemente sind zusammen. nicht verknüpfte Elemente sind separat.
-   Die erforderlichen Schritte sind im Hauptflow.
-   Optionale Schritte sind außerhalb des Hauptflusses und können möglicherweise durch einen passenden Hintergrund oder eine progressive Offenlegung hervorgehoben werden.
-   Häufig verwendete Elemente werden vor selten verwendeten Elementen im Scanpfad angezeigt.
-   Benutzer wissen immer, was als nächstes zu tun ist. Es gibt keine unerwarteten Sprünge oder Unterbrechungen im Aufgaben Fluss.

**Falsch:**

![Screenshot des unübersichtlichen Dialogfeld Layouts ](images/vis-layout-image20.png)

In diesem Beispiel wissen die Benutzer nicht, was als nächstes zu tun ist. Es gibt unerwartete Sprünge und Unterbrechungen im Aufgaben Fluss.

**Richtig:**

![Screenshot eines gut geplanten Dialog Felds ](images/vis-layout-image21.png)

In diesem Beispiel spiegelt die Darstellung der UI-Elemente die Schritte zum Ausführen der Aufgabe wider.

### <a name="grouping"></a>Gruppierung

Ein Layout hat eine Gruppierung, wenn logisch verwandte UI-Elemente eine klare visuelle Beziehung aufweisen. Gruppen sind wichtig, da es für Benutzer einfacher ist, eine Gruppe verwandter Elemente zu verstehen und sich darauf zu konzentrieren, als die Elemente einzeln. Gruppen machen ein Layout einfacher und leichter zu analysieren.

Es gibt folgende Möglichkeiten, um die Gruppierung anzuzeigen (bei zunehmender schwere haftigkeit):

-   **Struktur.** Sie können verwandte Steuerelemente nebeneinander gruppieren und zusätzlichen Abstand zwischen nicht verknüpften Steuerelementen einfügen.

    ![Abbildung von vier Symbolen mit vier Aufgaben Gruppen ](images/vis-layout-image22.png)

    In diesem Beispiel wird das Layout allein zum Anzeigen von Steuerelement Beziehungen verwendet.

-   **Trennzeichen.** Ein Trennzeichen ist eine horizontale oder vertikale Linie, die eine Gruppe von Steuerelementen vereinheitlicht. Trennzeichen bieten ein einfacheres, saubereres aussehen. Im Gegensatz zu Gruppen Feldern funktionieren Sie jedoch am besten, wenn Sie sich auf die gesamte Oberfläche erstrecken.

    ![Screenshot von drei Symbolen und drei Trennzeichen ](images/vis-layout-image23.png)

    In diesem Beispiel werden beschriftete Trennzeichen verwendet, um Steuerelement Beziehungen anzuzeigen.

-   **Aggregatoren.** Ein Aggregator ist eine Grafik, die eine visuelle Beziehung zwischen stark verknüpften Steuerelementen erstellt.

    ![Screenshot der Steuerelemente in einer elliptischen Linie ](images/vis-layout-image24.png)

    In diesem Beispiel wird ein Begrenzungs Aggregator verwendet, um die Beziehung zwischen den Steuerelementen hervorzuheben und Sie wie ein einzelnes Steuerelement anstelle von acht zu gestalten.

-   **Gruppen Felder.** Ein Gruppenfeld ist ein rechteckiger Frame, der einen Satz verwandter Steuerelemente umgibt.

    ![Screenshot der Kontrollkästchen in einem rechteckigen Rahmen ](images/vis-layout-image25.png)

    In diesem Beispiel umgibt ein Gruppenfeld eine Reihe verwandter Steuerelemente und bezeichnet diese.

-   **Hintergründe.** Sie können Hintergründe verwenden, um unterschiedliche Arten von Inhalten hervorzuheben oder hervorzuheben.

    ![Screenshot der linken Seite der Systemsteuerung ](images/vis-layout-image26.png)

    In diesem Beispiel wird der Aufgabenbereich der Systemsteuerung verwendet, um verwandte Aufgaben und System Steuerungselemente zu gruppieren.

    Um die visuelle Gruppierung zu vermeiden, ist die leichtesten Gewichtungs Gruppierung, die den Auftrag erfüllt, die beste Wahl. Weitere Informationen finden Sie unter [Gruppen Felder](ctrl-group-boxes.md), [Registerkarten](ctrl-tabs.md), [Trennzeichen und Hintergründe](vis-graphic.md).

Unabhängig vom Gruppierungs Stil können Sie mit Einzügen die Beziehung der Steuerelemente in einer Gruppe anzeigen. Steuerelemente, die Peers zueinander sind, sollten linksbündig ausgerichtet werden, und abhängige Steuerelemente werden 12 DLUs oder 18 relative Pixel eingerückt.

![Screenshot von drei Ebenen von eingerückt-Steuerelementen ](images/vis-layout-image27.png)

Abhängige Steuerelemente werden 12 DLUs oder 18 relative Pixel eingerückt. Dies ist Entwurfs bedingt der Abstand zwischen Kontrollkästchen und Options Feldern von ihren Bezeichnungen.

Sie wissen, dass ein Layout eine gute Gruppierung hat, wenn:

-   Das Fenster oder die Seiten haben höchstens 7 Gruppen.
-   Der Zweck der einzelnen Gruppen ist offensichtlich.
-   Die Beziehung zwischen Steuerelementen in jeder Gruppe ist offensichtlich, insbesondere die Abhängigkeit von Steuerelementen.
-   Die Gruppierung vereinfacht den Inhalt, anstatt ihn komplexer zu gestalten.

### <a name="alignment"></a>Ausrichtung

Die Ausrichtung ist die koordinierte Platzierung von UI-Elementen. Die Ausrichtung ist wichtig, da Sie die Überprüfung von Inhalten erleichtert und die Wahrnehmung der visuellen Komplexität durch die Benutzer beeinträchtigt wird.

Beim Bestimmen der Ausrichtung müssen mehrere Ziele berücksichtigt werden:

-   **Einfache horizontale Überprüfung.** Benutzer können ohne umständliche Lücken horizontal lesen und verwandte Elemente nebeneinander suchen.
-   **Einfache vertikale Überprüfung.** Benutzer können mit minimaler horizontaler Augenbewegung die Spalten verwandter Elemente Scannen und sofort ermitteln, was Sie suchen.
-   **Minimale visuelle Komplexität.** Benutzer betrachten ein Layout, das visuell Komplex ist, wenn es unnötige vertikale Ausrichtungs Rasterlinien aufweist.

### <a name="horizontal-alignment"></a>Horizontale Ausrichtung

**Linke Ausrichtung**

Aufgrund der Lesereihenfolge von links nach rechts funktioniert die linke Ausrichtung für die meisten Inhalte gut. Die linke Ausrichtung macht das vertikale Scannen von Spaltendaten leicht.

**Rechte Ausrichtung**

Die richtige Ausrichtung ist die beste Wahl für numerische Daten, insbesondere [Spalten numerischer Daten](ctrl-text-boxes.md). Die Rechte Ausrichtung funktioniert auch gut für [Commit-Schalt](glossary.md) Flächen und Steuerelemente, die mit dem rechten Fensterrand ausgerichtet sind.

![Screenshot der Schaltfläche "Erweiterte Suche mit Pfeil nach unten" ](images/vis-layout-image28.png)

In diesem Beispiel ist das erweiterte Steuerelement für die Suche progressives Offenlegung rechtsbündig, da es am rechten Fensterrand platziert wird.

**Ausrichtung zentrieren**

Die Ausrichtung des Mittelpunkts eignet sich am besten für Situationen, in denen die linke oder die Rechte Ausrichtung ungeeignet ist oder unausgeglichen erscheint.

![Screenshot der zentrierten Media Player-Steuerelemente ](images/vis-layout-image29.png)

In diesem Beispiel wird das Media Player-Steuerelement zentriert, um eine ausgeglichene Darstellung zu erzielen.

Zentrieren Sie Fenster Inhalte nicht, um Platz zu füllen.

**Falsch:**

![Screenshot eines Fensters mit zu viel Leerraum ](images/vis-layout-image30.png)

In diesem Beispiel ist der Inhalt in einem Fenster, das in der Größe geändert werden kann, nicht ordnungsgemäß zentriert.

### <a name="vertical-alignment"></a>Vertikale Ausrichtung

**Element Spitzen**

Aufgrund der Top-to-Bottom-Lesefolge funktioniert die obere Ausrichtung für die meisten Inhalte gut. Die obere Ausrichtung macht das horizontale Scannen von Benutzeroberflächen Elementen leicht.

**Textbaselines**

Wenn Sie Steuerelemente mit Text vertikal ausrichten, richten Sie die textbaselines so aus, dass Sie einen horizontalen horizontalen Lesefluss erhalten.

**Richtig:**

![Screenshot von Schaltflächen-und Beschriftungs Text ausgerichtet ](images/vis-layout-image31.png)

**Falsch:**

![Screenshot von Schaltflächen-und Beschriftungs Text nicht ausgerichtet ](images/vis-layout-image32.png)

Im richtigen Beispiel werden das Steuerelement und seine Bezeichnung vertikal durch ihre textbaselines ausgerichtet.

Sie wissen, dass ein Layout gute Ausrichtung hat, wenn Folgendes gilt:

-   Es ist einfach, sowohl horizontal als auch vertikal zu scannen.
-   Es verfügt über eine einfache visuelle Darstellung.

### <a name="label-alignment"></a>Beschriftungs Ausrichtung

Die allgemeinen Ausrichtungs Regeln gelten für Steuerelement Bezeichnungen, aber es handelt sich um ein gängiges Problem, das eine besondere Aufmerksamkeit verdient. Die Beschriftungs Ausrichtung hat folgende Ziele:

-   Vereinfachen Sie die vertikale Überprüfung, um das richtige Steuerelement zu finden.
-   Vereinfachen Sie das horizontale Scannen, um Bezeichnungen Ihren Steuerelementen zuzuordnen.
-   Einfache Lokalisierung und Behandlung von Bezeichnungen, die sich in verschiedenen Sprachen unterscheiden.
-   Funktioniert gut mit einer Mischung verschiedener Bezeichnungs Längen.
-   Ermöglicht die effiziente Verwendung von verfügbarem Speicherplatz, während der abgeschnittene Text vermieden wird.

Das Gesamtziel besteht darin, die Anzahl der Augenbewegungen zu verringern, die erforderlich sind, um zu ermitteln, welche Benutzer wahrscheinlich suchen, aber welche Art von Steuerelementen und welche Benutzer Sie suchen, hängt vom Kontext ab.

Es gibt vier allgemeine Bezeichnungs-und Ausrichtungs Stile, die jeweils die Vorteile haben:

-   Linksbündig ausgerichtete Bezeichnungen oberhalb von Steuerelementen
-   Linksbündig ausgerichtete Bezeichnungen auf der linken Seite von Steuerelementen
-   Linksbündig ausgerichtete Bezeichnungen auf der linken Seite von Steuerelementen, linksbündig bündig
-   Rechtsbündig ausgerichtete Bezeichnungen auf der linken Seite von Steuerelementen

**Linksbündig ausgerichtete Bezeichnungen oberhalb von Steuerelementen**

Dieser Stil ist am einfachsten zu lokalisieren, da das Layout nicht von der Länge der Bezeichnungen abhängt, sondern den meisten vertikalen Bereich einnimmt.

![Liste mit zwei Spalten von Bezeichnungen oberhalb von Steuerelementen ](images/vis-layout-image33.png)

Dieser Stil benötigt den meisten vertikalen Bereich, ist aber am einfachsten zu lokalisieren. Es ist eine bessere Wahl, um die meisten interaktiven Steuerelemente zu bezeichnen.

Beste Verwendung, wenn:

-   Die beschrifteten Steuerelemente sind interaktiv (nicht nur Text).
-   Die Benutzeroberfläche wird lokalisiert. Dieser Stil bietet häufig Raum für die doppelte oder sogar dreifache Länge der Bezeichnung.
-   Die Benutzeroberfläche verwendet eine Technologie mit festem Layout (z. b. Win32).
-   Es sind höchstens zehn Steuerelemente vorhanden. Bei weiteren Steuerelementen sind die Bezeichnungen schwer zu scannen.
-   Es ist ausreichend vertikaler Raum vorhanden, um die Bezeichnungen aufnehmen zu können.
-   Das Layout muss ein freies Formular und nicht nur Spalten sein.

**Linksbündig ausgerichtete Bezeichnungen auf der linken Seite von Steuerelementen**

Dieser Stil ist am einfachsten zu scannen und funktioniert auch gut, wenn sich Bezeichnungen stark voneinander unterscheiden, aber es ist schwieriger, die Bezeichnung dem Steuerelement zuzuordnen. Dieser Stil kann bei Bedarf mehrzeilige Bezeichnungen verwenden.

![Liste mit vier Spalten von Bezeichnungen Links von Steuerelementen ](images/vis-layout-image34.png)

Dieser Stil funktioniert gut. Es gibt jedoch zwei Spalten, aber es scheint, als würden vier Spalten vorhanden sein, sodass die Daten komplexer werden.

Beste Verwendung, wenn:

-   Benutzer werden wahrscheinlich vertikal Scannen, um nach bestimmten Bezeichnungen zu suchen.
-   Benutzer sind nicht in der Regel in der Regel von links nach rechts und von oben nach unten.
-   Es ist ausreichend horizontaler Raum vorhanden, um die Bezeichnungen aufnehmen zu können.
-   Die Bezeichnungen variieren erheblich.
-   Es gibt zahlreiche Steuerelemente, z. b. mit Formularen.
-   Es sind nur wenige Spalten vorhanden. Die Bezeichnungen und Steuerelemente werden visuell als zwei einzelne Spalten angezeigt.

**Linksbündig ausgerichtete Bezeichnungen auf der linken Seite von Steuerelementen, linksbündig bündig**

Dieser Stil vereinfacht die vertikale Überprüfung der Bezeichnungen und die Bezeichnungen und Steuerelemente, und ist sehr platzsparend. Es ist jedoch schwieriger, die Steuerelemente vertikal zu scannen. Die Steuerelemente sind rechtsbündig, um den verfügbaren Speicherplatz optimal zu nutzen.

![Liste mit zwei Spalten von Bezeichnungen mit unregelmäßigen Steuerelementen ](images/vis-layout-image35.png)

Dieser Stil ist kompakt und leicht lesbar, aber es ist schwierig, Steuerelemente vertikal zu scannen.

Beste Verwendung, wenn:

-   Die Benutzeroberfläche verwendet eine Variable layouttechnologie (z. b. Windows Presentation Foundation).
-   Benutzer werden wahrscheinlich vertikal Scannen, um nach bestimmten Bezeichnungen zu suchen.
-   Benutzer werden die Bezeichnungen und Steuerelemente wahrscheinlich von links nach rechts und von oben nach unten lesen.
-   Benutzer werden die Steuerelemente wahrscheinlich nicht vertikal scannen.
-   Der Steuerelement Text variiert in der Länge und wird wahrscheinlich abgeschnitten, wenn ein anderer Stil verwendet wurde.
-   Die Steuerelemente sind schreibgeschützt, z. b. schreibgeschützte Textfelder. Bei anderen Steuerelementen sieht diese Ausrichtung Sloppy aus. Die Steuerelemente können jedoch beim Klicken bearbeitet werden.
-   Es gibt viele Spalten, aber nur wenige Steuerelemente in einer Spalte.

**Rechtsbündig ausgerichtete Bezeichnungen auf der linken Seite von Steuerelementen**

Dieser Stil ist am einfachsten zu lesen, um die Bezeichnungen Ihren Steuerelementen zuzuordnen, aber es ist schwierig, die Bezeichnungen vertikal zu scannen, und funktioniert nicht gut, wenn labelslist mit eingezogenen Bezeichnungen und Steuerelementen stark voneinander abweicht.

![Liste mit eingerückt-Bezeichnungen und-Steuerelementen ](images/vis-layout-image36.png)

Dieser Stil ermöglicht eine einfache vertikale Überprüfung der Steuerelemente, macht es jedoch schwierig, die Bezeichnungen vertikal zu scannen.

Beste Verwendung, wenn:

-   Benutzer werden die Bezeichnungen und Steuerelemente wahrscheinlich von links nach rechts und von oben nach unten lesen.
-   Benutzer werden wahrscheinlich nicht vertikal durchsucht, um bestimmte Bezeichnungen zu finden, möglicherweise aus folgenden Gründen:
    -   Es gibt einige-Steuerelemente.
    -   Die Bezeichnungen sind bekannt.
    -   Die Steuerelemente sind größtenteils selbsterklärend und selten leer (möglicherweise verfügen Sie über Standardwerte, um leere Steuerelemente zu verhindern).
-   Es ist ausreichend horizontaler Raum vorhanden, um die Bezeichnungen aufnehmen zu können.
-   Die Bezeichnungen variieren nicht erheblich.
-   Viele Spalten vorhanden sind. Visuell werden die Bezeichnungen und Steuerelemente als einzelne Spalte angezeigt.

Vor der Übernahme eines dieser Stile sollten Sie jedoch zwei weitere Faktoren berücksichtigen:

-   Bevorzugen Sie einen Stil, den Sie im gesamten Programm konsistent verwenden können.
-   Linksbündig ausgerichtete Bezeichnungen entweder oberhalb der Steuerelemente auf der linken Seite von Steuerelementen sind die gängigsten Stile und sollten daher bevorzugt werden.

### <a name="balance"></a>Balance

Ein Fenster oder eine Seite hat einen Saldo, wenn der Inhalt gleichmäßig auf seine Oberfläche verteilt wird. Wenn die Oberfläche physisch die gleiche Gewichtung hat wie die visuelle Darstellung, würde ein ausgeglichenes Layout nicht an eine Seite tippen.

Das häufigste Problem ist, dass auf der linken Seite eines Fensters oder einer Seite zu viel Inhalt vorhanden ist. Sie können den Saldo auf folgende Weise erstellen:

-   Die Verwendung größerer Ränder auf der linken Seite als der Rechte Bereich.
-   Platzieren von UI-Elementen, die zum Ausführen einer Aufgabe auf der rechten Seite verwendet werden.
-   Platzieren von UI-Elementen, die in der Aufgabe in der Mitte verwendet werden.
-   Verlängern der Größenänderung oder mehrzeilige Steuerelemente.
-   Strategische Verwendung von Center-Ausrichtung.

![Bildschirm Abbildung von Drucker Links und Text auf der rechten Seite ](images/vis-layout-image37.png)

Dieses wohl ausgeglichene Layout der Assistenten Seite zeigt einen größeren linken Rand als rechts, um den Saldo zu verbessern.

Wenn diese Verfahren keinen Saldo erzielen, sollten Sie die Breite des Fensters oder der Seite verringern, um den Inhalt besser abzugleichen.

Um die Größe zu ändern, können Sie Inhalte nicht zentrieren, um den Ausgleich zu erreichen. Behalten Sie stattdessen einen festgelegten oberen linken Ursprung bei, definieren Sie eine maximale Oberfläche, und balancieren Sie den Inhalt im verwendeten Speicherplatz.

### <a name="grids"></a>Raster

Ein Raster ist ein unsichtbares zugrunde liegendes Ausrichtungssystem. Raster können symmetrisch sein, aber asymmetrische Raster funktionieren ebenfalls. Wenn Sie von einem einzelnen Fenster oder einer Seite verwendet werden, können Sie Inhalte in einer Oberfläche organisieren. Wenn das Raster wieder verwendet wird, erstellen Sie ein konsistentes Layout.

Die Anzahl der Rasterlinien wirkt sich auf die Wahrnehmung der visuellen Komplexität aus. Ein Layout mit weniger Rasterlinien erscheint einfacher als ein Layout mit mehr Rasterlinien.

**Visuell Komplex:**

![Screenshot des Dialog Felds "überlastet" ](images/vis-layout-image38.png)

**Visuell einfach:**

![Screenshot des organisierten Dialog Felds ](images/vis-layout-image39.png)

Unnötige Rasterlinien erstellen visuelle Komplexität.

Sie wissen, dass ein Layout in folgenden Programmen effektiv Raster verwendet:

-   Fenster oder Seiten mit ähnlichen Inhalten oder Funktionen weisen ein ähnliches Layout auf.
-   Wiederholte Entwurfs Elemente werden an ähnlichen Positionen in Windows und Seiten angezeigt.
-   Es sind keine unnötigen vertikalen und horizontalen Ausrichtungs Rasterlinien vorhanden.

### <a name="visual-simplicity"></a>Visuelle Einfachheit

Die visuelle Einfachheit ist der Eindruck, dass ein Layout nicht komplizierter ist, als es sein muss.

Sie wissen, dass ein Layout visuelle Einfachheit aufweist, wenn es Folgendes bietet:

-   Entfernt unnötige Ebenen von Window Chrome.
-   Zeigt den Inhalt mit höchstens sieben leicht identifizierbaren Gruppen an.
-   Verwendet Lightweight-Gruppierungen, z. b. Layout und Trennzeichen anstelle von Gruppen Feldern.
-   Verwendet Lightweight-Steuerelemente, z. b. Links anstelle von Befehls Schaltflächen für sekundäre Befehle, und Dropdown Listen anstelle von Listen für Auswahlmöglichkeiten.
-   Reduziert die Anzahl der vertikalen und horizontalen Ausrichtungs Rasterlinien.
-   Verringert die Anzahl der Steuerelement Größen, indem z. b. nur eine oder zwei Befehls Schaltflächen breiten auf einer Oberfläche verwendet werden.
-   Verwendet Progressive Offenlegung, um Benutzeroberflächen Elemente auszublenden, bis Sie benötigt werden.
-   Verwendet ausreichenden Platz, damit das Fenster oder die Seite nicht verkrampft ist.
-   Passt die Größe von Fenstern und Steuerelementen entsprechend an, um unnötigen Bildlauf
-   Verwendet eine einzelne Schriftart mit einer kleinen Anzahl von Größen und Textfarben.

Als allgemeine Regel gilt: Wenn ein Layoutelement gelöscht werden kann, ohne die Effektivität der Benutzeroberfläche zu beeinträchtigen, sollte es wahrscheinlich sein.

## <a name="guidelines"></a>Richtlinien

### <a name="screen-resolution-and-dpi"></a>Bildschirmauflösung und dpi

-   **Unterstützen Sie die minimale effektive Windows-Auflösung von 800 x 600 Pixel.** Für wichtige Benutzeroberflächen, die im abgesicherten Modus funktionieren müssen, unterstützen Sie eine effektive Auflösung von 640 x 480 Pixeln. Achten Sie darauf, den von der Taskleiste verwendeten Speicherplatz zu berücksichtigen, indem Sie 48 vertikale [relative Pixel](glossary.md) für Windows reservieren, der mit der Taskleiste angezeigt wird.
-   **Optimieren Sie die Größe der Größe der Fensterlayouts für eine effektive Auflösung von 1024 x 768 Pixeln.** Ändern Sie automatisch die Größe dieser Fenster für niedrigere Bildschirmauflösungen auf eine Weise, die noch funktionsfähig ist.
-   **Achten Sie darauf, dass Sie Ihre Fenster in 96 Punkten pro Zoll (dpi) (mit 800 x 600 Pixel), 120 dpi (bei 1024 x 768 Pixel) und 144 dpi-Modi (bei 1200 x 900 Pixeln) testen.** Überprüfen Sie Layoutprobleme, z. b. das Abschneiden von Steuerelementen, Text und Fenstern und das Strecken von Symbolen und Bitmaps.
-   **Für Programme mit Berührungs-und mobilen Verwendungs Szenarien optimieren Sie für 120 dpi.** High-dpi-Bildschirme sind aktuell auf touchpcs und mobilen PCs weit verbreitet.

### <a name="window-size"></a>Fenstergröße

-   **Wählen Sie eine Standardfenster Größe aus, die für den Inhalt geeignet ist.** Achten Sie darauf, größere anfängliche Fenstergrößen zu verwenden, wenn Sie den Raum effektiv verwenden können.
-   **Verwenden Sie ein ausgewogenes Höhen-zu-Breite-Seitenverhältnis.** Ein Seitenverhältnis zwischen 3:5 und 5:3 wird bevorzugt, obwohl für Meldungs Dialogfelder (z. b. Fehler und Warnungen) ein Seitenverhältnis von 1:3 verwendet werden kann.
-   **Verwenden Sie nach Möglichkeit die Größe der Fenstergröße, um Scrollleisten und abgeschnittene Daten zu vermeiden.** Fenster mit dynamischem Inhalt, Dokumenten, Bildern, Listen und Strukturen profitieren am meisten von Fenstern mit Größenänderung.
-   **Bei Textdokumenten wird eine maximale Zeilenlänge von 80 Zeichen berücksichtigt** , damit der Text leichter lesbar ist. (Zeichen umfassen Buchstaben, Interpunktions Zeichen und Leerzeichen.)
-   Fenster mit fester Größe:
    -   **Fenster mit fester Größe müssen vollständig sichtbar und Größe aufweisen, damit Sie in den Arbeitsbereich passen.**
-   Fenster mit Größenänderung:
    -   **Fenster mit Größenänderung können für eine höhere Auflösung optimiert werden, bei Bedarf aber zur Anzeigezeit auf die tatsächliche Bildschirmauflösung.**
    -   **Progressivere Fenstergrößen müssen progressivere Informationen anzeigen.** Stellen Sie sicher, dass mindestens ein Fenster Teil bzw. das Steuerelement Inhalt geändert werden konnte.
    -   **Behalten Sie den oberen linken Ursprung des Inhalts bei, wenn die Größe des Fensters geändert wird.** Verschieben Sie den Ursprung nicht, um den Inhalt auszugleichen, wenn sich die Fenstergröße ändert.
    -   **Legen Sie eine maximale Inhalts Größe fest, wenn der Inhalt zu breit zu breit ist.** Wenn der Inhalt unhandlich wird, ändern Sie die Größe des Inhalts Bereichs nicht länger als die maximale Breite, oder ändern Sie den Ursprung des Inhalts, wenn die Größe des Fensters vergrößert wird. Behalten Sie stattdessen eine maximale Breite und einen fixierten oberen linken Ursprung bei.
    -   **Legen Sie eine minimale Fenstergröße fest, wenn eine Größe vorhanden ist, unter der der Inhalt nicht mehr verwendbar ist.** Legen Sie für Steuerelemente, die in der Größe geändert werden können, die Element Größen mit minimaler Größe auf die kleinsten funktionsgrößen fest, z. b. die minimale funktionale Spaltenbreite Optionale Benutzeroberflächen Elemente sollten vollständig entfernt werden.
    -   **Sie sollten die Präsentation ändern, damit der Inhalt in geringerer Größe verwendet werden kann.**

        ![Screenshot der Media Player-Steuerelemente ](images/vis-layout-image16.png)

        In diesem Beispiel ändert Windows Media Player sein Format, wenn das Fenster für das Standardformat zu klein wird.

### <a name="control-size"></a>Steuerelement Größe

-   **Legen Sie alle interaktiven Steuerelemente auf mindestens eine relative 16 x 16 Pixel.** Dies funktioniert gut für alle Eingabegeräte, einschließlich der Windows-Tablet-und Touchscreen-Technologie.
-   **Größen Steuerelemente, um abgeschnittene Daten zu vermeiden.** Kürzen Sie keine Daten, die gelesen werden müssen, um eine Aufgabe auszuführen. Spalten der Größen Listenansicht, um abgeschnittene Daten zu vermeiden.
-   **Größen Steuerelemente, um unnötigen Bildlauf auszuschließen.** Legen Sie die Steuerelemente etwas größer, wenn Sie eine Scrollleiste vermeiden. Es sollten nur wenige vertikale Scrollleisten und keine unnötigen horizontalen Scrollleisten vorhanden sein.

    ![Screenshot der Listen Größen, um eine Scrollleiste zu vermeiden ](images/vis-layout-image40.png)

    In diesem Beispiel ist die Dropdown Liste so groß, dass die Scrollleiste entfernt wird.

-   **Reduzieren Sie die Anzahl der Steuerelement Größen auf einer Oberfläche.** Verwenden Sie die [standardmäßigen empfohlenen Steuerelement Größen](#recommended-sizing-and-spacing) , und verwenden Sie bei Bedarf einige konsistente oder kleinere Steuerelemente mit einer konsistenten Größe. Versuchen Sie, eine einzelne Breite für Listenfelder und Struktur Ansichten zu verwenden, und nicht mehr als drei breiten für Befehls Schaltflächen und Dropdown Listen. Allerdings sollten Textfeld-und Kombinations Feld breiten die Länge ihrer längsten oder erwarteten Eingaben vorschlagen.

    ![Screenshot des Dialog Felds mit Listen und Schaltflächen ](images/vis-layout-image41.png)

    In diesem Beispiel wird ein Listenfeld und eine Befehls Schaltfläche konsistent verwendet.

-   **Fügen Sie für Steuerelemente, deren Größe auf der Grundlage Ihres Texts basiert, für jeden Text, der lokalisiert werden soll, eine zusätzliche 30% (bis zu 200 Prozent für kürzerer Text) ein.** Diese Richtlinie setzt voraus, dass das Layout in englischer Sprache verwendet wird. Beachten Sie auch, dass diese Richtlinie auf den lokalisierten Text und nicht auf Zahlen verweist.
-   **Erweitern Sie statische Text Steuerelemente, Kontrollkästchen und Options Felder auf die maximale Breite, die in das Layout passt.** Dadurch wird das Abschneiden aus Text und Lokalisierung variabler Länge vermieden.

    **Falsch:**

    ![Screenshot der Fortschrittskontrolle und des partiellen Texts ](images/vis-layout-image42.png)

    In diesem Beispiel wird der Steuerelement Text unnötig abgeschnitten.

### <a name="control-spacing"></a>Abstand von Steuerelementen

-   **Wenn die Steuerelemente nicht berühren, haben Sie mindestens 3 DLUs (5 relative Pixel) zwischen Ihnen.** Andernfalls können Benutzer zwischen den Steuerelementen auf inaktiven Bereich klicken. Da das Klicken auf inaktiven Speicherplatz weder Ergebnis noch visuelles Feedback hat, sind die Benutzer häufig unsicher, was schief gelaufen ist.

### <a name="placement"></a>Platzierung

-   **Ordnen Sie die Elemente der Benutzeroberfläche auf einer Oberfläche an, um von links nach rechts, von oben nach unten (in westlichen Kulturen) zu fließen.** Die Platzierung der UI-Elemente übermittelt Ihre Beziehung und sollte die Schritte zum Ausführen der Aufgabe widerspiegeln.
-   **Platzieren Sie Benutzeroberflächen Elemente, die eine Aufgabe in der oberen linken Ecke oder der oberen Mitte initiieren.** Legen Sie das UI-Element fest, das Benutzer zuerst den größten visuellen Fokus sehen sollten.
-   **Platzieren Sie Benutzeroberflächen Elemente, die eine Aufgabe in der unteren rechten Ecke vervollständigen.**
-   **Platzieren Sie verwandte UI-Elemente zusammen, und trennen Sie nicht verknüpfte Elemente.**
-   **Platzieren Sie erforderliche Schritte im Hauptflow.**
-   **Platzieren Sie optionale Schritte außerhalb des Hauptflusses,** möglicherweise durch die Verwendung eines geeigneten Hintergrunds oder progressiver Offenlegung.
-   **Platzieren Sie häufig verwendete Elemente vor selten verwendeten Elementen** im Scanpfad.

### <a name="focus"></a>Fokus

-   **Wählen Sie ein einzelnes Benutzeroberflächen Element aus, das Benutzer zunächst als Mittelpunkt betrachten müssen.** Der Schwerpunkt sollte ein wichtiger Punkt sein, den Benutzer schnell finden und verstehen müssen.
-   **Platzieren Sie den Fokuspunkt in der oberen linken Ecke oder der oberen Mitte.**
-   **Geben Sie dem Schwerpunkt Punkt den größten visuellen Fokus,** wie z. b. einen prominenten Text, eine Standardauswahl oder den ersten Eingabefokus.

### <a name="alignment"></a>Ausrichtung

-   Verwenden Sie normalerweise Left Alignment.
-   Verwenden Sie die richtige Ausrichtung für numerische Daten, insbesondere Spalten numerischer Daten.
-   Verwenden Sie die Rechte Ausrichtung für Commit-Schaltflächen sowie Steuerelemente, die mit dem rechten Fensterrand ausgerichtet sind.
-   Verwenden Sie die Zentrier Ausrichtung, wenn die linke oder die Rechte Ausrichtung ungeeignet ist oder unausgeglichen erscheint.
-   Wenn Sie Steuerelemente mit Text vertikal ausrichten, richten Sie die textbaselines so aus, dass Sie einen horizontalen horizontalen Lesefluss erhalten.
-   Informationen zur Beschriftungs Ausrichtung finden Sie im Abschnitt "Bezeichnungs [Ausrichtung](#label-alignment) " unter Entwurfskonzepte.

### <a name="accessibility"></a>Eingabehilfen

-   **Verwenden Sie Layout nicht als einzige Möglichkeit, wichtige Informationen über eine Benutzeroberfläche zu vermitteln.** Benutzer mit Sehbehinderungen können diese Präsentation möglicherweise nicht interpretieren. Stellen Sie z. b. sicher, dass Steuerelement Bezeichnungen ihre Beziehung mit anderen Elementen kommunizieren.
-   **Betten Sie keine untergeordneten Steuerelemente in Steuerelement Bezeichnungen ein, um einen Satz oder Ausdruck zu erstellen** Solche Zuordnungen basieren ausschließlich auf dem Layout und werden nicht durch Tastaturnavigation oder Barrierefreiheits Technologien behandelt. Außerdem ist dieses Verfahren nicht lokalisierbar, da die Satzstruktur von der Sprache abweicht.

    **Falsch:**

    ![Screenshot eines Textfelds in der Mitte eines Satzes ](images/vis-layout-image43.png)

    In diesem Beispiel wird das Textfeld nicht ordnungsgemäß in der Bezeichnung des Kontrollkästchens platziert.

    **Richtig:**

    ![Screenshot eines Textfelds am Ende eines Satzes ](images/vis-layout-image44.png)

    Hier wird das Textfeld nach der Bezeichnung des Kontrollkästchens platziert.

-   **Ermöglichen des Zugriffs auf die Gruppierung.** Gruppen, die von Fensterbereichen, Gruppen Feldern, Trennzeichen, Text Bezeichnungen und Aggregatoren definiert werden, werden automatisch von hilfshilfen behandelt. Gruppen, die nur von der Platzierung und den Hintergründen definiert werden, sind jedoch nicht, und Sie müssen Programm gesteuert für die Barrierefreiheit definiert werden.

Weitere Richtlinien finden Sie unter [Barrierefreiheit](inter-accessibility.md).

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstände

**Steuern der Größe**

In der folgenden Tabelle werden die empfohlenen Größen (Breite x Höhe oder Höhe bei einer einzelnen Zahl) für allgemeine Benutzeroberflächen Elemente (9 pt) aufgelistet. Segoe UI bei 96 dpi). Die breiten, die auf dem längsten Element in englischer Sprache basieren, addieren 30 Prozent für die Lokalisierung (bis zu 200 Prozent für kürzerer Text) für beliebigen Text (aber keine Zahlen), der lokalisiert wird.



|                                                                                                 |                            |                                                                                                   |                                                                                                            |
|-------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
|                                                                                                 | **Steuerung**<br/>     | **Dialog Einheiten**<br/>                                                                       | **Relative Pixel**<br/>                                                                             |
| ![Screenshot der Kontrollkästchen und deren Bezeichnungen ](images/vis-layout-image45.png)<br/>       | Kontrollkästchen<br/>     | 10<br/>                                                                                     | 17<br/>                                                                                              |
| ![Screenshot des Kombinations Felds ](images/vis-layout-image46.png)<br/>                          | Kombinations Felder<br/>     | Breite des längsten Elements + 30% x 14<br/>                                                       | Breite des längsten Elements + 30% x 23<br/>                                                                |
| ![Screenshot einer Befehls Schaltfläche ](images/vis-layout-image47.png)<br/>                   | Befehls Schaltflächen<br/> | 50 x 14<br/>                                                                                | 75 x 23<br/>                                                                                         |
| ![Screenshot eines von zwei ausgewählten Befehls Verknüpfungen ](images/vis-layout-image48.png)<br/>  | Befehls Verknüpfungen<br/>   | 25 (eine Zeile) oder 35 (zwei Zeilen)<br/>                                                        | 41 (eine Zeile) oder 58 (zwei Zeilen)<br/>                                                                 |
| ![Screenshot einer Dropdown Liste ](images/vis-layout-image49.png)<br/>                   | Dropdownlisten<br/> | Breite der längsten gültigen Daten + 30% x 14<br/>                                                 | Breite des längsten Elements + 30% x 23<br/>                                                                |
| ![Screenshot eines Listen Felds ](images/vis-layout-image50.png)<br/>                         | Listenfelder<br/>      | Breite des längsten Elements + 30% x eine ganzzahlige Anzahl von Elementen (mindestens 3 Elemente)<br/>            |                                                                                                            |
| ![Screenshot einer Liste von Bilddateien ](images/vis-layout-image51.png)<br/>            | Listenansichten<br/>      | Spaltenbreiten, die abgeschnittene Daten vermeiden, sind eine ganzzahlige Anzahl von Elementen.<br/>                 |                                                                                                            |
| ![Screenshot einer Statusanzeige ](images/vis-layout-image52.png)<br/>                     | Status anzeigen<br/>   | 107 oder 237 x 8<br/>                                                                         | 160 oder 355 x 15<br/>                                                                                 |
| ![Screenshot der Options Felder ](images/vis-layout-image53.png)<br/>                      | Optionsfelder<br/>   | 10<br/>                                                                                     | 17<br/>                                                                                              |
| ![Screenshot des Schieberegler-Steuer Elements ](images/vis-layout-image54.png)<br/>                     | Schieberegler<br/>         | 15<br/>                                                                                     | 24<br/>                                                                                              |
| ![Screenshot von Text: "Select Time Zone" ](images/vis-layout-image55.png)<br/>           | Text (statisch)<br/>   | 8<br/>                                                                                      | 13<br/>                                                                                              |
| ![Screenshot des leeren Textfelds ](images/vis-layout-image56.png)<br/>                     | Textfelder<br/>      | Breite der längsten oder erwarteten Eingabe + 30% x 14 (eine Zeile) + 10 für jede weitere Zeile<br/> | Breite der längsten gültigen Daten + 30% x 23 relative Pixel (eine Zeile) + 16 für jede weitere Zeile<br/> |
| ![Screenshot der in Windows-Explorer untergeordneten Ordner ](images/vis-layout-image57.png)<br/> | Strukturansichten<br/>      | Breite des längsten Elements + 30% x eine ganzzahlige Anzahl von Elementen (mindestens 5 Elemente)<br/>            |                                                                                                            |



 

**Abstand**

In der folgenden Tabelle sind die empfohlenen Abstände zwischen allgemeinen Benutzeroberflächen Elementen (9 pt) aufgelistet. Segoe UI bei 96 dpi).



|                                                                                                   |                                                                                                       |                                                                                           |                                                                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
|                                                                                                   | **Element**<br/>                                                                                | **Dialog Einheiten**<br/>                                                               | **Relative Pixel**<br/>                                                            |
| ![Bild, das den Abstand in Dialogfeld Rändern anzeigt ](images/vis_layout_image58.jpeg)<br/>        | Dialog Feldränder<br/>                                                                         | 7 auf allen Seiten<br/>                                                                 | 11 auf allen Seiten<br/>                                                                |
| ![Bild, das den Abstand zwischen Bezeichnungen und Steuerelementen anzeigt ](images/vis_layout_image59.jpeg)<br/>  | Zwischen Text Bezeichnungen und den zugehörigen Steuerelementen (z. b. Textfelder und Listenfelder)<br/> | 3<br/>                                                                              | 5<br/>                                                                              |
| ![Bild mit Abstand zwischen verknüpften Steuerelementen ](images/vis_layout_image60.jpeg)<br/>     | Zwischen verknüpften Steuerelementen<br/>                                                                   | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Bild mit Abstand zwischen nicht verknüpften Steuerelementen ](images/vis_layout_image61.jpeg)<br/>   | Zwischen nicht verwandten Steuerelementen<br/>                                                                 | 7<br/>                                                                              | 11<br/>                                                                             |
| ![Bild, das den Abstand des ersten Steuer Elements in einer Gruppe anzeigt ](images/vis_layout_image62.jpeg)<br/>  | Erstes Steuerelement in einem Gruppenfeld<br/>                                                               | 11 unten am oberen Rand des Gruppen Felds vertikal zum Gruppenfeld Titel ausrichten<br/> | 16 unten am oberen Rand des Gruppen Felds. vertikal zum Gruppenfeld Titel ausrichten<br/> |
| ![Aa511279. between-Related (en-US, MSDN. 10). jpg](images/vis_layout_image60.jpeg)<br/>         | Zwischen Steuerelementen in einem Gruppenfeld<br/>                                                            | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Bild, das Abstand zwischen Schaltflächen anzeigt ](images/vis_layout_image63.jpeg)<br/>              | Zwischen horizontalen oder vertikal angeordneten Schaltflächen<br/>                                        | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Bild, das den Abstand des letzten Steuer Elements in einer Gruppe anzeigt ](images/vis_layout_image64.jpeg)<br/>   | Letztes Steuerelement in einem Gruppenfeld<br/>                                                                | 7 über dem unteren Rand des Gruppen Felds<br/>                                            | 11 über dem unteren Rand des Gruppen Felds<br/>                                           |
| ![Bild, das den Abstand von der linken Kante des Gruppen Felds anzeigt ](images/vis_layout_image65.jpeg)<br/>  | Vom linken Rand eines Gruppen Felds<br/>                                                          | 6<br/>                                                                              | 9<br/>                                                                              |
| ![Bild, das den Abstand der Text Bezeichnung neben Steuerelement anzeigt ](images/vis_layout_image66.jpeg)<br/> | Text Bezeichnung neben einem Steuerelement<br/>                                                                | 3 unten vom oberen Rand des Steuer Elements<br/>                                             | 5 vom oberen Rand des Steuer Elements nach unten<br/>                                             |
| ![Bild, das den Abstand zwischen Text Absätzen anzeigt ](images/vis_layout_image67.jpeg)<br/>   | Zwischen Text Absätzen<br/>                                                                 | 7<br/>                                                                              | 11<br/>                                                                             |
|                                                                                                   | Der kleinste Raum zwischen interaktiven Steuerelementen<br/>                                                | 3 oder kein Leerzeichen<br/>                                                                  | 5 oder kein Leerzeichen<br/>                                                                  |
|                                                                                                   | Der kleinste Raum zwischen einem nicht interaktiven Steuerelement und einem anderen Steuerelement<br/>                     | 2<br/>                                                                              | 3<br/>                                                                              |



 

 

