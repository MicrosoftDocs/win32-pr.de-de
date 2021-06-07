---
title: Strukturansichten
description: Mit einer Strukturansicht können Benutzer eine hierarchisch angeordnete Sammlung von Objekten anzeigen und mit ihnen interagieren, indem sie entweder eine einzelne Auswahl oder eine Mehrfachauswahl verwenden.
ms.assetid: f0206485-e028-41d8-9be2-5d59f0a0b677
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ade51b421350dc90bf72e2ff1a683bf1d352f7c1
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524494"
---
# <a name="tree-views"></a>Strukturansichten

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Mit einer Strukturansicht können Benutzer eine hierarchisch angeordnete Sammlung von Objekten anzeigen und mit ihnen interagieren, indem sie entweder eine einzelne Auswahl oder eine Mehrfachauswahl verwenden.

In einer Struktur werden Objekte, die Daten enthalten, als Blattknoten bezeichnet, und Objekte, die andere Objekte enthalten, werden als Containerknoten bezeichnet. Ein einzelner, oberster Containerknoten wird als Stammknoten bezeichnet. Benutzer können Containerknoten erweitern und reduzieren, indem sie auf die Plus- und Minus-Erweiterungsschaltflächen klicken.

![Screenshot der Fenster-Explorer-Strukturansicht ](images/ctrl-tree-views-image1.png)

Eine typische Strukturansicht.

> [!Note]  
> Richtlinien im Zusammenhang mit [Layout](vis-layout.md) und [Menüs](cmd-menus.md) werden in separaten Artikeln vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

**Hierarchische Daten bedeuten nicht, dass Sie eine Strukturansicht verwenden müssen.** Häufig ist eine [Listenansicht](ctrl-list-views.md) eine einfachere, aber leistungsfähigere Wahl. Listenansichten:

-   Unterstützung mehrerer verschiedener Ansichten.
-   Unterstützt das Sortieren von Daten nach einer der Spalten in der Detailansicht.
-   Unterstützung der Organisation von Daten in Gruppen, wodurch eine Hierarchie mit zwei Ebenen gebildet wird.

**Um eine Listenansicht zu verwenden, können Sie hierarchische Informationen mithilfe der folgenden Verfahren abschwächen:**

-   Entfernen Sie ggf. den Stammknoten, da er häufig nicht erforderlich ist.
-   Verwenden Sie Listenansichtsgruppen, Registerkarten, [Dropdownlisten](/windows/desktop/uxguide/ctrl-drop)oder [erweiterbare Überschriften,](glossary.md) um die Container der obersten Ebene zu ersetzen.

    ![Screenshot von Listenansichtsgruppen mit Listen ](images/ctrl-tree-views-image2.png)

    In diesem Beispiel werden Listenansichtsgruppen für die Container der obersten Ebene verwendet.

    ![Screenshot der Registerkarten, die für Container der obersten Ebene verwendet werden ](images/ctrl-tree-views-image3.png)

    In diesem Beispiel werden Registerkarten für die Container der obersten Ebene verwendet.

    ![Screenshot der Dropdownliste, die als Container verwendet wird ](images/ctrl-tree-views-image4.png)

    In diesem Beispiel wird eine Dropdownliste für die Container der obersten Ebene verwendet.

-   Wenn ein zugeordnetes Steuerelement den Inhalt des ausgewählten Containers anzeigt, kann dieses Steuerelement niedrigere Ebenen der Hierarchie anzeigen.

    ![Screenshot des Inhaltsverzeichnisbereichs ](images/ctrl-tree-views-image5.png)

    In diesem Beispiel werden Container auf niedriger Ebene im Dokumentfenster angezeigt.

**Sie müssen eine Strukturansicht verwenden, wenn Sie eine Hierarchie mit mehr als zwei Ebenen anzeigen müssen (ohne den Stammknoten).**

Berücksichtigen Sie die folgenden Fragen, um zu entscheiden, ob eine Strukturansicht das richtige Steuerelement ist:

