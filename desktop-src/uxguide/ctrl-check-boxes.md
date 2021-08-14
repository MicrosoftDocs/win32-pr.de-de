---
title: Kontrollkästchen
description: Mit einem Kontrollkästchen treffen Benutzer eine Entscheidung zwischen zwei eindeutig entgegengesetzten Optionen.
ms.assetid: 7c39987d-807b-41c1-9788-65c3d468b976
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 29666991d0a0659f7ff3a95f12953504b70c6dc782049ac8d93d70df73afa5d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118040611"
---
# <a name="check-boxes"></a>Kontrollkästchen

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Mit einem Kontrollkästchen treffen Benutzer eine Entscheidung zwischen zwei eindeutig entgegengesetzten Optionen. Die Kontrollkästchenbezeichnung gibt den ausgewählten Zustand an, während die Bedeutung des zustandsbecheckten Zustands das eindeutige Gegenteil des ausgewählten Zustands sein muss. Daher sollten Kontrollkästchen nur zum Aktivieren oder Deaktivieren einer Option oder zum Auswählen oder Deaktivieren **eines Elements verwendet werden.**

![Screenshot eines von vier ausgewählten Kontrollkästchen ](images/ctrl-check-boxes-image1.png)

Eine typische Gruppe von Kontrollkästchen.

> [!Note]  
> Richtlinien zum [Layout werden](vis-layout.md) in einem separaten Artikel vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Wird das Kontrollkästchen zum Aktivieren oder Deaktivieren einer Option oder zum Auswählen oder Deaktivieren eines Elements verwendet?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement.
-   **Sind die ausgewählten und cleared-Zustände klare und eindeutige Gegensätze?** Wenn dies nicht der Fall ist, verwenden Sie [Optionsfelder](ctrl-radio-buttons.md) oder eine [Dropdownliste,](/windows/desktop/uxguide/ctrl-drop) damit Sie die Zustände unabhängig voneinander beschriften können.
-   **Umfasst die Gruppe bei Verwendung in einer Gruppe unabhängige Auswahlmöglichkeiten, aus denen Benutzer null oder mehr auswählen können?** Falls nicht, sollten Sie Steuerelemente für abhängige Optionen in Betracht ziehen, z. B. Optionsfelder und [Kontrollkästchenstrukturansichten.](ctrl-tree-views.md)
-   **Umfasst die Gruppe bei Verwendung in einer Gruppe abhängige Auswahlmöglichkeiten, aus denen Benutzer eine oder mehrere auswählen müssen?** Wenn ja, verwenden Sie eine Gruppe von Kontrollkästchen, und behandeln Sie den Fehler, wenn keine der Optionen ausgewählt ist.
-   **Ist die Anzahl der Optionen in einer Gruppe 10 oder weniger?** Da der verwendete Bildschirmbereich proportional zur Anzahl der Optionen ist, sollten Sie die Anzahl der Kontrollkästchen auf 10 oder weniger festlegen. Verwenden Sie für mehr als 10 Optionen eine [Kontrollkästchenliste.](ctrl-list-boxes.md)
-   **Wäre ein Optionsfeld die bessere Wahl?** Wenn Kontrollkästchen nur zum Aktivieren oder Deaktivieren einer Option geeignet sind, können Optionsfelder für völlig unterschiedliche Optionen verwendet werden. Wenn beide Lösungen möglich sind:
    -   Verwenden Sie Optionsfelder, wenn die Bedeutung des Kontrollkästchens nicht ganz offensichtlich ist.

        **Falsch:**

        ![Screenshot eines Kontrollkästchens mit der Bezeichnung "Querformat" ](images/ctrl-check-boxes-image2.png)

        In diesem Beispiel ist die entgegengesetzte Wahl von Querformat nicht klar, daher ist das Kontrollkästchen keine gute Wahl.

        **Richtig:**

        ![Screenshot von zwei Optionsfeldern ](images/ctrl-check-boxes-image3.png)

        In diesem Beispiel sind die Optionen keine Gegensätze, daher sind Optionsfelder die bessere Wahl.

    -   Verwenden Sie Optionsfelder auf Assistentenseiten, um die Alternativen zu löschen, auch wenn ein Kontrollkästchen andernfalls akzeptabel ist.
    -   Verwenden Sie Optionsfelder, wenn genügend Bildschirmbereich vorhanden ist und die Optionen wichtig genug sind, um diesen Bildschirmbereich zu nutzen. Verwenden Sie andernfalls ein Kontrollkästchen oder eine Dropdownliste.

        **Falsch:**

        ![Screenshot der Schaltflächen "Show" und "Verhältnis nicht anzeigen" ](images/ctrl-check-boxes-image4.png)

        In diesem Beispiel sind die Optionen nicht wichtig genug, um Optionsfelder zu verwenden.

        **Richtig:**

        ![Screenshot des Kontrollkästchens ohne Meldung ](images/ctrl-check-boxes-image5.png)

        In diesem Beispiel ist ein Kontrollkästchen eine effiziente Verwendung des Bildschirmbereichs für diese Peripherieoption.

