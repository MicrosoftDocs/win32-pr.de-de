---
title: Funktionen der HTTP-Server-API, Version 2.0
description: Die HTTP-Server-API-Version 2.0 stellt die folgenden Funktionen bereit.
ms.assetid: 12daffca-b403-4f06-8037-206f90e33252
keywords:
- Funktionen der HTTP-Server-API, Version 2.0
- Functions HTTP, HTTP Server API Version 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e4d5c09c001caa58d43c1e61d800f66b39706b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549075"
---
# <a name="http-server-api-version-20-functions"></a><span data-ttu-id="2dccc-105">Funktionen der HTTP-Server-API, Version 2.0</span><span class="sxs-lookup"><span data-stu-id="2dccc-105">HTTP Server API version 2.0 functions</span></span>

<span data-ttu-id="2dccc-106">Die HTTP-Server-API-Version 2.0 stellt die folgenden Funktionen bereit.</span><span class="sxs-lookup"><span data-stu-id="2dccc-106">The HTTP Server API version 2.0 provides the following functions.</span></span>

| <span data-ttu-id="2dccc-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="2dccc-107">Function</span></span> | <span data-ttu-id="2dccc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2dccc-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="2dccc-109">**HttpDelegateRequestEx**</span><span class="sxs-lookup"><span data-stu-id="2dccc-109">**HttpDelegateRequestEx**</span></span>](/windows/win32/api/http/nf-http-httpdelegaterequestex) | <span data-ttu-id="2dccc-110">Delegiert eine Anforderung aus der Quellanforderungswarteschlange an die Zielanforderungswarteschlange.</span><span class="sxs-lookup"><span data-stu-id="2dccc-110">Delegates a request from the source request queue to the target request queue.</span></span> |
| [<span data-ttu-id="2dccc-111">**HttpFindUrlGroupId**</span><span class="sxs-lookup"><span data-stu-id="2dccc-111">**HttpFindUrlGroupId**</span></span>](/windows/win32/api/http/nf-http-httpfindurlgroupid) | <span data-ttu-id="2dccc-112">Ruft eine URL-Gruppen-ID für eine URL und eine Anforderungswarteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="2dccc-112">Retrieves a URL group ID for a URL and a request queue.</span></span> |
| [<span data-ttu-id="2dccc-113">**HttpIsFeatureSupported**</span><span class="sxs-lookup"><span data-stu-id="2dccc-113">**HttpIsFeatureSupported**</span></span>](/windows/win32/api/http/nf-http-httpisfeaturesupported) | <span data-ttu-id="2dccc-114">Überprüft, ob ein bestimmtes Feature unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2dccc-114">Checks whether a particular feature is supported.</span></span> |

## <a name="server-session"></a><span data-ttu-id="2dccc-115">Serversitzung</span><span class="sxs-lookup"><span data-stu-id="2dccc-115">Server session</span></span>

| <span data-ttu-id="2dccc-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="2dccc-116">Function</span></span> | <span data-ttu-id="2dccc-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2dccc-117">Description</span></span> |
|-|-|
| [<span data-ttu-id="2dccc-118">**HttpCloseServerSession**</span><span class="sxs-lookup"><span data-stu-id="2dccc-118">**HttpCloseServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseserversession) | |
| [<span data-ttu-id="2dccc-119">**HttpCreateServerSession**</span><span class="sxs-lookup"><span data-stu-id="2dccc-119">**HttpCreateServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateserversession) | |
| [<span data-ttu-id="2dccc-120">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="2dccc-120">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty) | |
| [<span data-ttu-id="2dccc-121">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="2dccc-121">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) | |

## <a name="url-groups"></a><span data-ttu-id="2dccc-122">URL-Gruppen</span><span class="sxs-lookup"><span data-stu-id="2dccc-122">URL Groups</span></span>

| <span data-ttu-id="2dccc-123">Funktion</span><span class="sxs-lookup"><span data-stu-id="2dccc-123">Function</span></span> | <span data-ttu-id="2dccc-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2dccc-124">Description</span></span> |
|-|-|
| [<span data-ttu-id="2dccc-125">**HttpAddUrlToUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="2dccc-125">**HttpAddUrlToUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) | |
| [<span data-ttu-id="2dccc-126">**HttpCreateUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="2dccc-126">**HttpCreateUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) | |
| [<span data-ttu-id="2dccc-127">**HttpCloseUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="2dccc-127">**HttpCloseUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) | |
| [<span data-ttu-id="2dccc-128">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="2dccc-128">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty) | |
| [<span data-ttu-id="2dccc-129">**HttpRemoveUrlFromUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="2dccc-129">**HttpRemoveUrlFromUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) | |
| [<span data-ttu-id="2dccc-130">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="2dccc-130">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) | |

## <a name="request-queue"></a><span data-ttu-id="2dccc-131">Anforderungs-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="2dccc-131">Request Queue</span></span>

| <span data-ttu-id="2dccc-132">Funktion</span><span class="sxs-lookup"><span data-stu-id="2dccc-132">Function</span></span> | <span data-ttu-id="2dccc-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2dccc-133">Description</span></span> |
|-|-|
| [<span data-ttu-id="2dccc-134">**HttpCloseRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="2dccc-134">**HttpCloseRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcloserequestqueue) | |
| [<span data-ttu-id="2dccc-135">**HttpCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="2dccc-135">**HttpCreateRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) | |
| [<span data-ttu-id="2dccc-136">**HttpQueryRequestQueueProperty**</span><span class="sxs-lookup"><span data-stu-id="2dccc-136">**HttpQueryRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) | |
| [<span data-ttu-id="2dccc-137">**HttpSetRequestQueueProperty**</span><span class="sxs-lookup"><span data-stu-id="2dccc-137">**HttpSetRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) | |
| [<span data-ttu-id="2dccc-138">**HttpShutdownRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="2dccc-138">**HttpShutdownRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpshutdownrequestqueue) | |
| [<span data-ttu-id="2dccc-139">**HttpWaitForDemandStart**</span><span class="sxs-lookup"><span data-stu-id="2dccc-139">**HttpWaitForDemandStart**</span></span>](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) | |

## <a name="related-topics"></a><span data-ttu-id="2dccc-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2dccc-140">Related topics</span></span>

[<span data-ttu-id="2dccc-141">HTTP Server API Version 2.0-Strukturen</span><span class="sxs-lookup"><span data-stu-id="2dccc-141">HTTP Server API version 2.0 structures</span></span>](http-server-api-version-2-0-structures.md)