-   **Sind die Daten hierarchisch?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement.
-   **Verfügt die Hierarchie über mindestens drei Ebenen (ohne Stamm)?** Wenn dies nicht der Fall ist, sollten Sie Alternativen wie Listenansichtsgruppen, Registerkarten, Dropdownlisten oder erweiterbare Überschriften in Betracht ziehen.
-   **Verfügen die Elemente über zusätzliche Daten?** Falls ja, sollten Sie eine Listenansicht im Detailansichtsmodus verwenden, um die zusätzlichen Daten in vollem Umfang zu nutzen.
-   **Beziehen sich die Daten auf niedrigerer Ebene auf unabhängige Subtasks?** In diesem Falle sollten Sie die Informationen in einem zugeordneten Steuerelement oder in einem separaten Fenster anzeigen (angezeigt über [Befehlsschaltflächen](ctrl-command-buttons.md) oder [Links).](ctrl-command-links.md)
-   **Sind die Zielbenutzer erweitert?** Fortgeschrittene Benutzer sind mit der Verwendung von Strukturen vertrauter. Wenn Ihre Anwendung auf Benutzer ausgerichtet ist, sollten Sie die Verwendung von Strukturansichten vermeiden.
-   **Verfügen die Elemente über eine einzelne, natürliche, hierarchische Kategorisierung, die den meisten Benutzern vertraut ist?** In diesem Falle eignen sich die Daten ideal für eine Strukturansicht. Wenn mehrere Ansichten oder Sortierungen erforderlich sind, verwenden Sie stattdessen eine Listenansicht.
-   **Müssen Benutzer die Daten auf niedrigerer Ebene in einigen, aber nicht in allen Szenarien oder in einigen, aber nicht immer sehen?** In diesem Falle eignen sich die Daten ideal für eine Strukturansicht.

> [!Note]  
> Manchmal wird ein Steuerelement, das wie eine Strukturansicht aussieht, mithilfe einer Listenansicht implementiert. Wenden Sie in solchen Fällen die Richtlinien basierend auf der Verwendung und nicht auf der Implementierung an.

 

## <a name="design-concepts"></a>Entwurfskonzepte

Strukturen dienen dazu, Daten zu organisieren und die Suche zu erleichtern, aber es ist schwierig, Daten innerhalb einer Struktur leicht auffindbar zu machen. Beachten Sie bei der Entscheidung über Strukturansichten und deren Organisation die folgenden Prinzipien.

### <a name="predictability-and-discoverability"></a>Vorhersagbarkeit und Auffindbarkeit

**Eine Strukturansicht basiert auf den Beziehungen zwischen Objekten.** Strukturen funktionieren am besten, wenn die Objekte eine klare, bekannte, sich gegenseitig ausschließende Beziehung bilden, in der jedes Objekt einem einzelnen, leicht zu bestimmenden Container zugeordnet ist.

**Ein erhebliches Problem besteht darin, dass ein Objekt auf verschiedenen Knoten angezeigt werden kann.** Wo würden Benutzer beispielsweise erwarten, ein Hardwaregerät zu finden, das Musik spielt, über eine große Festplatte verfügt und einen USB-Anschluss verwendet? Möglicherweise in einem von mehreren verschiedenen Containerknoten, z. B. Multimedia, Speicher, USB und möglicherweise in Hardwareressourcen. Eine Lösung besteht darin, jedes Objekt unabhängig von den Umständen unter dem jeweils am besten geeigneten Container zu platzieren. Ein anderer Ansatz besteht darin, jedes Objekt unter allen containern zu platzieren, die angewendet werden. Erstere höher gestuft eine einfache, saubere Hierarchie und die zweite höher erfindbarkeit jeder hat Vorteile und potenzielle Probleme.

**Benutzer verstehen das Layout der Struktur möglicherweise nicht vollständig, bilden aber ein mentales Modell der Beziehungen, nachdem sie eine Weile mit der Struktur interagiert haben.** Wenn dieses mentale Modell falsch ist, führt dies zu Verwirrung. Angenommen, ein Musikplayer ist in den Containern Multimedia, Storage und USB zu finden. Diese Anordnung verbessert die Auffindbarkeit. Wenn ein Benutzer das Gerät zum ersten Mal in Multimedia findet, kann der Benutzer daraus schließen, dass alle Geräte wie Musikplayer im Multimediacontainer angezeigt werden. Der Benutzer erwartet dann, dass ähnliche Geräte, z. B. Digitalkameras, im Multimediacontainer angezeigt werden, und wird verwechselt, wenn dies nicht der Fall ist.

**Die Herausforderung beim Entwerfen einer Struktur besteht darin, die Auffindbarkeit mit einem vorhersagbaren Benutzermodell in Einklang zu bringen, das Verwechslungen minimiert.**

