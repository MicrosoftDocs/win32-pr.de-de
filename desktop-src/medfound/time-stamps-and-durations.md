---
description: In diesem Thema wird beschrieben, wie Media Foundation Transformationen Zeitstempel verarbeiten sollten.
ms.assetid: 4ab576ce-becd-4736-921e-e463c0dff841
title: Zeitstempel und Dauer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2323c11fa0e3ec2b2b2d5ba1cefe4f5d5fa80c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130465"
---
# <a name="time-stamps-and-durations"></a>Zeitstempel und Dauer

In diesem Thema wird beschrieben, wie [Media Foundation Transformationen](media-foundation-transforms.md) Zeitstempel verarbeiten sollten.

Ein MFT muss in allen Ausgabe Beispielen als genau einen Zeitstempel und eine Dauer festgelegt werden. Bei einem einfachen MFT, das einen Eingabepuffer annimmt und ihn vollständig in einem Ausgabepuffer verarbeitet, sollte der MFT den Zeitstempel und die Dauer direkt aus dem Eingabe Beispiel in das Ausgabe Beispiel kopieren. Viele Transformationen sind jedoch komplexer als dies und erfordern möglicherweise komplexere Berechnungen der Ausgabezeit. Alle MFTs sollten die folgenden grundlegenden Regeln beachten:

-   Ein MFT sollte versuchen, einen Zeitstempel und eine Dauer für alle nicht komprimierten Video-oder audioausgabebeispiele abzulegen, wenn ein präziser Zeitstempel oder eine Dauer für die Eingabe Stichproben angegeben ist oder berechnet werden kann. Für einige Ausgabezeit Stempel ist möglicherweise eine Interpolations Zeit erforderlich, insbesondere für Decoder.
-   Die Zeitstempel und die Dauer der Eingabe Stichproben sollten in den Ausgabe Beispielen so weit wie möglich beibehalten werden.
-   Die Ausgabezeit Stempel oder-Zeiträume stimmen möglicherweise nicht mit der Eingabe ab, da die MFT Daten zurückgibt oder die Ausgabe in andere Teile als die Eingabe abbricht. In diesem Fall sollte der MFT den Ausgabezeit Stempel aus dem frühesten Eingabe Beispiel berechnen, der Daten enthält, die zum Erstellen des Ausgabe Beispiels verwendet werden. Fügen Sie zum Berechnen des Ausgabezeit Stempels der Dauer der Daten, die bereits aus diesem Beispiel transformiert wurden, den Eingabe Zeitstempel des entsprechenden Eingabe Beispiels hinzu. Im zweiten Beispiel am Ende dieses Abschnitts wird diese Idee veranschaulicht.
-   Wenn die Eingabe Beispiele eine Dauer aufweisen, sollte diese Dauer beibehalten werden. Wenn eine Eingabe Stichprobe keine Dauer hat, sollte der MFT nach Möglichkeit eine Dauer berechnen, die aus der Größe des Ausgabepuffers oder der durch den Medientyp gegebenen Daten Rate besteht.
-   Berechnete Zeiträume sollten abgeschnitten (abgerundet), nicht auf das nächste Inkrement gerundet werden. Die Pipeline verfügt über genügend Slack, um Zeiträume zu verarbeiten, die etwas ungenau sind, aber es ist einfacher für die Pipeline, eine Dauer zu verarbeiten, die 1% zu kurz ist als eine Dauer von 1% zu lang. Das heißt, es gibt keinen Grund, die Dauer absichtlich zu verkürzen, außer durch Rundung.

### <a name="decoders"></a>Decoder

Ein Decoder konvertiert komprimierte Pakete in unkomprimierte Daten. Da die Ausgabe nicht komprimiert ist, haben Decoder eine besondere Verpflichtung, die Zeitstempel und die Dauer zu korrigieren. Einige komprimierte Formate, insbesondere MPEG-2, haben keine Zeitstempel für alle Eingabe Pakete und haben häufig keine Dauer für ein Paket. Bei diesen Formaten ist der Decoder dafür verantwortlich, einen gültigen Zeitstempel und eine Dauer für jedes Ausgabe Beispiel zu setzen, indem er die impliziten Dauer der gesamten Ausgabe seit dem letzten Zeitstempel-Eingabe Beispiel summiert.

Wenn die Dauer für Videos nicht im komprimierten Format verfügbar ist, sollte der Decoder die Dauer als Umkehrung der Framerate berechnen, in 100-Nanosecond-Einheiten konvertiert und abgerundet werden.

