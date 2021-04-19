---
title: HTTP_RESPONSE_FLAG_ Konstanten (http. h)
description: Definieren Sie die Optionen zum Konfigurieren von Antworten in der HTTP-Server-API.
ms.assetid: bcb59457-fd22-4166-8a72-ba85209ec8c7
topic_type:
- apiref
api_name:
- HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96b7c34d453c1b9bbe45cf2c85ad268b414f3439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337503"
---
# <a name="http_response_flag_-constants"></a><span data-ttu-id="76f94-103">HTTP \_ - \_ antwortflag- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="76f94-103">HTTP\_RESPONSE\_FLAG\_ Constants</span></span>

<span data-ttu-id="76f94-104">Die **http \_ - \_ antwortflag \_** -Konstanten definieren Optionen zum Konfigurieren von Antworten in der HTTP-Server-API.</span><span class="sxs-lookup"><span data-stu-id="76f94-104">The **HTTP\_RESPONSE\_FLAG\_** constants define options to configure responses in the HTTP Server API.</span></span>

<span data-ttu-id="76f94-105">Diese Konstanten werden im **Flags** -Member der HTTP- [**\_ Antwort \_ v1**](/windows/desktop/api/Http/ns-http-http_response_v1) -Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="76f94-105">These constants are used in the **Flags** member of the [**HTTP\_RESPONSE\_V1**](/windows/desktop/api/Http/ns-http-http_response_v1) structure.</span></span>

<dl> <dt>

<span data-ttu-id="76f94-106"><span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**HTTP- \_ Antwort Kennzeichen \_ \_ mehrere \_ Codierungen \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="76f94-106"><span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**HTTP\_RESPONSE\_FLAG\_MULTIPLE\_ENCODINGS\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76f94-107">Andere Codierungen als das Identitäts Formular sind für diese Ressource verfügbar.</span><span class="sxs-lookup"><span data-stu-id="76f94-107">Encodings other than identity form are available for this resource.</span></span> <span data-ttu-id="76f94-108">Dieses Flag wird ignoriert, wenn die Anwendung nicht zum Zwischenspeichern aufgefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="76f94-108">This flag is ignored if the application has not asked for the response to be cached.</span></span> <span data-ttu-id="76f94-109">Sie wird als Hinweis für die HTTP-Server-API für die Aushandlung von Inhalten verwendet, wenn Sie aus dem Kernel-Antwort Cache bedient wird.</span><span class="sxs-lookup"><span data-stu-id="76f94-109">It's used as a hint to the HTTP Server API for content negotiation when serving from the kernel response cache.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76f94-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76f94-110">Requirements</span></span>



| <span data-ttu-id="76f94-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76f94-111">Requirement</span></span> | <span data-ttu-id="76f94-112">Wert</span><span class="sxs-lookup"><span data-stu-id="76f94-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="76f94-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76f94-113">Minimum supported client</span></span><br/> | <span data-ttu-id="76f94-114">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76f94-114">Windows 7 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="76f94-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76f94-115">Minimum supported server</span></span><br/> | <span data-ttu-id="76f94-116">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76f94-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="76f94-117">Header</span><span class="sxs-lookup"><span data-stu-id="76f94-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="76f94-118"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="76f94-118"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76f94-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76f94-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76f94-120">HTTP-Server-API, Version 2,0, Konstanten</span><span class="sxs-lookup"><span data-stu-id="76f94-120">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="76f94-121">**HTTP- \_ Antwort \_ v1**</span><span class="sxs-lookup"><span data-stu-id="76f94-121">**HTTP\_RESPONSE\_V1**</span></span>](/windows/desktop/api/Http/ns-http-http_response_v1)
</dt> </dl>

 

 





