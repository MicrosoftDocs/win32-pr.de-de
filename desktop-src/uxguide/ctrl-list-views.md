---
title: Auflisten von Ansichten
description: Mit einer Listenansicht können Benutzer eine Auflistung von Datenobjekten anzeigen und mit einer Auflistung von Datenobjekten interagieren. verwenden Sie dazu entweder eine einzelne Auswahl oder eine Mehrfachauswahl.
ms.assetid: 62a7bfc8-96a9-450d-9db9-ec9dab6687b7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c3c823b23c03f29ac6b80e10df79eac36653f2e4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103761283"
---
# <a name="list-views"></a>Auflisten von Ansichten

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Mit einer Listenansicht können Benutzer eine Auflistung von Datenobjekten anzeigen und mit einer Auflistung von Datenobjekten interagieren. verwenden Sie dazu entweder eine einzelne Auswahl oder eine Mehrfachauswahl.

![Screenshot der Listenansicht mit Spaltenüberschriften ](images/ctrl-list-views-image1.png)

Eine typische Listenansicht.

Listenansichten verfügen über mehr Flexibilität und Funktionalität als Listenfelder. Anders als bei Listenfeldern unterstützen Sie das Ändern von Sichten, das Gruppieren, mehrere Spalten mit Überschriften, das Sortieren nach Spalten, das Ändern der Spaltenbreite und-Reihenfolge, die Verwendung einer Zieh Quelle oder eines Ablage Ziels und das Kopieren von Daten in die Zwischenablage.

> [!Note]  
> Richtlinien im Zusammenhang mit [Layout](vis-layout.md) und [Listenfeldern](ctrl-list-boxes.md) werden in separaten Artikeln dargestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Eine Listenansicht ist mehr als nur ein flexibleres und funktionales Listenfeld: die zusätzliche Funktionalität führt zu einer anderen Verwendung. Die folgende Tabelle zeigt den Vergleich.



|                             |                                           |                                                                                                                                               |
|-----------------------------|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
|                             | **Listenfelder**<br/>                 | **Listenansichten**<br/>                                                                                                                     |
| **Datentyp**<br/>    | Sowohl Daten-als auch Programmoptionen.<br/> | Nur Daten.<br/>                                                                                                                         |
| **Contents**<br/>     | Nur Bezeichnungen.<br/>                   | Bezeichnungen und zusätzliche Daten, möglicherweise in mehreren Spalten.<br/>                                                                           |
| **Interaktion**<br/>  | Wird zum Treffen der Auswahl verwendet.<br/>    | Kann verwendet werden, um eine Auswahl zu treffen, wird aber häufig zum Anzeigen und interagieren mit Daten verwendet. Kann eine Zieh Quelle oder ein Ablage Ziel sein.<br/> |
| **Präsentation**<br/> | Festen.<br/>                         | Benutzer können Ansichten ändern, gruppieren, nach Spalten sortieren und Spaltenbreite und-Reihenfolge ändern.<br/>                                                |



 

Um zu entscheiden, ob dies die richtige Kontrolle ist, sollten Sie die folgenden Fragen beachten:

-   **Stellt die Liste Daten anstelle der Programmoptionen dar?** Falls nicht, sollten Sie stattdessen ein Listenfeld verwenden.
-   **Müssen Benutzer Sichten ändern, gruppieren, nach Spalten sortieren oder Spaltenbreite und-Reihenfolge ändern?** Wenn dies nicht der Folge ist, verwenden Sie stattdessen ein Listenfeld.
-   **Muss das Steuerelement eine Zieh Quelle oder ein Ablage Ziel sein?** Wenn dies der Fall ist, verwenden Sie eine Listenansicht.
-   **Müssen die Listenelemente in die Zwischenablage kopiert oder aus der Zwischenablage eingefügt werden?** Wenn dies der Fall ist, verwenden Sie eine Listenansicht.

### <a name="check-box-list-views"></a>Kontrollkästchen Listenansichten

