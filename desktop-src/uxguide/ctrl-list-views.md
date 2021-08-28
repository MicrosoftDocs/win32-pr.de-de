---
title: Listenansichten
description: Mit einer Listenansicht können Benutzer eine Sammlung von Datenobjekten anzeigen und mit ihr interagieren, indem sie entweder eine einzelne Auswahl oder eine Mehrfachauswahl verwenden.
ms.assetid: 62a7bfc8-96a9-450d-9db9-ec9dab6687b7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8b8a1ce068b03ddf2a7aba40a0044f79914102d3
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983063"
---
# <a name="list-views"></a>Listenansichten

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Mit einer Listenansicht können Benutzer eine Sammlung von Datenobjekten anzeigen und mit ihr interagieren, indem sie entweder eine einzelne Auswahl oder eine Mehrfachauswahl verwenden.

![Screenshot der Listenansicht mit Spaltenüberschriften ](images/ctrl-list-views-image1.png)

Eine typische Listenansicht.

Listenansichten verfügen über mehr Flexibilität und Funktionalität als Listenfelder. Im Gegensatz zu Listenfeldern unterstützen sie das Ändern von Sichten, Gruppieren, mehrere Spalten mit Überschriften, Sortieren nach Spalten, Ändern der Spaltenbreite und -reihenfolge, Das Ist eine Ziehquelle oder ein Ablageziel und das Kopieren von Daten in die und aus der Zwischenablage.

> [!Note]  
> Richtlinien im Zusammenhang [mit Layout-](vis-layout.md) [und Listenfeldern](ctrl-list-boxes.md) werden in separaten Artikeln vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Eine Listenansicht ist mehr als nur ein flexibleres und funktionales Listenfeld: Die zusätzliche Funktionalität führt zu einer unterschiedlichen Verwendung. Die folgende Tabelle zeigt den Vergleich.



|   Verwendung                          | Listenfelder                 | Listenansichten               |
|-----------------------------|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **Datentyp**<br/>    | Daten- und Programmoptionen.<br/> | Nur Daten.<br/>                                                                                                                         |
| **Contents**<br/>     | Nur Bezeichnungen.<br/>                   | Bezeichnungen und Zusätzliche Daten, möglicherweise in mehreren Spalten.<br/>                                                                           |
| **Interaktion**<br/>  | Wird zum Treffen von Auswahlen verwendet.<br/>    | Kann zum Treffen von Auswahlen verwendet werden, wird aber häufig zum Anzeigen und Interagieren mit Daten verwendet. Kann eine Ziehquelle oder ein Absturzziel sein.<br/> |
| **Präsentation**<br/> | Fest.<br/>                         | Benutzer können Sichten ändern, gruppieren, nach Spalten sortieren und Spaltenbreite und -reihenfolge ändern.<br/>                                                |



 

Um zu entscheiden, ob dies die richtige Kontrolle ist, sollten Sie die folgenden Fragen berücksichtigen:

-   **Werden in der Liste Daten anstelle von Programmoptionen angezeigt?** Falls nicht, sollten Sie stattdessen ein Listenfeld verwenden.
-   **Müssen Benutzer Sichten ändern, gruppieren, nach Spalten sortieren oder Spaltenbreite und -reihenfolge ändern?** Falls nicht, verwenden Sie stattdessen ein Listenfeld.
-   **Muss das Steuerelement eine Ziehquelle oder ein Absturzziel sein?** Wenn ja, verwenden Sie eine Listenansicht.
-   **Müssen die Listenelemente in die Zwischenablage kopiert oder aus der Zwischenablage eingefügt werden?** Wenn ja, verwenden Sie eine Listenansicht.

### <a name="check-box-list-views"></a>Kontrollkästchenlistenansichten

