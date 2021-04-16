---
title: Schieberegler (Entwurfs Grundlagen)
description: Mit einem Schieberegler können Benutzer aus einem kontinuierlichen Bereich von Werten auswählen.
ms.assetid: dee70fbc-6f18-43c7-9d41-4e97eac41e53
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7ff9791ab49c338e4c11e014a3e996771571add9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104558353"
---
# <a name="sliders-design-basics"></a>Schieberegler (Entwurfs Grundlagen)

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Mit einem Schieberegler können Benutzer aus einem kontinuierlichen Bereich von Werten auswählen. Ein Schieberegler verfügt über einen Balken, der den Bereich und einen Indikator mit dem aktuellen Wert anzeigt. Optionale Teil Striche zeigen Werte an.

![Darstellung von Balken, Schieberegler und Teil Strichen ](images/ctrl-sliders-image1.png)

Ein typischer Schieberegler.

> [!Note]  
> Richtlinien für das [Layout](vis-layout.md) werden in einem separaten Artikel dargestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Verwenden Sie einen Schieberegler, wenn die Benutzer in der Lage sein sollen **, definierte, zusammenhängende Werte (z. b. Volume oder Helligkeit) oder einen Bereich diskreter Werte (z. b. Bildschirm Auflösungseinstellungen) festzulegen.**

Eine Schieberegler ist eine gute Wahl, wenn Sie wissen, dass Benutzer den Wert als relative Anzahl betrachten und nicht als numerischen Wert. So denken Benutzer beispielsweise beim Festlegen der Audiolautstärke an "niedrig" oder "mittel", aber nicht an Werte wie "2" oder "5".

Orientieren Sie sich an folgenden Fragen:

-   **Handelt es sich bei der Einstellung um eine relative Anzahl?** Wenn dies nicht der [Fall ist, verwenden Sie](ctrl-radio-buttons.md)Options Felder oder eine [Dropdown](/windows/desktop/uxguide/ctrl-drop) Liste oder eine [einzelne Auswahlliste](ctrl-list-boxes.md).
-   **Handelt es sich bei der Einstellung um einen exakten, bekannten numerischen Wert?** Wenn dies der Fall ist, verwenden Sie [numerische Textfelder](ctrl-text-boxes.md).
-   **Wäre es für Benutzer hilfreich, sofort Feedback zur Auswirkung von Einstellungsänderungen zu erhalten?** Wenn ja, verwenden Sie einen Schieberegler. Beispielsweise können Benutzer eine Farbe leichter auswählen, wenn sie sofort sehen, wie sich Änderungen an den Werten für Farbton, Sättigung oder Leuchtdichte auswirken.
-   **Weist die Einstellung einen Bereich aus vier oder mehr Werten auf?** Ist dies nicht der Fall, verwenden Sie stattdessen Optionsfelder.
-   **Können Benutzer den Wert ändern?** Schieberegler dienen zur Benutzerinteraktion. Wenn ein Benutzer den Wert nicht jemals ändern kann, verwenden Sie stattdessen ein Schreib geschütztes [Textfeld](ctrl-text-boxes.md) .

Wenn ein Schieberegler oder ein numerisches Textfeld möglich ist, verwenden Sie ein numerisches Textfeld, wenn Folgendes gilt:

-   Der auf dem Bildschirm verfügbare Platz ist knapp.
-   Ein Benutzer wird die Verwendung der Tastatur wahrscheinlich bevorzugen.

Verwenden Sie in folgenden Fällen einen Schieberegler:

-   Benutzer profitieren von sofortigem Feedback.

## <a name="guidelines"></a>Richtlinien

-   **Verwenden Sie eine natürliche Ausrichtung.** Wenn der Schieberegler beispielsweise einen echten Wert darstellt, der normalerweise vertikal angezeigt wird (z. B. eine Temperatur), verwenden Sie die vertikale Ausrichtung.
-   **Orientieren Sie sich am Schieberegler, um die Kultur ihrer Benutzer widerzuspiegeln.** Wenn z. b. westliche Kulturen von links nach rechts gelesen werden, legen Sie bei horizontalen Schiebereglern das niedrige Ende des Bereichs auf der linken Seite und das hohe Ende auf der rechten Seite ab. Führen Sie für Kulturen, die von rechts nach links gelesen werden, das Gegenteil aus.
-   **Legen Sie die Größe des Steuer Elements so fest, dass ein Benutzer leicht den gewünschten Wert festlegen kann.** Stellen Sie für Einstellungen mit separaten Werten sicher, dass der Benutzer jeden Wert einfach mithilfe der Maus auswählen kann.
-   **Es empfiehlt sich, eine nichtlineare Skala zu verwenden, wenn der Wertebereich groß ist und Benutzer wahrscheinlich Werte an einem Ende des Bereichs auswählen.** Der Uhrzeitwert kann z. b. 1 Minute, 1 Stunde, 1 Tag oder 1 Monat betragen.
-   **Jedes Mal, wenn ein Benutzer eine Auswahl getroffen hat, sollten Sie sofort Feedback abgeben.** Beispielsweise wird mit der Microsoft Windows-volumesteuerung das resultierende audiovolume angegeben.
-   **Verwenden Sie Bezeichnungen, um den Wertebereich anzuzeigen.**

    **Ausnahme:** Wenn der Schieberegler vertikal ausgerichtet und die oberste Bezeichnung "Maximum", "High", "More" oder "äquivalente" ist, können Sie die anderen Bezeichnungen weglassen, da die Bedeutung "Clear" ist.

    ![Abbildung eines vertikalen Schiebereglers ](images/ctrl-sliders-image2.png)

    In diesem Beispiel macht die vertikale Ausrichtung des Schiebereglers die Bereichs Bezeichnungen unnötig.

