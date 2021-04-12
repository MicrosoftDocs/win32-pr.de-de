---
description: Algorithmustypen für die Warteschlangen Länge erhöhen die Anzahl der Elemente in einer Warteschlange in den einzelnen Stichproben Intervallen, wie von der entsprechenden Frequency-Eigenschaft angegeben&\# 8212; "Frequenz \_ PerfTime" usw.
ms.assetid: 514b1a79-ed9d-4ec6-a6ea-b3490291ce18
ms.tgt_platform: multiple
title: Algorithmustypen der Warteschlangen Länge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06665c2fb8fca014c7d722f0ea22cf7e86833ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215344"
---
# <a name="queue-length-algorithm-counter-types"></a>Algorithmustypen der Warteschlangen Länge

Algorithmustypen für die Warteschlangen Länge erhöhen die Anzahl der Elemente in einer Warteschlange in den einzelnen Stichproben Intervallen, wie in der entsprechenden Häufigkeit für Häufigkeits Häufigkeit \_ usw. angegeben. Das verarbeitete Ergebnis dividiert durch die Anzahl von Stichproben, um die durchschnittliche Warteschlangen Länge zu ermitteln.

Ein Beispiel hierfür ist die **avgdiskqueuelength** -Eigenschaft im [**Win32 \_ perfrawdata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) , die den Leistungsindikator \_ \_ 100ns-Typ- \_ \_ Indikators vom Typ "Queue" verwendet.



| CounterType-Konstante                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Leistung [ \_ Counter \_ queuelen- \_ Typ](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523008<br/>            | Die durchschnittliche Länge einer Warteschlange für eine Ressource im Zeitverlauf. Er zeigt den Quotienten aus der Differenz der während der letzten zwei Messintervalle beobachteten Warteschlangenlängen und der Dauer des Intervalls an.                       |
| Leistung [ \_ \_Large \_ queuelen- \_ Typ](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523264<br/>     | Die durchschnittliche Länge einer Warteschlange für eine Ressource im Zeitverlauf. Zähler dieses Typs zeigen den Quotienten aus der Differenz der während der letzten zwei Messintervalle beobachteten Warteschlangenlängen und der Dauer des Intervalls an. |
| Leistung [ \_ Counter \_ 100 NS \_ queuelen \_ Type](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 5571840<br/>     | Die durchschnittliche Länge einer Warteschlange für eine Ressource im Zeitverlauf in 100 Nanosekunden-Einheiten.                                                                                                                                        |
| Leistung [ \_ Counter- \_ obj- \_ Zeit \_ queuelen- \_ Typ](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 6620416<br/> | Uhrzeit, zu der ein Objekt in einer Warteschlange ist.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Leistungsdaten Typen](wmi-performance-counter-types.md)
</dt> </dl>

 

