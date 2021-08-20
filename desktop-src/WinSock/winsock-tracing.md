---
description: Winsock-Ablaufverfolgung
ms.assetid: 0c430fc2-28e7-4537-a887-4c36d24fedee
title: Winsock-Ablaufverfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb2d9593f4c2cea47e722075f1611151fb276cdf2646a2c9898a9c8d7d156098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321670"
---
# <a name="winsock-tracing"></a>Winsock-Ablaufverfolgung

## <a name="introduction"></a>Einführung

Die Winsock-Ablaufverfolgung ist ein Feature zur Problembehandlung, das in Binärdateien für den Einzelhandel aktiviert werden kann, um bestimmte Windows Socketereignisse mit minimalem Aufwand nachzuverfolgen. Das Ziel des Hinzufügens der Einzelhandelsablaufverfolgung zu Windows Sockets besteht darin, bessere Diagnosefunktionen für Entwickler und Produktsupport zu ermöglichen. Die Winsock-Netzwerkereignisablaufverfolgung unterstützt die Ablaufverfolgung von Socketvorgängen für IPv4- und IPv6-Anwendungen. Die Ablaufverfolgung für Winsock-Katalogänderungen unterstützt die Ablaufverfolgung von Änderungen, die von mehrstufigen Dienstanbietern (LSPs) am Winsock-Katalog vorgenommen wurden. Die Winsock-Ablaufverfolgung wird auf Windows Vista und höher unterstützt.

> [!Note]  
> Mehrstufige Dienstanbieter sind veraltet. Verwenden Sie ab Windows 8 und Windows Server 2012 [Windows Filterplattform](../fwp/windows-filtering-platform-start-page.md).

 

Wenn ein unerwarteter Fehler an einem Socket auftritt, ist der hauptanfällige Hinweis zum Diagnostizieren des Problems der zurückgegebene Fehlercode. Sehr häufig erklärt der zurückgegebene Fehlercode nicht, warum der Fehler aufgetreten ist, insbesondere wenn der Fehler vom zugrunde liegenden Netzwerktransport initiiert wird. Die Winsock-Ablaufverfolgung bietet eine ausführlichere Ablaufverfolgungsebene, die zusätzliche Informationen protokollieren kann, um Pufferbeschädigungen und schlecht geschriebene Anwendungen abzufangen.

Die Winsock-Ablaufverfolgung verwendet die Ereignisablaufverfolgung für Windows (ETW), eine allgemeine Hochgeschwindigkeits-Ablaufverfolgungsfunktion, die vom Betriebssystem bereitgestellt wird. Mithilfe eines Pufferungs- und Protokollierungsmechanismus, der im Kernel implementiert ist, stellt ETW einen Ablaufverfolgungsmechanismus für Ereignisse bereit, die sowohl von Benutzermodusanwendungen als auch von Gerätetreibern im Kernelmodus ausgelöst werden. Darüber hinaus bietet IHNEN ETW die Möglichkeit, die Protokollierung dynamisch zu aktivieren und zu deaktivieren, sodass sie problemlos eine detaillierte Ablaufverfolgung in Produktionsumgebungen durchführen kann, ohne dass Neustarts oder Neustarts der Anwendung erforderlich sind. Der Protokollierungsmechanismus verwendet Puffer, die von einem asynchronen Writerthread auf den Datenträger geschrieben werden. Dies ermöglicht umfangreichen Serveranwendungen das Schreiben von Ereignissen mit minimaler Beeinträchtigung. ETW wurde erstmals am Windows 2000 eingeführt. Unterstützung für die Winsock-Ablaufverfolgung mit ETW wurde auf Windows Vista und höher hinzugefügt. Allgemeine Informationen zu ETW finden Sie unter [Improve Debugging and Performance Tuning With ETW (Verbessern des Debuggens und der Leistungsoptimierung mit ETW).](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)

Die Winsock-Ablaufverfolgung kann nur auf Betriebssystemebene für alle Prozesse und Threads aktiviert werden, die auf einem Computer ausgeführt werden. Die Winsock-Ablaufverfolgung kann derzeit nicht nur für einen einzelnen Prozess oder Thread aktiviert werden. Wenn die Winsock-Netzwerkereignisablaufverfolgung aktiviert ist, werden alle Socketanwendungen (sowohl IPv4 als auch IPv6) auf einem Computer nachverfolgt.

In den folgenden Themen wird die Winsock-Ablaufverfolgung ausführlicher beschrieben:

-   [Winsock-Ablaufverfolgungsebenen](winsock-tracing-levels.md)
-   [Steuerung der Winsock-Ablaufverfolgung](control-of-winsock-tracing.md)
-   [Details zur Ablaufverfolgung von Winsock-Netzwerkereignissen](winsock-tracing-event-details.md)
-   [Details zur Ablaufverfolgung von Winsock-Katalogänderungen](winsock-layered-service-provider-tracing-event-details.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessertes Debugging und Leistungsoptimierung mit ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Debug- und Ablaufverfolgungs-Funktionen](debug-and-trace-facilities-2.md)
</dt> </dl>

 

 