### <a name="breadth-vs-depth"></a>Breite und Tiefe

Benutzerfreundlichkeitsstudien haben gezeigt, dass **Benutzer objekte in einer Struktur, die breit ist, erfolgreicher finden als in einer Struktur, die tief ist.** Wenn Sie also eine Struktur entwerfen, sollten Sie die Breite über die Tiefe bevorzugen. Im Idealfall sollte eine Struktur nicht mehr als vier Ebenen (ohne Zählung des Stammknotens) aufweisen, und die am häufigsten verwendeten Objekte sollten in den ersten beiden Ebenen angezeigt werden.

### <a name="other-principles"></a>Weitere Prinzipien

-   Wenn Benutzer das gesuchte Suchen finden, werden sie nicht mehr danach suchen. Sie suchen nicht, wo sonst ein Objekt gefunden werden könnte, da sie dies nicht benötigen. Diese Benutzer können davon ausgehen, dass der erste Pfad, den sie finden, der einzige Pfad ist.
-   Benutzer haben Probleme, Objekte in großen, komplexen Strukturen zu finden. Benutzer führen keine umfassende manuelle Suche durch, um Objekte in solchen Strukturen zu finden. sie werden beendet, sobald sie der Meinung sind, dass sie einen angemessenen Aufwand unternommen haben. Daher müssen große, komplexe Strukturen durch andere Zugriffsmethoden wie die Wortsuche, einen Index oder die Filterung ergänzt werden.
-   Einige Programme ermöglichen Es Benutzern, ihre eigenen Strukturen zu erstellen. Obwohl solche selbst entworfenen Strukturen möglicherweise auf das mentale Modell eines Benutzers ausgerichtet sind, werden sie häufig zufällig und schlecht verwaltet. Während z. B. ein Dateisystem, ein E-Mail-Programm und eine Favoritenliste in der Regel ähnliche Arten von Informationen speichern, sind Benutzer selten daran interessiert, sie auf die gleiche Weise zu organisieren.

**Wenn Sie nur eine Sache tun...**

Wägen Sie sorgfältig die Vor- und Nachteile der Verwendung von Strukturansichten ab. Hierarchisch angeordnete Daten bedeuten nicht, dass Sie eine Strukturansicht verwenden müssen.

## <a name="usage-patterns"></a>Verwendungsmuster

Strukturansichten weisen mehrere Verwendungsmuster auf:



| Verwendung                           |    Beispiel                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Strukturansichten nur mit Containerknoten**<br/> Benutzer können jeweils einen Container anzeigen und mit diesem interagieren. <br/>                        | In der Regel verfügen diese Strukturansichten über ein zugeordnetes Steuerelement, das den Inhalt des ausgewählten Containers anzeigt, sodass Benutzer jeweils nur mit einem Container interagieren können. <br/> ![Screenshot des Container- und Inhaltsbereichs ](images/ctrl-tree-views-image6.png)<br/> In diesem Beispiel enthält die Strukturansicht nur Containerknoten. Der Inhalt des ausgewählten Knotens wird im zugeordneten Listenansicht-Steuerelement angezeigt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Strukturansichten mit Container- und Blattknoten**<br/> Benutzer können Container und Blätter anzeigen und mit ihnen interagieren.<br/>                       | In der Regel verfügen diese Strukturansichten über ein zugeordnetes Steuerelement, das den Inhalt des ausgewählten Containers oder Blatts anzeigt. Wenn Benutzer mit Blättern interagieren können, ist es häufig erforderlich, die Mehrfachauswahl zu unterstützen. <br/> ![Screenshot des Strukturansichtsbereichs und des Inhaltsbereichs ](images/ctrl-tree-views-image7.png)<br/> in diesem Beispiel verfügt die Strukturansicht sowohl über Container- als auch über Blattknoten. Da mehrfache Auswahl unterstützt wird, wird der Inhalt der geöffneten Elemente mithilfe von [Registerkarten](ctrl-tabs.md) im zugeordneten Steuerelement angezeigt.<br/> Alternativ kann die Strukturansicht über eine organisierende Liste verfügen, in der die Container Überschriften und die Blätter Optionen sind. <br/> ![Screenshot der Strukturansicht mit Überschriften und Optionen ](images/ctrl-tree-views-image8.png)<br/> In diesem Beispiel sind die Strukturblätter Optionen, und die Container sind Optionskategorien.<br/> |
| **Kontrollkästchenstrukturansichten**<br/> Benutzer können eine beliebige Anzahl von Elementen auswählen, einschließlich keiner.<br/>                                             | Die Kontrollkästchen zeigen deutlich an, dass eine Mehrfachauswahl möglich ist. verwenden Sie dieses Strukturmuster, wenn mehrfache Auswahl wichtig oder häufig verwendet wird. <br/> ![Screenshot der Strukturansicht mit Kontrollkästchen ](images/ctrl-tree-views-image9.png)<br/> In diesem Beispiel ermöglicht eine Kontrollkästchenstrukturansicht die Auswahl von Features, die ein- oder ausgeschaltet werden können.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Strukturansichts-Generatoren**<br/> Benutzer können eine Struktur erstellen, indem sie einen Container oder ein Blatt gleichzeitig hinzufügen und optional die Reihenfolge festlegen.<br/> | Viele Strukturen können von Benutzern erstellt oder geändert werden. Einige Strukturen werden mithilfe von Kontextmenüs und Drag & Drop (z. B. die Ordner im Windows-Explorer) erstellt, während andere Strukturen mithilfe eines speziellen Dialogfelds erstellt werden (z. B. die Favoritenliste in Windows Internet Explorer). <br/> ![Screenshot des Dialogfelds "Favoriten" ](images/ctrl-tree-views-image10.png)<br/> In diesem Beispiel aus Internet Explorer können Benutzer mithilfe eines Dialogfelds eine eigene Liste von Favoriten erstellen.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| **Strukturansichten mit alternativen Zugriffsmethoden**<br/> -Benutzer können Objekte auf andere Weise suchen, als eine hierarchische Struktur zu verwenden.<br/>        | Wie bereits erwähnt, haben Benutzer Probleme beim Suchen von Objekten in großen, komplexen Strukturen. Daher sollten solche Strukturen durch andere Zugriffsmethoden ergänzt werden, z. B. eine Wortsuche, einen Index oder eine Filterung. <br/> ![Screenshot der Registerkarten "Inhalt", "Index" und "Favoriten" ](images/ctrl-tree-views-image11.png)<br/> In diesem Beispiel können Benutzer auch über ein Inhaltsverzeichnis, einen Index und Favoriten auf Informationen zugreifen. Für einige Benutzer können die Registerkarten "Index" und "Suche" nützlicher sein als die Registerkarte "Inhalt".<br/> ![Screenshot des Windows-Startmenüs und des Suchfelds ](images/ctrl-tree-views-image12.png)<br/> In diesem Beispiel ermöglicht die Windows Startmenü Benutzern auch den Zugriff auf Programme, Dateien und Webseiten, indem sie einen Teil des Namens in das Feld Suchen eingeben.<br/>                                                                                                             |



 

## <a name="guidelines"></a>Richtlinien

### <a name="presentation"></a>Präsentation

-   **Sortieren Sie die Elemente innerhalb eines Containers in einer logischen Reihenfolge.** Sortieren Sie Namen in alphabetischer Reihenfolge, Zahlen in numerischer Reihenfolge und Datumsangaben in chronologischer Reihenfolge.
-   **Verwenden Sie das Always Show Selection-Attribut,** damit Benutzer das ausgewählte Element direkt bestimmen können, auch wenn das Steuerelement keinen Eingabefokus hat.
-   **Wenn die Struktur als Inhaltsverzeichnis verwendet wird, verwenden Sie das Attribut Einzelnes Erweitern, um die Verwaltung der Struktur zu vereinfachen.** Auf diese Weise wird nur der relevante Teil der Struktur erweitert.
-   **Vermeiden Sie es, leere Strukturen zu präsentieren.** Wenn ein Benutzer eine Struktur erstellt, initialisieren Sie die Struktur mit Anweisungen oder Beispielelementen, die Benutzer möglicherweise benötigen.

    ![Screenshot der Favoritenliste in Internet Explorer ](images/ctrl-tree-views-image13.png)

    In diesem Beispiel enthält die Liste zunächst Beispiele.

