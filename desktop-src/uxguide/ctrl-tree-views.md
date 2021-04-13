---
title: Struktur Ansichten
description: Mit einer Strukturansicht können Benutzer eine hierarchisch angeordnete Auflistung von-Objekten anzeigen und mit ihnen interagieren, indem Sie entweder eine einzelne Auswahl oder eine Mehrfachauswahl verwenden.
ms.assetid: f0206485-e028-41d8-9be2-5d59f0a0b677
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c5cb2b6d48a30cba6de2136659231d9d37361621
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104564397"
---
# <a name="tree-views"></a>Struktur Ansichten

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Mit einer Strukturansicht können Benutzer eine hierarchisch angeordnete Auflistung von-Objekten anzeigen und mit ihnen interagieren, indem Sie entweder eine einzelne Auswahl oder eine Mehrfachauswahl verwenden.

In einer Struktur werden Objekte, die Daten enthalten, als Blattknoten bezeichnet und Objekte, die andere Objekte enthalten, als Container Knoten bezeichnet. Ein einzelner, der oberste Container Knoten wird als Stamm Knoten bezeichnet. Benutzer können Container Knoten erweitern oder reduzieren, indem Sie auf die Schaltflächen Plus und minus Expander klicken.

![Screenshot der Windows Explorer-Strukturansicht ](images/ctrl-tree-views-image1.png)

Eine typische Strukturansicht.

> [!Note]  
> Richtlinien im Zusammenhang mit [Layout](vis-layout.md) und [Menüs](cmd-menus.md) werden in separaten Artikeln dargestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

**Wenn Sie hierarchische Daten verwenden, bedeutet dies nicht, dass Sie eine Strukturansicht verwenden müssen.** Sehr häufig ist eine [Listenansicht](ctrl-list-views.md) eine einfachere, aber leistungsfähigere Wahl. Listenansichten:

-   Unterstützung mehrerer unterschiedlicher Ansichten.
-   Unterstützt das Sortieren von Daten in einer der Spalten in der Detailansicht.
-   Unterstützt das Organisieren von Daten in Gruppen und bildet eine Hierarchie mit zwei Ebenen.

**Um eine Listenansicht zu verwenden, können Sie hierarchische Informationen mithilfe der folgenden Techniken vereinfachen:**

-   Entfernen Sie den Stamm Knoten, falls vorhanden, da er häufig nicht erforderlich ist.
-   Verwenden Sie Listen Ansichts Gruppen, Registerkarten, [Dropdown Listen](/windows/desktop/uxguide/ctrl-drop)oder [erweiterbare Überschriften](glossary.md) , um die Container der obersten Ebene zu ersetzen.

    ![Screenshot der Listen Ansichts Gruppen mit Listen ](images/ctrl-tree-views-image2.png)

    In diesem Beispiel werden Listen Ansichts Gruppen für Container der obersten Ebene verwendet.

    ![Screenshot der für Container der obersten Ebene verwendeten Registerkarten ](images/ctrl-tree-views-image3.png)

    In diesem Beispiel werden Registerkarten für die Container der obersten Ebene verwendet.

    ![Screenshot der Dropdown Liste, die als Container verwendet wird ](images/ctrl-tree-views-image4.png)

    In diesem Beispiel wird eine Dropdown Liste für die Container der obersten Ebene verwendet.

-   Wenn ein zugeordnetes Steuerelement den Inhalt des ausgewählten Containers anzeigt, kann dieses Steuerelement niedrigere Ebenen der Hierarchie anzeigen.

    ![Screenshot des Bereichs "Inhaltsverzeichnis" ](images/ctrl-tree-views-image5.png)

    In diesem Beispiel werden Container auf niedriger Ebene im Dokument Fenster angezeigt.

**Sie müssen eine Strukturansicht verwenden, wenn Sie eine Hierarchie mit mehr als zwei Ebenen (ohne den Stamm Knoten) anzeigen müssen.**

