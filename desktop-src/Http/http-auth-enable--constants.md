---
title: HTTP_AUTH_ENABLE_ Konstanten (http. h)
description: Definieren Sie Authentifizierungs Schemas, die für eine URL-Gruppe aktiviert werden können.
ms.assetid: db22645f-c9e4-427e-b3d5-91d568aec7c5
topic_type:
- apiref
api_name:
- HTTP_AUTH_ENABLE_BASIC
- HTTP_AUTH_ENABLE_DIGEST
- HTTP_AUTH_ENABLE_KERBEROS
- HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING
- HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL
- HTTP_AUTH_ENABLE_NTLM
- HTTP_AUTH_ENABLE_NEGOTIATE
- HTTP_AUTH_ENABLE_ALL
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6462a4f9d884244f460c4bf7714b45d3e17600c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478939"
---
# <a name="http_auth_enable_-constants"></a><span data-ttu-id="7b168-103">HTTP-Authentifizierung \_ \_ Aktivieren von \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="7b168-103">HTTP\_AUTH\_ENABLE\_ Constants</span></span>

<span data-ttu-id="7b168-104">Die **http-Authentifizierung \_ \_ enable** -Konstanten definieren Authentifizierungs Schemas, die für eine URL-Gruppe aktiviert werden können.</span><span class="sxs-lookup"><span data-stu-id="7b168-104">The **HTTP\_AUTH\_ENABLE** constants define authentication schemes that can be enabled on a URL Group.</span></span>

<span data-ttu-id="7b168-105">Diese Konstanten werden in der [**http- \_ Server \_ Authentifizierungs \_ Info**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) -Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="7b168-105">These constants are used in the [**HTTP\_SERVER\_AUTHENTICATION\_INFO**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="7b168-106"><span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**HTTP-Authentifizierung ( \_ \_ Basic) aktivieren \_**</span><span class="sxs-lookup"><span data-stu-id="7b168-106"><span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**HTTP\_AUTH\_ENABLE\_BASIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7b168-107">Das Standard Authentifizierungsschema ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7b168-107">The Basic authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b168-108"><span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**HTTP-Authentifizierung \_ \_ enable \_ Digest**</span><span class="sxs-lookup"><span data-stu-id="7b168-108"><span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**HTTP\_AUTH\_ENABLE\_DIGEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7b168-109">Das Digest-Authentifizierungsschema ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7b168-109">The Digest authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b168-110"><span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**HTTP-Authentifizierung \_ \_ Aktivieren von \_ Kerberos**</span><span class="sxs-lookup"><span data-stu-id="7b168-110"><span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**HTTP\_AUTH\_ENABLE\_KERBEROS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7b168-111">Das Kerberos-Authentifizierungsschema ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7b168-111">The Kerberos authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b168-112"><span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**HTTP \_ auth \_ Ex- \_ Flag \_ enable \_ Kerberos \_ Credential \_ Caching**</span><span class="sxs-lookup"><span data-stu-id="7b168-112"><span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**HTTP\_AUTH\_EX\_FLAG\_ENABLE\_KERBEROS\_CREDENTIAL\_CACHING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7b168-113">Das Zwischenspeichern der Kerberos-Anmelde Informationen ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7b168-113">Kerberos credential caching is enabled.</span></span>

<span data-ttu-id="7b168-114">**Windows Server 2003 und früher:** Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7b168-114">**Windows Server 2003 and before:** Not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b168-115"><span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**HTTP \_ auth \_ Ex \_ Flag zum \_ erfassen \_ von Anmelde Informationen**</span><span class="sxs-lookup"><span data-stu-id="7b168-115"><span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**HTTP\_AUTH\_EX\_FLAG\_CAPTURE\_CREDENTIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7b168-116">Die HTTP-Server-API erfasst die Identität des Aufrufers und verwendet diese für die Authentifizierung nur für Aushandlungs-und Kerberos-Schemata</span><span class="sxs-lookup"><span data-stu-id="7b168-116">The HTTP Server API captures the caller identity and uses it for authentication for Negotiate and Kerberos schemes only.</span></span>

<span data-ttu-id="7b168-117">**Windows Server 2003 und früher:** Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7b168-117">**Windows Server 2003 and before:** Not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b168-118"><span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**HTTP-Authentifizierung \_ \_ Aktivieren von \_ NTLM**</span><span class="sxs-lookup"><span data-stu-id="7b168-118"><span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**HTTP\_AUTH\_ENABLE\_NTLM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7b168-119">Das NTLM-Authentifizierungsschema ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7b168-119">The NTLM authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b168-120"><span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**HTTP-Authentifizierung " \_ \_ aushandeln aktivieren" \_**</span><span class="sxs-lookup"><span data-stu-id="7b168-120"><span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**HTTP\_AUTH\_ENABLE\_NEGOTIATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7b168-121">Das Aushandlungs Authentifizierungsschema ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7b168-121">The Negotiate authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b168-122"><span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**HTTP-Authentifizierung \_ \_ \_ Alle aktivieren**</span><span class="sxs-lookup"><span data-stu-id="7b168-122"><span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**HTTP\_AUTH\_ENABLE\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7b168-123">Alle Authentifizierungs Schemas sind aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7b168-123">All authentication schemes are enabled.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b168-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b168-124">Requirements</span></span>



| <span data-ttu-id="7b168-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b168-125">Requirement</span></span> | <span data-ttu-id="7b168-126">Wert</span><span class="sxs-lookup"><span data-stu-id="7b168-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7b168-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b168-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7b168-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b168-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7b168-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b168-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7b168-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b168-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7b168-131">Header</span><span class="sxs-lookup"><span data-stu-id="7b168-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b168-132"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b168-132"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b168-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b168-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b168-134">HTTP-Server-API, Version 2,0, Konstanten</span><span class="sxs-lookup"><span data-stu-id="7b168-134">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="7b168-135">**HTTP- \_ Server \_ Authentifizierungs \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="7b168-135">**HTTP\_SERVER\_AUTHENTICATION\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
</dt> <dt>

[<span data-ttu-id="7b168-136">**Httptarturlgroupproperty**</span><span class="sxs-lookup"><span data-stu-id="7b168-136">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="7b168-137">**Httpsetserversessionproperty**</span><span class="sxs-lookup"><span data-stu-id="7b168-137">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="7b168-138">**Httpqueryurlgroupproperty**</span><span class="sxs-lookup"><span data-stu-id="7b168-138">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="7b168-139">**Httpqueryserversessionproperty**</span><span class="sxs-lookup"><span data-stu-id="7b168-139">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





