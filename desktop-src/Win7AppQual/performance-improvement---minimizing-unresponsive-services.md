---
description: .
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Bewährte Methoden zum minimieren nicht reagierender Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e1fbad7fe60c4165ebb97847c303482314f68e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868595"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a>Bewährte Methoden zum minimieren nicht reagierender Dienste

## <a name="affected-platform"></a>Betroffene Plattform

 **Clients** – Windows Vista \| Windows 7  

## <a name="description"></a>BESCHREIBUNG

Nicht reagierende Dienste können zu Timeouts, beendeten Sitzungen und sogar zum Verlust von Daten führen. Die Verwendung bewährter Methoden kann das Vorkommen nicht reagierender Dienste erheblich verringern.

## <a name="best-practices"></a>Bewährte Methoden

Stellen Sie sicher, dass Ihre Anwendungen und alle abhängigen Dienste und Treiber auf die Systemleistung und das Herunterfahren von Benachrichtigungen reagieren.

-   Alle Anwendungen sollten umgehend und ordnungsgemäß auf das Herunterfahren von Nachrichten wie WM \_ queryendsession und WM \_ EndSession reagieren, die darauf hinweisen, dass ein Herunterfahren ausgeführt wird.
-   Alle Dienste sollten umgehend auf SCM-Shutdown-Benachrichtigungen reagieren. Wenn dies nicht der Fall ist, werden Sie vom Computer als nicht reagierend behandelt, und es wird ein Timeout von 20 Sekunden initiiert, und der Computer wird beendet, und es wird die Gefahr verlorener Daten geöffnet. Dadurch wird dem Herunterfahren eines Computers auch 20 Sekunden hinzugefügt.
-   Alle Dienste, die über Kernel-Gerätetreiber Abhängigkeiten verfügen, sollten umgehend und ordnungsgemäß auf die Benachrichtigung zum Herunterfahren von "Iran" \_ \_ in ihren dispatchshutdown-Routinen reagieren

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

<dl>

[Windows Performance Toolkit](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