-   **Wird das Steuerelement verwendet, um 0 (null) oder mehr Elemente aus einer Liste von Daten auszuwählen?** Wenn Sie ein Element auswählen möchten, verwenden Sie stattdessen die einfache Auswahl.
-   **Ist die Mehrfachauswahl für den Task oder häufig verwendet?** Wenn dies der Fall ist, verwenden Sie eine Kontrollkästchen-Listenansicht, um die Mehrfachauswahl zu verdeutlichen, insbesondere, wenn die Ziel Benutzer nicht erweitert sind. Wenn dies nicht der Fall ist, verwenden Sie eine Standard Listenansicht für Mehrfachauswahl, wenn die Kontrollkästchen zu viel Aufmerksamkeit auf die Mehrfachauswahl ziehen oder zu einer zu großen Bildschirm Übersichtlichkeit führen würden.
-   **Ist die Stabilität der Mehrfachauswahl wichtig?** Wenn dies der Fall ist, verwenden Sie eine Liste der [Kontrollkästchen](ctrl-list-boxes.md), Listen Generator oder Liste hinzufügen/entfernen, da Sie nur auf nur ein einzelnes Element klicken. Mit einer standardmäßigen Mehrfachauswahl Liste ist es sehr einfach, alle Auswahlmöglichkeiten zu löschen.

> [!Note]  
> Manchmal wird ein Steuerelement, das wie eine Listenansicht aussieht, mithilfe eines Listen Felds implementiert und umgekehrt. Wenden Sie in solchen Fällen die Richtlinien auf Grundlage der Verwendung, nicht auf die Implementierung an.

 

## <a name="usage-patterns"></a>Verwendungsmuster

Alle Sichten unterstützen eine einfache Auswahl, bei der Benutzer jeweils nur ein Element auswählen können, und mehrere Auswahlmöglichkeiten, mit denen Benutzer beliebig viele Elemente auswählen können, einschließlich keine. Listen Sichten unterstützen den [Modus für erweiterte Auswahl](glossary.md), bei dem die Auswahl durchziehen oder mit UMSCHALT + Klicken oder STRG + Klicken erweitert werden kann, um Gruppen von zusammenhängenden bzw. nicht angrenzenden Werten auszuwählen. Anders als bei Listenfeldern wird der [Mehrfachauswahl Modus](glossary.md)nicht unterstützt, bei dem durch Klicken auf ein beliebiges Element der Auswahl Zustand unabhängig von der Umschalttaste und der STRG-Taste gewechselt wird.

### <a name="standard-list-view"></a>Standard Listenansicht

Das Listenansicht-Steuerelement unterstützt fünf Standardansichten:



|                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kachel**<br/> jedes Element wird als mittleres Symbol mit einer Bezeichnung und optionalen Details auf der rechten Seite angezeigt. <br/>                                                                                                                         | ![Screenshot von Miniaturansichten mit Titeln und Details ](images/ctrl-list-views-image2.png)<br/> Die Kachel Ansicht zeigt mittelgroße Symbole mit Bezeichnungen und optionalen Details auf der rechten Seite an.<br/>                                                                                                                                                                |
| **Großes Symbol**<br/> jedes Element wird als extra großes, großes oder mittleres Symbol mit einer darunter liegenden Bezeichnung angezeigt.<br/>                                                                                                                      | ![Screenshot der Listenansicht für große Miniaturansichten ](images/ctrl-list-views-image3.png)<br/> Die Ansicht "große Symbole" zeigt jedes Element als großes Symbol mit einer darunter liegenden Bezeichnung an.<br/>                                                                                                                                                                              |
| **Kleines Symbol**<br/> jedes Element wird als kleines Symbol mit einer Bezeichnung auf der rechten Seite angezeigt.<br/>                                                                                                                                           | ![Screenshot der Ansicht mit kleinen Miniaturansichten ](images/ctrl-list-views-image4.png)<br/> In der kleinen Symbol Ansicht werden alle Elemente als kleines Symbol mit der Bezeichnung auf der rechten Seite angezeigt.<br/>                                                                                                                                                                        |
| **Liste**<br/> jedes Element wird als kleines Symbol mit einer Bezeichnung auf der rechten Seite angezeigt.<br/>                                                                                                                                                 | im Listenmodus ordnet diese Ansicht Elemente in Spalten an und verwendet eine horizontale Scrollleiste. im Gegensatz dazu werden in der Symbol Ansichtsmodi Elemente in Zeilen sortiert und eine vertikale Scrollleiste verwendet. <br/> ![Screenshot der Listenansicht im Listenmodus ](images/ctrl-list-views-image5.png)<br/> Der Listenmodus zeigt jedes Element als kleines Symbol mit seiner Bezeichnung auf der rechten Seite an.<br/> |
| **Details**<br/> jedes Element wird als Zeile in einem Tabellenformat angezeigt. die Spalte ganz links enthält das optionale Symbol und die Bezeichnung des Elements, und die nachfolgenden Spalten enthalten zusätzliche Informationen, wie z. b. Element Eigenschaften.<br/> | Außerdem können Spalten hinzugefügt oder entfernt und neu angeordnet und die Größe der Größe geändert werden. Zeilen können nach Spalten gruppiert werden. <br/> ![Screenshot der Listenansicht im Detail Modus ](images/ctrl-list-views-image6.png)<br/> In der Detailansicht werden alle Elemente als Zeile in einem Tabellenformat angezeigt.<br/>                                                              |



 

