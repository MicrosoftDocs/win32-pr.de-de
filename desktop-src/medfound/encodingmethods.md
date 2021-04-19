---
description: Codierungs Methoden
ms.assetid: 17ab5ecc-0173-4c5c-9d65-40e506ab7e07
title: Codierungs Methoden (Microsoft Media Foundation)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4366f11ea9d120d638c5600f84fc16f6c5320f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342621"
---
# <a name="encoding-methods-microsoft-media-foundation"></a>Codierungs Methoden (Microsoft Media Foundation)

Die meisten Windows Media Audio-und Video Codecs unterstützen mehrere Codierungs Methoden. Wenn Sie wissen, wie und wann die einzelnen Methoden verwendet werden sollen, können Sie hochwertige komprimierte Inhalte erstellen.

Die Codierungs Methoden konzentrieren sich alle auf den Puffer, der vom Decoder verwendet wird, um komprimierte Eingabedaten zu verwalten. Dieser Puffer wird durch die Bitrate des Streams in Bits pro Sekunde und das Puffer Fenster in Millisekunden definiert. Beim Codieren hält der Codec die Beschränkungen des Puffers an. Weitere Informationen zum Puffer finden Sie unter unkomplizierter [Bucket-Puffer Modell](the-leaky-bucket-buffer-model.md).

## <a name="constant-bit-rate-encoding"></a>Konstante Bitrate-Codierung

Die Bitrate für jeden Stream, der von einem der Windows Media Audio-und Video Codecs codiert wurde, ist nicht konstant. Die Codierung der konstanten Bitrate (CBR) ist daher ein etwas irreführender Begriff. Das Unterscheidungsmerkmal eines CBR-codierten Streams ist ein kleines Puffer Fenster, das die Variation der Stichprobengröße einschränkt. Die CBR-Codierung wird primär für Inhalte verwendet, die über ein Netzwerk an das zugehörige Ziel gestreamt werden. In einem solchen Szenario ist es wichtig, dass Sie sich auf eine konsistente Bandbreitennutzung verlassen können.

Aus Sicht der Konfiguration unterscheidet sich die CBR-Codierung von den anderen Modi darin, dass Sie vor dem Codieren sowohl die durchschnittliche Bitrate des Ausgabe Inhalts als auch das Puffer Fenster festlegen, das für diese Bitrate gilt. In anderen Modi ist einer oder beide dieser Werte beim Konfigurieren des Encoders unbekannt und wird durch den Codec berechnet, während er codiert. CBR ist der Standard Codierungs Modus, der von den Windows Media Encoder-DMOS verwendet wird.

## <a name="two-pass-constant-bit-rate-encoding"></a>Two-Pass Konstante Bitrate-Codierung

Standard-CBR verwendet nur einen einzigen Codierungs Durchlauf. Sie geben ihren Inhalt als Eingabe Beispiele an, und der Codec komprimiert den Inhalt und gibt Ausgabe Beispiele zurück. Es ist auch möglich, Eingabe Beispiele zweimal zu verarbeiten. Beim ersten Durchlauf führt der Codec Berechnungen durch, um die Codierung für Ihre Inhalte zu optimieren. Beim zweiten Durchlauf verwendet der Codec die während der ersten Übergabe gesammelten Daten, um den Inhalt zu codieren.

Die zweistufige CBR-Codierung hat viele Vorteile. Dies führt häufig zu signifikanten Qualitätsvorteilen gegenüber der Standard-CBR-Codierung, ohne dass die Puffer Anforderungen geändert werden. Dadurch ist dieser Codierungs Modus ideal für Inhalte, die über ein Netzwerk gestreamt werden. Die einzige Situation, in der zwei-Pass-CBR nicht möglich ist, ist, wenn Sie Inhalt aus einer Live Quelle codieren und keinen zweiten Durchlauf verwenden können.

Der Ausgabe Medientyp eines CBR-Datenstroms mit zwei Pass ist mit dem eines standardmäßigen CBR-Streams identisch. Sie geben weiterhin die zu verwendende Bitrate und das Puffer Fenster an. Beim Konfigurieren des DMO müssen Sie zwei Durchgänge ausführen. Und Sie müssen den DMO Benachrichtigen, wenn Sie das Senden von Beispielen für den ersten Durchlauf abgeschlossen haben.

## <a name="quality-based-variable-bit-rate-encoding"></a>Quality-Based Variablen-Bitrate-Codierung

Da die CBR-Codierung nicht tatsächlich eine Konstante Bitrate beibehält, kann der Unterschied zwischen der IT und der variablenbitrate-Codierung (VBR) etwas Hazy erscheinen. Der primäre Unterschied zwischen CBR und VBR ist die Größe des verwendeten Puffer Fensters. VBR-codierte Streams verfügen in der Regel über große Puffer Fenster im Vergleich zu CBR-codierten Streams. Bei der Qualitäts basierten VBR handelt es sich nicht um eine Ausnahme, da Sie weder eine Bitrate noch ein Puffer Fenster dafür definieren. Stattdessen legen Sie einen Qualitäts Wert fest. Der Codec versucht dann, die Daten zu komprimieren, sodass die Qualität der codierten Medien während der gesamten Dauer konsistent ist, unabhängig von den Puffer Anforderungen des resultierenden Streams.

