---
description: Stellt Unterschiede zwischen Beispielen im Zeitverlauf dar und verwendet häufig einen Basiswert für die Berechnung.
ms.assetid: 613268ab-386b-421d-a5b5-aab6a065999c
ms.tgt_platform: multiple
title: Grundlegende algorithmuscounter-Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70514c10b2695aa940d48341752ef647dcca9719
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364156"
---
# <a name="basic-algorithm-counter-types"></a>Grundlegende algorithmuscounter-Typen

Grundlegende algorithmuszähtertypen stellen im allgemeinen Unterschiede zwischen den Beispielen im Zeitverlauf dar und verwenden häufig einen Basiswert für die Berechnung. Die Eigenschaft " **komponfreespace** " der Klasse " [**Win32 \_ perfformatteddata \_ perfdisk \_ PhysicalDisk**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) " gibt z. b. das Verhältnis des freien Speicherplatzes, der auf der physischen Datenträger Einheit verfügbar ist, zum gesamten nutzbaren Speicherplatz des ausgewählten physischen Laufwerks an. Diese Klasse enthält auch den Basiswert, " **prozentufreespace \_ Base**". Der prozentuale Anteil des freien Speicherplatzes wird durch Aufteilen von **prozentualer FreeSpace** durch die **\_ Basis** von Prozent und multipliziert mit 100% erreicht.

Die grundlegenden Algorithmen in der folgenden Tabelle werden bereitgestellt.



| CounterType-Konstante                                                                                    | BESCHREIBUNG                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Leistung [ \_ \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Unformatierte Bruch Dezimalzahl 537003008<br/>       | Das Verhältnis einer Teilmenge zu dem Satz als Prozentsatz. Dieser zähtertyp zeigt nur den aktuellen Prozentsatz an, nicht den Durchschnitt im Zeitverlauf.                                    |
| Leistung [ \_ Stichproben \_ Bruch](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Dezimaltrennzeichen 549585920<br/>    | Das durchschnittliche Verhältnis von Treffern zu allen Vorgängen während der letzten beiden Stichproben Intervalle. Dieser zähtertyp erfordert eine Basis Eigenschaft mit dem Leistungs \_ Proben- \_ Basis zähtertyp. |
| Leistung [ \_ Gegen \_ Delta](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))-Dezimaltrennzeichen 4195328<br/>        | Dieser Indikatortyp zeigt die Änderung des gemessenen Attributs zwischen den beiden letzten Messintervallen an.                                                         |
| Leistung [ \_ \_Großer \_ Delta](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))-Dezimaltrennzeichen 4195584<br/> | Identisch mit dem perf \_ -Leistungs Leistungs-gegen \_ Delta, aber eine 64-Bit-Darstellung für größere Werte.                                                                                        |
| Leistung [ \_ Verstrichene \_ Zeit](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 807666944<br/>       | Gesamtzeit zwischen dem Start des Prozesses und dem Zeitpunkt, zu dem dieser Wert berechnet wird.                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Leistungsdaten Typen](wmi-performance-counter-types.md)
</dt> </dl>

 

