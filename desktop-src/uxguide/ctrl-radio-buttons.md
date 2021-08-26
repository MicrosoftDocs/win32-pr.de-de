---
title: Optionsfelder
description: Mit einem Optionsfeld treffen Benutzer eine Auswahl aus einer Reihe von sich gegenseitig ausschließenden, verwandten Optionen.
ms.assetid: f9af0a8a-d4a1-464c-a967-bab88ae0726b
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: cbe870e1c1900de29dda515fd2142b951886929af46e69b4fea3fc6644e6f8fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934521"
---
# <a name="radio-buttons"></a>Optionsfelder

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Mit einem Optionsfeld treffen Benutzer eine Auswahl aus einer Reihe von sich gegenseitig ausschließenden, verwandten Optionen. Benutzer können eine und nur eine Option auswählen. Optionsfelder werden so genannt, da sie wie die Kanalvoreinstellungen auf Radios funktionieren.

![Screenshot von drei Optionsfeldern ](images/radio-buttons-image1.png)

Eine typische Gruppe von Optionsfeldern.

Eine Gruppe von Optionsfeldern verhält sich wie ein einzelnes Steuerelement. Nur auf die ausgewählte Auswahl kann über die TAB-TASTE zugegriffen werden, aber Benutzer können die Gruppe mithilfe der Pfeiltasten durchraden.

> [!Note]  
> Richtlinien im Zusammenhang [mit Layout](vis-layout.md) [und Tastaturnavigation](inter-keyboard.md) werden in einem separaten Artikel vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Wird das Steuerelement verwendet, um eine Option aus einer Reihe von Optionen zu wählen, die sich gegenseitig ausschließen?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Um mehrere Optionen zu wählen, [](ctrl-list-boxes.md) verwenden Sie [stattdessen Kontrollkästchen,](ctrl-check-boxes.md)eine Mehrfachauswahlliste oder eine Kontrollkästchenliste.
-   **Liegt die Anzahl der Optionen zwischen zwei und sieben?** Da der verwendete Bildschirmbereich proportional zur Anzahl der Optionen ist, behalten Sie die Anzahl der Optionen in einer Gruppe zwischen zwei und sieben bei. Verwenden Sie für acht oder mehr Optionen eine [Dropdownliste oder](/windows/desktop/uxguide/ctrl-drop) [eine Einzelauswahlliste.](ctrl-list-boxes.md)
-   **Wäre ein Kontrollkästchen die bessere Wahl?** Wenn nur zwei Optionen verfügbar sind, können Sie stattdessen ein [einzelnes Kontrollkästchen](ctrl-check-boxes.md) verwenden. Kontrollkästchen eignen sich jedoch nur zum Aktivieren oder Deaktivieren einer einzelnen Option, während Optionsfelder für völlig andere Alternativen verwendet werden können. Wenn beide Lösungen möglich sind:
    -   Verwenden Sie Optionsfelder, wenn die Bedeutung des Kontrollkästchens nicht ganz offensichtlich ist.

        **Falsch:**

        ![Screenshot des Kontrollkästchens "Querformat" ](images/radio-buttons-image2.png)

        **Richtig:**

        ![Screenshot der Optionsfelder für Querformat/Hochformat ](images/radio-buttons-image3.png)

        Im richtigen Beispiel sind die Optionen keine Gegensätze, daher sind Optionsfelder die bessere Wahl.

    -   Verwenden Sie Optionsfelder auf Assistentenseiten, um die Alternativen zu löschen, auch wenn ein Kontrollkästchen andernfalls akzeptabel ist.
    -   Verwenden Sie Optionsfelder, wenn genügend Bildschirmbereich vorhanden ist und die Optionen wichtig genug sind, um diesen Bildschirmbereich zu nutzen. Verwenden Sie andernfalls ein Kontrollkästchen oder eine Dropdownliste.

        **Falsch:**

        ![Screenshot der Optionsfelder "Show"/"Don't show" ](images/radio-buttons-image4.png)

        In diesem Beispiel sind die Optionen nicht wichtig genug, um Optionsfelder zu verwenden.

        **Richtig:**

        ![Screenshot des Kontrollkästchens "Diese Meldung nicht anzeigen" ](images/radio-buttons-image5.png)

        In diesem Beispiel ist ein Kontrollkästchen eine effiziente Verwendung des Bildschirmbereichs für diese Peripherieoption.

    -   Verwenden Sie ein Kontrollkästchen, wenn auf der Seite andere Kontrollkästchen angezeigt werden.

