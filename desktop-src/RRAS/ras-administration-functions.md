---
title: RAS-Verwaltungsfunktionen
description: In dieser Dokumentation werden RRAS-Funktionen beschrieben, die zum Entwickeln von Software zum Verwalten von RAS-DFÜ-Verbindungen verwendet werden.
ms.assetid: 27cf63e2-9dd3-4bc1-98af-e93055d89492
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0a18f6c49964d89c308b065289dd4de9fc22c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311063"
---
# <a name="ras-administration-functions"></a><span data-ttu-id="61655-103">RAS-Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="61655-103">RAS Administration Functions</span></span>

<span data-ttu-id="61655-104">In dieser Dokumentation werden RRAS-Funktionen beschrieben, die zum Entwickeln von Software zum Verwalten von RAS-DFÜ-Verbindungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61655-104">This documentation describes RRAS functions that are used to develop software to administer RAS dial-up connections.</span></span> <span data-ttu-id="61655-105">Zu diesen Funktionen gehören:</span><span class="sxs-lookup"><span data-stu-id="61655-105">These functions include:</span></span>

-   [<span data-ttu-id="61655-106">**Mpradminconnectionclearstats**</span><span class="sxs-lookup"><span data-stu-id="61655-106">**MprAdminConnectionClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)
-   [<span data-ttu-id="61655-107">**Mpradminconnectionenum**</span><span class="sxs-lookup"><span data-stu-id="61655-107">**MprAdminConnectionEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)
-   [<span data-ttu-id="61655-108">**Mpradminconnectionenumex**</span><span class="sxs-lookup"><span data-stu-id="61655-108">**MprAdminConnectionEnumEx**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenumex)
-   [<span data-ttu-id="61655-109">**Mpradminconnectiongetinfo**</span><span class="sxs-lookup"><span data-stu-id="61655-109">**MprAdminConnectionGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)
-   [<span data-ttu-id="61655-110">**Mpradminconnectiongetinfoex**</span><span class="sxs-lookup"><span data-stu-id="61655-110">**MprAdminConnectionGetInfoEx**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfoex)
-   [<span data-ttu-id="61655-111">**Mpradminconnectionremovequarantäne**</span><span class="sxs-lookup"><span data-stu-id="61655-111">**MprAdminConnectionRemoveQuarantine**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionremovequarantine)
-   [<span data-ttu-id="61655-112">**Mpradminportclearstats**</span><span class="sxs-lookup"><span data-stu-id="61655-112">**MprAdminPortClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)
-   [<span data-ttu-id="61655-113">**Mpradminportdisconnect**</span><span class="sxs-lookup"><span data-stu-id="61655-113">**MprAdminPortDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)
-   [<span data-ttu-id="61655-114">**Mpradminportenum**</span><span class="sxs-lookup"><span data-stu-id="61655-114">**MprAdminPortEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)
-   [<span data-ttu-id="61655-115">**Mpradminportgetinfo**</span><span class="sxs-lookup"><span data-stu-id="61655-115">**MprAdminPortGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)
-   [<span data-ttu-id="61655-116">**Mpradminportreset**</span><span class="sxs-lookup"><span data-stu-id="61655-116">**MprAdminPortReset**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

<span data-ttu-id="61655-117">Zusätzliche Funktionen werden sowohl für die RAS-Verwaltung als auch für die Routerverwaltung verwendet.</span><span class="sxs-lookup"><span data-stu-id="61655-117">Additional functions are used for both RAS administration and router administration.</span></span> <span data-ttu-id="61655-118">Die folgenden Funktionen sind in der Referenz zur [routerverwaltungfunktionen](router-administration-functions.md) dokumentiert:</span><span class="sxs-lookup"><span data-stu-id="61655-118">The following functions documented in the [Router Administration Functions](router-administration-functions.md) reference:</span></span>

-   [<span data-ttu-id="61655-119">**Mpradminbufferfree**</span><span class="sxs-lookup"><span data-stu-id="61655-119">**MprAdminBufferFree**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)
-   [<span data-ttu-id="61655-120">**Mpradmingeterrorstring**</span><span class="sxs-lookup"><span data-stu-id="61655-120">**MprAdminGetErrorString**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)
-   [<span data-ttu-id="61655-121">**Mpradminisservicerunning**</span><span class="sxs-lookup"><span data-stu-id="61655-121">**MprAdminIsServiceRunning**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)
-   [<span data-ttu-id="61655-122">**Mpradminserverconnect**</span><span class="sxs-lookup"><span data-stu-id="61655-122">**MprAdminServerConnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)
-   [<span data-ttu-id="61655-123">**Mpradminserverdisconnect**</span><span class="sxs-lookup"><span data-stu-id="61655-123">**MprAdminServerDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

<span data-ttu-id="61655-124">Verwenden Sie die im folgenden Thema beschriebenen Funktionen, um eine RAS-Verwaltungs-dll zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="61655-124">To implement a RAS administration DLL, use the functions described in the following topic:</span></span>

-   [<span data-ttu-id="61655-125">RAS-admin-DLL-Funktionen</span><span class="sxs-lookup"><span data-stu-id="61655-125">RAS Admin DLL Functions</span></span>](ras-admin-dll-functions.md)

<span data-ttu-id="61655-126">Zum Verwalten von Benutzern eines RAS-Servers verwenden Sie die Funktionen, die im folgenden Thema beschrieben werden:</span><span class="sxs-lookup"><span data-stu-id="61655-126">To manage users of a RAS server, use the functions described in the following topic:</span></span>

-   [<span data-ttu-id="61655-127">RAS-Benutzer Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="61655-127">RAS User Administration Functions</span></span>](ras-user-administration-functions.md)

 

 




