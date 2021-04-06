---
description: Die Zähler Typen der Genauigkeits Geber Algorithmen erhalten genauere Messwerte als systemtimer.
ms.assetid: f7159645-6287-47a3-895e-20dae6e0892a
ms.tgt_platform: multiple
title: Zähler Typen für Genauigkeits Geber Algorithmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a8864587fedc915678dfa4a9e578ca051e1262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759769"
---
# <a name="precision-timer-algorithm-counter-types"></a>Zähler Typen für Genauigkeits Geber Algorithmen

Die Zähler Typen der Genauigkeits Geber Algorithmen erhalten genauere Messwerte als systemtimer. Der Dienst, der die Daten bereitstellt, stellt auch einen Zeitstempel bereit. Dadurch werden die Fehler vermieden, die aufgrund der kurzen und Variablen Zeit zwischen der Erfassung des Systemzeit Stempels und der Auflistung der Daten aus der Leistungs-dll auftreten können. Dieser Basis Zeitstempel für Genauigkeits Timer ist eine perf \_ Precision- \_ Zeitstempel Eigenschaft, die unmittelbar auf die perf Precision-Zeit Geber Eigenschaft folgen muss \_ \_ .



| CounterType-Konstante                                                                                         | BESCHREIBUNG                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Leistung [ \_ Genauigkeits \_ System- \_ Timer](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 541525248<br/> | Ähnelt \_ dem Leistungs Zähler- \_ Timer, mit dem Unterschied, dass er anstelle des Systemzeit Stempels eine Zähler definierte Zeitbasis verwendet.             |
| Leistung [ \_ Genauigkeit \_ 100 NS \_ Timer](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 542573824<br/>  | Ähnelt dem perf-Wert von \_ 100 nsec \_ , außer dass er eine 100-ns-Zähler definierte Zeitbasis anstelle des System-100-ns-Zeitstempels verwendet. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Leistungsdaten Typen](wmi-performance-counter-types.md)
</dt> </dl>

 

