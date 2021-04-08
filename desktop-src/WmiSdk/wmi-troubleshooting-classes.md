---
description: WMI stellt eine Reihe von Problem Behandlungs Klassen bereit, die von Skripts und Anwendungen verwendet werden können, um Informationen über den internen WMI-Status während der WMI-Kern-und Anbieter Vorgänge
ms.assetid: 631e0cce-0e83-42e5-a381-e96b1f70d6f9
ms.tgt_platform: multiple
title: WMI-Fehler Behebungs Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b3972ba59c80a1495916ab24a72f6e93bef8e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960795"
---
# <a name="wmi-troubleshooting-classes"></a>WMI-Fehler Behebungs Klassen

WMI stellt eine Reihe von Problem Behandlungs Klassen bereit, die von Skripts und Anwendungen verwendet werden können, um Informationen über den internen WMI-Status während der WMI-Kern-und Anbieter Vorgänge Weitere Informationen zur Problembehandlung für WMI finden Sie unter [WMI-Problem](wmi-troubleshooting.md) Behandlung und [Anbieter Konfiguration und Fehler Behebungs Klassen](provider-configuration-and-troubleshooting-classes.md).

WMI verfügt über mehrere grundlegende Problem Behandlungs Klassen für WMI-Kern-und-Anbieter Vorgänge:

-   [**MSFT \_ WMIProvider-Leistungsindikatoren \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-counters)

    Auf jedem Computersystem wird nur eine dieser Klassen gefunden. Es bietet eine Anzahl von verschiedenen Anbieter Vorgängen in diesem System.

-   [**MSFT \_ wmiselfevent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    Die Ereignis Fehler Behebungs Klassen werden von [**MSFT \_ wmiselfevent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)abgeleitet. Abfragen dieser Klasse geben Instanzen von Ereignis Klassen zurück, z. b. [**MSFT \_ wmithread poolcreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) oder [**MSFT \_ WMIProvider \_ kreateinstanceenumasyncevent \_ Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).

    In der folgenden Liste finden Sie Links zu verschiedenen Kategorien von Ereignis Klassen, die von [**MSFT \_ wmiselfevent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)abgeleitet werden:

    -   [Klassen zur Problembehandlung bei Anbieter Ereignissen](provider-event-troubleshooting-classes.md)
    -   [Consumerprovider-Fehler Behebungs Klassen](consumerprovider-troubleshooting-classes.md)
    -   [Fehler Behebungs Klassen für WMI-Dienst Ereignisse](wmi-service-event-troubleshooting-classes.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Problembehandlung](wmi-troubleshooting.md)
</dt> <dt>

[Empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md)
</dt> </dl>

 

 
