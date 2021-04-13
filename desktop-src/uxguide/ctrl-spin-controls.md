---
title: Dreh Steuerelemente
description: Mit einem Drehfeld-Steuerelement können Benutzer auf Pfeil Schaltflächen klicken, um den Wert inkrementell im zugeordneten numerischen Textfeld zu ändern.
ms.assetid: 5f791fb9-1354-41b9-a9de-ddab35302d50
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 54ce622983e52d65fa58ef05aca783ff67ebce66
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351099"
---
# <a name="spin-controls"></a>Dreh Steuerelemente

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Mit einem Drehfeld-Steuerelement können Benutzer auf Pfeil Schaltflächen klicken, um den Wert inkrementell im zugeordneten [numerischen Textfeld](ctrl-text-boxes.md)zu ändern. Der Begriff Drehfeld bezieht sich auf die Kombination aus einem Textfeld und dem zugehörigen Drehfeld-Steuerelement.

![Screenshot des Drehfeld-Steuer Elements und Textfelds ](images/ctrl-spin-controls-image1.png)

Ein typisches Drehfeld.

Benutzer bevorzugen häufig Dreh Steuerelemente, da Sie Änderungen vornehmen können, ohne Ihre Hände von der Maus zu bewegen. Wenn das Drehfeld Steuerelement mit einem Textfeld gekoppelt ist, können Benutzereingaben direkt in das Textfeld eingeben oder einfügen, sodass die Verwendung des Drehungs Steuer Elements optional ist.

Während Dreh Steuerelemente für numerische Eingaben verwendet werden, muss die Eingabe keine reine ganze Zahl sein. Die Eingabe kann Dezimalzahlen sein und kann negative Vorzeichen, Trennzeichen (z. b. Doppelpunkte oder Bindestriche) und Einheits Modifizierer aufweisen.

> [!Note]  
> Richtlinien, die sich auf [Textfelder](ctrl-text-boxes.md) und [Layout](vis-layout.md) beziehen, werden in separaten Artikeln dargestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Wird das Steuerelement für numerische Eingaben verwendet?** Wenn dies nicht der Fall ist, verwenden Sie ein anderes Steuerelement, z. b. eine [Dropdown Liste](/windows/desktop/uxguide/ctrl-drop) oder einen [Schieberegler](ctrl-sliders.md), um einen festgelegten Satz von Werten auszuwählen Verwenden Sie Scrollleisten für den Bildlauf.
-   **Betrachten die Benutzer den Wert als relative Menge, nicht als numerischen Wert?** Wenn ja, verwenden Sie stattdessen einen Schieberegler. Verwenden Sie Drehfelder nur für exakte, bekannte numerische Werte. So denken Benutzer beispielsweise beim Festlegen der Audiolautstärke an "niedrig" oder "mittel", aber nicht an Werte wie "2" oder "5".
-   **Ist das Steuerelement mit einem Textfeld gekoppelt?** Wenn nicht, verwenden Sie nicht. Drehfeld-Steuerelemente dürfen nicht allein oder mit anderen Steuerelement Typen außer einem Textfeld verwendet werden.

    **Falsch:**

    ![Screenshot des Drehfeld-Steuer Elements, Grafik, kein Textfeld ](images/ctrl-spin-controls-image2.png)

    In diesem Beispiel wird ein Drehfeld-Steuerelement verwendet, um eine dynamische Grafik zu steuern.

-   **Sind zusammenhängende Wertebereiche gültig?** Wenn dies nicht der Fall ist, verwenden Sie stattdessen eine Dropdown Liste mit gültigen Werten.

    ![Screenshot der Dropdown Liste ](images/ctrl-spin-controls-image3.png)

    In diesem Beispiel sind nicht alle laufwerksnummern gültig. eine Dropdown Liste ist daher eine bessere Wahl.