Wenn die Dauer für Audiodaten nicht im komprimierten Format verfügbar ist, sollte der Decoder die Dauer als Umkehrung der audiobeispielrate multipliziert mit der Anzahl der Stichproben im Ausgabepuffer, in 100-Nanosecond-Einheiten konvertiert und abgerundet werden.

Eine Transformation sollte nur dann eine Stichprobe ohne einen Zeitstempel ausgeben, wenn die MFT nie einen Zeitstempel für ein Eingabe Beispiel erhalten hat, oder wenn es keine Möglichkeit gibt, einen exakten Ausgabezeit Stempel aus dem vorherigen Eingabe Zeitstempel zu berechnen.

### <a name="audio-decoders"></a>Audiodecoder

Für Audiodecoder wird die Dauer der einzelnen Ausgabe Stichprobe aus der audiosamplingrate und der Anzahl der PCM-Stichproben pro Kanal im Ausgabepuffer berechnet.

Die korrekte Methode zum Berechnen der Ausgabezeit Stempel hängt davon ab, ob die Eingabe Beispiele Zeitstempel enthalten.

Wenn die Eingabe Beispiele Zeitstempel enthalten, berechnet der Decoder die Ausgabezeit Stempel aus den Eingabe Zeitstempeln wie folgt:

-   Wenn jeder Eingabepuffer eine oder mehrere vollständige komprimierte Frames ohne partielle Frames enthält, entspricht der Ausgabezeit Stempel dem Eingabe Zeitstempel abzüglich der bekannten Latenz des Decoders. Ein Dolby Digital (AC-3)-Decoder hat z. b. eine Latenz von 256 PCM-Stichproben. Bei der Samplingrate von 48-kHz beträgt die Latenz z. b. 5,33 Millisekunden (MS). Wenn der Eingabe Zeitstempel also 1000 ms beträgt, lautet der Ausgabezeit Stempel 1000 – 5,33 = 994,66 ms. Wenn der Eingabepuffer mehr als einen vollständigen komprimierten Frame enthält, erzeugt der Decoder ein Ausgabe Beispiel für jeden Frame im Eingabe Beispiel. Alle Ausgabe Beispiele werden ordnungsgemäß mit einem Zeitstempel versehen, sodass keine Lücken vorhanden sind.
-   Abhängig vom Transport Format kann ein Eingabepuffer partielle Frames enthalten. Ein Puffer kann z. b. einen Teil eines Frames aus dem vorherigen Eingabepuffer enthalten, gefolgt von einem oder mehreren abgeschlossenen Frames, gefolgt vom Anfang des nächsten Frames. In diesem Fall ist es im allgemeinen richtig, anzunehmen, dass der Eingabe Zeitstempel dem ersten Frame entspricht, der innerhalb des Puffers beginnt. (Das heißt, ein partieller Frame, der im vorherigen Puffer gestartet wurde, ist nicht im Zeitstempel des aktuellen Puffers enthalten.) Berechnen Sie den Ausgabezeit Stempel entsprechend.

Wenn die Eingabe Beispiele keine Zeitstempel enthalten:

-   Der Decoder sollte seine eigenen Zeitstempel generieren und den ersten Ausgabezeit Stempel auf NULL festlegen.
-   Die Stichproben Dauer wird anhand der Anzahl von Ausgabe Beispielen im Puffer und der Stichprobenrate berechnet.
-   Nachfolgende Zeitstempel werden aus dem vorherigen Zeitstempel und der Dauer berechnet: Aktueller Zeitstempel + aktuelle Dauer = nächster Zeitstempel. Es sollten keine Lücken in den Ausgabezeit Stempeln vorliegen.

Wenn der Eingabedaten Strom Anfangszeit Stempel enthält, aber aus irgendeinem Grund zu keinem Zeitstempel wechselt, sollte der Decoder weiterhin seine eigenen Ausgabezeit Stempel generieren, sodass Sie kontinuierlich sind und keine Lücke vorhanden ist.

Wenn der Eingabedaten Strom Zeitstempel enthält, aber es gibt Lücken in den Zeiten, gibt der Decoder diese Lücken einfach weiter. Anders ausgedrückt: der Decoder sollte nicht versuchen, inkonsistente Zeitstempel im Eingabestream zu korrigieren.

### <a name="mixers"></a>Mischer

> [!Note]  
> In Windows Vista unterstützt die Media Foundation Pipeline keine MFTs mit mehr als einer Eingabe. MFTs mit mehreren Eingaben werden in Windows 7 unterstützt.

 

Ein Mixer nimmt mehrere Eingaben an und mischt sie in eine Ausgabe ein. Wenn die Eingabedaten Ströme nicht vollständig von der Rate gesperrt sind oder leicht zeitgleich versetzt werden, kann die festgelegte Zeit in der Ausgabe mehrdeutig sein. Im folgenden finden Sie einige Richtlinien, abhängig vom Medientyp:

-   Audio. Beim Start oder unmittelbar nach einer Ableitung oder Leerung sollte ein Audiomixer warten, bis Ausgabe Beispiele erzeugt werden, bis er ein Eingabe Beispiel für alle erforderlichen Eingabedaten Ströme erhalten hat. An diesem Punkt sollte der früheste Zeitstempel der anfänglichen Stichproben ausgewählt werden, der als Grundlage für die Ausgabezeit Stempel verwendet werden soll. Die anderen Streams sollten mit Ruhe aufgefüllt werden, um eine beliebige Zeit Abweichung zu bilden. Wenn eine Stichprobe in einem optionalen Eingabedaten Strom empfangen wird, sollte Sie auch in die Berechnung einbezogen werden. Ab diesem Zeitpunkt sollte der MFT eine kontinuierliche und ununterbrochene Kette von Ausgabezeit Stempeln entwickeln. Im Allgemeinen sollte der MFT nicht versuchen, einen Datenstrom in Relation zu einem anderen zu übertragen. Stattdessen sollte die Ausgabezeit Stempel aus dem Baseline-Zeitstempel, der Ausgabe Rate und den Puffergrößen berechnet werden. Wenn eine andere Ableitung oder Leerung auftritt, sollte der MFT seine Baseline-Zeitstempel zurücksetzen.

-   Video. Beim Start oder unmittelbar nach einer Ableitung oder Leerung sollte ein Video-Mixer warten, bis Ausgabe Beispiele erzeugt werden, bis er ein Eingabe Beispiel für alle erforderlichen Eingabedaten Ströme erhalten hat. An diesem Punkt sollte der früheste Zeitstempel der anfänglichen Stichproben ausgewählt werden, der als Grundlage für die Ausgabezeit Stempel verwendet werden soll. Im Allgemeinen sollte Sie sich darauf konzentrieren, kontinuierliche und reguläre Ausgabezeit Stempel und die Dauer zu korrigieren, auch wenn die Eingabe nicht so regulär ist, wenn dies durch wiederholte Eingabe Frames notwendig ist.

### <a name="encoders"></a>Encoder

Ein Encoder konvertiert unkomprimierte Audiodaten oder Videos in komprimierte Pakete. Ein Encoder sollte die folgenden Richtlinien befolgen:

-   Der Encoder muss den Konventionen des Ausgabeformats folgen. Wenn das Format in der Regel nicht jedes Beispiel mit einem Zeitstempel versehen wird, wie in MPEG-2, benötigen nicht alle Ausgabe Beispiele einen Zeitstempel und eine Dauer.

-   Die Eingabe Zeitstempel sollten im Ausgabeformat beibehalten werden, wenn das Format über Felder für Zeitstempel verfügt, es sei denn, es handelt sich um bessere Zeit Informationen, die von einer anderen Quelle verfügbar sind, z. b. die Anwendung selbst.

### <a name="multiplexers"></a>Multiplexers (

> [!Note]  
> In Windows Vista unterstützt die Media Foundation Pipeline keine MFTs mit mehr als einer Eingabe. MFTs mit mehreren Eingaben werden in Windows 7 unterstützt.

 

Ein Multiplexer kombiniert zwei unterschiedliche Audio-oder Videostreams zu einem verschachtelten Format, wie z. b. AVI oder MPEG-2-Transportstream. Ein Multiplexer sollte folgende Richtlinien befolgen:

-   Der Multiplexer muss den Konventionen des Ausgabeformats folgen. Wenn das Format in der Regel nicht jedes Beispiel mit einem Zeitstempel versehen wird, wie in MPEG-2, benötigen nicht alle Ausgabe Beispiele einen Zeitstempel und eine Dauer.

-   Der Zeitstempel sollte die früheste Zeit für einen Frame, der in diesem Paket beginnt, oder die Uhrzeit des ersten audiobeispiels widerspiegeln, die von diesem Paket decodiert wird. Ignorieren Sie diese Richtlinie, wenn Sie mit den Konventionen des Ausgabeformats in Konflikt steht.

### <a name="demultiplexers"></a>Demultiplexer

Ein Demultiplexer teilt ein überlappendes Format (z. b. AVI oder MPEG-2-Transportstream) in die zugrunde liegenden Audiodaten Ströme auf.

Wenn das Format bestimmte Zeitstempel Informationen enthält, die verwendet werden können, um genaue Ausgabezeit Stempel basierend auf den Eingabe Zeitstempeln zu berechnen, sollten diese Informationen verwendet werden. Wenn das Format jedoch Zeiten in einer vollständig anderen Basis enthält, die keine Beziehung zu den Eingabe Zeitstempeln haben, und ein präziser Offset zum Eingabe Zeitstempel nicht berechnet werden kann, sollten die eigenen Zeiten des Formats ignoriert werden.

