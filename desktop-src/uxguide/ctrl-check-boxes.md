---
title: Kontrollkästchen
description: Mithilfe eines Kontrollkästchens treffen Benutzer eine Entscheidung zwischen zwei eindeutig entgegengesetzten Entscheidungen.
ms.assetid: 7c39987d-807b-41c1-9788-65c3d468b976
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7a175893b2dfab2999ce37e3f00395d881f03973
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103961070"
---
# <a name="check-boxes"></a>Kontrollkästchen

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Mithilfe eines Kontrollkästchens treffen Benutzer eine Entscheidung zwischen zwei eindeutig entgegengesetzten Entscheidungen. Die Kontrollkästchen Bezeichnung gibt den ausgewählten Zustand an, wohingegen die Bedeutung des gelöschten Zustands das eindeutige Gegenteil des ausgewählten Zustands sein muss. Folglich **sollten Kontrollkästchen nur verwendet werden, um eine Option ein-oder auszuschalten oder ein Element auszuwählen oder zu deaktivieren.**

![Screenshot einer der vier aktivierten Kontrollkästchen ](images/ctrl-check-boxes-image1.png)

Eine typische Gruppe von Kontrollkästchen.

> [!Note]  
> Richtlinien für das [Layout](vis-layout.md) werden in einem separaten Artikel dargestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Wird das Kontrollkästchen verwendet, um eine Option ein-oder auszuschalten oder ein Element auszuwählen oder zu deaktivieren?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement.
-   **Sind die ausgewählten und gelöschten Zustände eindeutig und eindeutige Gegensätze?** Wenn dies nicht der Fall ist [, verwenden Sie](ctrl-radio-buttons.md) Options Felder oder eine [Dropdown Liste](/windows/desktop/uxguide/ctrl-drop) , damit Sie die Zustände unabhängig voneinander bezeichnen können.
-   **Wenn die Gruppe in einer Gruppe verwendet wird, besteht Sie aus unabhängigen Optionen, von denen aus die Benutzer NULL oder mehr auswählen können?** Falls nicht, sollten Sie Steuerelemente für abhängige Optionen wie Options Felder und [Kontrollkästchen](ctrl-tree-views.md)-Struktur Ansichten in Erwägung gezogen.
-   **Wenn die Gruppe in einer Gruppe verwendet wird, besteht Sie aus abhängigen Optionen, von denen Benutzer eine oder mehrere auswählen müssen?** Wenn dies der Fall ist, verwenden Sie eine Gruppe von Kontrollkästchen, und behandeln Sie den Fehler, wenn keine der Optionen ausgewählt ist.
-   **Ist die Anzahl der Optionen in einer Gruppe 10 oder weniger.** Da der verwendete Bildschirmbereich proportional zur Anzahl der Optionen ist, behalten Sie die Anzahl der Kontrollkästchen bei 10 oder weniger. Verwenden Sie für mehr als 10 Optionen eine [Kontrollkästchen Liste](ctrl-list-boxes.md).
-   **Wäre eine Options Schaltfläche eine bessere Wahl?** Wenn die Kontrollkästchen nur zum Aktivieren oder Deaktivieren einer Option geeignet sind, können Options Felder für vollkommen andere Optionen verwendet werden. Wenn beide Lösungen möglich sind:
    -   Verwenden Sie Options Felder, wenn die Bedeutung des Kontrollkästchens nicht vollständig ersichtlich ist.

        **Falsch:**

        ![Screenshot eines Kontrollkästchens mit der Bezeichnung "Landscape" ](images/ctrl-check-boxes-image2.png)

        In diesem Beispiel ist die umgekehrte Auswahl aus Landscape nicht klar, sodass das Kontrollkästchen keine gute Wahl ist.

        **Richtig:**

        ![Screenshot zweier Options Felder ](images/ctrl-check-boxes-image3.png)

        In diesem Beispiel sind die Optionen keine Gegensätze, daher sind Options Felder die bessere Wahl.

    -   Verwenden Sie Options Felder auf Assistenten Seiten, um die Alternativen zu löschen, selbst wenn ein Kontrollkästchen andernfalls akzeptabel ist.
    -   Verwenden Sie Options Felder, wenn genügend Platz auf dem Bildschirm vorhanden ist, und die Optionen sind wichtig genug, um diesen Bildschirmbereich gut verwenden zu können. Andernfalls verwenden Sie ein Kontrollkästchen oder eine Dropdown Liste.

        **Falsch:**

        ![Screenshot der Schaltflächen zum Anzeigen und Anzeigen von Verhältnis ](images/ctrl-check-boxes-image4.png)

        In diesem Beispiel sind die Optionen für die Verwendung von Options Feldern nicht wichtig genug.

        **Richtig:**

        ![Screenshot des Kontrollkästchens mit Meldung nicht anzeigen ](images/ctrl-check-boxes-image5.png)

        In diesem Beispiel ist ein Kontrollkästchen eine effiziente Verwendung des Bildschirm Raums für diese Peripherie Option.

