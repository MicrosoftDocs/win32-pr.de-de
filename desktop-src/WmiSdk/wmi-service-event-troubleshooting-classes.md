---
description: Problembehandlungsklassen für WMI-Dienstereignisse werden von Ereignissen innerhalb des WMI-Diensts generiert, z. B. durch die Erstellung eines Threadpools.
ms.assetid: 1a1251c8-a2f7-47ac-9db1-d780d7d272f0
ms.tgt_platform: multiple
title: Problembehandlungsklassen für WMI-Dienstereignis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e811ac5b276e5562f73b5b432d5f3255af5bab7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443061"
---
# <a name="wmi-service-event-troubleshooting-classes"></a>Problembehandlungsklassen für WMI-Dienstereignis

Problembehandlungsklassen für WMI-Dienstereignisse werden von Ereignissen innerhalb des WMI-Diensts generiert, z. B. durch die Erstellung eines Threadpools.

Sie können die abstrakte Basisklasse [**MSFT \_ WmiEssEvent-Benachrichtigungen**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) abonnieren, um alle abgeleiteten Ereignisse zu erhalten, die in der folgenden Tabelle aufgeführt sind.



|   Ereignis                                                                                        |   BESCHREIBUNG                                                                                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**MSFT \_ WmiEssEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent)                                   | Übergeordnete Klasse für alle Windows-Verwaltungsinstrumentation (WMI) Eventing SubSystem (ESS)-Selbstereignisse. |
| [**MSFT \_ WmiRegisterNotificationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiregisternotificationevent) | Stellt die Erstellung einer Ereignissenke für die Benachrichtigung für eine Ereignisabfrage dar.                       |
| [**MSFT \_ WmiCancelNotificationSink**](/previous-versions/windows/desktop/wmisystemprov/msft-wmicancelnotificationsink)       | wird generiert, wenn eine Ereignissenke abgebrochen wird.                                                           |
| [**MSFT \_ WmiThreadPoolEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolevent)                     | stellt eine Benachrichtigung über Threadereignisse im WMI-Ereignisuntersystem (ESS) zur Verfügung.                           |
| [**MSFT \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated)                 | Stellt eine Benachrichtigung beim Erstellen eines Threads im WMI-Ereignisuntersystem (ESS) zur                   |
| [**MSFT \_ WmiThreadPoolDeleted**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpooldeleted)                 | Stellt Benachrichtigungen zum Löschen eines Threads im WMI-Ereignisuntersystem (ESS) zurEntspricht.                   |
| [**MSFT \_ WmiFilterEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterevent)                             | Übergeordnete Klasse für alle permanenten Ereignis-Consumerfilterereignisse.                                        |
| [**MSFT \_ WmiFilterActivated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilteractivated)                     | Definiert die erfolgreiche Aktivierung eines permanenten Ereignisverbraucherabonnementfilters.                |
| [**MSFT \_ WmiFilterDeactivated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterdeactivated)                 | Definiert die erfolgreiche Deaktivierung eines permanenten Consumerabonnementfilters.                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Problembehandlung bei WMI](wmi-troubleshooting.md)
</dt> <dt>

Problembehandlung bei WMI
</dt> <dt>

[Überwachen von Ereignissen](monitoring-events.md)
</dt> <dt>

[Empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md)
</dt> </dl>

 

 