### <a name="list-view-variations"></a>Listen Ansichts Variationen



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Spaltenauswahl</strong><br/> Listenansichten verfügen manchmal über so viele Spalten, dass es nicht praktikabel ist, Sie alle anzuzeigen. In diesem Fall besteht der beste Ansatz darin, die nützlichsten Spalten standardmäßig anzuzeigen und Benutzern das Hinzufügen oder Entfernen von Spalten nach Bedarf zu ermöglichen. <br/></td>
<td><img src="images/ctrl-list-views-image7.png" alt="Screen shot of list view with Column Chooser menu " /><br/> Wenn Sie mit der rechten Maustaste auf die Spaltenüberschrift klicken, wird ein Kontextmenü angezeigt, in dem Benutzer Spalten hinzufügen oder entfernen<br/> <img src="images/ctrl-list-views-image8.png" alt="Screen shot of Choose Details dialog box " /><br/> Wenn Sie im Kontextmenü der Spaltenüberschrift auf weitere klicken, wird das Dialogfeld Spalten auswählen angezeigt, in dem Benutzer Spalten hinzufügen oder entfernen sowie diese neu anordnen können.<br/></td>
</tr>
<tr class="even">
<td><strong>Kontrollkästchen-Listenansicht</strong><br/> Ermöglicht Benutzern die Auswahl mehrerer Elemente.<br/></td>
<td>Listenansichten mit Mehrfachauswahl haben genau dasselbe Aussehen wie Listenansichten mit einfacher Auswahl. es gibt also keinen visuellen Hinweis darauf, dass Sie mehrere Auswahl unterstützen. Eine Kontrollkästchen-Listenansicht kann verwendet werden, um eindeutig anzugeben, dass mehrere Auswahlmöglichkeiten möglich sind. Folglich sollte dieses Muster für Aufgaben verwendet werden, bei denen die Mehrfachauswahl wesentlich oder häufig verwendet wird.<br/> <img src="images/ctrl-list-views-image9.png" alt="Screen shot of dialog box with several check boxes " /><br/> In diesem Beispiel verwendet eine kleine Symbol Ansicht Kontrollkästchen, da für die Aufgabe die Mehrfachauswahl erforderlich ist.<br/></td>
</tr>
<tr class="odd">
<td><strong>Auflisten von Ansichten mit Gruppen</strong><br/> Ordnen Sie die Daten in Gruppen an.<br/></td>
<td>Obwohl in den Detailansichten häufig das Sortieren der Daten nach einer beliebigen Spalte unterstützt wird, können Benutzer mithilfe von Listenansichten die Elemente in Gruppen organisieren. Die Gruppierung hat folgende Vorteile:<br/>
<ul>
<li>Gruppen funktionieren in allen Ansichten (mit Ausnahme von List), sodass Benutzer z. b. eine extra große Symbol Ansicht der Alben nach Künstlern gruppieren können.</li>
<li>Gruppen können Auflistungen auf hoher Ebene sein, die häufig aussagekräftiger sind als das Gruppieren direkt aus den Daten. Windows-Explorer gruppiert z. b. Datumsangaben in heute, gestern, letzte Woche, früher dieses Jahr und vor langer Zeit.</li>
</ul>
<img src="images/ctrl-list-views-image10.png" alt="Screen shot of list view with several data groups " /><br/> In diesem Beispiel zeigt das Windows-Willkommens Center gruppierte Elemente in einer Listenansicht an.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Richtlinien