-   **Wird das Steuerelement verwendet, um null oder mehr Elemente aus einer Datenliste zu wählen?** Verwenden Sie stattdessen eine einzelne Auswahl, um ein Element zu wählen.
-   **Ist die Mehrfachauswahl für die Aufgabe unerlässlich oder wird sie häufig verwendet?** Wenn ja, verwenden Sie eine Kontrollkästchenlistenansicht, um die Mehrfachauswahl offensichtlich zu machen, insbesondere, wenn Ihre Zielbenutzer nicht erweitert sind. Wenn nicht, verwenden Sie eine Standardmäßige Mehrfachauswahllistenansicht, wenn die Kontrollkästchen zu viel Aufmerksamkeit auf die Mehrfachauswahl ziehen oder zu viel Bildschirmübersicht führen würden.
-   **Ist die Stabilität der Mehrfachauswahl wichtig?** Wenn ja, verwenden Sie eine [Kontrollkästchenliste,](ctrl-list-boxes.md)einen Listen-Generator oder eine Liste zum Hinzufügen/Entfernen, da durch Klicken immer nur ein Element gleichzeitig geändert wird. Mit einer Standard-Mehrfachauswahlliste ist es sehr einfach, alle Auswahlen auch bei einem Zufall zu löschen.

> [!Note]  
> Manchmal wird ein Steuerelement, das wie eine Listenansicht aussieht, mithilfe eines Listenfelds implementiert und umgekehrt. Wenden Sie in solchen Fällen die Richtlinien basierend auf der Verwendung und nicht auf der Implementierung an.

 

## <a name="usage-patterns"></a>Verwendungsmuster

Alle Ansichten unterstützen eine einzelne Auswahl, bei der Benutzer nur ein Element gleichzeitig auswählen können, und mehrere Auswahlen, bei denen Benutzer eine beliebige Anzahl von Elementen auswählen können, einschließlich keiner. Listenansichten [](glossary.md)unterstützen den erweiterten Auswahlmodus, in dem die Auswahl durch Ziehen oder mit UMSCHALT+Klick oder STRG+Klick erweitert werden kann, um Gruppen von zusammenhängenden bzw. nicht benachbarten Werten auszuwählen. Im Gegensatz zu Listenfeldern [](glossary.md)unterstützen sie nicht den Mehrfachauswahlmodus, bei dem durch Klicken auf ein Element der Auswahlzustand unabhängig von der UMSCHALTTASTE und STRG-Taste umgeschaltet wird.

### <a name="standard-list-view"></a>Standardlistenansicht

Das Listenansicht-Steuerelement unterstützt fünf Standardansichten:



|    Verwendung    |   Beispiel        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kachel**<br/> Jedes Element wird als mittleres Symbol mit einer Bezeichnung und optionalen Details auf der rechten Seite angezeigt. <br/>                                                                                                                         | ![Screenshot von Miniaturansichten mit Titeln und Details ](images/ctrl-list-views-image2.png)<br/> In der Kachelansicht werden mittlere Symbole mit Bezeichnungen und optionalen Details auf der rechten Seite angezeigt.<br/>                                                                                                                                                                |
| **Großes Symbol**<br/> Jedes Element wird als besonders großes, großes oder mittleres Symbol mit einer Bezeichnung darunter angezeigt.<br/>                                                                                                                      | ![Screenshot der großen Miniaturansicht der Liste ](images/ctrl-list-views-image3.png)<br/> Große Symbolansicht zeigt jedes Element als großes Symbol mit einer Bezeichnung darunter an.<br/>                                                                                                                                                                              |
| **Kleines Symbol**<br/> Jedes Element wird als kleines Symbol mit einer Bezeichnung auf der rechten Seite angezeigt.<br/>                                                                                                                                           | ![Screenshot der kleinen Miniaturansicht der Liste ](images/ctrl-list-views-image4.png)<br/> Kleine Symbolansicht zeigt jedes Element als kleines Symbol mit seiner Bezeichnung auf der rechten Seite an.<br/>                                                                                                                                                                        |
| **Liste**<br/> Jedes Element wird als kleines Symbol mit einer Bezeichnung auf der rechten Seite angezeigt.<br/>                                                                                                                                                 | im Listenmodus ordnet diese Sicht Elemente in Spalten an und verwendet eine horizontale Scrollleiste. Im Gegensatz dazu ordnet der Symbolansichtsmodus Elemente in Zeilen an und verwendet eine vertikale Bildlaufleiste. <br/> ![Screenshot der Listenansicht im Listenmodus ](images/ctrl-list-views-image5.png)<br/> Im Listenmodus wird jedes Element als kleines Symbol mit der Bezeichnung auf der rechten Seite angezeigt.<br/> |
| **Details**<br/> Jedes Element wird als Zeile in einem Tabellenformat angezeigt. Die spalte ganz links enthält sowohl das optionale Symbol als auch die Bezeichnung des Elements, und die nachfolgenden Spalten enthalten zusätzliche Informationen, z. B. Elementeigenschaften.<br/> | Darüber hinaus können Spalten hinzugefügt oder entfernt sowie neu angeordnet und die Größe geändert werden. Zeilen können nach Spalte sortiert werden. <br/> ![Screenshot der Listenansicht im Detailmodus ](images/ctrl-list-views-image6.png)<br/> In der Detailansicht wird jedes Element als Zeile in einem Tabellenformat angezeigt.<br/>                                                              |



 

