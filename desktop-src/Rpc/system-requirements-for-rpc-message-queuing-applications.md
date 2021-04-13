---
title: System Anforderungen für RPC-Message Queuinganwendungen
description: Damit der Nachrichten Warteschlangen-Transport in einer RPC-Client/Server-Anwendung verwendet werden kann, müssen auf dem Server und den Client Computern die geeignete Betriebssystem Plattform und Message Queuing Software installiert sein.
ms.assetid: f90318a6-0be6-4e1a-a1a5-1709808b5d3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1274c888506a6868eb7ded5ba96c5f1ea8dc8b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390830"
---
# <a name="system-requirements-for-rpc-message-queuing-applications"></a><span data-ttu-id="7b191-103">System Anforderungen für RPC-Message Queuinganwendungen</span><span class="sxs-lookup"><span data-stu-id="7b191-103">System Requirements for RPC-Message Queuing Applications</span></span>

<span data-ttu-id="7b191-104">Damit der Nachrichten Warteschlangen-Transport in einer RPC-Client/Server-Anwendung verwendet werden kann, müssen auf dem Server und den Client Computern die geeignete Betriebssystem Plattform und Message Queuing Software installiert sein.</span><span class="sxs-lookup"><span data-stu-id="7b191-104">To use the message-queuing transport in an RPC client/server application, the server and client computers must have the appropriate operating system platform and Message Queuing software installed.</span></span>

<span data-ttu-id="7b191-105">Folgende Anforderungen gelten für Server Computer:</span><span class="sxs-lookup"><span data-stu-id="7b191-105">Requirements for server computers are:</span></span>

-   <span data-ttu-id="7b191-106">Microsoft Windows Server 2003, Windows XP oder Windows 2000 oder höher.</span><span class="sxs-lookup"><span data-stu-id="7b191-106">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later.</span></span>
-   <span data-ttu-id="7b191-107">SQL Server Version 6,5 oder höher.</span><span class="sxs-lookup"><span data-stu-id="7b191-107">SQL Server version 6.5 or later.</span></span>
-   <span data-ttu-id="7b191-108">Message Queuing primärer Enterprise Controller oder primärer Standort Controller.</span><span class="sxs-lookup"><span data-stu-id="7b191-108">Message Queuing Primary Enterprise Controller or Primary Site Controller.</span></span>
-   <span data-ttu-id="7b191-109">Serverseitige RPC-Transport-dll (RpcMqSvr.dll).</span><span class="sxs-lookup"><span data-stu-id="7b191-109">RPC server-side transport DLL (RpcMqSvr.dll).</span></span>

<span data-ttu-id="7b191-110">Anforderungen für Client Computer:</span><span class="sxs-lookup"><span data-stu-id="7b191-110">Requirements for client computers are:</span></span>

-   <span data-ttu-id="7b191-111">Microsoft Windows Server 2003, Windows XP oder Windows 2000 oder höher.</span><span class="sxs-lookup"><span data-stu-id="7b191-111">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later.</span></span>
-   <span data-ttu-id="7b191-112">Microsoft Message Queuing-Client.</span><span class="sxs-lookup"><span data-stu-id="7b191-112">Microsoft Message Queuing Client.</span></span>
-   <span data-ttu-id="7b191-113">Client seitige RPC-Transport-dll (RpcMqCl.dll).</span><span class="sxs-lookup"><span data-stu-id="7b191-113">RPC client-side transport DLL (RpcMqCl.dll).</span></span>

<span data-ttu-id="7b191-114">Wenn die MSMQ-Komponenten auf dem Client-und dem Server Computer installiert sind, werden die System Registrierungen automatisch so konfiguriert, dass Sie das [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq) -Nachrichten Warteschlangen-Transportprotokoll für Remote Prozedur Aufrufe enthalten.</span><span class="sxs-lookup"><span data-stu-id="7b191-114">When the MSMQ components are installed on the client and server computers, the system registries are automatically configured to include the [ncadg\_mq](/windows/desktop/Midl/ncadg-mq) message-queuing transport protocol for remote procedure calls.</span></span>

<span data-ttu-id="7b191-115">Zum Erstellen der RPC-MSMQ-Anwendung benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7b191-115">To build your RPC-MSMQ application you need the following:</span></span>

-   <span data-ttu-id="7b191-116">Microsoft Windows Server 2003, Windows XP oder Windows 2000 oder höher</span><span class="sxs-lookup"><span data-stu-id="7b191-116">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later</span></span>
-   <span data-ttu-id="7b191-117">Mittel l Version 3.1.76 oder höher.</span><span class="sxs-lookup"><span data-stu-id="7b191-117">MIDL version 3.1.76 or later.</span></span>

 

 