Um zu entscheiden, ob eine Strukturansicht das richtige Steuerelement ist, sollten Sie die folgenden Fragen beachten:

-   **Sind die Daten hierarchisch?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement.
-   **Hat die Hierarchie mindestens drei Ebenen (ohne den Stamm)?** Wenn dies nicht der Fall ist, sollten Sie Alternativen wie Listen Ansichts Gruppen, Registerkarten, Dropdown Listen oder erweiterbare Überschriften in Erwägung ziehen.
-   **Haben die Elemente zusätzliche Daten?** Wenn dies der Fall ist, sollten Sie eine Listenansicht im Detail Ansichtsmodus verwenden, um die zusätzlichen Daten in vollem Umfang zu nutzen.
-   **Beziehen sich die Daten auf niedrigerer Ebene auf unabhängige Unteraufgaben?** Wenn dies der Fall ist, sollten Sie die Informationen in einem zugeordneten Steuerelement oder in einem separaten Fenster anzeigen (angezeigt mithilfe von [Befehls](ctrl-command-buttons.md) Schaltflächen oder [Links](ctrl-command-links.md)).
-   **Sind die Ziel Benutzer erweitert?** Fortgeschrittene Benutzer sind besser mit der Verwendung von Strukturen vertraut. Wenn Ihre Anwendung auf Anfänger ausgerichtet ist, sollten Sie die Verwendung von Struktur Ansichten vermeiden.
-   **Verfügen die Elemente über eine einzelne, natürliche und hierarchische Kategorisierung, die den meisten Benutzern vertraut ist?** Wenn dies der Fall ist, sind die Daten für eine Strukturansicht ideal. Wenn Sie mehrere Ansichten oder Sortierungen benötigen, verwenden Sie stattdessen eine Listenansicht.
-   **Müssen die Benutzer die Daten auf niedrigerer Ebene in einigen, aber nicht in allen Szenarios oder in einigen, aber nicht in allen Fällen sehen?** Wenn dies der Fall ist, sind die Daten für eine Strukturansicht ideal.

> [!Note]  
> Manchmal wird ein Steuerelement, das wie eine Strukturansicht aussieht, mithilfe einer Listenansicht implementiert. Wenden Sie in solchen Fällen die Richtlinien auf Grundlage der Verwendung, nicht auf die Implementierung an.

 

## <a name="design-concepts"></a>Entwurfskonzepte

Strukturen sind zum Organisieren von Daten gedacht und können problemlos gefunden werden, aber es ist schwierig, die Daten in einer Struktur leicht auffindbar zu machen. Beachten Sie bei der Entscheidung über Struktur Ansichten und deren Organisation die folgenden Prinzipien.

### <a name="predictability-and-discoverability"></a>Vorhersagbarkeit und Auffindbarkeit

**Eine Strukturansicht basiert auf den Beziehungen zwischen Objekten.** Strukturen funktionieren am besten, wenn die Objekte eine klare, bekannte, sich gegenseitig ausschließende Beziehung bilden, in der jedes Objekt einem einzelnen, leicht zu erführenden Container zugeordnet ist.

**Ein erhebliches Problem ist, dass ein Objekt in verschiedenen Knoten vorkommen kann.** Wenn z. b. die Benutzer ein Hardware Gerät finden, das Musik spielt, eine große Festplatte hat und einen USB-Anschluss verwendet? Vielleicht in einem von mehreren unterschiedlichen Container Knoten wie Multimedia, Storage, USB und möglicherweise in Hardware Ressourcen. Eine Lösung besteht darin, jedes Objekt unabhängig von den Bedingungen unter dem jeweils am besten geeigneten Container zu platzieren. ein anderer Ansatz besteht darin, jedes Objekt in alle Container zu platzieren, die angewendet werden. Der erste fördert eine einfache, saubere Hierarchie, und letztere stuft die Auffindbarkeit herauf, die jeweils vor-und potenziellen Problemen stehen.