-   **Wäre eine Dropdownliste die bessere Wahl?** Wenn die Standardoption für die meisten Benutzer in den meisten Situationen empfohlen wird, können Optionsfelder mehr Aufmerksamkeit auf die Optionen als nötig ziehen.
    -   Ziehen Sie die Verwendung einer Dropdownliste in Betracht, wenn Sie nicht auf die Optionen aufmerksam machen möchten oder Benutzer nicht dazu ermutigen möchten, Änderungen vorzunehmen. Eine Dropdownliste konzentriert sich auf die aktuelle Auswahl, während Optionsfelder alle Optionen gleichermaßen hervorheben.

        ![Screenshot der höchsten Qualität als Standardschaltfläche ](images/radio-buttons-image6.png)

        In diesem Beispiel konzentriert sich eine Dropdownliste auf die aktuelle Auswahl und rät Benutzer davon ab, Änderungen vorzunehmen.

    -   Ziehen Sie eine Dropdownliste in Betracht, wenn auf der Seite andere Dropdownlisten angezeigt werden.

-   **Wäre ein Satz von Befehlsschaltflächen, Befehlslinks oder eine geteilte Schaltfläche die bessere Wahl?** Wenn die Optionsfelder nur verwendet werden, um die Art und Weise zu beeinflussen, wie ein Befehl ausgeführt wird, ist es häufig besser, stattdessen die Befehlsvariationen zu präsentieren. Auf diese Weise können Benutzer den richtigen Befehl mit einer einzigen Interaktion auswählen.
-   **Stellen die Optionen Programmoptionen anstelle von Daten vor?** Die Werte der Optionen sollten nicht auf Kontext oder anderen Daten basieren. Verwenden Sie für Daten eine Dropdownliste oder eine Einzelauswahlliste.
-   Wenn das Steuerelement auf einer Assistentenseite oder Systemsteuerung verwendet wird, ist das Steuerelement eine Antwort auf die Hauptanweisung, und können Benutzer **die Auswahl später ändern?** Falls ja, sollten Sie Befehlslinks anstelle von Optionsfeldern verwenden, um die Interaktion effizienter zu gestalten.
-   **Sind die Werte nicht numerisch?** Verwenden Sie für numerische Daten [Textfelder,](ctrl-text-boxes.md) [Dropdownlisten](/windows/desktop/uxguide/ctrl-drop)oder [Schieberegler](ctrl-sliders.md).

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Listen Sie die Optionen in einer logischen** Reihenfolge auf, z. B. mit der wahrscheinlichsten Auswahl auf den geringsten, einfachsten bis komplexen Vorgang oder dem geringsten Risiko für die meisten. Die alphabetische Sortierung wird nicht empfohlen, da sie sprachabhängig und daher nicht lokalisierbar ist.
-   **Wenn keine der Optionen eine gültige Option ist,** fügen Sie eine weitere Option hinzu, um diese Auswahl zu übernehmen, z. B. Keine oder Nicht angewendet.
-   **Richten Sie Optionsfelder lieber vertikal statt horizontal aus.** Die horizontale Ausrichtung ist schwieriger zu lesen und zu lokalisieren.

    **Richtig:**

    ![Screenshot der vertikalen Ausrichtung des Optionsfelds ](images/radio-buttons-image7.png)

    In diesem Beispiel werden die Optionsfelder vertikal ausgerichtet.

    **Falsch:**

    ![Screenshot der horizontalen Optionsfeldausrichtung ](images/radio-buttons-image8.png)

    In diesem Beispiel ist die horizontale Ausrichtung schwieriger zu lesen.

