---
description: Die Peer Gruppierungs-API kombiniert die Technologie der PNRP-Namespace Anbieter-API und der grapherstellungsapi.
ms.assetid: 0a575efe-968c-48ab-a446-0d910ecb5708
title: Informationen zur Gruppierungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e0c14e2731dd133afac32f2cd21905fa7e0c5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362238"
---
# <a name="about-the-grouping-api"></a><span data-ttu-id="a47f8-103">Informationen zur Gruppierungs-API</span><span class="sxs-lookup"><span data-stu-id="a47f8-103">About the Grouping API</span></span>

<span data-ttu-id="a47f8-104">Die Peer Gruppierungs-API kombiniert die Technologie der PNRP-Namespace Anbieter-API und der [grapherstellungsapi](graphing-api.md). [](pnrp-namespace-provider-api.md)</span><span class="sxs-lookup"><span data-stu-id="a47f8-104">The Peer Grouping API combines the technology of the [PNRP Name Space Provider API](pnrp-namespace-provider-api.md) and the [Graphing API](graphing-api.md).</span></span> <span data-ttu-id="a47f8-105">Durch die Gruppierung werden die folgenden zwei Teile der Technologie hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a47f8-105">Grouping adds the following two pieces of technology:</span></span>

-   <span data-ttu-id="a47f8-106">Eine Multiplexing-Ebene, die es mehreren Anwendungen ermöglicht, ein Diagramm, einen Port und eine datensatzdatenbank zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a47f8-106">A multiplexing layer that allows multiple applications to use one graph, one port, and one record database.</span></span>
-   <span data-ttu-id="a47f8-107">Sicherheit, durch die sichergestellt wird, dass nur Peers, die in eine Gruppe eingeladen wurden, während der gesamten Lebensdauer einer Gruppe beitreten und</span><span class="sxs-lookup"><span data-stu-id="a47f8-107">Security that ensures only peers invited to a group can join and connect throughout the lifetime of a group.</span></span>

<span data-ttu-id="a47f8-108">Die Gruppierung bietet eine barrierefreie und einfache Herangehensweise an das Peer Netzwerk aufgrund des einfachen aufrufflusses und sicheren Messaging.</span><span class="sxs-lookup"><span data-stu-id="a47f8-108">Grouping provides an accessible and easy approach to peer networking because of the straightforward call flow and secure messaging.</span></span> <span data-ttu-id="a47f8-109">Diese API nutzt PNRP für die Gruppen Ermittlung und einen standardmäßigen PKI-basierten Sicherheitsanbieter, anstatt einen Entwickler zum Implementieren eines solchen zu benötigen.</span><span class="sxs-lookup"><span data-stu-id="a47f8-109">This API utilizes PNRP for group discovery and a standard PKI-based security provider instead of requiring a developer to implement one.</span></span> <span data-ttu-id="a47f8-110">Wenn Ihre Anwendung jedoch mehr Flexibilität im Hinblick auf Sicherheitsoptionen erfordert, sollten Sie die [graphingapi](about-the-graphing-api.md)in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="a47f8-110">However, if your application demands greater flexibility in terms of security options, consider using the [Graphing API](about-the-graphing-api.md).</span></span>

<span data-ttu-id="a47f8-111">In der folgenden Tabelle sind die Themen dieses Gruppierungs-API-Abschnitts aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="a47f8-111">The following table identifies the topics in this Grouping API section:</span></span>

| <span data-ttu-id="a47f8-112">Thema</span><span class="sxs-lookup"><span data-stu-id="a47f8-112">Topic</span></span>                                                                | <span data-ttu-id="a47f8-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a47f8-113">Description</span></span>                                                                              |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a47f8-114">Arbeiten mit Gruppen</span><span class="sxs-lookup"><span data-stu-id="a47f8-114">How to Work With Groups</span></span>](how-to-work-with-groups.md)               | <span data-ttu-id="a47f8-115">Beschreibt den Aufruffluss in einer Peer Gruppierungs Anwendung vom Start bis zum Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="a47f8-115">Describes the call flow in a Peer Grouping application from startup to shutdown.</span></span>         |
| [<span data-ttu-id="a47f8-116">Funktionsweise der Gruppen Sicherheit</span><span class="sxs-lookup"><span data-stu-id="a47f8-116">How Group Security Works</span></span>](how-group-security-works.md)             | <span data-ttu-id="a47f8-117">Beschreibt, wie Peer Gruppenmitgliedschaft und Datenaustausch geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="a47f8-117">Describes how peer group membership and data exchanges are secured.</span></span>                      |
| [<span data-ttu-id="a47f8-118">Einladen eines Peers zu einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="a47f8-118">Inviting a Peer to a Group</span></span>](inviting-a-peer-to-a-group.md)         | <span data-ttu-id="a47f8-119">Beschreibt den Prozess, mit dem Peers eingeladen und einer Peer Gruppe hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a47f8-119">Describes the process by which peers are invited and added to a peer group.</span></span>              |
| [<span data-ttu-id="a47f8-120">Vorgehensweise beim Herstellen einer Verbindung mit einer Peer Gruppe</span><span class="sxs-lookup"><span data-stu-id="a47f8-120">How to Connect to a Peer Group</span></span>](how-to-connect-to-a-peer-group.md) | <span data-ttu-id="a47f8-121">Beschreibt, wie ein Peer eine Verbindung mit einer Peer Gruppe herstellt und mit dieser interagiert.</span><span class="sxs-lookup"><span data-stu-id="a47f8-121">Describes how a peer connects to and interacts with a peer group.</span></span>                        |
| [<span data-ttu-id="a47f8-122">Verwalten von Gruppendaten Sätzen</span><span class="sxs-lookup"><span data-stu-id="a47f8-122">Managing Group Records</span></span>](managing-group-records.md)                 | <span data-ttu-id="a47f8-123">Beschreibt Peer Gruppen-Datensätze und deren Verwaltung als Mitglied und Administrator.</span><span class="sxs-lookup"><span data-stu-id="a47f8-123">Describes peer group records and how to manage them as a member and as an administrator.</span></span> |



 

> [!Note]  
> <span data-ttu-id="a47f8-124">Anwendungen, die die Gruppierungs-API in einer Umgebung mit einer Firewall verwenden, benötigen Ausnahme Gruppen, die den für die Anwendung spezifischen Port abdecken, sowie den Port "3587-TCP" für die Gruppierungs-API und den Port "3540-UDP" für PNRP.</span><span class="sxs-lookup"><span data-stu-id="a47f8-124">Applications using the Grouping API in an environment with a firewall require exception groups that cover the port specific to the application, as well as port '3587-TCP' for the Grouping API and port '3540-UDP' for PNRP.</span></span> <span data-ttu-id="a47f8-125">Diese Ausnahme Gruppen sollten immer dann aktiviert werden, wenn die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a47f8-125">These exception groups should be enabled whenever the application is running.</span></span>

 

 

 



