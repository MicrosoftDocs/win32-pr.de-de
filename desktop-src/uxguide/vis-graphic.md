---
title: Grafische Elemente
description: Grafische Elemente zeigen Beziehungen, Hierarchie und Betonung visuell. Dazu zählen Hintergründe, Banner, Glas, Aggregatoren, Trennzeichen, Schatten und Handles.
ms.assetid: f9e741e9-a72e-4bdb-bd95-8916c7cf344f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a452668bc1685143273df80fd144642a18019213
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103961071"
---
# <a name="graphic-elements"></a>Grafische Elemente

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

*Grafische Elemente* zeigen Beziehungen, Hierarchie und Betonung visuell. Dazu zählen Hintergründe, Banner, Glas, Aggregatoren, Trennzeichen, Schatten und Handles.

![Screenshot von Windows-Explorer mit Schatten, usw. ](images/vis-graphic-image1.png)

Ein Beispiel mit mehreren Typen von Grafikelementen.

Grafische Elemente sind in der Regel nicht interaktiv. Trennzeichen sind jedoch interaktiv für Inhalte, die angepasst werden können, und Handles sind Grafiken, die Interaktivität anzeigen.

**Hinweis:** Richtlinien im Zusammenhang mit [Gruppen Feldern](ctrl-group-boxes.md), [Animationen](vis-animations.md), [Symbolen](vis-icons.md)und [Branding](exper-branding.md) werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Obwohl grafische Elemente eine starke visuelle Methode zum Angeben von Beziehungen sind, wird durch eine übermäßige Verwendung die Visualisierung hinzugefügt und der auf einer Oberfläche verfügbare Platz reduziert. Sie sollten sparsam verwendet werden.

Ein Entwurfs Trend in Microsoft Windows ist ein einfacheres, saubereres aussehen, da unnötige Grafiken und Linien eliminiert werden.

Um zu entscheiden, ob ein grafisches Element erforderlich ist, sollten Sie sich die folgenden Fragen stellen:

-   **Ist die Darstellung und die Kommunikation des Entwurfs ebenso klar und effektiv, ohne das-Element?** Wenn dies der Fall ist, entfernen Sie ihn.
-   **Können Sie die Beziehungen mithilfe von Layout allein übermitteln?** Wenn dies der Fall ist, verwenden Sie stattdessen das [Layout](vis-layout.md) . Sie können verwandte Steuerelemente nebeneinander platzieren und zusätzlichen Abstand zwischen nicht verknüpften Steuerelementen einfügen. Sie können auch den Einzug verwenden, um hierarchische Beziehungen anzuzeigen.

![Screenshot eines vier-Symbol-Layouts ](images/vis-graphic-image2.png)

In diesem Beispiel wird das Layout allein zum Anzeigen von Steuerelement Beziehungen verwendet.

-   **Wird die Kommunikation ohne Text wirksam?** Wenn dies nicht der Folge ist, verwenden Sie ein [Gruppenfeld](ctrl-group-boxes.md)mit der Bezeichnung Trenn [Zeichen](text-ui.md)oder eine andere Bezeichnung.

## <a name="usage-patterns"></a>Verwendungsmuster

Grafische Elemente weisen mehrere Verwendungs Muster auf:



|                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grafische Abbildungen**<br/> Verwenden Sie, um eine Idee visuell zu kommunizieren. <br/>                         | Grafische Abbildungen ähneln Symbolen, mit dem Unterschied, dass Sie beliebig groß sein können und in der Regel nicht interaktiv sind. <br/> ![Screenshot der CPU-Auslastung im Screenshot ](images/vis-graphic-image3.png)<br/> In diesem Beispiel wird eine grafische Abbildung verwendet, um die Art eines Features vorzuschlagen.<br/>                                                                                                                                                                                                        |
| **Hintergründe**<br/> Verwenden Sie, um unterschiedliche Arten von Inhalten hervorzuheben oder hervorzuheben. <br/>           | Hintergründe können zum Hervorheben wichtiger Inhalte verwendet werden. <br/> ![Screenshot der Virus Meldung im roten Hintergrund ](images/vis-graphic-image4.png)<br/> in diesem Beispiel wird ein Hintergrund verwendet, um eine wichtige Aufgabe hervorzuheben.<br/> Hintergründe können auch verwendet werden, um sekundäre Inhalte hervorzuheben. <br/> ![Screenshot der System Steuerungselemente ](images/vis-graphic-image5.png)<br/> In diesem Beispiel werden sekundäre Aufgaben durch die Suche in einem Aufgabenbereich aufgehoben.<br/>   |
| **Mitzubringen**<br/> wird verwendet, um einen wichtigen Status anzugeben. <br/>                                         | Im Gegensatz zu Hintergründen betonen Banner primär eine einzelne Text Zeichenfolge. <br/> ![Screenshot des Banners mit Einstellungs Informationen ](images/vis-graphic-image6.png)<br/> In diesem Beispiel wird ein Banner verwendet, um anzugeben, dass die Einstellungen der Seite von Gruppenrichtlinie gesteuert werden.<br/>                                                                                                                                                                                                       |
| **Glas**<br/> Verwenden Sie strategisch, um die visuelle Gewichtung eines Fensters zu verringern. <br/>                   | Glas kann die Gewichtung einer Oberfläche verringern, indem Sie sich auf den Inhalt und nicht auf das Fenster selbst konzentriert. <br/> ![Screenshot des Vogels in der Windows-Fotogalerie ](images/vis-graphic-image7.png)<br/> In diesem Beispiel konzentriert sich die Aufmerksamkeit des Benutzers auf den Inhalt und nicht auf die Steuerelemente.<br/>                                                                                                                                                                                                 |
| **Aggregatoren**<br/> Verwenden Sie, um eine visuelle Beziehung zwischen stark verknüpften Steuerelementen zu erstellen. <br/> | ![Screenshot der rückwärts-und vorwärts Navigationspfeile ](images/vis-graphic-image8.png)<br/> in diesem Beispiel wird ein aggregatorhintergrund verwendet, um die Beziehung zwischen den Schaltflächen "zurück" und "Vorwärts" im Explorer hervorzuheben.<br/> ![Screenshot der Steuerelemente der Windows-Fotogalerie ](images/vis-graphic-image7.png)<br/> In diesem Beispiel wird ein Begrenzungs Aggregator verwendet, um die Beziehung zwischen den Steuerelementen hervorzuheben und Sie wie ein einzelnes Steuerelement anstelle von acht zu gestalten.<br/> |
| **Trennzeichen**<br/> Verwenden Sie, um schwach Verwandte oder nicht verknüpfte Steuerelemente zu trennen. <br/>                   | Trennzeichen können interaktiv oder nicht interaktiv sein. interaktive Trennzeichen zwischen Inhalt, dessen Größe angepasst werden können, werden als Splitters bezeichnet. <br/> ![Screenshot des Splitter Trennzeichens für die namens Schaltfläche ](images/vis-graphic-image9.png)<br/> in diesem Beispiel wird ein interaktives Trennzeichen für Inhalts Inhalte verwendet, die angepasst werden können.<br/> ![Screenshot des Trenn Zeichens für Browserinformationen ](images/vis-graphic-image10.png)<br/> In diesem Beispiel ist das Trennzeichen nicht interaktiv.<br/>                  |
| **Shadows**<br/> Verwenden Sie, um Inhalt visuell gegen den Hintergrund darzustellen. <br/>             | ![Screenshot von vier Fotos mit Schatten ](images/vis-graphic-image11.png)<br/> In diesem Beispiel stellen Schatten die Grafik vor dem Hintergrund.<br/>                                                                                                                                                                                                                                                                                                                                   |
| **Hand**<br/> Verwenden Sie, um anzugeben, dass ein Objekt verschoben oder seine Größe geändert werden kann. <br/>                    | Handles sind immer interaktiv, und ihr Verhalten wird mit dem Mauszeiger auf Hover vorgeschlagen. <br/> ![Screenshot einer Fenster Ecke mit dem Zeiger zum Ändern der Größe ](images/vis-graphic-image12.png)<br/> ![Screenshot des Auswahl Felds mit dem Zeiger zum Ändern der Größe ](images/vis-graphic-image13.png)<br/> In diesen Beispielen geben Handles an, dass die Größe eines Objekts geändert werden kann.<br/>                                                                                                                       |



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Vermitteln Sie keine wichtigen Informationen nur über Grafikelemente.** Dies stellt Barrierefreiheits Probleme für Benutzer mit visuellen Behinderungen oder Beeinträchtigungen dar.