-   **Die Verwendung von Gruppenfeldern zum Organisieren von Gruppen von Optionsfeldern** wird neu organisiert. Dies führt häufig zu unnötigem Unübersichtlichkeitsbildschirm.
-   **Verwenden Sie keine Optionsfeldbezeichnungen als Gruppenfeldbezeichnungen.**
-   **Verwenden Sie die Auswahl eines Optionsfelds nicht für:**
    -   Führen Sie Befehle aus.
    -   Zeigen Sie andere Fenster an, z. B. ein Dialogfeld, um weitere Eingaben zu erfassen.
    -   Andere Steuerelemente im Zusammenhang mit dem ausgewählten Steuerelement dynamisch ein- oder ausblenden (Sprachlesegeräte können solche Ereignisse nicht erkennen). Sie können Text jedoch basierend auf der Auswahl dynamisch ändern.

### <a name="subordinate-controls"></a>Untergeordnete Steuerelemente

-   Platzieren Sie untergeordnete Steuerelemente rechts neben oder unter (eingezogen, leeren Sie mit der Optionsfeldbezeichnung) das Optionsfeld und dessen Bezeichnung. Beenden Sie die Optionsfeldbezeichnung mit einem Doppelpunkt.

    ![Screenshot des Steuerelements rechts von der Bezeichnung ](images/radio-buttons-image9.png)

    In diesem Beispiel teilen sich das Optionsfeld und das untergeordnete Steuerelement die Bezeichnung des Optionsfelds und dessen Zugriffsschlüssel. In diesem Fall verschieben die Pfeiltasten den Fokus vom Optionsfeld in das untergeordnete Textfeld.

-   **Lassen Sie abhängige bearbeitbare Textfelder und Dropdownlisten aktiviert, wenn sie die Bezeichnung des Optionsfelds gemeinsam verwenden.** Wenn Benutzer etwas eingeben oder in das Feld einfügen, wählen Sie automatisch die entsprechende Option aus. Dadurch wird die Interaktion vereinfacht.

    ![Screenshot des Dialogfelds "Seitenbereich" mit Textfeld ](images/radio-buttons-image10.png)

    In diesem Beispiel wählt die Eingabe einer Seitenzahl automatisch Pages aus.

-   **Vermeiden Sie das Schachteln von Optionsfeldern mit anderen Optionsfeldern oder Kontrollkästchen.** Behalten Sie nach Möglichkeit alle Optionen auf der gleichen Ebene bei.

    **Richtig:**

    ![Screenshot von linksbündig ausgerichteten Optionsfeldern ](images/radio-buttons-image11.png)

    In diesem Beispiel befinden sich die Optionen auf der gleichen Ebene.

    **Falsch:**

    ![Screenshot geschachtelter Optionsfelder ](images/radio-buttons-image12.png)

    In diesem Beispiel erhöht die Verwendung von geschachtelten Optionen die unnötige Komplexität.

-   Wenn Sie Optionsfelder mit anderen Optionsfeldern oder Kontrollkästchen schachteln, deaktivieren Sie diese untergeordneten Steuerelemente, bis die Option auf **hoher Ebene ausgewählt ist.** Dies vermeidet Verwirrung über die Bedeutung der untergeordneten Steuerelemente.

### <a name="default-values"></a>Standardwerte

