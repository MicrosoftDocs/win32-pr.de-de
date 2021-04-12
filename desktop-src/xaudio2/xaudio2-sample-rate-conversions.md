---
description: XAudio2 Voices können automatische Samplingrate-Konvertierungen durchführen, wenn die Eingabe Stichproben Rate von der Eingabe Stichproben Rate ihrer Ausgabe Stimmen abweicht.
ms.assetid: be34ce62-6552-45e2-a247-830ab55ea9ec
title: XAudio2 Sample-Raten Konvertierungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d437a45f9e896826bedc1418382fb257201722d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218552"
---
# <a name="xaudio2-sample-rate-conversions"></a>XAudio2 Sample-Raten Konvertierungen

XAudio2 Voices können automatische Samplingrate-Konvertierungen durchführen, wenn die Eingabe Stichproben Rate von der Eingabe Stichproben Rate ihrer Ausgabe Stimmen abweicht.

Für Abtastraten Konvertierungen gelten folgende Regeln:

-   Die Stichprobenrate für die Spracheingabe ist korrigiert.

    Stimmen können nur die Eingabe Stichproben Rate verarbeiten, die bei der Erstellung angegeben wurde. Bei der [**Bewältigung von Stimmen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) und [**Teil Mischungen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)wird die Eingabe Stichproben Rate mit dem *inputsamplerate* [**-Argument**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice) für die [**IXAudio2::::**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) Bei Quell stimmen wird die Eingabe Stichproben Rate der Stimme durch das psourceformat-Argument der [**IXAudio2:: | atesourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) -Funktion angegeben.

-   Alle Ausgabe Stimmen einer Stimme müssen die gleiche Eingabe Stichproben Rate aufweisen.

    Stimmen können von Ihrer Eingabe Stichproben Rate in eine beliebige Ausgabe Samplingrate konvertieren, aber alle Ausgabe Stimmen der Stimme müssen die gleiche Eingabe Stichproben Rate aufweisen. Beispielsweise könnte eine Stimme an eine beliebige Anzahl von Stimmen mit einer Eingabe Stichproben Rate von 22 kHz ausgegeben werden. Wenn dieselbe Stimme jedoch mehrere Ausgabe Stimmen enthielt, die jeweils eine andere Eingabe Stichprobe aufweisen, wäre das audiodiagramm nicht gültig.

-   Die Verarbeitung von Samplingrate erfolgt nur bei Bedarf.

    Das Umrechnen von Audiodaten in eine andere Stichprobenrate führt zu einem höheren Verarbeitungsaufwand, der besser zu vermeiden ist. Wenn die Eingabe Stichproben Rate einer Stimme mit der Eingabe Stichproben Rate der Ausgabe Stimmen übereinstimmt, wird diese Konvertierung nicht durchgeführt, und die Verarbeitungszeit wird verkürzt.

-   Die Ausgabe Stichproben Rate kann sich über die Lebensdauer einer Stimme unterscheiden.

    Die Ausgabe Stichproben Rate einer Stimme ist nicht korrigiert. Solange alle Ausgabe Stimmen die gleiche Eingabe Stichproben Rate aufweisen, ist das audiodiagramm gültig. Wenn eine Stimme so geändert wird, dass Sie in neue stimmen mit einer anderen Eingabe Stichproben Rate ausgegeben wird, konvertiert die Stimme in die Eingabe Stichproben Rate der neuen Stimmen.

Es gibt einige Szenarien, in denen es erforderlich ist, eine unter Mischungs Stimme hinzuzufügen, um eine Stichproben Raten Konvertierung zwischen Stimmen auszuführen. Wenn eine Stimme mit verschiedenen Eingabe Stichproben Raten in Stimmen ausgeben muss, kann nur eine der Stimmen eine direkte Ausgabe der ursprünglichen Stimme sein. Da alle Ausgabe Stimmen der Stimme die gleiche Eingabe Stichproben Rate aufweisen müssen, erhalten die anderen Stimmen indirekt eine Ausgabe. Es muss eine teilmix-Stimme mit der richtigen Eingabe Stichproben Rate vorhanden sein, die zwischen der ursprünglichen Stimme und der beabsichtigten Ausgabesprache liegt.

Angenommen, eine Quell Stimme mit einer Eingabe Stichproben Rate von 22 kHz muss in eine teilmischungs Sprache mit einer Eingabe Stichproben Rate von 11 kHz und eine Stimme mit einer Eingabe Stichproben Rate von 44,1 kHz ausgegeben werden. Da die beiden Ausgabe Stimmen unterschiedliche Eingabe Stichproben Raten aufweisen, müssen Sie mehr Teil Mischungs Stimmen zwischen der ursprünglichen Stimme und den vorgesehenen Ausgabe Stimmen einfügen. Um die Genauigkeit der Quell Stimme beizubehalten und unnötige, aufwändige Konvertierungen in höhere Stichproben Raten zu vermeiden, müssen Sie zwei Teil Mischungs stimmen mit 22 kHz-Stichproben Eingabe Raten in das Diagramm einfügen. Eine teilmischungs Stimme würde bei einer Teil Mischungs Stimme mit dem eingabeeffekt bei 11 kHz ausgegeben werden, und die andere unter Mischungs Sprache würde bei 44,1 kHz an die Stimme der Stimme ausgeben.

## <a name="examples-of-sample-rate-conversion-in-audio-graphs"></a>Beispiele für die Stichproben Raten Konvertierung in audiodiagrammen

Alle Stimmen haben dieselbe Stichproben Eingabe Rate. im audiodiagramm wird keine Stichproben Raten Konvertierung durchgeführt.![im audiodiagramm wird keine Stichproben Raten Konvertierung durchgeführt.](images/xaudio2-sample-rate-conversions-1.png)

Alle Stimmen haben dieselbe Stichproben Eingabe Rate außer der Stimme der Stimme. die Stichproben Raten Konvertierung erfolgt nur bei Daten, die an die Stimme der Stimme erfolgen. ![die Stichproben Raten Konvertierung erfolgt nur bei Daten, die an die Stimme der Stimme erfolgen.](images/xaudio2-sample-rate-conversions-2.png)

Stimmen haben unterschiedliche Stichproben Eingabe Raten und erfordern mehr teilmischungs Stimmen, um Stichproben Raten Konvertierungen auszuführen. die Stichproben Raten Konvertierung erfolgt an mehreren Stellen im audiodiagramm. ![die Stichproben Raten Konvertierung erfolgt an mehreren Stellen im audiodiagramm.](images/xaudio2-sample-rate-conversions-3.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Stimmen](voices.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> </dl>

 

 
