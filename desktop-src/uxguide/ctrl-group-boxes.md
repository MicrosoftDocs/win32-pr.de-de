---
title: Gruppenfelder
description: Ein Gruppenfeld ist ein rechteckiger Frame, der einen Satz verwandter Steuerelemente umgibt. Ein Gruppenfeld ist eine Möglichkeit zum visuellen Anzeigen von Beziehungen. Abgesehen von der möglichen Bereitstellung eines Zugriffsschlüssels für eine Gruppe von Steuerelementen bietet diese Funktion keine Funktionalität.
ms.assetid: 5b5ffb36-3ed1-44cd-af87-5cddf46c56a6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 67f930383f2d4412d30027971c6cab2bd3edcccd
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104560970"
---
# <a name="group-boxes"></a>Gruppenfelder

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Ein Gruppenfeld ist ein rechteckiger Frame, der einen Satz verwandter Steuerelemente umgibt. Ein Gruppenfeld ist eine Möglichkeit zum visuellen Anzeigen von Beziehungen. Abgesehen von der möglichen Bereitstellung eines Zugriffsschlüssels für eine Gruppe von Steuerelementen bietet diese Funktion keine Funktionalität.

![Screenshot des Gruppen Felds mit Kontrollkästchen ](images/ctrl-group-boxes-image1.png)

Ein typisches Gruppenfeld.

> [!Note]  
> Richtlinien für das [Layout](vis-layout.md) werden in einem separaten Artikel dargestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Obwohl Gruppen Felder eine starke visuelle Methode zum Angeben von Beziehungen sind, wird durch eine übermäßige Verwendung die visuelle Gruppierung hinzugefügt, und der auf einer Oberfläche verfügbare Platz wird erheblich reduziert. Sie sind visuell stark und sollten nur selten verwendet werden – nur, wenn es keine bessere Lösung gibt.

Ein Entwurfs Trend in Windows ist ein einfacheres, saubereres aussehen, da unnötige Zeilen eliminiert werden.

Um zu entscheiden, ob ein Gruppenfeld erforderlich ist, sollten Sie die folgenden Fragen beachten:

-   **Gibt es mehr als ein Steuerelement in der Gruppe?** Wenn dies nicht der Wert ist, verwenden Sie stattdessen eine einfache Text Bezeichnung. Eine seltene Ausnahme besteht darin, ein Gruppenfeld mit einem einzelnen Steuerelement zu verwenden, um die Konsistenz mit anderen Gruppen Feldern auf derselben Oberfläche aufrechtzuerhalten.

**Falsch:** ![ Screenshot des Gruppen Felds, das ein Textfeld enthält ](images/ctrl-group-boxes-image2.png)

In diesem Beispiel enthält das Feld Gruppe nur ein einzelnes Steuerelement.

-   **Sind die Steuerelemente verknüpft? Zeigt die Beziehung die Klarheit?** Wenn dies nicht der Folge ist, stellen Sie die Steuerelemente getrennt außerhalb eines Gruppen Felds dar.
-   **Befinden sich alle Steuerelemente in der Gruppe?** Wenn dies der Fall ist, geben Sie die Beziehung auf der größeren Oberfläche an, z. b. das übergeordnete Dialogfeld oder die

**Falsch:** ![ Screenshot des Gruppen Felds mit allen Steuerelementen ](images/ctrl-group-boxes-image3.png)

In diesem Beispiel befinden sich alle Steuerelemente (außer den Commit-Schaltflächen) im Dialogfeld im Gruppenfeld.

-   **Können Sie die Beziehungen mithilfe von Layout allein übermitteln?** Wenn dies der Fall ist, verwenden Sie stattdessen das [Layout](vis-layout.md) . Sie können verwandte Steuerelemente nebeneinander platzieren und zusätzlichen Abstand zwischen nicht verknüpften Steuerelementen einfügen. Sie können auch Überschriften und Einzug verwenden, um hierarchische Beziehungen anzuzeigen.

![Abbildung von vier Symbolen mit vier Aufgaben Gruppen ](images/ctrl-group-boxes-image4.png)

In diesem Beispiel wird das Layout allein zum Anzeigen von Steuerelement Beziehungen verwendet.

-   **Können Sie die Beziehungen mithilfe eines Trenn Zeichens effektiv kommunizieren?** Verwenden Sie in diesem Fall stattdessen ein Trennzeichen. Ein Trennzeichen ist eine horizontale Linie, die die darunter liegenden Steuerelemente vereinheitlicht. Trennzeichen bieten ein einfacheres, saubereres aussehen. Im Gegensatz zu Gruppen Feldern funktionieren Sie jedoch am besten, wenn Sie sich über die gesamte Breite der Oberfläche erstrecken.
    -   **Entwickler:** Sie können ein Trennzeichen mit einem geätzten Rechteck mit einer Höhe von eins implementieren.

![Screenshot, der e-Mail-Steuerelemente anzeigt, die durch geächene Rechteck Trennzeichen](images/ctrl-group-boxes-image5.png)

