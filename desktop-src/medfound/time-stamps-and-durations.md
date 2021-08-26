---
description: In diesem Thema wird beschrieben, Media Foundation Transformationen Zeitstempel verarbeiten sollten.
ms.assetid: 4ab576ce-becd-4736-921e-e463c0dff841
title: Zeitstempel und Dauer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22452e8b6b8094e643126f479f13b2c447db584588f3be1c1aa6595b3e7e2bb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953200"
---
# <a name="time-stamps-and-durations"></a>Zeitstempel und Dauer

In diesem Thema wird [beschrieben, Media Foundation Transformationen](media-foundation-transforms.md) Zeitstempel verarbeiten sollten.

Ein MFT muss einen Zeitstempel und eine Dauer für alle Ausgabebeispiele so genau wie möglich festlegen. Bei einem einfachen MFT, der einen Eingabepuffer verwendet und vollständig in einen Ausgabepuffer verarbeitet, sollte MFT einfach den Zeitstempel und die Dauer direkt aus dem Eingabebeispiel in das Ausgabebeispiel kopieren. Viele Transformationen sind jedoch komplexer als diese und erfordern möglicherweise komplexere Berechnungen der Ausgabezeit. Alle MFTs sollten die folgenden grundlegenden Regeln beachten:

-   Ein MFT sollte versuchen, einen Zeitstempel und eine Dauer für alle nicht komprimierten Video- oder Audioausgabebeispiele zu verwenden, wenn ein genauer Zeitstempel oder eine genaue Dauer für die Eingabebeispiele angegeben oder berechnet werden kann. Interpolation kann für einige Ausgabezeitstempel erforderlich sein, insbesondere für Decoder.
-   Die Zeitstempel und die Dauer der Eingabebeispiele sollten in den Ausgabebeispielen so weit wie möglich beibehalten werden.
-   Die Ausgabezeitstempel oder -daueren passen möglicherweise nicht zur Eingabe, da MFT Daten zurück hält oder die Ausgabe in andere Teile als die Eingabe unterbricht. In diesem Fall sollte MFT den Ausgabezeitstempel aus dem frühesten Eingabebeispiel berechnen, das Daten enthält, die zum Erstellen des Ausgabebeispiels verwendet wurden. Um den Ausgabezeitstempel zu berechnen, fügen Sie den Eingabezeitstempel des entsprechenden Eingabebeispiels der Dauer der Daten hinzu, die bereits aus dieser Stichprobe transformiert wurden. Im zweiten Beispiel am Ende dieses Abschnitts wird diese Idee veranschaulicht.
-   Wenn die Eingabebeispiele eine Dauer haben, sollte diese Dauer beibehalten werden. Wenn ein Eingabebeispiel nicht über eine Dauer verfügt, sollte der MFT nach Möglichkeit eine Dauer aus der Größe des Ausgabepuffers oder der vom Medientyp angegebenen Datenrate berechnen.
-   Berechnete Dauer sollten abgeschnitten (abgerundet) und nicht auf das nächste Inkrement gerundet werden. Die Pipeline verfügt über genügend Slack für die Behandlung geringfügig ungenauer Dauer, aber es ist einfacher für die Pipeline, eine Dauer zu verarbeiten, die 1 % zu kurz ist als eine Dauer, die 1 % zu lang ist. Es gibt jedoch keinen Grund, die Dauer absichtlich zu kürzen, ab hinaus durch Runden.

### <a name="decoders"></a>Decoder

Ein Decoder konvertiert komprimierte Pakete in nicht komprimierte Daten. Da die Ausgabe unkomprimiert ist, haben Decoder eine besondere Verpflichtung, die Zeitstempel und Die Dauer zu korrigieren. Einige komprimierte Formate, insbesondere MPEG-2, verfügen nicht über Zeitstempel für alle Eingabepakete und haben häufig keine Dauer für pakete. Bei diesen Formaten ist der Decoder dafür verantwortlich, einen gültigen Zeitstempel und eine gültige Dauer für jede Ausgabestichprobe zu verwenden, indem die impliziten Daueren der gesamten Ausgabe seit dem letzten Zeitstempel-Eingabebeispiel summiert werden.

Wenn die Dauer für Videos nicht im komprimierten Format verfügbar ist, sollte der Decoder die Dauer als Umkehrung der Bildfrequenz berechnen, in Einheiten von 100 Nanosekunden konvertiert und abgerundet werden.

