---
title: Drehsteuerelemente
description: Mit einem Drehsteuerelement können Benutzer auf Pfeilschaltflächen klicken, um den Wert innerhalb des zugehörigen numerischen Textfelds inkrementell zu ändern.
ms.assetid: 5f791fb9-1354-41b9-a9de-ddab35302d50
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b97f5acc8a3f904df3a868274356e5337f5cc9280a5eed81693d92ce9bf9a37c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118217359"
---
# <a name="spin-controls"></a>Drehsteuerelemente

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Mit einem Drehsteuerelement können Benutzer auf Pfeilschaltflächen klicken, um den Wert innerhalb des zugeordneten [numerischen Textfelds](ctrl-text-boxes.md)inkrementell zu ändern. Der Begriff Drehfeld bezieht sich auf die Kombination eines Textfelds und des zugehörigen Drehsteuerelements.

![Screenshot des Drehsteuerelements und des Textfelds ](images/ctrl-spin-controls-image1.png)

Ein typisches Drehfeld.

Benutzer bevorzugen häufig Drehsteuerelemente, da sie Änderungen vornehmen können, ohne ihre Hände mit der Maus zu bewegen. Wenn das Drehsteuerelement mit einem Textfeld gekoppelt ist, können Benutzer Eingaben direkt in das Textfeld eingeben oder einfügen, sodass die Verwendung des Drehsteuerelements optional ist.

Während Drehsteuerelemente für numerische Eingaben verwendet werden, muss die Eingabe keine reine ganze Zahl sein. Die Eingabe kann Dezimalzahlen sein und negative Vorzeichen, Trennzeichen (z. B. Doppelpunkte oder Bindestriche) und Einheitenmodifizierer aufweisen.

> [!Note]  
> Richtlinien im Zusammenhang mit [Textfeldern](ctrl-text-boxes.md) und [Layout](vis-layout.md) werden in separaten Artikeln vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Wird das Steuerelement für numerische Eingaben verwendet?** Wenn dies nicht der Fall ist, verwenden Sie ein anderes Steuerelement, z. B. eine [Dropdownliste](/windows/desktop/uxguide/ctrl-drop) oder einen [Schieberegler,](ctrl-sliders.md)um einen festen Satz von Werten auszuwählen. Verwenden Sie Bildlaufleisten zum Scrollen.
-   **Betrachten Benutzer den Wert als relative Menge, nicht als numerischen Wert?** Verwenden Sie in diesem Falle stattdessen einen Schieberegler. Verwenden Sie Drehfelder nur für genaue, bekannte numerische Werte. So denken Benutzer beispielsweise beim Festlegen der Audiolautstärke an "niedrig" oder "mittel", aber nicht an Werte wie "2" oder "5".
-   **Ist das Steuerelement mit einem Textfeld gekoppelt?** Wenn nicht, verwenden Sie nicht. Drehsteuerelemente sollten nicht allein oder mit anderen Steuerelementtypen außer einem Textfeld verwendet werden.

    **Falsch:**

    ![Screenshot des Drehsteuerelements, Grafik, kein Textfeld ](images/ctrl-spin-controls-image2.png)

    In diesem Beispiel wird ein Drehsteuerelement verwendet, um eine dynamische Grafik zu steuern.

-   **Sind zusammenhängende Wertebereiche gültig?** Wenn dies nicht der Fall ist, verwenden Sie stattdessen eine Dropdownliste gültiger Werte.

    ![Screenshot der Dropdownliste ](images/ctrl-spin-controls-image3.png)

    In diesem Beispiel sind nicht alle Laufwerknummern gültig, daher ist eine Dropdownliste eine bessere Wahl.

-   **Ist die Verwendung des Drehsteuerelements praktisch?** Die Verwendung eines Drehsteuerelements ist praktisch für:

    -   Eingabe einer kleinen Zahl, in der Regel unter 100.
    -   Vornehmen kleiner Änderungen an einem vorhandenen oder Standardwert.

    Drehsteuerelemente können zwar für jede numerische Eingabe verwendet werden, sind aber in anderen Situationen als diesen ineffizient.

-   **Ist das Drehsteuerelement hilfreich?** Wird das Steuerelement in einem Kontext verwendet, in dem Benutzer wahrscheinlich ihre Maus verwenden? Falls nicht, sollten Sie ein Drehungssteuerelement optional in Betracht ziehen.
-   **Sind die Dropdownlisten der gleichgeordneten Steuerelemente?** Wenn es andere Dropdownlisten gibt, sollten Sie eine Dropdownliste verwenden, um Konsistenz zu gewährleisten.

    ![Screenshot des Dialogfelds mit Dropdownlisten ](images/ctrl-spin-controls-image4.png)

    In diesem Beispiel kann ein Drehfeld verwendet werden, aber eine Dropdownliste wird aus Konsistenzgründen verwendet.

-   **Sind Touch- oder Stiftbenutzer ein primäres Ziel?** Wenn dies der Fall ist, sollten Sie stattdessen eine Dropdownliste verwenden. Die Pfeiltasten in einem Drehsteuerelement sind zu klein, um effizient mit Toucheingabe oder Stift verwendet zu werden.

Wenn ein Schieberegler oder ein Drehfeld möglich ist, verwenden Sie ein Drehfeld, wenn:

-   Der auf dem Bildschirm verfügbare Platz ist knapp.
-   Ein Benutzer bevorzugt wahrscheinlich die Tastatur.

Verwenden Sie in folgenden Fällen einen Schieberegler:

-   Benutzer profitieren von sofortigem Feedback.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Verwenden Sie Drehsteuerelemente, wann immer sie praktisch und hilfreich sind.** Siehe [Ist dies das richtige Steuerelement?](#is-this-the-right-control)

    -   **Ausnahme:** Um mit anderen Textfeldern auf derselben Benutzeroberfläche konsistent zu sein, verwenden Sie Drehsteuerelemente, auch wenn sie nicht immer praktisch sind.

    **Richtig:**

    ![Screenshot der Drehsteuerelemente für Monat, Tag und Jahr ](images/ctrl-spin-controls-image5.png)

    In diesem Beispiel wird ein Drehsteuerelement mit dem Steuerelement year aus Konsistenzgründen verwendet, obwohl es nicht immer praktisch ist.

    **Falsch:**

    ![Screenshot des Drehsteuerelements "IP-Adresse" ](images/ctrl-spin-controls-image6.png)

    In diesem Beispiel kann das Drehsteuerelement nicht verwendet werden.

-   **Machen Sie ein Drehsteuerelement immer zum "Kasten" des Textfelds.** Dadurch wird das Drehsteuerelement in das Textfeld platziert.

    **Richtig:**

    ![Screenshot des Drehsteuerelements im Textfeld ](images/ctrl-spin-controls-image7.png)

    **Falsch:**

    ![Screenshot des Drehsteuerelements außerhalb des Textfelds ](images/ctrl-spin-controls-image8.png)

    Im richtigen Beispiel wird das Drehsteuerelement in das zugehörige Textfeld platziert.

-   **Deaktivieren Sie ein Drehsteuerelement, wenn das zugehörige Textfeld deaktiviert ist.** Das Drehsteuerelement ist eine ergänzende Eingabemethode – nie die einzige Eingabemethode.

### <a name="values"></a>Werte

-   **Definieren Sie die obere Schaltfläche, um den Wert um eine Einheit zu erhöhen, und die untere Schaltfläche, um eine Einheit zu verringern.** In der Regel ist die Einheit eine Einheit, aber sie sollte die kleinste allgemeine Änderung des Werts sein. Im Idealfall sollte das Drehsteuerelement alle gültigen Werte abdecken, und es sollte bequemer sein, als den Text einzugeben.

    ![Screenshot des Drehsteuerelements "Ränder" ](images/ctrl-spin-controls-image9.png)

    In diesem Beispiel werden durch Klicken auf ein Drehsteuerelement die Werte um 0,1 geändert. Dies ist die kleinste allgemeine Änderung des Werts. Die Verwendung einer kleineren Einheit deckt den Bereich gültiger Werte ab, macht die Drehsteuerelemente jedoch unbrauchbar.

-   **Verwenden Sie das Drehsteuerelement, um die Eingabe auf gültige Werte zu beschränken.** Die Verwendung eines Drehsteuerelements sollte niemals zu einem falschen Wert führen.
-   **Starten Sie den Bereich am Ende eines Bereichs gültiger Werte neu.** Die Metapher des Drehsteuerelements ist, dass der Benutzer ein Rad mit Werten dreht, daher dieses radähnliche Verhalten.
    -   **Ausnahme:** Starten Sie den Bereich nicht neu, wenn der resultierende Wert sicher falsch ist.

        ![Screenshot des Drehsteuerelements "Anzahl von Kopien" ](images/ctrl-spin-controls-image10.png)

        In diesem Beispiel startet das Klicken auf die Schaltfläche mit dem Pfeil nach unten den Bereich nicht neu (indem der Höchstwert erreicht wird), da dieser Wert sicher falsch ist.

-   **Verwenden Sie Text anstelle spezieller numerischer Werte.** Ermöglichen Sie es Benutzern, diese speziellen Werte zu verwenden, anstatt sie kennen zu müssen, und geben Sie sie ein.

    ![Screenshot des Drehsteuerelements "Standbymodus nach (nie)" ](images/ctrl-spin-controls-image11.png)

    In diesem Beispiel ist Nie ein spezieller Wert, aber Benutzer können darauf losgehen.

-   **Wenn der Wert Trennzeichen enthält, sollte das zugeordnete Textfeld über mehrere Eingabefokuspunkte verfügen.** Auf diese Weise können die numerischen Segmente einzeln bearbeitet werden.

    ![Screenshot des Zeitdrehsteuerelements, ausgewählte Minuten ](images/ctrl-spin-controls-image12.png)

    In diesem Beispiel wirkt sich das Drehsteuerelement auf die Werte für Stunden, Minuten, Sekunden und A.M./P.M. aus– je nachdem, welcher Wert den Fokus hat.

-   **Wenn der Wert Einheiten enthält, verwenden Sie das Drehsteuerelement, um diese Einheiten ebenfalls zu ändern.**

    ![Screenshot des Zeitdrehsteuerelements, "a.m." Ausgewählt ](images/ctrl-spin-controls-image13.png)

    In diesem Beispiel kann das Drehsteuerelement verwendet werden, um Einheiten zu ändern.

## <a name="labels"></a>Bezeichnungen

-   Wenden Sie die [Textfeld-Bezeichnungsrichtlinien](ctrl-text-boxes.md) an, um das zugeordnete Textfeld zu beschriften. Drehungssteuerelemente werden nie direkt bezeichnet.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Drehungssteuerelemente:

-   Verweisen Sie nicht auf Drehungssteuerelemente in der Benutzerdokumentation. Verweisen Sie stattdessen auf die Bezeichnung des zugeordneten Textfelds.
-   Informationen zu Drehungssteuerelementen und Drehfeldern finden Sie nur in der Programmierung und in anderen technischen Dokumentationen.

Beispiel: Geben Sie im **Feld Datum** den Teil des Datums ein, den Sie ändern möchten, oder wählen Sie diesen aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Glossar](glossary.md)
</dt> </dl>

 

 