---
description: Codierungsmethoden
ms.assetid: 17ab5ecc-0173-4c5c-9d65-40e506ab7e07
title: Codierungsmethoden (Microsoft Media Foundation)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa11e9545aa38358e5e1c0fdb4dfc4b7a2c3ee13f24b0fa38fe76b9e8bddcc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974529"
---
# <a name="encoding-methods-microsoft-media-foundation"></a>Codierungsmethoden (Microsoft Media Foundation)

Die meisten Windows Medienaudio- und Videocodecs unterstützen mehrere Codierungsmethoden. Wenn Sie wissen, wie und wann sie verwendet werden sollten, können Sie qualitativ hochwertige komprimierte Inhalte erstellen.

Die Codierungsmethoden konzentrieren sich alle auf den Puffer, der vom Decoder zum Verwalten komprimierter Eingabedaten verwendet wird. Dieser Puffer wird durch die Bitrate des Streams in Bits pro Sekunde und das Pufferfenster in Millisekunden definiert. Bei der Codierung hält sich der Codec an die Einschränkungen des Puffers. Weitere Informationen zum Puffer finden Sie unter [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).

## <a name="constant-bit-rate-encoding"></a>Codierung konstanter Bitraten

Die Bitrate für alle Datenströme, die von einem der Windows Medienaudio- und Videocodecs codiert werden, ist nicht konstant. Die Codierung der konstanten Bitrate (CONSTANT Bit Rate, CBR) ist daher ein etwas irreführender Begriff. Das Unterscheidungsmerkmal eines CBR-codierten Streams ist ein kleines Pufferfenster, das die Variation der Stichprobengrößen einschränkt. Die CBR-Codierung wird hauptsächlich für Inhalte verwendet, die über ein Netzwerk an das Ziel gestreamt werden. In einem solchen Szenario ist es wichtig, sich auf eine konsistente Bandbreitennutzung verlassen zu können.

Aus Konfigurationssicht unterscheidet sich die CBR-Codierung von den anderen Modi darin, dass Sie vor beginn der Codierung sowohl die durchschnittliche Bitrate des Ausgabeinhalts als auch das Pufferfenster festlegen, das für diese Bitrate gilt. In anderen Modi ist einer oder beide dieser Werte unbekannt, wenn Sie den Encoder konfigurieren, und wird vom Codec berechnet, während er codiert wird. CBR ist der Standardcodierungsmodus, der von den Windows Media Encoder-DMOs verwendet wird.

## <a name="two-pass-constant-bit-rate-encoding"></a>Two-Pass Codierung konstanter Bitraten

Cbr Standard verwendet nur einen einzigen Codierungsdurchlauf. Sie geben Ihre Inhalte als Eingabebeispiele an, und der Codec komprimiert den Inhalt und gibt Ausgabebeispiele zurück. Es ist auch möglich, Eingabebeispiele zweimal zu verarbeiten. Beim ersten Durchlauf führt der Codec Berechnungen durch, um die Codierung für Ihren Inhalt zu optimieren. Beim zweiten Durchlauf verwendet der Codec die während des ersten Durchlaufs gesammelten Daten, um den Inhalt zu codieren.

Die CBR-Codierung mit zwei Durchlauf hat viele Vorteile. Dies führt häufig zu erheblichen Qualitätssteigerungen gegenüber der STANDARDMÄßIGEN CBR-Codierung, ohne die Pufferanforderungen zu ändern. Dadurch eignet sich dieser Codierungsmodus ideal für Inhalte, die über ein Netzwerk gestreamt werden. Die einzige Situation, in der die zweistufige CBR nicht möglich ist, ist, wenn Sie Inhalte aus einer Livequelle codieren und keinen zweiten Durchlauf verwenden können.

Der Ausgabemedientyp eines ZWEI-Pass-CBR-Streams ist identisch mit dem eines CBR-Standarddatenstroms. Sie geben weiterhin die zu verwendende Bitrate und das Pufferfenster an. Beim Konfigurieren der DMO müssen Sie festlegen, dass zwei Durchläufe ausgeführt werden. Außerdem müssen Sie die DMO benachrichtigen, wenn Sie mit dem Senden von Beispielen für den ersten Durchlauf fertig sind.

## <a name="quality-based-variable-bit-rate-encoding"></a>Quality-Based Codierung variabler Bitraten

Da die CBR-Codierung keine konstante Bitrate aufrechterhält, erscheint die Unterscheidung zwischen ihr und der Codierung variabler Bitraten (VBR) möglicherweise etwas verzeilt. Der Hauptunterschied zwischen CBR und VBR ist die Größe des verwendeten Pufferfensters. VBR-codierte Streams weisen im Vergleich zu CBR-codierten Streams in der Regel große Pufferfenster auf. Qualitätsbasierte VBR ist keine Ausnahme, da Sie dafür weder Bitrate noch Pufferfenster definieren. Stattdessen legen Sie einen Qualitätswert fest. Der Codec versucht dann, die Daten so zu komprimieren, dass die Qualität der codierten Medien während der gesamten Dauer konsistent ist, unabhängig von den Pufferanforderungen des resultierenden Streams.

