---
description: Details zu Winsock-Ablaufverfolgungsereignissen.
ms.assetid: 246AE0BE-E8E2-4291-8BF4-577F889F055B
title: Winsock-Ablaufverfolgungsereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b2f36991a187d32359694956efcc7b7e3243ac17efd769db454848b5f87e5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821984"
---
# <a name="winsock-tracing-events"></a>Winsock-Ablaufverfolgungsereignisse

In diesem Abschnitt werden ausführliche Informationen zu bestimmten Winsock-Ablaufverfolgungsereignissen beschrieben.

Die Winsock-Ablaufverfolgung ist ein Problembehandlungsfeature, das in Binärdateien für den Einzelhandel aktiviert werden kann, um bestimmte Ereignisse Windows Sockets mit minimalem Mehraufwand zu verfolgen. Dieses Feature ermöglicht bessere Diagnosefunktionen für Entwickler und den Produktsupport. Die Winsock-Netzwerkereignisablaufverfolgung unterstützt die Ablaufverfolgung von Socketvorgängen für IPv4- und IPv6-Anwendungen. Die Winsock-Katalogänderungsablaufverfolgung unterstützt die Ablaufverfolgung von Änderungen, die von mehrschichtigen Dienstanbietern (Layered Service Providers, LSPs) am Winsock-Katalog vorgenommen wurden.

> [!Note]  
> Mehrschichtige Dienstanbieter sind veraltet. Verwenden Sie ab Windows 8 Windows Server 2012 [Filterplattform Windows Filterplattform](../fwp/windows-filtering-platform-start-page.md).

 

Die Winsock-Ablaufverfolgung verwendet die Ereignisablaufverfolgung für Windows (ETW), eine allgemeine, vom Betriebssystem bereitgestellte Hochgeschwindigkeits-Ablaufverfolgungseinrichtung. ETW bietet einen Ablaufverfolgungsmechanismus für Ereignisse, die sowohl von Benutzermodusanwendungen als auch von Kernelmodus-Gerätetreibern ausgelöst werden. ETW kann die Protokollierung dynamisch aktivieren und deaktivieren, wodurch es einfach ist, eine detaillierte Ablaufverfolgung in Produktionsumgebungen durchzuführen, ohne dass Neustarts oder Anwendungsneustarts erforderlich sind. Unterstützung für die Winsock-Ablaufverfolgung mit ETW wurde in Windows Vista und höher hinzugefügt. Allgemeine Informationen zu ETW finden Sie unter [Improve Debugging and Performance Tuning With ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).

Die folgende Liste enthält ausführliche Informationen zu jedem Winsock-Ablaufverfolgungsereignis. Klicken Sie auf den Ereignisnamen, um weitere Informationen zu einem Ereignis zu erhalten.



| Veranstaltungsname                                                            | BESCHREIBUNG                                                                               |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**AFD \_ EVENT \_ CREATE**](afd-event-create.md)                        | Winsock-Netzwerkablaufverfolgungsereignis für einen Socketerstellungsvorgang.                            |
| [**\_AFD-EREIGNIS \_ CLOSE**](afd-event-close.md)                          | Winsock-Netzwerkablaufverfolgungsereignis für socket- Close-Vorgang.                                 |
| [**WINSOCK \_ WS2HELP \_ LSP \_ INSTALL**](winsock-ws2help-lsp-install.md) | Winsock-Katalogänderungsereignis für einen mehrschichtigen Dienstanbieter -Installationsvorgang (LSP). |
| [**WINSOCK \_ WS2HELP \_ LSP \_ REMOVE**](winsock-ws2help-lsp-remove.md)   | Winsock-Katalogänderungsereignis für einen LSP-Entfernungsvorgang (Layered Service Provider).      |
| [**WINSOCK \_ WS2HELP \_ LSP \_ DISABLE**](winsock-ws2help-lsp-disable.md) | Winsock-Katalogänderungsereignis für einen mehrschichtigen Dienstanbieter (Layered Service Provider, LSP) – Deaktivierungsvorgang.      |
| [**WINSOCK \_ WS2HELP \_ LSP \_ RESET**](winsock-ws2help-lsp-reset.md)     | Winsock-Katalogänderungsereignis für einen Winsock-Katalogzurücksetzungsvorgang.                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessertes Debugging und Leistungsoptimierung mit ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Winsock-Ablaufverfolgung](winsock-tracing.md)
</dt> <dt>

[Winsock-Ablaufverfolgungsebenen](winsock-tracing-levels.md)
</dt> <dt>

[Steuerung der Winsock-Ablaufverfolgung](control-of-winsock-tracing.md)
</dt> <dt>

[Details zur Winsock Network-Ereignisablaufverfolgung](winsock-tracing-event-details.md)
</dt> <dt>

[Details zur Ablaufverfolgung für Winsock-Katalogänderung](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