### <a name="list-view-variations"></a>Listenansichtsvariationen




| Bezeichnung | Wert |
|--------|-------|
| <strong>Spaltenauswahl</strong><br /> Listenansichten weisen manchmal so viele Spalten auf, dass es nicht praktikabel ist, sie alle zu zeigen. In diesem Fall ist der beste Ansatz, standardmäßig die nützlichsten Spalten anzuzeigen und Benutzern das Hinzufügen oder Entfernen von Spalten nach Bedarf zu ermöglichen. <br /> | <img src="images/ctrl-list-views-image7.png" alt="Screen shot of list view with Column Chooser menu " /><br /> Wenn Sie mit der rechten Maustaste auf die Spaltenüberschrift klicken, wird ein Kontextmenü angezeigt, über das Benutzer Spalten hinzufügen oder entfernen können.<br /><img src="images/ctrl-list-views-image8.png" alt="Screen shot of Choose Details dialog box " /><br /> Wenn Sie im Kontextmenü der Spaltenüberschrift auf Mehr klicken, wird das Dialogfeld Spalten auswählen angezeigt, in dem Benutzer Spalten hinzufügen oder entfernen sowie neu anordnen können.<br /> | 
| <strong>Kontrollkästchenlistenansicht</strong><br /> Benutzern das Auswählen mehrerer Elemente erlauben.<br /> | Mehrfachauswahllistenansichten haben genau das gleiche Aussehen wie Einzelauswahllistenansichten, sodass es keinen visuellen Hinweis darauf gibt, dass sie mehrfache Auswahl unterstützen. Eine Kontrollkästchenlistenansicht kann verwendet werden, um eindeutig anzugeben, dass eine Mehrfachauswahl möglich ist. Daher sollte dieses Muster für Aufgaben verwendet werden, bei denen mehrfache Auswahl wichtig oder häufig verwendet wird.<br /><img src="images/ctrl-list-views-image9.png" alt="Screen shot of dialog box with several check boxes " /><br /> In diesem Beispiel verwendet eine Kleine Symbolansicht Kontrollkästchen, da die Mehrfachauswahl für die Aufgabe unerlässlich ist.<br /> | 
| <strong>Auflisten von Ansichten mit Gruppen</strong><br /> Organisieren Sie die Daten in Gruppen.<br /> | Während Detailansichten häufig das Sortieren der Daten nach einer der Spalten unterstützen, ermöglichen Listenansichten benutzern darüber hinaus das Organisieren der Elemente in Gruppen. Einige Vorteile der Gruppierung sind:<br /><ul><li>Gruppen funktionieren in allen Ansichten (mit Ausnahme der Liste), sodass Benutzer z. B. eine besonders große Symbolansicht von Alben nach Interpret gruppieren können.</li><li>Gruppen können allgemeinere Sammlungen sein, die oft aussagekräftiger sind als das direkte Gruppieren von Daten. Beispielsweise gruppiert Windows Explorer Datumsangaben in Today, Today, Last week, Earlier this year und A long time ago.</li></ul><img src="images/ctrl-list-views-image10.png" alt="Screen shot of list view with several data groups " /><br /> In diesem Beispiel zeigt die Windows Begrüßungscenter gruppierte Elemente in einer Listenansicht an.<br /> | 




 