### <a name="presentation"></a>Präsentation

-   **Sortieren Sie Listenelemente in einer logischen Reihenfolge.** Sortieren von Namen in alphabetischer Reihenfolge, Zahlen in numerischer Reihenfolge und Datumsangaben in chronologischer Reihenfolge.
-   **Gestatten Sie ggf. Benutzern das Ändern der Sortierreihenfolge.** Die Benutzer Sortierung ist wichtig, wenn die Liste viele Elemente enthält oder wenn es Szenarien gibt, in denen Elemente effektiver in einer anderen Sortierreihenfolge als der Standard gefunden werden.
-   **Verwenden Sie das Attribut "Auswahl immer anzeigen** ", damit Benutzer das ausgewählte Element problemlos ermitteln können, auch wenn das Steuerelement nicht den Fokus besitzt.
-   **Vermeiden Sie die Darstellung leerer Listenansichten.** Wenn Benutzer eine Liste erstellen, initialisieren Sie die Liste mit Anweisungen oder Beispiel Elementen, die Benutzer möglicherweise benötigen.

    ![Screenshot des Such Dialogfelds mit Anweisungen ](images/ctrl-list-views-image11.png)

    In diesem Beispiel enthält die Suchlisten Ansicht anfänglich Anweisungen.

-   **Wenn Benutzer Sichten ändern, gruppieren, nach Spalten sortieren oder Spalten sowie deren Breite und Reihenfolge ändern können, nehmen Sie diese Einstellungen dauerhaft an, sodass Sie wirksam werden, wenn die Listenansicht das nächste Mal angezeigt wird.** Sorgen Sie dafür, dass Sie dauerhaft in einer Listenansicht gespeichert werden.

### <a name="interaction"></a>Interaktion

-   **Wählen Sie mit nur einem Klick das Listenelement aus, auf das der Benutzer zeigt. Ausnahme:** für das Befehls Verknüpfungs Listen Muster wählt das einmalige klicken das Element aus und schließt das Fenster oder navigiert zur nächsten Seite.
-   **Sie sollten das doppelte Klickverhalten bereitstellen.** Das Doppelklicken muss dieselbe Wirkung wie das Auswählen eines Elements und das Ausführen seines Standard Befehls haben.
-   **Doppelklick Verhalten redundant.** Es sollte immer eine Befehls Schaltfläche oder ein Kontextmenü Befehl vorhanden sein, der dieselbe Auswirkung hat.
-   Wenn ein Listenelement weitere Erläuterungen erfordert, **Stellen Sie die Erläuterung in einem** [Infotipp](ctrl-tooltips-and-infotips.md)bereit. Verwenden Sie vollständige Sätze und endinterpunktions Zeichen.

    ![Screenshot der Listenansicht mit Tastatur Infotipp ](images/ctrl-list-views-image12.png)

    In diesem Beispiel wird ein Infotipp verwendet, um weitere Informationen bereitzustellen.

-   **Stellen Sie Kontextmenüs relevanter Befehle bereit.** Zu diesen Befehlen zählen Ausschneiden, kopieren, einfügen, entfernen oder löschen, umbenennen und Eigenschaften.
-   **Wenn Benutzer die Sortierreihenfolge und die Gruppierung ändern können, geben Sie die Kontextmenüs Sortieren nach und Gruppieren nach an.** Beim ersten Klicken auf einen Spaltennamen wird die Liste in aufsteigender Reihenfolge für die Spalte sortiert oder gruppiert, der zweite Klick sortiert oder Gruppen in absteigender Reihenfolge. Verwenden Sie die vorherige Reihenfolge (aus einer anderen Spalte) als sekundären Schlüssel.

    ![Screenshot der Listenansicht mit "Sortieren nach"-Menü ](images/ctrl-list-views-image13.png)

    In diesem Beispiel ändert das Kontextmenü Sortieren nach die Sortierreihenfolge. Wenn Sie auf Name klicken, wird nach Name in aufsteigender Reihenfolge sortiert Wenn Sie erneut auf Name klicken, werden die Namen in absteigender Reihenfolge

