---
title: Schieberegler (Entwurfsgrundlagen)
description: Mit einem Schieberegler können Benutzer aus einem kontinuierlichen Wertebereich auswählen.
ms.assetid: dee70fbc-6f18-43c7-9d41-4e97eac41e53
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 73c6ae0cc490c338ec552d0e23e829c791689f6f822d324feaa863ccbb441d73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349893"
---
# <a name="sliders-design-basics"></a>Schieberegler (Entwurfsgrundlagen)

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Mit einem Schieberegler können Benutzer aus einem kontinuierlichen Wertebereich auswählen. Ein Schieberegler verfügt über einen Balken, der den Bereich und einen Indikator anzeigt, der den aktuellen Wert anzeigt. Optionale Teilstriche zeigen Werte an.

![Abbildung mit Balken, Schiebereglern und Teilstrichen ](images/ctrl-sliders-image1.png)

Ein typischer Schieberegler.

> [!Note]  
> Richtlinien zum [Layout](vis-layout.md) werden in einem separaten Artikel vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Verwenden Sie einen Schieberegler, wenn Sie möchten, dass Ihre Benutzer **definierte, zusammenhängende Werte (z. B. Lautstärke oder Helligkeit) oder einen Bereich diskreter Werte (z. B. Bildschirmauflösungseinstellungen) festlegen können.**

Eine Schieberegler ist eine gute Wahl, wenn Sie wissen, dass Benutzer den Wert als relative Anzahl betrachten und nicht als numerischen Wert. So denken Benutzer beispielsweise beim Festlegen der Audiolautstärke an "niedrig" oder "mittel", aber nicht an Werte wie "2" oder "5".

Orientieren Sie sich an folgenden Fragen:

-   **Handelt es sich bei der Einstellung um eine relative Anzahl?** Wenn dies nicht der Fall ist, verwenden Sie [Optionsfelder](ctrl-radio-buttons.md)oder eine [Dropdownliste](/windows/desktop/uxguide/ctrl-drop) oder [eine Einzelauswahlliste.](ctrl-list-boxes.md)
-   **Handelt es sich bei der Einstellung um einen exakten, bekannten numerischen Wert?** Wenn ja, verwenden Sie ein [numerisches Textfeld.](ctrl-text-boxes.md)
-   **Wäre es für Benutzer hilfreich, sofort Feedback zur Auswirkung von Einstellungsänderungen zu erhalten?** Wenn ja, verwenden Sie einen Schieberegler. Beispielsweise können Benutzer eine Farbe leichter auswählen, wenn sie sofort sehen, wie sich Änderungen an den Werten für Farbton, Sättigung oder Leuchtdichte auswirken.
-   **Weist die Einstellung einen Bereich aus vier oder mehr Werten auf?** Ist dies nicht der Fall, verwenden Sie stattdessen Optionsfelder.
-   **Können Benutzer den Wert ändern?** Schieberegler dienen zur Benutzerinteraktion. Wenn ein Benutzer den Wert nie ändern kann, verwenden Sie stattdessen ein schreibgeschütztes [Textfeld.](ctrl-text-boxes.md)

Wenn ein Schieberegler oder ein numerisches Textfeld möglich ist, verwenden Sie ein numerisches Textfeld, wenn:

-   Der auf dem Bildschirm verfügbare Platz ist knapp.
-   Ein Benutzer bevorzugt wahrscheinlich die Tastatur.

Verwenden Sie in folgenden Fällen einen Schieberegler:

-   Benutzer profitieren von sofortigem Feedback.

## <a name="guidelines"></a>Richtlinien

-   **Verwenden Sie eine natürliche Ausrichtung.** Wenn der Schieberegler beispielsweise einen echten Wert darstellt, der normalerweise vertikal angezeigt wird (z. B. eine Temperatur), verwenden Sie die vertikale Ausrichtung.
-   **Richten Sie den Schieberegler so aus, dass er die Kultur Ihrer Benutzer widerspiegelt.** Beispielsweise lesen die kulturellen Kulturen von links nach rechts. Legen Sie also bei horizontalen Schiebereglern das untere Ende des Bereichs links und das obere Ende auf der rechten Seite ab. Für Kulturen, die von rechts nach links lesen, tun Sie das Gegenteil.
-   **Passen Sie die Größe des Steuerelements an, sodass ein Benutzer den gewünschten Wert problemlos festlegen kann.** Stellen Sie für Einstellungen mit separaten Werten sicher, dass der Benutzer jeden Wert einfach mithilfe der Maus auswählen kann.
-   **Erwägen Sie die Verwendung einer nicht linearen Skala, wenn der Wertebereich groß ist und Benutzer wahrscheinlich Werte an einem Ende des Bereichs auswählen.** Der Zeitwert kann beispielsweise 1 Minute, 1 Stunde, 1 Tag oder 1 Monat sein.
-   **Geben Sie nach Möglichkeit sofort Feedback, während oder nachdem ein Benutzer eine Auswahl getroffen hat.** Beispielsweise gibt der Microsoft Windows Lautstärkeregler aus, um die resultierende Audiolautstärke anzugeben.
-   **Verwenden Sie Bezeichnungen, um den Wertebereich anzuzeigen.**

    **Ausnahme:** Wenn der Schieberegler vertikal ausgerichtet ist und die obere Bezeichnung Maximum, High, More oder equivalent lautet, können Sie die anderen Bezeichnungen weglassen, da die Bedeutung klar ist.

    ![Abbildung eines vertikalen Schiebereglers ](images/ctrl-sliders-image2.png)

    In diesem Beispiel macht die vertikale Ausrichtung des Schiebereglers die Bereichsbezeichnungen überflüssig.

