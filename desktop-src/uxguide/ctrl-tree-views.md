---
title: Strukturansichten
description: Mit einer Strukturansicht können Benutzer eine hierarchisch angeordnete Auflistung von Objekten anzeigen und mit ihr interagieren, indem sie entweder eine einzelne Auswahl oder eine Mehrfachauswahl verwenden.
ms.assetid: f0206485-e028-41d8-9be2-5d59f0a0b677
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b0b5a456673338fec7240bb3b3a11047327239f70675786f26add1bbecdb7211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118217648"
---
# <a name="tree-views"></a>Strukturansichten

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Mit einer Strukturansicht können Benutzer eine hierarchisch angeordnete Auflistung von Objekten anzeigen und mit ihr interagieren, indem sie entweder eine einzelne Auswahl oder eine Mehrfachauswahl verwenden.

In einer Struktur werden Objekte, die Daten enthalten, als Blattknoten und Objekte, die andere Objekte enthalten, als Containerknoten bezeichnet. Ein einzelner oberster Containerknoten wird als Stammknoten bezeichnet. Benutzer können Containerknoten erweitern und reduzieren, indem sie auf die Schaltflächen plus und minus des Expanders klicken.

![Screenshot der Windows-Explorer-Strukturansicht ](images/ctrl-tree-views-image1.png)

Eine typische Strukturansicht.

> [!Note]  
> Richtlinien im Zusammenhang [mit Layout](vis-layout.md) [und Menüs](cmd-menus.md) werden in separaten Artikeln vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

**Hierarchische Daten bedeuten nicht, dass Sie eine Strukturansicht verwenden müssen.** Sehr oft ist [eine Listenansicht](ctrl-list-views.md) eine einfachere, aber leistungsfähigere Wahl. Listenansichten:

-   Unterstützen Sie mehrere verschiedene Ansichten.
-   Unterstützung für das Sortieren von Daten nach einer der Spalten in der Detailansicht.
-   Unterstützung der Organisation von Daten in Gruppen, die eine Hierarchie mit zwei Ebenen bilden.

**Um eine Listenansicht zu verwenden, können Sie hierarchische Informationen mithilfe der folgenden Techniken abflachen:**

-   Entfernen Sie den Stammknoten, falls vorhanden, da er häufig nicht erforderlich ist.
-   Verwenden Sie Listenansichtsgruppen, [](/windows/desktop/uxguide/ctrl-drop)Registerkarten, Dropdownlisten oder [erweiterbare](glossary.md) Überschriften, um die Container der obersten Ebene zu ersetzen.

    ![Screenshot von Listenansichtsgruppen mit Listen ](images/ctrl-tree-views-image2.png)

    In diesem Beispiel werden Listenansichtsgruppen für die Container der obersten Ebene verwendet.

    ![Screenshot der Registerkarten, die für Container der obersten Ebene verwendet werden ](images/ctrl-tree-views-image3.png)

    In diesem Beispiel werden Registerkarten für die Container der obersten Ebene verwendet.

    ![Screenshot der Dropdownliste, die als Container verwendet wird ](images/ctrl-tree-views-image4.png)

    In diesem Beispiel wird eine Dropdownliste für die Container der obersten Ebene verwendet.

-   Wenn ein zugeordnetes Steuerelement den Inhalt des ausgewählten Containers anzeigt, kann dieses Steuerelement niedrigere Ebenen der Hierarchie anzeigen.

    ![Screenshot des Inhaltsverzeichnisbereichs ](images/ctrl-tree-views-image5.png)

    In diesem Beispiel werden Container auf niedriger Ebene im Dokumentfenster angezeigt.

**Sie müssen eine Strukturansicht verwenden, wenn Sie eine Hierarchie mit mehr als zwei Ebenen (ohne den Stammknoten) anzeigen müssen.**

Berücksichtigen Sie die folgenden Fragen, um zu entscheiden, ob eine Strukturansicht das richtige Steuerelement ist:

-   **Sind die Daten hierarchisch?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement.
-   **Verfügt die Hierarchie über mindestens drei Ebenen (ohne den Stamm)?** Wenn dies nicht der Fall ist, sollten Sie Alternativen wie Listenansichtsgruppen, Registerkarten, Dropdownlisten oder erweiterbare Überschriften in Betracht ziehen.
-   **Verfügen die Elemente über zusätzliche Daten?** Falls ja, sollten Sie eine Listenansicht im Ansichtsmodus Details verwenden, um die zusätzlichen Daten vollständig zu nutzen.
-   **Beziehen sich die Daten auf niedrigerer Ebene auf unabhängige Subtasks?** Falls ja, sollten Sie die Informationen in einem zugeordneten Steuerelement oder in einem separaten Fenster (mithilfe von Befehlsschaltflächen [oder](ctrl-command-buttons.md) Links) [anzeigen.](ctrl-command-links.md)
-   **Sind die Zielbenutzer erweitert?** Fortgeschrittene Benutzer sind mit der Verwendung von Strukturen vertrauter. Wenn Ihre Anwendung auf erfahrene Benutzer ausgerichtet ist, vermeiden Sie die Verwendung von Strukturansichten.
-   **Verfügen die Elemente über eine einzelne, natürliche, hierarchische Kategorisierung, die den meisten Benutzern vertraut ist?** Wenn ja, sind die Daten ideal für eine Strukturansicht. Wenn mehrere Ansichten oder Sortierungen benötigt werden, verwenden Sie stattdessen eine Listenansicht.
-   **Müssen Benutzer die Daten auf niedrigerer Ebene in einigen, aber nicht in allen Szenarien oder in einigen, aber nicht in der ganzen Zeit sehen?** Wenn ja, sind die Daten ideal für eine Strukturansicht.

> [!Note]  
> Manchmal wird ein Steuerelement, das wie eine Strukturansicht aussieht, mithilfe einer Listenansicht implementiert. Wenden Sie in solchen Fällen die Richtlinien basierend auf der Verwendung und nicht auf der Implementierung an.

 

## <a name="design-concepts"></a>Entwurfskonzepte

Strukturen dienen dazu, Daten zu organisieren und leicht zu finden, aber es ist schwierig, Daten innerhalb einer Struktur leicht zu erkennen. Beachten Sie bei der Entscheidung über Strukturansichten und deren Organisation die folgenden Prinzipien.

### <a name="predictability-and-discoverability"></a>Vorhersagbarkeit und Aufholbarkeit

**Eine Strukturansicht basiert auf den Beziehungen zwischen Objekten.** Strukturen funktionieren am besten, wenn die Objekte eine klare, bekannte, sich gegenseitig ausschließende Beziehung bilden, in der jedes Objekt einem einzelnen, leicht zu bestimmenden Container zu ordnet.

**Ein erhebliches Problem ist, dass ein Objekt auf verschiedenen Knoten angezeigt werden kann.** Wo erwarten Benutzer beispielsweise, ein Hardwaregerät zu finden, das Musik abspielt, über eine große Festplatte verfügt und einen USB-Anschluss verwendet? Möglicherweise in einem von mehreren verschiedenen Containerknoten, z. B. Multimedia, Storage, USB und möglicherweise in Hardwareressourcen. Eine Lösung besteht im Platzieren jedes Objekts unter dem am besten geeigneten Container, unabhängig von den Umständen. Ein weiterer Ansatz besteht im Platzieren jedes Objekts unter allen containern, die angewendet werden. Erstere fördern eine einfache, saubere Hierarchie, und letztere fördert die Aufholbarkeit, die jeweils Vorteile und potenzielle Probleme hat.

**Benutzer verstehen das Layout der Struktur möglicherweise nicht vollständig, aber sie bilden ein mentales Modell der Beziehungen, nachdem sie eine Weile mit der Struktur interagiert haben.** Wenn dieses mentale Modell falsch ist, führt dies zu Verwirrung. Angenommen, ein Musikplayer ist in den Containern Multimedia, Storage und USB zu finden. Diese Anordnung verbessert die Aufholbarkeit. Wenn ein Benutzer das Gerät erstmals in Multimedia findet, kann der Benutzer daraus schließen, dass alle Geräte wie Musikplayer im Multimediacontainer angezeigt werden. Der Benutzer erwartet dann, dass ähnliche Geräte, z. B. Digitalkameras, im Multimediacontainer angezeigt werden, und wird verwirrend, wenn dies nicht der Fall ist.

**Die Herausforderung beim Entwerfen einer Struktur besteht darin, die Aufholbarkeit mit einem vorhersagbaren Benutzermodell zu ausgleichen, das Verwirrung minimiert.**

