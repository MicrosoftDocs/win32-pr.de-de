---
title: Informationen zur Routing Protokoll Schnittstelle
description: In der folgenden Dokumentation wird die Integration von Routing Protokollen von Drittanbietern in den Routing-und RAS-Dienst (RRAS) beschrieben.
ms.assetid: 593e3b8a-6f26-47c6-aa93-520d36db7a6f
keywords:
- RRAS für Routing-und RAS-Dienst, Routing Protokoll Schnittstelle
- Routing-und RAS-Dienst RRAS, Routing Protokoll Schnittstelle, beschrieben
- Routing Protokoll Schnittstelle RRAS
- RRAS-Routing Protokoll Schnittstelle, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bc663f249ca42ebbae509c164a828d603a9b968
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711838"
---
# <a name="about-routing-protocol-interface"></a><span data-ttu-id="f62a7-107">Informationen zur Routing Protokoll Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f62a7-107">About Routing Protocol Interface</span></span>

<span data-ttu-id="f62a7-108">In der folgenden Dokumentation wird die Integration von Routing Protokollen von Drittanbietern in den Routing-und RAS-Dienst (RRAS) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f62a7-108">The following documentation describes the integration of third-party routing protocols into the Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="f62a7-109">RRAS ist eine Funktion von Windows, die als Multiprotokollrouter fungiert.</span><span class="sxs-lookup"><span data-stu-id="f62a7-109">RRAS is a feature of Windows that acts as a multi-protocol router.</span></span> <span data-ttu-id="f62a7-110">RRAS definiert die Schnittstelle zwischen dem routermanager und dem Routing Protokoll.</span><span class="sxs-lookup"><span data-stu-id="f62a7-110">RRAS defines the interface between the router manager and the routing protocol.</span></span> <span data-ttu-id="f62a7-111">Das Routing Protokoll wird in einer Dynamic Link Library (dll) implementiert.</span><span class="sxs-lookup"><span data-stu-id="f62a7-111">The routing protocol is implemented in a dynamic link library (DLL).</span></span>

<span data-ttu-id="f62a7-112">Verwenden Sie diese Schnittstelle, um Routing Protokolle, wie z. b. IGRP, nlsp und BGP, als benutzermodusdlls zu implementieren, die mit RRAS funktionieren.</span><span class="sxs-lookup"><span data-stu-id="f62a7-112">Use this interface to implement routing protocols, such as IGRP, NLSP, and BGP, as user-mode DLLs that work with RRAS.</span></span>

<span data-ttu-id="f62a7-113">In dieser Dokumentation werden die folgenden Themen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="f62a7-113">This documentation describes the following topics:</span></span>

-   [<span data-ttu-id="f62a7-114">Adapter</span><span class="sxs-lookup"><span data-stu-id="f62a7-114">Adapters</span></span>](adapters.md)
-   [<span data-ttu-id="f62a7-115">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f62a7-115">Interfaces</span></span>](interfaces.md)
-   [<span data-ttu-id="f62a7-116">Statische und automatische statische Routen</span><span class="sxs-lookup"><span data-stu-id="f62a7-116">Static and Autostatic Routes</span></span>](static-and-autostatic-routes.md)

 

 