-   Da eine Gruppe von Optionsfeldern eine Reihe von sich gegenseitig ausschließenden Optionen darstellt, **muss standardmäßig immer ein Optionsfeld ausgewählt sein. Wählen Sie die sicherste (um Daten- oder Systemzugriffsverluste zu verhindern) und** die sicherste und private Option aus. Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequemste Option aus.
-   **Ausnahmen:** Sie haben keine Standardauswahl, wenn:
    -   **Es gibt keine akzeptable Standardoption aus Sicherheits-, Sicherheits- oder rechtlichen Gründen, weshalb der Benutzer eine explizite Auswahl treffen muss.** Wenn der Benutzer keine Auswahl getroffen hat, zeigen Sie eine Fehlermeldung an, um eine zu erzwingen.
    -   **Die Benutzeroberfläche muss den aktuellen Zustand widerspiegeln, und die Option wurde noch nicht festgelegt.** Ein Standardwert impliziert fälschlicherweise, dass der Benutzer keine Auswahl treffen muss.
    -   **Ziel ist es, unvoreingenommene Daten zu sammeln.** Standardwerte würden die Datensammlung verzerren.
    -   **Die Gruppe von Optionsfeldern stellt eine Eigenschaft in einem gemischten Zustand dar. Dies** geschieht, wenn eine Eigenschaft für mehrere Objekte angezeigt wird, die nicht über die gleiche Einstellung verfügen. Zeigen Sie in diesem Fall keine Fehlermeldung an, da jedes Objekt einen gültigen Zustand aufweist.
-   **Machen Sie die erste Option zur Standardoption**, da Benutzer dies häufig erwarten, es sei denn, diese Reihenfolge ist nicht logisch. Dazu müssen Sie möglicherweise die Optionsbezeichnungen ändern.

    **Falsch:**

    ![Screenshot des letzten Optionsfelds als Standardoption ](images/radio-buttons-image13.png)

    In diesem Beispiel ist die Standardoption nicht die erste Option.

    **Richtig:**

    ![Screenshot des ersten Optionsfelds als Standard ](images/radio-buttons-image14.png)

    In diesem Beispiel werden die Optionsbezeichnungen so umformuliert, dass die erste Option zur Standardoption wird.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größen- und Abstände

![Screenshot der Größen- und Abstände von Optionsfeldern ](images/radio-buttons-image15.png)

Empfohlene Größen- und Abstandstasten für Optionsfelder.

## <a name="labels"></a>Bezeichnungen

### <a name="radio-button-labels"></a>Optionsfeldbezeichnungen

-   Beschriften Sie jedes Optionsfeld.

<!-- -->

-   Weisen Sie jeder Bezeichnung einen eindeutigen [Zugriffsschlüssel](glossary.md) zu. Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).
-   Verwenden Sie [die Groß-/Großschreibung im Satzformat.](glossary.md)
-   Schreiben Sie die Bezeichnung als Ausdruck, nicht als Satz, und verwenden Sie keine endende Interpunktion.
    -   **Ausnahme:** Wenn eine Optionsfeldbezeichnung auch ein untergeordnetes Steuerelement bezeichnet, das darauf folgt, beenden Sie die Bezeichnung mit einem Doppelpunkt.
-   Verwenden Sie parallele Ausdrücke, und versuchen Sie, die Länge für alle Bezeichnungen ungefähr gleich zu halten.
-   Konzentrieren Sie den Bezeichnungstext auf die Unterschiede zwischen den Optionen. Wenn alle Optionen denselben einführenden Text aufweisen, verschieben Sie diesen Text in die Gruppenbezeichnung.
-   Verwenden Sie positive Ausdrücke. Verwenden Sie z. B. do anstelle von do not, und drucken Sie anstelle von nicht drucken.
-   Beschreiben Sie nur die Option mit der Bezeichnung . Halten Sie Bezeichnungen kurz, damit Sie in Nachrichten und Dokumentationen leicht darauf verweisen können. Wenn die Option eine weitere Erläuterung erfordert, geben Sie die Erklärung in einem [statischen Textsteuerelement](glossary.md) mit vollständigen Sätzen und endender Interpunktion an.

    ![Screenshot von Optionsfeldern mit erläuterndem Text](images/radio-buttons-image16.png)

    In diesem Beispiel werden die Optionen mit separaten statischen Textsteuerelementen erläutert.

    > [!Note]  
    > Das Hinzufügen einer Erklärung zu einem Optionsfeld bedeutet nicht, dass Sie Erklärungen für alle Optionsfelder bereitstellen müssen. Geben Sie ggf. die relevanten Informationen in der Bezeichnung an, und verwenden Sie Erklärungen nur bei Bedarf. Geben Sie die Bezeichnung nicht nur aus Konsistenzgründen neu an.

     