## <a name="guidelines"></a>Richtlinien

### <a name="presentation"></a>Präsentation

-   **Sortiert Listenelemente in einer logischen Reihenfolge.** Sortieren Sie Namen in alphabetischer Reihenfolge, Zahlen in numerischer Reihenfolge und Datumsangaben in chronologischer Reihenfolge.
-   **Lassen Sie ggf. zu, dass Benutzer die Sortierreihenfolge ändern können.** Die Benutzersortierung ist wichtig, wenn die Liste viele Elemente enthält oder wenn es Szenarien gibt, in denen Elemente mit einer anderen Sortierreihenfolge als der Standardreihenfolge effektiver gefunden werden.
-   **Verwenden Sie das Always Show Selection-Attribut,** damit Benutzer das ausgewählte Element direkt bestimmen können, auch wenn das Steuerelement nicht den Fokus besitzt.
-   **Vermeiden Sie die Darstellung leerer Listenansichten.** Wenn Benutzer eine Liste erstellen, initialisieren Sie die Liste mit Anweisungen oder Beispielelementen, die Benutzer möglicherweise benötigen.

    ![Screenshot des Suchdialogfelds mit Anweisungen ](images/ctrl-list-views-image11.png)

    In diesem Beispiel enthält die Suchlistenansicht zunächst Anweisungen.

-   **Wenn Benutzer Sichten ändern, gruppieren, nach Spalten sortieren oder Spalten und deren Breite und Reihenfolge ändern können, lassen Sie diese Einstellungen beibehalten, damit sie bei der nächsten Anzeige der Listenansicht wirksam werden.** Legen Sie fest, dass sie in einer Listenansicht pro Benutzer beibehalten werden.

### <a name="interaction"></a>Interaktion

-   **Wählen Sie mit nur einem Klick das Listenelement aus, auf das der Benutzer verweist. Ausnahme:** Für das Befehlslinklistenmuster wählt ein Klick das Element aus und schließt entweder das Fenster oder navigiert zur nächsten Seite.
-   **Erwägen Sie die Bereitstellung eines Doppelklickverhaltens.** Doppelklicken sollte die gleiche Auswirkung wie das Auswählen eines Elements und das Ausführen des Standardbefehls haben.
-   **Redundantes Doppelklickverhalten.** Es sollte immer eine Befehlsschaltfläche oder ein Kontextmenübefehl mit der gleichen Auswirkung vorhanden sein.
-   Wenn ein Listenelement eine weitere Erläuterung erfordert, **geben Sie die Erklärung in einem** [Infotip an.](ctrl-tooltips-and-infotips.md) Verwenden Sie vollständige Sätze und endende Interpunktion.

    ![Screenshot der Listenansicht mit Tastaturinfo ](images/ctrl-list-views-image12.png)

    In diesem Beispiel wird eine Infotip verwendet, um weitere Informationen bereitzustellen.

-   **Geben Sie Kontextmenüs relevanter Befehle an.** Zu diesen Befehlen gehören Ausschneiden, Kopieren, Einfügen, Entfernen oder Löschen, Umbenennen und Eigenschaften.
-   **Wenn Benutzer die Sortierreihenfolge und Gruppierung ändern können, geben Sie die Kontextmenüs Sortieren nach und Gruppieren nach an.** Mit dem ersten Klick auf einen Spaltennamen wird die Liste in aufsteigender Reihenfolge für diese Spalte sortiert oder gruppiert. Beim zweiten Klick wird die Liste in absteigender Reihenfolge sortiert oder gruppiert. Verwenden Sie die vorherige Reihenfolge (aus einer anderen Spalte) als sekundären Schlüssel.

    ![Screenshot der Listenansicht mit dem Menü "Sortieren nach" ](images/ctrl-list-views-image13.png)

    In diesem Beispiel ändert das Kontextmenü Sortieren nach die Sortierreihenfolge. Wenn Sie auf Name klicken, wird der Name in aufsteigender Reihenfolge sortiert. Wenn Sie erneut auf Name klicken, wird der Name in absteigender Reihenfolge sortiert.