-   **Verwenden Sie Teil Striche, wenn Benutzer den ungefähren Wert der Einstellung kennen müssen.**
-   **Verwenden Sie Teil Striche und eine Wert Bezeichnung, wenn Benutzer den genauen Wert der gewählten Einstellung kennen müssen.** Verwenden Sie immer eine Wert Bezeichnung, wenn ein Benutzer die Einheiten kennen muss, damit die Einstellung sinnvoll ist.

    ![Abbildung des Schiebereglers mit angezeigter Anzahl von Pixeln ](images/ctrl-sliders-image3.png)

    In diesem Beispiel wird eine Bezeichnung verwendet, um den ausgewählten Wert eindeutig anzugeben.

-   **Platzieren Sie bei horizontal ausgerichteten Schiebereglern Teil Striche unter dem Schieberegler.** Bei vertikal ausgerichteten Schiebereglern platzieren Sie Teil Striche für westliche Kulturen nach rechts. Führen Sie für Kulturen, die von rechts nach links gelesen werden, das Gegenteil aus.
-   **Platzieren Sie die Wert Bezeichnung vollständig unter dem Schieberegler-Steuerelement, damit die Beziehung eindeutig ist.**

    **Falsch:**

    ![Abbildung einer Bezeichnung, die länger als der Schieberegler ist ](images/ctrl-sliders-image4.png)

    In diesem Beispiel wird die Wert Bezeichnung nicht am Schieberegler ausgerichtet.

-   **Wenn Sie einen Schieberegler deaktivieren, deaktivieren Sie auch alle zugeordneten Bezeichnungen.**
-   **Verwenden Sie für dieselbe Einstellung nicht sowohl einen Schieberegler als auch ein numerisches Textfeld.** Verwenden Sie nur das geeignetere Steuerelement.

    **Ausnahme:** Verwenden Sie beide Steuerelemente, wenn der Benutzer sofortiges Feedback benötigt und einen exakten numerischen Wert festlegen kann.

-   **Verwenden Sie einen Schieberegler nicht als Statusanzeige.**
-   **Ändern Sie nicht die Größe des Schieberegler-Indikators von der Standardgröße.**

    **Falsch:**

    ![Abbildung des Schiebereglers, der kleiner ist als der Standardwert ](images/ctrl-sliders-image5.png)

    In diesem Beispiel wird eine Größe verwendet, die kleiner als der Standardwert ist.

    **Richtig:**

    ![Abbildung mit dem Standard Schieberegler ](images/ctrl-sliders-image6.png)

    In diesem Beispiel wird die Standardgröße verwendet.

-   **Markieren Sie nicht jeden Teil Strich.**

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstände

![Abbildung der empfohlenen schiebereglergröße und des Abstands ](images/ctrl-sliders-image7.png)

Empfohlene Größe und Abstände für Schieberegler.

## <a name="labels"></a>Bezeichnungen

### <a name="slider-labels"></a>Schiebereglerbeschriftungen

-   Verwenden Sie eine statische Text Bezeichnung, die mit einem Doppelpunkt endet, oder eine Gruppenfeld Bezeichnung ohne endende Interpunktions Zeichen.
-   Weisen Sie jeder Bezeichnung einen eindeutigen Zugriffsschlüssel zu. Informationen zu Zuweisungs Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Positionieren Sie die Schieberegler-Bezeichnung entweder auf der linken Seite des Schiebereglers oder höher, und richten Sie am linken Rand des Schiebereglers (oder im linken Bereichs Bezeichner, falls vorhanden) an.

### <a name="range-labels"></a>Bereichsbeschriftungen

-   Beschriften Sie die beiden Enden des Schiebereglerbereichs, sofern dies nicht aufgrund einer vertikalen Ausrichtung unnötig ist.
-   Verwenden Sie nach Möglichkeit nur Word für jede Bezeichnung.
-   Verwenden Sie keine Interpunktion am Ende.
-   Stellen Sie sicher, dass die Beschriftungen aussagekräftig und parallel sind. Beispiele: „Maximum/Minimum“, „Mehr/Weniger“, „Niedrig/Hoch“, „Leise/Laut“.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Weisen Sie keine Zugriffsschlüssel zu.

### <a name="value-labels"></a>Wertbeschriftungen

-   Wenn Sie eine Wertbeschriftung benötigen, zeigen Sie sie unter dem Schieberegler an.
-   Zentrieren Sie den Text relativ zum Steuerelement, und schließen Sie die Einheiten ein (beispielsweise Pixel).

    ![Abbildung der Bezeichnung, zentriert mit dem Schieberegler ](images/ctrl-sliders-image8.png)

    In diesem Beispiel wird die Wert Bezeichnung unter dem Schieberegler zentriert und umfasst die Einheiten.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Schieberegler:

-   Verwenden Sie den genauen Bezeichnungs Text, einschließlich der Groß-und Kleinschreibung, und schließen Sie den Schieberegler ein Fügen Sie den Unterstrich oder Doppelpunkt des Zugriffsschlüssels nicht ein.
-   Verwenden Sie Move, um die Benutzerinteraktion zu beschreiben.
-   Formatieren Sie nach Möglichkeit die Bezeichnung mit fettem Text. Andernfalls sollten Sie die Bezeichnung nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: um die Bildschirmauflösung zu vergrößern, verschieben Sie den Schieberegler für die **Bildschirmauflösung** nach rechts.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Glossar](glossary.md)
</dt> </dl>

 

 