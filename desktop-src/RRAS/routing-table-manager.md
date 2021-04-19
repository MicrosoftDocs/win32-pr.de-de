---
title: Routing Tabellen-Manager
description: Der Routing Tabellen-Manager ist das zentrale Repository von Routing Informationen für alle Routing Protokolle, die unter dem Routing-und RAS-Dienst (RRAS) betrieben werden.
ms.assetid: 7b01704e-c1fb-40e3-89cf-1206fdf9fd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98094eb34c8575e0c24854813fc7458c98749568
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341838"
---
# <a name="routing-table-manager"></a><span data-ttu-id="e42ca-103">Routing Tabellen-Manager</span><span class="sxs-lookup"><span data-stu-id="e42ca-103">Routing Table Manager</span></span>

<span data-ttu-id="e42ca-104">Der Routing Tabellen-Manager ist das zentrale Repository von Routing Informationen für alle Routing Protokolle, die unter dem Routing-und RAS-Dienst (RRAS) betrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e42ca-104">The routing table manager is the central repository of routing information for all routing protocols that operate under the Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="e42ca-105">Clients werden benachrichtigt, wenn Änderungen aufgetreten sind, und Clients können private Informationen austauschen.</span><span class="sxs-lookup"><span data-stu-id="e42ca-105">It notifies clients when changes have occurred, and allows clients to exchange private information.</span></span>

<span data-ttu-id="e42ca-106">Der Routing Tabellen-Manager bietet Routing Informationen für alle interessierten Clients, z. b. Routing Protokolle, Verwaltungsprogramme und Überwachungsprogramme.</span><span class="sxs-lookup"><span data-stu-id="e42ca-106">The routing table manager provides routing information to all interested clients, such as routing protocols, management programs, and monitoring programs.</span></span> <span data-ttu-id="e42ca-107">Der Routing Tabellen-Manager bestimmt außerdem die beste Route zu jedem Zielnetzwerk, das den Routing Protokollen bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="e42ca-107">The routing table manager also determines the best route to each destination network that is known to the routing protocols.</span></span> <span data-ttu-id="e42ca-108">Der Routing Tabellen-Manager bestimmt diese Route basierend auf den Prioritäten des Routing Protokolls und den Metriken, die den Routen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e42ca-108">The routing table manager determines this route based on routing protocol priorities and on the metrics associated with the routes.</span></span> <span data-ttu-id="e42ca-109">Die Person, die den Router verwaltet, kann Routing Protokoll Prioritäten mithilfe der RRAS-Verwaltungskonsole konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e42ca-109">The person administering the router can configure routing protocol priorities using the RRAS management console.</span></span>

<span data-ttu-id="e42ca-110">Der Routing Tabellen-Manager übergibt die Informationen der besten Route an die Weiterleitungen (eine pro Adressfamilie oder eine pro Schnittstelle) und an alle interessierten Clients.</span><span class="sxs-lookup"><span data-stu-id="e42ca-110">The routing table manager passes the best-route information to the forwarders (one per address family, or one per interface) and to all interested clients.</span></span>

<span data-ttu-id="e42ca-111">Jeder Client wird beim Routing Tabellen-Manager registriert, und in Return wird ein Handle empfangen, das der Client zum Hinzufügen oder Löschen von Routen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e42ca-111">Each client registers with the routing table manager, and in return receives a handle that the client uses to add or delete routes.</span></span> <span data-ttu-id="e42ca-112">Clients können in der Routing Tabelle gespeicherte Informationen abrufen.</span><span class="sxs-lookup"><span data-stu-id="e42ca-112">Clients can retrieve information stored in the routing table.</span></span> <span data-ttu-id="e42ca-113">Darüber hinaus können sich Clients beim Routing Tabellen-Manager registrieren, um Benachrichtigungen über Änderungen an der optimalen Route zu einem Ziel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e42ca-113">Additionally, clients can register with the routing table manager to receive notification of changes to the best route to a destination.</span></span>

 

 




