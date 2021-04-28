---
title: Kernelmoduscache
description: Kernelmoduscache
ms.assetid: f9a46ff4-779b-4b3a-b8f5-1ae10a3c0a61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83c409b00da03c0550899f5d26c4e6a0fa215118
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090888"
---
# <a name="kernel-mode-cache"></a><span data-ttu-id="28a0d-103">Kernelmoduscache</span><span class="sxs-lookup"><span data-stu-id="28a0d-103">Kernel Mode Cache</span></span>

<span data-ttu-id="28a0d-104">Mit der HTTP Server-API Version 2.0 können Anwendungen Antworten mit statischem Inhalt im Kernelmodus zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="28a0d-104">The HTTP Server version 2.0 API allows applications to cache responses with static content in kernel mode.</span></span> <span data-ttu-id="28a0d-105">Eine höhere Leistung wird erzielt, wenn Anforderungen aus dem Kernelcache bedient werden, ohne in den Benutzermodus zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="28a0d-105">Increased performance is achieved when requests are served from the kernel cache without transitioning to user mode.</span></span>

<span data-ttu-id="28a0d-106">Die HTTP-Server-API wendet die entsprechenden Eigenschaftenkonfigurationen auf alle Anforderungen an, die vom Kernelcache bereitgestellt werden, einschließlich der Protokollierung von Antworten.</span><span class="sxs-lookup"><span data-stu-id="28a0d-106">The HTTP Server API applies the appropriate property configurations to all requests served from the kernel cache, including logging responses.</span></span> <span data-ttu-id="28a0d-107">Anforderungen, die eine Authentifizierung erfordern, werden jedoch nicht aus dem Cache bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="28a0d-107">Requests that require authentication, however, will not be served from the cache.</span></span>

<span data-ttu-id="28a0d-108">Die HTTP-Server-API beschränkt den Cache im Kernelmodus auf Anforderungen, die die folgenden Bedingungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="28a0d-108">The HTTP Server API limits the kernel mode cache to requests that meet the following conditions:</span></span>

-   <span data-ttu-id="28a0d-109">Das Anforderungsverb ist GET, und die gesamte Anforderung wird empfangen.</span><span class="sxs-lookup"><span data-stu-id="28a0d-109">The request verb is GET and the entire request is received.</span></span>
-   <span data-ttu-id="28a0d-110">Die Anforderung darf keinen Entitätskörper haben.</span><span class="sxs-lookup"><span data-stu-id="28a0d-110">The request must not have an entity body.</span></span>
-   <span data-ttu-id="28a0d-111">Das HTTP-Protokoll ist Version 1.0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="28a0d-111">The HTTP protocol is version 1.0 or later.</span></span>
-   <span data-ttu-id="28a0d-112">Der Header "Translate: f" ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="28a0d-112">The "Translate: f " header is not present.</span></span>
-   <span data-ttu-id="28a0d-113">Es sind keine anderen Header als "Expect: 100-Continue" vorhanden.</span><span class="sxs-lookup"><span data-stu-id="28a0d-113">Expect headers other than "Expect: 100-Continue" are not present.</span></span>
-   <span data-ttu-id="28a0d-114">Der Autorisierungsheader ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="28a0d-114">The authorization header is not present.</span></span>
-   <span data-ttu-id="28a0d-115">Die Range- If-Range-Header sind nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="28a0d-115">The Range and If-Range headers are not present.</span></span>

<span data-ttu-id="28a0d-116">Zusätzlich zu den Einschränkungen für die Anforderung muss die Antwort auch die folgenden Bedingungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="28a0d-116">In addition to the restrictions on the request, the response must also meet the following conditions:</span></span>

-   <span data-ttu-id="28a0d-117">Die Antwortgröße ist standardmäßig auf 256 KB beschränkt.</span><span class="sxs-lookup"><span data-stu-id="28a0d-117">Response size is limited to 256 KB, by default.</span></span> <span data-ttu-id="28a0d-118">Um die Größe der zwischengespeicherten Antwort zu ändern, legen Sie den **Registrierungswert UriMaxUriBytes** auf die erforderliche Anzahl von Bytes fest.</span><span class="sxs-lookup"><span data-stu-id="28a0d-118">To change the size of the response that is cached, set the **UriMaxUriBytes** registry value to the required number of bytes.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   <span data-ttu-id="28a0d-119">Die gesamte Antwort muss in einem einzigen Aufruf von [**HttpSendHttpResponse bereitgestellt werden.**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)</span><span class="sxs-lookup"><span data-stu-id="28a0d-119">The entire response must be provided in a single call to [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).</span></span>
-   <span data-ttu-id="28a0d-120">Der Datumsheader in der Antwort darf nicht unterdrückt werden.</span><span class="sxs-lookup"><span data-stu-id="28a0d-120">The date header on the response must not be suppressed.</span></span>
-   <span data-ttu-id="28a0d-121">Wenn der Zuletzt geänderte Header vorhanden ist, muss der Wert des Headers die richtige Syntax aufweisen.</span><span class="sxs-lookup"><span data-stu-id="28a0d-121">If the last-modified header is present, the value of the header must have the correct syntax.</span></span> <span data-ttu-id="28a0d-122">Der Zeitwert in diesem Header wird für die Überprüfung des Cachesteuerelements verwendet.</span><span class="sxs-lookup"><span data-stu-id="28a0d-122">The time value in this header is used for cache control verification.</span></span>
-   <span data-ttu-id="28a0d-123">Der Kernelmoduscache verfügt über genügend Speicherplatz, um die Antwort zu speichern.</span><span class="sxs-lookup"><span data-stu-id="28a0d-123">The kernel mode cache has enough space left to store the response.</span></span>

<span data-ttu-id="28a0d-124">Standardmäßig ist der Kernelmodus-Antwortcache aktiviert.</span><span class="sxs-lookup"><span data-stu-id="28a0d-124">By default, kernel mode response cache is enabled.</span></span> <span data-ttu-id="28a0d-125">Wenn eine der oben aufgeführten Bedingungen für die Anforderung oder Antwort nicht erfüllt ist, wird die Antwort gesendet, aber nicht zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="28a0d-125">If any of the conditions for the request or response listed above are not met, the response will be sent, but it will not be cached.</span></span> <span data-ttu-id="28a0d-126">In der HTTP Server-API version 2.0 enthält [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) einen optionalen *pCachePolicy-Parameter,* um die [**HTTP CACHE \_ \_ POLICY-Struktur**](/windows/desktop/api/Http/ns-http-http_cache_policy) zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="28a0d-126">In HTTP Server version 2.0 API, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) includes an optional *pCachePolicy* parameter to pass the [**HTTP\_CACHE\_POLICY**](/windows/desktop/api/Http/ns-http-http_cache_policy) structure.</span></span> <span data-ttu-id="28a0d-127">Anwendungen verwenden die Cacherichtlinienstruktur, um den Cache zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="28a0d-127">Applications use the cache policy structure to configure the cache.</span></span>

 

 




