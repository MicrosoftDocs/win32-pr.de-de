---
description: In der folgenden Tabelle sind Problem Behandlungs Ereignis Klassen aufgelistet, die von Ereignisconsumer-Anbieter Vorgängen generiert werden.
ms.assetid: dd685a41-8eae-4977-ab94-902dd8dddcc9
ms.tgt_platform: multiple
title: Consumerprovider-Fehler Behebungs Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 536c23fb35ca6a4d2146cf87782768c51f37a6ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357919"
---
# <a name="consumerprovider-troubleshooting-classes"></a>Consumerprovider-Fehler Behebungs Klassen

In der folgenden Tabelle sind Problem Behandlungs Ereignis Klassen aufgelistet, die von [*Ereignisconsumer-Anbieter*](gloss-e.md) Vorgängen generiert werden.

Sie können die abstrakte Basisklasse " [**MSFT \_ providerevent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) "-Benachrichtigungen abonnieren, um alle der folgenden Ereignisse zu erhalten.



|                                                                                                 |                                                                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**MSFT \_ wmiproviderevent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiproviderevent)                               | Übergeordnete Klasse für alle Consumer-Anbieter Ereignisse.                                  |
| [**MSFT \_ wmiconsumerproviderloaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderloaded)             | Definiert die erfolgreiche Aktivierung des COM-Objekts des Ereignisconsumeranbieters.    |
| [**MSFT \_ wmiconsumerproviderentladen**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderunloaded)         | Definiert die erfolgreiche initiaktivierung des COM-Objekts des Ereignisconsumeranbieters.  |
| [**MSFT \_ wmiconsumerprovidersinkloaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkloaded)     | Definiert die erfolgreiche Aktivierung des Senkenobjekts des Ereignisconsumeranbieters.   |
| [**MSFT \_ wmiconsumerprovidersinkunloaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkunloaded) | Definiert die erfolgreiche initiaktivierung des Senkenobjekts des ereignishandleranbieters. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Problembehandlung](wmi-troubleshooting.md)
</dt> <dt>

WMI-Problembehandlung
</dt> <dt>

[Empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md)
</dt> </dl>

 

 
