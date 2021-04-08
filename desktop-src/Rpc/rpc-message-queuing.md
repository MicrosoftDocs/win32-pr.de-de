---
title: RPC-Message Queuing
description: Mit Message Queuing (MSMQ) können Benutzer unabhängig vom aktuellen Status der kommunizierenden Anwendungen und Systeme über Netzwerke und Systeme hinweg kommunizieren.
ms.assetid: f1c8665b-3754-4c2e-b3ac-bba1f4b329e1
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, Message Queueing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b72e9e35ec2aa1cc440c0d0356c681c4fe8548c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037376"
---
# <a name="rpc-message-queuing"></a>RPC-Message Queuing

Mit Message Queuing (MSMQ) können Benutzer unabhängig vom aktuellen Status der kommunizierenden Anwendungen und Systeme über Netzwerke und Systeme hinweg kommunizieren. Anwendungen senden und empfangen Nachrichten über Nachrichten Warteschlangen, die von MSMQ verwaltet werden. Die Nachrichten Warteschlangen funktionieren auch dann weiterhin, wenn die Client-oder Serveranwendung nicht ausgeführt wird. Message Queueing bietet Folgendes:

-   **Asynchrones Messaging.** Mit dem asynchronen MSMQ-Messaging kann eine Client Anwendung eine Nachricht an einen Server senden und sofort zurückkehren, auch wenn der Zielcomputer oder das Serverprogramm nicht antwortet.
-   **Garantierte Nachrichtenübermittlung.** Wenn eine Anwendung über MSMQ eine Nachricht sendet, erreicht die Nachricht auch dann das Ziel, wenn die Zielanwendung nicht gleichzeitig ausgeführt wird oder die Netzwerke und Systeme offline sind.
-   **Routing und dynamische Konfiguration.** MSMQ bietet ein flexibles Routing über heterogene Netzwerke. Die Konfiguration solcher Netzwerke kann ohne größere Änderungen an Systemen und Netzwerken selbst dynamisch geändert werden.
-   **Verbindungsloses Messaging.** Anwendungen, die MSMQ verwenden, müssen keine direkten Sitzungen mit Zielanwendungen einrichten.
-   [Sicherheit:](security.md) MSMQ bietet eine sichere Kommunikation basierend auf der Windows-Sicherheit und der kryptografieapi (CryptoAPI) für die Verschlüsselung und digitale Signaturen.
-   **Priorisiertes Messaging.** MSMQ überträgt Nachrichten über Netzwerke basierend auf der Priorität und ermöglicht eine schnellere Kommunikation für kritische Anwendungen.

Microsoft RPC erweitert das Open Software Foundation – Data Communications equipment (OSF-DCE)-Modell für Remote Prozedur Aufrufe, indem verteilte Anwendungen die Verwendung von MSMQ als Transport ermöglichen und viele ihrer Features steuern können. Diese Funktion ist sowohl für herkömmliche RPC-Anwendungen als auch **über die Schnitt** Stelle "Schnittstelle" für COM-Anwendungen verfügbar.

> [!Note]  
> RPC Message Queueing ist nur unter Windows 2000 verfügbar. Spätere Versionen von Windows unterstützen RPC Message Queueing nicht.

 

Die folgenden Themen bieten eine Übersicht über Message Queueing:

-   [Übersicht über Message Queuing Services-Architektur](overview-of-message-queuing-services-architecture.md)
-   [Eigenschaften von Message und Message Queue](message-and-message-queue-properties.md)
-   [Verwenden von MSMQ als RPC-Transport](using-msmq-as-an-rpc-transport.md)
-   [System Anforderungen für RPC-Message \_ Queuinganwendungen](system-requirements-for-rpc-message-queuing-applications.md)
-   [Entwickeln von RPC-Message Queuinganwendungen](developing-rpc-message-queuing-applications.md)
-   [MSMQ-Sicherheitsdienste](msmq-security-services.md)

 

 