-   **Ermöglichen Sie den Zugriff auf die Spalten Kopfzeile der Listenansicht über die Tastatur.**
    -   **Entwickler:** Dies können Sie erreichen, indem Sie den Fokus auf das Spaltenheader-Steuerelement festlegen. Diese Funktion ist neu in Windows Vista.
-   **Deaktivieren Sie bei der Deaktivierung einer Listenansicht auch alle zugeordneten Bezeichnungen und Befehls Schaltflächen.**
-   **Vermeiden Sie horizontales Scrollen.** Der Listenmodus verwendet horizontales Scrollen. Dieser Modus ist in der Regel die kompakteste, aber ein horizontaler Bildlauf ist im allgemeinen schwieriger zu verwenden als vertikaler Bildlauf. Verwenden Sie stattdessen die kleine Symbol Ansicht, wenn die Kompaktheit nicht wichtig ist. Der Listenmodus ist jedoch eine gute Wahl, wenn viele alphabetisch sortierte Elemente vorhanden sind und ausreichend Bildschirmfläche für ein breites Steuerelement verfügbar ist.

    **Annehmbar:**

    ![Screenshot eines breiten Listenmodus-Steuer Elements ](images/ctrl-list-views-image14.png)

    In diesem Beispiel wird der Listenmodus verwendet, da viele Elemente vorhanden sind und für ein breites Steuerelement ausreichend Speicherplatz verfügbar ist.

### <a name="multiple-selection-lists"></a>Mehrfachauswahl Listen

-   Es empfiehlt sich, **die Anzahl der ausgewählten Elemente unterhalb der Liste anzuzeigen**. Dies gilt insbesondere, wenn Benutzer wahrscheinlich mehrere Elemente auswählen. Diese Informationen bieten nicht nur nützliches Feedback, sondern auch deutlich, dass die Listenansicht Mehrfachauswahl unterstützt.

    ![Screenshot der Liste mit fünf ausgewählten Miniaturansichten ](images/ctrl-list-views-image15.png)

    In diesem Beispiel wird die Anzahl der ausgewählten Elemente unterhalb der Liste angezeigt.

-   Alternativ können Sie anstelle der Anzahl ausgewählter Elemente auch andere Auswahl Metriken bereitstellen, die aussagekräftiger sein können, z. b. die für die Auswahl erforderlichen Ressourcen.

    ![Screenshot des Dialog Felds mit Speicherplatz ](images/ctrl-list-views-image16.png)

    In diesem Beispiel ist der Speicherplatz, der zum Installieren der Komponenten erforderlich ist, aussagekräftiger, als die Anzahl der ausgewählten Komponenten.

-   Wenn möglicherweise viele Elemente vorhanden sind und alle Elemente ausgewählt oder gelöscht werden, fügen Sie für Kontrollkästchen Listenansichten die Option Alle auswählen und alle Befehls Schaltflächen löschen.
-   **Verwenden Sie Kontrollkästchen mit gemischtem Zustand, um die partielle Auswahl der Elemente in einem Container anzugeben.** Der gemischte Zustand wird nicht als dritter Zustand eines einzelnen Elements verwendet.

### <a name="changing-views"></a>Ändern von Ansichten

Wenn Benutzer Ansichten ändern können:

-   **Wählen Sie standardmäßig die am einfachsten geeignete Ansicht aus.** Alle Änderungen, die Benutzer vornehmen, sollten dauerhaft in einer pro-Listen-Ansicht vorgenommen werden.
-   **Ändern Sie die Ansicht mithilfe einer unterteilten Schaltfläche, Menü Schaltfläche oder Dropdown Liste.** Verwenden Sie nach Möglichkeit eine [Trenn Schaltfläche](ctrl-command-buttons.md) auf der Symbolleiste, und ändern Sie die Bezeichnung der Schaltfläche, um die aktuelle Ansicht anzuzeigen.

    ![Screenshot der Liste mit der geteilten Schaltfläche "Views" ](images/ctrl-list-views-image17.png)

    In diesem Beispiel wird eine unterteilte Schaltfläche auf der Symbolleiste verwendet, um Ansichten zu ändern.

