---
description: WMI stellt eine Reihe von Problembehandlungsklassen bereit, die Skripts und Anwendungen verwenden können, um Informationen zum internen WMI-Status während WMI-Kern- und Anbietervorgängen abzurufen.
ms.assetid: 631e0cce-0e83-42e5-a381-e96b1f70d6f9
ms.tgt_platform: multiple
title: WMI-Problembehandlungsklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9d3c5f1d40cd5da9e61ff289fc0b137ec7613ec8156fb0acc4f225e793a8407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049858"
---
# <a name="wmi-troubleshooting-classes"></a>WMI-Problembehandlungsklassen

WMI stellt eine Reihe von Problembehandlungsklassen bereit, die Skripts und Anwendungen verwenden können, um Informationen zum internen WMI-Status während WMI-Kern- und Anbietervorgängen abzurufen. Weitere Informationen zur WMI-Problembehandlung finden Sie unter [WMI-Problembehandlung](wmi-troubleshooting.md) und [Anbieterkonfiguration und Problembehandlungsklassen.](provider-configuration-and-troubleshooting-classes.md)

WMI verfügt über mehrere grundlegende Problembehandlungsklassen für WMI-Kern- und -Anbietervorgänge:

-   [**MSFT \_ \_ WmiProvider-Indikatoren**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-counters)

    Auf jedem Computersystem befindet sich nur eine dieser Klassen. Sie stellt die Anzahl verschiedener Arten von Anbietervorgängen auf diesem System bereit.

-   [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    Die Ereignisbehandlungsklassen werden von [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)abgeleitet. Abfragen dieser Klasse geben Instanzen von Ereignisklassen wie [**MSFT \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) oder [**MSFT \_ WmiProvider \_ CreateInstanceEnumAsyncEvent \_ Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post)zurück.

    Die folgende Liste enthält Links zu verschiedenen Kategorien von Ereignisklassen, die von [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)abgeleitet werden:

    -   [Problembehandlungsklassen für Anbieterereignisse](provider-event-troubleshooting-classes.md)
    -   [ConsumerProvider-Problembehandlungsklassen](consumerprovider-troubleshooting-classes.md)
    -   [Problembehandlungsklassen für WMI-Dienstereignisse](wmi-service-event-troubleshooting-classes.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Problembehandlung](wmi-troubleshooting.md)
</dt> <dt>

[Empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md)
</dt> </dl>

 

 