### <a name="breadth-vs-depth"></a>Breite im Vergleich zu Tiefe

Benutzerfreundlichkeitsstudien haben gezeigt, dass Benutzer bei der Suche nach Objekten in einer Struktur, die breit ist, erfolgreicher sind als **in** einer Struktur, die tief ist. Daher sollten Sie beim Entwerfen einer Struktur die Breite gegenüber der Tiefe bevorzugen. Im Idealfall sollte eine Struktur nicht mehr als vier Ebenen (ohne Zählung des Stammknotens) haben, und die objekte, auf die am häufigsten zugegriffen wird, sollten auf den ersten beiden Ebenen angezeigt werden.

### <a name="other-principles"></a>Andere Prinzipien

-   Wenn Benutzer das finden, was sie suchen, werden sie nicht mehr gesucht. Sie suchen nicht, wo sonst ein Objekt gefunden werden könnte, da sie dies nicht benötigen. Diese Benutzer können davon ausgehen, dass der erste Pfad, den sie finden, der einzige Pfad ist.
-   Benutzer haben Probleme, Objekte in großen, komplexen Strukturen zu finden. Benutzer führen keine vollständige, manuelle Suche durch, um Objekte in solchen Strukturen zu finden. Sie halten an, sobald sie der Meinung sind, dass sie einen angemessenen Aufwand unternommen haben. Daher müssen große, komplexe Strukturen durch andere Zugriffsmethoden wie die Wortsuche, einen Index oder die Filterung ergänzt werden.
-   Einige Programme ermöglichen Es Benutzern, eigene Strukturen zu erstellen. Solche selbst entworfenen Strukturen können zwar am mentalen Modell eines Benutzers ausgerichtet sein, sie werden jedoch häufig willkürlich erstellt und schlecht gepflegt. Während beispielsweise ein Dateisystem, ein E-Mail-Programm und eine Favoritenliste in der Regel ähnliche Arten von Informationen speichern, ist es für Benutzer selten so, dass sie auf die gleiche Weise organisiert werden.

**Wenn Sie nur eins tun...**

Abwägen Sie sorgfältig die Vor- und Nachteile der Verwendung von Strukturansichten. Hierarchisch angeordnete Daten bedeuten nicht, dass Sie eine Strukturansicht verwenden müssen.

## <a name="usage-patterns"></a>Verwendungsmuster

Strukturansichten haben mehrere Verwendungsmuster:



