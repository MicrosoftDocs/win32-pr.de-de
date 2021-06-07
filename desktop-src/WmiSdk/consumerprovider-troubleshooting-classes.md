---
description: In der folgenden Tabelle sind die Problembehandlungsereignisklassen aufgeführt, die von Ereignisverbraucheranbietervorgängen generiert werden.
ms.assetid: dd685a41-8eae-4977-ab94-902dd8dddcc9
ms.tgt_platform: multiple
title: ConsumerProvider-Problembehandlungsklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 740b8c0eb1884181fa84efe26e0611dda4b1712f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443611"
---
# <a name="consumerprovider-troubleshooting-classes"></a>ConsumerProvider-Problembehandlungsklassen

In der folgenden Tabelle sind die Problembehandlungsereignisklassen aufgeführt, die von [*Ereignisverbraucheranbietervorgängen*](gloss-e.md) generiert werden.

Sie können die abstrakte Basisklasse [**MSFT \_ ProviderEvent-Benachrichtigungen**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) abonnieren, um alle folgenden Ereignisse abzurufen.



| Ereignis                                                                                                | BESCHREIBUNG                                                                                |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**MSFT \_ WmiProviderEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiproviderevent)                               | Übergeordnete Klasse für alle Consumeranbieterereignisse.                                  |
| [**MSFT \_ WmiConsumerProviderLoaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderloaded)             | Definiert die erfolgreiche Aktivierung des COM-Objekts des Ereignisverbraucheranbieters.    |
| [**MSFT \_ WmiConsumerProviderUnloaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderunloaded)         | Definiert die erfolgreiche Deaktivierung des COM-Objekts des Ereignisverbraucheranbieters.  |
| [**MSFT \_ WmiConsumerProviderSinkLoaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkloaded)     | Definiert die erfolgreiche Aktivierung des Senkenobjekts des Ereignisverbraucheranbieters.   |
| [**MSFT \_ WmiConsumerProviderSinkUnloaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkunloaded) | Definiert die erfolgreiche Deaktivierung des Senkenobjekts des Ereignisverbraucheranbieters. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Problembehandlung](wmi-troubleshooting.md)
</dt> <dt>

WMI-Problembehandlung
</dt> <dt>

[Empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md)
</dt> </dl>

 

 
