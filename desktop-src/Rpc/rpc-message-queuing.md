---
title: RPC-Message Queuing
description: mit Message Queuing (MSMQ) können Benutzer unabhängig vom aktuellen Zustand der kommunizierenden Anwendungen und Systeme über Netzwerke und Systeme hinweg kommunizieren.
ms.assetid: f1c8665b-3754-4c2e-b3ac-bba1f4b329e1
keywords:
- Remoteprozeduraufruf RPC , beschrieben, Message Queuing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c44296068087dc2fd4423dbb3294c3c7a417e8a983ec958c2ad765ff87ea81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018380"
---
# <a name="rpc-message-queuing"></a>RPC-Message Queuing

mit Message Queuing (MSMQ) können Benutzer unabhängig vom aktuellen Zustand der kommunizierenden Anwendungen und Systeme über Netzwerke und Systeme hinweg kommunizieren. Anwendungen senden und empfangen Nachrichten über Nachrichtenwarteschlangen, die MSMQ verwaltet. Die Nachrichtenwarteschlangen funktionieren auch dann weiterhin, wenn die Client- oder Serveranwendung nicht ausgeführt wird. Message Queuing bietet Folgendes:

-   **Asynchrones Messaging.** Mit dem asynchronen MSMQ-Messaging kann eine Clientanwendung eine Nachricht an einen Server senden und sofort zurückgeben, auch wenn der Zielcomputer oder das Serverprogramm nicht reagiert.
-   **Garantierte Nachrichtenübermittlung.** Wenn eine Anwendung eine Nachricht über MSMQ sendet, erreicht die Nachricht auch dann ihr Ziel, wenn die Zielanwendung nicht gleichzeitig ausgeführt wird oder die Netzwerke und Systeme offline sind.
-   **Routing und dynamische Konfiguration.** MSMQ bietet flexibles Routing über heterogene Netzwerke. Die Konfiguration solcher Netzwerke kann dynamisch ohne größere Änderungen an Systemen und Netzwerken selbst geändert werden.
-   **Verbindungsloses Messaging.** Anwendungen, die MSMQ verwenden, müssen keine direkten Sitzungen mit Zielanwendungen einrichten.
-   [Sicherheit](security.md). MSMQ bietet eine sichere Kommunikation basierend auf Windows Sicherheit und kryptografischer API (CryptoAPI) für Verschlüsselung und digitale Signaturen.
-   **Priorisiertes Messaging.** MSMQ überträgt Nachrichten basierend auf der Priorität netzwerkübergreifend, sodass kritische Anwendungen schneller kommunizieren können.

Microsoft RPC erweitert das OSF-DCE-Modell (Open Software Foundation–Data Communications Equipment) für Remoteprozeduraufrufe, indem verteilten Anwendungen ermöglicht wird, MSMQ als Transport zu verwenden und viele seiner Features zu steuern. Diese Funktionalität ist sowohl für herkömmliche RPC-Anwendungen als auch über die **IRPCOptions-Schnittstelle** für COM-Anwendungen verfügbar.

> [!Note]  
> RPC-Nachrichtenwarteschlangen sind nur auf Windows 2000 verfügbar. Höhere Versionen von Windows unterstützen rpc message queuing nicht.

 

Die folgenden Themen bieten eine Übersicht über Message Queuing:

-   [Übersicht über Message Queuing Services-Architektur](overview-of-message-queuing-services-architecture.md)
-   [Nachrichten- und Nachrichtenwarteschlangeneigenschaften](message-and-message-queue-properties.md)
-   [Verwenden von MSMQ als RPC-Transport](using-msmq-as-an-rpc-transport.md)
-   [Systemanforderungen für RPC-Message \_ Queuing-Anwendungen](system-requirements-for-rpc-message-queuing-applications.md)
-   [Entwickeln von RPC-Message Queuing-Anwendungen](developing-rpc-message-queuing-applications.md)
-   [MSMQ-Sicherheitsdienste](msmq-security-services.md)

 

 




