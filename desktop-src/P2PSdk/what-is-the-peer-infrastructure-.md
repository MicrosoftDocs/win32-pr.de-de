---
description: Die Peer Infrastruktur ist eine Reihe von verschiedenen APIs, die leistungsstark und flexibel sind.
ms.assetid: aed7585a-88e5-4ca3-a8c3-e2ccfe13d35d
title: Was ist die Peer Infrastruktur?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873717b3f90497fe9ab9f50bb9c18e6f0692a4e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362472"
---
# <a name="what-is-the-peer-infrastructure"></a><span data-ttu-id="d5827-103">Was ist die Peer Infrastruktur?</span><span class="sxs-lookup"><span data-stu-id="d5827-103">What is the Peer Infrastructure?</span></span>

<span data-ttu-id="d5827-104">Die Peer Infrastruktur ist eine Reihe von verschiedenen APIs, die leistungsstark und flexibel sind.</span><span class="sxs-lookup"><span data-stu-id="d5827-104">The Peer Infrastructure is a set of several APIs that are powerful and flexible.</span></span> <span data-ttu-id="d5827-105">Die Hauptkomponenten umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d5827-105">The major components include the following:</span></span>

-   [<span data-ttu-id="d5827-106">Peer graphende-API</span><span class="sxs-lookup"><span data-stu-id="d5827-106">Peer Graphing API</span></span>](#peer-graphing-api)
-   [<span data-ttu-id="d5827-107">Peer Gruppierungs-API</span><span class="sxs-lookup"><span data-stu-id="d5827-107">Peer Grouping API</span></span>](#peer-grouping-api)
-   [<span data-ttu-id="d5827-108">Peer Identity Manager-API</span><span class="sxs-lookup"><span data-stu-id="d5827-108">Peer Identity Manager API</span></span>](#peer-identity-manager-api)
-   [<span data-ttu-id="d5827-109">PNRP-Namespace Anbieter-API</span><span class="sxs-lookup"><span data-stu-id="d5827-109">PNRP Namespace Provider API</span></span>](#pnrp-namespace-provider-api)

## <a name="peer-graphing-api"></a><span data-ttu-id="d5827-110">Peer graphende-API</span><span class="sxs-lookup"><span data-stu-id="d5827-110">Peer Graphing API</span></span>

<span data-ttu-id="d5827-111">Die Peer Infrastruktur bietet eine graphingtechnologie, die Informationen effizient und zuverlässig zwischen Peers in einem Peer Diagramm übergibt.</span><span class="sxs-lookup"><span data-stu-id="d5827-111">The Peer Infrastructure provides a graphing technology that can pass information efficiently and reliably between peers in a peer graph.</span></span> <span data-ttu-id="d5827-112">Die [Peer graphende-API](graphing-api.md) stellt sicher, dass jeder Knoten über eine konsistente Sicht der Daten in einem Diagramm verfügt.</span><span class="sxs-lookup"><span data-stu-id="d5827-112">The [Peer Graphing API](graphing-api.md) ensures that each node has a consistent view of the data in a graph.</span></span>

<span data-ttu-id="d5827-113">Mit der [Peer graphingapi](graphing-api.md) können Sie folgende Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="d5827-113">You can use the [Peer Graphing API](graphing-api.md) to do the following:</span></span>

-   <span data-ttu-id="d5827-114">Erstellen und Verwalten von Peer Diagrammen</span><span class="sxs-lookup"><span data-stu-id="d5827-114">Create and manage peer graphs</span></span>
-   <span data-ttu-id="d5827-115">Auflisten von und interagieren mit anderen Peers in einem Peer Diagramm</span><span class="sxs-lookup"><span data-stu-id="d5827-115">Enumerate and interact with other peers in a peer graph</span></span>
-   <span data-ttu-id="d5827-116">Senden von Daten in Form eines Daten [Satzes](records.md) an jeden Knoten in einem Peer Diagramm</span><span class="sxs-lookup"><span data-stu-id="d5827-116">Send data in the form of a [record](records.md) to each node in a peer graph</span></span>

## <a name="peer-grouping-api"></a><span data-ttu-id="d5827-117">Peer Gruppierungs-API</span><span class="sxs-lookup"><span data-stu-id="d5827-117">Peer Grouping API</span></span>

<span data-ttu-id="d5827-118">Die [Peer Gruppierungs-API](grouping-api.md) kombiniert und erweitert die Peer- [PNRP](#pnrp-namespace-provider-api) -und [graphingapis](#peer-graphing-api) und fügt die folgenden beiden Komponenten hinzu:</span><span class="sxs-lookup"><span data-stu-id="d5827-118">The [Peer Grouping API](grouping-api.md) combines and enhances the Peer [PNRP](#pnrp-namespace-provider-api) and [Graphing](#peer-graphing-api) APIs, and adds the following two components:</span></span>

-   <span data-ttu-id="d5827-119">Eine Multiplexing-Ebene, die es ermöglicht, dass mehrere Anwendungen auf einer Peer Entität eine Verbindung mit einer Gruppe herstellen.</span><span class="sxs-lookup"><span data-stu-id="d5827-119">A multiplexing layer that allows multiple applications running on one peer entity to connect to a group</span></span>
-   <span data-ttu-id="d5827-120">Ein bestimmtes Sicherheitsmodell, das sicherstellt, dass nur Peers, die an eine Gruppe eingeladen wurden, über die Lebensdauer der Gruppe eine Verbindung mit der Gruppe herstellen</span><span class="sxs-lookup"><span data-stu-id="d5827-120">A specific security model that ensures only peers invited to a group can connect to the group through the lifetime of the group</span></span>

<span data-ttu-id="d5827-121">Mit der Peer Gruppierungs-API können Sie folgende Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="d5827-121">You can use the Peer Grouping API to do the following:</span></span>

-   <span data-ttu-id="d5827-122">Erstellen und Verwalten von sicheren Peer Gruppen</span><span class="sxs-lookup"><span data-stu-id="d5827-122">Create and manage secure peer groups</span></span>
-   <span data-ttu-id="d5827-123">Auflisten von und interagieren mit anderen Peers in einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="d5827-123">Enumerate and interact with other peers in a group</span></span>
-   <span data-ttu-id="d5827-124">Senden von Daten in Form eines Daten [Satzes](records.md) an jeden Knoten in einer Peer Gruppe</span><span class="sxs-lookup"><span data-stu-id="d5827-124">Send data in the form of a [record](records.md) to each node in a peer group</span></span>

## <a name="peer-identity-manager-api"></a><span data-ttu-id="d5827-125">Peer Identity Manager-API</span><span class="sxs-lookup"><span data-stu-id="d5827-125">Peer Identity Manager API</span></span>

<span data-ttu-id="d5827-126">Mithilfe der [Peer Identity Manager-API](identity-manager-api.md) können Sie sichere [Peer Namen](peer-names.md) erstellen, mit denen PNRP sicherstellen kann, dass eine Person, die einen Namen veröffentlicht, den Namen offiziell besitzt.</span><span class="sxs-lookup"><span data-stu-id="d5827-126">By using the [Peer Identity Manager API](identity-manager-api.md) you can create secure [peer names](peer-names.md) that PNRP can use to ensure that a person publishing a name officially owns the name.</span></span> <span data-ttu-id="d5827-127">Peer Namen werden auch als Identitäten bezeichnet und in der Peer Gruppierungs-API verwendet, um die einzelnen Personen in einer Gruppe zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d5827-127">Peer names are also called identities, and they are used in the Peer Grouping API to identify the individuals in a group.</span></span>

<span data-ttu-id="d5827-128">Mit der [Peer Identity Manager-API](identity-manager-api.md) können Sie folgende Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="d5827-128">You can use the [Peer Identity Manager API](identity-manager-api.md) to do the following:</span></span>

-   <span data-ttu-id="d5827-129">Erstellen, auflisten und Verwalten von Peer Identitäten.</span><span class="sxs-lookup"><span data-stu-id="d5827-129">Create, enumerate, and manage peer identities.</span></span>

## <a name="pnrp-namespace-provider-api"></a><span data-ttu-id="d5827-130">PNRP-Namespace Anbieter-API</span><span class="sxs-lookup"><span data-stu-id="d5827-130">PNRP Namespace Provider API</span></span>

<span data-ttu-id="d5827-131">Die Peer Infrastruktur bietet eine Server lose namens Auflösungs Technologie, die als [PNRP-Namespace Anbieter-API](pnrp-namespace-provider-api.md)bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="d5827-131">The Peer Infrastructure provides a serverless name resolution technology called the [PNRP Namespace Provider API](pnrp-namespace-provider-api.md).</span></span> <span data-ttu-id="d5827-132">Mithilfe der Anbieter-API für den Winsock 2-PNRP-Namespace können Peer-, Dienst-, Computer-und Peer Gruppen Endpunkte einen anderen Endpunkt in einer PNRP- [Cloud](clouds.md)verwalten, registrieren, seine Registrierung aufheben und auflösen.</span><span class="sxs-lookup"><span data-stu-id="d5827-132">By using the Winsock 2 PNRP Namespace Provider API, a peer, service, computing device, and peer group endpoint can manage, register, unregister, and resolve another endpoint in a PNRP [cloud](clouds.md).</span></span>

> [!Note]  
> <span data-ttu-id="d5827-133">PNRP ist ein Akronym für das **Peer Name Resolution-Protokoll**.</span><span class="sxs-lookup"><span data-stu-id="d5827-133">PNRP is an acronym for **peer name resolution protocol**.</span></span>

 

 

 



