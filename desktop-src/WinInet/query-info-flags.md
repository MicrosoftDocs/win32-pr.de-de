---
title: Abfrageinfoflags (WinInet. h)
description: Die folgenden Listen enthalten die von "HttpQueryInfo" und "queryInfo" verwendeten Attribute und modifiziererer.
ms.assetid: b1613193-ae03-411e-bf05-de42f471cd8c
topic_type:
- apiref
api_name:
- HTTP_QUERY_ACCEPT
- HTTP_QUERY_ACCEPT_CHARSET
- HTTP_QUERY_ACCEPT_ENCODING
- HTTP_QUERY_ACCEPT_LANGUAGE
- HTTP_QUERY_ACCEPT_RANGES
- HTTP_QUERY_AGE
- HTTP_QUERY_ALLOW
- HTTP_QUERY_AUTHORIZATION
- HTTP_QUERY_CACHE_CONTROL
- HTTP_QUERY_CONNECTION
- HTTP_QUERY_CONTENT_BASE
- HTTP_QUERY_CONTENT_DESCRIPTION
- HTTP_QUERY_CONTENT_DISPOSITION
- HTTP_QUERY_CONTENT_ENCODING
- HTTP_QUERY_CONTENT_ID
- HTTP_QUERY_CONTENT_LANGUAGE
- HTTP_QUERY_CONTENT_LENGTH
- HTTP_QUERY_CONTENT_LOCATION
- HTTP_QUERY_CONTENT_MD5
- HTTP_QUERY_CONTENT_RANGE
- HTTP_QUERY_CONTENT_TRANSFER_ENCODING
- HTTP_QUERY_CONTENT_TYPE
- HTTP_QUERY_COOKIE
- HTTP_QUERY_COST
- HTTP_QUERY_CUSTOM
- HTTP_QUERY_DATE
- HTTP_QUERY_DERIVED_FROM
- HTTP_QUERY_ECHO_HEADERS
- HTTP_QUERY_ECHO_HEADERS_CRLF
- HTTP_QUERY_ECHO_REPLY
- HTTP_QUERY_ECHO_REQUEST
- HTTP_QUERY_ETAG
- HTTP_QUERY_EXPECT
- HTTP_QUERY_EXPIRES
- HTTP_QUERY_FORWARDED
- HTTP_QUERY_FROM
- HTTP_QUERY_HOST
- HTTP_QUERY_IF_MATCH
- HTTP_QUERY_IF_MODIFIED_SINCE
- HTTP_QUERY_IF_NONE_MATCH
- HTTP_QUERY_IF_RANGE
- HTTP_QUERY_IF_UNMODIFIED_SINCE
- HTTP_QUERY_LAST_MODIFIED
- HTTP_QUERY_LINK
- HTTP_QUERY_LOCATION
- HTTP_QUERY_MAX
- HTTP_QUERY_MAX_FORWARDS
- HTTP_QUERY_MESSAGE_ID
- HTTP_QUERY_MIME_VERSION
- HTTP_QUERY_ORIG_URI
- HTTP_QUERY_PRAGMA
- HTTP_QUERY_PROXY_AUTHENTICATE
- HTTP_QUERY_PROXY_AUTHORIZATION
- HTTP_QUERY_PROXY_CONNECTION
- HTTP_QUERY_PUBLIC
- HTTP_QUERY_RANGE
- HTTP_QUERY_RAW_HEADERS
- HTTP_QUERY_RAW_HEADERS_CRLF
- HTTP_QUERY_REFERER
- HTTP_QUERY_REFRESH
- HTTP_QUERY_REQUEST_METHOD
- HTTP_QUERY_RETRY_AFTER
- HTTP_QUERY_SERVER
- HTTP_QUERY_SET_COOKIE
- HTTP_QUERY_STATUS_CODE
- HTTP_QUERY_STATUS_TEXT
- HTTP_QUERY_TITLE
- HTTP_QUERY_TRANSFER_ENCODING
- HTTP_QUERY_UNLESS_MODIFIED_SINCE
- HTTP_QUERY_UPGRADE
- HTTP_QUERY_URI
- HTTP_QUERY_USER_AGENT
- HTTP_QUERY_VARY
- HTTP_QUERY_VERSION
- HTTP_QUERY_VIA
- HTTP_QUERY_WARNING
- HTTP_QUERY_WWW_AUTHENTICATE
- HTTP_QUERY_X_CONTENT_TYPE_OPTIONS
- HTTP_QUERY_P3P
- HTTP_QUERY_X_P2P_PEERDIST
- HTTP_QUERY_TRANSLATE
- HTTP_QUERY_X_UA_COMPATIBLE
- HTTP_QUERY_DEFAULT_STYLE
- HTTP_QUERY_X_FRAME_OPTIONS
- HTTP_QUERY_X_XSS_PROTECTION
- HTTP_QUERY_FLAG_COALESCE
- HTTP_QUERY_FLAG_NUMBER
- HTTP_QUERY_FLAG_REQUEST_HEADERS
- HTTP_QUERY_FLAG_SYSTEMTIME
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f3a6166c59e158d041e730d2198f6e1b066a8b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344111"
---
# <a name="query-info-flags-winineth"></a><span data-ttu-id="459fd-103">Abfrageinfoflags (WinInet. h)</span><span class="sxs-lookup"><span data-stu-id="459fd-103">Query Info Flags (Wininet.h)</span></span>

<span data-ttu-id="459fd-104">Die folgenden Listen enthalten die von " [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) " und " [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))" verwendeten Attribute und modifiziererer.</span><span class="sxs-lookup"><span data-stu-id="459fd-104">The following lists contain the attributes and modifiers used by [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) and [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).</span></span>