| Verwendung                           |    Beispiel                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Strukturansichten mit nur Containerknoten**<br/> Benutzer können einen Container nach dem anderen anzeigen und mit ihm interagieren. <br/>                        | In der Regel verfügen diese Strukturansichten über ein zugeordnetes Steuerelement, das den Inhalt des ausgewählten Containers anzeigt, sodass Benutzer immer nur mit einem Container gleichzeitig interagieren können. <br/> ![Screenshot des Containerbereichs und des Inhaltsbereichs ](images/ctrl-tree-views-image6.png)<br/> In diesem Beispiel verfügt die Strukturansicht nur über Containerknoten. Der Inhalt des ausgewählten Knotens wird im zugeordneten Listenansicht-Steuerelement angezeigt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Strukturansichten mit Container- und Blattknoten**<br/> Benutzer können Container und Blätter anzeigen und mit ihnen interagieren.<br/>                       | In der Regel verfügen diese Strukturansichten über ein zugeordnetes Steuerelement, das den Inhalt des ausgewählten Containers oder Blatts anzeigt. Wenn Benutzer mit Blättern interagieren können, ist es häufig erforderlich, die Mehrfachauswahl zu unterstützen. <br/> ![Screenshot des Strukturansichtsbereichs und des Inhaltsbereichs ](images/ctrl-tree-views-image7.png)<br/> In diesem Beispiel enthält die Strukturansicht sowohl Containerknoten als auch Blattknoten. Da die Mehrfachauswahl unterstützt wird, wird der Inhalt der geöffneten Elemente mithilfe von Registerkarten im [zugeordneten](ctrl-tabs.md) Steuerelement angezeigt.<br/> Alternativ kann die Strukturansicht über eine geordnete Liste verfügen, in der die Container Überschriften und die Blätter Optionen sind. <br/> ![Screenshot der Strukturansicht mit Überschriften und Optionen ](images/ctrl-tree-views-image8.png)<br/> In diesem Beispiel sind die Strukturblätter Optionen, und die Container sind Optionskategorien.<br/> |
| **Kontrollkästchenstrukturansichten**<br/> Benutzer können eine beliebige Anzahl von Elementen auswählen, einschließlich keiner.<br/>                                             | Die Kontrollkästchen geben deutlich an, dass eine Mehrfachauswahl möglich ist. Verwenden Sie dieses Strukturmuster, wenn die Mehrfachauswahl wichtig oder häufig verwendet wird. <br/> ![Screenshot der Strukturansicht mit Kontrollkästchen ](images/ctrl-tree-views-image9.png)<br/> In diesem Beispiel ermöglicht eine Kontrollkästchen-Strukturansicht die Auswahl von Features, die aktiviert oder deaktiviert werden können.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Strukturansichts-Generatoren**<br/> Benutzer können eine Struktur erstellen, indem sie jeweils einen Container oder ein Blatt hinzufügen und optional die Reihenfolge festlegen.<br/> | Viele Strukturen können von Benutzern erstellt oder geändert werden. Einige Strukturen werden direkt über Kontextmenüs und Drag & Drop (z. B. die Ordner im Windows-Explorer) erstellt, während andere Strukturen mithilfe eines spezialisierten Dialogfelds erstellt werden (z. B. die Favoritenliste in Windows Internet Explorer). <br/> ![Screenshot des Dialogfelds "Favoriten" ](images/ctrl-tree-views-image10.png)<br/> In diesem Beispiel aus Internet Explorer können Benutzer mithilfe eines Dialogfelds eine eigene Liste von Favoriten erstellen.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| **Strukturansichten mit alternativen Zugriffsmethoden**<br/> Benutzer können Objekte auf andere Weise als mithilfe einer hierarchischen Struktur suchen.<br/>        | Wie bereits erwähnt, haben Benutzer Probleme beim Suchen von Objekten in großen, komplexen Strukturen, sodass diese Strukturen durch andere Zugriffsmethoden wie eine Wortsuche, einen Index oder filtert ergänzt werden sollten. <br/> ![Screenshot der Registerkarten "Inhalt", "Index" und "Favoriten" ](images/ctrl-tree-views-image11.png)<br/> In diesem Beispiel können Benutzer auch über ein Inhaltsverzeichnis, einen Index und Favoriten auf Informationen zugreifen. Für einige Benutzer können die Index- und Suchregisterkarten nützlicher sein als die Registerkarte "Inhalt".<br/> ![Screenshot des Windows-Startmenüs und des Suchfelds ](images/ctrl-tree-views-image12.png)<br/> In diesem Beispiel ermöglicht die Windows Startmenü Benutzern auch den Zugriff auf Programme, Dateien und Webseiten, indem sie einen Teil des Namens in das Feld Suchen eingeben.<br/>                                                                                                             |



 

## <a name="guidelines"></a>Richtlinien

### <a name="presentation"></a>Präsentation

-   **Sortieren Sie die Elemente in einem Container in einer logischen Reihenfolge.** Sortieren Sie Namen in alphabetischer Reihenfolge, Zahlen in numerischer Reihenfolge und Datumsangaben in chronologischer Reihenfolge.
-   **Verwenden Sie das Always Show Selection-Attribut,** damit Benutzer das ausgewählte Element leicht bestimmen können, auch wenn das Steuerelement keinen Eingabefokus besitzt.
-   **Wenn die Struktur als Inhaltsverzeichnis fungiert, verwenden Sie das Attribut Single Expand, um die Verwaltung der Struktur zu vereinfachen.** Auf diese Weise wird nur der relevante Teil der Struktur erweitert.
-   **Vermeiden Sie die Darstellung leerer Strukturen.** Wenn ein Benutzer eine Struktur erstellt, initialisieren Sie die Struktur mit Anweisungen oder Beispielelementen, die Benutzer möglicherweise benötigen.

    ![Screenshot der Favoritenliste von Internet Explorer ](images/ctrl-tree-views-image13.png)

    In diesem Beispiel wird die Liste zunächst mit Beispielen dargestellt.