-   **Ermöglichen Sie den Zugriff auf die Spaltenüberschrift der Listenansicht über die Tastatur.**
    -   **Entwickler:** Sie können dies erreichen, indem Sie den Fokus auf das Spaltenheadersteuerelement festlegen. Diese Funktion ist für Windows Vista neu.
-   **Deaktivieren Sie beim Deaktivieren einer Listenansicht auch alle zugeordneten Bezeichnungen und Befehlsschaltflächen.**
-   **Vermeiden Sie horizontales Scrollen.** Der Listenmodus verwendet horizontales Scrollen. Dieser Modus ist in der Regel der kompakteste, aber horizontales Scrollen ist im Allgemeinen schwieriger zu verwenden als vertikales Scrollen. Ziehen Sie stattdessen die Verwendung der Ansicht Kleines Symbol in Betracht, wenn Kompaktheit nicht wichtig ist. Der Listenmodus ist jedoch eine gute Wahl, wenn viele alphabetisch sortierte Elemente und ausreichend Bildschirmfläche für ein breit sortiertes Steuerelement vorhanden sind.

    **Annehmbar:**

    ![Screenshot eines Breitlistenmodus-Steuerelements ](images/ctrl-list-views-image14.png)

    In diesem Beispiel wird der Listenmodus verwendet, da es viele Elemente und viel verfügbaren Bildschirmbereich für ein wide-Steuerelement gibt.

### <a name="multiple-selection-lists"></a>Mehrfachauswahllisten

-   **Erwägen Sie, die Anzahl der ausgewählten Elemente unterhalb der Liste anzuzeigen,** insbesondere, wenn Benutzer wahrscheinlich mehrere Elemente auswählen. Diese Informationen geben nicht nur nützliches Feedback, sondern geben auch deutlich an, dass die Listenansicht die Mehrfachauswahl unterstützt.

    ![Screenshot der Liste mit fünf ausgewählten Miniaturansichten ](images/ctrl-list-views-image15.png)

    In diesem Beispiel wird die Anzahl der ausgewählten Elemente unterhalb der Liste angezeigt.

-   Alternativ können Sie anstelle der Anzahl der ausgewählten Elemente andere Auswahlmetriken verwenden, die möglicherweise aussagekräftiger sind, z. B. die für die Auswahl erforderlichen Ressourcen.

    ![Screenshot des Dialogfelds mit Speicherplatz auf dem Datenträger ](images/ctrl-list-views-image16.png)

    In diesem Beispiel ist der Speicherplatz, der für die Installation der Komponenten erforderlich ist, aussagekräftiger als die Anzahl der ausgewählten Komponenten.

-   Wenn potenziell viele Elemente vorhanden sind und alle Elemente ausgewählt oder gelöscht werden können, fügen Sie für Kontrollkästchenlisten die Schaltflächen Alle auswählen und Alle löschen hinzu.
-   **Verwenden Sie Kontrollkästchen mit gemischten Zuständen, um eine Teilauswahl der Elemente in einem Container anzugeben.** Der gemischte Zustand wird nicht als dritter Zustand für ein einzelnes Element verwendet.

### <a name="changing-views"></a>Ändern von Ansichten

Wenn Benutzer Ansichten ändern können:

-   **Wählen Sie standardmäßig die bequemste Ansicht aus.** Alle Änderungen, die Benutzer vornehmen, sollten in einer Listenansicht pro Benutzer persistent gemacht werden.
-   **Ändern Sie die Ansicht mithilfe einer geteilten Schaltfläche, einer Menüschaltfläche oder einer Dropdownliste.** Verwenden Sie nach Möglichkeit eine [unterteilte Schaltfläche](ctrl-command-buttons.md) auf der Symbolleiste, und ändern Sie die Schaltflächenbezeichnung, um die aktuelle Ansicht widerzuspiegeln.

    ![Screenshot der Liste mit geteilter Schaltfläche "Ansichten" ](images/ctrl-list-views-image17.png)

    In diesem Beispiel wird eine geteilte Schaltfläche auf der Symbolleiste verwendet, um Ansichten zu ändern.

