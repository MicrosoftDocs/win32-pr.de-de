---
description: Bewährte Methoden zum Minimieren nicht reagierender Dienste
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Bewährte Methoden zum Minimieren nicht reagierender Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cf3f37620fc00834b3c25a92292c889785818c2810cac7c12e788de8bf1fb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994850"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a>Bewährte Methoden zum Minimieren nicht reagierender Dienste

## <a name="affected-platform"></a>Betroffene Plattform

 **Clients** – Windows Vista \| Windows 7  

## <a name="description"></a>BESCHREIBUNG

Nicht reagierende Dienste können zu Timeouts, beendeten Sitzungen und sogar verlorenen Daten führen. Die Verwendung bewährter Methoden kann das Auftreten nicht reagierender Dienste deutlich reduzieren.

## <a name="best-practices"></a>Empfehlungen

Stellen Sie sicher, dass Ihre Anwendungen und alle abhängigen Dienste und Treiber auf Benachrichtigungen zu Systemleistung und Herunterfahren reagieren.

-   Alle Anwendungen sollten umgehend und angemessen auf Meldungen zum Herunterfahren reagieren, z. B. WM QUERYENDSESSION und WM ENDSESSION, die darauf hinweisen, dass ein \_ \_ Herunterfahren ausgeführt wird.
-   Alle Dienste sollten sofort auf Benachrichtigungen zum Herunterfahren des SCM reagieren. Wenn dies nicht der Fall ist, behandelt der Computer sie als nicht reagierend und initiiert ein 20-Sekunden-Time out und beendet sie, was die Möglichkeit eines Verlusts von Daten eröffnet. Dadurch wird auch die Zeit zum Herunterfahren eines Computers um 20 Sekunden erhöht.
-   Alle Dienste, die über Kernelgerätetreiberabhängigkeiten verfügen, sollten umgehend und angemessen auf IRP \_ MJ \_ SHUTDOWN-Benachrichtigungen in ihren DispatchShutdown-Routinen reagieren.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

<dl>

[Windows Performance Toolkit](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



