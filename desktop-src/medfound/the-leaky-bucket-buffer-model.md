---
description: Das &\# 0034;leaky bucket&\# 0034;-Modell ist eine Möglichkeit, die Pufferanforderungen für eine reibungslose Wiedergabe zu modellieren.
ms.assetid: 2f7f80d6-3abb-462f-a571-b223a1d59da6
title: Das Leaky Bucket Buffer Model (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848a0088a0e2b155deb6945e4a6532edb2677dc484341e50172f1bb1eb8187d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238051"
---
# <a name="the-leaky-bucket-buffer-model-microsoft-media-foundation"></a>Das Leaky Bucket Buffer Model (Microsoft Media Foundation)

Wenn Sie Medien über ein Netzwerk streamen, empfängt der Decoder codierte Daten mit einer theoretisch konstanten Rate (der Übertragungsrate). Der Decoder nutzt diese Daten, um eine decodierte Ausgabe zu erzeugen. Im allgemeinen Fall verwendet der Decoder die Daten jedoch mit einer *variablen* Rate, da der Encoder dann eine variable Codierungsrate verwenden kann.

Das "Leaky Bucket"-Modell ist eine Möglichkeit, die Pufferanforderungen für eine reibungslose Wiedergabe zu modellieren. In diesem Modell verwaltet der Decoder einen Puffer. Codierte Daten werden aus dem Netzwerk in den Puffer und aus dem Puffer in den Decoder übertragen. Wenn der Puffer unterfließt, bedeutet dies, dass der Decoder Daten schneller aus dem Puffer entfernt, als vom Netzwerk bereitgestellt wird. Wenn der Puffer überläuft, bedeutet dies, dass das Netzwerk Daten schneller liefert, als der Decoder sie verbraucht.

In diesem Thema wird das Modell "Leaky Bucket" von Puffern für die Codierung und Decodierung beschrieben.

-   [Der Bucket "Leaky"](#the-leaky-bucket)
-   [Der verwendete Bucket](#the-bucket-in-use)
-   [Festlegen von "Leaky Bucket Values" für ASF Streams](#setting-leaky-bucket-values-for-asf-streams)
-   [Leaky Bucket Values in the ASF Multiplexer](#leaky-bucket-values-in-the-asf-multiplexer)
-   [Aktualisieren von Leaky Bucket-Werten in der ASF-Mediensenke](#updating-leaky-bucket-values-in-the-asf-media-sink)
-   [Zugehörige Themen](#related-topics)

## <a name="the-leaky-bucket"></a>Der Bucket "Leaky"

Um das leaky Bucket-Modell zu verstehen, ziehen Sie einen Bucket mit einem kleinen Löcher am unteren Rand in Betracht. Drei Parameter definieren den Bucket:

-   Die Kapazität (B)
-   Die Rate, mit der Wasser aus dem Bucket fließt (R)
-   Die anfängliche Füllkraft des Buckets (F)

In dieser Metapher ist der Bucket der Puffer:

![Abbildung, die einen Puffer als Bucket, die Eingaberate als Wasser, das in den Bucket eintritt, und die Ausgaberate als Wasser, das durch eine Lücke im Bucket verlässt](images/asf-components03.png)

Wenn Wasser mit der genauen Rate *R* in den Bucket eingespeisten wird, verbleibt der Bucket bei F, da die Eingaberate der Ausgaberate entspricht. Wenn die Eingaberate steigt, während *R* konstant bleibt, sammelt der Bucket Wasser. Wenn die Eingaberate für einen längeren Zeitraum größer als *R* ist, überläuft der Bucket schließlich. Die Eingaberate kann jedoch in *R* variieren, ohne den Bucket zu überlaufen, solange die durchschnittliche Eingaberate die Kapazität des Buckets nicht überschreitet. Je größer die Kapazität ist, desto mehr kann die Eingaberate innerhalb eines bestimmten Zeitfensters variieren.

In ASF wird der leaky-Bucket durch drei Parameter definiert:

-   Die durchschnittliche Bitrate in Bytes pro Sekunde, die der Ausgaberate (*R*) entspricht.
-   Das Pufferfenster in Millisekunden, das der Bucketkapazität (*B*) entspricht.
-   Die anfängliche Pufferfülle, die im Allgemeinen auf 0 (null) festgelegt ist.

Die Bitrate misst die durchschnittliche Anzahl von Bits pro Sekunde im codierten Stream. Das Pufferfenster misst die Anzahl der Millisekunden an Daten mit dieser Bitrate, die in den Puffer passen kann. Die Größe des Puffers in Bits ist gleich R \* (B/1000).

ASF-Nutzlastdaten können zu unregelmäßigen Zeiten und in unregelmäßigen Mengen in den Bucket "Leaky" gelangen, müssen den Bucket jedoch mit einer konstanten positiven Bitrate belassen. Aufgrund des Pufferfensters gibt es eine mögliche Verzögerung zwischen dem Zeitpunkt, zu dem die Nutzlast in den Bucket eintritt, und dem Zeitpunkt, zu dem sie verlässt. Die maximale Verzögerung, die auftreten kann, ist *B* / *R*. Die Nutzlastdaten, die in den Bucket gelangen, sind gemäß der Präsentationszeit und dürfen nie über den Bucket überlaufen. Zusätzlich zur Präsentationszeit verfügt jede Nutzlast auch über eine Sendezeit– die Zeit, zu der die Nutzlastdaten den Bucket gemäß der Bitrate verlassen. Die Sendezeit muss vor der Präsentationszeit liegen, um sicherzustellen, dass jede Nutzlast den Bucket vor oder zur Präsentationszeit verlässt, wenn der leckige Bucket fast voll ist. Um dies zu erreichen, werden die Präsentationszeiten durch den *B* / *R-Wert* *(das Preroll)* nach vorn verschoben, und die Sendezeiten erhalten einen Vorsprung, der bei null beginnt. Die Sendezeit darf nicht später als die Präsentationszeit sein, da dies darauf hindeutet, dass die Nutzlast zu spät in den Bucket gelangt ist und nicht in das Datenobjekt aufgenommen werden kann. Der Prerollwert ist im [ASF-Headerobjekt](asf-file-structure.md) enthalten.

Für störungsfreies Streaming über das Netzwerk müssen komprimierte Streams innerhalb des Medieninhalts während der gesamten Wiedergabedauer eine konstante Bitrate beibehalten. Das ASF Leaky Bucket-Modell stellt sicher, dass Mediendaten mit konstanter Bitrate über das Netzwerk gesendet werden. Die Parameter des Buckets "Leaky" werden im Eigenschaftenobjekt des erweiterten Datenstroms des [ASF-Headerobjekts](asf-file-structure.md)angegeben. In Microsoft Media Foundation werden sie als Attribute für den Medientyp festgelegt, der den Stream darstellt.

Die Leaky-Bucketwerte werden sowohl in der ASF-Dateisenke als auch im zugrunde liegenden ASF-Multiplexerobjekt sowie im Windows Media-Encoder definiert. Diese Werte können gleich oder unterschiedlich sein. Betrachten Sie beispielsweise ein Streamingszenario, bei dem die Audiobeispiele später als die Videobeispiele übermittelt werden müssen, damit die Datei ohne Latenz gestreamt werden kann. Um dies zu erreichen, kann der leaky-Bucket des Audiostreams in der Mediensenke auf einen höheren Wert als den im Windows Media-Audioencoder festgelegten Wert festgelegt werden.

Um B/R-Werte im Encoder festzulegen, muss die Anwendung die Eigenschaften [**MFPKEY \_ CODG,**](mfpkey-ravgproperty.md) [**MFPKEY \_ BAVG,**](mfpkey-bavgproperty.md) [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md)und [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md) festlegen. Informationen zum Festlegen von Eigenschaften im Encoder finden Sie unter [Codierungseigenschaften.](configuring-the-encoder.md)

## <a name="the-bucket-in-use"></a>Der verwendete Bucket

Das Ziel eines Encoders besteht darin, sicherzustellen, dass der Inhalt nie über den Puffer überläuft. Der Encoder verwendet die Bitrate und pufferfensterwerte als Handbücher. Die tatsächliche Anzahl von Bits, die über einen beliebigen Zeitraum übergeben werden, der dem Pufferfenster entspricht, darf nie größer als das Doppelte der Puffergröße sein.

Sehen Sie sich das folgende Beispiel an: Sie verfügen über einen 3-Zoll-Bucket mit einem Löcher darin, durch den pro Minute ein 1-Liter-Fluss fließen kann. Sie legen den Bucket unter einen Spigot und öffnen das Ventil, um das Wasser mit einer Rate von 1 Liter pro Minute auszulassen. Das Wasser fließt so schnell wie möglich aus dem Bucket, sodass kein zusätzliches Wasser im Bucket verbleibt. Anschließend erhöhen Sie den Fluss vom Spigot auf zwei Blöcke pro Minute. Jede Minute, in der das Wasser mit dieser Rate fließt, gelangen zwei Kästchen in den Bucket, und 1 Lecks gehen aus, sodass 1 Ausfluss im Bucket verbleibt. Am Ende von 3 Minuten sind 6 Strömen Wasser in den Bucket gelangt, 3 Lecks sind ausgegangen, und der Bucket ist voll.

In der Praxis wird die theoretisch maximale Datenrate über ein Intervall, das dem Pufferfenster entspricht, nie erreicht. Im vorherigen Beispiel wurde eine konstante Datenrate angenommen. Bei demselben Bucket mit drei Blöcken können Sie die Flussrate von den Spigoten für eine Minute auf 6 Mal pro Minute erhöhen und die Vergrößerung dann zwei Minuten lang deaktivieren. Obwohl die Gesamtmenge des Wassers, das in den Bucket aufgenommen wird, innerhalb des theoretischen Höchstwerts für das Pufferfenster liegt, führt die Häufung dieses Betrags in einem Teil des Fensters dazu, dass der Bucket überläuft. Bei 6 Litern pro Minute überläuft der 3-Liter-Bucket kurz nach Ablauf von 30 Sekunden. Daher hängt die tatsächliche maximale Datenmenge, die während eines beliebigen Intervalls, das der Pufferfenstereinstellung entspricht, an den Puffer übermittelt werden kann, von der Größe der einzelnen Stichproben und deren Übermittlung ab.

Bisher wurde in den Beispielen nur der Puffer erläutert, der vom Decoder verwendet wird. Es wird jedoch auch ein leckhafter Bucketpuffer vom Encoder verwendet, der den komprimierten Inhalt erstellt. Der Encoder nimmt alle erforderlichen Anpassungen an den Komprimierungsalgorithmen vor, um die Bitrate der komprimierten Stichproben innerhalb der Grenzen zu halten, die durch die Bitrate und das Pufferfenster beschrieben werden, vorausgesetzt, dass die Stichproben mit konstanter Rate an den Decoder übermittelt werden. Sie können sich den Encoder-Bucket als Spiegelung des Decoder-Buckets vorstellen. Der Encoderbucket wird mit einer variablen Rate gefüllt, die durch die Größe der einzelnen Stichproben bestimmt wird, und leckt mit einer konstanten Rate, die der durchschnittlichen Bitrate entspricht.

Betrachten Sie das folgende Beispiel eines Encoders und Decoders, die über ein Netzwerk miteinander verbunden sind. Sie codieren eine Videodatei mit 30 Frames pro Sekunde mit einer Bitrate von 6.000 Bits pro Sekunde und einem Pufferfenster von 3 Sekunden (eine Gesamtpuffergröße von 18.000 Bits). Das erste Beispiel wird als Keyframe codiert und nimmt 7.000 Bits in Anspruch. Der Encoderpuffer enthält jetzt 7.000 Bits. Die nächsten 29 Frames sind alle Deltaframes mit insgesamt 3.000 Bits. In der ersten Sekunde des Inhalts (30 Frames) würde die Pufferfülle also bei 10.000 Bits liegen, wenn nichts verloren geht. Wir wissen, dass die Bitrate des Streams 6.000 Bits pro Sekunde beträgt. Nachdem die erste Sekunde des codierten Inhalts in den Encoderpuffer gestellt wurde, sinkt die Vollzahl auf 4.000 Bits. In der Decodierungsanwendung wird dieser Stream mit 6.000 Bits pro Sekunde an den Decoderpuffer übermittelt. Nach einer Sekunde enthält der Puffer 6.000 Bits. Das erste Beispiel enthält 7.000 Bits, sodass der Decoderpuffer mehr gefüllt werden muss, bevor der Decoder mit dem Entfernen von Stichproben beginnt.

## <a name="setting-leaky-bucket-values-for-asf-streams"></a>Festlegen von "Leaky Bucket Values" für ASF Streams

In einem Dateicodierungsszenario kann eine Anwendung beim Konfigurieren der Datenströme im [ASF-Profil](asf-profile.md)die werte für den verlustfreien Bucket festlegen.

Nachdem Sie den Stream erstellt haben und einen Verweis auf die [**IMFASFStreamConfig-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) des Streams haben, können Sie die Werte mit den folgenden Attributen festlegen:

-   [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (Durchschnittliche Bucketwerte für Lecks)
-   [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (maximale Bucketwerte für Lecks)

Informationen zum Hinzufügen von Streams und abrufen des **IMFASFStreamConfig-Zeigers** finden Sie unter [Adding Stream Information to the ASF File Sink (Hinzufügen von Streaminformationen zur ASF-Dateisenke).](adding-stream-information-to-the-asf-file-sink.md)

Diese Werte enthalten die folgenden Informationen:

-   Durchschnittliche Bitrate: Abrufen der durchschnittlichen Bitrate aus dem Ausgabemedientyp, der während der Medientypaushandlung ausgewählt wird. Verwenden Sie das [**MF \_ MT AUDIO \_ \_ AVG BYTES PER \_ \_ \_ SECOND-Attribut**](mf-mt-audio-avg-bytes-per-second-attribute.md) (für Audiostreams) oder das [**MF MT \_ \_ AVG \_ BITRATE-Attribut**](mf-mt-avg-bitrate-attribute.md) (für Videostreams).
-   Pufferfenster: Wenn Sie über eine Instanz des Encoders verfügen und Ausgabemedientypen ausgehandelt haben, können Sie diesen Wert später aktualisieren, indem Sie den Encoder für die [**IWMCodecLeakyBucket-Schnittstelle**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) abfragen und dann [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces.h, wmcodecdspuuid.lib) aufrufen. Andernfalls verwenden Sie den Standardwert von 3000 Millisekunden.
-   Anfangspuffergröße: Auf 0 festgelegt.

Die von der Anwendung bereitgestellten Werte hängen vom Typ der Codierung und vom Medientyp des Streams ab. Beispielsweise erfordert [die Codierung konstanter Bitraten](constant-bit-rate-encoding.md) eine vordefinierte feste Bitrate und ein Pufferfenster. Die Anwendung kann diese leaky bucket-Werte angeben, indem sie die [**MFPKEY \_ VIDEOWINDOW-Codierungseigenschaft**](mfpkey-videowindowproperty.md) und das [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1-Attribut**](mf-asfstreamconfig-leakybucket1-attribute.md) im Stream festlegt. Die angegebenen Pufferfensterwerte werden verwendet, um sicherzustellen, dass für die codierte Datei die richtigen Sendezeiten für die Datenpakete markiert sind und der Prerollwert im ASF-Headerobjekt angezeigt wird. Es reicht aus, **MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1** festzulegen, da diese angegebenen Werte in das [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2-Attribut**](mf-asfstreamconfig-leakybucket2-attribute.md) kopiert werden.

Für 2-Pass-Codierungsmodi müssen Sie beide Attribute festlegen, um die Durchschnitts- und Höchstwerte anzugeben.

Bei der VBR-Codierung kann die Anwendung die vom Encoder verwendeten werte für den verlustreichen Bucket erst abfragen, nachdem der Codierungsdurchlauf abgeschlossen ist. Daher kann die Anwendung beim Konfigurieren der Mediensenke festlegen, dass die Attribute oder Eigenschaften im Zusammenhang mit verlustbeschaffenen Buckets nicht festgelegt werden sollen. Nach der Codierung muss die Anwendung den Encoder für die Eigenschaften [**MFPKEY \_ MICG,**](mfpkey-ravgproperty.md) [**MFPKEY \_ BAVG,**](mfpkey-bavgproperty.md) [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md)und [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md) abfragen und in der Mediensenke festlegen, sodass die genauen Werte im Headerobjekt widergespiegelt werden. Ein Codebeispiel zum Aktualisieren der Werte für die VBR-Codierung finden Sie unter "Aktualisieren von Codierungseigenschaften in der Dateisenke" in [Tutorial: 1-Pass Windows Mediencodierung.](tutorial--1-pass-windows-media-encoding.md)

Wenn Sie Windows Medieninhalt ohne Codierung von der Quelle in die Mediensenke kopieren, müssen die Werte für den verlustbeschwerte Bucket in der Mediensenke festgelegt werden.

## <a name="leaky-bucket-values-in-the-asf-multiplexer"></a>Leaky Bucket Values in the ASF Multiplexer

In Media Foundation werden die Werte für die verlustbeschwerte Buckets von [ASF Multiplexer](asf-multiplexer.md) verwendet, um die internen Bucketwerte für Lecks einzurichten, die zum Generieren von Datenpaketen verwendet werden. Die Nutzlast ist in einem Medienbeispiel enthalten, und eine Reihe von Medienbeispielen stellt ein ASF-Datenpaket dar. Basierend auf den wertlosen Buckets und der Präsentationszeit weist der Multiplexer für jedes Medienbeispiel eine Sendezeit zu, sodass die Bitraten der über das Netzwerk gesendeten Pakete mit einer konstanten Bitrate (*R*) erfolgen.

Eine Anwendung kann keine verlustbesendigen Bucketwerte im Multiplexer direkt festlegen. Die Werte müssen in der ASF-Mediensenke bereitgestellt werden, die die entsprechenden Werte für den Multiplexer festlegt. Die in [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) und [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) festgelegten Werte werden vom Multiplexer verwendet, um zu überprüfen, ob die an die ASF-Mediensenke gesendeten Stichproben mit den angegebenen Werten generiert werden.

## <a name="updating-leaky-bucket-values-in-the-asf-media-sink"></a>Aktualisieren von Leaky Bucket-Werten in der ASF-Mediensenke

Eine Anwendung kann die Werte für undichte Buckets auf Streamebene überschreiben (im ASF-Profil während der Streamerstellung festgelegt), indem sie die [**MFPKEY \_ ASFSTREAMSINK \_ CORRECTED \_ LEAKYBUCKET-Eigenschaft**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) im Eigenschaftenspeicher der Mediensenke festlegt. Um einen Verweis auf den Eigenschaftenspeicher abzurufen, verwenden Sie das ContentInfo-Objekt, das von der Mediensenke implementiert wird. Weitere Informationen finden Sie unter [Festlegen von Eigenschaften in der Dateisenke.](setting-properties-in-the-file-sink.md)

**Hinweis**  Dieser Vorgang ist nur für Audiostreams zulässig.

Diese Eigenschaft muss festgelegt werden, nachdem Sie den Ausgabetyp für den Encoder festgelegt haben. Basierend auf der im Medientyp festgelegten Bitrate berechnet der Encoder die Puffergröße, um sicherzustellen, dass die generierten Medienbeispiele nie über den Puffer hinauslaufen. Der Encoder nimmt während der Komprimierung die erforderlichen Anpassungen vor, um die Bitrate der komprimierten Stichproben innerhalb der Grenzen zu halten, die durch die Bitrate und das Pufferfenster beschrieben werden.

Ähnlich wie bei den Streamkonfigurationsattributen für leaky-Buckets legen Sie die durchschnittliche Bitrate und die Puffergröße sowie die anfängliche Pufferfülle in einem Array von DWORDs fest. Weitere Informationen finden Sie im Abschnitt "Setting Leaky Bucket Values for ASF Streams" in diesem Thema.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Unterstützung in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Windows Media-Codecs](windows-media-codecs.md)
</dt> </dl>

 

 
