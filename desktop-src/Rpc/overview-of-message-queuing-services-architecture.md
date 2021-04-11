---
title: Übersicht über Message Queuing Services-Architektur
description: Message Queuing Services (MSMQ) verwendet ein Site/Enterprise-Modell. In der Regel ist eine Site ein physischer Standort, z. b. ein Gebäude. Ein Unternehmen besteht aus einem oder mehreren Standorten und repräsentiert eine Organisation.
ms.assetid: f5c54c58-8ec5-49b7-a184-aed9a8100960
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2226c185d32cb628529b34ba33d5569bd51ac28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310724"
---
# <a name="overview-of-message-queuing-services-architecture"></a><span data-ttu-id="4a0f2-105">Übersicht über Message Queuing Services-Architektur</span><span class="sxs-lookup"><span data-stu-id="4a0f2-105">Overview of Message Queuing Services Architecture</span></span>

<span data-ttu-id="4a0f2-106">Message Queuing Services (MSMQ) verwendet ein Site/Enterprise-Modell.</span><span class="sxs-lookup"><span data-stu-id="4a0f2-106">Message Queuing Services (MSMQ) uses a site/enterprise model.</span></span> <span data-ttu-id="4a0f2-107">In der Regel ist eine Site ein physischer Standort, z. b. ein Gebäude.</span><span class="sxs-lookup"><span data-stu-id="4a0f2-107">Typically, a site is a physical location, such as a building.</span></span> <span data-ttu-id="4a0f2-108">Ein Unternehmen besteht aus einem oder mehreren Standorten und repräsentiert eine Organisation.</span><span class="sxs-lookup"><span data-stu-id="4a0f2-108">An enterprise consists of one or more sites and represents an organization.</span></span>

<span data-ttu-id="4a0f2-109">Das folgende Diagramm veranschaulicht die Architektur des MSMQ-Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="4a0f2-109">The following diagram illustrates the architecture of the MSMQ Service.</span></span>

![MSMQ-Architektur](images/msmq.png)

<span data-ttu-id="4a0f2-111">Das Herzstück von MSMQ ist die MQIS-Datenbank (Message Queue Information Service), die zusätzlich zu SQL Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a0f2-111">At the heart of MSMQ is the Message Queue Information Service (MQIS) database, which runs on top of SQL Server.</span></span> <span data-ttu-id="4a0f2-112">Ein Unternehmen verfügt über einen einzigen Master-MQIS, der als primärer Enterprise Controller bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="4a0f2-112">An enterprise has a single master MQIS, called the Primary Enterprise Controller.</span></span> <span data-ttu-id="4a0f2-113">Jeder Standort verfügt über eigene MQIS, die als *primärer Standort Controller* und NULL oder mehr *Sicherungs Standort Controller* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="4a0f2-113">Each site has its own MQIS, called a *primary site controller* and zero or more *backup site controllers*.</span></span> <span data-ttu-id="4a0f2-114">Schließlich gibt es die einzelnen Client Computer, die jeweils über einen eigenen Warteschlangen-Manager verfügen und als Dienst implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="4a0f2-114">Finally, there are the individual client computers, each of which has its own queue manager, implemented as a service.</span></span> <span data-ttu-id="4a0f2-115">Der primäre Unternehmens Controller kann auch ein primärer Standort Controller sein, und jeder Controller kann auch ein Client sein.</span><span class="sxs-lookup"><span data-stu-id="4a0f2-115">The Primary Enterprise Controller can also be a Primary Site Controller, and any controller can also be a client.</span></span>

<span data-ttu-id="4a0f2-116">Nachrichten Warteschlangen können entweder öffentlich oder privat sein.</span><span class="sxs-lookup"><span data-stu-id="4a0f2-116">Message queues can be either public or private.</span></span> <span data-ttu-id="4a0f2-117">Öffentliche Warteschlangen werden in Active Directory registriert und sind über das Netzwerk zugänglich.</span><span class="sxs-lookup"><span data-stu-id="4a0f2-117">Public queues are registered in Active Directory and are accessible across the network.</span></span> <span data-ttu-id="4a0f2-118">Nachrichten in einer öffentlichen Warteschlange werden im gesamten Unternehmen unter Kontrolle von MSMQ weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="4a0f2-118">Messages in a public queue are routed throughout the enterprise, under the control of MSMQ.</span></span> <span data-ttu-id="4a0f2-119">Client Anwendungs Nachrichten werden vom Warteschlangen-Manager des Clients in die Ziel Warteschlange verschoben, indem zwischen den Warteschlangen-Managern der Standort Controller gewechselt wird.</span><span class="sxs-lookup"><span data-stu-id="4a0f2-119">Client application messages move from the client's queue manager to the destination queue by traveling between the queue managers of the site controllers.</span></span>

<span data-ttu-id="4a0f2-120">Private Warteschlangen werden vom lokalen Warteschlangen-Manager verwaltet und sind nicht in Active Directory registriert.</span><span class="sxs-lookup"><span data-stu-id="4a0f2-120">Private queues are maintained by the local queue manager and are not registered in Active Directory.</span></span> <span data-ttu-id="4a0f2-121">Der Bereich privater Warteschlangen Nachrichten ist auf den Computer beschränkt, auf dem Sie sich befinden.</span><span class="sxs-lookup"><span data-stu-id="4a0f2-121">The scope of private queue messages is limited to the computer on which they reside.</span></span>

 

 