Wenn die Dauer für Audiodaten nicht im komprimierten Format verfügbar ist, sollte der Decoder die Dauer als Umkehrung der Audioabtastrate multipliziert mit der Anzahl der Stichproben im Ausgabepuffer berechnen, in Einheiten von 100 Nanosekunden konvertiert und abgerundet werden.

Eine Transformation sollte nur dann eine Stichprobe ohne Zeitstempel aus geben, wenn MFT noch nie einen Zeitstempel für ein Eingabebeispiel erhalten hat oder wenn es keine Möglichkeit gibt, einen genauen Ausgabezeitstempel aus dem vorherigen Eingabezeitstempel zu berechnen.

### <a name="audio-decoders"></a>Audiodecoder

Bei Audiodecodern wird die Dauer jedes Ausgabebeispiels anhand der Audio-Samplingrate und der Anzahl der PCM-Stichproben pro Kanal im Ausgabepuffer berechnet.

Die richtige Methode zum Berechnen von Ausgabezeitstempeln hängt davon ab, ob die Eingabebeispiele Zeitstempel enthalten.

Wenn die Eingabebeispiele Zeitstempel enthalten, berechnet der Decoder die Ausgabezeitstempel wie folgt aus den Eingabezeitstempeln:

-   Wenn jeder Eingabepuffer einen oder mehrere vollständige komprimierte Frames ohne partielle Frames enthält, entspricht der Ausgabezeitstempel dem Eingabezeitstempel abzüglich der bekannten Latenz des Decoders. Beispielsweise hat ein Dolby Digital-Decoder (AC-3) eine Latenz von 256 PCM-Beispielen. Bei einer Samplingrate von 48 kHz beträgt die Latenz beispielsweise 5,33 Millisekunden (msec). Wenn der Eingabezeitstempel also 1.000 msec beträgt, beträgt der Ausgabezeitstempel 1000 – 5,33 = 994,66 msec. Wenn der Eingabepuffer mehr als einen gesamten komprimierten Frame enthält, erzeugt der Decoder ein Ausgabebeispiel für jeden Frame im Eingabebeispiel. Alle Ausgabebeispiele werden ordnungsgemäß mit einem Zeitstempel versehen, sodass keine Lücken bestehen.
-   Je nach Transportformat kann ein Eingabepuffer partielle Frames enthalten. Beispielsweise kann ein Puffer einen Teil eines Frames aus dem vorherigen Eingabepuffer enthalten, gefolgt von einem oder mehr vollständigen Frames, gefolgt vom Anfang des nächsten Frames. In diesem Fall ist es in der Regel richtig, davon auszugehen, dass der Eingabezeitstempel dem ersten Frame entspricht, der innerhalb des Puffers beginnt. (Das heißt, ein teiler Frame, der im vorherigen Puffer gestartet wurde, ist nicht im Zeitstempel für den aktuellen Puffer enthalten.) Berechnen Sie den Ausgabezeitstempel entsprechend.

Wenn die Eingabebeispiele keine Zeitstempel enthalten:

-   Der Decoder sollte seine eigenen Zeitstempel generieren und den ersten Ausgabezeitstempel auf 0 (null) festlegen.
-   Die Stichprobendauer wird aus der Anzahl der Ausgabestichproben im Puffer und der Abtastrate berechnet.
-   Nachfolgende Zeitstempel werden aus dem vorherigen Zeitstempel und der Dauer berechnet: Aktueller Zeitstempel + aktuelle Dauer = nächster Zeitstempel. Es sollten keine Lücken in den Ausgabezeitstempeln bestehen.

Wenn der Eingabestream anfänglich Zeitstempel enthält, aber aus irgendeinem Grund zu keinen Zeitstempeln wechselt, sollte der Decoder weiterhin seine eigenen Ausgabezeitstempel generieren, damit sie kontinuierlich sind und keine Lücke besteht.

Wenn der Eingabestream Zeitstempel enthält, aber Lücken in den Zeiten bestehen, gibt der Decoder diese Lücken einfach weiter. Anders ausgedrückt: Der Decoder sollte nicht versuchen, inkonsistente Zeitstempel im Eingabestream zu korrigieren.

### <a name="mixers"></a>Mischer

> [!Note]  
> In Windows Vista unterstützt die Media Foundation-Pipeline keine MFTs mit mehr als einer Eingabe. MFTs mit mehreren Eingaben werden in Windows 7 unterstützt.

 

Ein Mixer nimmt mehrere Eingaben und gemischt sie in einer Ausgabe. Wenn die Eingabestreams nicht vollständig mit der Rate gesperrt sind oder in der Zeit leicht voneinander entfernt werden, kann es zu Mehrdeutigkeiten darüber kommen, welche Zeit für die Ausgabe festgelegt werden soll. Abhängig vom Medientyp finden Sie hier einige Richtlinien:

-   Audio. Beim Start oder unmittelbar nach einem Leeren oder Leeren sollte ein Audiomixer warten, bis Ausgabebeispiele erzeugt werden, bis er ein Eingabebeispiel für alle erforderlichen Eingabestreams erhalten hat. An diesem Punkt sollte der früheste Zeitstempel der ersten Stichproben als Baseline für die Ausgabezeitstempel verwendet werden. Die anderen Datenströme sollten mit Stille aufschlossen werden, um jede Zeitabweichung zu dämpfen. Wenn eine Stichprobe für einen optionalen Eingabestream empfangen wird, sollte sie auch in die Berechnung einbezogen werden. Ab diesem Zeitpunkt sollte MFT eine kontinuierliche und ununterbrochene Kette von Ausgabezeitstempeln erzeugen. Im Allgemeinen sollte MFT nicht versuchen, eine Datenstromdrift relativ zu einem anderen zu berücksichtigen. Stattdessen sollten die Ausgabezeitstempel aus dem Baselinezeitstempel, der Ausgaberate und den Puffergrößen berechnet werden. Wenn ein weiterer Leerungs- oder Leerungsstempel auftritt, sollte der MFT seine Baselinezeitstempel zurücksetzen.

-   Video. Beim Start oder unmittelbar nach einem Leeren oder Leeren sollte ein Videomixer warten, bis Ausgabebeispiele erzeugt werden, bis er ein Eingabebeispiel für alle erforderlichen Eingabestreams erhalten hat. An diesem Punkt sollte der früheste Zeitstempel der ersten Stichproben als Baseline für die Ausgabezeitstempel verwendet werden. Im Allgemeinen sollte versucht werden, fortlaufende und reguläre Ausgabezeitstempel und feste Dauer zu behalten, auch wenn die Eingabe nicht so normal ist, wenn dies erforderlich ist, indem eingabeframes wiederholt werden.

### <a name="encoders"></a>Encoder

Ein Encoder konvertiert unkomprimierte Audio- oder Videodaten in komprimierte Pakete. Ein Encoder sollte die folgenden Richtlinien befolgen:

-   Der Encoder sollte die Konventionen des Ausgabeformats befolgen. Wenn das Format nicht in der Regel einen Zeitstempel für jede Stichprobe enthält, wie in MPEG-2, benötigt nicht jedes Ausgabebeispiel einen Zeitstempel und eine Dauer.

-   Die Eingabezeitstempel sollten im Ausgabeformat beibehalten werden, wenn das Format Felder für Zeitstempel enthält, es sei denn, bessere Zeitinformationen sind von einer anderen Quelle wie der Anwendung selbst verfügbar.

### <a name="multiplexers"></a>Multiplexer

> [!Note]  
> In Windows Vista unterstützt die Media Foundation-Pipeline keine MFTs mit mehr als einer Eingabe. MFTs mit mehreren Eingaben werden in Windows 7 unterstützt.

 

Ein Multiplexer kombiniert zwei verschiedene Audio- oder Videostreams in einem überlappten Format, z. B. AVI oder MPEG-2 Transport Stream. Ein Multiplexer sollte die folgenden Richtlinien befolgen:

-   Der Multiplexer sollte die Konventionen des Ausgabeformats befolgen. Wenn das Format nicht in der Regel einen Zeitstempel für jede Stichprobe enthält, wie in MPEG-2, benötigt nicht jedes Ausgabebeispiel einen Zeitstempel und eine Dauer.

-   Der Zeitstempel sollte die früheste Zeit widerspiegeln, die auf einem beliebigen Frame platziert wird, der in diesem Paket beginnt, oder die Zeit des ersten Audiobeispiels, das aus diesem Paket decodiert würde. Ignorieren Sie diese Richtlinie, wenn sie mit den Konventionen des Ausgabeformats in Konflikt steht.

### <a name="demultiplexers"></a>Demultiplexer

Ein Demultiplexer teilt ein verleerter Format, z. B. AVI oder MPEG-2 Transport Stream, in die zugrunde liegenden Audio- und Videostreams auf.

