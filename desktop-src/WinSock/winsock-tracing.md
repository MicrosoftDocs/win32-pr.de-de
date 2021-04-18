---
description: Winsock-Ablauf Verfolgung
ms.assetid: 0c430fc2-28e7-4537-a887-4c36d24fedee
title: Winsock-Ablauf Verfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803be6220d4d2d440811033786b0f043fab0ff9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343293"
---
# <a name="winsock-tracing"></a>Winsock-Ablauf Verfolgung

## <a name="introduction"></a>Einführung

Die Winsock-Ablauf Verfolgung ist ein Feature zur Problembehandlung, das in Binärdateien im Einzelhandel aktiviert werden kann, um bestimmte Windows Socket-Ereignisse mit minimalem mehr Aufwand Das Ziel, Windows Sockets eine Einzelhandels Ablauf Verfolgung hinzuzufügen, besteht darin, für Entwickler und den Produktsupport bessere Diagnosefunktionen zu ermöglichen. Die Winsock-Netzwerk Ereignis Ablauf Verfolgung unterstützt Ablaufverfolgungs-Socketvorgänge für IPv4-und IPv6 Die Ablauf Verfolgung der Winsock-Katalog Änderung unterstützt die Ablauf Verfolgung von Änderungen, die an den Winsock-Katalog durch mehrstufige Dienstanbieter (LSPs Die Winsock-Ablauf Verfolgung wird unter Windows Vista und höher unterstützt.

> [!Note]  
> Mehrstufige Dienstanbieter sind veraltet. Ab Windows 8 und Windows Server 2012 verwenden Sie die [Windows-Filter Plattform](../fwp/windows-filtering-platform-start-page.md).

 

Wenn bei einem Socket ein unerwarteter Fehler auftritt, wird der Fehlercode zurückgegeben, um das Problem zu diagnostizieren. Der zurückgegebene Fehlercode erläutert häufig nicht, warum der Fehler aufgetreten ist. Dies gilt insbesondere, wenn der Fehler vom zugrunde liegenden Netzwerk Transport initiiert wird. Die Winsock-Ablauf Verfolgung bietet eine ausführlichere Ablauf Verfolgungs Ebene, die zusätzliche Informationen protokollieren kann, um Puffer Beschädigungen und schlecht geschriebene Anwendungen abzufangen.

Die Winsock-Ablauf Verfolgung verwendet die Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw), eine allgemeine, hoch Geschwindigkeits Ablauf Verfolgungs Funktion des Betriebssystems. Mit einem in dem Kernel implementierten Puffer-und Protokollierungs Mechanismus stellt ETW einen Ablauf Verfolgungs Mechanismus für Ereignisse bereit, die von Anwendungen im Benutzermodus und im Kernel Modus-Gerätetreibern ausgelöst werden. Außerdem haben Sie mit etw die Möglichkeit, die Protokollierung dynamisch zu aktivieren und zu deaktivieren, sodass Sie die detaillierte Ablauf Verfolgung in Produktionsumgebungen ohne Neustarts oder Anwendungs Neustarts problemlos durchführen können. Der Protokollierungs Mechanismus verwendet Puffer, die von einem asynchronen Writer-Thread auf den Datenträger geschrieben werden. Dadurch können umfangreiche Server Anwendungen Ereignisse mit minimaler Störung schreiben. Etw wurde erstmals unter Windows 2000 eingeführt. Unterstützung für die Winsock-Ablauf Verfolgung mit etw wurde unter Windows Vista und höher hinzugefügt. Allgemeine Informationen zu etw finden Sie unter verbessertes [Debugging und Leistungsoptimierung mit etw](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).

Die Winsock-Ablauf Verfolgung kann nur auf Betriebssystemebene für alle Prozesse und Threads aktiviert werden, die auf einem Computer ausgeführt werden. Die Winsock-Ablauf Verfolgung kann derzeit nur für einen einzelnen Prozess oder Thread aktiviert werden. Wenn die Winsock-Netzwerk Ereignis Ablauf Verfolgung aktiviert ist, werden alle Socketanwendungen (sowohl IPv4 als auch IPv6) auf einem Computer nachverfolgt.

In den folgenden Themen wird die Winsock-Ablauf Verfolgung ausführlicher beschrieben:

-   [Winsock-Ablauf Verfolgungs Ebenen](winsock-tracing-levels.md)
-   [Kontrolle über die Winsock-Ablauf Verfolgung](control-of-winsock-tracing.md)
-   [Details der Winsock-Netzwerk Ereignis Ablauf Verfolgung](winsock-tracing-event-details.md)
-   [Details zur Änderung der Winsock-Katalog Änderung](winsock-layered-service-provider-tracing-event-details.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessertes Debugging und Leistungsoptimierung mit ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Debug-und Ablauf Verfolgungs Funktionen](debug-and-trace-facilities-2.md)
</dt> </dl>

 

 