-   Verwenden Sie ein Kontrollkästchen, wenn im Fenster andere Kontrollkästchen vorhanden sind.
-   **Stellt die Option anstelle von Daten eine Programm Option dar?** Die Werte der Option sollten nicht auf dem Kontext oder anderen Daten basieren. Verwenden Sie für Daten eine Kontrollkästchen Liste oder eine [Mehrfachauswahl Liste](ctrl-list-boxes.md).

## <a name="usage-patterns"></a>Verwendungsmuster

Kontrollkästchen verfügen über mehrere Verwendungs Muster:



|                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Eine individuelle Auswahl** Ein einzelnes Kontrollkästchen wird verwendet, um eine einzelne Auswahl auszuwählen. <br/>                                                                                                             | ![Screenshot eines Kontrollkästchens mit der Bezeichnung "Erinnerung" ](images/ctrl-check-boxes-image6.png)<br/> Ein einzelnes Kontrollkästchen wird für eine individuelle Auswahl verwendet.<br/>                                                                                                                                                                                                                                                                                                                        |
| **Unabhängige Optionen (0 (null) oder mehr)** Eine Gruppe von Kontrollkästchen wird verwendet, um aus einem Satz von NULL oder mehr Optionen auszuwählen.<br/>                                                                              | anders als Steuerelemente mit einfacher Auswahl [, wie](ctrl-radio-buttons.md)z. b. Options Felder, können Benutzer eine beliebige Kombination von Optionen in einer Gruppe von Kontrollkästchen auswählen.<br/> ![Screenshot von zwei ausgewählten aktivierten Kontrollkästchen ](images/ctrl-check-boxes-image7.png)<br/> Eine Gruppe von Kontrollkästchen wird für unabhängige Optionen verwendet.<br/>                                                                                                                                                  |
| **Abhängige Auswahlmöglichkeiten (mindestens eine)** Eine Gruppe von Kontrollkästchen kann auch verwendet werden, um aus einem Satz von einer oder mehreren Optionen auszuwählen.<br/>                                                                         | **möglicherweise müssen Sie eine Auswahl von einer oder mehreren abhängigen Optionen darstellen**. Da Microsoft? Windows nicht über ein Steuerelement verfügt, das diese Art von Eingaben direkt unterstützt, ist die beste Lösung, eine Gruppe von Kontrollkästchen zu verwenden und den Fehler zu behandeln, wenn keine der Optionen ausgewählt ist.<br/> ![Screenshot eines der beiden ausgewählten Kontrollkästchen ](images/ctrl-check-boxes-image8.png)<br/> Eine Gruppe von Kontrollkästchen wird verwendet, wenn mindestens ein Protokoll ausgewählt werden muss.<br/> |
| **Gemischte Auswahl** Zusätzlich zu den ausgewählten und gelöschten Zuständen haben Kontrollkästchen auch einen gemischten Zustand für Mehrfachauswahl, um anzugeben, dass die Option für einige, aber nicht für alle Objekte festgelegt ist.<br/> | ![Screenshot eines schreibgeschützten Volltext-Kontrollkästchens ](images/ctrl-check-boxes-image9.png)<br/> Ein Kontrollkästchen mit gemischtem Zustand.<br/>                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Gruppenbezogene Kontrollkästchen**. Kombinieren Sie verknüpfte Optionen, und trennen Sie nicht verknüpfte Optionen in Gruppen von höchstens 10 Gruppen, bei Bedarf unter Verwendung mehrerer Gruppen.

    ![Screenshot der zugehörigen und nicht verknüpften Kontrollkästchen ](images/ctrl-check-boxes-image10.png)

    Ein Beispiel für Gruppen verwandter, unabhängiger Optionen.

