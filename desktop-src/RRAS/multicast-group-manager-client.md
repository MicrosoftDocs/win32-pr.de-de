---
title: Multicast-Gruppen-Manager-Client
description: Ein Client ist eine Entität, die eine MGM-Funktion aufruft, z. b. ein Routing Protokoll oder eine administrative Anwendung.
ms.assetid: 98d13b48-9f1d-4649-a5a3-03926c7facee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5f2a8ba63903c084547e3d04ea04474171651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714064"
---
# <a name="multicast-group-manager-client"></a><span data-ttu-id="1e24f-103">Multicast-Gruppen-Manager-Client</span><span class="sxs-lookup"><span data-stu-id="1e24f-103">Multicast Group Manager Client</span></span>

<span data-ttu-id="1e24f-104">Ein Client ist eine Entität, die eine MGM-Funktion aufruft, z. b. ein Routing Protokoll oder eine administrative Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1e24f-104">A client is an entity that calls an MGM function, such as a routing protocol or an administrative application.</span></span>

<span data-ttu-id="1e24f-105">Die MGM-API wird hauptsächlich von Multicast Routing Protokollen verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e24f-105">The MGM API is used primarily by multicast routing protocols.</span></span> <span data-ttu-id="1e24f-106">Entwickler von Multicast Routing Protokollen verwenden die MGM-API für Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1e24f-106">Developers of multicast routing protocols use the MGM API to:</span></span>

-   <span data-ttu-id="1e24f-107">Beibehalten der Gruppenmitgliedschaft</span><span class="sxs-lookup"><span data-stu-id="1e24f-107">Maintain group membership</span></span>
-   <span data-ttu-id="1e24f-108">Steuerungs Schnittstellen Besitz</span><span class="sxs-lookup"><span data-stu-id="1e24f-108">Control interface ownership</span></span>
-   <span data-ttu-id="1e24f-109">Empfangen von Benachrichtigungen vom Multicast-Gruppen-Manager bezüglich anderer Multicast Routing Protokolle Anforderungen für Multicast Daten</span><span class="sxs-lookup"><span data-stu-id="1e24f-109">Receive notifications from the multicast group manager regarding other multicast routing protocols' requests for multicast data</span></span>

<span data-ttu-id="1e24f-110">Bestimmte administrative Anwendungen, die MFEs (Multicast-Weiterleitungs Einträge) überwachen müssen, können dies ohne hinzufügen oder Entfernen von Gruppenmitgliedschaften tun.</span><span class="sxs-lookup"><span data-stu-id="1e24f-110">Specific administrative applications that must monitor multicast forwarding entries (MFEs) can do so without adding or removing group membership.</span></span> <span data-ttu-id="1e24f-111">Entwickler von Administratoren verwenden bestimmte MGM-Funktionen zum Überprüfen von Informationen in MFEs.</span><span class="sxs-lookup"><span data-stu-id="1e24f-111">Administrative application developers use specific MGM functions to review information in MFEs.</span></span>

> [!Note]  
> <span data-ttu-id="1e24f-112">Multicast Routing Protokolle greifen auch auf MFEs zu.</span><span class="sxs-lookup"><span data-stu-id="1e24f-112">Multicast routing protocols also access MFEs.</span></span>

 

<span data-ttu-id="1e24f-113">Ein MFE leitet Informationen weiter, die vom Multicast-Gruppen-Manager basierend auf der Gruppenmitgliedschaft erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1e24f-113">An MFE is forwarding information that the multicast group manager creates based on group membership.</span></span> <span data-ttu-id="1e24f-114">Die vom Multicast-Gruppen-Manager abgerufenen MFEs können statistische Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1e24f-114">The MFEs that are retrieved from the multicast group manager can provide statistical information.</span></span> <span data-ttu-id="1e24f-115">Eine administrative Anwendung kann diese Informationen dann verwenden, um die entsprechenden Aktionen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="1e24f-115">An administrative application can then use this information to determine the appropriate actions.</span></span> <span data-ttu-id="1e24f-116">Beispielsweise kann eine administrative Anwendung Aktionen ausführen, die auf der Menge der Pakete auf einer bestimmten Schnittstelle basieren.</span><span class="sxs-lookup"><span data-stu-id="1e24f-116">For example, an administrative application could perform actions that are based on the volume of packets on a specific interface.</span></span>

 

 