**Benutzer können das Layout der Struktur nicht vollständig verstehen, Sie bilden jedoch ein geistiges Modell der Beziehungen, nachdem Sie eine Weile mit der Struktur interagieren.** Wenn dieses geistige Modell falsch ist, führt dies zu Verwirrung. Nehmen wir beispielsweise an, dass sich ein Musikplayer in Multimedia-, Speicher-und USB-Containern befindet. Durch diese Anordnung wird die Auffindbarkeit verbessert. Wenn ein Benutzer das Gerät zum ersten Mal in Multimedia findet, wird der Benutzer möglicherweise davon ausgehen, dass alle Geräte wie Musik-Player im Multimedia-Container angezeigt werden. Der Benutzer erwartet dann, dass ähnliche Geräte (z. b. digitale Kameras) im Multimedia-Container angezeigt werden und verwirrt, wenn dies nicht der Fall ist.

**Die Herausforderung beim Entwerfen einer Struktur besteht darin, die Auffindbarkeit mit einem vorhersagbaren Benutzer Modell auszugleichen, das Verwirrung minimiert.**

### <a name="breadth-vs-depth"></a>Breite und Tiefe

Nutzbarkeits Studien haben ergeben, dass die **Benutzer bei der Suche nach Objekten in einer Struktur, die weitgehend stark ist, nicht in einer tiefgreifenden Struktur erfolgreich sind**. Wenn Sie also eine Struktur entwerfen, sollten Sie Breite im Detail bevorzugen. Idealerweise sollte eine Struktur nicht mehr als vier Ebenen aufweisen (ohne den Stamm Knoten zu zählen), und die am häufigsten verwendeten Objekte sollten in den ersten beiden Ebenen angezeigt werden.

### <a name="other-principles"></a>Weitere Prinzipien

-   Wenn Benutzer suchen, nach denen Sie suchen, können Sie nicht mehr suchen. Sie sehen nicht, wo ein Objekt möglicherweise gefunden wird, da es nicht erforderlich ist. Diese Benutzer können davon ausgehen, dass der erste Pfad, den Sie finden, der einzige Pfad ist.
-   Benutzer haben Probleme beim Auffinden von Objekten in großen, komplexen Strukturen. Benutzer führen keine vollständige manuelle Suche durch, um Objekte in solchen Strukturen zu finden. Sie werden angehalten, wenn Sie der Ansicht sind, dass Sie einen angemessenen Aufwand aufgewendet haben. Daher müssen große, komplexe Strukturen durch andere Zugriffsmethoden ergänzt werden, wie z. b. die Suche nach Word, einen Index oder das Filtern.
-   Einige Programme ermöglichen Benutzern das Erstellen eigener Strukturen. Diese selbst entworfenen Strukturen können zwar an das geistige Modell eines Benutzers angepasst werden, Sie werden jedoch oft willkürlich und unzureichend verwaltet. Wenn z. b. ein Dateisystem, ein e-Mail-Programm und eine Favoritenliste in der Regel ähnliche Arten von Informationen speichern, stören sich Benutzer selten darauf, Sie auf dieselbe Weise zu organisieren.

**Wenn Sie nur eine Aktion ausführen...**

Wiegen Sie die Vorteile und Nachteile der Verwendung von Struktur Ansichten sorgfältig aus. Das verwenden hierarchisch angeordneter Daten bedeutet nicht, dass Sie eine Strukturansicht verwenden müssen.

## <a name="usage-patterns"></a>Verwendungsmuster

Struktur Ansichten verfügen über mehrere Verwendungs Muster:



|                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Struktur Ansichten mit nur Container Knoten**<br/> Benutzer können jeweils einen Container anzeigen und mit ihnen interagieren. <br/>                        | In der Regel verfügen diese Struktur Ansichten über ein zugeordnetes Steuerelement, das den Inhalt des ausgewählten Containers anzeigt, sodass Benutzer nur mit jeweils einem Container interagieren können. <br/> ![Screenshot des Bereichs "Container" und "Inhalt" ](images/ctrl-tree-views-image6.png)<br/> In diesem Beispiel enthält die Strukturansicht nur Container Knoten. Der Inhalt des ausgewählten Knotens wird im zugeordneten Listenansicht-Steuerelement angezeigt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Struktur Ansichten mit Container-und Blattknoten**<br/> Benutzer können Container und Blätter anzeigen und mit ihnen interagieren.<br/>                       | In der Regel verfügen diese Struktur Ansichten über ein zugeordnetes Steuerelement, das den Inhalt des ausgewählten Containers oder Blatts anzeigt. Wenn Benutzer mit Blättern interagieren können, ist es häufig erforderlich, die Mehrfachauswahl zu unterstützen. <br/> ![Screenshot des Fensters "Strukturansicht" und "Inhalt" ](images/ctrl-tree-views-image7.png)<br/> in diesem Beispiel enthält die Strukturansicht sowohl Container-als auch Blattknoten. Da die Mehrfachauswahl unterstützt wird, werden die Inhalte der geöffneten Elemente mithilfe von [Registerkarten](ctrl-tabs.md) im zugeordneten Steuerelement angezeigt.<br/> Alternativ kann die Strukturansicht über eine organisierte Liste verfügen, in der die Container Überschriften sind und die Blätter Optionen sind. <br/> ![Screenshot der Strukturansicht mit Überschriften und Optionen ](images/ctrl-tree-views-image8.png)<br/> In diesem Beispiel sind die Struktur Blätter Optionen, und die Container sind Options Kategorien.<br/> |
| **Strukturansicht für Kontrollkästchen**<br/> Benutzer können beliebig viele Elemente auswählen, einschließlich "keine".<br/>                                             | Die Kontrollkästchen geben eindeutig an, dass mehrere Auswahlmöglichkeiten möglich sind. Verwenden Sie dieses Struktur Muster, wenn Mehrfachauswahl erforderlich oder häufig verwendet wird. <br/> ![Screenshot der Strukturansicht mit Kontrollkästchen ](images/ctrl-tree-views-image9.png)<br/> In diesem Beispiel ermöglicht eine Kontrollkästchen-Strukturansicht die Auswahl von Funktionen, die aktiviert oder deaktiviert werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Strukturansicht-Generatoren**<br/> Benutzer können eine Struktur erstellen, indem Sie einen Container oder ein Blatt gleichzeitig hinzufügen und optional die Reihenfolge festlegen.<br/> | Viele Strukturen können von Benutzern erstellt oder geändert werden. einige Strukturen werden mithilfe von Kontextmenüs und Drag & amp; Drop (z. b. die Ordner in Windows-Explorer) direkt erstellt, während andere Strukturen mithilfe eines spezialisierten Dialog Felds erstellt werden (z. b. die Favoritenliste in Windows Internet Explorer). <br/> ![Screenshot des Dialog Felds "Favoriten" ](images/ctrl-tree-views-image10.png)<br/> In diesem Beispiel aus Internet Explorer können Benutzer mit einem Dialogfeld eine eigene Liste von Favoriten erstellen.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| **Struktur Ansichten mit alternativen Zugriffsmethoden**<br/> Benutzer können Objekte auf andere Weise als mit einer hierarchischen Struktur suchen.<br/>        | Wie bereits erwähnt, haben Benutzer Probleme beim Auffinden von Objekten in großen, komplexen Strukturen, sodass solche Strukturen durch andere Zugriffsmethoden, z. b. eine Wort Suche, einen Index oder eine Filterung, ergänzt werden sollten. <br/> ![Screenshot der Registerkarten Inhalt, Index und Favoriten ](images/ctrl-tree-views-image11.png)<br/> in diesem Beispiel können Benutzer auch auf Informationen mithilfe eines Inhaltsverzeichnisses, eines Indexes und von Favoriten zugreifen. für einige Benutzer können die Registerkarten Index und Search nützlicher sein als die Registerkarte Inhalt.<br/> ![Screenshot des Windows-Startmenüs und-Suchfelds ](images/ctrl-tree-views-image12.png)<br/> In diesem Beispiel ermöglicht das Windows-Startmenü Benutzern auch den Zugriff auf Programme, Dateien und Webseiten, indem Sie einen Teil des Namens in das Suchfeld eingeben.<br/>                                                                                                             |



 

