---
description: Zeit in DirectShow-Bearbeitungs Diensten
ms.assetid: 4e8cc766-97f3-45d5-9c4a-5cd6e9ad9c09
title: Zeit in DirectShow-Bearbeitungs Diensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421831742a2805f58d61c2258dad89d339131f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352796"
---
# <a name="time-in-directshow-editing-services"></a>Zeit in DirectShow-Bearbeitungs Diensten

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Zum Bearbeiten von Videos müssen Sie mit einigen wichtigen Zeit Steuerungskonzepten arbeiten. Beispiel:

-   Jeder Clip hat eine Dauer.
-   Clips, Übergänge und Effekte werden zu bestimmten Zeitpunkten in einem Projekt angezeigt.
-   Video hat eine Frame Rate, ausgedrückt in Frames pro Sekunde (fps).

[DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) (des) stellen verschiedene Methoden bereit, mit denen Zeiten und Frameraten festgelegt oder abgerufen werden. Die Bedeutung dieser Werte hängt vom Kontext ab.

**Uhrzeitwerte**

Wenn ein Parameter einen Zeitpunkt ausdrückt, sind drei unterschiedliche Bedeutungen möglich:

-   Zeitachsen *Zeit*: die Zeit relativ zum Anfang der Zeitachse. Beispielsweise kann ein Clip 2 Sekunden in der Zeitachse beginnen, oder es kann 15 Sekunden in der Zeitachse passieren. Die Zeitachse bestimmt das endgültige gerenderte Projekt, sodass Sie sich die Zeitachsen Zeit auch als "Projektzeit" vorstellen können.
-   *Medien Zeit*: ein Punkt in einer Quelldatei relativ zum Anfang der Datei, wie bei normaler Wiedergabe erreicht. Wenn Sie z. b. über eine Videodatei mit 10 Sekunden verfügen, wird der Punkt, der sich in der Datei befindet, 5 Sekunden lang angezeigt.
-   Über *geordnete Zeit*: Zeit relativ zu einem Objekt in der Zeitachse. Wenn ein Objekt z. b. bei 8 Sekunden auf der Zeitachse beginnt und ein anderes Objekt enthält, das bei 10 Sekunden auf der Zeitachse beginnt, beginnt das untergeordnete Objekt in Relation zum übergeordneten Element um 2 Sekunden. Virtuelle Spuren beginnen bei Zeit NULL, relativ zur Zeitachse. Daher ist die übergeordnete Zeit für jedes Objekt in einer virtuellen Spur gleich der Zeitachsen Zeit.

Die Medien Zeit gilt nur für Quell Objekte. Jedes Quell Objekt verfügt über eine Start Zeit für Medien und eine Medien Endzeit. Angenommen, Sie haben einen Video Clip mit 10 Sekunden, und Sie möchten nur 5 Sekunden von der Mitte des Clips verwenden, wobei die ersten 2 Sekunden und die letzten 3 Sekunden des Clips gekürzt werden. Wenn Sie möchten, dass der Clip 20 Sekunden im Projekt angezeigt wird (und eine normale Wiedergabe Rate annehmen), geben Sie die folgenden Start-und Endzeit Zeiten an.

-   Medien Start: 2 Sekunden
-   Medien Ende: 7 Sekunden
-   Zeitachse: 20 Sekunden
-   Zeitachsen Ende: 25 Sekunden

    ![Einfügen eines Quell Clips in eine Zeitachse](images/des-time1.png)

**Frame Raten**

Die Framerate ist die "Geschwindigkeit" eines Mediendaten Stroms, gemessen in Frames pro Sekunde. Wie bei Zeitwerten hängt die Bedeutung einer Framerate vom Kontext ab:

-   **Ausgabe Rahmenrate:** Die Framerate des endgültigen gerenderten Projekts, das von der Gruppe definiert wird. Wenn Sie das Projekt gerendern, wird jede Gruppe zu einem separaten Mediendaten Strom mit eigener Framerate.
-   **Quellbildrate:** Die Framerate, in der die Quelldatei ursprünglich erstellt wurde. Die erstellte Frame Rate muss nicht mit der Ausgabe Frame Rate der Gruppe identisch sein. Des führt das automatische Upsampling oder Downsampling der Datei nach Bedarf aus. Bei den meisten Medienformaten kann der die Framerate ermitteln, indem er das Format untersucht. Eine DIB-Sequenz ist eine Ausnahme. Sie müssen die Framerate einer DIB-Sequenz angeben. (Weitere Informationen finden Sie unter [Arbeiten mit Quellen](working-with-sources.md).)

**Wiedergabe Rate:** Die sichtbare Geschwindigkeit eines Quell Clips, wenn er im Projekt angezeigt wird. Beispielsweise können 10 Sekunden "Video" auf der Zeitachse in 5 Sekunden passen. Folglich steigt die Geschwindigkeit des Clips um den Faktor 2, wie im folgenden Diagramm veranschaulicht.

![schnellere Wiedergabe einer Quelle](images/des-time2.png)

(Bei einer Audioquelle würde die Tonhöhe ebenfalls verschoben werden.) Die folgende Formel bestimmt die Wiedergabe Rate eines Quell Clips:

-   Wiedergabe Rate = (Medien Start – Medien Start)/(Zeitachsen Ende – Zeitachse starten)

Beachten Sie, dass jede dieser drei Raten unabhängig von den anderen Sätzen ist:

-   Sie können einen Clip beschleunigen oder verlangsamen, indem Sie die Medien Zeiten anpassen. Dies wirkt sich nicht auf die Framerate der endgültigen Ausgabe aus.
-   Sie können die Ausgabe Frame Rate erhöhen oder verringern, ohne zu beeinflussen, wie schnell eine Datei wiedergegeben wird.
-   Sie können innerhalb derselben Gruppe die Quelldateien kombinieren, die unterschiedliche erstellte Frameraten aufweisen, und des führt einen Upsample-oder Downsample-Vorgang für jeden Clip aus, der mit der Framerate der Gruppe übereinstimmt.

Wenn Sie ein Projekt erstellen, werden alle Uhrzeiten auf die nächste Frame Grenze gerundet, wie durch die Gruppen Rahmenrate festgelegt. Nehmen wir beispielsweise an, dass eine Videogruppe eine Frame Rate von 30 fps hat. Jeder Frame beträgt ungefähr 33 Millisekunden (MS). Angenommen, Sie fügen der Zeitachse einen 1,68-Sekunden-Quellclip hinzu, beginnend bei Zeit NULL. Die Quelle endet nicht genau an einer Frame Grenze, sodass die Endzeit auf 1,6666 Sekunden (50 Frames) gerundet. Wenn Sie bis zu 1,68 Sekunden im gerenderten Projekt suchen, suchen Sie tatsächlich nach dem Ende der Quelle bis zum 51-Frame.

Allerdings wird die Endzeit der Quelle von des nicht überschrieben. Sie können später die Gruppen Rahmenrate ändern oder die Quelle an eine neue Stelle in der Zeitachse verschieben, auf der Sie anders gerundet wird. Daher behält der die ursprüngliche Endzeit bei und rundet nur bei Bedarf auf. Weitere Informationen finden Sie unter [**iamtimelineobj:: fixtimes**](iamtimelineobj-fixtimes.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einführung in DirectShow-Bearbeitungs Dienste](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