-   Über **prüfen Sie die Verwendung von Gruppen Feldern, um Gruppen von Kontrollkästchen zu organisieren** . Dies führt häufig zu unnötiger Bildschirm Übersichtlichkeit.
-   **Auflisten von Kontrollkästchen in einer logischen Reihenfolge**, z. b. Gruppieren von stark verknüpften Optionen oder Erstmaliges platzieren der gängigsten Optionen oder befolgen anderer natürlicher Fortschritte. Eine alphabetische Sortierung wird nicht empfohlen, da Sie sprachabhängig und daher nicht lokalisierbar ist.
-   **Aktivieren Sie die Kontrollkästchen Vertikal, nicht horizontal**. Die horizontale Ausrichtung ist schwieriger zu lesen.

    **Richtig:**

    ![Screenshot der vertikal ausgerichteten Kontrollkästchen ](images/ctrl-check-boxes-image11.png)

    In diesem Beispiel sind die Kontrollkästchen ordnungsgemäß ausgerichtet.

    **Falsch:**

    ![Screenshot der horizontal ausgerichteten Kontrollkästchen ](images/ctrl-check-boxes-image12.png)

    In diesem Beispiel ist die horizontale Ausrichtung schwieriger zu lesen.

-   **Verwenden Sie den gemischten Zustand nicht, um einen dritten Zustand darzustellen.** Der gemischte Zustand wird verwendet, um anzugeben, dass eine Option für einige, aber nicht für alle untergeordneten Objekte festgelegt ist. Benutzer sollten nicht in der Lage sein, einen gemischten Zustand direkt festzulegen, da der gemischte Zustand eine Reflektion der untergeordneten Objekte ist. Der gemischte Zustand wird nicht als dritter Zustand eines einzelnen Elements verwendet. Wenn Sie einen dritten Status darstellen möchten, verwenden Sie stattdessen Options Felder oder eine Dropdown Liste.

    **Falsch:**

    ![Screenshot des dashboarddienstanbieter (Solid Blue Theme) ](images/ctrl-check-boxes-image13.png)

    In diesem Beispiel soll der gemischte Zustand angeben, dass der Design Dienst nicht installiert ist.

    **Richtig:**

    ![Screenshot der Dropdown Liste mit drei Optionen ](images/ctrl-check-boxes-image14.png)

    In diesem Beispiel können Benutzer aus einer Liste mit drei Clear-Optionen auswählen.

-   **Wenn Sie auf einen gemischten Zustand klicken, wird das Kontrollkästchen Alle ausgewählten, alle gelöschten und ursprünglichen gemischten Zustände durchlaufen.** Zur Vergebung ist es wichtig, dass Sie den ursprünglichen gemischten Zustand wiederherstellen können, da die Einstellungen dem Benutzer sehr komplex oder unbekannt sein können. Andernfalls besteht die einzige Möglichkeit zum Wiederherstellen des gemischten Zustands mit Zuversicht darin, den Task abzubrechen und zu beginnen.
-   **Verwenden Sie keine Kontrollkästchen als Fortschrittsanzeige**. Verwenden Sie stattdessen ein Status [Anzeige](progress-bars.md) -Steuerelement.

    **Falsch:**

    ![Screenshot von vier Kontrollkästchen, die den Fortschritt anzeigen ](images/ctrl-check-boxes-image15.png)

    In diesem Beispiel werden Kontrollkästchen fälschlicherweise als Fortschrittsanzeige verwendet.

    **Richtig:**

    ![Screenshot einer teilweise gefüllten Statusanzeige ](images/ctrl-check-boxes-image16.png)

    Beispiel für eine typische Statusanzeige.