## <a name="guidelines"></a>Richtlinien

### <a name="presentation"></a>Präsentation

-   **Sortieren Sie die Elemente in einem Container in einer logischen Reihenfolge.** Sortieren von Namen in alphabetischer Reihenfolge, Zahlen in numerischer Reihenfolge und Datumsangaben in chronologischer Reihenfolge.
-   **Verwenden Sie das Attribut "Auswahl immer anzeigen** ", damit Benutzer das ausgewählte Element problemlos ermitteln können, auch wenn das Steuerelement nicht den Eingabefokus besitzt.
-   **Wenn die Struktur als Inhaltsverzeichnis fungiert, verwenden Sie das einzelne Expand-Attribut, um die Verwaltung der Struktur zu vereinfachen.** Auf diese Weise wird nur der relevante Teil der Struktur erweitert.
-   **Vermeiden Sie es, leere Strukturen darzustellen.** Wenn ein Benutzer eine Struktur erstellt, initialisieren Sie die Struktur mit Anweisungen oder Beispiel Elementen, die Benutzer möglicherweise benötigen.

    ![Screenshot der Internet Explorer-Favoritenliste ](images/ctrl-tree-views-image13.png)

    In diesem Beispiel wird die Liste anfänglich mit Beispielen dargestellt.

-   **Machen Sie die Container Knoten nicht reduzierbar, wenn die Benutzer keinen Grund haben, Sie zu reduzieren.** Dadurch wird unnötige Komplexität hinzugefügt.
-   **Wenn die Last Leistung problematisch ist, zeigen Sie standardmäßig nur die Container der ersten und zweiten Ebene der Struktur an.** Anschließend können Sie zusätzliche Daten Bedarfs gesteuert laden, wenn ein Benutzer Verzweigungen in der Struktur erweitert.
-   **Wenn Benutzer einen Container erweitern oder reduzieren, legen Sie diesen Zustand dauerhaft fest, sodass er beim nächsten Anzeigen der Strukturansicht wirksam** wird, es sei denn, die Benutzer werden wahrscheinlich lieber mit dem Standardzustand beginnen. Persistenz sollte in einer Struktur bezogenen Ansicht (pro Benutzer) erfolgen.
-   **Wenn auf der Basis von Containern ähnlicher Inhalt vorhanden ist, sollten Sie visuelle Hinweise verwenden, um Sie zu unterscheiden.**

    **Falsch:**

    ![Screenshot der Outlook-Elemente mit unterschiedlichen Symbolen ](images/ctrl-tree-views-image14.png)

    In diesem Beispiel haben die Ordner Mailbox und Archive ähnliche Inhalte. Nachdem die Strukturen erweitert wurden, ist es für Benutzer sehr schwierig, zu wissen, wo Sie sich in der Struktur befinden, was zu Verwechslungen führt. Das Verwenden von etwas anderen Symbolen in den verschiedenen Abschnitten würde dieses Problem beheben.