-   **Geben Sie ein Kontextmenü für die Ansicht an.**

    ![Screenshot der Liste mit dem Kontextmenü "Ansicht" ](images/ctrl-list-views-image18.png)

In diesem Beispiel wird ein Kontextmenü Ansicht verwendet, um Ansichten zu ändern.

### <a name="details-views"></a>Detailansichten

-   **Verwenden Sie die Kachel Ansicht, um die Lesbarkeit zu verbessern.**

    **Annehmbar:**

    ![Screenshot der Detail Liste mit schmalen Spalten ](images/ctrl-list-views-image19.png)

    In diesem Beispiel sind zu viele Daten vorhanden, und das Fenster, die Liste und die Spalten sind zu klein, sodass die Listenelemente schwer lesbar sind.

    **Besserer**

    ![Screenshot der Detail Liste mit Daten in Gruppen ](images/ctrl-list-views-image20.png)

    In diesem Beispiel zeigt die Kachel Ansicht die Daten ohne Abschneiden an.

-   **Wählen Sie Standard Spaltenbreite aus, die für die längsten Daten geeignet ist.** Listenansichten kürzen lange Daten automatisch mit Ellipsen, sodass die Spaltenbreite geeignet ist, wenn standardmäßig nur wenige Ellipsen angezeigt werden. Benutzer können die Größe von Spalten ändern, bevorzugen jedoch andere Lösungen:

    -   Größe jeder Spaltenbreite an die entsprechenden Daten anpassen.
    -   Größe der Steuerelement Breite an die entsprechenden Spalten und alle möglichen Scrollleisten anpassen.
    -   Verwenden Sie bei Bedarf den horizontalen Bildlauf.
    -   Kürzen von Daten nur für Elemente mit ungeraden Elementen oder als letztes Mittel.

    Wenn Daten in normaler Größe standardmäßig abgeschnitten werden müssen, können Sie die Größe der Fenster-und Listenansicht ändern. Fügen Sie zusätzliche 30 Prozent (bis zu 200 Prozent für kürzerer Text) für Text (aber nicht zahlen) ein, der lokalisiert wird.

    **Falsch:**

    ![Screenshot der Listen Spalten mit abgeschnittene Daten ](images/ctrl-list-views-image21.png)

    In diesem Beispiel werden die meisten Daten abgeschnitten. Die vielen Ellipsen weisen eindeutig darauf hin, dass die Steuerelement-und Spaltenbreite für die Daten zu klein ist.

    **Falsch:**

    ![Screenshot einer einspaltigen Liste mit abgeschnittene Daten ](images/ctrl-list-views-image22.png)

    In diesem Beispiel werden Daten ohne Grund abgeschnitten.

-   **Wählen Sie eine geeignete Standard Spaltenreihenfolge aus.** Ordnen Sie die Spalten im Allgemeinen wie folgt an:

    -   Zuerst der Elementname oder die identifizierenden Daten.
    -   Als nächstes sind andere Daten nützlich, um die Listenelemente zu unterscheiden.
    -   Als nächstes sind die nützlichsten (vorzugsweise kurze oder mit fester Länge) Daten.
    -   Als nächstes weniger nützlich (kurze oder mit fester Länge bevorzugte Daten).
    -   Die letzten, langen Daten mit variabler Länge.

    Long, Variable Length-Data wird in den letzten Spalten platziert, um den Bedarf an horizontaler Bildlauf zu verringern. Platzieren Sie in diesen Kategorien Verwandte Informationen in einer logischen Sequenz.

-   **Gestatten Sie den Benutzern ggf. das Hinzufügen und Entfernen von Spalten, und ändern Sie die Reihenfolge.** Zeigen Sie die nützlichsten Spalten standardmäßig an. Dies wird mit dem Drag Drop-Attribut des Headers erreicht.
-   Wählen Sie eine für die Daten geeignete Ausrichtung aus. Verwenden Sie die folgenden Regeln:
    -   Rechtsbündig ausrichten von Zahlen, Währungen und Uhrzeiten.
    -   Linksbündig ausrichten von Text, IDs (auch wenn numerisch) und Datumsangaben.