-   **Verwenden Sie Teilstriche, wenn Benutzer den ungefähren Wert der Einstellung kennen müssen.**
-   **Verwenden Sie Teilstriche und eine Wertbezeichnung, wenn Benutzer den genauen Wert der von ihnen gewählten Einstellung kennen müssen.** Verwenden Sie immer eine Wertbezeichnung, wenn ein Benutzer die Einheiten kennen muss, um die Einstellung sinnvoll zu gestalten.

    ![Abbildung des Schiebereglers mit ausgewählter Anzahl von Pixeln ](images/ctrl-sliders-image3.png)

    In diesem Beispiel wird eine Bezeichnung verwendet, um den ausgewählten Wert eindeutig anzugeben.

-   **Platzieren Sie bei horizontal ausgerichteten Schiebereglern Teilstriche unter dem Schieberegler.** Platzieren Sie bei vertikal ausgerichteten Schiebereglern teilstriche rechts für westländische Kulturen. Für Kulturen, die von rechts nach links lesen, tun Sie das Gegenteil.
-   **Platzieren Sie die Wertbezeichnung vollständig unter dem Schieberegler-Steuerelement, damit die Beziehung klar ist.**

    **Falsch:**

    ![Abbildung einer Bezeichnung, die länger als der Schieberegler ist ](images/ctrl-sliders-image4.png)

    In diesem Beispiel wird die Wertbezeichnung nicht unter dem Schieberegler ausgerichtet.

-   **Wenn Sie einen Schieberegler deaktivieren, deaktivieren Sie auch alle zugeordneten Bezeichnungen.**
-   **Verwenden Sie nicht sowohl einen Schieberegler als auch ein numerisches Textfeld für dieselbe Einstellung.** Verwenden Sie nur das geeignetere Steuerelement.

    **Ausnahme:** Verwenden Sie beide Steuerelemente, wenn der Benutzer sowohl sofortiges Feedback als auch die Möglichkeit benötigt, einen genauen numerischen Wert festzulegen.

-   **Verwenden Sie einen Schieberegler nicht als Statusanzeige.**
-   **Ändern Sie die Größe des Schiebereglerindikators nicht von der Standardgröße.**

    **Falsch:**

    ![Abbildung des Schiebereglers, der kleiner als der Standardwert ist ](images/ctrl-sliders-image5.png)

    In diesem Beispiel wird eine Größe verwendet, die kleiner als der Standardwert ist.

    **Richtig:**

    ![Abbildung des Standardschiebereglers ](images/ctrl-sliders-image6.png)

    In diesem Beispiel wird die Standardgröße verwendet.

-   **Beschriften Sie nicht jedes Teilstrichs.**

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größen- und Abstände

![Abbildung der empfohlenen Größen- und Abstandsgröße des Schiebereglers ](images/ctrl-sliders-image7.png)

Empfohlene Größen- und Abstände für Schieberegler.

## <a name="labels"></a>Bezeichnungen

### <a name="slider-labels"></a>Schiebereglerbeschriftungen

-   Verwenden Sie eine statische Textbezeichnung, die mit einem Doppelpunkt endet, oder eine Gruppenfeldbezeichnung ohne Endpunktion.
-   Weisen Sie jeder Bezeichnung einen eindeutigen Zugriffsschlüssel zu. Zuweisungsrichtlinien finden Sie unter [Tastatur.](inter-keyboard.md)
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Positionieren Sie die Beschriftung des Schiebereglers entweder links vom Schieberegler oder darüber und am linken Rand des Schiebereglers ausgerichtet (oder der bezeichner des linken Bereichs, falls vorhanden).

### <a name="range-labels"></a>Bereichsbeschriftungen

-   Beschriften Sie die beiden Enden des Schiebereglerbereichs, sofern dies nicht aufgrund einer vertikalen Ausrichtung unnötig ist.
-   Verwenden Sie nach Möglichkeit nur das Wort für jede Bezeichnung.
-   Verwenden Sie keine Interpunktion am Ende.
-   Stellen Sie sicher, dass die Beschriftungen aussagekräftig und parallel sind. Beispiele: „Maximum/Minimum“, „Mehr/Weniger“, „Niedrig/Hoch“, „Leise/Laut“.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Weisen Sie keine Zugriffsschlüssel zu.

### <a name="value-labels"></a>Wertbeschriftungen

-   Wenn Sie eine Wertbeschriftung benötigen, zeigen Sie sie unter dem Schieberegler an.
-   Zentrieren Sie den Text relativ zum Steuerelement, und schließen Sie die Einheiten ein (beispielsweise Pixel).

    ![Abbildung der Bezeichnung, die unter dem Schieberegler zentriert ist ](images/ctrl-sliders-image8.png)

    In diesem Beispiel wird die Wertbezeichnung unter dem Schieberegler zentriert und enthält die Einheiten.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Schieberegler:

-   Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Großschreibung, und schließen Sie den Wortschieberegler ein. Schließen Sie keinen Unterstrich oder Doppelpunkt des Zugriffsschlüssels ein.
-   Um die Benutzerinteraktion zu beschreiben, verwenden Sie move.
-   Formatieren Sie die Bezeichnung nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

Beispiel: Um die Bildschirmauflösung zu erhöhen, verschieben Sie den **Bildschirmauflösungsschieberegler** nach rechts.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Glossar](glossary.md)
</dt> </dl>

 

 