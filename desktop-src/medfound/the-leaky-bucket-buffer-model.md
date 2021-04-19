---
description: Der &\# 0034; Leaky Bucket&\# 0034; Modell ist eine Möglichkeit, die Puffer Anforderungen für die reibungslose Wiedergabe zu modellieren.
ms.assetid: 2f7f80d6-3abb-462f-a571-b223a1d59da6
title: Das undichte Bucket-Puffer Modell (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5a99932fb121808f6a49323360c47c09d0acbb
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106355111"
---
# <a name="the-leaky-bucket-buffer-model-microsoft-media-foundation"></a>Das undichte Bucket-Puffer Modell (Microsoft Media Foundation)

Wenn Sie Medien über ein Netzwerk streamen, empfängt der Decoder codierte Daten mit einer theoretisch Konstanten Rate (der Übertragungsrate). Der Decoder verwendet diese Daten, um decodierte Ausgaben zu liefern. Im Allgemeinen verwendet der Decoder die Daten jedoch mit einer *Variablen* Rate, da der Encoder dann eine Variablen Codierungsrate verwenden kann.

Das "Leaky Bucket"-Modell ist eine Möglichkeit, die Puffer Anforderungen für die reibungslose Wiedergabe zu modellieren. In diesem Modell verwaltet der Decoder einen Puffer. Codierte Daten werden vom Netzwerk in den Puffer und vom Puffer in den Decoder. Wenn der Puffer unterfließt, bedeutet dies, dass der Decoder Daten aus dem Puffer schneller entfernt, als vom Netzwerk bereitgestellt werden. Wenn der Puffer überläuft, bedeutet dies, dass das Netzwerkdaten schneller bereitstellt, als der Decoder Sie verwendet.

In diesem Thema wird das Modell "Leaky Bucket" der Puffer für die Codierung und Decodierung beschrieben.

-   [Der Bucket "Leaky"](#the-leaky-bucket)
-   [Der verwendete Bucket](#the-bucket-in-use)
-   [Festlegen von Leaky-Bucket-Werten für ASF-Streams](#setting-leaky-bucket-values-for-asf-streams)
-   [Leaky-Bucket-Werte im ASF-Multiplexer](#leaky-bucket-values-in-the-asf-multiplexer)
-   [Aktualisieren von Leaky-Bucket-Werten in der ASF-Medien Senke](#updating-leaky-bucket-values-in-the-asf-media-sink)
-   [Zugehörige Themen](#related-topics)

## <a name="the-leaky-bucket"></a>Der Bucket "Leaky"

Um das Modell "Leaky Bucket" zu verstehen, betrachten Sie einen Bucket mit einem kleinen Loch unten. Der Bucket wird durch drei Parameter definiert:

-   Die Kapazität (B)
-   Die Rate, mit der Wasser aus dem Bucket fließt (R)
-   Der anfängliche Füllwert des Bucket (F).

In dieser Metapher ist der Bucket der Puffer:

![die Abbildung zeigt einen Puffer als Bucket, eine Eingabe Rate als Wasser in den Bucket und die Ausgabe Rate als Wasser, das eine Lücke im Bucket verlässt.](images/asf-components03.png)

Wenn Wasser in den Bucket zu genau der Geschwindigkeit von *R* gegossen wird, verbleibt der Bucket bei F, da die Eingabe Rate der Ausgabe Rate entspricht. Wenn die Eingabe Rate zunimmt, während *R* konstant bleibt, akkumuliert der Bucket Wasser. Wenn die Eingabe Rate für einen längeren Zeitraum größer als *R* ist, wird der Bucket letztendlich überläuft. Allerdings kann die Eingabe Rate um *R* variieren, ohne den Bucket zu überschreiten, solange die durchschnittliche Eingangs Rate die Kapazität des Bucket nicht überschreitet. Je größer die Kapazität ist, desto mehr kann die Eingabe Rate innerhalb eines bestimmten Zeitfensters variieren.

In ASF wird der "Leaky"-Bucket durch drei Parameter definiert:

-   Die durchschnittliche Bitrate (in Bytes pro Sekunde), die der Ausgabe Rate (*R*) entspricht.
-   Das Puffer Fenster (gemessen in Millisekunden), das der Bucket-Kapazität (*B*) entspricht.
-   Der anfängliche Puffer Füll Wert, der im Allgemeinen auf 0 (null) festgelegt ist.

Die Bitrate misst die durchschnittliche Anzahl von Bits pro Sekunde im codierten Stream. Das Puffer Fenster misst die Anzahl der Millisekunden der Daten an dieser Bitrate, die in den Puffer passen. Die Größe des Puffers in Bits ist gleich R \* (B/1000).

Bei den ASF-Nutzlastdaten kann es vorkommen, dass der Lecky-Bucket zu unregelmäßigen Zeiten und unregelmäßig ist, der Bucket jedoch mit einer Konstanten positiven Bitrate belassen werden muss. Aufgrund des Puffer Fensters gibt es eine mögliche Verzögerung zwischen dem Zeitpunkt, zu dem die Nutzlast in den Bucket gelangt und wann Sie verlässt. Die maximale Verzögerung, die auftreten kann, ist *B* / *R*. Die Nutzlastdaten, die in den Bucket eingegeben werden, entsprechen der Präsentationszeit und dürfen niemals einen Überlauf des Bucket verursachen. Zusätzlich zur Präsentationszeit verfügt jede Nutzlast auch über eine Sendezeit – die Zeit, zu der die Nutzlastdaten den Bucket entsprechend der Bitrate verlassen. Die Sendezeit muss vor der Präsentationszeit liegen, um sicherzustellen, dass jede Nutzlast den Bucket vor oder während der Präsentationszeit verlässt, wenn der Leaky-Bucket fast voll ist. Um dies zu erreichen, werden die Präsentations Zeiten um den *B* / *R* -Wert (das *ein Vorlauf ausgeführt*) verschoben, und die Sendezeiten erhalten einen Anfang, beginnend bei Null. Die Sendezeit darf nicht später sein als die Präsentationszeit, da dies darauf hindeuten würde, dass die Nutzlast zu spät in den Bucket gelangt und nicht in das Datenobjekt eingeschlossen werden kann. Der ein Vorlauf ausgeführt-Wert ist im [ASF-Header Objekt](asf-file-structure.md) enthalten.

Bei einem fehlerfreien Streaming über das Netzwerk müssen komprimierte Datenströme innerhalb des Medien Inhalts während der Wiedergabedauer eine Konstante Bitrate beibehält. Das Modell "ASF Leaky Bucket" stellt sicher, dass Mediendaten mit konstanter Bitrate über das Netzwerk gesendet werden. Die Parameter des "Leaky"-Bucket werden im Eigenschaften Objekt des erweiterten Streams des [ASF-Header Objekts](asf-file-structure.md)angegeben. In Microsoft Media Foundation werden Sie als Attribute für den Medientyp festgelegt, der den Stream darstellt.

Die Lecks-Bucket-Werte werden sowohl in der ASF-Datei-Senke als auch im zugrunde liegenden ASF Multiplexer-Objekt und dem Windows Media Encoder definiert. Diese Werte können gleich oder unterschiedlich sein. Stellen Sie sich beispielsweise ein Streamingszenario vor, das erfordert, dass die Audiobeispiele später als die Videobeispiele zugestellt werden, damit die Datei ohne Latenz gestreamt werden kann. Um dies zu erreichen, kann der UNY-Bucket des Audiodatenstroms in der Medien Senke auf einen Wert festgelegt werden, der höher als der im Windows Media-Audioencoder festgelegte Wert ist.

Um B/R-Werte im Encoder festzulegen, muss die Anwendung die [**\_ bmax**](mfpkey-bmaxproperty.md) -Eigenschaften " [**mfpkey \_ Ravg**](mfpkey-ravgproperty.md)", " [**mfpkey \_ bavg**](mfpkey-bavgproperty.md)", " [**mfpkey \_ Rmax**](mfpkey-rmaxproperty.md)" und "mfpkey" festlegen. Weitere Informationen zum Festlegen von Eigenschaften im Encoder finden Sie unter [Codierungs Eigenschaften](configuring-the-encoder.md).

## <a name="the-bucket-in-use"></a>Der verwendete Bucket

Das Ziel eines Encoders besteht darin sicherzustellen, dass der Inhalt niemals den Puffer überschreitet. Der Encoder verwendet die Werte für Bitrate und Puffer Fenster als Handbücher. Die tatsächliche Anzahl von Bits, die über einen beliebigen Zeitraum des Puffer Fensters übergeben wird, darf nicht größer als die doppelte Größe des Puffers sein.

Sehen Sie sich das folgende Beispiel an: Sie haben einen 3-Gallone-Bucket mit einem Loch darin, in dem 1 Gallone pro Minute fließen kann. Sie platzieren den Bucket unter einem Spigot und öffnen das Ventil, um Wasser mit einer Rate von 1 Gallone pro Minute auszulassen. Der Wasserfluss fließt so schnell wie möglich aus dem Bucket, ohne zusätzliche im Bucket. Dann erhöhen Sie den Flow von Spigot auf 2 Gallonen pro Minute. Jede Minute, in der sich der Wasserfluss ergibt, werden 2 Gallonen in den Bucket geleitet und 1 Gallone wird verworfen, sodass 1 Gallone im Bucket bleibt. Am Ende der drei Minuten sind 6 Gallonen des Wassers in den Bucket gewechselt, drei Gallonen sind ausgelaufen, und der Bucket ist voll.

In der Praxis wird die theoretisch maximale Datenrate für ein Intervall, das dem Puffer Fenster entspricht, niemals erreicht. Im vorherigen Beispiel wurde eine konstante Datenrate angenommen. Mit dem gleichen 3-Gallon-Bucket können Sie die Flowrate von Spigot auf 6 Gallonen pro Minute für eine Minute erhöhen und dann den Spigot für zwei Minuten deaktivieren. Obwohl sich die Gesamtmenge an Wasser in den Bucket innerhalb des theoretischen Höchstwerts für das Puffer Fenster befindet, bewirkt die Konzentration dieses Betrags in einen Teil des Fensters einen Überlauf des Bucket. Bei 6 Gallonen pro Minute wird der 3-Gallon-Bucket kurz nach 30 Sekunden überlaufen. Daher hängt die tatsächliche maximale Datenmenge, die für die Dauer eines beliebigen Intervalls gleich der Puffer Fenster Einstellung an den Puffer übermittelt werden kann, von der Größe einzelner Stichproben und der übermittelten ab.

Bisher haben die Beispiele nur den vom Decoder verwendeten Puffer behandelt, aber auch der Encoder verwendet einen unkomprimierten Bucket-Puffer, der den komprimierten Inhalt erstellt. Der Encoder führt alle Anpassungen aus, die für die Komprimierungs Algorithmen erforderlich sind, um die Bitrate der komprimierten Stichproben innerhalb der durch die Bitrate und das Puffer Fenster beschriebenen Grenzen beizubehalten. dabei wird vorausgesetzt, dass die Beispiele mit konstanter Rate an den Decoder übermittelt werden. Sie können sich den Encoder-Bucket als Spiegelung des Decoder-Bucket vorstellen. Der Encoder-Bucket wird mit einer Variablen Rate aufgefüllt, die durch die Größe der einzelnen Stichproben und die Werte mit einer konstanten Rate, die der durchschnittlichen Bitrate entspricht, bestimmt wird.

Sehen Sie sich das folgende Beispiel eines Encoders und Decoders an, die über ein Netzwerk miteinander verbunden sind. Sie codieren eine Videodatei mit 30 Frames pro Sekunde mit einer Bitrate von 6.000 Bits pro Sekunde und einem Puffer Fenster von 3 Sekunden (eine Gesamt Puffergröße von 18.000 Bits). Das erste Beispiel wird als Keyframe codiert und erfordert 7.000 Bits. Der Encoder-Puffer enthält jetzt 7.000 Bits. Die nächsten 29 Frames sind alle Delta Frames, die insgesamt 3.000 Bits betragen. Der erste zweite Inhalt (30 Frames) würde also den Puffer in 10.000 Bits einfügen, wenn nichts zurückgegeben würde. Wir wissen, dass die Bitrate des Streams 6.000 Bits pro Sekunde beträgt. Nachdem die erste Sekunde von codiertem Inhalt in den Codierungs Puffer eingefügt wurde, wird der Füllwert auf 4.000 Bits festgestellt. In der Decodierungs Anwendung wird dieser Stream an den Decoder-Puffer mit 6.000 Bits pro Sekunde übermittelt. Nach einer Sekunde enthält der Puffer 6.000 Bits. Das erste Beispiel enthält 7.000 Bits, sodass der Decoder-Puffer mehr ausgefüllt werden muss, bevor der Decoder mit dem Entfernen von Beispielen beginnt.

## <a name="setting-leaky-bucket-values-for-asf-streams"></a>Festlegen von Leaky-Bucket-Werten für ASF-Streams

In einem Datei Codierungs Szenario kann eine Anwendung die Werte für den Leaky-Bucket beim Konfigurieren der Streams im [ASF-Profil](asf-profile.md)festlegen.

Nachdem Sie den Stream erstellt und einen Verweis auf die [**imfasfstreamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) -Schnittstelle des Streams erstellt haben, können Sie die Werte mithilfe der folgenden Attribute festlegen:

-   [**MF \_ Asfstreamconfig \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (durchschnittliche Anzahl von Lecks-Bucket-Werten)
-   [**MF \_ Asfstreamconfig \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (maximale Anzahl von unzulässigen Bucket-Werten)

Weitere Informationen zum Hinzufügen von Streams und zum erhalten des **imfasfstreamconfig** -Zeigers finden [Sie unter Hinzufügen von streaminformationen zur ASF-Datei Senke](adding-stream-information-to-the-asf-file-sink.md).

Diese Werte enthalten die folgenden Informationen:

-   Durchschnittliche Bitrate: Geben Sie die durchschnittliche Bitrate aus dem Ausgabe Medientyp an, der während der Medientyp Aushandlung ausgewählt wird. Verwenden Sie das Attribut " [**MF \_ MT \_ -audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md) " (für audiodatenstreams) oder das " [**MF \_ MT \_ AVG \_ Bitrate**](mf-mt-avg-bitrate-attribute.md) "-Attribut (für Videostreams).
-   Puffer Fenster: Wenn Sie über eine Instanz des Encoders verfügen und Ausgabemedien Typen ausgehandelt haben, können Sie diesen Wert zu einem späteren Zeitpunkt aktualisieren, indem Sie den Encoder für die [**iwmcodecleakybucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) -Schnittstelle Abfragen und anschließend [**iwmcodecleakybucket:: getbuffersizebits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecigesichter. h, wmcodecdspuuid Andernfalls verwenden Sie den Standardwert von 3000 Millisekunden.
-   Anfängliche Puffergröße: wird auf 0 festgelegt.

Die Werte, die von der Anwendung bereitgestellt werden, hängen vom Codierungstyp und dem Medientyp des Streams ab. Beispielsweise erfordert die [Konstante Bitrate-Codierung](constant-bit-rate-encoding.md) eine vorgegebene festgelegte Bitrate und ein Puffer Fenster. Die Anwendung kann diese Lecks-Bucket-Werte angeben, indem Sie die Eigenschaft " [**mfpkey \_ videowindow**](mfpkey-videowindowproperty.md) Encoding" und das Attribut " [**MF \_ asfstreamconfig \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) " für den Datenstrom festlegt. Die angegebenen Puffer Fenster Werte werden verwendet, um sicherzustellen, dass für die codierte Datei die richtigen Sendezeiten in den Datenpaketen gekennzeichnet sind und der ein Vorlauf ausgeführt-Wert im Objekt des ASF-Headers angezeigt wird. Es genügt, dass Sie " **MF \_ asfstreamconfig \_ LEAKYBUCKET1** " festlegen, da diese angegebenen Werte in das MF-Attribut " [**\_ asfstreamconfig \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) " kopiert werden.

Für den 2-Durchlauf-Codierungs Modus müssen Sie beide Attribute festlegen, um die durchschnittlichen und maximalen Werte anzugeben.

Bei der VBR-Codierung kann die Anwendung nach Abschluss der Codierungs Übergabe die vom Encoder verwendeten Werte vom Typ "Leaky Bucket" Abfragen. Aus diesem Grund kann die Anwendung beim Konfigurieren der Medien Senke festlegen, dass die Attribute oder Eigenschaften, die sich auf ein unkompatibilitäts Bucket beziehen, festgelegt werden. Nach der Codierung muss die Anwendung den Encoder nach den Eigenschaften " [**mfpkey \_ Ravg**](mfpkey-ravgproperty.md)", " [**mfpkey \_ bavg**](mfpkey-bavgproperty.md)", " [**mfpkey \_ Rmax**](mfpkey-rmaxproperty.md)" und " [**mfpkey \_ bmax**](mfpkey-bmaxproperty.md) " Abfragen und Sie in der Medien Senke festlegen, damit die exakten Werte im Header Objekt widergespiegelt werden. Ein Codebeispiel zum Aktualisieren der Werte für die VBR-Codierung finden Sie unter "Aktualisieren der Codierungs Eigenschaften in der Datei Senke" in [Tutorial: 1-Pass Windows Media Encoding](tutorial--1-pass-windows-media-encoding.md).

Wenn Sie Windows Media-Inhalte aus der Quelle in die Medien Senke ohne Codierung kopieren, müssen die Werte für den Leaky-Bucket in der Medien Senke festgelegt werden.

## <a name="leaky-bucket-values-in-the-asf-multiplexer"></a>Leaky-Bucket-Werte im ASF-Multiplexer

In Media Foundation werden die Werte für den Leaky-Hashwert vom [ASF Multiplexer](asf-multiplexer.md) verwendet, um die internen Lecks-Bucket-Werte einzurichten, die für die Generierung von Datenpaketen verwendet werden. Die Nutzlast ist in einem Medien Beispiel enthalten, und eine Reihe von Medien Beispielen bilden ein ASF-Datenpaket. Basierend auf den unkonstanten Bucket-Werten und der Präsentationszeit weist der Multiplexer eine Sendezeit für jedes Medien Beispiel zu, sodass die Bitraten der über das Netzwerk gesendeten Pakete zu einer konstanten Bitrate (*R*) werden.

Eine Anwendung kann im Multiplexer nicht direkt Werte für "Leaky Bucket" festlegen. Die Werte müssen in der ASF-Medien Senke bereitgestellt werden, mit der die entsprechenden Werte für den Multiplexer festgelegt werden. Die in [**MF \_ asfstreamconfig \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) und [**MF \_ asfstreamconfig \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) festgelegten Werte werden vom Multiplexer verwendet, um zu überprüfen, ob die an die ASF-Medien Senke gesendeten Beispiele mithilfe der angegebenen Werte generiert werden.

## <a name="updating-leaky-bucket-values-in-the-asf-media-sink"></a>Aktualisieren von Leaky-Bucket-Werten in der ASF-Medien Senke

Eine Anwendung kann die Lecks-Bucket-Werte auf Streamebene (festgelegt im ASF-Profil während der Datenstrom Erstellung) überschreiben, indem die [**mfpkey \_ asfstreamsink \_ korrigiert \_ leakybucket**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) -Eigenschaft im Eigenschaften Speicher der Medien Senke festgelegt wird. Um einen Verweis auf den Eigenschaften Speicher zu erhalten, verwenden Sie das von der Medien Senke implementierte ContentInfo-Objekt. Weitere Informationen finden Sie unter [Festlegen von Eigenschaften in der Datei Senke](setting-properties-in-the-file-sink.md).

**Hinweis**  Dieser Vorgang ist nur für Audiostreams zulässig.

Diese Eigenschaft muss festgelegt werden, nachdem Sie den Ausgabetyp für den Encoder festgelegt haben. Basierend auf der Bitrate, die im Medientyp festgelegt ist, berechnet der Encoder die Puffergröße, um sicherzustellen, dass die generierten Medien Beispiele niemals einen Überlauf des Puffers verursachen. Der Encoder nimmt während der Komprimierung erforderliche Anpassungen vor, um die Bitrate der komprimierten Stichproben innerhalb der Grenzen beizubehalten, die durch die Bitrate und das Puffer Fenster beschrieben werden.

Legen Sie ähnlich wie bei den Datenstrom-Konfigurations Attributen für leckige Bucket die durchschnittliche Bitrate und die Puffergröße sowie die anfängliche Puffergröße in einem Array von DWords fest. Weitere Informationen finden Sie im Abschnitt "Festlegen von Lecks-Bucket-Werten für ASF-Streams" in diesem Thema.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützung von ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Windows Media-Codecs](windows-media-codecs.md)
</dt> </dl>

 

 
