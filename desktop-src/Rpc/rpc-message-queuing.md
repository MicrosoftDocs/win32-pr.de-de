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
# <a name="rpc-message-queuing"></a><span data-ttu-id="09c30-104">RPC-Message Queuing</span><span class="sxs-lookup"><span data-stu-id="09c30-104">RPC Message Queuing</span></span>

<span data-ttu-id="09c30-105">Mit Message Queuing (MSMQ) können Benutzer unabhängig vom aktuellen Status der kommunizierenden Anwendungen und Systeme über Netzwerke und Systeme hinweg kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="09c30-105">Message Queuing (MSMQ) lets users communicate across networks and systems regardless of the current state of the communicating applications and systems.</span></span> <span data-ttu-id="09c30-106">Anwendungen senden und empfangen Nachrichten über Nachrichten Warteschlangen, die von MSMQ verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="09c30-106">Applications send and receive messages through message queues that MSMQ maintains.</span></span> <span data-ttu-id="09c30-107">Die Nachrichten Warteschlangen funktionieren auch dann weiterhin, wenn die Client-oder Serveranwendung nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09c30-107">The message queues continue to function even when the client or server application is not running.</span></span> <span data-ttu-id="09c30-108">Message Queueing bietet Folgendes:</span><span class="sxs-lookup"><span data-stu-id="09c30-108">Message queuing provides:</span></span>

-   <span data-ttu-id="09c30-109">**Asynchrones Messaging.**</span><span class="sxs-lookup"><span data-stu-id="09c30-109">**Asynchronous messaging.**</span></span> <span data-ttu-id="09c30-110">Mit dem asynchronen MSMQ-Messaging kann eine Client Anwendung eine Nachricht an einen Server senden und sofort zurückkehren, auch wenn der Zielcomputer oder das Serverprogramm nicht antwortet.</span><span class="sxs-lookup"><span data-stu-id="09c30-110">With MSMQ asynchronous messaging, a client application can send a message to a server and return immediately, even if the target computer or server program is not responding.</span></span>
-   <span data-ttu-id="09c30-111">**Garantierte Nachrichtenübermittlung.**</span><span class="sxs-lookup"><span data-stu-id="09c30-111">**Guaranteed message delivery.**</span></span> <span data-ttu-id="09c30-112">Wenn eine Anwendung über MSMQ eine Nachricht sendet, erreicht die Nachricht auch dann das Ziel, wenn die Zielanwendung nicht gleichzeitig ausgeführt wird oder die Netzwerke und Systeme offline sind.</span><span class="sxs-lookup"><span data-stu-id="09c30-112">When an application sends a message through MSMQ, the message will reach its destination even if the destination application is not running at the same time or the networks and systems are offline.</span></span>
-   <span data-ttu-id="09c30-113">**Routing und dynamische Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="09c30-113">**Routing and dynamic configuration.**</span></span> <span data-ttu-id="09c30-114">MSMQ bietet ein flexibles Routing über heterogene Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="09c30-114">MSMQ provides flexible routing over heterogeneous networks.</span></span> <span data-ttu-id="09c30-115">Die Konfiguration solcher Netzwerke kann ohne größere Änderungen an Systemen und Netzwerken selbst dynamisch geändert werden.</span><span class="sxs-lookup"><span data-stu-id="09c30-115">The configuration of such networks can be changed dynamically without any major changes to systems and networks themselves.</span></span>
-   <span data-ttu-id="09c30-116">**Verbindungsloses Messaging.**</span><span class="sxs-lookup"><span data-stu-id="09c30-116">**Connectionless messaging.**</span></span> <span data-ttu-id="09c30-117">Anwendungen, die MSMQ verwenden, müssen keine direkten Sitzungen mit Zielanwendungen einrichten.</span><span class="sxs-lookup"><span data-stu-id="09c30-117">Applications using MSMQ do not need to set up direct sessions with target applications.</span></span>
-   <span data-ttu-id="09c30-118">[Sicherheit:](security.md)</span><span class="sxs-lookup"><span data-stu-id="09c30-118">[Security](security.md).</span></span> <span data-ttu-id="09c30-119">MSMQ bietet eine sichere Kommunikation basierend auf der Windows-Sicherheit und der kryptografieapi (CryptoAPI) für die Verschlüsselung und digitale Signaturen.</span><span class="sxs-lookup"><span data-stu-id="09c30-119">MSMQ provides secure communication based on Windows security and the Cryptographic API (CryptoAPI) for encryption and digital signatures.</span></span>
-   <span data-ttu-id="09c30-120">**Priorisiertes Messaging.**</span><span class="sxs-lookup"><span data-stu-id="09c30-120">**Prioritized Messaging.**</span></span> <span data-ttu-id="09c30-121">MSMQ überträgt Nachrichten über Netzwerke basierend auf der Priorität und ermöglicht eine schnellere Kommunikation für kritische Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="09c30-121">MSMQ transfers messages across networks based on priority, allowing faster communication for critical applications.</span></span>