Wenn das Format keine verwendbaren Zeitstempel Informationen enthält, sollte der Demultiplexer diese Regeln befolgen:

-   Nicht komprimierte Ausgabestreams sollten nach Möglichkeit über gültige Zeitstempel und Dauer verfügen, die anhand des nächstgelegenen vorherigen Eingabe Zeitstempels berechnet werden.

-   Komprimierte Ausgabestreams sollten Zeitstempel nur für das erste Ausgabe Beispiel aufweisen, das aus einem Eingabe Beispiel mit einem Zeitstempel abgeleitet ist. Wenn das Eingabe Beispiel keinen Zeitstempel hat, sollten keine Ausgabe Beispiele, die von diesem Eingabe Beispiel abgeleitet werden, über einen Zeitstempel verfügen. Wenn das Eingabe Beispiel in mehrere Ausgabe Beispiele aufgeteilt ist, sollte nur das erste Ausgabe Beispiel einen Zeitstempel aufweisen, und der Rest sollte keine Zeitstempel enthalten.

### <a name="examples"></a>Beispiele

Beispiel 1: Angenommen, ein Videoeffekt nimmt immer einen nicht komprimierten Eingabe Rahmen an, wendet den Effekt an und kopiert ihn in die Ausgabe. Er hält niemals Frames zurück oder puffert Eingaben. Diese MFT kopiert einfach den Zeitstempel und die Dauer aus dem Eingabe Beispiel in das Ausgabe Beispiel, sofern diese verfügbar sind, und führt überhaupt keine Zeit Berechnungen durch.

Beispiel 2: Nehmen wir an, dass ein Audioeffekt alle 10 Millisekunden (MS) jedes Eingabe Puffers transformiert und die zusätzlichen 10 MS zum kombinieren mit dem nächsten Puffer speichert. Es wird ein Datenstrom von Beispielen abgerufen, die alle eine Dauer von 50 ms haben. Die Eingabe Zeiten sind in der folgenden Tabelle aufgeführt.



| Beispiel | Eingabe Zeit | Eingabe Dauer | Ausgabezeit | Ausgabe Dauer |
|--------|------------|----------------|-------------|-----------------|
| 1      | 20         | 50             | 20          | 40              |
| 2      | 70         | 50             | 60          | 50              |
| 3      | 121        | 50             | 110         | 50              |
| 4      | 171        | 50             | 161         | 50              |



 

Beachten Sie die 1-MS-Abweichung zwischen der tatsächlichen Dauer von Stichprobe 2 und der impliziten Dauer basierend auf dem nächsten Zeitstempel (121? 70 = 51).

Da der MFT 10 MS zurückhält, gibt er die ersten 40 ms der Eingabe Stichprobe 1 als Ausgabe Beispiel 1 mit einem Zeitstempel von 20 ms und einer Dauer von 40 ms aus.

Ausgabe Beispiel 2 kombiniert die 10 MS, die zuvor mit 40 ms der Eingabe Stichprobe 2 zurück gehalten wurden. Dieses Beispiel erhält einen Zeitstempel von 60 ms (der Zeitstempel des vorherigen Eingabe Beispiels, 20 ms, zuzüglich der Dauer der Daten, die aus diesem Beispiel bereits verarbeitet wurden, 40 ms). Es erhält eine Dauer von 50 ms.

Ebenso hat das nächste Beispiel einen Zeitstempel von 110ms (70ms + 40 ms) mit einer Dauer von 50 ms.

Die nächste Berechnung ist interessanter. Der implizite Zeitstempel aus der vorherigen Ausgabezeit und Dauer beträgt 160 MS (Zeitstempel 110 ms + Dauer 50 ms). Allerdings sollte der Ausgabezeit Stempel aus dem Eingabe Zeitstempel des frühesten Eingabe Beispiels berechnet werden, das das Ausgabe Beispiel zeitlich überlappt, zuzüglich der Länge der Daten, die bereits aus diesem Beispiel verarbeitet wurden. Das nächstgelegene überlappende Eingabe Beispiel ist das Beispiel 4 (Zeitstempel = 171), aber dies ist nicht das früheste. Das früheste überlappende Beispiel ist Sample 3 (Zeitstempel = 121). Wenn die 40 ms hinzugefügt werden, die aus diesem Beispiel bereits verarbeitet wurden, ist das Ergebnis 161.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben eines benutzerdefinierten MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 



