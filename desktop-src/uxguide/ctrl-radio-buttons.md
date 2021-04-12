---
title: Options Felder
description: Mit einem Optionsfeld treffen Benutzer eine Auswahl zwischen einem Satz von sich gegenseitig ausschließenden Optionen.
ms.assetid: f9af0a8a-d4a1-464c-a967-bab88ae0726b
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 00495695753506702015431c889e74d5a7effe9a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104218946"
---
# <a name="radio-buttons"></a>Options Felder

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Mit einem Optionsfeld treffen Benutzer eine Auswahl zwischen einem Satz von sich gegenseitig ausschließenden Optionen. Benutzer können nur eine Option auswählen. Options Felder werden so aufgerufen, dass Sie wie die channelvoreinstellungen in Radios funktionieren.

![Screenshot von drei Options Feldern ](images/radio-buttons-image1.png)

Eine typische Gruppe von Options Feldern.

Eine Gruppe von Options Feldern verhält sich wie ein einzelnes Steuerelement. Nur die ausgewählte Auswahl ist über die Tab-Taste zugänglich, Benutzer können jedoch mithilfe der Pfeiltasten durch die Gruppe durchlaufen werden.

> [!Note]  
> Die Richtlinien im Zusammenhang mit [Layout](vis-layout.md) und [Tastaturnavigation](inter-keyboard.md) werden in einem separaten Artikel dargestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Wird das Steuerelement verwendet, um eine Option aus einem Satz von sich gegenseitig ausschließenden Optionen auszuwählen?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Wenn Sie mehrere Optionen auswählen möchten, verwenden [Sie stattdessen Kontrollkästchen](ctrl-check-boxes.md), eine [Mehrfachauswahl Liste](ctrl-list-boxes.md) oder eine Kontrollkästchen Liste.
-   **Ist die Anzahl von Optionen zwischen zwei und sieben?** Da der verwendete Bildschirmbereich proportional zur Anzahl der Optionen ist, behalten Sie die Anzahl der Optionen in einer Gruppe zwischen zwei und sieben. Verwenden Sie für acht oder mehr Optionen eine [Dropdown Liste](/windows/desktop/uxguide/ctrl-drop) oder eine [einfache Auswahlliste](ctrl-list-boxes.md).
-   **Ist ein Kontrollkästchen eine bessere Wahl?** Wenn nur zwei Optionen vorhanden sind, können Sie stattdessen ein einzelnes [Kontrollkästchen](ctrl-check-boxes.md) verwenden. Kontrollkästchen eignen sich jedoch nur zum Aktivieren oder Deaktivieren einer einzelnen Option, während Options Felder für vollkommen unterschiedliche Alternativen eingesetzt werden können. Wenn beide Lösungen möglich sind:
    -   Verwenden Sie Options Felder, wenn die Bedeutung des Kontrollkästchens nicht vollständig ersichtlich ist.

        **Falsch:**

        ![Kontrollkästchen für das Querformat ](images/radio-buttons-image2.png)

        **Richtig:**

        ![Screenshot der Options Felder für Querformat/Hochformat ](images/radio-buttons-image3.png)

        Im richtigen Beispiel sind die Optionen keine Gegensätze, daher sind Options Felder die bessere Wahl.

    -   Verwenden Sie Options Felder auf Assistenten Seiten, um die Alternativen zu löschen, selbst wenn ein Kontrollkästchen andernfalls akzeptabel ist.
    -   Verwenden Sie Options Felder, wenn genügend Platz auf dem Bildschirm vorhanden ist, und die Optionen sind wichtig genug, um diesen Bildschirmbereich gut verwenden zu können. Andernfalls verwenden Sie ein Kontrollkästchen oder eine Dropdown Liste.

        **Falsch:**

        ![Screenshot der Options Felder "anzeigen/nicht anzeigen" ](images/radio-buttons-image4.png)

        In diesem Beispiel sind die Optionen für die Verwendung von Options Feldern nicht wichtig genug.

        **Richtig:**

        ![Screenshot des Kontrollkästchens diese Meldung nicht anzeigen ](images/radio-buttons-image5.png)

        In diesem Beispiel ist ein Kontrollkästchen eine effiziente Verwendung des Bildschirm Raums für diese Peripherie Option.

    -   Verwenden Sie ein Kontrollkästchen, wenn auf der Seite andere Kontrollkästchen vorhanden sind.

