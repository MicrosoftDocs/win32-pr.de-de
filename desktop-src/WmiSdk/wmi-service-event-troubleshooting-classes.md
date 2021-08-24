---
description: Klassen zur Problembehandlung von WMI-Dienstereignissen werden von Ereignissen innerhalb des WMI-Diensts generiert, z. B. der Erstellung von Threadpools.
ms.assetid: 1a1251c8-a2f7-47ac-9db1-d780d7d272f0
ms.tgt_platform: multiple
title: Problembehandlungsklassen für WMI-Dienstereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99be30a6b2f0551cae4e0abe269da5341e34e1444eb1545ca96377a43b5415ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502800"
---
# <a name="wmi-service-event-troubleshooting-classes"></a>Problembehandlungsklassen für WMI-Dienstereignisse

Klassen zur Problembehandlung von WMI-Dienstereignissen werden von Ereignissen innerhalb des WMI-Diensts generiert, z. B. der Erstellung von Threadpools.

Sie können die abstrakte Basisklasse [**MSFT \_ WmiEssEvent-Benachrichtigungen**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) abonnieren, um alle abgeleiteten Ereignisse abzurufen, die in der folgenden Tabelle aufgeführt sind.



|   Ereignis                                                                                        |   Beschreibung                                                                                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**MSFT \_ WmiEssEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent)                                   | Übergeordnete Klasse für alle ESS-Ereignisse (Eventing SubSystem) der Windows Management Instrumentation (WMI). |
| [**MSFT \_ WmiRegisterNotificationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiregisternotificationevent) | Stellt die Erstellung einer Ereignissenke für die Benachrichtigung für eine Ereignisabfrage dar.                       |
| [**MSFT \_ WmiCancelNotificationSink**](/previous-versions/windows/desktop/wmisystemprov/msft-wmicancelnotificationsink)       | wird generiert, wenn eine Ereignissenke abgebrochen wird.                                                           |
| [**MSFT \_ WmiThreadPoolEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolevent)                     | stellt eine Benachrichtigung über Threadereignisse im WMI-Ereignisuntersystem (ESS) bereit.                           |
| [**MSFT \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated)                 | Stellt eine Benachrichtigung bereit, wenn ein Thread im WMI-Ereignisuntersystem (ESS) erstellt wird.                   |
| [**MSFT \_ WmiThreadPoolDeleted**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpooldeleted)                 | Stellt eine Benachrichtigung bereit, wenn ein Thread im WMI-Ereignisuntersystem (ESS) gelöscht wird.                   |
| [**MSFT \_ WmiFilterEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterevent)                             | Übergeordnete Klasse für alle permanenten Ereignis-Consumerfilterereignisse.                                        |
| [**MSFT \_ WmiFilterActivated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilteractivated)                     | Definiert die erfolgreiche Aktivierung eines permanenten Ereignisverbraucherabonnementfilters.                |
| [**MSFT \_ WmiFilterDeactivated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterdeactivated)                 | Definiert die erfolgreiche Deaktivierung eines permanenten Consumerabonnementfilters.                    |



 

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

 

 