Wenn das Format bestimmte Zeitstempelinformationen enthält, die verwendet werden können, um genaue Ausgabezeitstempel basierend auf den Eingabezeitstempeln zu berechnen, sollten diese Informationen verwendet werden. Wenn das Format jedoch Zeiten in einer völlig anderen Basis enthält, die keine Beziehung zu den Eingabezeitstempeln haben und ein genauer Offset zum Eingabezeitstempel nicht berechnet werden kann, sollten die eigenen Zeiten des Formats ignoriert werden.

Wenn das Format keine nutzbaren Zeitstempelinformationen enthält, sollte der Demultiplexer die folgenden Regeln befolgen:

-   Unkomprimierte Ausgabestreams sollten nach Möglichkeit gültige Zeitstempel und Dauer haben, die aus dem nächstgelegenen vorherigen Eingabezeitstempel berechnet werden.

-   Komprimierte Ausgabestreams sollten nur Zeitstempel für das erste Ausgabebeispiel haben, das aus einem Eingabebeispiel mit einem Zeitstempel abgeleitet wurde. Wenn das Eingabebeispiel nicht über einen Zeitstempel verfügt, sollten keine Ausgabebeispiele, die aus diesem Eingabebeispiel abgeleitet wurden, einen Zeitstempel haben. Wenn das Eingabebeispiel in mehrere Ausgabebeispiele zerbrochen ist, sollte nur das erste Ausgabebeispiel einen Zeitstempel und der Rest keine Zeitstempel haben.

### <a name="examples"></a>Beispiele

Beispiel 1: Angenommen, ein Videoeffekt nimmt immer einen unkomprimierten Eingaberahmen an, wendet den Effekt an und kopiert ihn in die Ausgabe. Er hält niemals Frames zurück oder puffert eingaben. Dieser MFT kopiert einfach den Zeitstempel und die Dauer aus dem Eingabebeispiel in das Ausgabebeispiel, sofern diese verfügbar sind, und führt keine Zeitberechnungen durch.

Beispiel 2: Angenommen, ein Audioeffekt transformiert alle bis auf 10 Millisekunden (ms) jedes Eingabepuffers und spart die zusätzlichen 10 ms für die Kombination mit dem nächsten Puffer. Sie ruft einen Datenstrom von Stichproben ab, die alle eine Dauer von 50 ms haben. Die Eingabezeiten werden in der folgenden Tabelle angezeigt.



| Beispiel | Eingabezeit | Eingabedauer | Ausgabezeit | Ausgabedauer |
|--------|------------|----------------|-------------|-----------------|
| 1      | 20         | 50             | 20          | 40              |
| 2      | 70         | 50             | 60          | 50              |
| 3      | 121        | 50             | 110         | 50              |
| 4      | 171        | 50             | 161         | 50              |



 

Beachten Sie die Abweichung von 1 ms zwischen der tatsächlichen Dauer von Stichprobe 2 und der impliziten Dauer basierend auf dem nächsten Zeitstempel (121 ? 70 = 51).

Da der MFT 10 ms zurückhält, gibt er die ersten 40 ms der Eingabestichprobe 1 als Ausgabebeispiel 1 mit einem Zeitstempel von 20 ms und einer Dauer von 40 ms aus.

Ausgabebeispiel 2 kombiniert die zuvor zurückgehaltenen 10 ms mit 40 ms des Eingabebeispiels 2. Dieses Beispiel erhält einen Zeitstempel von 60 ms (der Zeitstempel des vorherigen Eingabebeispiels, 20 ms, plus die Dauer der daten, die bereits aus diesem Beispiel verarbeitet wurden, 40 ms). Es wird eine Dauer von 50 ms angegeben.

Analog dazu hat das nächste Beispiel einen Zeitstempel von 110 ms (70 ms + 40 ms) mit einer Dauer von 50 ms.

Die nächste Berechnung ist interessanter. Der implizite Zeitstempel aus der vorherigen Ausgabezeit und Dauer beträgt 160 ms (Zeitstempel 110 ms + Dauer 50 ms). Der Ausgabezeitstempel sollte jedoch anhand des Eingabezeitstempels des frühesten Eingabebeispiels berechnet werden, das die Ausgabestichprobe zeitlich überlappt, sowie aus der Länge aller Daten, die bereits aus dieser Stichprobe verarbeitet wurden. Das nächstgelegene überlappende Eingabebeispiel ist die Stichprobe 4 (Zeitstempel = 171), aber dies ist nicht das früheste. Die früheste überlappende Stichprobe ist Beispiel 3 (Zeitstempel = 121). Wenn Sie die 40 ms hinzufügen, die bereits aus diesem Beispiel verarbeitet wurden, ergibt sich das Ergebnis 161.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben eines benutzerdefinierten MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 



