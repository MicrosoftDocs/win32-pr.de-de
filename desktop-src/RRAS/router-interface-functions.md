---
title: Funktionen der Routerschnittstelle
description: Verwenden Sie die folgenden Funktionen, um Schnittstellen auf dem Router zu verwalten.
ms.assetid: e988753e-908a-4c42-aad3-dd9f641c90a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a5318eedfbc3a04c13549012fda3bd4d93b4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309156"
---
# <a name="router-interface-functions"></a><span data-ttu-id="40495-103">Funktionen der Routerschnittstelle</span><span class="sxs-lookup"><span data-stu-id="40495-103">Router Interface Functions</span></span>

<span data-ttu-id="40495-104">Verwenden Sie die folgenden Funktionen, um Schnittstellen auf dem Router zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="40495-104">Use the following functions to administer interfaces on the router.</span></span>



| <span data-ttu-id="40495-105">Verwaltungsfunktion</span><span class="sxs-lookup"><span data-stu-id="40495-105">Administration Function</span></span>                                          | <span data-ttu-id="40495-106">Konfigurationsfunktion</span><span class="sxs-lookup"><span data-stu-id="40495-106">Configuration Function</span></span>                                             |
|------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="40495-107">**Mpradmininterfakecreate**</span><span class="sxs-lookup"><span data-stu-id="40495-107">**MprAdminInterfaceCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate)       | [<span data-ttu-id="40495-108">**Mprconfiginterfaecreate**</span><span class="sxs-lookup"><span data-stu-id="40495-108">**MprConfigInterfaceCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate)       |
| [<span data-ttu-id="40495-109">**Mpradmininterfacedelete**</span><span class="sxs-lookup"><span data-stu-id="40495-109">**MprAdminInterfaceDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete)       | [<span data-ttu-id="40495-110">**Mprconfiginterfacedelete**</span><span class="sxs-lookup"><span data-stu-id="40495-110">**MprConfigInterfaceDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacedelete)       |
| [<span data-ttu-id="40495-111">**Mpradmininterfaceerum**</span><span class="sxs-lookup"><span data-stu-id="40495-111">**MprAdminInterfaceEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfaceenum)           | [<span data-ttu-id="40495-112">**Mprconfiginterfacereum**</span><span class="sxs-lookup"><span data-stu-id="40495-112">**MprConfigInterfaceEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfaceenum)           |
| [<span data-ttu-id="40495-113">**Mpradmininterfacegethandle**</span><span class="sxs-lookup"><span data-stu-id="40495-113">**MprAdminInterfaceGetHandle**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegethandle) | [<span data-ttu-id="40495-114">**Mprconfiginterfacegethandle**</span><span class="sxs-lookup"><span data-stu-id="40495-114">**MprConfigInterfaceGetHandle**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegethandle) |
| [<span data-ttu-id="40495-115">**Mpradmininterfacegetinfo**</span><span class="sxs-lookup"><span data-stu-id="40495-115">**MprAdminInterfaceGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegetinfo)     | [<span data-ttu-id="40495-116">**Mprconfiginterfacegetinfo**</span><span class="sxs-lookup"><span data-stu-id="40495-116">**MprConfigInterfaceGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegetinfo)     |
| [<span data-ttu-id="40495-117">**Mpradmininterfakesetinfo**</span><span class="sxs-lookup"><span data-stu-id="40495-117">**MprAdminInterfaceSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo)     | [<span data-ttu-id="40495-118">**Mprconfiginterfakesetinfo**</span><span class="sxs-lookup"><span data-stu-id="40495-118">**MprConfigInterfaceSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo)     |



 

<span data-ttu-id="40495-119">Diese Funktionen wirken sich auf die Schnittstellen selbst aus, nicht auf Clients, die auf den Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="40495-119">These functions affect the interfaces themselves, not clients running on the interfaces.</span></span> <span data-ttu-id="40495-120">Aus diesem Grund erfordert keine der Funktionen, dass der Aufrufer einen bestimmten Transport (IP oder IPX) angibt. Obwohl Clients (z. b. Routing Protokolle) bestimmten Transporten zugeordnet sind, sind die Schnittstellen nicht selbst.</span><span class="sxs-lookup"><span data-stu-id="40495-120">For this reason, none of the functions require the caller to specify a particular transport (IP or IPX); although clients (such as routing protocols) are associated with particular transports, the interfaces themselves are not.</span></span>

<span data-ttu-id="40495-121">Diese Funktionen werden direkt von Dim verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="40495-121">These functions are handled directly by DIM.</span></span> <span data-ttu-id="40495-122">Die Router-Manager werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="40495-122">They do not utilize the router managers.</span></span>

<span data-ttu-id="40495-123">Die [**mpradmininterfacecreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) -und [**mpradmininterfacedelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) -Funktionen können keine LAN-Schnittstellen erstellen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="40495-123">The [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) and [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) functions cannot create or delete LAN interfaces.</span></span> <span data-ttu-id="40495-124">Sie können nur Schnittstellen mit Bedarf erstellen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="40495-124">They can only create or delete demand-dial interfaces.</span></span> <span data-ttu-id="40495-125">Eine Liste der Schnittstellentypen finden Sie unter [**Router \_ Interface \_ Type**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) .</span><span class="sxs-lookup"><span data-stu-id="40495-125">See [**ROUTER\_INTERFACE\_TYPE**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) for a list of interface types.</span></span>

 

 