-   Verwenden Sie ein Kontrollkästchen, wenn im Fenster andere Kontrollkästchen angezeigt werden.
-   **Stellt die Option anstelle von Daten eine Programmoption dar?** Die Werte der Option sollten nicht auf Kontext oder anderen Daten basieren. Verwenden Sie für Daten eine Kontrollkästchenliste oder [eine Mehrfachauswahlliste.](ctrl-list-boxes.md)

## <a name="usage-patterns"></a>Verwendungsmuster

Kontrollkästchen verfügen über mehrere Verwendungsmuster:



|    Verwendung                                                                          |         Beispiel                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Eine individuelle Auswahl** Ein einzelnes Kontrollkästchen wird verwendet, um eine einzelne Auswahl auszuwählen. <br/>                                                                                                             | ![Screenshot eines Kontrollkästchens mit Erinnere mich Bezeichnung ](images/ctrl-check-boxes-image6.png)<br/> Ein einzelnes Kontrollkästchen wird für eine einzelne Auswahl verwendet.<br/>                                                                                                                                                                                                                                                                                                                        |
| **Unabhängige Auswahlmöglichkeiten (null oder mehr)** Eine Gruppe von Kontrollkästchen wird verwendet, um aus einer Gruppe von 0 (null) oder mehr Optionen auszuwählen.<br/>                                                                              | Im Gegensatz zu Steuerelementen mit einzelner Auswahl, z. B. [Optionsfeldern,](ctrl-radio-buttons.md)können Benutzer eine beliebige Kombination von Optionen in einer Gruppe von Kontrollkästchen auswählen.<br/> ![Screenshot von zwei von drei aktivierten Kontrollkästchen ](images/ctrl-check-boxes-image7.png)<br/> Eine Gruppe von Kontrollkästchen wird für unabhängige Auswahlmöglichkeiten verwendet.<br/>                                                                                                                                                  |
| **Abhängige Auswahl (mindestens eine)** Eine Gruppe von Kontrollkästchen kann auch verwendet werden, um eine oder mehrere Auswahlmöglichkeiten auszuwählen.<br/>                                                                         | **Möglicherweise müssen Sie eine Auswahl einer oder mehrere abhängige Optionen darstellen.** Da microsoft?windows kein Steuerelement hat, das diese Art von Eingabe direkt unterstützt, empfiehlt es sich, eine Gruppe von Kontrollkästchen zu verwenden und den Fehler zu behandeln, wenn keine der Optionen ausgewählt ist.<br/> ![Screenshot eines von zwei aktivierten Kontrollkästchen ](images/ctrl-check-boxes-image8.png)<br/> Eine Gruppe von Kontrollkästchen wird verwendet, in der mindestens ein Protokoll ausgewählt werden muss.<br/> |
| **Gemischte Auswahl** Zusätzlich zu den ausgewählten und aktivierten Zuzuständen weisen Kontrollkästchen auch einen gemischten Zustand für die Mehrfachauswahl auf, um anzugeben, dass die Option für einige, aber nicht für alle Objekte festgelegt ist.<br/> | ![Screenshot eines vollblauen schreibgeschützten Kontrollkästchens ](images/ctrl-check-boxes-image9.png)<br/> Ein Kontrollkästchen mit gemischtem Zustand.<br/>                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Gruppenbezogene Kontrollkästchen.** Kombinieren Sie verwandte Optionen, und trennen Sie nicht verknüpfte Optionen in Gruppen von 10 oder weniger, und verwenden Sie bei Bedarf mehrere Gruppen.

    ![Screenshot verwandter und nicht verknüpfter Kontrollkästchen ](images/ctrl-check-boxes-image10.png)

    Ein Beispiel für Gruppen verwandter, unabhängiger Optionen.