-   **Zeigt deaktivierte Kontrollkästchen mit dem richtigen Auswahl Zustand an.** Obwohl die Benutzer Sie nicht ändern können, werden bei deaktivierten Kontrollkästchen Informationen angezeigt, sodass Sie mit den Ergebnissen konsistent sein sollten.

    **Falsch:**

    ![Screenshot eines von zwei Kontrollkästchen abdimmt ](images/ctrl-check-boxes-image17.png)

    In diesem Beispiel sollte die Option "Always Read This section Aloud" gelöscht werden, da der Abschnitt nicht gelesen wird, wenn die Option deaktiviert ist.

-   **Verwenden Sie die Auswahl eines Kontrollkästchens nicht für** Folgendes:
    -   Ausführen von Befehlen.
    -   Zeigen Sie andere Fenster an, z. b. ein Dialogfeld, um weitere Eingaben zu erfassen.
    -   Dynamische Anzeige anderer Steuerelemente, die mit dem ausgewählten Steuerelement verknüpft sind (Sprachausgabe können solche Ereignisse nicht erkennen).

### <a name="dont-show-this-item-again"></a>Nicht anzeigen <item> erneut

-   **Verwenden Sie <item> die Option Diese Option nicht mehr anzeigen, um Benutzern das Unterdrücken eines wiederkehrenden Dialog Felds nur dann zu gestatten, wenn es keine bessere Alternative gibt.** Versuchen Sie, vorher zu ermitteln, ob Benutzer das Dialogfeld wirklich benötigen. Wenn dies der Fall ist, sollten Sie das Dialogfeld immer anzeigen, wenn dies nicht der Fall ist.

Weitere Richtlinien und Beispiele finden Sie unter [Dialog Felder](win-dialog-box.md).

### <a name="subordinate-controls"></a>Untergeordnete Steuerelemente

-   Platzieren Sie untergeordnete Steuerelemente rechts von oder unten (eingerückt, mit der Kontrollkästchen Bezeichnung) mit dem Kontrollkästchen und der zugehörigen Bezeichnung. Beenden Sie die Bezeichnung des Kontrollkästchens mit einem Doppelpunkt.

    ![Screenshot des Textfelds unterhalb der Kontrollkästchen Bezeichnung ](images/ctrl-check-boxes-image18.png)

    In diesem Beispiel werden das Kontrollkästchen und das untergeordnete Steuerelement die Kontrollkästchen Bezeichnung und deren Zugriffstaste gemeinsam verwenden.

-   **Lassen Sie abhängige, bearbeitbare Textfelder und Dropdown Listen aktiviert, wenn Sie die Bezeichnung des Kontrollkästchens freigeben.** Wenn Benutzer Elemente eingeben oder in das Feld einfügen, wählen Sie die entsprechende Option automatisch aus. Dies vereinfacht die Interaktion.

    ![Screenshot von Kopf-und Fußzeilen Textfeldern ](images/ctrl-check-boxes-image19.png)

    Wenn Sie in diesem Beispiel eine Kopf-oder Fußzeile eingeben, wird die Option automatisch ausgewählt.

-   Wenn Sie Kontrollkästchen mit Options Feldern oder anderen Kontrollkästchen Schachteln, **Deaktivieren Sie diese untergeordneten Steuerelemente, bis die Option auf hoher Ebene ausgewählt ist**. Dadurch wird Verwirrung in Bezug auf die Bedeutung der untergeordneten Steuerelemente vermieden.
-   Aktivieren Sie das Kontrollkästchen in der Aktivier Reihenfolge, um untergeordnete Steuerelemente zu einem Kontrollkästchen zusammenzustellen.
-   **Wenn Sie eine Option auswählen, aktivieren Sie die Option untergeordnete Kontrollkästchen, aktivieren Sie diese Kontrollkästchen explizit, um die Beziehung klar zu machen.**

    **Falsch:**

    ![Screenshot: ausgewählte Schaltfläche, gelöschte Kontrollkästchen ](images/ctrl-check-boxes-image20.png)

    In diesem Beispiel werden die untergeordneten Kontrollkästchen nicht ausgewählt.

    **Richtig:**

    ![Screenshot: ausgewählte Schaltfläche, ausgewählte Kontrollkästchen ](images/ctrl-check-boxes-image21.png)

    In diesem Beispiel werden die untergeordneten Kontrollkästchen aktiviert, sodass Ihre Beziehung zur ausgewählten Option deaktiviert ist.