-   **Lassen Sie die Containerknoten nicht reduzierbar, wenn Benutzer keinen Grund haben, sie zu reduzieren.** Dies führt zu unnötiger Komplexität.
-   **Wenn die Ladeleistung ein Problem darstellt, zeigen Sie standardmäßig nur die Container der ersten und zweiten Ebene der Struktur an.** Sie können dann bei Bedarf zusätzliche Daten laden, wenn ein Benutzer Verzweigungen in der Struktur erweitert.
-   **Wenn Benutzer einen Container** erweitern oder reduzieren, sollten Sie diesen Zustand beibehalten, damit er beim nächsten Anzeigen der Strukturansicht wirksam wird, es sei denn, Benutzer bevorzugen wahrscheinlich den Start im Standardzustand. Persistenz sollte pro Struktur und Pro-Benutzer-Ansicht erfolgen.
-   **Wenn Container auf hoher Ebene ähnliche Inhalte haben, sollten Sie visuelle Hinweise verwenden, um sie zu unterscheiden.**

    **Falsch:**

    ![Screenshot von Outlook-Elementen mit unterschiedlichen Symbolen ](images/ctrl-tree-views-image14.png)

    In diesem Beispiel haben die Ordner Postfach und Archiv ähnliche Inhalte. Sobald die Strukturen weiter erweitert sind, ist es für Benutzer sehr schwierig zu wissen, wo sie sich in der Struktur befinden, was zu Verwirrung führt. Wenn Sie in den verschiedenen Abschnitten etwas andere Symbole verwenden, wird dieses Problem behoben.

-   **Erneutes Herstellen von Verbindungslinien.** Obwohl diese Zeilen eindeutig Beziehungen zwischen Container- und Blattknoten zeigen, fügen sie visuelle Unübersichtlichkeit hinzu, ohne das Verständnis erheblich zu verbessern. Insbesondere helfen sie nicht, wenn Knoten nahe beieinander liegen, und sie helfen auch nicht, wenn Knoten so weit voneinander entfernt sind, dass ein Bildlauf erforderlich ist.

    **Richtig:**

    ![Screenshot der Strukturansicht mit Verbindungslinien ](images/ctrl-tree-views-image15.png)

    **Besser:**

    ![Screenshot der Strukturansicht ohne Verbinden von Linien ](images/ctrl-tree-views-image16.png)

    Die Verbindungsleitungen helfen wenig, das Verständnis zu verinern.

### <a name="interaction"></a>Interaktion

-   **Erwägen Sie die Bereitstellung eines Doppelklickverhaltens.** Doppelklicken sollte die gleiche Wirkung wie das Auswählen eines Elements und das Ausführen des Standardbefehls haben.
-   **Machen Sie das Doppelklickverhalten redundant.** Es sollte immer eine Befehlsschaltfläche oder ein Kontextmenübefehl mit der gleichen Auswirkung geben.
-   Wenn ein Element eine weitere Erläuterung erfordert, **geben Sie die Erklärung in einem Infotip an.**

    ![Screenshot von Favoriten mit Infotip für ein Element ](images/ctrl-tree-views-image17.png)

    In diesem Beispiel enthält ein Infotip weitere Informationen.

-   **Stellen Sie Kontextmenüs relevanter Befehle zur Verfügung.** Zu diesen Befehlen gehören Ausschneiden, Kopieren, Einfügen, Entfernen oder Löschen, Umbenennen und Eigenschaften.
-   **Deaktivieren Sie beim Deaktivieren einer Strukturansicht auch alle zugeordneten Bezeichnungen und Befehlsschaltflächen.**

### <a name="tree-organization"></a>Strukturorganisation

-   **Verwenden Sie eine natürliche hierarchische Struktur, die den meisten Benutzern vertraut ist.**
-   **Wenn Sie eine solche Struktur nicht verwenden können, versuchen Sie, die Aufholbarkeit mit einem vorhersagbaren Benutzermodell zu ausgleichen, das Verwirrung minimiert.**
-   **Um die Aufholbarkeit sicher zu verbessern, platzieren Sie ein Element in mehreren Containern, wenn:**
    -   Das Element ist nicht mit anderen ähnlichen Elementen verknüpft (sodass Benutzer nicht durch falsche Zuordnungen verwirrend sind).
    -   Es gibt nur einige dieser redundant gefundenen Elemente (sodass die Struktur nicht aufgebläht wird).
