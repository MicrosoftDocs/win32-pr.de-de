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

Die Winsock-Ablaufverfolgung ist ein Problembehandlungsfeature, das in Binärdateien für den Einzelhandel aktiviert werden kann, um bestimmte Ereignisse Windows Sockets mit minimalem Mehraufwand zu verfolgen. Das Ziel des Hinzufügens der Einzelhandelsablaufverfolgung zu Windows Sockets besteht im Ermöglichen besserer Diagnosefunktionen für Entwickler und Produktsupport. Die Winsock-Netzwerkereignisablaufverfolgung unterstützt die Ablaufverfolgung von Socketvorgängen für IPv4- und IPv6-Anwendungen. Die Winsock-Katalogänderungsablaufverfolgung unterstützt die Ablaufverfolgung von Änderungen, die von mehrschichtigen Dienstanbietern (Layered Service Providers, LSPs) am Winsock-Katalog vorgenommen wurden. Die Winsock-Ablaufverfolgung wird unter Windows Vista und höher unterstützt.

> [!Note]  
> Mehrschichtige Dienstanbieter sind veraltet. Verwenden Sie ab Windows 8 Windows Server 2012 Filterplattform [Windows Filterplattform](../fwp/windows-filtering-platform-start-page.md).

 

Wenn bei einem Socket ein unerwarteter Fehler auftritt, ist der zurückgegebene Fehlercode der wichtigste Hinweis zur Diagnose des Problems. Sehr häufig erklärt der zurückgegebene Fehlercode nicht, warum der Fehler aufgetreten ist, insbesondere wenn der Fehler vom zugrunde liegenden Netzwerktransport initiiert wird. Die Winsock-Ablaufverfolgung bietet eine ausführlichere Ablaufverfolgungsebene, mit der zusätzliche Informationen protokolliert werden können, um Pufferbeschädigungen und schlecht geschriebene Anwendungen zu abfangen.

Die Winsock-Ablaufverfolgung verwendet die Ereignisablaufverfolgung für Windows (ETW), eine allgemeine, vom Betriebssystem bereitgestellte Hochgeschwindigkeits-Ablaufverfolgungseinrichtung. Mithilfe eines im Kernel implementierten Pufferungs- und Protokollierungsmechanismus bietet ETW einen Ablaufverfolgungsmechanismus für Ereignisse, die sowohl von Benutzermodusanwendungen als auch von Gerätetreibern im Kernelmodus ausgelöst werden. Darüber hinaus bietet ETW Ihnen die Möglichkeit, die Protokollierung dynamisch zu aktivieren und zu deaktivieren, wodurch es einfach ist, eine detaillierte Ablaufverfolgung in Produktionsumgebungen durchzuführen, ohne dass Neustarts oder Neustarts der Anwendung erforderlich sind. Der Protokollierungsmechanismus verwendet Puffer, die von einem asynchronen Writerthread auf den Datenträger geschrieben werden. Dies ermöglicht es großen Serveranwendungen, Ereignisse mit minimaler Beeinträchtigung zu schreiben. ETW wurde erstmals ab Windows 2000 eingeführt. Unterstützung für die Winsock-Ablaufverfolgung mit ETW wurde in Windows Vista und höher hinzugefügt. Allgemeine Informationen zu ETW finden Sie unter [Improve Debugging and Performance Tuning With ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).

Die Winsock-Ablaufverfolgung kann nur auf Betriebssystemebene für alle Prozesse und Threads aktiviert werden, die auf einem Computer ausgeführt werden. Die Winsock-Ablaufverfolgung kann derzeit nicht nur für einen einzelnen Prozess oder Thread aktiviert werden. Wenn die Winsock-Netzwerkereignisablaufverfolgung aktiviert ist, werden alle Socketanwendungen (sowohl IPv4 als auch IPv6) auf einem Computer nachverfolgt.

In den folgenden Themen wird die Winsock-Ablaufverfolgung ausführlicher beschrieben:

-   [Winsock-Ablaufverfolgungsebenen](winsock-tracing-levels.md)
-   [Steuerung der Winsock-Ablaufverfolgung](control-of-winsock-tracing.md)
-   [Details zur Winsock Network-Ereignisablaufverfolgung](winsock-tracing-event-details.md)
-   [Details zur Ablaufverfolgung für Winsock-Katalogänderung](winsock-layered-service-provider-tracing-event-details.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessertes Debugging und Leistungsoptimierung mit ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Debug- und Ablaufverfolgungs-Funktionen](debug-and-trace-facilities-2.md)
</dt> </dl>

 

 
