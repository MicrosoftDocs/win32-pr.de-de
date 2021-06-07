---
title: Grafische Elemente
description: Grafische Elemente zeigen Beziehungen, Hierarchien und Hervorhebungen visuell an. Sie umfassen Hintergründe, Banner, Brillen, Aggregatoren, Trennzeichen, Schatten und Ziehpunkte.
ms.assetid: f9e741e9-a72e-4bdb-bd95-8916c7cf344f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 03db1f7a90554848f71cd43cdfa769597b71cd2f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444631"
---
# <a name="graphic-elements"></a>Grafische Elemente

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

*Grafische Elemente* zeigen Beziehungen, Hierarchien und Hervorhebungen visuell an. Sie umfassen Hintergründe, Banner, Brillen, Aggregatoren, Trennzeichen, Schatten und Ziehpunkte.

![Screenshot des Windows-Explorers mit Schatten usw. ](images/vis-graphic-image1.png)

Ein Beispiel mit mehreren Typen von grafischen Elementen.

Grafische Elemente sind in der Regel nicht interaktiv. Trennzeichen sind jedoch interaktiv für inhalte, deren Größe geändert werden kann, und Handles sind Grafiken, die Interaktivität zeigen.

**Hinweis:** Richtlinien im Zusammenhang mit [Gruppenfeldern,](ctrl-group-boxes.md) [Animationen,](vis-animations.md) [Symbolen](vis-icons.md)und [Branding](exper-branding.md) werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Grafikelemente sind zwar ein sicheres visuelles Mittel zum Angeben von Beziehungen, aber die übermäßig hohe Wiederverwendung sorgt für visuelle Überladenheit und reduziert den verfügbaren Platz auf einer Oberfläche. Sie sollten nur selten verwendet werden.

Ein Designtrend in Microsoft Windows ist eine einfachere, übersichtlichere Darstellung, indem unnötige Grafiken und Linien beseitigt werden.

Berücksichtigen Sie die folgenden Fragen, um zu entscheiden, ob ein grafikgrafisches Element erforderlich ist:

-   **Ist die Darstellung und Kommunikation des Entwurfs ohne das -Element genauso klar und effektiv?** Wenn ja, entfernen Sie es.
-   **Können Sie die Beziehungen effektiv nur mithilfe des Layouts kommunizieren?** Verwenden Sie in diesem Falle stattdessen [layout.](vis-layout.md) Sie können verwandte Steuerelemente nebeneinander platzieren und zusätzliche Abstände zwischen nicht verknüpften Steuerelementen platzieren. Sie können den Einzug auch verwenden, um hierarchische Beziehungen anzuzeigen.

![Screenshot eines Layouts mit vier Symbolen ](images/vis-graphic-image2.png)

In diesem Beispiel wird layout allein verwendet, um Steuerelementbeziehungen anzuzeigen.

-   **Ist die Kommunikation ohne Text effektiv?** Verwenden Sie andernfalls ein [Gruppenfeld,](ctrl-group-boxes.md)bezeichnetes Trennzeichen oder eine andere [Bezeichnung.](text-ui.md)

## <a name="usage-patterns"></a>Verwendungsmuster

Grafische Elemente weisen mehrere Verwendungsmuster auf:



| Element                                                                                                              |   BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grafische Abbildungen**<br/> verwenden, um eine Idee visuell zu kommunizieren. <br/>                         | Grafische Abbildungen ähneln Symbolen, außer dass sie eine beliebige Größe aufweisen können und in der Regel nicht interaktiv sind. <br/> ![Screenshot: Diagramm des CPU-Nutzungsverlaufs ](images/vis-graphic-image3.png)<br/> In diesem Beispiel wird eine grafische Abbildung verwendet, um die Art eines Features vorzuschlagen.<br/>                                                                                                                                                                                                        |
| **Hintergründe**<br/> verwenden, um verschiedene Inhaltstypen hervorzuheben oder zu deaktivieren. <br/>           | Hintergrundinformationen können verwendet werden, um wichtige Inhalte hervorzuheben. <br/> ![Screenshot der Virusmeldung auf rotem Hintergrund ](images/vis-graphic-image4.png)<br/> In diesem Beispiel wird ein Hintergrund verwendet, um eine wichtige Aufgabe hervorzuheben.<br/> -Hintergründe können auch verwendet werden, um sekundären Inhalt zu deaktivieren. <br/> ![Screenshot der Systemsteuerungselemente ](images/vis-graphic-image5.png)<br/> In diesem Beispiel werden sekundäre Aufgaben durch die Suche in einem Aufgabenbereich nicht mehr hervorgehoben.<br/>   |
| **Banner**<br/> wird verwendet, um einen wichtigen Status anzugeben. <br/>                                         | Im Gegensatz zu Hintergründen wird bei Bannern in erster Linie eine einzelne Textzeichenfolge hervorgehoben. <br/> ![Screenshot des Banners mit Einstellungsinformationen ](images/vis-graphic-image6.png)<br/> In diesem Beispiel wird ein Banner verwendet, um anzugeben, dass die Einstellungen der Seite durch Gruppenrichtlinie gesteuert werden.<br/>                                                                                                                                                                                                       |
| **Glas**<br/> verwenden Sie strategisch, um die visuelle Gewichtung eines Fensters zu reduzieren. <br/>                   | Glass kann die Gewichtung einer Oberfläche reduzieren, indem es sich auf den Inhalt und nicht auf das Fenster selbst konzentriert. <br/> ![Screenshot des Vogels in der Windows-Fotogalerie ](images/vis-graphic-image7.png)<br/> In diesem Beispiel konzentriert glass die Aufmerksamkeit des Benutzers auf den Inhalt und nicht auf die Steuerelemente.<br/>                                                                                                                                                                                                 |
| **Aggregatoren**<br/> verwenden Sie , um eine visuelle Beziehung zwischen stark verknüpften Steuerelementen zu erstellen. <br/> | ![Screenshot der Rückwärts- und Vorwärtsnavigationspfeile ](images/vis-graphic-image8.png)<br/> In diesem Beispiel wird ein Aggregatorhintergrund verwendet, um die Beziehung zwischen den Schaltflächen "Zurück" und "Vorwärts" im Explorer hervorzuheben.<br/> ![Screenshot von Windows-Fotokatalog-Steuerelementen ](images/vis-graphic-image7.png)<br/> In diesem Beispiel wird ein Begrenzungsaggregator verwendet, um die Beziehung zwischen den Steuerelementen hervorzuheben und sie wie ein einzelnes Steuerelement statt acht zu gestalten.<br/> |
| **Trennzeichen**<br/> verwenden, um schwach verwandte oder nicht verknüpfte Steuerelemente zu trennen. <br/>                   | Trennzeichen können entweder interaktiv oder nicht interaktiv sein. Interaktive Trennzeichen zwischen veränderbaren Inhalten werden als Splitter bezeichnet. <br/> ![Screenshot des Splittertrennzeichens für die Namensschaltfläche ](images/vis-graphic-image9.png)<br/> In diesem Beispiel wird ein interaktives Trennzeichen für inhalte verwendet, deren Größe geändert werden kann.<br/> ![Screenshot des Trennzeichens für Browserinformationen ](images/vis-graphic-image10.png)<br/> In diesem Beispiel ist das Trennzeichen nicht interaktiv.<br/>                  |
| **Shadows**<br/> verwenden Sie , um Inhalte visuell vor dem Hintergrund abzuheben. <br/>             | ![Screenshot von vier Fotos mit Schatten ](images/vis-graphic-image11.png)<br/> In diesem Beispiel heben sich die Grafiken durch Schatten vor dem Hintergrund ab.<br/>                                                                                                                                                                                                                                                                                                                                   |
| **Griffe**<br/> Verwenden Sie , um anzugeben, dass ein Objekt verschoben oder seine Größe geändert werden kann. <br/>                    | Handles sind immer interaktiv, und ihr Verhalten wird durch den Mauszeiger beim Zeigen vorgeschlagen. <br/> ![Screenshot einer Fensterecke mit Zeiger zum Ändern der Größe ](images/vis-graphic-image12.png)<br/> ![Screenshot des Auswahlfelds mit Zeiger zur Größenänderung ](images/vis-graphic-image13.png)<br/> In diesen Beispielen geben Handles an, dass die Größe eines Objekts geändert werden kann.<br/>                                                                                                                       |



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Übermitteln Sie wichtige Informationen nicht allein über grafische Elemente.** Dies führt zu Problemen bei der Barrierefreiheit für Benutzer mit Sehbehinderung oder Sehbehinderung.

