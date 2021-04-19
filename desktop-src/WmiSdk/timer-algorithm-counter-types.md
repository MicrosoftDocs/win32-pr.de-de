---
description: Zähler Typen für Zeit Geber Algorithmen basieren auf dem Umfang der verstärkten Verwendung des Leistungsobjekts für einen Beispiel Zeitraum.
ms.assetid: 4ec49efc-2b0f-4205-8b58-fb121da32b4e
ms.tgt_platform: multiple
title: Zähler Typen für Timer-Algorithmus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee815e6740c8736d0a7f2194b25e521368bbe96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352757"
---
# <a name="timer-algorithm-counter-types"></a>Zähler Typen für Timer-Algorithmus

Zähler Typen für Zeit Geber Algorithmen basieren auf dem Umfang der verstärkten Verwendung des Leistungsobjekts für einen Beispiel Zeitraum. Die Daten des Zählers sind eine zunehmende Quantums der Gesamtaktivität für ein Objekt bis zu dem Zeitpunkt, an dem das Beispiel stattfindet. Der Unterschied zwischen den beiden Beispielen gibt die Gesamtzeit an, während der das Objekt während des Beispiel Zeitraums aktiv ist.

Die Aufteilung durch den Beispiel Zeitraum führt zu einer Zeitspanne, in der das Objekt während eines Zeitraums aktiv ist. Durch die Aufteilung durch die Anzahl interner Abruf Interrupts wird die durchschnittliche Verwendung zwischen Abruf Beispielen bestimmt.

Beispielsweise verwendet die **avgdisksecperread** -Eigenschaft in der [**Win32 \_ perfrawdata \_ perfdisk \_ PhysicalDisk**](/previous-versions//aa394308(v=vs.85)) -Klasse den **perf \_ Average \_ Timer** Counter Type. Es berechnet die durchschnittliche Zeit in Sekunden für das Lesen von Daten vom Datenträger und erfordert die Basis Eigenschaft **avgdisksecperread \_**. Im Gegensatz zum Leistungs **\_ Zähler- \_ Timer** stellt die durchschnittliche Zeit Geber Basis eine kumulierte Anzahl von Vorgängen dar, und die Zählerdaten sind ein Lauf Zeitwert, was bedeutet, dass die Gesamtzeit aller Vorgänge in Sekunden ergibt, wenn Sie durch die Zeitbasis dividiert wird.



| Counter-typkonstante                                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Leistungs \_ Zähler- \_ Timer](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimalzahl 541132032<br/>             | Die durchschnittliche Zeit, die eine Komponente als Prozentsatz der gesamten Stichproben Zeit aktiv ist.<br/>                                                                                                                                                                                                                                                                                                         |
| [Leistungs \_ Zähler- \_ Timer- \_ Inv](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimalzahl 557909248<br/>        | Der durchschnittliche Prozentsatz der während des Samplingintervalls beobachteten Zeit, dass das Objekt nicht aktiv ist. Dieser zähtertyp ist identisch mit dem Wert von **perf \_ 100nsec \_ Timer \_ Inv** , mit dem Unterschied, dass er die Zeit in Einheiten von Ticks des systemleistungtimers und nicht in 100-ns-Einheiten misst.<br/>                                                                                                                       |
| [Perf-Durchschnittszeit Geber \_ \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimalzahl 805438464<br/>             | Die durchschnittliche Zeit zum Durchführen eines Prozesses oder eines Vorgangs. Dieser zählungstyp zeigt das Verhältnis der insgesamt verstrichenen Zeit des Stichproben Intervalls zur Anzahl der Prozesse oder Vorgänge an, die während dieser Zeit abgeschlossen wurden.<br/> Dieser zähtertyp erfordert eine Basis Eigenschaft mit der **durchschnittlichen perf- \_ \_ Basis** als zähtertyp.<br/>                                                                         |
| [Perf \_ 100 nSek. \_ Timer](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimalzahl 542180608<br/>             | Die aktive Zeit einer Komponente als Prozentsatz der gesamten verstrichenen Zeit in Einheiten von 100 ns des Stichproben Intervalls.<br/>                                                                                                                                                                                                                                                                          |
| [Perf \_ 100 nSek. Zeit Geber \_ \_ Inv](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimalzahl 558957824<br/>        | Der Prozentsatz der Zeit, zu der das Objekt nicht verwendet wurde. Dieser zähtertyp ist mit dem Leistungsindikatoren- **\_ \_ Timer \_ Inv** identisch, mit dem Unterschied, dass er die Zeit in 100-ns-Einheiten und nicht in den Zeitgeber Ticks der Systemleistung<br/>                                                                                                                                                                                   |
| [Leistungs \_ Zähler für \_ Multi- \_ Timer](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimalzahl 574686464<br/>      | Die aktive Zeit einer oder mehrerer Komponenten als Prozentsatz der Gesamtzeit des Stichproben Intervalls. Dieser zähtertyp unterscheidet sich von einem leistungsfähigen **\_ \_ \_ Multitimer von perf 100 nsec** , da er die Zeit in Einheiten von Ticks des systemleistungtimers und nicht in 100-ns-Einheiten misst.<br/> Dieser zähtertyp erfordert eine Basis Eigenschaft mit dem Leistungs **\_ Zählers \_ \_ MultiBase** -zähtertyp.<br/>        |
| [Leistungs \_ Zähler \_ \_ Multitimer \_ Inv](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimalzahl 591463680<br/> | Inaktive Zeit einer oder mehrerer Komponenten als Prozentsatz der Gesamtzeit des Stichproben Intervalls. Dieser zähtertyp unterscheidet sich von der Leistungsfähigkeit von **\_ 100 nsec mit mehreren Zeit Geber \_ \_ \_ Inv** insofern, als er die Zeit in Einheiten von Ticks des systemleistungtimers und nicht in 100-ns-Einheiten misst.<br/> Dieser zähtertyp erfordert eine Basis Eigenschaft mit dem Leistungs **\_ Zählers \_ \_ MultiBase** -zähtertyp.<br/> |
| [Perf \_ 100 nSek. \_ Multi- \_ Timer](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimalzahl 575735040<br/>      | Dieser zähtertyp zeigt den aktiven Zeitpunkt einer oder mehrerer Komponenten als Prozentsatz der Gesamtzeit (100-ns-Einheiten) des Stichproben Intervalls an.<br/> Dieser zähtertyp erfordert eine Basis Eigenschaft mit dem Leistungs **\_ Zählers \_ \_ MultiBase** -zähtertyp.<br/>                                                                                                                                     |
| [Perf \_ 100 nSek. \_ mehrstufige \_ \_ Inv](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimalzahl 592512256<br/> | Inaktive Zeit einer oder mehrerer Komponenten als Prozentsatz der Gesamtzeit des Stichproben Intervalls. Leistungsindikatoren dieses Typs messen die Zeit in 100-ns-Einheiten.<br/> Dieser zähtertyp erfordert eine Basis Eigenschaft mit dem Leistungs **\_ Zählers \_ \_ MultiBase** -zähtertyp.<br/>                                                                                                                          |
| [Perf \_ obj \_ Zeit \_ Geber](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Dezimalzahl 543229184<br/>           | Ein 64-Bit-Timer in Objekt spezifischen Einheiten.<br/>                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Leistungsdaten Typen](wmi-performance-counter-types.md)
</dt> </dl>

 

