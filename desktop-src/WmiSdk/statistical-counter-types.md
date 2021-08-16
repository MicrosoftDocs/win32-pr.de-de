---
description: Der WMI-Leistungsindikator "Formatierte Leistung Datenanbieter berechnet die statistischen Indikatortypen für eine angegebene Anzahl von Unformatierten Indikatordatenbeispielen.
ms.assetid: a7e32ef2-fad1-449c-beee-07db4b93e3fe
ms.tgt_platform: multiple
title: Statistische Indikatortypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1289bae423305bac863afefaba8e5700268d98e594fe767d597c8470aa4f1ac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314819"
---
# <a name="statistical-counter-types"></a>Statistische Indikatortypen

Der WMI-Hochleistungs-Leistungsindikator ["Formatierte Datenanbieter](formatted-performance-data-provider.md) berechnet die statistischen Indikatortypen für eine angegebene Anzahl von Unformatierten Indikatordatenbeispielen. Die Algorithmen für die Indikatortypen erfordern keine geerbten Zeitstempel- oder Häufigkeitseigenschaften (z. B. **TimeStamp \_ PerfTime** oder **Frequency \_ PerfTime),** die andere Indikatortypen erfordern.

Stattdessen unterstützen die statistischen Indikatortypen einen **Qualifizierer,** der an identifiziert, wie viele Stichproben verwendet werden. Ein Beispiel wird gesammelt, wenn die [**Refresh-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) für das Leistungsobjekt aufgerufen wird. Verwenden Sie für Skripts die [**SWbemRefresher.Refresh-Methode.**](swbemrefresher-refresh.md) Die berechneten Daten enthalten das Ergebnis der Berechnung, die für die **SampleWindow-Anzahl** von Stichproben aus der Rohdateneigenschaft ausgeführt wurde. Die Rohdaten für die Berechnung stammen aus dem Eigenschaftennamen, der im **Counter-Qualifizierer** angegeben ist.

Weitere Informationen finden Sie unter [Abrufen statistischer Leistungsdaten](obtaining-statistical-performance-data.md) und [Zugreifen auf vorinstallierte WMI-Leistungsklassen.](accessing-wmi-preinstalled-performance-classes.md)



| CounterType-Konstante                    | Beschreibung                                                                                                                                                                                |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [COOKER \_ AVERAGE](cooker-average.md)   | Summiert wiederholte Beobachtungen einer Eigenschaft in einer [**Win32 \_ PerfRawData-Klasse**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) und dividiert die Summe durch die Anzahl der Beobachtungen.                              |
| [COOKER \_ MAX](cooker-max.md)           | Größter Wert aus einer Reihe von Beobachtungen einer Eigenschaft in einer [**Win32 \_ PerfRawData-Klasse.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)                                                                    |
| [COOKER \_ MIN](cooker-min.md)           | Kleinster Wert aus einer Reihe von Beobachtungen einer Eigenschaft in einer [**Win32 \_ PerfRawData-Klasse.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)                                                                   |
| [COOKER \_ RANGE](cooker-range.md)       | Unterschied zwischen den [Min-](cooker-min.md) und [Max-Werten](cooker-max.md) für einen Satz roher Beobachtungen einer Eigenschaft in einer [**Win32 \_ PerfRawData-Klasse.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) |
| [COOKER \_ VARIANCE](cooker-variance.md) | Maß für Die Variabilität, die verwendet werden kann, um eine Reihe roher Beobachtungen einer Eigenschaft in einer [**Win32 \_ PerfRawData-Klasse zu**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) charakterisieren.            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Leistungsindikatortypen](wmi-performance-counter-types.md)
</dt> <dt>

[Überwachen von Leistungsdaten](monitoring-performance-data.md)
</dt> <dt>

[Aktualisieren von WMI-Daten in Skripts](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[Zugreifen auf Leistungsdaten in Skripts](accessing-performance-data-in-script.md)
</dt> <dt>

[Zugreifen auf Leistungsdaten in C++](accessing-performance-data-in-c--.md)
</dt> </dl>

 

 