-   **Verwenden Sie die einfachste hierarchische Struktur, die gut funktioniert.** Gehen Sie folgendermaßen vor:
    -   Platzieren Sie die objekte, auf die am häufigsten zugegriffen wird, in den ersten beiden Ebenen der Struktur (ohne Zählung des Stammknotens), und platzieren Sie weniger häufig verwendete Objekte weiter unten in der Hierarchie.
    -   Vermeiden Sie unnötige Container, oder kombinieren Sie redundante Container auf Zwischenebene.
-   **Die Breite gegenüber der Tiefe bevorzugen.** Im Idealfall sollte eine Struktur nicht mehr als vier Ebenen haben, und die objekte, auf die am häufigsten zugegriffen wird, sollten in den ersten beiden Ebenen angezeigt werden.
-   **Ermitteln Sie, ob Sie wirklich einen Stammknoten benötigen.** Geben Sie einen Stammknoten an, wenn Benutzer Befehle für die gesamte Struktur ausführen müssen (möglicherweise über ein Kontextmenü auf dem Stammknoten). Andernfalls ist die Struktur einfacher und einfacher zu verwenden.
-   **Wenn die Struktur über alternative Zugriffsmethoden wie eine Wortsuche oder einen Index verfügt, optimieren Sie die Struktur für das Durchsuchen, indem Sie sich auf den nützlichsten Inhalt konzentrieren.** Bei alternativen Zugriffsmethoden muss der Inhalt der Struktur nicht umfassend sein. Die Vereinfachung der Struktur erleichtert es Benutzern, die nützlichsten Inhalte zu finden.

### <a name="check-box-tree-views"></a>Kontrollkästchenstrukturansichten

-   **Zeigt die Anzahl der ausgewählten Elemente unterhalb der Liste an,** insbesondere, wenn Benutzer wahrscheinlich mehrere Elemente auswählen. Dieses Feedback hilft Benutzern zu bestätigen, dass ihre Auswahl richtig ist.

    ![Screenshot der Anzahl ausgewählter Elemente ](images/ctrl-tree-views-image18.png)

    In diesem Beispiel wird die Anzahl der ausgewählten Elemente unterhalb der Struktur angezeigt. Es ist klar, dass zwei Elemente nicht ausgewählt sind.

-   Wenn potenziell viele Elemente enthalten sind und sie wahrscheinlich alle auswählen oder löschen, fügen Sie Alle auswählen und Alle Befehlsschaltflächen löschen hinzu.
-   **Verwenden Sie Kontrollkästchen mit gemischtem Zustand, um eine Teilauswahl der Elemente in einem Container anzugeben.**

    **Richtig:**

    ![Screenshot des Fensters mit Kontrollkästchen für gemischten Zustand ](images/ctrl-tree-views-image19.png)

    In diesem Beispiel werden die Kontrollkästchen für gemischten Zustand verwendet, um eine Teilauswahl anzugeben.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstand

![Screenshot der Größen- und Abstandsgröße der Strukturansicht ](images/ctrl-tree-views-image20.png)

Empfohlene Größe und Abstand für Strukturansichtssteuerelemente.

-   **Wählen Sie eine Strukturansichtsbreite aus,** die das horizontale Scrollen für die meisten Elemente vermeidet, wenn die Struktur vollständig erweitert ist.
-   **Fügen Sie zusätzliche 30 Prozent hinzu, um die Lokalisierung zu ermöglichen.**
-   **Wählen Sie eine Strukturansichtshöhe aus, die unnötiges vertikales Scrollen überflüssig macht.** Erwägen Sie, eine Strukturansicht etwas länger zu gestalten (oder noch mehr, wenn Platz verfügbar ist), wenn dies die Notwendigkeit einer vertikalen Bildlaufleiste reduziert.

    **Falsch:**

    ![Screenshot des kurzen, schmalen Strukturansichtssteuerelements ](images/ctrl-tree-views-image21.png)

    In diesem Beispiel würden die Bildlaufleisten in den meisten Fällen entfernt, wenn die Strukturansicht etwas breiter und länger wäre. In dieser bestimmten Struktur kann jeweils nur ein Container geöffnet werden.

-   **Wenn Benutzer davon profitieren, die Strukturansicht zu vergrößern, können Sie die Größe der Strukturansicht und des übergeordneten Fensters ändern.** Auf diese Weise können Benutzer die Größe der Strukturansicht nach Bedarf anpassen.