### <a name="graphic-designs"></a>Grafik Entwürfe

-   **Grafiken sind am effektivsten, wenn Sie eine einzelne einfache Idee verstärken.** Komplexe Grafiken, die interpretiert werden müssen, funktionieren nicht gut. "Hieroglyphics" ist für Höhlenzeichnungen am besten geeignet.

    **Falsch:**

    ![Screenshot der Warnung mithilfe komplexer Grafik ](images/vis-graphic-image14.png)

    In diesem Beispiel versucht eine komplexe Grafik aus Windows XP, eine komplexe Vertrauensstellungs Entscheidung zu erläutern.

-   **Verwenden Sie keine Pfeile, Chevrons, Schaltflächen Rahmen oder andere mit interaktiven Steuerelementen verbundene Kosten.** Dadurch werden Benutzer zur Interaktion mit Ihren Grafiken aufgefordert.
-   **Vermeiden Sie in ihren Entwürfen, dass Sie in ihren Entwürfen in der Design-und gelb-und grünen Striche sind** Um Verwirrung zu vermeiden, reservieren Sie diese Farben, um den Status zu kommunizieren. Wenn Sie diese Farben für etwas anderes als den Status verwenden müssen, verwenden Sie anstelle reiner Farben gedämpfte Töne.
-   **Verwenden Sie Kultur neutrale Entwürfe.** Was in einem Land, in einer Region oder in einer Kultur eine bestimmte Bedeutung haben kann, hat möglicherweise nicht die gleiche Bedeutung in einem anderen Land.
-   **Vermeiden Sie es, Personen, Gesichter, Geschlecht oder Textteil sowie religiöse, politische und nationale Symbole zu verwenden.** Solche Bilder können möglicherweise nicht einfach übersetzt werden oder können anstößig sein.
-   **Wenn Sie Personen oder Benutzer repräsentieren müssen, stellen Sie Sie generisch dar.** vermeiden Sie realistische Darstellungen.

### <a name="backgrounds-and-banners"></a>Hintergründe und Banner

-   **Um Inhalte hervorzuheben, verwenden Sie den dunklen Text auf einem hellen Hintergrund.** Schwarzer Text in einem hellgrauen oder gelben Hintergrund funktioniert gut.

    ![Screenshot des blauen linktexts im gelben Hintergrund ](images/vis-graphic-image15.png)

    In diesem Beispiel erhält der Link die Aufmerksamkeit des Benutzers, da er sich in einem gelben Hintergrund befindet.

-   **Um den Inhalt zu entfernen, verwenden Sie den hellen Text in einem dunklen Hintergrund.** Weißer Text in einem dunkelgrauen oder blauen Hintergrund funktioniert gut.

    ![Screenshot des Links "weißer Hilfe" im grünen Hintergrund ](images/vis-graphic-image16.png)

    In diesem Beispiel wird der Inhalt durch den dunklen Hintergrund hervorgehoben.

-   **Wenn ein Farbverlauf verwendet wird, stellen Sie sicher, dass die Textfarbe für den gesamten Farbverlauf über einen guten Kontrast verfügt.**
-   **Verwenden Sie immer ein 16x16-Pixel-Symbol, um auf das Banner aufmerksam zu machen.** Banner sind zu leicht zu übersehen. Weitere Richtlinien und Beispiele finden Sie unter [Standard Symbole](vis-std-icons.md).
-   **Verwenden Sie Hintergründe und Banner mit Bedacht.** Obwohl die Absicht des Hintergrunds oder Banners darin besteht, Inhalte hervorzuheben, sind die Ergebnisse oft das Gegenteil eines als "Banner Blindheit" bezeichneten Phänomens.

