---
description: Bewährte Methoden zum Minimieren von nicht reagierenden Diensten
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Bewährte Methoden zum Minimieren von nicht reagierenden Diensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90416e8256383e16fd78c436dfaa8d6a2186c540
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087998"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a>Bewährte Methoden zum Minimieren von nicht reagierenden Diensten

## <a name="affected-platform"></a>Betroffene Plattform

 **Clients** – Windows Vista \| Windows 7  

## <a name="description"></a>BESCHREIBUNG

Nicht reagierende Dienste können zu Timeouts, beendeten Sitzungen und sogar zu Datenverlusten führen. Die Verwendung bewährter Methoden kann das Auftreten nicht reagierender Dienste erheblich reduzieren.

## <a name="best-practices"></a>Bewährte Methoden

Stellen Sie sicher, dass Ihre Anwendungen und alle abhängigen Dienste und Treiber auf Benachrichtigungen zum Ein- und Herunterfahren des Systems reagieren.

-   Alle Anwendungen sollten sofort und angemessen auf Meldungen zum Herunterfahren reagieren, z. B. WM \_ QUERYENDSESSION und WM \_ ENDSESSION, die darauf hinweisen, dass ein Herunterfahren ausgeführt wird.
-   Alle Dienste sollten sofort auf Benachrichtigungen zum Herunterfahren des SCM reagieren. Wenn sie dies nicht tun, behandelt der Computer sie als nicht reagierend, initiiert ein Time out von 20 Sekunden und beendet sie, wodurch die Möglichkeit besteht, dass Daten verloren gehen. Dies erhöht auch die Zeit zum Herunterfahren eines Computers um 20 Sekunden.
-   Alle Dienste mit Kernelgerätetreiberabhängigkeiten sollten in \_ ihren DispatchShutdown-Routinen umgehend und entsprechend auf die IRP MJ \_ SHUTDOWN-Benachrichtigung reagieren.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

<dl>

[Windows Performance Toolkit](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



