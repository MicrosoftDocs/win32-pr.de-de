---
title: HTTP_RESPONSE (http. h)
description: Die Version der HTTP- \_ Antwort Struktur ist abhängig von der Version der Anforderungs Warteschlange, die der HTTP-Server-API Version 1,0-Anforderungs Warteschlange verwendet wird. Dies ist eine HTTP- \_ Anforderung \_ v1-Struktur. Http-Server-API Version 2,0 Anforderungs Warteschlange Dies ist eine HTTP- \_ Anforderung \_ v2-Struktur.
ms.assetid: F94646C0-7293-4543-842B-F08D8C7E2247
keywords:
- HTTP_RESPONSE
- HTTP_RESPONSE
- PHTTP_RESPONSE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a8445021aa61b94ae83a55937b1db5ca4e3c577
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391782"
---
# <a name="http_response"></a><span data-ttu-id="fbbab-106">HTTP- \_ Antwort</span><span class="sxs-lookup"><span data-stu-id="fbbab-106">HTTP\_RESPONSE</span></span>

<span data-ttu-id="fbbab-107">Die Version der **http- \_ Antwort** Struktur ist abhängig von der Version der Anforderungs Warteschlange, die wie folgt verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="fbbab-107">The version of the **HTTP\_RESPONSE** structure is dependent on the version of the request queue used as follows:</span></span>

-   <span data-ttu-id="fbbab-108">Http Server-API, Version 1,0, Anforderungs Warteschlange: Dies ist eine [**http- \_ Anforderung \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="fbbab-108">HTTP Server API Version 1.0 request queue: This is an [**HTTP\_REQUEST\_V1**](/windows/desktop/api/Http/ns-http-http_request_v1) structure.</span></span>
-   <span data-ttu-id="fbbab-109">Http-Server-API, Version 2,0, Anforderungs Warteschlange: Dies ist eine [**http \_ Request \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="fbbab-109">HTTP Server API Version 2.0 request queue: This is an [**HTTP\_REQUEST\_V2**](/windows/desktop/api/Http/ns-http-http_request_v2) structure.</span></span>

<span data-ttu-id="fbbab-110">Verwenden Sie [**http- \_ Anforderungen \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) und [**http \_ Request \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) nicht direkt in Ihrem Code. bei Verwendung der **http- \_ Antwort** wird stattdessen sichergestellt, dass die richtige Version der Struktur basierend auf der Version der Anforderungs Warteschlange verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fbbab-110">Do not use [**HTTP\_REQUEST\_V1**](/windows/desktop/api/Http/ns-http-http_request_v1) and [**HTTP\_REQUEST\_V2**](/windows/desktop/api/Http/ns-http-http_request_v2) directly in your code; using **HTTP\_RESPONSE** instead ensures the proper version of the structure is used based on the version of the request queue.</span></span>


```C++
typedef HTTP_REQUEST_V1 HTTP_RESPONSE;
typedef HTTP_REQUEST_V2 HTTP_RESPONSE;
typedef HTTP_RESPONSE* PHTTP_RESPONSE;
```



<dl> <dt>

<span data-ttu-id="fbbab-111">**HTTP- \_ Antwort**</span><span class="sxs-lookup"><span data-stu-id="fbbab-111">**HTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="fbbab-112">Die Anforderung erfolgte aus einer v1-Anforderungs Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="fbbab-112">Request was from a v1 request queue.</span></span>

</dd> <dt>

<span data-ttu-id="fbbab-113">**HTTP- \_ Antwort**</span><span class="sxs-lookup"><span data-stu-id="fbbab-113">**HTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="fbbab-114">Die Anforderung erfolgte aus einer v2-Anforderungs Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="fbbab-114">Request was from a v2 request queue.</span></span>

</dd> <dt>

<span data-ttu-id="fbbab-115">**Phttp- \_ Antwort**</span><span class="sxs-lookup"><span data-stu-id="fbbab-115">**PHTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="fbbab-116">Zeiger auf eine **http- \_ Antwort** Struktur.</span><span class="sxs-lookup"><span data-stu-id="fbbab-116">Pointer to an **HTTP\_RESPONSE** structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fbbab-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbbab-117">Requirements</span></span>



| <span data-ttu-id="fbbab-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbbab-118">Requirement</span></span> | <span data-ttu-id="fbbab-119">Wert</span><span class="sxs-lookup"><span data-stu-id="fbbab-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fbbab-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fbbab-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fbbab-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbbab-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fbbab-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fbbab-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fbbab-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbbab-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fbbab-124">Header</span><span class="sxs-lookup"><span data-stu-id="fbbab-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbbab-125"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbbab-125"><dt>Http.h</dt></span></span> </dl> |



 

 





