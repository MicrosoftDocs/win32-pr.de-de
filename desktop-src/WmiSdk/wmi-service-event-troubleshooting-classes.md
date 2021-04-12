---
description: Fehler Behebungs Klassen für WMI-Dienst Ereignisse werden durch Ereignisse im WMI-Dienst generiert, z. b. die Erstellung eines Thread Pools.
ms.assetid: 1a1251c8-a2f7-47ac-9db1-d780d7d272f0
ms.tgt_platform: multiple
title: Fehler Behebungs Klassen für WMI-Dienst Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf3728b6ae150a948fdf71515e27f17ca7280f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218164"
---
# <a name="wmi-service-event-troubleshooting-classes"></a>Fehler Behebungs Klassen für WMI-Dienst Ereignisse

Fehler Behebungs Klassen für WMI-Dienst Ereignisse werden durch Ereignisse im WMI-Dienst generiert, z. b. die Erstellung eines Thread Pools.

Sie können die abstrakte Basisklasse " [**MSFT \_ wmiesabvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) "-Benachrichtigungen abonnieren, um alle abgeleiteten Ereignisse zu erhalten, die in der folgenden Tabelle aufgeführt sind.



|                                                                                           |                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**MSFT \_ wmiesabvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent)                                   | Übergeordnete Klasse für alle nicht-selbst Ereignisse (ESS) des Eventing-Subsystems (Windows-Verwaltungsinstrumentation). |
| [**MSFT \_ wmiregisternotificationevent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiregisternotificationevent) | Stellt die Erstellung einer Ereignis Senke für die Benachrichtigung für eine Ereignis Abfrage dar.                       |
| [**MSFT \_ wmicancelnotificationsink**](/previous-versions/windows/desktop/wmisystemprov/msft-wmicancelnotificationsink)       | wird generiert, wenn eine Ereignis Senke abgebrochen wird.                                                           |
| [**MSFT \_ wmithread poolevent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolevent)                     | stellt eine Benachrichtigung über Thread Ereignisse im WMI-Ereignis Subsystem (ESS) bereit.                           |
| [**MSFT \_ wmithread poolcreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated)                 | Stellt eine Benachrichtigung bereit, wenn ein Thread im WMI-Ereignis Subsystem (ESS) erstellt wird.                   |
| [**MSFT \_ wmithread pooldeleted**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpooldeleted)                 | Stellt eine Benachrichtigung bereit, wenn ein Thread im WMI-Ereignis Subsystem (ESS) gelöscht wird.                   |
| [**MSFT \_ wmifilterevent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterevent)                             | Übergeordnete Klasse für alle permanenten Ereignisconsumer-Filter Ereignisse.                                        |
| [**MSFT \_ wmifilteraktivierte**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilteractivated)                     | Definiert die erfolgreiche Aktivierung eines permanenten ereignisconsumerabonnementfilters.                |
| [**MSFT \_ wmifilterdeaktiviert**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterdeactivated)                 | Definiert die erfolgreiche Aktivierung eines permanenten Kunden Abonnement Filters.                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Problembehandlung](wmi-troubleshooting.md)
</dt> <dt>

WMI-Problembehandlung
</dt> <dt>

[Überwachen von Ereignissen](monitoring-events.md)
</dt> <dt>

[Empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md)
</dt> </dl>

 

 