-   **Machen Sie die Containerknoten nicht reduzierbar, wenn Benutzer keinen Grund haben, sie zu reduzieren.** Dies erhöht unnötige Komplexität.
-   **Wenn die Ladeleistung ein Problem darstellt, zeigen Sie standardmäßig nur die Container der ersten und zweiten Ebene der Struktur an.** Sie können dann bei Bedarf zusätzliche Daten laden, wenn ein Benutzer Verzweigungen in der Struktur erweitert.
-   **Wenn Benutzer einen Container erweitern oder reduzieren, sorgen Sie dafür, dass dieser Zustand beibehalten wird, damit er bei der nächsten Anzeige der Strukturansicht wirksam wird,** es sei denn, Benutzer bevorzugen es, im Standardzustand zu beginnen. Persistenz sollte pro Strukturansicht und pro Benutzer erfolgen.
-   **Wenn Container auf hoher Ebene ähnliche Inhalte aufweisen, sollten Sie visuelle Hinweise verwenden, um sie zu unterscheiden.**

    **Falsch:**

    ![Screenshot von Outlook-Elementen mit unterschiedlichen Symbolen ](images/ctrl-tree-views-image14.png)

    In diesem Beispiel weisen die Ordner Postfach und Archiv ähnliche Inhalte auf. Sobald die Strukturen weiter erweitert wurden, ist es für Benutzer sehr schwierig zu wissen, wo sie sich in der Struktur befinden, was zu Verwirrung führt. Wenn Sie in den verschiedenen Abschnitten etwas andere Symbole verwenden, wird dieses Problem behoben.

-   **Neuwähnen von Verbindungslinien.** Obwohl diese Linien die Beziehungen zwischen Container- und Blattknoten deutlich zeigen, fügen sie visuelle Überladung hinzu, ohne das Verständnis erheblich zu verbessern. Insbesondere helfen sie nicht, wenn Knoten nah beieinander liegen, und sie helfen auch nicht, wenn die Knoten so weit voneinander entfernt sind, dass ein Bildlauf erforderlich ist.

    **Richtig:**

    ![Screenshot der Strukturansicht mit Verbindungslinien ](images/ctrl-tree-views-image15.png)

    **Besser:**

    ![Screenshot der Strukturansicht ohne Verbindungslinien ](images/ctrl-tree-views-image16.png)

    Die Verbindungslinien unterstützen das Verständnis nur wenig.

### <a name="interaction"></a>Interaktion

-   **Erwägen Sie die Bereitstellung eines Doppelklickverhaltens.** Doppelklicken sollte die gleiche Auswirkung wie das Auswählen eines Elements und das Ausführen des Standardbefehls haben.
-   **Redundantes Doppelklickverhalten.** Es sollte immer eine Befehlsschaltfläche oder ein Kontextmenübefehl mit der gleichen Auswirkung vorhanden sein.
-   Wenn ein Element eine weitere Erläuterung erfordert, **geben Sie die Erklärung in einem Infotip an.**

    ![Screenshot der Favoriten mit Infotip für ein Element ](images/ctrl-tree-views-image17.png)

    In diesem Beispiel enthält ein Infotip weitere Informationen.

-   **Geben Sie Kontextmenüs relevanter Befehle an.** Zu diesen Befehlen gehören Ausschneiden, Kopieren, Einfügen, Entfernen oder Löschen, Umbenennen und Eigenschaften.
-   **Deaktivieren Sie beim Deaktivieren einer Strukturansicht auch alle zugeordneten Bezeichnungen und Befehlsschaltflächen.**

### <a name="tree-organization"></a>Strukturorganisation

-   **Verwenden Sie eine natürliche hierarchische Struktur, die den meisten Benutzern vertraut ist.**
-   **Wenn Sie eine solche Struktur nicht verwenden können, versuchen Sie, die Auffindbarkeit mit einem vorhersagbaren Benutzermodell in Einklang zu bringen, das Verwechslungen minimiert.**
-   **Um die Auffindbarkeit sicher zu verbessern, platzieren Sie ein Element in mehreren Containern, wenn:**
    -   Das Element ist nicht mit anderen ähnlichen Elementen verknüpft (sodass Benutzer nicht durch falsche Zuordnungen verwechselt werden).
    -   Es gibt nur einige dieser redundant angeordneten Elemente (sodass die Struktur nicht aufgeblätt wird).
