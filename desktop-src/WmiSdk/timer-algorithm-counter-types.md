---
description: Timeralgorithmus-Indikatortypen basieren auf dem Umfang der zunehmenden Verwendung des Leistungsobjekts über einen Stichprobenzeitraum.
ms.assetid: 4ec49efc-2b0f-4205-8b58-fb121da32b4e
ms.tgt_platform: multiple
title: Timer-Algorithmus-Indikatortypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e3a606babb005eca7f01f75f735cd6d6a9da29c9c1427c56614c318f9465f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554014"
---
# <a name="timer-algorithm-counter-types"></a>Timer-Algorithmus-Indikatortypen

Timeralgorithmus-Indikatortypen basieren auf dem Umfang der zunehmenden Verwendung des Leistungsobjekts über einen Stichprobenzeitraum. Die Indikatordaten sind ein zunehmendes Quantenmaß der Gesamtaktivität für ein Objekt bis zu dem Zeitpunkt, zu dem die Stichprobe stattfindet. Der Unterschied zwischen den beiden Stichproben gibt die Gesamtzeit an, die das Objekt während des Stichprobenzeitraums aktiv ist.

Die Division durch den Beispielzeitraum führt zu einem Teil der Zeit, in der das Objekt während eines Zeitraums aktiv ist. Die Division durch die Anzahl interner Abrufunterbrechungen bestimmt die durchschnittliche Verwendung zwischen den Abrufbeispielen.

Beispielsweise verwendet die **AvgDiskSecPerRead-Eigenschaft** in der [**Win32 \_ PerfRawData \_ PerfDisk \_ PhysicalDisk-Klasse**](/previous-versions//aa394308(v=vs.85)) den **PERF \_ AVERAGE \_ TIMER-Indikatortyp.** Er berechnet die durchschnittliche Zeit in Sekunden für das Lesen von Daten vom Datenträger und erfordert die Basiseigenschaft **AvgDiskSecPerRead \_ Base.** Im Gegensatz zu PERF COUNTER TIMER stellt die durchschnittliche **\_ \_ Timerbasis** eine akkumulierende Anzahl von Vorgängen dar, und die Leistungsindikatordaten sind ein Laufzeitwert, was bedeutet, dass bei Dividierung durch die Zeitbasis die Gesamtzeit aller Vorgänge in Sekunden ergibt.



| Indikatortypkonst constant                                                                                                      | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_ \_ LEISTUNGSINDIKATOR-TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimaltrennzeichen 541132032<br/>             | Durchschnittliche Zeit, die eine Komponente als Prozentsatz der gesamten Stichprobenzeit aktiv ist.<br/>                                                                                                                                                                                                                                                                                                         |
| [\_ \_ \_ LEISTUNGSINDIKATOR-TIMER-INV](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimaltrennzeichen 557909248<br/>        | Durchschnittlicher Prozentsatz der Zeit, die während des Stichprobenintervalls beobachtet wurde, dass das Objekt nicht aktiv ist. Dieser Indikatortyp ist identisch mit **PERF \_ 100NSEC \_ TIMER \_ INV,** mit der Ausnahme, dass die Zeit in Einheiten von Ticks des Systemleistungszeiters und nicht in Einheiten von 100ns misst wird.<br/>                                                                                                                       |
| [PERF \_ AVERAGE \_ TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimaltrennzeichen 805438464<br/>             | Durchschnittliche Zeit zum Abschließen eines Prozesses oder Vorgangs. Dieser Indikatortyp zeigt ein Verhältnis zwischen der gesamten verstrichenen Zeit des Stichprobenintervalls und der Anzahl von Prozessen oder Vorgängen an, die während dieser Zeit abgeschlossen wurden.<br/> Dieser Indikatortyp erfordert eine Basiseigenschaft mit **PERF \_ AVERAGE \_ BASE** als Indikatortyp.<br/>                                                                         |
| [PERF \_ 100NSEC \_ TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimaltrennzeichen 542180608<br/>             | Die aktive Zeit einer Komponente als Prozentsatz der insgesamt verstrichenen Zeit in Einheiten von 100 ns des Stichprobenintervalls.<br/>                                                                                                                                                                                                                                                                          |
| [PERF \_ 100NSEC \_ TIMER \_ INV](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimaltrennzeichen 558957824<br/>        | Prozentsatz der Zeit, die das Objekt nicht verwendet wurde. Dieser Indikatortyp ist identisch mit **PERF \_ COUNTER \_ TIMER \_ INV,** mit der Ausnahme, dass er die Zeit in Einheiten von 100ns und nicht in Systemleistungs-Timer-Ticks misst.<br/>                                                                                                                                                                                   |
| [PERF \_ COUNTER \_ MULTI \_ TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimaltrennzeichen 574686464<br/>      | Die aktive Zeit einer oder mehrere Komponenten als Prozentsatz der Gesamtzeit des Stichprobenintervalls. Dieser Indikatortyp unterscheidet sich von **PERF \_ 100NSEC \_ MULTI \_ TIMER** dadurch, dass er die Zeit in Einheiten von Ticks des Systemleistungs-Timers statt in Einheiten von 100ns misst.<br/> Dieser Indikatortyp erfordert eine Basiseigenschaft mit dem **PERF \_ COUNTER MULTI \_ \_ BASE-Indikatortyp.**<br/>        |
| [LEISTUNGSINDIKATOR \_ \_ \_ MULTI-TIMER-INV \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimaltrennzeichen 591463680<br/> | Inaktive Zeit einer oder mehrere Komponenten als Prozentsatz der Gesamtzeit des Stichprobenintervalls. Dieser Indikatortyp unterscheidet sich von **PERF \_ 100NSEC \_ MULTI \_ TIMER \_ INV** dadurch, dass er die Zeit in Einheiten von Ticks des Systemleistungs-Timers und nicht in Einheiten von 100ns misst.<br/> Dieser Indikatortyp erfordert eine Basiseigenschaft mit dem **PERF \_ COUNTER MULTI \_ \_ BASE-Indikatortyp.**<br/> |
| [PERF \_ 100NSEC \_ MULTI \_ TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimaltrennzeichen 575735040<br/>      | Dieser Indikatortyp zeigt die aktive Zeit einer oder mehrere Komponenten als Prozentsatz der Gesamtzeit (100 ns-Einheiten) des Stichprobenintervalls an.<br/> Dieser Indikatortyp erfordert eine Basiseigenschaft mit dem **PERF \_ COUNTER MULTI \_ \_ BASE-Indikatortyp.**<br/>                                                                                                                                     |
| [PERF \_ 100NSEC \_ MULTI \_ TIMER \_ INV](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimaltrennzeichen 592512256<br/> | Inaktive Zeit einer oder mehrere Komponenten als Prozentsatz der Gesamtzeit des Stichprobenintervalls. Leistungsindikatoren dieses Typs messen die Zeit in Einheiten von 100 ns.<br/> Dieser Indikatortyp erfordert eine Basiseigenschaft mit dem **PERF \_ COUNTER MULTI \_ \_ BASE-Indikatortyp.**<br/>                                                                                                                          |
| [PERF \_ OBJ \_ TIME \_ TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimaltrennzeichen 543229184<br/>           | Ein 64-Bit-Timer in objektspezifischen Einheiten.<br/>                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Leistungsindikatortypen](wmi-performance-counter-types.md)
</dt> </dl>

 