### <a name="graphic-designs"></a>Grafische Entwürfe

-   **Grafiken sind am effektivsten, wenn sie eine einzelne einfache Idee verstärken.** Komplexe Grafiken, die interpretiert werden müssen, funktionieren nicht gut. Hieroglyphen sind am besten für Cave-Zeichnungen übrig.

    **Falsch:**

    ![Screenshot der Warnung mit komplexer Grafik ](images/vis-graphic-image14.png)

    In diesem Beispiel versucht eine komplexe Grafik von Windows XP ineffektiv, eine komplexe Vertrauensentscheidung zu erklären.

-   **Verwenden Sie keine Pfeile, Chevrons, Schaltflächenrahmen oder andere Mitwirkende, die interaktiven Steuerelementen zugeordnet sind.** Auf diese Weise werden Benutzer zur Interaktion mit Ihren Grafiken eingeladen.
-   **Vermeiden Sie in Ihren Entwürfen Rein-Rot-, Gelb- und Grünstriche.** Um Verwirrung zu vermeiden, reservieren Sie diese Farben, um den Status zu kommunizieren. Wenn Sie diese Farben für etwas anderes als den Status verwenden müssen, verwenden Sie stumme Töne anstelle von reinen Farben.
-   **Verwenden Sie kulturneutrale Entwürfe.** Was in einem Land, einer Region oder einer Kultur eine bestimmte Bedeutung haben kann, hat möglicherweise nicht die gleiche Bedeutung in einem anderen Land.
-   **Vermeiden Sie die Verwendung von Personen, Gesichtern, Geschlecht oder Körperteilen sowie von Politischem, Politischem und Nationalsymbol.** Solche Bilder sind möglicherweise nicht einfach zu übersetzen oder anstößig.
-   **Wenn Sie Personen oder Benutzer darstellen müssen, stellen Sie sie generisch dar.** Vermeiden Sie realistische Darstellungen.

### <a name="backgrounds-and-banners"></a>Hintergründe und Banner

-   **Um Inhalte zu hervorheben, verwenden Sie dunklen Text auf einem hellen Hintergrund.** Schwarzer Text auf hellgrauem oder gelbem Hintergrund funktioniert gut.

    ![Screenshot von blauem Linktext auf gelbem Hintergrund ](images/vis-graphic-image15.png)

    In diesem Beispiel erhält der Link die Aufmerksamkeit des Benutzers, da er sich auf einem gelben Hintergrund befindet.

-   **Um den Inhalt zu heben, verwenden Sie hellen Text auf einem dunklen Hintergrund.** Weißer Text auf einem dunkelgrauen oder blauen Hintergrund funktioniert gut.

    ![Screenshot des weißen Hilfelinks auf grünem Hintergrund ](images/vis-graphic-image16.png)

    In diesem Beispiel hebt der dunkle Hintergrund den Inhalt hervor.

-   **Wenn ein Farbverlauf verwendet wird, stellen Sie sicher, dass die Textfarbe im gesamten Farbverlauf einen guten Kontrast auft.**
-   **Verwenden Sie immer ein 16 x 16 Pixel großes Symbol, um die Aufmerksamkeit auf das Banner zu ziehen.** Banner sind andernfalls zu einfach zu übersehen. Weitere Richtlinien und Beispiele finden Sie unter [Standardsymbole.](vis-std-icons.md)
-   **Verwenden Sie Hintergründe und Banner mit Vorsicht.** Obwohl die Absicht des Hintergrunds oder Banners sein kann, Inhalte zu hervorheben, sind die Ergebnisse häufig das Gegenteil eines Als "Bannerblending" bezeichneten Satzes.

