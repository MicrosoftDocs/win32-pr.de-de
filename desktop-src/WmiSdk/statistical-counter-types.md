---
description: Die Leistungs Datenanbieter für die leistungsstarke WMI-Leistung berechnet die statistischen Leistungs Zählers für eine angegebene Anzahl von Rohdaten-Leistungs Beispielen.
ms.assetid: a7e32ef2-fad1-449c-beee-07db4b93e3fe
ms.tgt_platform: multiple
title: Statistische Counter-Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb97224b06881cbc3c8b1375c04a4df5be1095f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042587"
---
# <a name="statistical-counter-types"></a>Statistische Counter-Typen

Die [Leistungs Datenanbieter](formatted-performance-data-provider.md) für die leistungsstarke WMI-Leistung berechnet die statistischen Leistungs Zählers für eine angegebene Anzahl von Rohdaten-Leistungs Beispielen. Die Algorithmen für die Counter-Typen erfordern keine geerbten Zeitstempel-oder Häufigkeits Eigenschaften (z. b. " **Zeitstempel \_ PerfTime** " oder " **Frequency \_ PerfTime**"), die für andere Leistungstypen erforderlich sind

Stattdessen unterstützen die statistischen Counter-Typen einen **Qualifizierer** , der die Anzahl der zu verwendenden Beispiele identifiziert. Ein Beispiel wird gesammelt, wenn die [**Aktualisierungs**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) Methode für das Leistungs Objekt aufgerufen wird. Verwenden Sie für Skripts die Methode " [**Swap. Refresh**](swbemrefresher-refresh.md) ". Die berechneten Daten enthalten das Ergebnis der Berechnung, die für die **samplewindow** -Anzahl von Stichproben aus der Rohdaten-Eigenschaft ausgeführt wird. Die Rohdaten für die Berechnung sind frm der im **Counter** -Qualifizierer angegebene Eigenschaftsname.

Weitere Informationen finden Sie unter Abrufen [statistischer Leistungsdaten](obtaining-statistical-performance-data.md) und [zugreifen auf vorinstallierte WMI-Leistungsklassen](accessing-wmi-preinstalled-performance-classes.md).



| CounterType-Konstante                    | BESCHREIBUNG                                                                                                                                                                                |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_kochmittel Wert](cooker-average.md)   | Fasst wiederholte Beobachtungen einer Eigenschaft in einer [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klasse zusammen und dividiert die Summe durch die Anzahl von Beobachtungen.                              |
| [Maximaler kochwert \_](cooker-max.md)           | Größter Wert aus einem Satz von Beobachtungen einer Eigenschaft in einer [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klasse.                                                                    |
| [Koch \_ Min.](cooker-min.md)           | Der kleinste Wert aus einem Satz von Beobachtungen einer Eigenschaft in einer [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klasse.                                                                   |
| [Koch \_ Bereich](cooker-range.md)       | Der Unterschied [zwischen den minimalen](cooker-min.md) und [maximalen](cooker-max.md) Werten für einen Satz von unformatierten Beobachtungen einer Eigenschaft in einer [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klasse. |
| [Koch \_ Varianz](cooker-variance.md) | Das Maß der Varianz, das verwendet werden kann, um die Dispersion für eine Reihe von unformatierten Beobachtungen einer Eigenschaft in einer " [**\_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) "-Klasse zu charakterisieren.            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Leistungsdaten Typen](wmi-performance-counter-types.md)
</dt> <dt>

[Überwachen von Leistungsdaten](monitoring-performance-data.md)
</dt> <dt>

[Aktualisieren von WMI-Daten in Skripts](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[Zugreifen auf Leistungsdaten im Skript](accessing-performance-data-in-script.md)
</dt> <dt>

[Zugreifen auf Leistungsdaten in C++](accessing-performance-data-in-c--.md)
</dt> </dl>

 

 