-   **Wäre eine Dropdown Liste eine bessere Wahl?** Wenn die Standardoption für die meisten Benutzer in den meisten Fällen empfohlen wird, kann es vorkommen, dass Options Felder mehr Aufmerksamkeit auf die Optionen als notwendig zeichnen.
    -   Ziehen Sie in Erwägung, eine Dropdown Liste zu verwenden, wenn Sie nicht auf die Optionen aufmerksam machen möchten, oder wenn Sie nicht möchten, dass Benutzer Änderungen vornehmen. Eine Dropdown Liste konzentriert sich auf die aktuelle Auswahl, während Options Felder alle Optionen gleichermaßen hervorheben.

        ![Screenshot der höchsten Qualität als Standard Schaltfläche ](images/radio-buttons-image6.png)

        In diesem Beispiel konzentriert sich eine Dropdown Liste auf die aktuelle Auswahl und verhindert, dass Benutzer Änderungen vornehmen.

    -   Ziehen Sie eine Dropdown Liste in Erwägung, wenn auf der Seite andere Dropdown Listen vorhanden sind.

-   **Wäre eine Reihe von Befehls Schaltflächen, Befehls Verknüpfungen oder eine Trenn Schaltfläche eine bessere Wahl?** Wenn die Options Felder nur verwendet werden, um zu beeinflussen, wie ein Befehl ausgeführt wird, ist es häufig besser, stattdessen die Befehls Variationen darzustellen. Auf diese Weise können Benutzer den richtigen Befehl mit einer einzelnen Interaktion auswählen.
-   **Stellen die Optionen Programmoptionen anstelle von Daten dar?** Die Optionswerte sollten nicht auf dem Kontext oder anderen Daten basieren. Verwenden Sie für Daten eine Dropdown Liste oder eine einfache Auswahlliste.
-   Wenn das Steuerelement auf einer Assistenten Seite oder Systemsteuerung verwendet wird, **ist das Steuerelement eine Antwort auf die Haupt Anweisung und kann Benutzer später die Auswahl ändern?** Wenn dies der Fall ist, sollten Sie anstelle von Options Feldern Befehls Verknüpfungen verwenden, um die Interaktion effizienter zu gestalten.
-   **Sind die Werte nicht numerisch?** Verwenden Sie für numerische Daten [Textfelder](ctrl-text-boxes.md), [Dropdown Listen](/windows/desktop/uxguide/ctrl-drop)oder [Schieberegler](ctrl-sliders.md).

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Listen Sie die Optionen in einer logischen Reihenfolge auf,** z. b. mit der wahrscheinlichsten, wenn Sie am wahrscheinlichsten oder am einfachsten mit der höchsten Komplexität ausgewählt werden. Die alphabetische Reihenfolge wird nicht empfohlen, da Sie sprachabhängig und daher nicht lokalisierbar ist.
-   **Wenn keine der Optionen gültig ist, fügen Sie eine weitere Option zum Reflektieren dieser Auswahl hinzu,** z. b. keine oder nicht.
-   **Es empfiehlt sich, Options Felder vertikal anstelle von horizontal auszurichten.** Die horizontale Ausrichtung ist schwieriger zu lesen und zu lokalisieren.

    **Richtig:**

    ![Screenshot der vertikalen Optionsfeld Ausrichtung ](images/radio-buttons-image7.png)

    In diesem Beispiel werden die Options Felder vertikal ausgerichtet.

    **Falsch:**

    ![Screenshot der horizontalen Optionsfeld Ausrichtung ](images/radio-buttons-image8.png)

    In diesem Beispiel ist die horizontale Ausrichtung schwieriger zu lesen.

