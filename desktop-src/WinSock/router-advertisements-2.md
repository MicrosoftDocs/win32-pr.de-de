---
description: Der Inhalt von IPv6-Routerankündigungen wird automatisch von den veröffentlichten Routen in der Routing Tabelle abgeleitet. Nicht veröffentlichte Routen werden für das Routing verwendet, werden jedoch beim Erstellen von Routerankündigungen ignoriert.
ms.assetid: 27b735db-4e87-497b-b39c-e464cf44f09e
title: IPv6-Routerankündigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a75b31a988595cba85d23dbafc1bd93ffff4ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349143"
---
# <a name="ipv6-router-advertisements"></a><span data-ttu-id="e3084-104">IPv6-Routerankündigungen</span><span class="sxs-lookup"><span data-stu-id="e3084-104">IPv6 Router Advertisements</span></span>

<span data-ttu-id="e3084-105">Der Inhalt von IPv6-Routerankündigungen wird automatisch von den veröffentlichten Routen in der Routing Tabelle abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e3084-105">The content of IPv6 router advertisements is automatically derived from the published routes in the routing table.</span></span> <span data-ttu-id="e3084-106">Nicht veröffentlichte Routen werden für das Routing verwendet, werden jedoch beim Erstellen von Routerankündigungen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e3084-106">Nonpublished routes are used for routing but are ignored when constructing router advertisements.</span></span>

<span data-ttu-id="e3084-107">Routerankündigungen für IPv6 enthalten immer eine Quell Verbindungsschicht-Adress Option und eine MTU-Option.</span><span class="sxs-lookup"><span data-stu-id="e3084-107">Router advertisements for IPv6 always contain a source link-layer address option and an MTU option.</span></span> <span data-ttu-id="e3084-108">Der Wert für die MTU-Option wird von der aktuellen Link-MTU der Sende Schnittstelle entnommen.</span><span class="sxs-lookup"><span data-stu-id="e3084-108">The value for the MTU option is taken from the sending interface's current link MTU.</span></span> <span data-ttu-id="e3084-109">Dieser Wert kann mit dem IPv6-Befehl "IPMTU" geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e3084-109">This value can be changed with the ipv6 ifc mtu command.</span></span>

<span data-ttu-id="e3084-110">Die Routerankündigung hat nur eine routerlebensdauer, wenn eine veröffentlichte Standardroute vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e3084-110">The router advertisement only has a nonzero router lifetime if there is a published default route.</span></span> <span data-ttu-id="e3084-111">Eine Standardroute ist eine Route für das Präfix mit der Länge 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e3084-111">A default route is a route for the zero-length prefix.</span></span>

<span data-ttu-id="e3084-112">Veröffentlichte on-Link-Routen führen zu Präfix Informations Optionen in Routerankündigungen.</span><span class="sxs-lookup"><span data-stu-id="e3084-112">Published on-link routes result in prefix information options in router advertisements.</span></span> <span data-ttu-id="e3084-113">Wenn das on-Link-Präfix 64 Bits hat, wird für die Option für die Präfix Informationen sowohl L als auch Bits festgelegt, und Hosts, die Sie empfangen, werden Adressen automatisch konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e3084-113">If the on-link prefix has 64 bits, the prefix information option has both the L and A bits set and hosts receiving it will autoconfigure addresses.</span></span>

<span data-ttu-id="e3084-114">Eine Schnittstelle, die Routerankündigungen sendet, konfiguriert auch Adressen für sich selbst auf der Grundlage der von ihr gesendeten Optionen für Präfix Informationen automatisch.</span><span class="sxs-lookup"><span data-stu-id="e3084-114">An interface that sends router advertisements will also autoconfigure addresses for itself based on the prefix information options that it sends.</span></span>

<span data-ttu-id="e3084-115">Es wird empfohlen, eine begrenzte Dauer Lebensdauer für alle veröffentlichten Routen (z. b. 30 Minuten) zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e3084-115">A finite nonaging lifetime on all published routes (for example, 30 minutes) is recommended.</span></span> <span data-ttu-id="e3084-116">Wenn Sie eine Route zurückziehen möchten, können Sie die Route so ändern, dass Sie eine Alterungs Lebensdauer hat.</span><span class="sxs-lookup"><span data-stu-id="e3084-116">If you decide to retract a route, you can change the route to have an aging lifetime.</span></span> <span data-ttu-id="e3084-117">Die Route wird im Verlauf mehrerer Routerankündigungen verwendet und verschwindet dann vom Router und allen Hosts, die die Routerankündigungen empfangen.</span><span class="sxs-lookup"><span data-stu-id="e3084-117">The route will age over the course of several router advertisements and then disappear from both the router and any hosts receiving the router advertisements.</span></span>

<span data-ttu-id="e3084-118">Routen, die Hosts über das Alter von Routerankündigungen suchen und nicht veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="e3084-118">Routes that hosts find through router advertisements age and are not published.</span></span> <span data-ttu-id="e3084-119">Adressen, die von Routerankündigungen ebenfalls automatisch konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="e3084-119">Addresses autoconfigured from router advertisements age as well.</span></span>

 

 