-   **Überdenken Sie das Verbinden von Zeilen** Obwohl in diesen Zeilen eindeutig Beziehungen zwischen Container-und Blattknoten angezeigt werden, fügen Sie visuelle Cluster hinzu, ohne das Verständnis erheblich zu unterstützen. Insbesondere sind Sie nicht hilfreich, wenn Knoten nah beieinander sind, und Sie helfen nicht, wenn Knoten so weit voneinander entfernt sind, dass ein Bildlauf erforderlich ist.

    **Richtig:**

    ![Screenshot der Strukturansicht mit Verbindungslinien ](images/ctrl-tree-views-image15.png)

    **Besserer**

    ![Screenshot der Strukturansicht ohne Verbindungslinien ](images/ctrl-tree-views-image16.png)

    Die Verbindungslinien unterstützen kaum das Verständnis.

### <a name="interaction"></a>Interaktion

-   **Sie sollten das doppelte Klickverhalten bereitstellen.** Das Doppelklicken muss dieselbe Wirkung wie das Auswählen eines Elements und das Ausführen seines Standard Befehls haben.
-   **Doppelklick Verhalten redundant.** Es sollte immer eine Befehls Schaltfläche oder ein Kontextmenü Befehl vorhanden sein, der dieselbe Auswirkung hat.
-   Wenn ein Element ausführlicher erläutert werden muss, **Geben Sie die Erläuterung in einem InfoTipp** an.

    ![Screenshot von Favoriten mit Infotipp für ein Element ](images/ctrl-tree-views-image17.png)

    In diesem Beispiel enthält ein Infotipp Weitere Informationen.

-   **Stellen Sie Kontextmenüs relevanter Befehle bereit.** Zu diesen Befehlen zählen Ausschneiden, kopieren, einfügen, entfernen oder löschen, umbenennen und Eigenschaften.
-   **Deaktivieren Sie bei der Deaktivierung einer Strukturansicht auch alle zugeordneten Bezeichnungen und Befehls Schaltflächen.**

### <a name="tree-organization"></a>Struktur Organisation

-   **Verwenden Sie eine natürliche hierarchische Struktur, die den meisten Benutzern vertraut ist.**
-   **Wenn Sie diese Struktur nicht verwenden können, versuchen Sie, die Auffindbarkeit mit einem vorhersagbaren Benutzer Modell auszugleichen, das Verwirrung minimiert.**
-   **Um die Auffindbarkeit sicher zu verbessern, platzieren Sie ein Element in mehreren Containern, wenn:**
    -   Das Element steht nicht im Zusammenhang mit anderen ähnlichen Elementen (sodass Benutzer nicht durch falsche Zuordnungen verwechselt werden).
    -   Es gibt nur einige der redundant gefundenen Elemente (sodass die Struktur nicht in den BLOB-Bereich wird).
-   **Verwenden Sie die einfachste hierarchische Struktur, die gut funktioniert.** Gehen Sie folgendermaßen vor:
    -   Platzieren Sie die am häufigsten verwendeten Objekte in den ersten beiden Ebenen der Struktur (ohne den Stamm Knoten zu zählen), und platzieren Sie weniger häufig verwendete Objekte weiter unten in der Hierarchie.
    -   Vermeiden Sie unnötige oder kombinierende Container der Zwischenebene.
-   **Breite über Tiefe bevorzugen.** Idealerweise sollte eine Struktur nicht mehr als vier Ebenen aufweisen, und die am häufigsten verwendeten Objekte sollten in den ersten beiden Ebenen angezeigt werden.
-   **Stellen Sie fest, ob Sie wirklich einen Stamm Knoten benötigen.** Geben Sie einen Stamm Knoten an, wenn Benutzer in der Lage sein müssen, Befehle in der gesamten Struktur auszuführen (möglicherweise mithilfe eines Kontextmenüs auf dem Stamm Knoten). Andernfalls ist die Struktur einfacher und ohne diese zu verwenden.
-   **Wenn die Struktur Alternative Zugriffsmethoden hat, z. b. eine Wort Suche oder einen Index, optimieren Sie die Struktur für das Durchsuchen, indem Sie sich auf die nützlichsten Inhalte konzentrieren.** Bei alternativen Zugriffsmethoden muss der Inhalt der Struktur nicht umfassend sein. Wenn Sie die Struktur vereinfachen, ist es für Benutzer einfacher, die nützlichsten Inhalte zu finden.