-   **Die Neuordnung der Verwendung von Gruppenfeldern zum Organisieren von Gruppen von Kontrollkästchen** führt häufig zu unnötiger Bildschirmübersicht.
-   **Listen Sie Kontrollkästchen in einer logischen** Reihenfolge auf, z. B. gruppieren Sie hochgradig verwandte Optionen, platzieren Sie die gängigsten Optionen an erster Stelle, oder folgen Sie einem anderen natürlichen Fortschritt. Die alphabetische Sortierung wird nicht empfohlen, da sie sprachabhängig und daher nicht lokalisierbar ist.
-   **Kontrollkästchen vertikal ausrichten, nicht horizontal.** Die horizontale Ausrichtung ist schwieriger zu lesen.

    **Richtig:**

    ![Screenshot der vertikal ausgerichteten Kontrollkästchen ](images/ctrl-check-boxes-image11.png)

    In diesem Beispiel sind die Kontrollkästchen ordnungsgemäß ausgerichtet.

    **Falsch:**

    ![Screenshot der horizontal ausgerichteten Kontrollkästchen ](images/ctrl-check-boxes-image12.png)

    In diesem Beispiel ist die horizontale Ausrichtung schwieriger zu lesen.

-   **Verwenden Sie nicht den gemischten Zustand, um einen dritten Zustand zu repräsentieren.** Der gemischte Zustand wird verwendet, um anzugeben, dass eine Option für einige, aber nicht für alle untergeordneten Objekte festgelegt ist. Benutzer sollten nicht direkt einen gemischten Zustand festlegen können, sondern der gemischte Zustand ist eine Reflektion der untergeordneten Objekte. Der gemischte Zustand wird nicht als dritter Zustand für ein einzelnes Element verwendet. Verwenden Sie stattdessen Optionsfelder oder eine Dropdownliste, um einen dritten Zustand zu repräsentieren.

    **Falsch:**

    ![Screenshot des Kontrollkästchens "Solid Blue Theme Service" ](images/ctrl-check-boxes-image13.png)

    In diesem Beispiel soll der gemischte Zustand angeben, dass der Designdienst nicht installiert ist.

    **Richtig:**

    ![Screenshot der Dropdownliste mit drei Optionen ](images/ctrl-check-boxes-image14.png)

    In diesem Beispiel können Benutzer aus einer Liste mit drei eindeutigen Optionen auswählen.

-   **Wenn Sie auf ein Kontrollkästchen für gemischten Zustand klicken, sollten alle ausgewählten, alle markierten und die ursprünglichen gemischten Zustände durcheinander geraden.** Aus Gründen der Nähe ist es wichtig, den ursprünglichen gemischten Zustand wiederherstellen zu können, da die Einstellungen für den Benutzer komplex oder unbekannt sein können. Andernfalls besteht die einzige Möglichkeit, den gemischten Zustand mit Sicherheit wiederherzustellen, darin, die Aufgabe abzubricht und von vorn zu beginnen.
-   **Verwenden Sie keine Kontrollkästchen als Statusanzeige.** Verwenden Sie [stattdessen ein Statusanzeige-Steuerelement.](progress-bars.md)

    **Falsch:**

    ![Screenshot von vier Kontrollkästchen mit Status ](images/ctrl-check-boxes-image15.png)

    In diesem Beispiel werden Kontrollkästchen fälschlicherweise als Statusanzeige verwendet.

    **Richtig:**

    ![Screenshot einer teilweise ausgefüllten Statusleiste ](images/ctrl-check-boxes-image16.png)

    Beispiel für eine typische Statusleiste.

