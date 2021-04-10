---
title: Kernelmoduscache
description: .
ms.assetid: f9a46ff4-779b-4b3a-b8f5-1ae10a3c0a61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9264535a58c033d66fd3fcc39988a292afc2a27f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037502"
---
# <a name="kernel-mode-cache"></a><span data-ttu-id="ebbb3-103">Kernelmoduscache</span><span class="sxs-lookup"><span data-stu-id="ebbb3-103">Kernel Mode Cache</span></span>

<span data-ttu-id="ebbb3-104">Die HTTP-Server Version 2,0-API ermöglicht Anwendungen das Zwischenspeichern von Antworten mit statischen Inhalten im Kernel Modus.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-104">The HTTP Server version 2.0 API allows applications to cache responses with static content in kernel mode.</span></span> <span data-ttu-id="ebbb3-105">Eine bessere Leistung wird erzielt, wenn Anforderungen aus dem Kernel Cache bereitgestellt werden, ohne in den Benutzermodus übergeht.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-105">Increased performance is achieved when requests are served from the kernel cache without transitioning to user mode.</span></span>

<span data-ttu-id="ebbb3-106">Die HTTP-Server-API wendet die entsprechenden Eigenschaften Konfigurationen auf alle Anforderungen aus dem Kernel Cache an, einschließlich Protokollierungs Antworten.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-106">The HTTP Server API applies the appropriate property configurations to all requests served from the kernel cache, including logging responses.</span></span> <span data-ttu-id="ebbb3-107">Anforderungen, die eine Authentifizierung erfordern, werden jedoch nicht aus dem Cache bedient.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-107">Requests that require authentication, however, will not be served from the cache.</span></span>

<span data-ttu-id="ebbb3-108">Die HTTP-Server-API schränkt den Kernelmoduscache auf Anforderungen ein, die die folgenden Bedingungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="ebbb3-108">The HTTP Server API limits the kernel mode cache to requests that meet the following conditions:</span></span>

-   <span data-ttu-id="ebbb3-109">Das Anforderungs Verb lautet Get, und die gesamte Anforderung wird empfangen.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-109">The request verb is GET and the entire request is received.</span></span>
-   <span data-ttu-id="ebbb3-110">Die Anforderung darf keinen Entitäts Text enthalten.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-110">The request must not have an entity body.</span></span>
-   <span data-ttu-id="ebbb3-111">Das HTTP-Protokoll ist Version 1,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-111">The HTTP protocol is version 1.0 or later.</span></span>
-   <span data-ttu-id="ebbb3-112">Der Header "Translation: f" ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-112">The "Translate: f " header is not present.</span></span>
-   <span data-ttu-id="ebbb3-113">Erwarten Sie, dass keine anderen Header als "erwartet: 100-Continue" vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-113">Expect headers other than "Expect: 100-Continue" are not present.</span></span>
-   <span data-ttu-id="ebbb3-114">Der Autorisierungs Header ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-114">The authorization header is not present.</span></span>
-   <span data-ttu-id="ebbb3-115">Die Header Range und If-Range sind nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-115">The Range and If-Range headers are not present.</span></span>

<span data-ttu-id="ebbb3-116">Zusätzlich zu den Einschränkungen für die Anforderung muss die Antwort auch die folgenden Bedingungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="ebbb3-116">In addition to the restrictions on the request, the response must also meet the following conditions:</span></span>

-   <span data-ttu-id="ebbb3-117">Die Antwort Größe ist standardmäßig auf 256 KB beschränkt.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-117">Response size is limited to 256 KB, by default.</span></span> <span data-ttu-id="ebbb3-118">Um die Größe der zwischengespeicherten Antwort zu ändern, legen Sie für den Registrierungs Wert **urimaxuribytes** die erforderliche Anzahl von Bytes fest.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-118">To change the size of the response that is cached, set the **UriMaxUriBytes** registry value to the required number of bytes.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   <span data-ttu-id="ebbb3-119">Die gesamte Antwort muss in einem einzelnen [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)-Befehl angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-119">The entire response must be provided in a single call to [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).</span></span>
-   <span data-ttu-id="ebbb3-120">Der Date-Header für die Antwort darf nicht unterdrückt werden.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-120">The date header on the response must not be suppressed.</span></span>
-   <span data-ttu-id="ebbb3-121">Wenn der Last-modified-Header vorhanden ist, muss der Wert des-Headers über die korrekte Syntax verfügen.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-121">If the last-modified header is present, the value of the header must have the correct syntax.</span></span> <span data-ttu-id="ebbb3-122">Der Uhrzeitwert in diesem Header wird zur Überprüfung der Cache Steuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-122">The time value in this header is used for cache control verification.</span></span>
-   <span data-ttu-id="ebbb3-123">Der Kernelmoduscache verfügt über genügend Speicherplatz zum Speichern der Antwort.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-123">The kernel mode cache has enough space left to store the response.</span></span>

<span data-ttu-id="ebbb3-124">Standardmäßig ist der Kernel Modus-Antwort Cache aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-124">By default, kernel mode response cache is enabled.</span></span> <span data-ttu-id="ebbb3-125">Wenn eine der Bedingungen für die oben aufgeführte Anforderung oder Antwort nicht erfüllt ist, wird die Antwort gesendet, Sie wird jedoch nicht zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-125">If any of the conditions for the request or response listed above are not met, the response will be sent, but it will not be cached.</span></span> <span data-ttu-id="ebbb3-126">In der HTTP-Server Version 2,0-API enthält [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) einen optionalen *pcachepolicy* -Parameter, um die [**http- \_ Cache \_ Richtlinien**](/windows/desktop/api/Http/ns-http-http_cache_policy) Struktur zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-126">In HTTP Server version 2.0 API, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) includes an optional *pCachePolicy* parameter to pass the [**HTTP\_CACHE\_POLICY**](/windows/desktop/api/Http/ns-http-http_cache_policy) structure.</span></span> <span data-ttu-id="ebbb3-127">Anwendungen verwenden die Cache Richtlinien Struktur, um den Cache zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ebbb3-127">Applications use the cache policy structure to configure the cache.</span></span>

 

 




