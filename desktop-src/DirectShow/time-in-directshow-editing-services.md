---
description: Zeit in DirectShow-Bearbeitungsdiensten
ms.assetid: 4e8cc766-97f3-45d5-9c4a-5cd6e9ad9c09
title: Zeit in DirectShow-Bearbeitungsdiensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afc99ff2391ea7975daed7b4152e869741f9990561417131942c4d86e904fca8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083620"
---
# <a name="time-in-directshow-editing-services"></a>Zeit in DirectShow-Bearbeitungsdiensten

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Zum Bearbeiten von Videos müssen Sie mit einigen wichtigen Zeitsteuerungskonzepten arbeiten. Beispiel:

-   Jeder Clip hat eine Dauer.
-   Clips, Übergänge und Effekte werden zu bestimmten Zeiten in einem Projekt angezeigt.
-   Video hat eine Bildfrequenz, ausgedrückt in Frames pro Sekunde (FPS).

[DirectShow Editing Services](directshow-editing-services.md) (DES) stellt verschiedene Methoden zum Festlegen oder Abrufen von Zeiten und Frameraten zur Verfügung. Die Bedeutung dieser Werte hängt vom Kontext ab.

**Zeitwerte**

Wenn ein Parameter eine Uhrzeit ausdrückt, sind drei unterschiedliche Bedeutungen möglich:

-   *Zeitachse:* Die Zeit relativ zum Anfang der Zeitachse. Beispielsweise kann ein Clip 2 Sekunden in der Zeitachse beginnen, oder ein Übergang kann 15 Sekunden in die Zeitachse erfolgen. Die Zeitachse bestimmt das endgültige gerenderte Projekt, sodass Sie die Zeitachse auch als "Projektzeit" einplanen können.
-   *Medienzeit:* Ein Punkt in einer Quelldatei relativ zum Anfang der Datei, der während der normalen Wiedergabe erreicht wird. Wenn Sie beispielsweise über eine 10-Sekunden-Videodatei verfügen, erfolgt der Punkt in der Mitte der Datei bei 5 Sekunden, ausgedrückt als Medienzeit.
-   *Übergeordnete Zeit:* Zeit relativ zu einem Objekt auf der Zeitachse. Wenn ein Objekt beispielsweise bei 8 Sekunden auf der Zeitachse beginnt und ein weiteres Objekt enthält, das bei 10 Sekunden auf der Zeitachse beginnt, beginnt das untergeordnete Objekt bei 2 Sekunden relativ zum übergeordneten Objekt. Die virtuellen Spuren beginnen alle zum Zeitpunkt 0 (null) relativ zur Zeitachse. Daher entspricht die übergeordnete Zeit für jedes Objekt in einer virtuellen Spur der Zeitachse.

Die Medienzeit gilt nur für Quellobjekte. Jedes Quellobjekt verfügt über eine Medienstartzeit und eine Medienstoppzeit. Angenommen, Sie verfügen über einen 10-Sekunden-Videoclip und möchten nur 5 Sekunden ab der Mitte des Clips verwenden, um die ersten 2 Sekunden und die letzten 3 Sekunden vom Clip zu kürzen. Wenn der Clip 20 Sekunden im Projekt angezeigt werden soll (und eine normale Wiedergaberate angenommen wird), geben Sie die folgenden Start- und Stoppzeiten an.

-   Medienstart: 2 Sekunden
-   Medienstopp: 7 Sekunden
-   Zeitachsenstart: 20 Sekunden
-   Zeitachsenstopp: 25 Sekunden

    ![Einfügen eines Quellclips auf einer Zeitachse](images/des-time1.png)

**Frameraten**

Die Bildfrequenz ist die "Geschwindigkeit" eines Medienstreams, gemessen in Frames pro Sekunde. Wie bei Zeitwerten hängt die Bedeutung einer Framerate vom Kontext ab:

-   **Ausgabebildrate:** Die Framerate des endgültigen gerenderten Projekts, definiert durch die Gruppe. Wenn Sie das Projekt rendern, wird jede Gruppe zu einem separaten Medienstream mit eigener Bildfrequenz.
-   **Quellframerate:** Die Framerate, in der die Quelldatei ursprünglich verfasst wurde. Die Erstellungsbildrate muss nicht mit der Ausgabebildrate der Gruppe übereinstimmen. DES führt bei Bedarf automatisch eine Upsample- oder Downsampple-Anweisung für die Datei durch. Bei den meisten Medienformaten kann DES die Bildfrequenz ermitteln, indem das Format untersucht wird. Eine DIB-Sequenz ist eine Ausnahme. Sie müssen die Framerate einer DIB-Sequenz angeben. (Weitere Informationen finden Sie unter [Arbeiten mit Quellen](working-with-sources.md).)

**Wiedergaberate:** Die offensichtliche Geschwindigkeit eines Quellclips, wenn er im Projekt angezeigt wird. Beispielsweise kann ein Video von 10 Sekunden auf der Zeitachse in 5 Sekunden passen. Daher erhöht sich die Geschwindigkeit des Clips um den Faktor 2, wie im folgenden Diagramm veranschaulicht.

![Schnelleres Wiedereinspielen einer Quelle](images/des-time2.png)

(Bei einer Audioquelle würde sich auch die Tonhöhe verschieben.) Die folgende Formel bestimmt die Wiedergaberate eines Quellclips:

-   Wiedergaberate = (Medienstopp – Medienstart) / (Zeitachsenstopp – Zeitachsenstart)

Beachten Sie, dass jeder dieser drei Tarife unabhängig von den anderen tarifen ist:

-   Sie können einen Clip beschleunigen oder verlangsamen, indem Sie die Medienzeiten anpassen. Dies wirkt sich nicht auf die Framerate der endgültigen Ausgabe aus.
-   Sie können die Ausgabebildrate erhöhen oder verringern, ohne die Geschwindigkeit einer Datei zu beeinträchtigen.
-   Innerhalb derselben Gruppe können Sie Quelldateien mit unterschiedlichen Bildfrequenzen kombinieren, und DES wird jeden Clip upsample oder downsample, um die Framerate der Gruppe zu verwenden.

Wenn Sie ein Projekt rendern, werden alle Zeiten auf die nächste Rahmengrenze gerundet, wie durch die Gruppenbildrate festgelegt. Angenommen, eine Videogruppe hat eine Bildfrequenz von 30 Fps. Jeder Frame beträgt ungefähr 33 Millisekunden (ms). Angenommen, Sie fügen der Zeitachse einen 1,68-Sekunden-Quellclip hinzu, beginnend mit dem Zeitpunkt 0 (null). Da die Quelle nicht genau an einer Rahmengrenze endet, rundet DES die Stoppzeit auf 1,6666 Sekunden (50 Frames) ab. Wenn Sie im gerenderten Projekt nach 1,68 Sekunden suchen, suchen Sie tatsächlich nach dem Ende der Quelle bis zum 51. Frame.

Des überschreibt jedoch nicht die Stopzeit der Quelle. Sie können später die Bildfrequenz der Gruppe ändern oder die Quelle an eine neue Stelle in der Zeitachse verschieben, wo sie anders gerundet wird. Daher behält DES die ursprüngliche Stoppzeit bei und rundet nur bei Bedarf. Weitere Informationen finden Sie unter [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit DirectShow-Bearbeitungsdiensten](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



