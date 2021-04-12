---
description: Gegen Typen von Counter-Algorithmus-Algorithmen können Raten oder Durchschnittswerte für ein Beispiel oder über einen Zeitraum für einen bestimmten Vorgang berechnen.
ms.assetid: 4423e35e-2a93-4f68-8494-89df05268cc9
ms.tgt_platform: multiple
title: Gegen Typen von Algorithmus-Algorithmus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12bd55a2a9cc9cc9193a86ffe740ebfa856c0ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346748"
---
# <a name="counter-algorithm-counter-types"></a>Gegen Typen von Algorithmus-Algorithmus

Gegen Typen von Counter-Algorithmus-Algorithmen können Raten oder Durchschnittswerte für ein Beispiel oder über einen Zeitraum für einen bestimmten Vorgang berechnen.

Die **avgdiskbytespertransfer** -Eigenschaft in der [**Win32 \_ perfrawdata \_ perfdisk \_ PhysicalDisk**](/previous-versions//aa394308(v=vs.85)) -Klasse verwendet den durchschnittlichen perf- \_ \_ Massen CounterType. In diesem Fall ist die Übertragung der Vorgang, und die kumulierte Anzahl von Bytes, die gesendet werden, sind die Daten des Zählers. Bei zwei Beispielen führt das Aufteilen der Differenz von akkumulierten Bytes durch den Unterschied in der Anhäufung von Übertragungen zur durchschnittlichen Anzahl von Bytes pro Übertragung während des Zeitraums zwischen den Stichproben.

Die folgenden gegen Algorithmen werden bereitgestellt:



| Counter Type                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Leistung [ \_ Durchschnittlicher \_ Massen](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Wert 1073874176<br/>       | Die durchschnittliche Anzahl der verarbeiteten Elemente während eines Vorgangs. Dieser zähtertyp zeigt das Verhältnis der verarbeiteten Elemente (z. b. gesendete Bytes) an die Anzahl der abgeschlossenen Vorgänge an und erfordert eine Basis Eigenschaft mit der durchschnittlichen perf- \_ \_ Basis als zähtertyp. |
| Leistung [ \_ Counter- \_ Counter](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))-Dezimalwert 272696320<br/>     | Die durchschnittliche Anzahl der Vorgänge, die während der einzelnen Sekunden des Stichproben Intervalls abgeschlossen wurden. .                                                                                                                                                                          |
| Leistung [ \_ Sample \_ Counter](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4260864<br/>        | Die durchschnittliche Anzahl von Vorgängen, die in einer Sekunde abgeschlossen wurden. Dieser zähtertyp erfordert eine Basis Eigenschaft mit dem Counter Type perf \_ Sample \_ base.                                                                                                                   |
| Leistung [ \_ Zähler für die \_ Massen \_ Zählung](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))in Dezimal 272696576<br/> | Die durchschnittliche Anzahl der Vorgänge, die während der einzelnen Sekunden des Stichproben Intervalls abgeschlossen wurden. Dieser zähtertyp ist mit dem Leistungs \_ Zählers des Leistungs Zählers identisch \_ , aber er verwendet größere Felder, um größere Werte zu verarbeiten.                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Leistungsdaten Typen](wmi-performance-counter-types.md)
</dt> </dl>

 