-   **Geben Sie ein Kontextmenü Ansicht an.**

    ![Screenshot der Liste mit Kontextmenü "Ansicht" ](images/ctrl-list-views-image18.png)

In diesem Beispiel wird ein Kontextmenü Ansicht verwendet, um Ansichten zu ändern.

### <a name="details-views"></a>Detailansichten

-   **Erwägen Sie die Verwendung der Kachelansicht, um die Lesbarkeit zu verbessern.**

    **Annehmbar:**

    ![Screenshot der Detailliste mit schmalen Spalten ](images/ctrl-list-views-image19.png)

    In diesem Beispiel sind zu viele Daten vorhanden, und Fenster, Liste und Spalten sind zu klein, sodass die Listenelemente schwer zu lesen sind.

    **Besser:**

    ![Screenshot der Detailliste mit Daten in Gruppen ](images/ctrl-list-views-image20.png)

    In diesem Beispiel zeigt die Kachelansicht die Daten ohne Kürzung an.

-   **Wählen Sie die Standardspaltenbreiten aus, die für die längsten Daten geeignet sind.** Listenansichten kürzen lange Daten automatisch mit Ellipsen, sodass die Spaltenbreiten geeignet sind, wenn standardmäßig nur wenige Ellipsen angezeigt werden. Während Benutzer die Größe von Spalten ändern können, bevorzugen Sie andere Lösungen:

    -   Passen Sie jede Spaltenbreite so an, dass sie ihren Daten entspricht.
    -   Passen Sie die Breite des Steuerelements an die Spalten und alle wahrscheinlichen Bildlaufleisten an.
    -   Verwenden Sie bei Bedarf horizontales Scrollen.
    -   Sie haben Daten nur für Elemente mit ungerader Größe oder als letzte Möglichkeit abgeschnitten.

    Wenn Daten normaler Größe standardmäßig abgeschnitten werden müssen, können Sie die Größe des Fensters und der Listenansicht ändern. Fügen Sie zusätzliche 30 Prozent (bis zu 200 Prozent für kürzeren Text) für jeden Text (aber keine Zahlen) ein, der lokalisiert wird.

    **Falsch:**

    ![Screenshot der Listenspalten mit abgeschnittenen Daten ](images/ctrl-list-views-image21.png)

    In diesem Beispiel werden die meisten Daten abgeschnitten. Die vielen Auslassungszeichen deuten deutlich darauf hin, dass das Steuerelement und die Spaltenbreite zu klein für die Daten sind.

    **Falsch:**

    ![Screenshot einer einspaltigen Liste mit abgeschnittenen Daten ](images/ctrl-list-views-image22.png)

    In diesem Beispiel werden Daten ohne Grund abgeschnitten.

-   **Wählen Sie eine geeignete Standardspaltenreihenfolge aus.** Ordnen Sie die Spalten im Allgemeinen wie folgt an:

    -   Zuerst der Elementname oder die identifizierenden Daten.
    -   Als Nächstes sind andere Daten hilfreich, um die Listenelemente zu unterscheiden.
    -   Als Nächstes die nützlichsten Daten (vorzugsweise kurz oder mit fester Länge).
    -   Als Nächstes werden weniger nützliche Daten (bevorzugt kurze oder feste Länge) angezeigt.
    -   Letzte, lange Daten variabler Länge.

    Lange, variable Längendaten werden in die letzten Spalten platziert, um den Bedarf an horizontalem Scrollen zu reduzieren. Platzieren Sie in diesen Kategorien verwandte Informationen zusammen in einer logischen Sequenz.

-   **Erlauben Sie Benutzern gegebenenfalls, Spalten hinzuzufügen und zu entfernen sowie die Reihenfolge zu ändern.** Standardmäßig werden die nützlichsten Spalten angezeigt. Dies wird mit dem Header Drag Drop-Attribut erreicht.
-   Wählen Sie eine für die Daten geeignete Ausrichtung aus. Verwenden Sie die folgenden Regeln:
    -   Richten Sie Zahlen, Währungen und Zeiten nach rechts aus.
    -   Links ausgerichteter Text, IDs (auch wenn numerisch) und Datumsangaben.