<span data-ttu-id="09c30-122">Microsoft RPC erweitert das Open Software Foundation – Data Communications equipment (OSF-DCE)-Modell für Remote Prozedur Aufrufe, indem verteilte Anwendungen die Verwendung von MSMQ als Transport ermöglichen und viele ihrer Features steuern können.</span><span class="sxs-lookup"><span data-stu-id="09c30-122">Microsoft RPC extends the Open Software Foundation–Data Communications Equipment (OSF-DCE) model for remote procedure calls by allowing distributed applications to use MSMQ as a transport and to control many of its features.</span></span> <span data-ttu-id="09c30-123">Diese Funktion ist sowohl für herkömmliche RPC-Anwendungen als auch **über die Schnitt** Stelle "Schnittstelle" für COM-Anwendungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="09c30-123">This functionality is available both to conventional RPC applications and, through the **IRPCOptions** interface, to COM applications.</span></span>

> [!Note]  
> <span data-ttu-id="09c30-124">RPC Message Queueing ist nur unter Windows 2000 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="09c30-124">RPC message queuing is available only on Windows 2000.</span></span> <span data-ttu-id="09c30-125">Spätere Versionen von Windows unterstützen RPC Message Queueing nicht.</span><span class="sxs-lookup"><span data-stu-id="09c30-125">Later versions of Windows do not support RPC message queuing.</span></span>

 

<span data-ttu-id="09c30-126">Die folgenden Themen bieten eine Übersicht über Message Queueing:</span><span class="sxs-lookup"><span data-stu-id="09c30-126">The following topics provide an overview of message queuing:</span></span>

-   [<span data-ttu-id="09c30-127">Übersicht über Message Queuing Services-Architektur</span><span class="sxs-lookup"><span data-stu-id="09c30-127">Overview of Message Queuing Services Architecture</span></span>](overview-of-message-queuing-services-architecture.md)
-   [<span data-ttu-id="09c30-128">Eigenschaften von Message und Message Queue</span><span class="sxs-lookup"><span data-stu-id="09c30-128">Message and Message Queue Properties</span></span>](message-and-message-queue-properties.md)
-   [<span data-ttu-id="09c30-129">Verwenden von MSMQ als RPC-Transport</span><span class="sxs-lookup"><span data-stu-id="09c30-129">Using MSMQ as an RPC Transport</span></span>](using-msmq-as-an-rpc-transport.md)
-   [<span data-ttu-id="09c30-130">System Anforderungen für RPC-Message \_ Queuinganwendungen</span><span class="sxs-lookup"><span data-stu-id="09c30-130">System Requirements for RPC-Message\_Queuing Applications</span></span>](system-requirements-for-rpc-message-queuing-applications.md)
-   [<span data-ttu-id="09c30-131">Entwickeln von RPC-Message Queuinganwendungen</span><span class="sxs-lookup"><span data-stu-id="09c30-131">Developing RPC-Message Queuing Applications</span></span>](developing-rpc-message-queuing-applications.md)
-   [<span data-ttu-id="09c30-132">MSMQ-Sicherheitsdienste</span><span class="sxs-lookup"><span data-stu-id="09c30-132">MSMQ Security Services</span></span>](msmq-security-services.md)

 

 