-   **Verwenden Sie abhängige Kontrollkästchen, wenn die alternativen unnötige Komplexität hinzufügen**. Obwohl Kontrollkästchen unabhängige Optionen sein sollten, fügen Alternativen wie Options Felder unnötige Komplexität mit sich.

    **Richtig:**

    ![Screenshot der verwirrenden Schaltflächen und Kontrollkästchen ](images/ctrl-check-boxes-image22.png)

    In diesem Beispiel ist die Verwendung von Options Feldern genau, aber es entsteht unnötige Komplexität.

    **Besserer**

    ![nur Screenshot von Kontrollkästchen ](images/ctrl-check-boxes-image23.png)

    In diesem Beispiel ist die Verwendung von Kontrollkästchen einfacher und ermöglicht es den Benutzern, sich auf die Auswahl der gewünschten Optionen anstelle der komplexen Beziehung zu konzentrieren.

    **Wichtig: wenden Sie diese Richtlinie nur in sehr seltenen Fällen an**, wenn die Darstellung der Abhängigkeiten zu einer erheblichen Komplexität führt, ohne die Klarheit zu erhöhen Im vorherigen Beispiel ist es unwahrscheinlich, dass Benutzer versuchen, sowohl das hoch gestellt als auch den Index zu wählen. wenn dies der Fall ist, wäre es einfach zu verstehen, dass es sich um exklusive Optionen handelt.

### <a name="default-values"></a>Standardwerte

-   Wenn ein Kontrollkästchen für eine Benutzer Option gilt, **legen Sie den sichersten (um Datenverlust oder System Zugriff zu verhindern), den sichersten und den privaten Zustand standardmäßig fest.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie den wahrscheinlichsten oder einfachsten Wert aus.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstände

![Abbildung der vorgeschlagenen Größe und des Abstands des Kontrollkästchens ](images/ctrl-check-boxes-image24.png)

Empfohlene Größe und Abstände für Kontrollkästchen.

## <a name="labels"></a>Bezeichnungen

**Kontrollkästchen Bezeichnungen**

-   Beschriften Sie jedes Kontrollkästchen.
-   Weisen Sie jeder Bezeichnung einen eindeutigen [Zugriffsschlüssel](glossary.md) zu. Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   Schreiben Sie die Bezeichnung als Ausdruck oder imperativer Satz, und verwenden Sie keine endinterpunktions Zeichen.
    -   **Ausnahme:** Wenn eine Kontrollkästchen-Bezeichnung auch ein untergeordnetes Steuerelement bezeichnet, das darauf folgt, beenden Sie die Bezeichnung mit einem Doppelpunkt.
-   Schreiben Sie die Bezeichnung, sodass der ausgewählte Zustand des Kontrollkästchens beschrieben wird.
-   Verwenden Sie für eine Gruppe von Kontrollkästchen parallele Ausdrücke, und versuchen Sie, die Länge für alle Bezeichnungen auf denselben Wert zu beschränken.
-   Für eine Gruppe von Kontrollkästchen können Sie den Bezeichnungs Text auf die Unterschiede zwischen den Optionen konzentrieren. Wenn alle Optionen denselben einführenden Text aufweisen, verschieben Sie diesen Text in die Gruppen Bezeichnung.
-   Verwenden Sie einen positiven Ausdruck. Geben Sie keine Bezeichnung ein, sodass das Aktivieren eines Kontrollkästchens bedeutet, dass keine Aktion ausgeführt werden soll.

    -   **Ausnahme: diese Kontrollkästchen werden nicht <item> mehr angezeigt** .

    **Falsch:**

    ![Screenshot der negativen Bezeichnung "Ausschalten"](images/ctrl-check-boxes-image25.png)

    In diesem Beispiel verwendet die Option keine positive Formulierung.