-   Bei sortierbaren Spaltenüberschriften **sortiert der erste Klick auf eine Überschrift die Liste in aufsteigender Reihenfolge nach der Spalte. der zweite Klick wird in absteigender Reihenfolge sortiert.** Verwenden Sie die vorherige Sortierreihenfolge (aus einer anderen Spalte) als sekundären Sortierschlüssel.

    ![Screenshot der Detail Liste mit sortierten Daten ](images/ctrl-list-views-image23.png)

    In diesem Beispiel wurde zuerst auf die Spalte Name und dann auf die Spalte Typ geklickt. Daher ist der Typ in aufsteigender Reihenfolge der primäre Sortierschlüssel, und der Name in aufsteigender Reihenfolge ist der sekundäre.

-   **Verwenden Sie das Attribut "Select" der vollständigen Zeile** , damit Benutzer die ausgewählten Elemente in allen Spalten leicht bestimmen können.
-   **Verwenden Sie keine sortierbare Spaltenüberschrift, es sei denn, die Daten können sortiert werden.**
-   **Verwenden Sie keine Spaltenüberschrift, wenn nur eine Spalte vorhanden ist und die Sortierung nicht rückgängig gemacht werden muss.** Verwenden Sie stattdessen eine Bezeichnung, um die Daten zu identifizieren.

    **Falsch:**

    ![Screenshot der Liste mit der Bezeichnung in der Spalten Kopfzeile ](images/ctrl-list-views-image24.png)

    **Richtig:**

    ![Screenshot der Liste mit der Bezeichnung über dem Steuerelement ](images/ctrl-list-views-image25.png)

    Im richtigen Beispiel wird anstelle eines Spalten Headers eine Bezeichnung verwendet.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstände

![Screenshot der Listengröße und des Abstands ](images/ctrl-list-views-image26.png)

Empfohlene Größe und Abstände für Listenansichten.

-   **Wählen Sie eine Listen Ansichts Höhe aus, die eine ganzzahlige Anzahl von Elementen anzeigt.** Vermeiden Sie das vertikale Abschneiden von Elementen.
-   **Wählen Sie eine Listen Ansichts Größe aus, die unnötigen vertikalen und horizontalen Bildlauf in allen unterstützten Sichten eliminiert.** Listenansichten sollten zwischen 3 und 20 Elementen angezeigt werden. Es empfiehlt sich, eine Listenansicht etwas größer zu machen, wenn eine Schiebe Leiste entfernt wird. Listen mit potenziell vielen Elementen sollten mindestens fünf Elemente anzeigen, um den Bildlauf zu vereinfachen, indem mehr Elemente gleichzeitig angezeigt werden und die Bild Lauf Leiste leichter positioniert wird.
-   **Wenn Benutzer davon profitieren, dass die Listenansicht größer wird, können Sie die Listenansicht und deren übergeordnetes Fenster ändern.** Auf diese Weise können Benutzer die Größe der Listenansicht nach Bedarf anpassen. Allerdings sollten in der Größe geänderte Listen Sichten nicht weniger als drei Elemente angezeigt werden.

## <a name="labels"></a>Bezeichnungen

### <a name="control-labels"></a>Steuerelement Bezeichnungen

-   Alle Listen Sichten benötigen Bezeichnungen. Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz, und beenden Sie mit einem Doppelpunkt mithilfe von statischem Text.
-   Weisen Sie einen eindeutigen [Zugriffsschlüssel](glossary.md) für jede Bezeichnung zu. Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   Positionieren Sie die Bezeichnung über dem Steuerelement, und richten Sie die Bezeichnung am linken Rand des Steuer Elements aus.
-   Schreiben Sie für Listenansichten mit Mehrfachauswahl die Bezeichnung, die eindeutig angibt, dass mehrere Auswahlmöglichkeiten möglich sind. Die Kontrollkästchen-Ansichts Bezeichnungen können weniger explizit sein.

    **Richtig:**

    ![Screenshot der Bezeichnung: Wählen Sie ein oder mehrere Add-ons aus. ](images/ctrl-list-views-image27.png)

    In diesem Beispiel gibt die Bezeichnung eindeutig an, dass mehrere Auswahlmöglichkeiten möglich sind.

    **Falsch:**

    ![Screenshot der Bezeichnung: Add-ons ](images/ctrl-list-views-image28.png)

    In diesem Beispiel stellt die Bezeichnung keine Informationen zur Mehrfachauswahl zur Verfügung.

    **Annehmbar:**

    ![Screenshot der Kontrollkästchen-Listen Bezeichnung: Add-ons ](images/ctrl-list-views-image29.png)

    In diesem Beispiel geben die Kontrollkästchen eindeutig an, dass eine Mehrfachauswahl möglich ist, sodass die Bezeichnung nicht explizit sein muss.