-   **Überprüfen Sie die Verwendung von Gruppen Feldern, um Gruppen von Options Feldern zu organisieren**– Dies führt häufig zu unnötiger Bildschirm Übersichtlichkeit.
-   **Verwenden Sie keine Optionsfeld Bezeichnungen als Gruppenfeld Bezeichnungen.**
-   **Verwenden Sie die Auswahl einer Options Schaltfläche nicht für Folgendes:**
    -   Ausführen von Befehlen.
    -   Zeigen Sie andere Fenster an, z. b. ein Dialogfeld, um weitere Eingaben zu erfassen.
    -   Dynamisches ein-oder Ausblenden anderer Steuerelemente, die mit dem ausgewählten Steuerelement verknüpft sind (Sprachausgabe können solche Ereignisse nicht erkennen). Sie können den Text jedoch dynamisch basierend auf der Auswahl ändern.

### <a name="subordinate-controls"></a>Untergeordnete Steuerelemente

-   Platzieren Sie untergeordnete Steuerelemente rechts von oder unten (eingerückt, mit der Optionsfeld Bezeichnung) mit dem Optionsfeld und der zugehörigen Bezeichnung. Beenden Sie die Bezeichnung für das Optionsfeld mit einem Doppelpunkt.

    ![Screenshot des Steuer Elements auf der rechten Seite der Bezeichnung ](images/radio-buttons-image9.png)

    In diesem Beispiel geben das Optionsfeld und das untergeordnete Steuerelement die Optionsfeld Bezeichnung und deren Zugriffstaste frei. In diesem Fall verschieben die Pfeiltasten den Fokus von der Options Schaltfläche auf das untergeordnete Textfeld.

-   **Lassen Sie abhängige, bearbeitbare Textfelder und Dropdown Listen aktiviert, wenn Sie die Bezeichnung des Options Felds freigeben.** Wenn Benutzer Elemente eingeben oder in das Feld einfügen, wählen Sie die entsprechende Option automatisch aus. Dies vereinfacht die Interaktion.

    ![Screenshot des Dialog Felds "Seitenbereich" mit Textfeld ](images/radio-buttons-image10.png)

    Wenn Sie in diesem Beispiel eine Seitenzahl eingeben, werden die Seiten automatisch ausgewählt.

-   **Vermeiden Sie die Schachtelung von Options Feldern mit anderen Options Feldern oder Kontrollkästchen.** Behalten Sie, wenn möglich, alle Optionen auf derselben Ebene bei.

    **Richtig:**

    ![Screenshot der linksbündig ausgerichteten Options Felder ](images/radio-buttons-image11.png)

    In diesem Beispiel befinden sich die Optionen auf derselben Ebene.

    **Falsch:**

    ![Screenshot der Schaltfläche "Schaltflächen" ](images/radio-buttons-image12.png)

    In diesem Beispiel fügt die Verwendung von Optionen für die Verwendung von Optionen unnötige Komplexität hinzu.

-   Wenn Sie Options Felder mit anderen Options Feldern oder Kontrollkästchen Schachteln, **Deaktivieren Sie diese untergeordneten Steuerelemente, bis die Option auf hoher Ebene ausgewählt ist.** Dadurch wird Verwirrung in Bezug auf die Bedeutung der untergeordneten Steuerelemente vermieden.

### <a name="default-values"></a>Standardwerte