-   **Verwendet das Dreh Steuerelement praktisch?** Die Verwendung eines Drehfeld-Steuer Elements ist praktisch für:

    -   Eingeben einer kleinen Zahl, normalerweise unter 100.
    -   Vornehmen kleiner Änderungen an einem vorhandenen oder Standardwert.

    Drehfeld-Steuerelemente können zwar für beliebige numerische Eingaben verwendet werden, Sie sind jedoch in anderen Situationen ineffizient.

-   **Ist das Dreh Steuerelement hilfreich?** Wird das Steuerelement in einem Kontext verwendet, in dem Benutzer wahrscheinlich Ihre Maus verwenden? Wenn dies nicht der gibt, sollten Sie ein Spin-Steuerelement optional
-   **Sind die Dropdown Listen der gleich geordneten Steuerelemente?** Wenn andere Dropdown Listen vorhanden sind, sollten Sie in Erwägung ziehen, eine Dropdown Liste für die Konsistenz zu verwenden.

    ![Screenshot des Dialog Felds mit Dropdown Listen ](images/ctrl-spin-controls-image4.png)

    In diesem Beispiel könnte ein Drehfeld verwendet werden, aber eine Dropdown Liste wird aus Gründen der Konsistenz verwendet.

-   **Handelt es sich bei Berührungs-oder Stift Benutzern um ein primäres Ziel** Wenn dies der Fall ist, sollten Sie stattdessen eine Dropdown Liste verwenden. Die Pfeil Schaltflächen in einem Drehfeld-Steuerelement sind zu klein, um effizient mit berühren oder einem Stift verwendet werden zu können.

Wenn ein Schieberegler oder ein Drehfeld möglich ist, verwenden Sie ein Drehfeld, wenn Folgendes gilt:

-   Der auf dem Bildschirm verfügbare Platz ist knapp.
-   Ein Benutzer wird die Verwendung der Tastatur wahrscheinlich bevorzugen.

Verwenden Sie in folgenden Fällen einen Schieberegler:

