---
title: Drehungssteuerelemente
description: Mit einem Drehungssteuerfeld können Benutzer auf Pfeilschaltflächen klicken, um den Wert inkrementell innerhalb des zugehörigen numerischen Textfelds zu ändern.
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
# <a name="spin-controls"></a>Drehungssteuerelemente

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Mit einem Drehungssteuerfeld können Benutzer auf Pfeilschaltflächen klicken, um den Wert inkrementell innerhalb des zugeordneten [numerischen Textfelds zu ändern.](ctrl-text-boxes.md) Der Begriff Drehfeld bezieht sich auf die Kombination aus einem Textfeld und dem zugehörigen Drehungssteuerfeld.

![Screenshot des Drehungssteuerfelds und des Textfelds ](images/ctrl-spin-controls-image1.png)

Ein typisches Drehfeld.

Benutzer bevorzugen häufig Drehsteuerelemente, da sie Änderungen vornehmen können, ohne ihre Hände mit der Maus zu bewegen. Wenn das Drehungssteuerfeld mit einem Textfeld gekoppelt ist, können Benutzer Eingaben direkt in das Textfeld eingeben oder einfügen. Daher ist die Verwendung des Drehungssteuerfelds optional.

Drehungssteuerelemente werden zwar für numerische Eingaben verwendet, die Eingabe muss jedoch keine reine ganze Zahl sein. Die Eingabe kann Dezimalzahlen sein und negative Vorzeichen, Trennzeichen (z. B. Doppelpunkte oder Bindestriche) und Einheitenmodifizierer enthalten.

> [!Note]  
> Richtlinien für [Textfelder und](ctrl-text-boxes.md) [Layout werden](vis-layout.md) in separaten Artikeln vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Wird das Steuerelement für numerische Eingaben verwendet?** Wenn dies nicht der Fall [](/windows/desktop/uxguide/ctrl-drop) ist, verwenden Sie ein anderes Steuerelement, z. B. eine Dropdownliste oder einen Schieberegler, [](ctrl-sliders.md)um einen festen Satz von Werten auszuwählen. Verwenden Sie Scrollleisten für das Scrollen.
-   **Stellen sich Benutzer den Wert als relative Menge und nicht als numerischen Wert vor?** Falls ja, verwenden Sie stattdessen einen Schieberegler. Verwenden Sie Drehfelder nur für genaue, bekannte numerische Werte. So denken Benutzer beispielsweise beim Festlegen der Audiolautstärke an "niedrig" oder "mittel", aber nicht an Werte wie "2" oder "5".
-   **Ist das Steuerelement mit einem Textfeld gekoppelt?** Falls nicht, verwenden Sie nicht . Spin-Steuerelemente sollten nicht allein oder mit anderen Steuerelementtypen außer einem Textfeld verwendet werden.

    **Falsch:**

    ![Screenshot des Drehungssteuerfelds, Grafik, kein Textfeld ](images/ctrl-spin-controls-image2.png)

    In diesem Beispiel wird ein Drehungssteuer steuerelement verwendet, um eine dynamische Grafik zu steuern.

-   **Sind zusammenhängende Wertbereiche gültig?** Wenn dies nicht der Fall ist, verwenden Sie stattdessen eine Dropdownliste gültiger Werte.

    ![Screenshot der Dropdownliste ](images/ctrl-spin-controls-image3.png)

    In diesem Beispiel sind nicht alle Laufwerknummern gültig, daher ist eine Dropdownliste die bessere Wahl.

-   **Ist die Verwendung des Drehungssteuer steuerelements praktisch?** Die Verwendung eines Drehungssteuer steuerelements ist für:

    -   Eingabe einer kleinen Zahl, in der Regel unter 100.
    -   Vornehmen kleiner Änderungen an einem vorhandenen oder Standardwert.

    Drehungssteuerelemente können zwar für beliebige numerische Eingaben verwendet werden, sind jedoch in anderen Situationen als diesen ineffizient.

-   **Ist das Drehungssteuer steuerelement hilfreich?** Wird das Steuerelement in einem Kontext verwendet, in dem Benutzer wahrscheinlich ihre Maus verwenden? Wenn dies nicht der Dert ist, sollten Sie ein Drehungssteuersteuersystem als optional betrachten.
-   **Sind die Dropdownlisten für gleichgeordnete Steuerelemente?** Wenn es andere Dropdownlisten gibt, sollten Sie eine Dropdownliste verwenden, um Konsistenz zu gewährleisten.

    ![Screenshot des Dialogfelds mit Dropdownlisten ](images/ctrl-spin-controls-image4.png)

    In diesem Beispiel kann ein Drehfeld verwendet werden, aber aus Konsistenz-Grund wird eine Dropdownliste verwendet.

-   **Sind Touch- oder Stiftbenutzer ein primäres Ziel?** Wenn dies der Fall ist, sollten Sie stattdessen eine Dropdownliste verwenden. Die Pfeilschaltflächen in einem Drehungssteuer steuerelement sind zu klein, um sie effizient mit touch oder einem Stift verwenden zu können.

Wenn ein Schieberegler oder ein Drehfeld möglich ist, verwenden Sie ein Drehfeld, wenn:

-   Der auf dem Bildschirm verfügbare Platz ist knapp.
-   Ein Benutzer bevorzugt wahrscheinlich die Verwendung der Tastatur.

Verwenden Sie in folgenden Fällen einen Schieberegler:

-   Benutzer profitieren von sofortigem Feedback.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Verwenden Sie Drehungssteuerelemente, wenn sie praktisch und hilfreich sind.** Siehe [Ist dies das richtige Steuerelement?](#is-this-the-right-control)

    -   **Ausnahme:** Um mit anderen Textfeldern auf derselben Benutzeroberfläche konsistent zu sein, verwenden Sie Drehungssteuerelemente, auch wenn sie nicht immer praktikabel sind.

    **Richtig:**

    ![Screenshot der Drehungssteuerelemente "Monat", "Tag", "Jahr" ](images/ctrl-spin-controls-image5.png)

    In diesem Beispiel wird ein Drehungssteuer steuerelement mit der Jahressteuerung verwendet, um Konsistenz zu gewährleisten, auch wenn es nicht immer praktikabel ist.

    **Falsch:**

    ![Screenshot des DREH-Steuerelements für IP-Adressen ](images/ctrl-spin-controls-image6.png)

    In diesem Beispiel ist das Drehungssteuer steuerelement nicht verwendbar.

-   **Machen Sie ein Drehungssteuerfeld immer als "Schachtelung" des Textfelds.** Dadurch wird das Drehungssteuerfeld in das Textfeld eingefügt.

    **Richtig:**

    ![Screenshot des Drehungssteuerfelds im Textfeld ](images/ctrl-spin-controls-image7.png)

    **Falsch:**

    ![Screenshot des Drehungssteuerfelds außerhalb des Textfelds ](images/ctrl-spin-controls-image8.png)

    Im richtigen Beispiel wird das Drehungssteuerfeld in das zugeordnete Textfeld eingefügt.

-   **Deaktivieren Sie ein Drehungssteuerfeld, wenn das zugeordnete Textfeld deaktiviert ist.** Das Drehungssteuerfeld ist eine zusätzliche Eingabemethode– nie die einzige Eingabemethode.

### <a name="values"></a>Werte

-   **Definieren Sie die obere Schaltfläche, um den Wert um eine Einheit zu erhöhen, und die untere Schaltfläche, um eine Einheit zu verringern.** In der Regel ist die Einheit eine Einheit, aber es sollte die kleinste häufige Änderung des Werts sein. Im Idealfall sollte das Drehungssteuerfeld alle gültigen Werte abdecken, und es sollte bequemer als die Eingabe im Text sein.

    ![Screenshot: Drehungssteuerung "Ränder" ](images/ctrl-spin-controls-image9.png)

    In diesem Beispiel ändert das Klicken auf ein Drehungssteuer steuerelement die Werte um 0,1. Dies ist die kleinste häufige Änderung des Werts. Die Verwendung einer kleineren Einheit würde den Bereich gültiger Werte abdecken, aber die Drehungssteuerelemente unbrauchbar machen.

-   **Verwenden Sie das Drehungssteuerfeld, um die Eingabe auf gültige Werte zu beschränken.** Die Verwendung eines Drehungssteuerwerts sollte nie zu einem falschen Wert führen.
-   **Starten Sie den Bereich am Ende eines gültigen Wertebereichs neu.** Die Drehungssteuermetapher ist, dass der Benutzer ein Werterad dreht, daher ist dieses radbasierte Verhalten.
    -   **Ausnahme:** Starten Sie den Bereich nicht neu, wenn der resultierende Wert sicher falsch ist.

        ![Screenshot des Drehungssteuerzeichens "Anzahl von Kopien" ](images/ctrl-spin-controls-image10.png)

        In diesem Beispiel wird der Bereich durch Klicken auf die Nach-unten-Pfeilschaltfläche nicht neu gestartet (indem auf den Maximalwert geklickt wird), da dieser Wert sicher falsch ist.

-   **Verwenden Sie Text anstelle spezieller numerischer Werte.** Ermöglichen Sie es Benutzern, diese speziellen Werte zu verwenden, anstatt sie kennen und eingeben zu müssen.

    ![Screenshot des Drehsteuerungsmodus "Sleep after (never)" ](images/ctrl-spin-controls-image11.png)

    In diesem Beispiel ist Nie ein spezieller Wert, aber Benutzer können ihn drehen.

-   **Wenn der Wert Trennzeichen enthält, sollte das zugeordnete Textfeld über mehrere Eingabefokuspunkte verfügen.** Dadurch können die numerischen Segmente einzeln bearbeitet werden.

    ![Screenshot des Zeitspin-Steuerelements, ausgewählte Minuten ](images/ctrl-spin-controls-image12.png)

    In diesem Beispiel wirkt sich das Drehungssteuerwert auf die Werte für Stunden, Minuten, Sekunden und A.M./P.M. aus– unabhängig davon, welcher Wert den Fokus besitzt.

-   **Wenn der Wert Einheiten hat, verwenden Sie auch das Drehungssteuer steuerelement, um diese Einheiten zu ändern.**

    ![Screenshot des Zeitspin-Steuerelements "a.m." Ausgewählt ](images/ctrl-spin-controls-image13.png)

    In diesem Beispiel kann das Drehungssteuer steuerelement verwendet werden, um Einheiten zu ändern.

## <a name="labels"></a>Bezeichnungen

-   Wenden Sie die Richtlinien für die [Textfeldbeschriftung](ctrl-text-boxes.md) an, um das zugeordnete Textfeld zu bezeichnen. Drehsteuerelemente werden nie direkt bezeichnet.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Drehsteuerelemente:

-   Verweisen Sie in der Benutzerdokumentation nicht auf Drehsteuerelemente. Verweisen Sie stattdessen auf die Bezeichnung des zugeordneten Textfelds.
-   Informationen zu Drehsteuerelementen und Drehfeldern finden Sie nur in der Programmierung und in anderen technischen Dokumentationen.

Beispiel: Geben Sie im Feld **Datum** den Teil des Datums ein, den Sie ändern möchten, oder wählen Sie diesen aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Glossar](glossary.md)
</dt> </dl>

 

 