-   Da eine Gruppe von Options Feldern eine Reihe von sich gegenseitig ausschließenden Optionen darstellt, ist **standardmäßig immer ein Optionsfeld ausgewählt. Wählen Sie das sicherste (zum Verhindern von Datenverlust oder System Zugriff) und die sicherste und private Option aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequeme Option aus.
-   **Ausnahmen:** Keine Standardauswahl, wenn:
    -   **Es gibt keine akzeptable Standardoption für Sicherheit, Sicherheit oder rechtliche Gründe. Daher muss der Benutzer eine explizite Auswahl treffen.** Wenn der Benutzer keine Auswahl treffen soll, zeigen Sie eine Fehlermeldung an, um eine zu erzwingen.
    -   **Die Benutzeroberfläche (UI) muss den aktuellen Status widerspiegeln, und die Option wurde noch nicht festgelegt.** Ein Standardwert impliziert fälschlicherweise, dass der Benutzer keine Auswahl treffen muss.
    -   **Ziel ist es, unausgewogene Daten zu erfassen.** Der Standardwert ist die Datensammlung.
    -   **Die Gruppe der Options Felder stellt eine Eigenschaft in einem gemischten Zustand dar**. Dies geschieht, wenn eine Eigenschaft für mehrere Objekte angezeigt wird, die nicht die gleiche Einstellung aufweisen. Zeigen Sie in diesem Fall keine Fehlermeldung an, da jedes Objekt einen gültigen Status aufweist.
-   **Legen Sie die erste Option als Standardoption** fest, da Benutzer häufig diese – erwarten, es sei denn, diese Reihenfolge ist logisch. Zu diesem Zweck müssen Sie möglicherweise die Options Bezeichnungen ändern.

    **Falsch:**

    ![Screenshot des letzten Options Felds als Standardoption ](images/radio-buttons-image13.png)

    In diesem Beispiel ist die Standardoption nicht die erste Option.

    **Richtig:**

    ![Screenshot des ersten Options Felds als Standard ](images/radio-buttons-image14.png)

    In diesem Beispiel werden die Options Bezeichnungen neu formuliert, um die erste Option als Standardoption zu aktivieren.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstände

![Screenshot der Optionsfeld Größe und des Abstands ](images/radio-buttons-image15.png)

Empfohlene Größe und Abstände für options Felder.

## <a name="labels"></a>Bezeichnungen

### <a name="radio-button-labels"></a>Optionsfeld Bezeichnungen

-   Bezeichnen Sie jedes Optionsfeld.

<!-- -->

-   Weisen Sie jeder Bezeichnung einen eindeutigen [Zugriffsschlüssel](glossary.md) zu. Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   Schreiben Sie die Bezeichnung als Ausdruck und nicht als Satz, und verwenden Sie keine endinterpunktions Zeichen.
    -   **Ausnahme:** Wenn eine Optionsfeld Bezeichnung auch ein untergeordnetes Steuerelement bezeichnet, das darauf folgt, beenden Sie die Bezeichnung mit einem Doppelpunkt.
-   Verwenden Sie parallele Ausdrücke, und versuchen Sie, die Länge für alle Bezeichnungen gleich zu halten.
-   Fokussieren Sie den Bezeichnungs Text auf die Unterschiede zwischen den Optionen. Wenn alle Optionen denselben einführenden Text aufweisen, verschieben Sie diesen Text in die Gruppen Bezeichnung.
-   Verwenden Sie einen positiven Ausdruck. Verwenden Sie z. b. do anstelle of do not, und Print anstelle von nicht drucken.
-   Beschreiben Sie nur die Option mit der Bezeichnung. Halten Sie Bezeichnungen kurz, damit Sie in Nachrichten und Dokumentationen leicht darauf verweisen können. Wenn die Option eine weitere Erläuterung erfordert, stellen Sie die Erläuterung in einem [statischen Text](glossary.md) Steuerelement mithilfe von vollständigen Sätzen und endinterpunktions Zeichen bereit.

    ![Screenshot der Options Felder mit erklärendem Text](images/radio-buttons-image16.png)

    In diesem Beispiel werden die Optionen mithilfe separater statischer Text Steuerelemente erläutert.

    > [!Note]  
    > Das Hinzufügen einer Erläuterung zu einem Optionsfeld bedeutet nicht, dass Sie Erklärungen für alle Options Felder angeben müssen. Geben Sie die relevanten Informationen in der Bezeichnung an, wenn dies möglich ist, und verwenden Sie nur bei Bedarf Erklärungen. Geben Sie die Bezeichnung nicht nur auf Konsistenz zurück.

     