### <a name="glass"></a>Glas

-   **Es empfiehlt sich, Glas strategisch in kleinen Regionen zu verwenden, die den Fensterrahmen ohne Text berühren.** Dies kann einem Programm ein einfacheres, helleres aussehen ermöglichen, indem die Region als Teil des Frames angezeigt wird.
-   **Verwenden Sie kein Glas in Situationen, in denen ein einfacher Fenster Hintergrund attraktiver oder leichter zu verwenden wäre.**

### <a name="separators"></a>Trennzeichen

-   **Verwenden Sie vertikale und horizontale Linien für Trennzeichen.** Stellen Sie sicher, dass genügend Speicherplatz zwischen den Trennzeichen und den getrennten Inhalten vorhanden ist.
-   Bei Trennzeichen zwischen sitbarem Inhalt (Splitters) können Sie den Zeiger zum Ändern der Größe beim Hover anzeigen.

![Screenshot, der einen Splitter mit einem Zeiger zum Ändern der Größe anzeigt.](images/vis-graphic-image17.png)

![Screenshot des Splitters mit dem Zeiger zum Ändern der Größe ](images/vis-graphic-image18.png)

In diesen Beispielen werden Zeiger zur Größenänderung angezeigt, wenn Sie darauf zeigen.

### <a name="shadows"></a>Shadows

-   **Verwenden Sie nur, um den wichtigsten Inhalt Ihres Programms oder die Objekte, die gezogen werden, für den Hintergrund visuell darzustellen.** Beachten Sie, dass Schatten in anderen Situationen als visueller Übersichtlichkeit angesehen werden.

### <a name="high-dpi-support"></a>Hohe dpi-Unterstützung

-   **Unterstützung von 96-und 120-dpi-Video Modi (dpi).** Erkennen Sie den dpi-Modus beim Start, und behandeln Sie dpi-Änderungs Ereignisse. Windows ist für 96-und 120-DPI-Werte optimiert und verwendet standardmäßig 96 dpi.
-   **Es empfiehlt sich, separate Bitmaps bereitzustellen, die speziell für 96-und 120-dpi gerendert werden.** Geben Sie mindestens 96-und 120-dpi-Versionen für die wichtigsten, sichtbaren Bitmaps an, und zentrieren oder Skalieren Sie die anderen. Solche Anwendungen werden als "High-dpi-fähig" angesehen und bieten eine bessere allgemeine visuelle Darstellung als Programme, die automatisch von Windows skaliert werden.
    -   Entwickler: Sie können ein Programm mit hoher dpi-Unterstützung deklarieren (und die automatische Skalierung verhindern), indem Sie das dpi-abhängige Flag im Programm Manifest festlegen oder die SetProcessDPIAware ()-API während der Programm Initialisierung aufrufen. Sie können Makros verwenden, um die Auswahl der richtigen Grafiken zu vereinfachen. Für Win32-Bitmaps können Sie "SS \_ CenterImage" verwenden, um \_ realsizecontrol für die Skalierung zu zentrieren oder zu verwenden.
-   Überprüfen Sie Ihr Programm in 96 und 120 dpi für:
    -   Grafiken, die zu klein oder zu groß sind.
    -   Grafiken, die abgeschnitten, überlappen oder anderweitig nicht ordnungsgemäß passen.
    -   Grafiken, die unzureichend gestreckt ("pixil") sind.
    -   Text, der in grafischen Hintergründen abgeschnitten oder nicht passt.

## <a name="text"></a>Text

-   **Verwenden Sie für Barrierefreiheit und Lokalisierung keinen Text in Grafiken.** Stellen Sie nur Ausnahmen dar, um [Brandings](exper-branding.md) und Text als abstraktes Konzept darzustellen.

 

