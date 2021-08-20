---
title: Verwenden von zeitierten Ebenen
description: Verwenden von zeitierten Ebenen
ms.assetid: 4a253521-3036-488a-98bc-62596b538f68
keywords:
- Visualisierungen, Zeitereignisse
- Benutzerdefinierte Visualisierungen, Zeitereignisse
- Visualisierungen, Frequency-Array
- Benutzerdefinierte Visualisierungen, Frequency-Array
- Visualisierungen, Wellenformarray
- Benutzerdefinierte Visualisierungen, Wellenformarray
- Visualisierungen, Zustandsvariable
- Benutzerdefinierte Visualisierungen, Zustandsvariable
- visualisierungen,timeStamp-Variable
- Benutzerdefinierte Visualisierungen, timeStamp-Variable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6ce4d675fa37a519952f1b31d3c52cd93005a82eef977b7bd7d77623f1e508
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116937"
---
# <a name="using-timed-levels"></a>Verwenden von zeitierten Ebenen

Die **TimedLevel-Struktur** besteht aus zwei zweidimensionalen Arrays, einem Zustandswert und einem Zeitstempelwert.

## <a name="frequency-array"></a>Frequency Array

Das frequency-Array ist ein zweidimensionales Array. Die erste Dimension jedes Arrays entspricht dem Stereoaudiokanal (links oder rechts), und die zweite entspricht den Frequenzebenen (in Bytes) der Momentaufnahme, wobei das Audiospektrum in 1024 Bereiche unterteilt ist.

Sie können die vom Windows Media Player bereitgestellten Frequency-Arraydaten wie folgt abrufen:


```C++
TimedLevel *pLevels;
int snapshot = pLevels->frequency[0][0];
```



Der Wert der Momentaufnahme ist für den linken Kanal und enthält den Wert des untersten Teils des Frequenzspektrums. Wenn die Momentaufnahme z. B. einen großen Wert hat, gibt sie an, dass der niedrigste 1024. Teil des Frequenzspektrums eine umfangreiche Häufigkeit aufzuweisen hat. Der Wert 0 (null) gibt an, dass in diesem Teil des Spektrums für den linken Kanal keine Werte mit niedriger Frequenz vorhanden sind. Wenn Sie über ein monophones Signal verfügen, verfügt nur die erste Dimension über gültige Werte.

Wenn das Signal nicht Stereo ist, enthält das zweite Array eine Kopie des Monosignals. Das heißt, frequency \[ 0 \] \[ *n* \] und frequency \[ 1 \] \[ *n* \] enthalten die gleichen Daten, wobei *n* der Index in einer bestimmten Zelle ist.

## <a name="waveform-array"></a>Waveform-Array

Das Wellenformarray ist auch ein zweidimensionales Array. Die erste Dimension des Arrays entspricht dem Kanal (links oder rechts), und die zweite entspricht den Leistungsstufen (in Bytes) der Momentaufnahme, wobei die Audioleistung in 1024 zusammenhängende Zeitsegmente aufgeteilt wird.

Sie können die Wellenformarraydaten wie folgt aus Windows Media Player abrufen:


```C++
TimedLevel *pLevels;
int snapshot = pLevels->waveform[0][0];

```



Der Wert der Momentaufnahme ist für den linken Kanal und enthält den ersten Wert der quantisierten Momentaufnahme der Energiewerte. Wenn eine Momentaufnahme erstellt wird, besteht sie aus 1024 kleinen inkrementellen Messungen der Audioleistung. Der niedrigste Wert des Arrays wird durch die erste inkrementelle Messung der Audioleistung generiert. Beachten Sie, dass die Werte der Potenz von -128 bis +127 gemessen werden, die Werte im Array jedoch zwischen 0 und 255 liegen. Wenn Sie über eine monophone Welle verfügen, hat nur die erste Dimension gültige Werte.

Wenn das Signal nicht Stereo ist, enthält das zweite Array eine Kopie des Monosignals. Das heißt, waveform \[ 0 \] \[ *n* \] und waveform \[ 1 \] \[ *n* \] enthalten die gleichen Daten, wobei *n* der Index in einer bestimmten Zelle ist.

## <a name="state"></a>State

Die Zustandsvariable gibt den Audiowiedergabezustand von Windows Media Player an. Die PlayerState-Enumerationswerte sind


```C++
    stop_state              = 0,    // audio is currently stopped
    pause_state             = 1,    // audio is currently paused
    play_state              = 2     // audio is currently playing

```



Sie können diese Variable verwenden, um abhängig vom Audiowiedergabezustand unterschiedliche Aktionen durchzuführen. Beispielsweise können Sie eine Art von Visualisierung wiedergeben, wenn die Audiowiedergabe erfolgt, und eine andere, wenn sie beendet wird.

## <a name="time-stamp"></a>Zeitstempel

Die Variable timeStamp gibt die aktuelle Zeit an, zu der die Momentaufnahme erstellt wird. Dies kann verwendet werden, um zu messen, wie oft die Momentaufnahmen erstellt werden.

Sie können diese Variable verwenden, um die Animationen zu zeitieren. Wenn die Momentaufnahmen zu häufig sind, können Sie Ihr Bild ordnungsgemäß herabsetzen, damit es auf die von Ihnen gewünschte Weise angezeigt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Rendern**](implementing-render.md)
</dt> </dl>

 

 




