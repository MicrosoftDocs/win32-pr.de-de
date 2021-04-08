---
title: Veröffentlichen in einem Domänen System Container
description: Der System Container einer Domänen Partition enthält Betriebsinformationen pro Domäne.
ms.assetid: 18bb3409-774e-42d9-8f27-6c582d74ca86
ms.tgt_platform: multiple
keywords:
- Veröffentlichen in einem Domänen System-Container AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf7d1febd91e3540c7bc2002a36d33346820344
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855391"
---
# <a name="publishing-in-a-domain-system-container"></a><span data-ttu-id="819a7-104">Veröffentlichen in einem Domänen System Container</span><span class="sxs-lookup"><span data-stu-id="819a7-104">Publishing in a Domain System Container</span></span>

<span data-ttu-id="819a7-105">Der System Container einer Domänen Partition enthält Betriebsinformationen pro Domäne.</span><span class="sxs-lookup"><span data-stu-id="819a7-105">The System container of a domain partition holds per-domain operational information.</span></span> <span data-ttu-id="819a7-106">Dies schließt die standardmäßige lokale Sicherheitsrichtlinie, die Nachverfolgung von Datei Verknüpfungen, Netzwerk Besprechungen und Container für die Verbindungspunkte von Windows Sockets Registration and Resolution (RNR) und RPC Name Service (RpcNs) ein.</span><span class="sxs-lookup"><span data-stu-id="819a7-106">This includes the default local security policy, file link tracking, network meetings, and containers for Windows Sockets registration and resolution (RnR) and RPC name service (RpcNs) connection points.</span></span> <span data-ttu-id="819a7-107">Der System Container ist standardmäßig ausgeblendet und bietet einen geeigneten Ort zum Speichern von Objekten, die für Administratoren von Interesse sind, aber nicht für Endbenutzer.</span><span class="sxs-lookup"><span data-stu-id="819a7-107">The system container is hidden, by default, and provides a convenient place for storing objects that are of interest to administrators, but not to end users.</span></span>

<span data-ttu-id="819a7-108">Dienste, die nicht an einen einzelnen Host gebunden sind, können Ihre SCPs unter dem System Container einer Domänen Partition erstellen.</span><span class="sxs-lookup"><span data-stu-id="819a7-108">Services that are not tied to a single host may want to create their SCPs under the System container of a domain partition.</span></span> <span data-ttu-id="819a7-109">Diese Alternative eignet sich für Dienste mit Replikaten, die auf mehreren Hosts installiert sind, wobei jedes Replikat für Clients in der gesamten Domäne identische Dienste bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="819a7-109">This alternative can be useful for services with replicas installed on multiple hosts, each replica providing identical services to clients throughout the domain.</span></span> <span data-ttu-id="819a7-110">Sie ermöglicht es Ihnen, alle Objekte für den replizierten Dienst in einem einzelnen Container zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="819a7-110">It enables you to group all the objects for the replicated service under a single container.</span></span>

<span data-ttu-id="819a7-111">Dienste, die Dienst spezifische Objekte im System Container erstellen, müssen folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="819a7-111">Services that create service-specific objects in the System container must do the following:</span></span>

1.  <span data-ttu-id="819a7-112">Erstellen Sie einen unter Container des Objektklassen **Containers** als direkt untergeordnetes Element des System Containers.</span><span class="sxs-lookup"><span data-stu-id="819a7-112">Create a sub-container of object class **container** as an immediate child of the System container.</span></span> <span data-ttu-id="819a7-113">Weisen Sie diesem unter Container einen Namen zu, der ihn im Zusammenhang mit dem Dienst eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="819a7-113">Give this sub-container a name that clearly identifies it as pertaining to the service.</span></span>
2.  <span data-ttu-id="819a7-114">Erstellen Sie die Dienst bezogenen Objekte in diesem unter Container.</span><span class="sxs-lookup"><span data-stu-id="819a7-114">Create the service-related objects in this sub-container.</span></span> <span data-ttu-id="819a7-115">Beispielsweise verwendet NetMeeting den Besprechungs Container zum Veröffentlichen von Netzwerk Besprechungs Objekten.</span><span class="sxs-lookup"><span data-stu-id="819a7-115">For example, NetMeeting uses the Meetings container to publish network meeting objects.</span></span>

<span data-ttu-id="819a7-116">Ein Anbieter mit mehreren Produkten kann eine ähnliche Strategie zum Gruppieren von Dienst bezogenen Objekten für alle seine Produkte verwenden.</span><span class="sxs-lookup"><span data-stu-id="819a7-116">A vendor with multiple products can use a similar strategy to group service-related objects for all of its products.</span></span> <span data-ttu-id="819a7-117">In diesem Fall können Sie ein **Container** Objekt mit einem Namen erstellen, der den Anbieter eindeutig identifiziert. Erstellen Sie dann **Container** Objekte für jeden Dienst als untergeordnete Elemente des Hersteller Containers.</span><span class="sxs-lookup"><span data-stu-id="819a7-117">In this case, you could create a **container** object with a name that clearly identifies the vendor; then create **container** objects for each service as children of the vendor container.</span></span> <span data-ttu-id="819a7-118">Erstellen Sie den herstellerspezifischen Container als untergeordnetes Element des System Containers.</span><span class="sxs-lookup"><span data-stu-id="819a7-118">Create the vendor-specific container as a child of the System container.</span></span>

 

 