### <a name="check-box-tree-views"></a>Strukturansicht für Kontrollkästchen

-   **Zeigt die Anzahl der ausgewählten Elemente unterhalb der Liste** an, insbesondere, wenn Benutzer wahrscheinlich mehrere Elemente auswählen. Mithilfe dieses Feedbacks können Benutzer bestätigen, dass Ihre Auswahl richtig ist.

    ![Screenshot der Anzahl ausgewählter Elemente ](images/ctrl-tree-views-image18.png)

    In diesem Beispiel wird die Anzahl der ausgewählten Elemente unterhalb der Struktur angezeigt. Es ist klar, dass zwei Elemente nicht ausgewählt sind.

-   Wenn es potenziell viele Elemente gibt und Sie alle auswählen oder löschen, fügen Sie die Option Alles auswählen und alle Befehls Schaltflächen Löschen hinzu.
-   **Verwenden Sie Kontrollkästchen mit gemischtem Zustand, um die partielle Auswahl der Elemente in einem Container anzugeben.**

    **Richtig:**

    ![Screenshot des Fensters mit den Kontrollkästchen für gemischten Zustand ](images/ctrl-tree-views-image19.png)

    In diesem Beispiel werden die Kontrollkästchen für den gemischten Zustand verwendet, um die partielle Auswahl anzugeben.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstände

![Screenshot der Größenanpassung und des Abstands der Baumansicht ](images/ctrl-tree-views-image20.png)

Empfohlene Größe und Abstände für Strukturansicht-Steuerelemente.

-   **Wählen Sie eine Struktur Ansichts Breite aus, die** für die meisten Elemente keinen horizontalen Bildlauf durchführen muss, wenn die Struktur vollständig erweitert ist.
-   **Fügen Sie zusätzliche 30 Prozent ein, um die Lokalisierung zu ermöglichen.**
-   **Wählen Sie eine Struktur Ansichts Höhe aus, die unnötige vertikale Bildläufe ausschließt.** Nehmen Sie an, dass eine Strukturansicht etwas länger ist (oder sogar noch mehr, wenn verfügbarer Speicherplatz vorhanden ist), wenn dies dazu führt, dass eine vertikale Schiebe Leiste reduziert wird.

    **Falsch:**

    ![Screenshot des kurzen, schmalen Strukturansicht-Steuer Elements ](images/ctrl-tree-views-image21.png)

    In diesem Beispiel würden die Bild Lauf leisten in den meisten Fällen durch eine etwas breitere und längere Darstellung der Strukturansicht eliminiert werden. In dieser speziellen Struktur kann jeweils nur ein einziger Container geöffnet werden.

-   **Wenn Benutzer davon profitieren, dass die Strukturansicht größer wird, können Sie die Strukturansicht und deren übergeordnetes Fenster ändern.** Auf diese Weise können Benutzer die Struktur Ansichts Größe nach Bedarf anpassen.

## <a name="labels"></a>Bezeichnungen

### <a name="control-labels"></a>Steuerelement Bezeichnungen