-   **Deaktivierte Kontrollkästchen mit dem richtigen Auswahlzustand anzeigen.** Obwohl Benutzer sie nicht ändern können, vermitteln deaktivierte Kontrollkästchen Informationen, sodass sie mit den Ergebnissen konsistent sein sollten.

    **Falsch:**

    ![Screenshot eines von zwei abgeblendet dargestellten Kontrollkästchen ](images/ctrl-check-boxes-image17.png)

    In diesem Beispiel sollte die Option "Diesen Abschnitt immer laut lesen" deaktiviert werden, da der Abschnitt nicht gelesen wird, wenn die Option deaktiviert ist.

-   **Verwenden Sie die Auswahl eines Kontrollkästchens nicht für**:
    -   Führen Sie Befehle aus.
    -   Zeigen Sie andere Fenster an, z. B. ein Dialogfeld, um weitere Eingaben zu erfassen.
    -   Dynamisches Anzeigen anderer Steuerelemente im Zusammenhang mit dem ausgewählten Steuerelement (Sprachanzeigen können solche Ereignisse nicht erkennen).

### <a name="dont-show-this-item-again"></a>Nicht anzeigen <item> Wieder

-   **Erwägen Sie die Verwendung der Option Nicht mehr anzeigen, damit Benutzer ein wiederkehrendes Dialogfeld nur unterdrücken können, wenn es keine bessere <item> Alternative gibt.** Versuchen Sie, im Voraus zu ermitteln, ob Benutzer den Dialog wirklich benötigen. wenn sie dies tun, zeigen Sie immer den Dialog an, und wenn nicht, beseitigen Sie den Dialog.

Weitere Richtlinien und Beispiele finden Sie unter [Dialogfelder](win-dialog-box.md).

### <a name="subordinate-controls"></a>Untergeordnete Steuerelemente

-   Platzieren Sie untergeordnete Steuerelemente rechts neben oder unter (eingezogen, leeren Sie mit der Kontrollkästchenbezeichnung) das Kontrollkästchen und dessen Bezeichnung. Beenden Sie die Kontrollkästchenbezeichnung mit einem Doppelpunkt.

    ![Screenshot des Textfelds unterhalb der Kontrollkästchenbezeichnung ](images/ctrl-check-boxes-image18.png)

    In diesem Beispiel verwenden das Kontrollkästchen und das untergeordnete Steuerelement die Kontrollkästchenbezeichnung und den Zugriffsschlüssel gemeinsam.

-   **Lassen Sie abhängige bearbeitbare Textfelder und Dropdownlisten aktiviert, wenn sie die Bezeichnung des Kontrollkästchens gemeinsam verwenden.** Wenn Benutzer etwas eingeben oder in das Feld einfügen, wählen Sie automatisch die entsprechende Option aus. Dadurch wird die Interaktion vereinfacht.

    ![Screenshot von Kopf- und Fußzeilentextfeldern ](images/ctrl-check-boxes-image19.png)

    In diesem Beispiel wählt die Eingabe einer Kopf- oder Fußzeile automatisch die Option aus.

-   Wenn Sie Kontrollkästchen mit Optionsfeldern oder anderen Kontrollkästchen schachteln, deaktivieren Sie diese untergeordneten Steuerelemente, bis die **Option auf hoher Ebene ausgewählt ist.** Dies vermeidet Verwirrung über die Bedeutung der untergeordneten Steuerelemente.
-   Ordnen Sie untergeordnete Steuerelemente einem Kontrollkästchen zu, das mit dem Kontrollkästchen in der Registerkarten reihenfolge zusammenhängend ist.
-   **Wenn die Auswahl einer Option das Aktivieren untergeordneter Kontrollkästchen impliziert, aktivieren Sie diese Kontrollkästchen explizit, um die Beziehung zu löschen.**

    **Falsch:**

    ![Screenshot: ausgewählte Schaltfläche, aktivierte Kontrollkästchen ](images/ctrl-check-boxes-image20.png)

    In diesem Beispiel sind die untergeordneten Kontrollkästchen nicht aktiviert.

    **Richtig:**

    ![Screenshot: ausgewählte Schaltfläche, ausgewählte Kontrollkästchen ](images/ctrl-check-boxes-image21.png)

    In diesem Beispiel sind die untergeordneten Kontrollkästchen aktiviert, wodurch die Beziehung zur ausgewählten Option eindeutig wird.