-   **Wenn eine Option dringend empfohlen wird, fügen Sie der Bezeichnung "(empfohlen)" hinzu.** Achten Sie darauf, der Steuerelementbezeichnung und nicht den zusätzlichen Hinweisen hinzuzufügen.
-   **Wenn eine Option nur für fortgeschrittene Benutzer vorgesehen ist, fügen Sie der Bezeichnung "(advanced)" hinzu.** Achten Sie darauf, der Steuerelementbezeichnung und nicht den zusätzlichen Hinweisen hinzuzufügen.
-   Wenn Sie mehrzeilige Bezeichnungen verwenden müssen, richten Sie den oberen Rand der Bezeichnung mit dem Optionsfeld aus.
-   Verwenden Sie kein untergeordnetes Steuerelement, die darin enthaltenen Werte oder seine Einheitenbezeichnung, um einen Satz oder Ausdruck zu erstellen. Ein solches Design ist nicht lokalisierbar, da die Satzstruktur je nach Sprache variiert.

### <a name="radio-button-group-labels"></a>Optionsfeldgruppenbezeichnungen

-   Verwenden Sie die Gruppenbezeichnung, um den Zweck der Gruppe zu erläutern, und nicht, wie Sie die Auswahl treffen. Angenommen, Benutzer wissen, wie Optionsfelder verwendet werden. Sagen Sie beispielsweise nicht "Wählen Sie eine der folgenden Optionen aus".
-   Alle Optionsfeldgruppen benötigen Bezeichnungen. Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz, und enden Sie mit einem Doppelpunkt mit statischem Text oder einem Gruppenfeld.

    **Ausnahme:** Lassen Sie die Bezeichnung aus, wenn es sich lediglich um eine Neuanordnung der [Hauptanweisung](glossary.md)eines Dialogfelds handelt. In diesem Fall nimmt die Hauptanweisung den Doppelpunkt (sofern es sich nicht um eine Frage handelt) und den Zugriffsschlüssel (sofern vorhanden).

    **Annehmbar:**

    ![Screenshot der redundanten Optionsfeldgruppenbezeichnung ](images/radio-buttons-image17.png)

    In diesem Beispiel ist die Optionsfeldgruppenbezeichnung nur eine Neuanordnung der Hauptanweisung.

    **Besser:**

    ![Screenshot der Hauptanweisung des Optionsfelds ](images/radio-buttons-image18.png)

    In diesem Beispiel wird die redundante Bezeichnung entfernt, sodass die Main-Anweisung den Doppelpunkt annimmt.

-   Weisen Sie der Bezeichnung keinen Zugriffsschlüssel zu. Dies ist nicht erforderlich und erschwert die Zuweisung der anderen Zugriffsschlüssel.
    -   **Ausnahme:** Wenn nicht alle Steuerelemente eindeutige Zugriffsschlüssel haben können, können Sie der Bezeichnung anstelle der einzelnen Steuerelemente einen Zugriffsschlüssel zuweisen. Weitere Informationen finden Sie unter [Tastatur](inter-keyboard.md).

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Optionsfelder:

-   Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Großschreibung, aber nicht den Unterstrich oder Doppelpunkt des Zugriffsschlüssels.
-   In der Programmierung und anderen technischen Dokumentationen werden Optionsfelder als Optionsfelder bezeichnet. Überall andernfalls werden Optionsschaltflächen verwendet, insbesondere in der Benutzerdokumentation.
-   Um die Benutzerinteraktion zu beschreiben, klicken Sie auf .
-   Formatieren Sie die Bezeichnung nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

Beispiel: Klicken Sie auf **aktuelle Seite**, und klicken Sie dann auf **OK**.

 

 