## <a name="labels"></a>Bezeichnungen

### <a name="control-labels"></a>Steuerelementbezeichnungen

-   Alle Strukturansichten benötigen Bezeichnungen. Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz, der mit einem Doppelpunkt endet und [statischen Text verwendet.](glossary.md)
-   Weisen Sie einen eindeutigen Zugriffsschlüssel zu. Zuweisungsrichtlinien finden Sie unter [Tastatur.](inter-keyboard.md)
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Positionieren Sie die Bezeichnung über dem Steuerelement, und richten Sie die Bezeichnung am linken Rand des Steuerelements aus.
-   Schreiben Sie für Strukturansichten mit mehrfacher Auswahl die Bezeichnung, damit klar ist, dass eine Mehrfachauswahl möglich ist. Bezeichnungen der Kontrollkästchenstrukturansicht können weniger explizit sein.

    **Falsch:**

    ![Screenshot der Strukturansicht mit Komponentenbezeichnung ](images/ctrl-tree-views-image22.png)

    In diesem Beispiel stellt die Bezeichnung keine Informationen zur Mehrfachauswahl bereit.

    **Besser:**

    ![Screenshot der Strukturansicht mit einer oder mehreren Bezeichnungen ](images/ctrl-tree-views-image23.png)

    In diesem Beispiel gibt die Bezeichnung deutlich an, dass eine Mehrfachauswahl möglich ist.

    **Beste:**

    ![Screenshot der Strukturansicht mit Kontrollkästchen ](images/ctrl-tree-views-image24.png)

    In diesem Beispiel weisen die Kontrollkästchen deutlich darauf hin, dass mehrere Auswahlmöglichkeiten möglich sind, sodass die Bezeichnung nicht explizit sein muss.

### <a name="data-text"></a>Datentext

-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.

### <a name="instructional-text"></a>Anweisungstext

-   Wenn Sie Anweisungstext zu einer Strukturansicht hinzufügen müssen, fügen Sie ihn über der Bezeichnung hinzu. Verwenden Sie vollständige Sätze mit endender Interpunktion.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Ergänzende Erklärungen, die hilfreich, aber nicht notwendig sind, sollten kurz gehalten werden. Platzieren Sie diese Informationen entweder in Klammern zwischen der Bezeichnung und dem Doppelpunkt, nach der Main-Anweisung, wenn sie anstelle einer Bezeichnung verwendet wird, oder unterhalb des Steuerelements.

    ![Screenshot der Erklärung unterhalb der Strukturansicht ](images/ctrl-tree-views-image8.png)

    In diesem Beispiel befindet sich die ergänzende Erklärung unterhalb des -Steuerelements.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Strukturansichten:

-   Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Großschreibung, aber nicht den Unterstrich oder Doppelpunkt des Zugriffsschlüssels. Schließen Sie die Wortliste oder hierarchische Liste ein, wenn der Kontext eine Unterscheidung von regulären Listen erfordert.
-   Verwenden Sie für Strukturelemente den genauen Elementtext, einschließlich der Groß-/Großschreibung.
-   Strukturansichten werden nur in der Programmierung und anderen technischen Dokumentationen als Strukturansichten bezeichnet. Verwenden Sie überall sonst listen- oder hierarchische Listen, da der Begriff Struktur für die meisten Benutzer verwirrend ist.
-   Verwenden Sie zum Beschreiben der Benutzerinteraktion select für die Daten, und erweitern und reduzieren Sie die Schaltflächen Plus und Minus.
-   Formatieren Sie nach Möglichkeit die Bezeichnung und die Strukturelemente mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung und die Elemente nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

Beispiel: Wählen Sie in der Liste **Inhalt** **Benutzeroberfläche Entwerfen** aus.

Beim Verweisen auf Kontrollkästchen in einer Strukturansicht:

-   Verwenden Sie den genauen Bezeichnungstext einschließlich der Groß-/Großschreibung, und schließen Sie das Kontrollkästchen Wörter ein. Schließen Sie den Zugriffsschlüsselunterstrich nicht ein.
-   Um die Benutzerinteraktion zu beschreiben, verwenden Sie select und clear.
-   Formatieren Sie die Bezeichnung nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

Beispiel: Aktivieren Sie in der Liste **Zu sichernde Elemente** das **Kontrollkästchen Eigene Dokumente.**