-   **Wenn eine Option dringend empfohlen wird, fügen Sie "(empfohlen)" der Bezeichnung hinzu.** Stellen Sie sicher, dass Sie der Steuerelement Bezeichnung und nicht den ergänzenden Notizen hinzufügen.
-   **Wenn eine Option nur für fortgeschrittene Benutzer vorgesehen ist, fügen Sie der Bezeichnung "(erweitert)" hinzu.** Stellen Sie sicher, dass Sie der Steuerelement Bezeichnung und nicht den ergänzenden Notizen hinzufügen.
-   Wenn Sie mehrzeilige Bezeichnungen verwenden müssen, richten Sie den oberen Rand der Bezeichnung mit dem Optionsfeld aus.
-   Verwenden Sie kein untergeordnetes Steuerelement, die darin enthaltenen Werte oder die zugehörige Einheiten Bezeichnung, um einen Satz oder einen Ausdruck zu erstellen. Ein solcher Entwurf ist nicht lokalisierbar, da die Satzstruktur von der Sprache abweicht.

### <a name="radio-button-group-labels"></a>Optionsfeld-Gruppen Bezeichnungen

-   Verwenden Sie die Gruppen Bezeichnung, um den Zweck der Gruppe zu erläutern, nicht, wie Sie die Auswahl treffen möchten. Angenommen, die Benutzer wissen, wie Options Felder verwendet werden. Nehmen Sie beispielsweise an, dass Sie eine der folgenden Optionen auswählen.
-   Alle Optionsfeld Gruppen benötigen Bezeichnungen. Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz, und beenden Sie mit einem Doppelpunkt mithilfe von statischem Text oder einem Gruppenfeld.

    **Ausnahme:** Lassen Sie die Bezeichnung aus, wenn es sich lediglich um eine erneute Anweisung der [Haupt Anweisung](glossary.md)eines Dialog Felds handelt. In diesem Fall nimmt die main-Anweisung den Doppelpunkt (es sei denn, es handelt sich um eine Frage) und die Zugriffstaste (sofern vorhanden).

    **Annehmbar:**

    ![Screenshot der redundanten Optionsfeld-Gruppen Bezeichnung ](images/radio-buttons-image17.png)

    In diesem Beispiel ist die Optionsfeld-Gruppen Bezeichnung lediglich eine erneute Anweisung der Main-Anweisung.

    **Besserer**

    ![Screenshot der Optionsfeld-Haupt Anweisung ](images/radio-buttons-image18.png)

    In diesem Beispiel wird die redundante Bezeichnung entfernt, sodass die Haupt Anweisung den Doppelpunkt annimmt.

-   Weisen Sie der Bezeichnung keinen Zugriffsschlüssel zu. Dies ist nicht erforderlich, sodass die Zuweisung der anderen Zugriffsschlüssel erschwert wird.
    -   **Ausnahme:** Wenn nicht alle Steuerelemente über eindeutige Zugriffstasten verfügen können, können Sie der Bezeichnung anstelle der einzelnen Steuerelemente einen Zugriffsschlüssel zuweisen. Weitere Informationen finden Sie unter [Tastatur](inter-keyboard.md).

## <a name="documentation"></a>Dokumentation

Wenn Sie auf Options Felder verweisen:

-   Verwenden Sie den genauen Bezeichnungs Text, einschließlich der Groß-und Kleinschreibung, aber nicht den Unterstrich oder Doppelpunkt des Zugriffsschlüssels.
-   Informationen zum Programmieren und zur anderen technischen Dokumentation finden Sie unter Options Felder als Options Felder. Überall sonst verwenden Sie Options Schaltflächen, insbesondere in der Benutzerdokumentation.
-   Um die Benutzerinteraktion zu beschreiben, verwenden Sie klicken.
-   Formatieren Sie nach Möglichkeit die Bezeichnung mit fettem Text. Andernfalls sollten Sie die Bezeichnung nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Klicken Sie auf **aktuelle Seite**, und klicken Sie dann auf **OK**.

 

 