-   Benutzer profitieren von sofortigem Feedback.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Verwenden Sie Dreh Steuerelemente, wenn Sie praktisch und hilfreich sind.** Siehe [ist das richtige Steuerelement?](#is-this-the-right-control)

    -   **Ausnahme:** Um mit anderen Textfeldern auf derselben Benutzeroberfläche konsistent zu sein, verwenden Sie die Drehfeld-Steuerelemente, auch wenn Sie nicht immer praktikabel sind.

    **Richtig:**

    ![Screenshot der Drehfeld-Steuerelemente für Monat, Tag, Jahr ](images/ctrl-spin-controls-image5.png)

    In diesem Beispiel wird ein Drehfeld-Steuerelement für die Konsistenz mit dem Year-Steuerelement verwendet, auch wenn es nicht immer praktikabel ist.

    **Falsch:**

    ![Screenshot des Drehungs Steuer Elements für IP-Adressen ](images/ctrl-spin-controls-image6.png)

    In diesem Beispiel ist das Drehfeld-Steuerelement unbrauchbar.

-   **Legen Sie den "Kumpel" des Textfelds immer als Dreh Steuerelement ab.** Dadurch wird das Drehfeld-Steuerelement in das Textfeld eingefügt.

    **Richtig:**

    ![Screenshot des Dreh Steuer Elements, das sich im Textfeld befindet ](images/ctrl-spin-controls-image7.png)

    **Falsch:**

    ![Screenshot des Drehfeld-Steuer Elements außerhalb des Textfelds ](images/ctrl-spin-controls-image8.png)

    Im richtigen Beispiel wird das Drehfeld-Steuerelement in das zugehörige Textfeld eingefügt.

-   **Deaktivieren Sie ein Drehfeld-Steuerelement, wenn das zugehörige Textfeld deaktiviert ist.** Das Spin-Steuerelement ist eine ergänzende Eingabemethode – nie die einzige Eingabemethode.

### <a name="values"></a>Werte

-   **Definieren Sie die oberste Schaltfläche, um den Wert um eine Einheit zu vergrößern, und die untere Schaltfläche, um um eine Einheit zu verringern.** In der Regel handelt es sich um eine Einheit, die jedoch die kleinste allgemeine Änderung des Werts sein sollte. Im Idealfall sollte das Drehfeld-Steuerelement alle gültigen Werte abdecken, und es sollte bequemer sein als das Eingeben des Texts.

    ![Screenshot des Dreh Steuer Elements "Ränder" ](images/ctrl-spin-controls-image9.png)

    Wenn Sie in diesem Beispiel auf ein Drehfeld-Steuerelement klicken, werden die Werte von 1 geändert. Dies ist die kleinste allgemeine Änderung des Werts. Durch die Verwendung einer kleineren Einheit wird der Bereich gültiger Werte abgedeckt, aber die Dreh Steuerelemente können unbrauchbar werden.

-   **Verwenden Sie das Drehfeld-Steuerelement, um Eingaben auf gültige Werte einzuschränken.** Die Verwendung eines Drehfeld-Steuer Elements sollte nie zu einem falschen Wert führen.
-   **Starten Sie den Bereich am Ende eines Bereichs gültiger Werte neu.** Das Dreh Steuerelement-Metapher ist, dass der Benutzer ein Rad mit Werten spinnt, also dieses Rad-like-Verhalten.
    -   **Ausnahme:** Starten Sie den Bereich nicht neu, wenn der resultierende Wert nicht korrekt ist.

        ![Screenshot des Dreh Steuer Elements "Anzahl der Kopien" ](images/ctrl-spin-controls-image10.png)

        Wenn Sie in diesem Beispiel auf die Schaltfläche mit dem Pfeil nach unten klicken, wird der Bereich nicht neu gestartet (durch den maximalen Wert), da dieser Wert sicher nicht korrekt ist.

-   **Verwenden Sie anstelle von besonderen numerischen Werten Text.** Ermöglichen Sie es Benutzern, diese besonderen Werte zu verwenden, anstatt Sie kennen zu müssen, und geben Sie Sie ein.

    ![Screenshot des "Standby after (Never)"-Drehfeld Steuer Elements ](images/ctrl-spin-controls-image11.png)

    In diesem Beispiel ist nie ein spezieller Wert, aber Benutzer können darauf drehen.

-   **Wenn der Wert Trennzeichen aufweist, sollte das zugehörige Textfeld über mehrere Eingabefokus Punkte verfügen.** Auf diese Weise können die numerischen Segmente einzeln bearbeitet werden.

    ![Screenshot des Zeit drehenden Steuer Elements, Minuten ausgewählt ](images/ctrl-spin-controls-image12.png)

    In diesem Beispiel wirkt sich das Spin-Steuerelement auf die Werte für Stunden, Minuten, Sekunden und Uhr/p.m.-Kennung –, je nachdem, welcher Fokus hat.

-   **Wenn der Werteinheiten aufweist, verwenden Sie das Drehfeld-Steuerelement, um diese Einheiten ebenfalls zu ändern.**

    ![Screenshot des Time-Spin-Steuer Elements, "Uhr" Ausgewählt ](images/ctrl-spin-controls-image13.png)

    In diesem Beispiel kann das Drehfeld-Steuerelement zum Ändern von Einheiten verwendet werden.

## <a name="labels"></a>Bezeichnungen

-   Wenden Sie die [Textfeld-Beschriftungs](ctrl-text-boxes.md) Richtlinien an, um das zugehörige Textfeld zu bezeichnen Drehfeld-Steuerelemente werden niemals direkt bezeichnet.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Dreh Steuerelemente:

-   In der Benutzerdokumentation finden Sie keine Informationen zu den Dreh Steuerelementen. Verweisen Sie stattdessen auf die Bezeichnung des zugeordneten Textfelds.
-   Weitere Informationen finden Sie unter Dreh Steuerelemente und Drehfelder nur in der Programmierung und in anderen technischen Dokumentationen.

Beispiel: Geben Sie im Feld **Datum** den Datums Abschnitt ein, den Sie ändern möchten, oder wählen Sie ihn aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Glossar](glossary.md)
</dt> </dl>

 

 