-   Bei sortierbaren Spaltenüberschriften sortiert der erste Klick auf eine Überschrift die Liste in aufsteigender Reihenfolge für die Spalte, während der zweite Klick in absteigender **Reihenfolge sortiert wird.** Verwenden Sie die vorherige Sortierreihenfolge (aus einer anderen Spalte) als sekundären Sortierschlüssel.

    ![Screenshot der Detailliste mit sortierten Daten ](images/ctrl-list-views-image23.png)

    In diesem Beispiel wurde zuerst auf die Spalte Name und dann auf die Spalte Typ geklickt. Daher ist Typ in aufsteigender Reihenfolge der primäre Sortierschlüssel und Name in aufsteigender Reihenfolge der sekundäre.

-   **Verwenden Sie das Attribut Full Row Select,** damit Benutzer die ausgewählten Elemente in allen Spalten leicht bestimmen können.
-   **Verwenden Sie nur dann einen sortierbaren Spaltenheader, wenn die Daten sortiert werden können.**
-   **Verwenden Sie keinen Spaltenheader, wenn es nur eine Spalte gibt und keine umgekehrte Sortierung notwendig ist.** Verwenden Sie stattdessen eine Bezeichnung, um die Daten zu identifizieren.

    **Falsch:**

    ![Screenshot der Liste mit Bezeichnung im Spaltenheader ](images/ctrl-list-views-image24.png)

    **Richtig:**

    ![Screenshot der Liste mit der Bezeichnung über dem Steuerelement ](images/ctrl-list-views-image25.png)

    Im richtigen Beispiel wird anstelle eines Spaltenheaders eine Bezeichnung verwendet.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstand

![Screenshot: Größen- und Abstandsgröße der Liste ](images/ctrl-list-views-image26.png)

Empfohlene Größe und Abstand für Listenansichten.

-   **Wählen Sie eine Listenansichtshöhe aus, die eine ganzzahliger Anzahl von Elementen anzeigt.** Vermeiden Sie das vertikale Abschneiden von Elementen.
-   **Wählen Sie eine Listenansichtsgröße aus, die unnötiges vertikales und horizontales Scrollen in allen unterstützten Ansichten verhindert.** Listenansichten sollten zwischen 3 und 20 Elemente anzeigen. Erwägen Sie, eine Listenansicht etwas größer zu machen, wenn dadurch eine Scrollleiste entfernt wird. Listen mit potenziell vielen Elementen sollten mindestens fünf Elemente anzeigen, um das Scrollen zu erleichtern, indem mehr Elemente gleichzeitig angezeigt werden und die Position der Scrollleiste vereinfacht wird.
-   **Wenn Benutzer davon profitieren, die Listenansicht zu vergrößern, können Sie die Größe der Listenansicht und des übergeordneten Fensters ändern.** Auf diese Weise können Benutzer die Größe der Listenansicht nach Bedarf anpassen. In Listenansichten, die die Größe ändern können, sollten jedoch nicht weniger als drei Elemente angezeigt werden.

## <a name="labels"></a>Bezeichnungen

### <a name="control-labels"></a>Steuerelementbezeichnungen

-   Alle Listenansichten benötigen Bezeichnungen. Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz, der mit einem Doppelpunkt endet, der statischen Text verwendet.
-   Weisen Sie für [jede Bezeichnung einen eindeutigen](glossary.md) Zugriffsschlüssel zu. Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).
-   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md)
-   Positionieren Sie die Bezeichnung über dem Steuerelement, und richten Sie die Bezeichnung am linken Rand des Steuerelements aus.
-   Schreiben Sie für Listenansichten mit mehrfacher Auswahl die Bezeichnung, die deutlich angibt, dass eine Mehrfachauswahl möglich ist. Bezeichnungen von Kontrollkästchenlistenansichten können weniger explizit sein.

    **Richtig:**

    ![Screenshot der Bezeichnung: Wählen Sie ein oder mehrere Add-Ons aus. ](images/ctrl-list-views-image27.png)

    In diesem Beispiel gibt die Bezeichnung eindeutig an, dass eine Mehrfachauswahl möglich ist.

    **Falsch:**

    ![Screenshot der Bezeichnung: Add-Ons ](images/ctrl-list-views-image28.png)

    In diesem Beispiel stellt die Bezeichnung keine Informationen zur Mehrfachauswahl zur Verfügung.

    **Annehmbar:**

    ![Screenshot der Bezeichnung der Kontrollkästchenliste: Add-Ons ](images/ctrl-list-views-image29.png)

    In diesem Beispiel weisen die Kontrollkästchen eindeutig darauf hin, dass eine Mehrfachauswahl möglich ist, sodass die Bezeichnung nicht explizit sein muss.