-   **Verwenden Sie abhängige Kontrollkästchen, wenn die Alternativen unnötige Komplexität hinzufügen.** Kontrollkästchen sollten zwar unabhängige Optionen sein, aber manchmal erhöhen Alternativen wie Optionsfelder unnötige Komplexität.

    **Richtig:**

    ![Screenshot verwirrender Schaltflächen und Kontrollkästchen ](images/ctrl-check-boxes-image22.png)

    In diesem Beispiel ist die Verwendung von Optionsfeldern genau, führt jedoch zu unnötiger Komplexität.

    **Besser:**

    ![Screenshot der Kontrollkästchen ](images/ctrl-check-boxes-image23.png)

    In diesem Beispiel ist die Verwendung von Kontrollkästchen einfacher und ermöglicht es Benutzern, sich auf die Auswahl der gewünschten Optionen anstatt auf ihre komplexe Beziehung zu konzentrieren.

    **Wichtig: Wenden Sie diese Richtlinie nur in äußerst seltenen Fällen an,** wenn das Anzeigen der Abhängigkeiten zu einer erheblichen Komplexität führt, ohne mehr Klarheit zu schaffen. Im vorherigen Beispiel ist es unwahrscheinlich, dass Benutzer versuchen würden, sowohl superscript als auch subscript zu wählen. Wenn dies der Fall wäre, wäre es leicht zu verstehen, dass es sich um exklusive Optionen handelt.

### <a name="default-values"></a>Standardwerte

-   Wenn ein Kontrollkästchen für eine Benutzeroption vorgesehen ist, legen Sie den sichersten (um Datenverlust oder Systemzugriff zu verhindern) standardmäßig den sichersten und privaten **Zustand fest.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie den wahrscheinlichsten oder bequemsten Wert aus.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstand

![Abbildung der vorgeschlagenen Kontrollkästchen für Größe und Abstand ](images/ctrl-check-boxes-image24.png)

Empfohlene Größe und Abstand für Kontrollkästchen.

## <a name="labels"></a>Bezeichnungen

**Kontrollkästchenbezeichnungen**

-   Beschriften Sie jedes Kontrollkästchen.
-   Weisen Sie jeder [Bezeichnung einen eindeutigen](glossary.md) Zugriffsschlüssel zu. Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).
-   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md)
-   Schreiben Sie die Bezeichnung als Ausdruck oder imperativen Satz, und verwenden Sie keine endende Interpunktion.
    -   **Ausnahme:** Wenn eine Kontrollkästchenbezeichnung auch ein untergeordnetes Steuerelement bezeichnet, das darauf folgt, beenden Sie die Bezeichnung mit einem Doppelpunkt.
-   Schreiben Sie die Bezeichnung so, dass sie den ausgewählten Zustand des Kontrollkästchens beschreibt.
-   Verwenden Sie für eine Gruppe von Kontrollkästchen parallele Formulierungen, und versuchen Sie, die Länge für alle Bezeichnungen ungefähr gleich zu halten.
-   Bei einer Gruppe von Kontrollkästchen sollten Sie den Bezeichnungstext auf die Unterschiede zwischen den Optionen konzentrieren. Wenn alle Optionen denselben Einführungstext haben, verschieben Sie diesen Text in die Gruppenbezeichnung.
-   Verwenden Sie positive Formulierungen. Geben Sie eine Bezeichnung nicht so aus, dass das Aktivieren eines Kontrollkästchens bedeutet, keine Aktion durchzuführen.

    -   **Ausnahme: Zeigen Sie diese Kontrollkästchen <item> nicht** erneut an.

    **Falsch:**

    ![Screenshot der negativen Bezeichnung "turn off"](images/ctrl-check-boxes-image25.png)

    In diesem Beispiel verwendet die Option keinen positiven Ausdruck.