Qualitätsbasierte VBR verwendet einen einzelnen Codierungsdurchlauf und erstellt tendenziell große komprimierte Streams. Nach Abschluss der Codierung legt der Codec die Pufferanforderungen fest, damit der Decoder die Daten dekomprimieren kann. Der codierte VBR-Stream eignet sich nicht für das Streaming über ein Netzwerk. Daher sollte qualitätsbasierte VBR nur für lokale Wiedergabeszenarien (oder herunterladen und wiedergeben) verwendet werden.

## <a name="unconstrained-variable-bit-rate-encoding"></a>Codierung der uneingeschränkten Variablenbitrate

Im Gegensatz zur qualitätsbasierten VBR codiert die uneingeschränkte VBR nicht mit einer bestimmten Qualitätsstufe. Stattdessen wird der Inhalt in die höchstmögliche Qualität codiert, während eine angegebene Bitrate beibehalten wird. Die nicht eingeschränkte VBR verwendet zwei Codierungsdurchläufe und ähnelt der CBR mit zwei Durchläufen, mit der Ausnahme, dass Sie keine Pufferfenstereinstellung für den Stream angeben. Dies bedeutet, dass es keine Beschränkung für die Größe einzelner Stichproben im Stream gibt, solange die durchschnittliche Bitrate kleiner oder gleich dem von Ihnen festgelegten Wert ist.

Die nicht eingeschränkte VBR ist nur von begrenztem Nutzen, da es nur wenige Wiedergabeszenarien gibt, die Anforderungen haben, die den Pufferanforderungen entsprechen. Der Codec kann das Pufferfenster auf den wert festlegen, der nach der Codierung erforderlich ist, sodass Sie keine Kontrolle über die Puffergröße haben. In den meisten Fällen sollten Sie qualitätsbasierte VBR verwenden, wenn Sie sich keine Gedanken über die Größe des Puffers oder die Konsistenz der Bandbreitennutzung machen.

## <a name="peak-constrained-variable-bit-rate-encoding"></a>Peak-Constrained Codierung variabler Bitraten

Der endgültige Codierungsmodus ist vbr mit maximaler Auslastung. Wie bei einer uneingeschränkten VBR verwendet dieser Modus zwei Codierungsdurchläufe und Codieren in eine angegebene Bitrate. Bei vbr-Spitzengrenzwerten konfigurieren Sie jedoch auch den Spitzenwert für die Codierung. Spitzenwerte ähneln normalen Pufferkonfigurationswerten: Es gibt eine Spitzenbitrate und ein Spitzenpufferfenster. Die Datei wird so codiert, dass sie einem Puffer entspricht, der durch die Spitzenwerte beschrieben wird, mit der Bedingung, dass die durchschnittliche Gesamtbitrate des Streams mindestens dem von Ihnen angegebenen durchschnittlichen Bitratenwert entspricht.

Eine eingeschränkte VBR kann schwierig zu konzeptualisieren sein. Hier ist die einfachste Möglichkeit, sich das verwendete Puffermodell zu vorstellen. Angenommen, der Stream ist ein CBR-Datenstrom mit der Spitzenbitrate und dem Spitzenpufferfenster, die zum Definieren des Puffers verwendet werden. In der Regel ist die Spitzenbitrate recht hoch. Der Encoder stellt sicher, dass der erwartete durchschnittliche Bitratenwert, den Sie angeben, während der Dauer des Streams beibehalten wird. An einem bestimmten Punkt im Stream ist die durchschnittliche Bitrate garantiert größer als die Gesamtdatenstromgröße in Bits geteilt durch die Streamdauer in Sekunden).

Betrachten Sie das folgende Beispiel: Sie konfigurieren einen Datenstrom mit einer durchschnittlichen Bitrate von 16.000 Bits pro Sekunde, einer Spitzenbitrate von 48.000 Bits pro Sekunde und einem Spitzenpufferfenster von 3.000 (3 Sekunden). Die Größe des für den Stream verwendeten Puffers beträgt 144.000 Bits (48.000 Bits pro Sekunde x 3 Sekunden), die durch die Spitzenwerte bestimmt werden. Der Encoder komprimiert die Daten so, dass sie diesem Puffer entsprechen. Darüber hinaus muss die durchschnittliche Bitrate des Streams 16.000 oder weniger betragen. Wenn der Encoder einige sehr große Stichproben erstellen muss, um ein komplexes Inhaltssegment zu verarbeiten, kann er die große Puffergröße nutzen. Andere Teile des Streams müssen jedoch mit einer niedrigeren Bitrate codiert werden, um den Durchschnitt auf die angegebene Ebene zu senken.

Die VBR-Codierung mit maximaler Einschränkung eignet sich für Wiedergabegeräte mit begrenzter Pufferkapazität und einigen Datenrateneinschränkungen. Ein häufiges Beispiel hierfür ist die für DVDs verwendete Codierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der VBR-Codierung](usingvbrencoding.md)
</dt> <dt>

[Windows Media-Codecs](windows-media-codecs.md)
</dt> </dl>

 

 