<span data-ttu-id="459fd-105">Die Attributflags werden von [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (oder [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) verwendet, um anzugeben, welche Daten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="459fd-105">The attribute flags are used by [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (or [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) to indicate what data to retrieve.</span></span> <span data-ttu-id="459fd-106">Die meisten Attributflags werden direkt einem bestimmten HTTP-Header zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="459fd-106">Most of the attribute flags map directly to a specific HTTP header.</span></span> <span data-ttu-id="459fd-107">Es gibt auch einige spezielle Flags, wie z. b. [http- \_ Abfrage \_ \_ rohheader](/windows), die nicht mit einem bestimmten Header verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="459fd-107">There are also some special flags, such as [HTTP\_QUERY\_RAW\_HEADERS](/windows), that are not related to a specific header.</span></span>

<dl> <dt>

<span data-ttu-id="459fd-108"><span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**akzeptieren der HTTP- \_ Abfrage \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-108"><span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**HTTP\_QUERY\_ACCEPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-109">24</span><span class="sxs-lookup"><span data-stu-id="459fd-109">24</span></span>
</dt> <dt>



<span data-ttu-id="459fd-110">Ruft die zulässigen Medientypen für die Antwort ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-110">Retrieves the acceptable media types for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-111"><span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**Zeichensatz für HTTP- \_ Abfrage \_ Annahme \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-111"><span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**HTTP\_QUERY\_ACCEPT\_CHARSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-112">25</span><span class="sxs-lookup"><span data-stu-id="459fd-112">25</span></span>
</dt> <dt>



<span data-ttu-id="459fd-113">Ruft die zulässigen Zeichensätze für die Antwort ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-113">Retrieves the acceptable character sets for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-114"><span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**Codierung der HTTP- \_ Abfrage \_ Annahme \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-114"><span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**HTTP\_QUERY\_ACCEPT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-115">26</span><span class="sxs-lookup"><span data-stu-id="459fd-115">26</span></span>
</dt> <dt>



<span data-ttu-id="459fd-116">Ruft die zulässigen Content-Coding-Werte für die Antwort ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-116">Retrieves the acceptable content-coding values for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-117"><span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**HTTP- \_ Abfrage \_ Accept- \_ Sprache**</span><span class="sxs-lookup"><span data-stu-id="459fd-117"><span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**HTTP\_QUERY\_ACCEPT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-118">27</span><span class="sxs-lookup"><span data-stu-id="459fd-118">27</span></span>
</dt> <dt>



<span data-ttu-id="459fd-119">Ruft die zulässigen natürlichen Sprachen für die Antwort ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-119">Retrieves the acceptable natural languages for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-120"><span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**Accept-Bereiche der HTTP- \_ Abfrage \_ \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-120"><span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**HTTP\_QUERY\_ACCEPT\_RANGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-121">42</span><span class="sxs-lookup"><span data-stu-id="459fd-121">42</span></span>
</dt> <dt>



<span data-ttu-id="459fd-122">Ruft die Typen von Bereichs Anforderungen ab, die für eine Ressource akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="459fd-122">Retrieves the types of range requests that are accepted for a resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-123"><span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**HTTP- \_ Abfrage \_ Alter**</span><span class="sxs-lookup"><span data-stu-id="459fd-123"><span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**HTTP\_QUERY\_AGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-124">48</span><span class="sxs-lookup"><span data-stu-id="459fd-124">48</span></span>
</dt> <dt>



<span data-ttu-id="459fd-125">Ruft das Feld "Age Response-Header" ab, das die Schätzung des Absenders der Zeitspanne enthält, seit die Antwort auf dem Ursprungsserver generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="459fd-125">Retrieves the Age response-header field, which contains the sender's estimate of the amount of time since the response was generated at the origin server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-126"><span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**HTTP- \_ Abfrage \_ zulassen**</span><span class="sxs-lookup"><span data-stu-id="459fd-126"><span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**HTTP\_QUERY\_ALLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-127">7</span><span class="sxs-lookup"><span data-stu-id="459fd-127">7</span></span>
</dt> <dt>



<span data-ttu-id="459fd-128">Empfängt die vom Server unterstützten HTTP-Verben.</span><span class="sxs-lookup"><span data-stu-id="459fd-128">Receives the HTTP verbs supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-129"><span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**HTTP- \_ Abfrage \_ Autorisierung**</span><span class="sxs-lookup"><span data-stu-id="459fd-129"><span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**HTTP\_QUERY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-130">28</span><span class="sxs-lookup"><span data-stu-id="459fd-130">28</span></span>
</dt> <dt>



<span data-ttu-id="459fd-131">Ruft die Autorisierungs Anmelde Informationen ab, die für eine Anforderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="459fd-131">Retrieves the authorization credentials used for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-132"><span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**HTTP- \_ Abfrage \_ Cache- \_ Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="459fd-132"><span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**HTTP\_QUERY\_CACHE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-133">49</span><span class="sxs-lookup"><span data-stu-id="459fd-133">49</span></span>
</dt> <dt>



<span data-ttu-id="459fd-134">Ruft die Cache Steuerungs Direktiven ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-134">Retrieves the cache control directives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-135"><span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**HTTP- \_ Abfrage \_ Verbindung**</span><span class="sxs-lookup"><span data-stu-id="459fd-135"><span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**HTTP\_QUERY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-136">23</span><span class="sxs-lookup"><span data-stu-id="459fd-136">23</span></span>
</dt> <dt>



<span data-ttu-id="459fd-137">Ruft alle Optionen ab, die für eine bestimmte Verbindung angegeben werden und nicht von Proxys über weitere Verbindungen kommuniziert werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="459fd-137">Retrieves any options that are specified for a particular connection and must not be communicated by proxies over further connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-138"><span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**Basis für HTTP- \_ Abfrage \_ Inhalt \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-138"><span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**HTTP\_QUERY\_CONTENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-139">50</span><span class="sxs-lookup"><span data-stu-id="459fd-139">50</span></span>
</dt> <dt>



<span data-ttu-id="459fd-140">Ruft den Basis-URI (Uniform Resource Identifier) zum Auflösen relativer URLs innerhalb der Entität ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-140">Retrieves the base URI (Uniform Resource Identifier) for resolving relative URLs within the entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-141"><span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**Beschreibung der HTTP- \_ Abfrage \_ Inhalte \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-141"><span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**HTTP\_QUERY\_CONTENT\_DESCRIPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-142">4</span><span class="sxs-lookup"><span data-stu-id="459fd-142">4</span></span>
</dt> <dt>



<span data-ttu-id="459fd-143">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="459fd-143">Obsolete.</span></span> <span data-ttu-id="459fd-144">Wird nur für die Legacy Anwendungs Kompatibilität beibehalten.</span><span class="sxs-lookup"><span data-stu-id="459fd-144">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-145"><span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**HTTP- \_ Abfrage \_ Inhalts \_ Disposition**</span><span class="sxs-lookup"><span data-stu-id="459fd-145"><span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**HTTP\_QUERY\_CONTENT\_DISPOSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-146">47</span><span class="sxs-lookup"><span data-stu-id="459fd-146">47</span></span>
</dt> <dt>



<span data-ttu-id="459fd-147">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="459fd-147">Obsolete.</span></span> <span data-ttu-id="459fd-148">Wird nur für die Legacy Anwendungs Kompatibilität beibehalten.</span><span class="sxs-lookup"><span data-stu-id="459fd-148">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-149"><span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**Codierung von http- \_ Abfrage \_ Inhalten \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-149"><span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**HTTP\_QUERY\_CONTENT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-150">29</span><span class="sxs-lookup"><span data-stu-id="459fd-150">29</span></span>
</dt> <dt>



<span data-ttu-id="459fd-151">Ruft alle zusätzlichen Inhalts Codierungen ab, die auf die gesamte Ressource angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="459fd-151">Retrieves any additional content codings that have been applied to the entire resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-152"><span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**Inhalts-ID der HTTP- \_ Abfrage \_ \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-152"><span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**HTTP\_QUERY\_CONTENT\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-153">3</span><span class="sxs-lookup"><span data-stu-id="459fd-153">3</span></span>
</dt> <dt>



<span data-ttu-id="459fd-154">Ruft die Inhalts Identifikation ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-154">Retrieves the content identification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-155"><span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**Sprache für HTTP- \_ Abfrage \_ Inhalt \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-155"><span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**HTTP\_QUERY\_CONTENT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-156">6</span><span class="sxs-lookup"><span data-stu-id="459fd-156">6</span></span>
</dt> <dt>



<span data-ttu-id="459fd-157">Ruft die Sprache ab, in der sich der Inhalt befindet.</span><span class="sxs-lookup"><span data-stu-id="459fd-157">Retrieves the language that the content is in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-158"><span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**Länge der HTTP- \_ Abfrage \_ Inhalte \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-158"><span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**HTTP\_QUERY\_CONTENT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-159">5</span><span class="sxs-lookup"><span data-stu-id="459fd-159">5</span></span>
</dt> <dt>



<span data-ttu-id="459fd-160">Ruft die Größe der Ressource in Bytes ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-160">Retrieves the size of the resource, in bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-161"><span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**Speicherort der HTTP- \_ Abfrage \_ Inhalte \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-161"><span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**HTTP\_QUERY\_CONTENT\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-162">51</span><span class="sxs-lookup"><span data-stu-id="459fd-162">51</span></span>
</dt> <dt>



<span data-ttu-id="459fd-163">Ruft den Ressourcen Speicherort für die in der Nachricht eingeschlossene Entität ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-163">Retrieves the resource location for the entity enclosed in the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-164"><span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**HTTP- \_ Abfrage \_ Inhalt \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="459fd-164"><span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**HTTP\_QUERY\_CONTENT\_MD5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-165">52</span><span class="sxs-lookup"><span data-stu-id="459fd-165">52</span></span>
</dt> <dt>



<span data-ttu-id="459fd-166">Ruft einen MD5-Digest des Entitäts Texts ab, um eine End-to-End-Nachrichten Integritätsprüfung (MIC) für den Entitäts Text bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="459fd-166">Retrieves an MD5 digest of the entity-body for the purpose of providing an end-to-end message integrity check (MIC) for the entity-body.</span></span> <span data-ttu-id="459fd-167">Weitere Informationen finden Sie unter RFC1864, dem Content-MD5-Header Feld unter [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864) .</span><span class="sxs-lookup"><span data-stu-id="459fd-167">For more information, see RFC1864, The Content-MD5 Header Field, at [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-168"><span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**\_ \_ Inhalts \_ Bereich der HTTP-Abfrage**</span><span class="sxs-lookup"><span data-stu-id="459fd-168"><span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**HTTP\_QUERY\_CONTENT\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-169">53</span><span class="sxs-lookup"><span data-stu-id="459fd-169">53</span></span>
</dt> <dt>



<span data-ttu-id="459fd-170">Ruft den Speicherort im vollständigen Entitäts Text ab, in den der partielle Entitäts Text eingefügt werden soll, und die Gesamtgröße des vollständigen Entitäts Texts.</span><span class="sxs-lookup"><span data-stu-id="459fd-170">Retrieves the location in the full entity-body where the partial entity-body should be inserted and the total size of the full entity-body.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-171"><span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**Codierung der HTTP- \_ Abfrage \_ Inhalts \_ Übertragung \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-171"><span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**HTTP\_QUERY\_CONTENT\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-172">2</span><span class="sxs-lookup"><span data-stu-id="459fd-172">2</span></span>
</dt> <dt>



<span data-ttu-id="459fd-173">Empfängt die zusätzliche Inhalts Codierung, die auf die Ressource angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="459fd-173">Receives the additional content coding that has been applied to the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-174"><span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**\_Inhaltstyp für http-Abfragen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-174"><span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**HTTP\_QUERY\_CONTENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-175">1</span><span class="sxs-lookup"><span data-stu-id="459fd-175">1</span></span>
</dt> <dt>



<span data-ttu-id="459fd-176">Empfängt den Inhaltstyp der Ressource (z. b. Text/HTML).</span><span class="sxs-lookup"><span data-stu-id="459fd-176">Receives the content type of the resource (such as text/html).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-177"><span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**HTTP- \_ Abfrage \_ Cookie**</span><span class="sxs-lookup"><span data-stu-id="459fd-177"><span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**HTTP\_QUERY\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-178">44</span><span class="sxs-lookup"><span data-stu-id="459fd-178">44</span></span>
</dt> <dt>



<span data-ttu-id="459fd-179">Ruft alle Cookies ab, die der Anforderung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="459fd-179">Retrieves any cookies associated with the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-180"><span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**Kosten der HTTP- \_ Abfrage \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-180"><span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**HTTP\_QUERY\_COST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-181">15</span><span class="sxs-lookup"><span data-stu-id="459fd-181">15</span></span>
</dt> <dt>



<span data-ttu-id="459fd-182">Wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="459fd-182">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-183"><span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**\_ \_ benutzerdefinierte HTTP-Abfrage**</span><span class="sxs-lookup"><span data-stu-id="459fd-183"><span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**HTTP\_QUERY\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-184">65.535</span><span class="sxs-lookup"><span data-stu-id="459fd-184">65535</span></span>
</dt> <dt>



<span data-ttu-id="459fd-185">Bewirkt, dass [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) nach dem in *lpvbuffer* angegebenen Header Namen sucht und die Header Daten in *lpvbuffer* speichert.</span><span class="sxs-lookup"><span data-stu-id="459fd-185">Causes [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) to search for the header name specified in *lpvBuffer* and store the header data in *lpvBuffer*.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-186"><span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**Datum der HTTP- \_ Abfrage \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-186"><span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**HTTP\_QUERY\_DATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-187">9</span><span class="sxs-lookup"><span data-stu-id="459fd-187">9</span></span>
</dt> <dt>



<span data-ttu-id="459fd-188">Empfängt das Datum und die Uhrzeit, zu der die Nachricht stammt.</span><span class="sxs-lookup"><span data-stu-id="459fd-188">Receives the date and time at which the message was originated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-189"><span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**\_ \_ von abgeleitete HTTP-Abfrage \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-189"><span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**HTTP\_QUERY\_DERIVED\_FROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-190">14</span><span class="sxs-lookup"><span data-stu-id="459fd-190">14</span></span>
</dt> <dt>



<span data-ttu-id="459fd-191">Wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="459fd-191">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-192"><span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**\_ \_ Echo \_ Header der HTTP-Abfrage**</span><span class="sxs-lookup"><span data-stu-id="459fd-192"><span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**HTTP\_QUERY\_ECHO\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-193">73</span><span class="sxs-lookup"><span data-stu-id="459fd-193">73</span></span>
</dt> <dt>



<span data-ttu-id="459fd-194">Derzeit nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="459fd-194">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-195"><span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**HTTP- \_ Abfrage \_ Echo \_ Header \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="459fd-195"><span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**HTTP\_QUERY\_ECHO\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-196">74</span><span class="sxs-lookup"><span data-stu-id="459fd-196">74</span></span>
</dt> <dt>



<span data-ttu-id="459fd-197">Derzeit nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="459fd-197">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-198"><span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**HTTP- \_ Abfrage- \_ Echo \_ Antwort**</span><span class="sxs-lookup"><span data-stu-id="459fd-198"><span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**HTTP\_QUERY\_ECHO\_REPLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-199">72</span><span class="sxs-lookup"><span data-stu-id="459fd-199">72</span></span>
</dt> <dt>



<span data-ttu-id="459fd-200">Derzeit nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="459fd-200">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-201"><span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**\_ \_ Echo \_ Anforderung der HTTP-Abfrage**</span><span class="sxs-lookup"><span data-stu-id="459fd-201"><span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**HTTP\_QUERY\_ECHO\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-202">71</span><span class="sxs-lookup"><span data-stu-id="459fd-202">71</span></span>
</dt> <dt>



<span data-ttu-id="459fd-203">Derzeit nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="459fd-203">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-204"><span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**HTTP- \_ Abfrage- \_ ETag**</span><span class="sxs-lookup"><span data-stu-id="459fd-204"><span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**HTTP\_QUERY\_ETAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-205">54</span><span class="sxs-lookup"><span data-stu-id="459fd-205">54</span></span>
</dt> <dt>



<span data-ttu-id="459fd-206">Ruft das Entitätstag der zugeordneten Entität ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-206">Retrieves the entity tag for the associated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-207"><span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**erwartete http- \_ Abfrage \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-207"><span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**HTTP\_QUERY\_EXPECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-208">68</span><span class="sxs-lookup"><span data-stu-id="459fd-208">68</span></span>
</dt> <dt>



<span data-ttu-id="459fd-209">Ruft den erwarteten Header ab, der angibt, ob die Client Anwendung Antworten auf 100-Reihen erwarten soll.</span><span class="sxs-lookup"><span data-stu-id="459fd-209">Retrieves the Expect header, which indicates whether the client application should expect 100 series responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-210"><span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**HTTP- \_ Abfrage \_ läuft ab**</span><span class="sxs-lookup"><span data-stu-id="459fd-210"><span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**HTTP\_QUERY\_EXPIRES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-211">10</span><span class="sxs-lookup"><span data-stu-id="459fd-211">10</span></span>
</dt> <dt>



<span data-ttu-id="459fd-212">Empfängt das Datum und die Uhrzeit, nach der die Ressource als veraltet betrachtet werden soll.</span><span class="sxs-lookup"><span data-stu-id="459fd-212">Receives the date and time after which the resource should be considered outdated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-213"><span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**\_ \_ weitergeleitete HTTP-Abfrage**</span><span class="sxs-lookup"><span data-stu-id="459fd-213"><span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**HTTP\_QUERY\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-214">30</span><span class="sxs-lookup"><span data-stu-id="459fd-214">30</span></span>
</dt> <dt>



<span data-ttu-id="459fd-215">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="459fd-215">Obsolete.</span></span> <span data-ttu-id="459fd-216">Wird nur für die Legacy Anwendungs Kompatibilität beibehalten.</span><span class="sxs-lookup"><span data-stu-id="459fd-216">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-217"><span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**HTTP- \_ Abfrage \_ aus**</span><span class="sxs-lookup"><span data-stu-id="459fd-217"><span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**HTTP\_QUERY\_FROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-218">31</span><span class="sxs-lookup"><span data-stu-id="459fd-218">31</span></span>
</dt> <dt>



<span data-ttu-id="459fd-219">Ruft die e-Mail-Adresse für den Benutzer ab, der den anfordernden Benutzer-Agent steuert, wenn der from-Header angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="459fd-219">Retrieves the email address for the human user who controls the requesting user agent if the From header is given.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-220"><span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**HTTP- \_ Abfrage \_ Host**</span><span class="sxs-lookup"><span data-stu-id="459fd-220"><span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**HTTP\_QUERY\_HOST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-221">55</span><span class="sxs-lookup"><span data-stu-id="459fd-221">55</span></span>
</dt> <dt>



<span data-ttu-id="459fd-222">Ruft den Internet Host und die Portnummer der angeforderten Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-222">Retrieves the Internet host and port number of the resource being requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-223"><span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**HTTP- \_ Abfrage \_ bei Übereinstimmung \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-223"><span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**HTTP\_QUERY\_IF\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-224">56</span><span class="sxs-lookup"><span data-stu-id="459fd-224">56</span></span>
</dt> <dt>



<span data-ttu-id="459fd-225">Ruft den Inhalt des If-Match Anforderungs Header Felds ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-225">Retrieves the contents of the If-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-226"><span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**HTTP- \_ Abfrage \_ bei \_ Änderung \_ seit**</span><span class="sxs-lookup"><span data-stu-id="459fd-226"><span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**HTTP\_QUERY\_IF\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-227">32</span><span class="sxs-lookup"><span data-stu-id="459fd-227">32</span></span>
</dt> <dt>



<span data-ttu-id="459fd-228">Ruft den Inhalt des If-modified-since-Headers ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-228">Retrieves the contents of the If-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-229"><span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**HTTP- \_ Abfrage, \_ Wenn keiner gefunden wird \_ \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-229"><span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**HTTP\_QUERY\_IF\_NONE\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-230">57</span><span class="sxs-lookup"><span data-stu-id="459fd-230">57</span></span>
</dt> <dt>



<span data-ttu-id="459fd-231">Ruft den Inhalt des Felds "If-None-Match Request-Header" ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-231">Retrieves the contents of the If-None-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-232"><span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**HTTP- \_ Abfrage, \_ Wenn \_ Bereich**</span><span class="sxs-lookup"><span data-stu-id="459fd-232"><span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**HTTP\_QUERY\_IF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-233">58</span><span class="sxs-lookup"><span data-stu-id="459fd-233">58</span></span>
</dt> <dt>



<span data-ttu-id="459fd-234">Ruft den Inhalt des If-Range Anforderungs Header Felds ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-234">Retrieves the contents of the If-Range request-header field.</span></span> <span data-ttu-id="459fd-235">Dieser Header ermöglicht der Client Anwendung, zu überprüfen, ob die Entität, die sich auf eine partielle Kopie der Entität im Client Anwendungscache bezieht, nicht aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="459fd-235">This header enables the client application to verify that the entity related to a partial copy of the entity in the client application cache has not been updated.</span></span> <span data-ttu-id="459fd-236">Wenn die Entität nicht aktualisiert wurde, senden Sie die Teile, die die Client Anwendung fehlt.</span><span class="sxs-lookup"><span data-stu-id="459fd-236">If the entity has not been updated, send the parts that the client application is missing.</span></span> <span data-ttu-id="459fd-237">Wenn die Entität aktualisiert wurde, senden Sie die gesamte aktualisierte Entität.</span><span class="sxs-lookup"><span data-stu-id="459fd-237">If the entity has been updated, send the entire updated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-238"><span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**HTTP- \_ Abfrage, \_ Wenn \_ nicht geändert \_ seit**</span><span class="sxs-lookup"><span data-stu-id="459fd-238"><span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**HTTP\_QUERY\_IF\_UNMODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-239">59</span><span class="sxs-lookup"><span data-stu-id="459fd-239">59</span></span>
</dt> <dt>



<span data-ttu-id="459fd-240">Ruft den Inhalt des Felds "If-Unmodified-Since" des Anforderungs Headers ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-240">Retrieves the contents of the If-Unmodified-Since request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-241"><span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**\_ \_ Letzte \_ Änderung der HTTP-Abfrage**</span><span class="sxs-lookup"><span data-stu-id="459fd-241"><span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**HTTP\_QUERY\_LAST\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-242">11</span><span class="sxs-lookup"><span data-stu-id="459fd-242">11</span></span>
</dt> <dt>



<span data-ttu-id="459fd-243">Empfängt das Datum und die Uhrzeit, zu denen der Server glaubt, dass die Ressource zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="459fd-243">Receives the date and time at which the server believes the resource was last modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-244"><span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**HTTP- \_ Abfrage \_ Link**</span><span class="sxs-lookup"><span data-stu-id="459fd-244"><span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**HTTP\_QUERY\_LINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-245">16</span><span class="sxs-lookup"><span data-stu-id="459fd-245">16</span></span>
</dt> <dt>



<span data-ttu-id="459fd-246">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="459fd-246">Obsolete.</span></span> <span data-ttu-id="459fd-247">Wird nur für die Legacy Anwendungs Kompatibilität beibehalten.</span><span class="sxs-lookup"><span data-stu-id="459fd-247">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-248"><span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**HTTP- \_ Abfrage \_ Speicherort**</span><span class="sxs-lookup"><span data-stu-id="459fd-248"><span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**HTTP\_QUERY\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-249">33</span><span class="sxs-lookup"><span data-stu-id="459fd-249">33</span></span>
</dt> <dt>



<span data-ttu-id="459fd-250">Ruft den absoluten Uniform Resource Identifier (URI) ab, der in einem "Location"-Antwortheader verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="459fd-250">Retrieves the absolute Uniform Resource Identifier (URI) used in a Location response-header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-251"><span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**Max. http- \_ Abfrage \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-251"><span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**HTTP\_QUERY\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-252">78</span><span class="sxs-lookup"><span data-stu-id="459fd-252">78</span></span>
</dt> <dt>



<span data-ttu-id="459fd-253">Kein abfrageflag.</span><span class="sxs-lookup"><span data-stu-id="459fd-253">Not a query flag.</span></span> <span data-ttu-id="459fd-254">Gibt den maximalen Wert eines HTTP- \_ Abfrage \_ \* Werts an.</span><span class="sxs-lookup"><span data-stu-id="459fd-254">Indicates the maximum value of an HTTP\_QUERY\_\* value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-255"><span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**maximale HTTP-Abfrage-Weiterleitung \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-255"><span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**HTTP\_QUERY\_MAX\_FORWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-256">60</span><span class="sxs-lookup"><span data-stu-id="459fd-256">60</span></span>
</dt> <dt>



<span data-ttu-id="459fd-257">Ruft die Anzahl von Proxys oder Gateways ab, die die Anforderung an den nächsten eingehenden Server weiterleiten können.</span><span class="sxs-lookup"><span data-stu-id="459fd-257">Retrieves the number of proxies or gateways that can forward the request to the next inbound server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-258"><span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**ID der HTTP- \_ Abfrage \_ Nachricht \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-258"><span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**HTTP\_QUERY\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-259">12</span><span class="sxs-lookup"><span data-stu-id="459fd-259">12</span></span>
</dt> <dt>



<span data-ttu-id="459fd-260">Wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="459fd-260">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-261"><span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**MIME-Version der HTTP- \_ Abfrage \_ \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-261"><span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**HTTP\_QUERY\_MIME\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-262">0</span><span class="sxs-lookup"><span data-stu-id="459fd-262">0</span></span>
</dt> <dt>



<span data-ttu-id="459fd-263">Empfängt die Version des MIME-Protokolls, das zum Erstellen der Nachricht verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="459fd-263">Receives the version of the MIME protocol that was used to construct the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-264"><span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**URI der HTTP- \_ Abfrage- \_ \_ URI**</span><span class="sxs-lookup"><span data-stu-id="459fd-264"><span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**HTTP\_QUERY\_ORIG\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-265">34</span><span class="sxs-lookup"><span data-stu-id="459fd-265">34</span></span>
</dt> <dt>



<span data-ttu-id="459fd-266">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="459fd-266">Obsolete.</span></span> <span data-ttu-id="459fd-267">Wird nur für die Legacy Anwendungs Kompatibilität beibehalten.</span><span class="sxs-lookup"><span data-stu-id="459fd-267">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-268"><span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**HTTP- \_ Abfrage- \_ pragma**</span><span class="sxs-lookup"><span data-stu-id="459fd-268"><span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**HTTP\_QUERY\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-269">17</span><span class="sxs-lookup"><span data-stu-id="459fd-269">17</span></span>
</dt> <dt>



<span data-ttu-id="459fd-270">Empfängt die Implementierungs spezifischen Direktiven, die ggf. für jeden Empfänger in der Anforderungs-/Antwortkette gelten.</span><span class="sxs-lookup"><span data-stu-id="459fd-270">Receives the implementation-specific directives that might apply to any recipient along the request/response chain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-271"><span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**HTTP- \_ Abfrage \_ Proxy \_ authentifizieren**</span><span class="sxs-lookup"><span data-stu-id="459fd-271"><span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**HTTP\_QUERY\_PROXY\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-272">41</span><span class="sxs-lookup"><span data-stu-id="459fd-272">41</span></span>
</dt> <dt>



<span data-ttu-id="459fd-273">Ruft das vom Proxy zurückgegebene Authentifizierungsschema und den Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-273">Retrieves the authentication scheme and realm returned by the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-274"><span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**HTTP- \_ Abfrage \_ Proxy- \_ Autorisierung**</span><span class="sxs-lookup"><span data-stu-id="459fd-274"><span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**HTTP\_QUERY\_PROXY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-275">61</span><span class="sxs-lookup"><span data-stu-id="459fd-275">61</span></span>
</dt> <dt>



<span data-ttu-id="459fd-276">Ruft den Header ab, der verwendet wird, um den Benutzer für einen Proxy zu identifizieren, für den eine Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="459fd-276">Retrieves the header that is used to identify the user to a proxy that requires authentication.</span></span> <span data-ttu-id="459fd-277">Dieser Header kann nur abgerufen werden, bevor die Anforderung an den Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="459fd-277">This header can only be retrieved before the request is sent to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-278"><span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**HTTP- \_ Abfrage \_ Proxy \_ Verbindung**</span><span class="sxs-lookup"><span data-stu-id="459fd-278"><span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**HTTP\_QUERY\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-279">69</span><span class="sxs-lookup"><span data-stu-id="459fd-279">69</span></span>
</dt> <dt>



<span data-ttu-id="459fd-280">Ruft den Proxy-Connection-Header ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-280">Retrieves the Proxy-Connection header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-281"><span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**öffentliche http- \_ Abfrage \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-281"><span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**HTTP\_QUERY\_PUBLIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-282">8</span><span class="sxs-lookup"><span data-stu-id="459fd-282">8</span></span>
</dt> <dt>



<span data-ttu-id="459fd-283">Empfängt Methoden, die auf diesem Server verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="459fd-283">Receives methods available at this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-284"><span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**HTTP- \_ Abfrage \_ Bereich**</span><span class="sxs-lookup"><span data-stu-id="459fd-284"><span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**HTTP\_QUERY\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-285">62</span><span class="sxs-lookup"><span data-stu-id="459fd-285">62</span></span>
</dt> <dt>



<span data-ttu-id="459fd-286">Ruft den Byte Bereich einer Entität ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-286">Retrieves the byte range of an entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-287"><span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**\_ \_ Rohdaten \_ Header der HTTP-Abfrage**</span><span class="sxs-lookup"><span data-stu-id="459fd-287"><span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**HTTP\_QUERY\_RAW\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-288">21</span><span class="sxs-lookup"><span data-stu-id="459fd-288">21</span></span>
</dt> <dt>



<span data-ttu-id="459fd-289">Empfängt alle vom Server zurückgegebenen Header.</span><span class="sxs-lookup"><span data-stu-id="459fd-289">Receives all the headers returned by the server.</span></span> <span data-ttu-id="459fd-290">Jeder Header wird durch " \\ 0" beendet.</span><span class="sxs-lookup"><span data-stu-id="459fd-290">Each header is terminated by "\\0".</span></span> <span data-ttu-id="459fd-291">Eine zusätzliche " \\ 0" beendet die Liste der Header.</span><span class="sxs-lookup"><span data-stu-id="459fd-291">An additional "\\0" terminates the list of headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-292"><span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**HTTP \_ - \_ Abfrage \_ rohheader \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="459fd-292"><span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**HTTP\_QUERY\_RAW\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-293">22</span><span class="sxs-lookup"><span data-stu-id="459fd-293">22</span></span>
</dt> <dt>



<span data-ttu-id="459fd-294">Empfängt alle vom Server zurückgegebenen Header.</span><span class="sxs-lookup"><span data-stu-id="459fd-294">Receives all the headers returned by the server.</span></span> <span data-ttu-id="459fd-295">Jeder Header wird durch eine Wagen Rücklauf/Zeilenvorschub-Sequenz (CR/LF) getrennt.</span><span class="sxs-lookup"><span data-stu-id="459fd-295">Each header is separated by a carriage return/line feed (CR/LF) sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-296"><span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**HTTP- \_ Abfrage \_ Verweis**</span><span class="sxs-lookup"><span data-stu-id="459fd-296"><span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**HTTP\_QUERY\_REFERER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-297">35</span><span class="sxs-lookup"><span data-stu-id="459fd-297">35</span></span>
</dt> <dt>



<span data-ttu-id="459fd-298">Empfängt den Uniform Resource Identifier (URI) der Ressource, in der der angeforderte URI abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="459fd-298">Receives the Uniform Resource Identifier (URI) of the resource where the requested URI was obtained.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-299"><span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**Aktualisierung der HTTP- \_ Abfrage \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-299"><span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**HTTP\_QUERY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-300">46</span><span class="sxs-lookup"><span data-stu-id="459fd-300">46</span></span>
</dt> <dt>



<span data-ttu-id="459fd-301">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="459fd-301">Obsolete.</span></span> <span data-ttu-id="459fd-302">Wird nur für die Legacy Anwendungs Kompatibilität beibehalten.</span><span class="sxs-lookup"><span data-stu-id="459fd-302">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-303"><span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**HTTP- \_ Abfrage \_ Anforderungs \_ Methode**</span><span class="sxs-lookup"><span data-stu-id="459fd-303"><span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**HTTP\_QUERY\_REQUEST\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-304">45</span><span class="sxs-lookup"><span data-stu-id="459fd-304">45</span></span>
</dt> <dt>



<span data-ttu-id="459fd-305">Empfängt das HTTP-Verb, das in der Anforderung verwendet wird, in der Regel Get oder Post.</span><span class="sxs-lookup"><span data-stu-id="459fd-305">Receives the HTTP verb that is being used in the request, typically GET or POST.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-306"><span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**Wiederholung der HTTP- \_ Abfrage \_ \_ nach**</span><span class="sxs-lookup"><span data-stu-id="459fd-306"><span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**HTTP\_QUERY\_RETRY\_AFTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-307">36</span><span class="sxs-lookup"><span data-stu-id="459fd-307">36</span></span>
</dt> <dt>



<span data-ttu-id="459fd-308">Ruft die Zeitspanne ab, die erwartet wird, dass der Dienst nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="459fd-308">Retrieves the amount of time the service is expected to be unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-309"><span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**HTTP- \_ Abfrage \_ Server**</span><span class="sxs-lookup"><span data-stu-id="459fd-309"><span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**HTTP\_QUERY\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-310">37</span><span class="sxs-lookup"><span data-stu-id="459fd-310">37</span></span>
</dt> <dt>



<span data-ttu-id="459fd-311">Ruft Daten über die Software ab, die vom Ursprungsserver verwendet wird, um die Anforderung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="459fd-311">Retrieves data about the software used by the origin server to handle the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-312"><span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**HTTP- \_ Abfrage \_ Satz \_ Cookie**</span><span class="sxs-lookup"><span data-stu-id="459fd-312"><span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**HTTP\_QUERY\_SET\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-313">43</span><span class="sxs-lookup"><span data-stu-id="459fd-313">43</span></span>
</dt> <dt>



<span data-ttu-id="459fd-314">Empfängt den Wert des Cookies, der für die Anforderung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="459fd-314">Receives the value of the cookie set for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-315"><span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**\_ \_ Status \_ Code der HTTP-Abfrage**</span><span class="sxs-lookup"><span data-stu-id="459fd-315"><span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**HTTP\_QUERY\_STATUS\_CODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-316">19</span><span class="sxs-lookup"><span data-stu-id="459fd-316">19</span></span>
</dt> <dt>



<span data-ttu-id="459fd-317">Empfängt den vom Server zurückgegebenen Statuscode.</span><span class="sxs-lookup"><span data-stu-id="459fd-317">Receives the status code returned by the server.</span></span> <span data-ttu-id="459fd-318">Weitere Informationen und eine Liste möglicher Werte finden Sie unter [**http-Status Codes**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="459fd-318">For more information and a list of possible values, see [**HTTP Status Codes**](http-status-codes.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-319"><span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**Text der HTTP- \_ Abfrage \_ Status \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-319"><span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**HTTP\_QUERY\_STATUS\_TEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-320">20</span><span class="sxs-lookup"><span data-stu-id="459fd-320">20</span></span>
</dt> <dt>



<span data-ttu-id="459fd-321">Empfängt jeden zusätzlichen Text, der vom Server in der Antwort Zeile zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="459fd-321">Receives any additional text returned by the server on the response line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-322"><span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**HTTP- \_ Abfrage \_ Titel**</span><span class="sxs-lookup"><span data-stu-id="459fd-322"><span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**HTTP\_QUERY\_TITLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-323">38</span><span class="sxs-lookup"><span data-stu-id="459fd-323">38</span></span>
</dt> <dt>



<span data-ttu-id="459fd-324">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="459fd-324">Obsolete.</span></span> <span data-ttu-id="459fd-325">Wird nur für die Legacy Anwendungs Kompatibilität beibehalten.</span><span class="sxs-lookup"><span data-stu-id="459fd-325">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-326"><span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**HTTP- \_ Abfrage \_ Übertragungs \_ Codierung**</span><span class="sxs-lookup"><span data-stu-id="459fd-326"><span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**HTTP\_QUERY\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-327">63</span><span class="sxs-lookup"><span data-stu-id="459fd-327">63</span></span>
</dt> <dt>



<span data-ttu-id="459fd-328">Ruft den Typ der Transformation ab, die auf den Nachrichtentext angewendet wurde, sodass er sicher zwischen dem Absender und dem Empfänger übertragen werden kann.</span><span class="sxs-lookup"><span data-stu-id="459fd-328">Retrieves the type of transformation that has been applied to the message body so it can be safely transferred between the sender and recipient.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-329"><span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**HTTP- \_ Abfrage, \_ sofern nicht \_ geändert \_ seit**</span><span class="sxs-lookup"><span data-stu-id="459fd-329"><span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**HTTP\_QUERY\_UNLESS\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-330">70</span><span class="sxs-lookup"><span data-stu-id="459fd-330">70</span></span>
</dt> <dt>



<span data-ttu-id="459fd-331">Ruft den-nicht-Modified-Since-Header ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-331">Retrieves the Unless-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-332"><span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**Upgrade der HTTP- \_ Abfrage \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-332"><span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**HTTP\_QUERY\_UPGRADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-333">64</span><span class="sxs-lookup"><span data-stu-id="459fd-333">64</span></span>
</dt> <dt>



<span data-ttu-id="459fd-334">Ruft die zusätzlichen Kommunikationsprotokolle ab, die vom Server unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="459fd-334">Retrieves the additional communication protocols that are supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-335"><span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**HTTP- \_ Abfrage- \_ URI**</span><span class="sxs-lookup"><span data-stu-id="459fd-335"><span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**HTTP\_QUERY\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-336">13</span><span class="sxs-lookup"><span data-stu-id="459fd-336">13</span></span>
</dt> <dt>



<span data-ttu-id="459fd-337">Empfängt einige oder alle URIs (Uniform Resource Identifier), durch die die Request-URI-Ressource identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="459fd-337">Receives some or all of the Uniform Resource Identifiers (URIs) by which the Request-URI resource can be identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-338"><span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**Benutzer-Agent für HTTP- \_ Abfragen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-338"><span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**HTTP\_QUERY\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-339">39</span><span class="sxs-lookup"><span data-stu-id="459fd-339">39</span></span>
</dt> <dt>



<span data-ttu-id="459fd-340">Ruft Daten über den Benutzer-Agent ab, von dem die Anforderung stammt.</span><span class="sxs-lookup"><span data-stu-id="459fd-340">Retrieves data about the user agent that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-341"><span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**HTTP- \_ Abfrage \_ variiert**</span><span class="sxs-lookup"><span data-stu-id="459fd-341"><span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**HTTP\_QUERY\_VARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-342">65</span><span class="sxs-lookup"><span data-stu-id="459fd-342">65</span></span>
</dt> <dt>



<span data-ttu-id="459fd-343">Ruft den Header ab, der angibt, dass die Entität mithilfe einer servergesteuerten Aushandlung aus einer Reihe von verfügbaren Darstellungen der Antwort ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="459fd-343">Retrieves the header that indicates that the entity was selected from a number of available representations of the response using server-driven negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-344"><span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**HTTP- \_ Abfrage \_ Version**</span><span class="sxs-lookup"><span data-stu-id="459fd-344"><span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**HTTP\_QUERY\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-345">18</span><span class="sxs-lookup"><span data-stu-id="459fd-345">18</span></span>
</dt> <dt>



<span data-ttu-id="459fd-346">Empfängt den letzten Antwort Code, der vom Server zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="459fd-346">Receives the last response code returned by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-347"><span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**HTTP- \_ Abfrage \_ über**</span><span class="sxs-lookup"><span data-stu-id="459fd-347"><span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**HTTP\_QUERY\_VIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-348">66</span><span class="sxs-lookup"><span data-stu-id="459fd-348">66</span></span>
</dt> <dt>



<span data-ttu-id="459fd-349">Ruft die zwischen Protokolle und Empfänger zwischen dem Benutzer-Agent und dem Server bei Anforderungen sowie zwischen dem Ursprungsserver und dem Client bei Antworten ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-349">Retrieves the intermediate protocols and recipients between the user agent and the server on requests, and between the origin server and the client on responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-350"><span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**HTTP- \_ Abfrage \_ Warnung**</span><span class="sxs-lookup"><span data-stu-id="459fd-350"><span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**HTTP\_QUERY\_WARNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-351">67</span><span class="sxs-lookup"><span data-stu-id="459fd-351">67</span></span>
</dt> <dt>



<span data-ttu-id="459fd-352">Ruft zusätzliche Daten über den Status einer Antwort ab, die möglicherweise nicht durch den Antwortstatus Code reflektiert werden.</span><span class="sxs-lookup"><span data-stu-id="459fd-352">Retrieves additional data about the status of a response that might not be reflected by the response status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-353"><span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**HTTP- \_ Abfrage \_ www- \_ Authentifizierung**</span><span class="sxs-lookup"><span data-stu-id="459fd-353"><span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**HTTP\_QUERY\_WWW\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-354">40</span><span class="sxs-lookup"><span data-stu-id="459fd-354">40</span></span>
</dt> <dt>



<span data-ttu-id="459fd-355">Ruft das vom Server zurückgegebene Authentifizierungsschema und den Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-355">Retrieves the authentication scheme and realm returned by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-356"><span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**Optionen für HTTP- \_ Abfrage \_ X- \_ \_ Inhaltstyp \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-356"><span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**HTTP\_QUERY\_X\_CONTENT\_TYPE\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-357">79</span><span class="sxs-lookup"><span data-stu-id="459fd-357">79</span></span>
</dt> <dt>



<span data-ttu-id="459fd-358">Ruft den Header Wert "X-Content-Type-Options" ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-358">Retrieves the X-Content-Type-Options header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-359"><span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**HTTP- \_ Abfrage \_ P3P**</span><span class="sxs-lookup"><span data-stu-id="459fd-359"><span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**HTTP\_QUERY\_P3P**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-360">80</span><span class="sxs-lookup"><span data-stu-id="459fd-360">80</span></span>
</dt> <dt>



<span data-ttu-id="459fd-361">Ruft den P3P-Header Wert ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-361">Retrieves the P3P header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-362"><span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**HTTP- \_ Abfrage \_ X P2P- \_ \_ Peer**</span><span class="sxs-lookup"><span data-stu-id="459fd-362"><span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**HTTP\_QUERY\_X\_P2P\_PEERDIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-363">81</span><span class="sxs-lookup"><span data-stu-id="459fd-363">81</span></span>
</dt> <dt>



<span data-ttu-id="459fd-364">Ruft den X-P2P-Peer--Header Wert ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-364">Retrieves the X-P2P-PeerDist header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-365"><span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**HTTP- \_ Abfrage Übersetzung \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-365"><span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**HTTP\_QUERY\_TRANSLATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-366">82</span><span class="sxs-lookup"><span data-stu-id="459fd-366">82</span></span>
</dt> <dt>



<span data-ttu-id="459fd-367">Ruft den Wert des Translation-Headers ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-367">Retrieves the translate header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-368"><span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**HTTP- \_ Abfrage \_ X UA- \_ \_ kompatibel**</span><span class="sxs-lookup"><span data-stu-id="459fd-368"><span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**HTTP\_QUERY\_X\_UA\_COMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-369">83</span><span class="sxs-lookup"><span data-stu-id="459fd-369">83</span></span>
</dt> <dt>



<span data-ttu-id="459fd-370">Ruft den X-UA-kompatiblen Header Wert ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-370">Retrieves the X-UA-Compatible header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-371"><span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**\_ \_ Standard \_ Stil der HTTP-Abfrage**</span><span class="sxs-lookup"><span data-stu-id="459fd-371"><span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**HTTP\_QUERY\_DEFAULT\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-372">84</span><span class="sxs-lookup"><span data-stu-id="459fd-372">84</span></span>
</dt> <dt>



<span data-ttu-id="459fd-373">Ruft den Default-Style-Header Wert ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-373">Retrieves the Default-Style header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-374"><span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**Optionen für HTTP- \_ Abfrage \_ X- \_ Frame \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-374"><span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**HTTP\_QUERY\_X\_FRAME\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-375">85</span><span class="sxs-lookup"><span data-stu-id="459fd-375">85</span></span>
</dt> <dt>



<span data-ttu-id="459fd-376">Ruft den X-Frame-Options-Header Wert ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-376">Retrieves the X-Frame-Options header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-377"><span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**HTTP- \_ Abfrage \_ X- \_ XSS- \_ Schutz**</span><span class="sxs-lookup"><span data-stu-id="459fd-377"><span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**HTTP\_QUERY\_X\_XSS\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-378">86</span><span class="sxs-lookup"><span data-stu-id="459fd-378">86</span></span>
</dt> <dt>



<span data-ttu-id="459fd-379">Ruft den X-XSS-Protection-Header Wert ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-379">Retrieves the X-XSS-Protection header value.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="459fd-380">Die Modifiziererflags werden zusammen mit einem attributflag verwendet, um die Anforderung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="459fd-380">The modifier flags are used in conjunction with an attribute flag to modify the request.</span></span> <span data-ttu-id="459fd-381">Modifiziererflags ändern entweder das Format der zurückgegebenen Daten oder geben an, wo [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (oder [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) nach den Daten suchen soll.</span><span class="sxs-lookup"><span data-stu-id="459fd-381">Modifier flags either modify the format of the data returned or indicate where [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (or [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) should search for the data.</span></span>

<dl> <dt>

<span data-ttu-id="459fd-382"><span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**HTTP \_ - \_ abfrageflag- \_ COALESCE**</span><span class="sxs-lookup"><span data-stu-id="459fd-382"><span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**HTTP\_QUERY\_FLAG\_COALESCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-383">0x10000000</span><span class="sxs-lookup"><span data-stu-id="459fd-383">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="459fd-384">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="459fd-384">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-385"><span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**HTTP \_ - \_ abfrageflagnummer \_**</span><span class="sxs-lookup"><span data-stu-id="459fd-385"><span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**HTTP\_QUERY\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-386">0x20000000</span><span class="sxs-lookup"><span data-stu-id="459fd-386">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="459fd-387">Gibt die Daten als 32-Bit-Zahl für Header zurück, deren Wert eine Zahl ist, z. b. der Statuscode.</span><span class="sxs-lookup"><span data-stu-id="459fd-387">Returns the data as a 32-bit number for headers whose value is a number, such as the status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-388"><span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**HTTP-Abfrage Kennzeichen- \_ \_ \_ Anforderungs \_ Header**</span><span class="sxs-lookup"><span data-stu-id="459fd-388"><span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**HTTP\_QUERY\_FLAG\_REQUEST\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-389">0x80000000</span><span class="sxs-lookup"><span data-stu-id="459fd-389">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="459fd-390">Fragt nur Anforderungs Header ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-390">Queries request headers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="459fd-391"><span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**HTTP \_ - \_ abfrageflag \_ SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="459fd-391"><span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**HTTP\_QUERY\_FLAG\_SYSTEMTIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459fd-392">0x40000000</span><span class="sxs-lookup"><span data-stu-id="459fd-392">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="459fd-393">Gibt den Header Wert als [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur zurück, die die Anwendung nicht benötigt, um die Daten zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="459fd-393">Returns the header value as a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure, which does not require the application to parse the data.</span></span> <span data-ttu-id="459fd-394">Verwenden Sie für Header, deren Wert eine Datums-/uhrzeitzeile ist, z. b. "Last-modified-time".</span><span class="sxs-lookup"><span data-stu-id="459fd-394">Use for headers whose value is a date/time string, such as "Last-Modified-Time".</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="459fd-395">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="459fd-395">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="459fd-396">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="459fd-396">WinINet does not support server implementations.</span></span> <span data-ttu-id="459fd-397">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="459fd-397">In addition, it should not be used from a service.</span></span> <span data-ttu-id="459fd-398">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="459fd-398">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="459fd-399">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="459fd-399">Requirements</span></span>



| <span data-ttu-id="459fd-400">Anforderung</span><span class="sxs-lookup"><span data-stu-id="459fd-400">Requirement</span></span> | <span data-ttu-id="459fd-401">Wert</span><span class="sxs-lookup"><span data-stu-id="459fd-401">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="459fd-402">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="459fd-402">Minimum supported client</span></span><br/> | <span data-ttu-id="459fd-403">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="459fd-403">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="459fd-404">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="459fd-404">Minimum supported server</span></span><br/> | <span data-ttu-id="459fd-405">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="459fd-405">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="459fd-406">Header</span><span class="sxs-lookup"><span data-stu-id="459fd-406">Header</span></span><br/>                   | <dl> <span data-ttu-id="459fd-407"><dt>Wininet. h</dt></span><span class="sxs-lookup"><span data-stu-id="459fd-407"><dt>Wininet.h</dt></span></span> </dl> |



 