-   Alle Struktur Ansichten benötigen Bezeichnungen. Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz, enden Sie mit einem Doppelpunkt, und verwenden Sie [statischen Text](glossary.md).
-   Weisen Sie einen eindeutigen Zugriffsschlüssel zu. Informationen zu Zuweisungs Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Positionieren Sie die Bezeichnung über dem Steuerelement, und richten Sie die Bezeichnung am linken Rand des Steuer Elements aus.
-   Schreiben Sie bei Mehrfachauswahl-Struktur Ansichten die Bezeichnung, damit klar ist, dass mehrere Auswahlmöglichkeiten möglich sind. Die Kontrollkästchen Struktur Ansichts Bezeichnungen können weniger explizit sein.

    **Falsch:**

    ![Screenshot der Strukturansicht mit der Bezeichnung "Komponenten" ](images/ctrl-tree-views-image22.png)

    In diesem Beispiel stellt die Bezeichnung keine Informationen zur Mehrfachauswahl zur Verfügung.

    **Besserer**

    ![Screenshot der Strukturansicht mit einer oder mehreren Bezeichnung ](images/ctrl-tree-views-image23.png)

    In diesem Beispiel gibt die Bezeichnung eindeutig an, dass mehrere Auswahlmöglichkeiten möglich sind.

    **Best**

    ![Screenshot der Strukturansicht mit Kontrollkästchen ](images/ctrl-tree-views-image24.png)

    In diesem Beispiel geben die Kontrollkästchen eindeutig an, dass eine Mehrfachauswahl möglich ist, sodass die Bezeichnung nicht explizit sein muss.

### <a name="data-text"></a>Datentext

-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.

### <a name="instructional-text"></a>Anweisungs Text

-   Wenn Sie Anweisungs Text über eine Strukturansicht hinzufügen müssen, fügen Sie ihn oberhalb der Bezeichnung hinzu. Verwenden Sie vollständige Sätze mit endinterpunktions Zeichen.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Ergänzende Erklärungen, die hilfreich, aber nicht erforderlich sind, sollten kurz gehalten werden. Platzieren Sie diese Informationen entweder in Klammern zwischen der Bezeichnung und dem Doppelpunkt, und zwar nach der Haupt Anweisung, wenn Sie anstelle einer Bezeichnung verwendet wird, oder unterhalb des Steuer Elements.

    ![Screenshot der Erläuterung unterhalb der Strukturansicht ](images/ctrl-tree-views-image8.png)

    In diesem Beispiel befindet sich die ergänzende Erklärung unterhalb der Steuerung.

## <a name="documentation"></a>Dokumentation

Beim Verweis auf Struktur Ansichten:

-   Verwenden Sie den genauen Bezeichnungs Text, einschließlich der Groß-und Kleinschreibung, aber nicht den Unterstrich oder Doppelpunkt des Zugriffsschlüssels. Fügen Sie die Wortliste oder die hierarchische Liste ein, wenn der Kontext einen Unterschied zu regulären Listen erfordert.
-   Verwenden Sie für Baum Elemente den exakten Element Text, einschließlich der Groß-/Kleinschreibung.
-   Weitere Informationen finden Sie in den Struktur Ansichten nur in der Programmierung und in anderen technischen Dokumentationen. Verwenden Sie in allen anderen Fällen Liste oder hierarchische Liste, da der Begriff Baum für die meisten Benutzer verwirrend ist.
-   Um die Interaktion von Benutzern zu beschreiben, verwenden Sie für die Daten auswählen, und erweitern und reduzieren Sie für die Schaltflächen Plus und minus.
-   Formatieren Sie nach Möglichkeit die Bezeichnung und die Strukturelemente mithilfe von fettem Text. Andernfalls sollten Sie die Bezeichnung und die Elemente nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Wählen Sie in der Liste **Inhalt** die Option **Benutzeroberflächen Entwurf** aus.

Beim Verweisen auf Kontrollkästchen in einer Strukturansicht:

-   Verwenden Sie den genauen Bezeichnungs Text einschließlich der Groß-und Kleinschreibung, und schließen Sie das Kontrollkästchen Wörter ein Fügen Sie den Unterstrich "Zugriffsschlüssel" nicht ein.
-   Verwenden Sie zum Beschreiben der Benutzerinteraktion SELECT und Clear.
-   Formatieren Sie nach Möglichkeit die Bezeichnung mit fettem Text. Andernfalls sollten Sie die Bezeichnung nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Aktivieren Sie in der Liste zu sichernde **Elemente** das Kontrollkästchen **Eigene Dokumente** .