In diesem Beispiel werden beschriftete Trennzeichen verwendet, um Steuerelement Beziehungen anzuzeigen.

![Screenshot der Steuerelemente, die durch Trennzeichen festgelegt wurden ](images/ctrl-group-boxes-image6.png)

In diesem Beispiel werden nicht beschriftete Trennzeichen verwendet, um Steuerelement Beziehungen anzuzeigen.

-   **Können Sie die Beziehungen ohne Text effektiv kommunizieren?** Wenn dies der Fall ist, sollten Sie grafische Elemente wie [Hintergründe](vis-graphic.md) oder Aggregatoren verwenden.

## <a name="guidelines"></a>Richtlinien

-   **Gruppieren Sie keine Gruppen Felder.** Verwenden Sie Layout, um Beziehungen in einem Gruppenfeld anzuzeigen.

**Falsch:** ![ Screenshot eines Gruppen Felds in einem Gruppenfeld ](images/ctrl-group-boxes-image7.png)

In diesem Beispiel führen die Felder für die gruppierten Gruppen zu einem unnötigen visuellen Cluster.

**Richtig:** ![ Screenshot der gleichen Steuerelemente in einem Gruppenfeld ](images/ctrl-group-boxes-image8.png)

In diesem Beispiel wird die gleiche Steuerelement Beziehung stattdessen mithilfe des Layouts angezeigt.

-   Legen Sie keine Steuerelemente in Gruppenfeld Bezeichnungen ab.
    -   **Ausnahme:** Sie können ein Kontrollkästchen als Gruppenfeld Bezeichnung verwenden, wenn alle Steuerelemente im Feld durch das Kontrollkästchen aktiviert und deaktiviert sind.

**Falsch:** ![ Screenshot der Dropdown Liste für eine Gruppenfeld Bezeichnung ](images/ctrl-group-boxes-image9.png)

In diesem Beispiel wird eine Dropdown Liste falsch in einem Gruppenfeld platziert. In diesem Beispiel sollten stattdessen [Registerkarten](https://msdn.microsoft.com/library/windows/desktop/aa511493.aspx) verwendet werden.

-   **Deaktivieren Sie Gruppen Felder nicht.** Um anzugeben, dass derzeit keine Gruppe von Steuerelementen angewendet wird, deaktivieren Sie alle Steuerelemente innerhalb des Gruppen Felds, jedoch nicht das Gruppenfeld selbst. Dieser Ansatz ist besser zugänglich und kann von allen Benutzeroberflächen-Frameworks konsistent unterstützt werden.

## <a name="labels"></a>Bezeichnungen

-   Bezeichnung alle Gruppen Felder.
-   Weisen Sie der Bezeichnung keinen Zugriffsschlüssel zu. Dies ist nicht erforderlich und macht die Zuweisung der anderen Zugriffsschlüssel erschwert. Weisen Sie stattdessen den Steuerelementen innerhalb des Gruppen Felds Zugriffstasten zu.
    -   **Ausnahme:** Wenn eine Oberfläche über viele Steuerelemente verfügt, sind möglicherweise nicht genügend Zugriffsschlüssel verfügbar. Wenn dies der Fall ist, verringern Sie die Anzahl der Zugriffsschlüssel, indem Sie Sie den Gruppen Feldern anstelle der Steuerelemente in den Gruppen Feldern zuweisen.
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   Schreiben Sie die Bezeichnung mithilfe eines Substantiv oder eines Substantiv Ausdrucks, nicht als Satz, und verwenden Sie keine endinterpunktions Zeichen, einschließlich Doppelpunkte.
-   Verwenden Sie parallele Ausdrücke für Gruppenfeld Bezeichnungen innerhalb derselben Oberfläche.
-   Halten Sie die Gruppenfeld Bezeichnungen kurz. Verwenden Sie keinen Anweisungs Text als Bezeichnung. Sie können jedoch einen Anweisungs Text in das Gruppenfeld haben.
-   Wiederholen Sie nicht die Bezeichnung für das Gruppenfeld im Feld Steuerelement Bezeichnungen. Wenn das Feld Gruppe beispielsweise als Ausrichtung bezeichnet wird, bezeichnen Sie die Options Felder Links, rechts usw., nicht linke Ausrichtung oder Rechte Ausrichtung.
-   Verweisen Sie nicht auf Gruppen Felder im Text der Benutzeroberfläche.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Gruppen Felder:

-   Informationen zu Gruppen Feldern finden Sie nur im Programmierer und in anderen technischen Dokumentationen. Verwenden Sie für Gruppenfeld zwei klein geschriebene Wörter.
-   An anderer Stelle ist es unnötig, den Namen des Gruppen Felds in eine Prozedur aufzunehmen, es sei denn, ein Dialogfeld enthält mehr als eine Option mit dem gleichen Namen. Verwenden Sie in solchen Fällen unter mit dem Namen des Gruppen Felds.
-   Formatieren Sie nach Möglichkeit die Bezeichnung mit fettem Text. Andernfalls sollten Sie die Bezeichnung nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Wählen Sie unter **Effekte** die Option **ausgeblendet** aus.

 

 