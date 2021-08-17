---
description: Die Genauigkeits-Timer-Algorithmus-Indikatortypen erhalten genauere Messwerte als Systemzeitindikatoren.
ms.assetid: f7159645-6287-47a3-895e-20dae6e0892a
ms.tgt_platform: multiple
title: Genauigkeits-Timeralgorithmus-Indikatortypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 137d136db0b4dd579dfec4673b09ce216bef4042d9356b3938b79e7817e3d83a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131032"
---
# <a name="precision-timer-algorithm-counter-types"></a>Genauigkeits-Timeralgorithmus-Indikatortypen

Die Genauigkeits-Timer-Algorithmus-Indikatortypen erhalten genauere Messwerte als Systemzeitindikatoren. Der Dienst, der die Daten zur Verfügung stellt, stellt auch einen Zeitstempel zur Verfügung, der die Fehler beseitigt, die aufgrund der kleinen und variablen Zeit auftreten können, die zwischen der Erfassung des Systemzeitstempels und der Erfassung der Daten aus der Leistungs-DLL verstreicht. Dieser Basiszeitstempel für Genauigkeits-Timer ist eine PERF PRECISION TIMESTAMP-Eigenschaft, die unmittelbar auf die \_ \_ PERF \_ PRECISION \_ TIMER-Eigenschaft folgen muss.



| CounterType-Konstante                                                                                         | Beschreibung                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [PERF \_ PRECISION \_ SYSTEM \_ TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 541525248<br/> | Ähnlich wie PERF COUNTER TIMER, mit der Ausnahme, dass anstelle des Systemzeitstempels eine indikatordefinierte \_ \_ Zeitbasis verwendet wird.             |
| [PERF \_ GENAUIGKEIT: \_ 100NS \_ TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 542573824<br/>  | Ähnlich wie PERF 100NSEC TIMER, mit der Ausnahme, dass anstelle des Systemzeitstempels \_ \_ 100ns eine 100ns-Indikator-definierte Zeitbasis verwendet wird. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Leistungsindikatortypen](wmi-performance-counter-types.md)
</dt> </dl>

 