-   Sie können Einheiten (Sekunden, Verbindungen usw.) in Klammern hinter der Bezeichnung angeben.

### <a name="heading-labels"></a>Überschriften Bezeichnungen

-   Halten Sie die Überschriften Bezeichnungen kurz (drei Wörter oder weniger).
-   Verwenden Sie ein einzelnes Substantiv oder einen nominalen Ausdruck ohne endinterpunktions Zeichen.
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   Richten Sie die Überschrift auf die gleiche Weise wie die Daten aus.

### <a name="group-labels"></a>Gruppen Bezeichnungen

-   Verwenden Sie die folgenden Gruppen Bezeichnungen für Auflistungen auf hoher Ebene:
    -   Names: Verwenden Sie den ersten Buchstaben des Namens oder der Buchstaben.
    -   Größen: nicht angegeben, 0 KB, 0-10 KB, 10-100 KB, 100 KB-1 MB, 1-16 MB, 16-128 MB
    -   Datumsangaben: heute, gestern, letzte Woche, früher dieses Jahr und vor längerer Zeit.
-   Andernfalls verwenden Gruppen Bezeichnungen genau den Text der zu gruppierenden Daten, einschließlich der Groß-und Kleinschreibung.

### <a name="data-text"></a>Datentext

-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.

### <a name="instructional-text"></a>Anweisungs Text

-   Wenn Sie Anweisungs Text über eine Listenansicht hinzufügen müssen, fügen Sie ihn oberhalb der Bezeichnung hinzu. Verwenden Sie vollständige Sätze mit endinterpunktions Zeichen.
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   Zusätzliche Informationen, die hilfreich, aber nicht erforderlich sind, sollten kurz gehalten werden. Legen Sie diese Informationen entweder in Klammern zwischen der Bezeichnung und dem Doppelpunkt oder ohne Klammern unterhalb des Steuer Elements ab.

## <a name="documentation"></a>Dokumentation

Beim Verweis auf Listenansichten:

-   Verwenden Sie den genauen Bezeichnungs Text, einschließlich der Groß-/Kleinschreibung, aber nicht den Unterstrich oder Doppelpunkt des Zugriffsschlüssels, und fügen Sie die Word Es wird nicht als Listenfeld, Listenansicht oder Feld bezeichnet.
-   Verwenden Sie für Listen Daten den genauen Datentext einschließlich der Groß-/Kleinschreibung.
-   Weitere Informationen finden Sie in den Listenansichten nur in der Programmierung und in anderen technischen Dokumentationen. Die Liste wird von überall sonst verwendet.
-   Um die Benutzerinteraktion zu beschreiben, verwenden Sie für die Daten auswählen, und klicken Sie auf für die Überschriften.
-   Formatieren Sie nach Möglichkeit die Beschriftungs-und Listen Optionen mithilfe von fettem Text. Andernfalls sollten Sie die Bezeichnung und die Optionen nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Wählen Sie in der Liste " **Programme und Dienste** " die Option **Datei-und Druckerfreigabe** aus.

Beim Verweisen auf Kontrollkästchen in einer Listenansicht:

-   Verwenden Sie den genauen Bezeichnungs Text einschließlich der Groß-und Kleinschreibung, und schließen Sie das Kontrollkästchen Word ein Fügen Sie den Unterstrich "Zugriffsschlüssel" nicht ein.
-   Verwenden Sie zum Beschreiben der Benutzerinteraktion SELECT und Clear.
-   Formatieren Sie nach Möglichkeit die Bezeichnung mit fettem Text. Andernfalls sollten Sie die Bezeichnung nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Aktivieren Sie das Kontrollkästchen unter **Streichung** .

 