-   **Verwenden Sie die einfachste hierarchische Struktur, die gut funktioniert.** Gehen Sie folgendermaßen vor:
    -   Platzieren Sie die Objekte, auf die am häufigsten zugegriffen wird, in den ersten beiden Ebenen der Struktur (ohne Zählung des Stammknotens), und platzieren Sie objekte, auf die seltener zugegriffen wird, weiter unten in der Hierarchie.
    -   Vermeiden Sie unnötige Container oder kombinieren Sie redundante Container auf Zwischenebene.
-   **Breite über Tiefe bevorzugen.** Im Idealfall sollte eine Struktur nicht mehr als vier Ebenen aufweisen, und die am häufigsten verwendeten Objekte sollten in den ersten beiden Ebenen angezeigt werden.
-   **Ermitteln Sie, ob Sie wirklich einen Stammknoten benötigen.** Geben Sie einen Stammknoten an, wenn Benutzer Befehle für die gesamte Struktur ausführen müssen (möglicherweise über ein Kontextmenü auf dem Stammknoten). Andernfalls ist die Struktur einfacher und einfacher zu verwenden, ohne sie zu verwenden.
-   **Wenn die Struktur über alternative Zugriffsmethoden wie eine Wortsuche oder einen Index verfügt, optimieren Sie die Struktur für das Durchsuchen, indem Sie sich auf die nützlichsten Inhalte konzentrieren.** Bei alternativen Zugriffsmethoden muss der Inhalt der Struktur nicht umfassend sein. Die Vereinfachung der Struktur erleichtert Benutzern die Suche nach den nützlichsten Inhalten.

### <a name="check-box-tree-views"></a>Kontrollkästchenstrukturansichten

-   **Zeigt die Anzahl der ausgewählten Elemente unterhalb der Liste** an, insbesondere, wenn Benutzer wahrscheinlich mehrere Elemente auswählen. Dieses Feedback hilft Benutzern zu bestätigen, dass ihre Auswahl richtig ist.

    ![Screenshot der Anzahl ausgewählter Elemente ](images/ctrl-tree-views-image18.png)

    In diesem Beispiel wird die Anzahl der ausgewählten Elemente unterhalb der Struktur angezeigt. Es ist klar, dass zwei Elemente nicht ausgewählt sind.

-   Wenn potenziell viele Elemente vorhanden sind und alle Elemente ausgewählt oder gelöscht werden, fügen Sie die Befehlsschaltflächen Alle auswählen und Alle löschen hinzu.
-   **Verwenden Sie Kontrollkästchen mit gemischten Zuständen, um eine Teilauswahl der Elemente in einem Container anzugeben.**

    **Richtig:**

    ![Screenshot des Fensters mit Kontrollkästchen für gemischten Zustand ](images/ctrl-tree-views-image19.png)

    In diesem Beispiel werden die Kontrollkästchen für gemischten Zustand verwendet, um eine Teilauswahl anzugeben.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größen- und Abstände

![Screenshot der Größe und des Abstands der Strukturansicht ](images/ctrl-tree-views-image20.png)

Empfohlene Größen- und Abstandseinstellungen für Strukturansichtssteuerelemente.

-   Wählen Sie eine Breite der **Strukturansicht aus, die das horizontale Scrollen** für die meisten Elemente vermeidet, wenn die Struktur vollständig erweitert ist.
-   **Schließen Sie zusätzliche 30 Prozent ein, um die Lokalisierung zu bieten.**
-   **Wählen Sie eine Strukturansichtshöhe aus, die unnötiges vertikales Scrollen verhindert.** Erwägen Sie, eine Strukturansicht etwas länger zu machen (oder sogar noch mehr, wenn Platz verfügbar ist), wenn dies die Notwendigkeit einer vertikalen Scrollleiste reduziert.

    **Falsch:**

    ![Screenshot des kurzen Steuerelements für die schmale Strukturansicht ](images/ctrl-tree-views-image21.png)

    In diesem Beispiel würden die Bildlaufleisten in den meisten Fällen entfernt, wenn die Strukturansicht etwas breiter und länger wäre. In dieser bestimmten Struktur kann nur ein Container gleichzeitig geöffnet werden.

-   **Wenn Benutzer davon profitieren, die Strukturansicht zu vergrößern, können Sie die Größe der Strukturansicht und des übergeordneten Fensters ändern.** Auf diese Weise können Benutzer die Strukturansichtsgröße nach Bedarf anpassen.