Quality-based VBR verwendet einen einzelnen Codierungs Durchlauf und erstellt tendenziell große komprimierte Datenströme. Nach Abschluss der Codierung legt der Codec die Puffer Anforderungen fest, damit der Decoder die Daten dekomprimieren kann. Der codierte VBR-Datenstrom eignet sich nicht für das Streaming über ein Netzwerk. Daher sollte der Qualitäts basierte VBR nur für lokale Wiedergabe Szenarien (oder herunterladen und wiedergeben) verwendet werden.

## <a name="unconstrained-variable-bit-rate-encoding"></a>Unbeschränkte Variablen Bitrate-Codierung

Anders als bei der Qualitäts basierten VBR wird der uneingeschränkte VBR nicht in eine bestimmte Qualitätsstufe codiert. Stattdessen wird der Inhalt in die höchste mögliche Qualität codiert, während eine angegebene Bitrate beibehalten wird. Der uneingeschränkte VBR verwendet zwei Codierungs Durchgänge und ähnelt zwei-Pass-CBR, mit dem Unterschied, dass Sie keine Puffer Fenster Einstellung für den Stream angeben. Dies bedeutet, dass es keine Beschränkung auf die Größe der einzelnen Stichproben im Stream gibt, solange die durchschnittliche Bitrate kleiner oder gleich dem Wert ist, den Sie festgelegt haben.

Der uneingeschränkte Gebrauch von VBR ist eingeschränkt, da es nur wenige Wiedergabe Szenarios gibt, bei denen die Anforderungen an die Puffer Anforderungen bestehen. Der Codec kann das Puffer Fenster auf einen beliebigen Wert festlegen, der nach der Codierung erforderlich ist, sodass Sie keine Kontrolle über die Puffergröße haben. In den meisten Fällen sollten Sie, wenn Sie sich keine Gedanken über die Größe des Puffers oder die Konsistenz der Bandbreitennutzung machen, ein Qualitäts basiertes VBR verwenden.

## <a name="peak-constrained-variable-bit-rate-encoding"></a>Peak-Constrained Variablen-Bitrate-Codierung

Der endgültige Codierungs Modus ist VBR mit hoher Einschränkung. Wie bei nicht eingeschränkten VBR werden in diesem Modus zwei Codierungs Überläufen verwendet und in eine angegebene Bitrate codiert. Bei einem eingeschränkten VBR mit hoher Auslastung konfigurieren Sie jedoch auch den Höchstwert für die Codierung. Spitzenwerte ähneln den normalen Puffer Konfigurations Werten: Es gibt eine Spitzen Bitrate und ein Spitzen Puffer Fenster. Die Datei wird so codiert, dass Sie einem Puffer entspricht, der durch die Spitzenwerte beschrieben wird. die Bedingung ist, dass die durchschnittliche Bitrate des Streams kleiner oder kleiner als der Wert für die durchschnittliche Bitrate ist, den Sie angeben.

Eingeschränkte VBR können schwierig zu konzipieren sein. Dies ist die einfachste Möglichkeit, sich das verwendete Puffer Modell vorzustellen. Angenommen, der Stream ist ein CBR-Datenstrom mit der Spitzen Bitrate und dem Spitzen Puffer Fenster, das zum Definieren des Puffers verwendet wird. In der Regel ist die Spitzen Bitrate sehr hoch. Der Encoder stellt sicher, dass der erwartete Wert für die durchschnittliche Bitrate, den Sie angeben, während der Dauer des Streams beibehalten wird. An einem bestimmten Punkt im Stream ist die durchschnittliche Bitrate garantiert größer als die gesamte Streamgröße in Bits dividiert durch die Dauer des Datenstroms in Sekunden.

Sehen Sie sich das folgende Beispiel an: Sie konfigurieren einen Stream mit einer durchschnittlichen Bitrate von 16.000 Bits pro Sekunde, einer Spitzen Bitrate von 48.000 Bits pro Sekunde und einem Spitzen Puffer Fenster von 3.000 (3 Sekunden). Die Größe des für den Stream verwendeten Puffers beträgt 144.000 Bits (48.000 Bits pro Sekunde x 3 Sekunden), wie von den Spitzenwerten festgelegt. Der Encoder komprimiert die Daten, damit Sie diesem Puffer entsprechen. Außerdem muss die durchschnittliche Bitrate des Streams 16.000 oder weniger betragen. Wenn der Encoder einige sehr große Beispiele zum Verarbeiten komplexer Inhalts Segmente erstellen muss, kann er die große Puffergröße nutzen. Andere Teile des Streams müssen jedoch mit einer niedrigeren Bitrate codiert werden, um den Durchschnitt auf die angegebene Ebene zu verringern.

Die mit Spitzen Beschränkung beschränkte VBR-Codierung ist nützlich für die Wiedergabe von Geräten mit einer begrenzten Pufferkapazität und einigen Datenraten Einschränkungen. Ein gängiges Beispiel hierfür ist die Codierung, die für DVDs verwendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der VBR-Codierung](usingvbrencoding.md)
</dt> <dt>

[Windows Media-Codecs](windows-media-codecs.md)
</dt> </dl>

 

 



