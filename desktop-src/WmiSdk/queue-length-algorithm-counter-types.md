---
description: Algorithmuszählertypen mit Warteschlangenlänge erhöhen die Anzahl der Elemente in einer Warteschlange in jedem Stichprobenintervall gemäß der entsprechenden frequency-Eigenschaft&\# 8212; Frequency \_ PerfTime, und so weiter.
ms.assetid: 514b1a79-ed9d-4ec6-a6ea-b3490291ce18
ms.tgt_platform: multiple
title: Algorithmuszählertypen mit Warteschlangenlänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9fd3019e9a5e7150402266fd206d3f460f3d0ae3b07f4c6c7d51e82473e9dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316537"
---
# <a name="queue-length-algorithm-counter-types"></a>Algorithmuszählertypen mit Warteschlangenlänge

Algorithmuszählertypen mit Warteschlangenlänge erhöhen die Anzahl der Elemente in einer Warteschlange in jedem Stichprobenintervall, wie von der entsprechenden frequency-Eigenschaft Frequency \_ PerfTime angegeben und so weiter. Das durchschnittliche Ergebnis der Warteschlange wird durch die Anzahl der Stichproben dividiert, um die durchschnittliche Warteschlangenlänge zu erzeugen.

Ein Beispiel hierfür ist die **AvgDiskQueueLength-Eigenschaft** im [**logischen Datenträger Win32 \_ PerfRawData \_ PerfDisk, \_**](./retrieving-raw-and-formatted-performance-data.md) die den INDIKATORtyp PERF \_ COUNTER \_ 100NS \_ QUEUELEN TYPE \_ verwendet.



| CounterType-Konstante                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PERF \_ COUNTER \_ QUEUELEN \_ TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523008<br/>            | Durchschnittliche Länge einer Warteschlange für eine Ressource im Laufe der Zeit. Er zeigt den Quotienten aus der Differenz der während der letzten zwei Messintervalle beobachteten Warteschlangenlängen und der Dauer des Intervalls an.                       |
| [PERF \_ COUNTER \_ LARGE \_ QUEUELEN \_ TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523264<br/>     | Durchschnittliche Länge einer Warteschlange für eine Ressource im Laufe der Zeit. Zähler dieses Typs zeigen den Quotienten aus der Differenz der während der letzten zwei Messintervalle beobachteten Warteschlangenlängen und der Dauer des Intervalls an. |
| [PERF \_ COUNTER \_ 100NS \_ QUEUELEN \_ TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 5571840<br/>     | Durchschnittliche Länge einer Warteschlange für eine Ressource im Laufe der Zeit in Einheiten von 100 Nanosekunden.                                                                                                                                        |
| [PERF \_ COUNTER \_ OBJ \_ TIME \_ QUEUELEN \_ TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 6620416<br/> | Zeit, zu der sich ein Objekt in einer Warteschlange befindet.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Leistungsindikatortypen](wmi-performance-counter-types.md)
</dt> </dl>

 

