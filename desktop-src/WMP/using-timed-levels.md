---
title: Verwenden von zeitgesteuerten Ebenen
description: Verwenden von zeitgesteuerten Ebenen
ms.assetid: 4a253521-3036-488a-98bc-62596b538f68
keywords:
- Visualisierungen, zeitgesteuerte Ereignisse
- benutzerdefinierte Visualisierungen, zeitgesteuerte Ereignisse
- Visualisierungen, Häufigkeits Array
- benutzerdefinierte Visualisierungen, Häufigkeits Array
- Visualisierungen, Wellenform Array
- benutzerdefinierte Visualisierungen, Wellenform Array
- Visualisierungen, Zustands Variable
- benutzerdefinierte Visualisierungen, Zustands Variable
- Visualisierungen, timestamp-Variable
- benutzerdefinierte Visualisierungen, timestamp-Variable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2d9a23818d57305b3b205ea2e17b6dda2884e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036987"
---
# <a name="using-timed-levels"></a>Verwenden von zeitgesteuerten Ebenen

Die **timedlevel** -Struktur besteht aus 2 2-dimensionalen Arrays, einem Zustandswert und einem Zeitstempelwert.

## <a name="frequency-array"></a>Frequency-Array

Das Frequency-Array ist ein zweidimensionales Array. Die erste Dimension jedes Arrays entspricht dem Stereo Audiokanal (links oder rechts), und der zweite entspricht den Frequenz Ebenen (in Bytes) der Momentaufnahme, in der das Audiospektrum in 1024 Regionen aufgeteilt ist.

Die vom Windows-Media Player bereitgestellten Häufigkeits Array Daten können wie folgt angezeigt werden:


```C++
TimedLevel *pLevels;
int snapshot = pLevels->frequency[0][0];
```



Der Wert von Snapshot ist für den linken Kanal und enthält den Wert des untersten Teils des Häufigkeits Spektrums. Wenn die Momentaufnahme beispielsweise einen großen Wert aufweist, gibt Sie an, dass der niedrigste 1024-Teil des Häufigkeits Spektrums sehr umfangreich ist. Der Wert 0 (null) gibt an, dass in diesem Teil des Spektrums für den linken Kanal keine niedrigen Häufigkeits Werte vorhanden sind. Wenn Sie über ein Monophonic-Signal verfügen, hat nur die erste Dimension gültige Werte.

Wenn das Signal nicht Stereo ist, enthält das zweite Array eine Kopie des Mono-Signals. Das heißt, \[ die Häufigkeit 0 \] \[ *n* \] und \[ die Häufigkeit 1 \] \[ *n* \] enthalten die gleichen Daten, wobei *n* der Index in einer bestimmten Zelle ist.

## <a name="waveform-array"></a>Waveform-Array

Das Wellenform-Array ist auch ein zweidimensionales Array. Die erste Dimension des Arrays entspricht dem Kanal (links oder rechts), und der zweite entspricht den Leistungsebenen (in Bytes) der Momentaufnahme, in der die audiopotenz in 1024 aufeinander folgende Zeit Segmente aufgeteilt wird.

Sie können die Wellenform-Array Daten von Windows Media Player auf folgende Weise erhalten:


```C++
TimedLevel *pLevels;
int snapshot = pLevels->waveform[0][0];

```



Der Wert von Snapshot ist für den linken Kanal und enthält den ersten Wert der quantifizierten Momentaufnahme der Stromwerte. Wenn eine Momentaufnahme erstellt wird, besteht aus 1024 winzigen inkrementellen Messungen der audiopotenz. Der niedrigste Wert des Arrays wird durch das erste inkrementelle Maß an audiopotenz generiert. Beachten Sie, dass die Werte der Potenz von-128 bis + 127 gemessen werden, die Werte im Array jedoch zwischen 0 und 255 liegen. Wenn Sie über eine Mono-Welle verfügen, hat nur die erste Dimension gültige Werte.

Wenn das Signal nicht Stereo ist, enthält das zweite Array eine Kopie des Mono-Signals. Das heißt, Wellenform \[ 0 \] \[ *n* \] und Wellenform \[ 1 \] \[ *n* \] enthalten dieselben Daten, wobei *n* der Index in einer bestimmten Zelle ist.

## <a name="state"></a>State

Die Zustands Variable gibt den Audiowiedergabe Status von Windows-Media Player wieder. Die playerstate-Enumerationswerte lauten.


```C++
    stop_state              = 0,    // audio is currently stopped
    pause_state             = 1,    // audio is currently paused
    play_state              = 2     // audio is currently playing

```



Sie können diese Variable verwenden, um je nach Audiowiedergabe Status verschiedene Aktionen durchführen. Sie können z. b. eine Art von Visualisierung wiedergeben, wenn die Audiodatei abgespielt wird, und eine andere, wenn Sie angehalten wird.

## <a name="time-stamp"></a>Zeitstempel

Die timestamp-Variable gibt die aktuelle Zeit an, zu der die Momentaufnahme erstellt wird. Dies kann verwendet werden, um zu messen, wie häufig die Momentaufnahmen erstellt werden.

Sie können diese Variable verwenden, um Ihre Animationen zu Zeit zu verwenden. Wenn die Momentaufnahmen zu häufig vorkommen, können Sie das Abbild ordnungsgemäß herabstufen, sodass es auf die von Ihnen gewählte Weise angezeigt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Rendering**](implementing-render.md)
</dt> </dl>

 

 