## <a name="labels"></a>Bezeichnungen

### <a name="control-labels"></a>Steuerelementbezeichnungen

-   Alle Strukturansichten benötigen Bezeichnungen. Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz, der mit einem Doppelpunkt endet und [statischen Text verwendet.](glossary.md)
-   Weisen Sie einen eindeutigen Zugriffsschlüssel zu. Zuweisungsrichtlinien finden Sie unter [Tastatur](inter-keyboard.md).
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Positionieren Sie die Bezeichnung über dem Steuerelement, und richten Sie die Bezeichnung am linken Rand des Steuerelements aus.
-   Schreiben Sie für Mehrfachauswahl-Strukturansichten die Bezeichnung, damit klar ist, dass mehrere Auswahlen möglich sind. Bezeichnungen der Kontrollkästchenstrukturansicht können weniger explizit sein.

    **Falsch:**

    ![Screenshot der Strukturansicht mit Komponentenbezeichnung ](images/ctrl-tree-views-image22.png)

    In diesem Beispiel stellt die Bezeichnung keine Informationen zur Mehrfachauswahl zur Verfügung.

    **Besser:**

    ![Screenshot der Strukturansicht mit der Bezeichnung "eine oder mehrere" ](images/ctrl-tree-views-image23.png)

    In diesem Beispiel gibt die Bezeichnung eindeutig an, dass eine Mehrfachauswahl möglich ist.

    **Beste:**

    ![Screenshot der Strukturansicht mit Kontrollkästchen ](images/ctrl-tree-views-image24.png)

    In diesem Beispiel weisen die Kontrollkästchen eindeutig darauf hin, dass eine Mehrfachauswahl möglich ist, sodass die Bezeichnung nicht explizit sein muss.

### <a name="data-text"></a>Datentext

-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.

### <a name="instructional-text"></a>Anweisungstext

-   Wenn Sie Anweisungstext zu einer Strukturansicht hinzufügen müssen, fügen Sie ihn über der Bezeichnung hinzu. Verwenden Sie vollständige Sätze mit endender Interpunktion.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Ergänzende Erläuterungen, die hilfreich, aber nicht notwendig sind, sollten kurz gehalten werden. Platzieren Sie diese Informationen entweder in Klammern zwischen der Bezeichnung und dem Doppelpunkt, nach der Main-Anweisung, wenn sie anstelle einer Bezeichnung verwendet wird, oder unterhalb des Steuerelements.

    ![Screenshot der Erklärung unterhalb der Strukturansicht ](images/ctrl-tree-views-image8.png)

    In diesem Beispiel befindet sich die ergänzende Erklärung unterhalb des Steuerelements.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Strukturansichten:

-   Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Unterstriche, aber schließen Sie nicht den Unterstrich oder Doppelpunkt des Zugriffsschlüssels ein. Schließen Sie die Wortliste oder hierarchische Liste ein, wenn der Kontext eine Unterscheidung von regulären Listen erfordert.
-   Verwenden Sie für Strukturelemente den genauen Elementtext, einschließlich der Groß-/Groß-/Groß-/Unterform.
-   Strukturansichten werden nur in der Programmierung und in anderen technischen Dokumentationen als Strukturansichten bezeichnet. Verwenden Sie überall sonst Listen oder hierarchische Listen, da die Begriffsstruktur für die meisten Benutzer verwirrend ist.
-   Um die Benutzerinteraktion zu beschreiben, verwenden Sie select für die Daten, und erweitern und reduzieren Sie für die Plus- und Minusschaltflächen.
-   Formatieren Sie die Bezeichnung und die Strukturelemente nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung und die Elemente nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Wählen Sie in **der Liste** Inhalt Benutzeroberfläche **Design aus.**

Beim Verweisen auf Kontrollkästchen in einer Strukturansicht:

-   Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Unterschrift, und schließen Sie das Kontrollkästchen Wörter ein. Schließen Sie den Unterstrich der Zugriffsschlüssel nicht ein.
-   Verwenden Sie select und clear, um die Benutzerinteraktion zu beschreiben.
-   Formatieren Sie die Bezeichnung nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Aktivieren Sie in **der Liste Zu sichernde** Elemente das **Eigene Dokumente** Kontrollkästchen.