-   Sie können Einheiten (Sekunden, Verbindungen und so weiter) in Klammern nach der Bezeichnung angeben.

### <a name="heading-labels"></a>Überschriftenbezeichnungen

-   Halten Sie die Überschriftenbezeichnungen kurz (drei Wörter oder weniger).
-   Verwenden Sie ein einzelnes Nomen oder einen nomen Ausdruck ohne endende Interpunktion.
-   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md)
-   Richten Sie die Überschrift auf die gleiche Weise wie die Daten aus.

### <a name="group-labels"></a>Gruppenbezeichnungen

-   Verwenden Sie die folgenden Gruppenbezeichnungen für Sammlungen auf hoher Ebene:
    -   Namen: Verwenden Sie den ersten Buchstaben von Namen oder Buchstabenbereichen.
    -   Größen: Nicht angegeben, 0 KB, 0-10 KB, 10-100 KB, 100 KB - 1 MB, 1-16 MB, 16-128 MB
    -   Datumsangaben: Today, Today, Last week, Earlier this year und A long time ago.
-   Andernfalls verwenden Gruppenbezeichnungen den genauen Text der zu gruppierenden Daten, einschließlich Groß- und Interpunktion.

### <a name="data-text"></a>Datentext

-   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md)

### <a name="instructional-text"></a>Anweisungstext

-   Wenn Sie Anweisungstext zu einer Listenansicht hinzufügen müssen, fügen Sie ihn über der Bezeichnung hinzu. Verwenden Sie vollständige Sätze mit endender Interpunktion.
-   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md)
-   Zusätzliche Informationen, die hilfreich, aber nicht erforderlich sind, sollten kurz gehalten werden. Platzieren Sie diese Informationen entweder in Klammern zwischen der Bezeichnung und dem Doppelpunkt oder ohne Klammern unterhalb des Steuerelements.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Listenansichten:

-   Verwenden Sie den genauen Bezeichnungstext einschließlich der Groß-/Unterstriche, aber schließen Sie nicht den Unterstrich oder Doppelpunkt des Zugriffs ein, und fügen Sie die Wortliste ein. Verweisen Sie nicht auf ein Listenfeld als Listenfeld, Listenansicht oder Feld.
-   Verwenden Sie für Listendaten den genauen Datentext, einschließlich der Groß-/Groß-/Großbucht.
-   Listenansichten werden nur in der Programmierung und in anderen technischen Dokumentationen als Listenansichten bezeichnet. Überall sonst verwenden Sie eine Liste.
-   Verwenden Sie select für die Daten, und klicken Sie auf die Überschriften, um die Benutzerinteraktion zu beschreiben.
-   Formatieren Sie die Bezeichnungs- und Listenoptionen nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung und die Optionen nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Wählen Sie in **der Liste Programme und Dienste** die Option **Datei- und Druckerfreigabe aus.**

Beim Verweisen auf Kontrollkästchen in einer Listenansicht:

-   Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Unterschrift, und schließen Sie das Kontrollkästchen wort ein. Schließen Sie den Unterstrich der Zugriffsschlüssel nicht ein.
-   Verwenden Sie select und clear, um die Benutzerinteraktion zu beschreiben.
-   Formatieren Sie die Bezeichnung nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Aktivieren Sie das **Kontrollkästchen** Unterstrichen.

 