### <a name="glass"></a>Glas

-   **Erwägen Sie die strategische Verwendung von Glass in kleinen Regionen, die den Fensterrahmen ohne Text berühren.** Dies kann einem Programm ein einfacheres, leichteres und kohäsiveres Aussehen verleihen, indem der Bereich als Teil des Rahmens angezeigt wird.
-   **Verwenden Sie kein Glass in Situationen, in denen ein einfacher Fensterhintergrund ansprechender oder einfacher zu verwenden wäre.**

### <a name="separators"></a>Trennzeichen

-   **Verwenden Sie vertikale und horizontale Linien für Trennzeichen.** Stellen Sie sicher, dass zwischen den Trennzeichen und dem zu trennenden Inhalt ausreichend Platz vorhanden ist.
-   Für Trennzeichen zwischen sizierbarem Inhalt (Splitter) zeigen Sie den Größenzeiger an, wenn Sie darauf zeigen.

![Screenshot: Splitter mit Zeiger zum Ändern der Größe](images/vis-graphic-image17.png)

![Screenshot des Splitters mit Größenvergrößerungszeiger ](images/vis-graphic-image18.png)

In diesen Beispielen werden größenvergrößerte Zeiger angezeigt, wenn Sie darauf zeigen.

### <a name="shadows"></a>Shadows

-   **Verwenden Sie nur , damit die wichtigsten Inhalte oder Objekte des Programms, die gezogen werden, visuell vor dem Hintergrund stehen.** Betrachten Sie Schatten in anderen Situationen als unübersichtlich.

### <a name="high-dpi-support"></a>Unterstützung für hohe DPI-Leistung

-   **Unterstützt die Videomodi 96 und 120 Punkte pro Zoll (dpi).** Erkennen Sie den dpi-Modus beim Start, und behandeln Sie DPI-Änderungsereignisse. Windows ist für 96 und 120 dpi optimiert und verwendet standardmäßig 96 dpi.
-   **Es wird bevorzugt, separate Bitmaps zur Verfügung zu stellen, die speziell für 96 und 120 dpi gerendert werden, statt Grafiken zu skalieren.** Stellen Sie mindestens 96- und 120-DPI-Versionen für die wichtigsten, sichtbaren Bitmaps zur Verfügung, und zentrieren oder skalieren Sie die anderen. Solche Anwendungen werden als "high-dpi aware" betrachtet und bieten eine bessere visuelle Gesamterfahrung als Programme, die automatisch von Windows skaliert werden.
    -   Entwickler: Sie können ein Programm mit hoher DPI-Leistung deklarieren (und die automatische Skalierung verhindern), indem Sie das dpi-orientierte Flag im Manifest des Programms festlegen oder die SetProcessDPIAware()-API während der Programmin initialisierung aufrufen. Sie können Makros verwenden, um die Auswahl der richtigen Grafiken zu vereinfachen. Für Win32-Bitmaps können Sie SS CENTERIMAGE zum Zentrieren oder \_ SS \_ REALSIZECONTROL zum Skalieren verwenden.
-   Überprüfen Sie Ihr Programm in 96 und 120 dpi auf:
    -   Grafiken, die zu klein oder zu groß sind.
    -   Grafiken, die abgeschnitten, überlappend oder anderweitig nicht ordnungsgemäß passen.
    -   Grafiken, die schlecht gestreckt ("pixiliert") sind.
    -   Text, der abgeschnitten ist oder nicht in grafische Hintergründe passt.

## <a name="text"></a>Text

-   **Verwenden Sie für Barrierefreiheit und Lokalisierung keinen Text in Grafiken.** Machen Sie Ausnahmen nur, um [Branding und](exper-branding.md) Text als abstraktes Konzept zu darstellen.

 