-   Beschreiben Sie nur die Option mit der Bezeichnung. Halten Sie Bezeichnungen kurz, damit sie einfach in Nachrichten und Dokumentationen darauf verweisen können. Wenn die Option eine weitere Erläuterung erfordert, geben Sie die Erklärung in einem statischen [Textsteuerfeld](./glossary.md) an, indem Sie vollständige Sätze und Satzzeichen beenden.

    > [!Note]
    >
    > Das Hinzufügen einer Erklärung zu einem Kontrollkästchen in einer Gruppe bedeutet nicht, dass Sie Erklärungen für alle Kontrollkästchen in der Gruppe bereitstellen müssen. Geben Sie nach Bedarf die relevanten Informationen in der Bezeichnung an, und verwenden Sie Erklärungen nur bei Bedarf. Geben Sie die Bezeichnung nicht nur aus Konsistenz- und Konsistenz- heiterkeits-heiterkeit neu.

     

    ![Screenshot von Kontrollkästchen, Bezeichnung und Beschreibung ](images/ctrl-check-boxes-image26.png)

    In diesem Beispiel enthält eine Kontrollkästchenbezeichnung zusätzlichen erläuternden Text darunter.

-   Wenn eine Option dringend empfohlen wird, sollten Sie der Bezeichnung "(recommended)" hinzufügen. Achten Sie darauf, der Steuerelementbezeichnung und nicht den zusätzlichen Hinweisen hinzuzufügen.
-   Wenn Sie mehrzeilenbeschriftungen verwenden müssen, richten Sie den oberen Teil der Bezeichnung mit dem Kontrollkästchen aus.
-   Verwenden Sie kein untergeordnetes Steuerelement, die werte, die es enthält, oder seine Einheitenbezeichnung, um einen Satz oder Ausdruck zu erstellen. Ein solcher Entwurf ist nicht lokalisierbar, da die Satzstruktur je nach Sprache variiert.

    **Falsch:**

    ![Screenshot der Kontrollkästchenbezeichnung mit Textfeld ](images/ctrl-check-boxes-image27.png)

    In diesem Beispiel wird das Textfeld fälschlicherweise in der Kontrollkästchenbezeichnung platziert.

**Kontrollkästchengruppenbezeichnungen**

-   Verwenden Sie die Gruppenbezeichnung, um den Zweck der Gruppe und nicht die Auswahl zu erläutern. Angenommen, Benutzer wissen, wie Kontrollkästchen verwendet werden. Geben Sie beispielsweise nicht "Wählen Sie eine der folgenden Optionen aus".
-   Beenden Sie jede Bezeichnung mit einem Doppelpunkt.
-   Weisen Sie der Bezeichnung keinen Zugriffsschlüssel zu. Dies ist nicht erforderlich und erschwert die Zuweisung der anderen Zugriffsschlüssel.
-   Wenn Sie eine oder mehrere abhängige Optionen auswählen, erläutern Sie die Anforderung für die Bezeichnung.

    **Richtig:**

    ![Screenshot der Bezeichnung für zwei Steuerelemente: Protokolle ](images/ctrl-check-boxes-image28.png)

    In diesem Beispiel könnten Benutzer denken, dass sie nur eine Auswahl treffen können.

    **Besser:**

    ![Screenshot der Bezeichnung: Protokolle wählen mindestens eine Auswählung aus. ](images/ctrl-check-boxes-image29.png)

    In diesem Beispiel ist klar, dass Benutzer mehr als eine Auswahl treffen können.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Kontrollkästchen:

-   Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Großschreibung, aber nicht den Unterstrich oder Doppelpunkt des Zugriffsschlüssels. Schließen Sie das Wort ein Kontrollkästchen ein.
-   Verweisen Sie auf ein Kontrollkästchen als Kontrollkästchen, nicht als Option, als Kontrollkästchen oder einfach als Kontrollkästchen, da das Kontrollkästchen allein für Lokalisierer mehrdeutig ist.
-   Um die Benutzerinteraktion zu beschreiben, verwenden Sie select und clear.
-   Formatieren Sie die Bezeichnung nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

    Beispiel: Aktivieren Sie das Kontrollkästchen **Unterstreichung.**

