---
description: Indikator-Algorithmus-Indikatortypen können Raten oder Durchschnittsbytes für eine Stichprobe oder über einen bestimmten Zeitraum für einen bestimmten Vorgang berechnen.
ms.assetid: 4423e35e-2a93-4f68-8494-89df05268cc9
ms.tgt_platform: multiple
title: Indikatortypen für Zähleralgorithmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5568d4df0d1b50fd55a4f9d007d6506cf59a8f67a05885c21d64a6be8812536c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131432"
---
# <a name="counter-algorithm-counter-types"></a>Indikatortypen für Zähleralgorithmen

Indikator-Algorithmus-Indikatortypen können Raten oder Durchschnittsbytes für eine Stichprobe oder über einen bestimmten Zeitraum für einen bestimmten Vorgang berechnen.

Die **AvgDiskBytesPerTransfer-Eigenschaft** in der [**Win32 \_ PerfRawData \_ PerfDisk \_ PhysicalDisk-Klasse**](/previous-versions//aa394308(v=vs.85)) verwendet den PERF \_ AVERAGE \_ BULK-Indikatortyp. In diesem Fall ist die Übertragung der Vorgang, und die akkumulierende Anzahl gesendeter Bytes sind die Indikatordaten. Bei zwei beliebigen Stichproben wird die durchschnittliche Anzahl von Bytes pro Übertragung während des Zeitraums zwischen den Stichproben erzeugt, wenn die Differenz der akkumulierten Bytes durch die Differenz beim Akkumulieren von Übertragungen dividiert wird.

Die folgenden Leistungsindikatoralgorithmen werden bereitgestellt:



| Countertype                                                                                              | Beschreibung                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PERF \_ AVERAGE \_ BULK](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 1073874176<br/>       | Die durchschnittliche Anzahl der während eines Vorgangs verarbeiteten Elemente. Dieser Indikatortyp zeigt ein Verhältnis der verarbeiteten Elemente (z. B. gesendete Bytes) zur Anzahl der abgeschlossenen Vorgänge an und erfordert eine Basiseigenschaft mit PERF AVERAGE BASE als \_ \_ Indikatortyp. |
| [PERF \_ COUNTER \_ COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696320<br/>     | Durchschnittliche Anzahl von Vorgängen, die während jeder Sekunde des Stichprobenintervalls abgeschlossen wurden. .                                                                                                                                                                          |
| [PERF \_ SAMPLE \_ COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4260864<br/>        | Durchschnittliche Anzahl der in einer Sekunde abgeschlossenen Vorgänge. Dieser Indikatortyp erfordert eine Basiseigenschaft mit dem Leistungsindikatortyp PERF \_ SAMPLE \_ BASE.                                                                                                                   |
| [PERF \_ COUNTER \_ BULK \_ COUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696576<br/> | Durchschnittliche Anzahl von Vorgängen, die während jeder Sekunde des Stichprobenintervalls abgeschlossen wurden. Dieser Indikatortyp ist identisch mit dem PERF COUNTER COUNTER-Typ, verwendet jedoch größere \_ \_ Felder, um größere Werte aufnehmen zu können.                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Leistungsindikatortypen](wmi-performance-counter-types.md)
</dt> </dl>

 

