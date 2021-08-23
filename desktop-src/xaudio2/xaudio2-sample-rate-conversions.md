---
description: XAudio2-Stimmen können automatische Stichprobenratenkonvertierungen durchführen, wenn sich ihre Eingabestichprobenrate von der Eingabestichprobenrate ihrer Ausgabestimmen unterscheiden.
ms.assetid: be34ce62-6552-45e2-a247-830ab55ea9ec
title: XAudio2 Sample Rate Conversions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af82983d1d9307551e516f1b8b60676b4b250450da65f416c340446c5a906f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962523"
---
# <a name="xaudio2-sample-rate-conversions"></a>XAudio2 Sample Rate Conversions

XAudio2-Stimmen können automatische Stichprobenratenkonvertierungen durchführen, wenn sich ihre Eingabestichprobenrate von der Eingabestichprobenrate ihrer Ausgabestimmen unterscheiden.

Beispielratenkonvertierungen folgen den folgenden Regeln:

-   Die Abtastrate der Spracheingabe ist fest.

    Stimmen können nur die Eingabestichprobenrate verarbeiten, die beim Erstellen angegeben wurde. Für [**die Masteringstimmen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) und Untermischungsstimmen wird die Eingabestichprobenrate mit dem *InputSampleRate-Argument* für die [**Funktionen IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) und [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice) angegeben. [](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) Bei Quellstimmen wird die Eingabestichprobenrate der Stimme durch das pSourceFormat-Argument für die [**IXAudio2::CreateSourceVoice-Funktion**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) angegeben.

-   Alle Ausgabestimmen einer Stimme müssen die gleiche Eingabestichprobenrate haben.

    Stimmen können von ihrer Eingabestichprobenrate in eine beliebige Ausgabestichprobenrate konvertiert werden, aber alle Ausgabestimmen der Stimme müssen die gleiche Eingabestichprobenrate haben. Beispielsweise könnte eine Stimme mit einer Eingabestichprobenrate von 22 kHz an eine beliebige Anzahl von Stimmen ausgegeben werden. Wenn dieselbe Stimme jedoch mehrere Ausgabestimmen hätte, von denen jede eine andere Eingabestichprobenrate auftraten, wäre das Audiodiagramm ungültig.

-   Die Konvertierung der Stichprobenrate erfolgt nur bei Bedarf.

    Das Konvertieren von Audiodaten in eine andere Abtastrate verursacht mehr Verarbeitungsaufwand, was zu vermeiden ist. Wenn die Eingabestichprobenrate einer Stimme mit der Eingabestichprobenrate ihrer Ausgabestimmen entspricht, erfolgt diese Konvertierung nicht, und die Verarbeitungszeit wird verkürzt.

-   Die Ausgabestichprobenrate kann im Laufe der Lebensdauer einer Stimme variieren.

    Die Ausgabestichprobenrate einer Stimme ist nicht festgelegt. Solange alle Ausgabestimmen die gleiche Eingabestichprobenrate haben, ist das Audiodiagramm gültig. Wenn eine Stimme so geändert wird, dass sie an neue Stimmen mit einer anderen Eingabestichprobenrate ausgegeben wird, wird die Stimme in die Eingabestichprobenrate der neuen Stimmen konvertiert.

Es gibt einige Szenarien, in denen es erforderlich ist, eine Untermischungsstimme hinzuzufügen, um eine Konvertierung der Stichprobenrate zwischen Stimmen durchzuführen. Wenn eine Stimme an Stimmen mit verschiedenen Eingabestichprobenraten ausgegeben werden muss, kann nur eine der Stimmen eine direkte Ausgabe der ursprünglichen Stimme sein. Da alle Ausgabestimmen einer Stimme die gleiche Eingabestichprobenrate haben müssen, erhalten die anderen Stimmen indirekt eine Ausgabe. Es muss eine Untermischung der Stimme mit der richtigen Eingabestichprobenrate zwischen der ursprünglichen Stimme und der beabsichtigten Ausgabestimme geben.

Betrachten Sie beispielsweise eine Quellstimme mit einer Eingabestichprobenrate von 22 kHz, die an eine Untermischungsstimme mit einer Eingabestichprobenrate von 11 kHz und einer Masterstimme mit einer Eingabestichprobenrate von 44,1 kHz ausgegeben werden muss. Da die beiden Ausgabestimmen unterschiedliche Eingabestichprobenraten haben, müssen Sie mehr Untermischungsstimmen zwischen der ursprünglichen Stimme und den beabsichtigten Ausgabestimmen einfügen. Um die Genauigkeit der Quellstimme zu erhalten und unnötige teure Konvertierungen in höhere Stichprobenraten zu vermeiden, müssen Sie zwei Untermischungsstimmen mit 22-kHz-Beispieleingaberaten in das Diagramm einfügen. Eine Untermischungsstimme würde mit 11 kHz an die Untermischungsstimme mit dem Halleffekt ausgegeben, und die andere Untermischungsstimme würde mit 44,1 kHz an die Masterstimme ausgegeben.

## <a name="examples-of-sample-rate-conversion-in-audio-graphs"></a>Beispiele für die Konvertierung der Abtastrate in Audiographen

Alle Stimmen haben die gleiche Stichprobeneingaberate. Im Audiodiagramm wird keine Konvertierung der Abtastrate durchgeführt.![Im Audiodiagramm wird keine Konvertierung der Abtastrate durchgeführt.](images/xaudio2-sample-rate-conversions-1.png)

Alle Stimmen haben die gleiche Stichprobeneingaberate außer der Masterstimme. Die Konvertierung der Stichprobenrate erfolgt nur für Daten, die an die Masterstimme gehen. ![Die Konvertierung der Stichprobenrate erfolgt nur für Daten, die an die Masterstimme gehen.](images/xaudio2-sample-rate-conversions-2.png)

Stimmen haben unterschiedliche Stichprobeneingaberaten und erfordern mehr Untermischungsstimmen, um Konvertierungen der Stichprobenrate durchzuführen. Die Konvertierung der Abtastrate wird an mehreren Stellen im Audiographen durchgeführt. ![Die Konvertierung der Abtastrate wird an mehreren Stellen im Audiographen durchgeführt.](images/xaudio2-sample-rate-conversions-3.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Stimmen](voices.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> </dl>

 

 