-   Beschreiben Sie nur die Option mit der Bezeichnung. Halten Sie Bezeichnungen kurz, damit Sie in Nachrichten und Dokumentationen leicht darauf verweisen können. Wenn die Option eine weitere Erläuterung erfordert, stellen Sie die Erläuterung in einem [statischen Text](./glossary.md) Steuerelement mithilfe von vollständigen Sätzen und endinterpunktions Zeichen bereit.

    > [!Note]
    >
    > Das Hinzufügen einer Erläuterung zu einem Kontrollkästchen in einer Gruppe bedeutet nicht, dass Sie Erklärungen für alle Kontrollkästchen in der Gruppe angeben müssen. Geben Sie die relevanten Informationen in der Bezeichnung an, wenn dies möglich ist, und verwenden Sie nur bei Bedarf Erklärungen. Geben Sie die Bezeichnung nicht nur auf Konsistenz zurück.

     

    ![Screenshot des Kontrollkästchens, der Bezeichnung und der Beschreibung ](images/ctrl-check-boxes-image26.png)

    In diesem Beispiel enthält eine Kontrollkästchen Bezeichnung zusätzlichen erläuternden Text darunter.

-   Wenn eine Option dringend empfohlen wird, sollten Sie "(empfohlen)" der Bezeichnung hinzufügen. Stellen Sie sicher, dass Sie der Steuerelement Bezeichnung und nicht den ergänzenden Notizen hinzufügen.
-   Wenn Sie mehrzeilige Bezeichnungen verwenden müssen, richten Sie den oberen Rand der Bezeichnung mit dem Kontrollkästchen aus.
-   Verwenden Sie kein untergeordnetes Steuerelement, die darin enthaltenen Werte oder die zugehörige Einheiten Bezeichnung, um einen Satz oder einen Ausdruck zu erstellen. Ein solcher Entwurf ist nicht lokalisierbar, da die Satzstruktur von der Sprache abweicht.

    **Falsch:**

    ![Screenshot der CheckBox-Bezeichnung mit dem darin angezeigten Textfeld ](images/ctrl-check-boxes-image27.png)

    In diesem Beispiel wird das Textfeld falsch in der Bezeichnung des Kontrollkästchens platziert.

**Kontrollkästchen-Gruppen Bezeichnungen**

-   Verwenden Sie die Gruppen Bezeichnung, um den Zweck der Gruppe zu erläutern, nicht, wie Sie die Auswahl treffen möchten. Angenommen, die Benutzer wissen, wie Kontrollkästchen verwendet werden. Nehmen Sie beispielsweise an, dass Sie eine der folgenden Optionen auswählen.
-   Beenden Sie jede Bezeichnung mit einem Doppelpunkt.
-   Weisen Sie der Bezeichnung keinen Zugriffsschlüssel zu. Dies ist nicht erforderlich, sodass die Zuweisung der anderen Zugriffsschlüssel erschwert wird.
-   Um eine oder mehrere abhängige Optionen auszuwählen, erklären Sie die Anforderung für die Bezeichnung.

    **Richtig:**

    ![Screenshot der Bezeichnung für zwei Steuerelemente: Protokolle ](images/ctrl-check-boxes-image28.png)

    In diesem Beispiel denken Benutzer möglicherweise, dass Sie nur eine Auswahl treffen können.

    **Besserer**

    ![Screenshot der Bezeichnung: Protokolle wählen Sie mindestens einen aus. ](images/ctrl-check-boxes-image29.png)

    In diesem Beispiel ist es klar, dass Benutzer mehr als eine Auswahl treffen können.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Kontrollkästchen:

-   Verwenden Sie den genauen Bezeichnungs Text, einschließlich der Groß-und Kleinschreibung, aber nicht den Unterstrich oder Doppelpunkt des Zugriffsschlüssels. Kontrollkästchen Word einschließen.
-   Aktivieren Sie ein Kontrollkästchen als Kontrollkästchen, nicht Option, Kontrollkästchen oder nur Box, da Box allein für Lokalisierer mehrdeutig ist.
-   Verwenden Sie zum Beschreiben der Benutzerinteraktion SELECT und Clear.
-   Formatieren Sie nach Möglichkeit die Bezeichnung mit fettem Text. Andernfalls sollten Sie die Bezeichnung nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

    Beispiel: Aktivieren Sie das Kontrollkästchen unter **Streichung** .

