---
description: Diese Attribute und modifiziererer werden von WinHttpQueryHeaders verwendet.
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: Abfrageinfoflags (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9ffc8f4ba4a947fe6fb277617c99460c43ffb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042479"
---
# <a name="query-info-flags-winhttph"></a><span data-ttu-id="19bf1-103">Abfrageinfoflags (WinHTTP. h)</span><span class="sxs-lookup"><span data-stu-id="19bf1-103">Query Info Flags (Winhttp.h)</span></span>

<span data-ttu-id="19bf1-104">Diese Attribute und modifiziererer werden von [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)verwendet.</span><span class="sxs-lookup"><span data-stu-id="19bf1-104">These attributes and modifiers are used by [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

<span data-ttu-id="19bf1-105">Die Attributflags werden von [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) verwendet, um anzugeben, welche Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="19bf1-105">The attribute flags are used by [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) to indicate what information to retrieve.</span></span> <span data-ttu-id="19bf1-106">Die meisten Attributflags werden direkt einem bestimmten HTTP-Header zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="19bf1-106">Most of the attribute flags map directly to a specific HTTP header.</span></span> <span data-ttu-id="19bf1-107">Außerdem gibt es einige spezielle Flags, z. b. WinHTTP- \_ Abfrage \_ Rohdaten \_ Header, die nicht mit einem bestimmten Header verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="19bf1-107">There are also some special flags, such as WINHTTP\_QUERY\_RAW\_HEADERS, that are not related to a specific header.</span></span>

<dl> <dt>

<span data-ttu-id="19bf1-108"><span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**WinHTTP- \_ Abfrage \_ Annahme**</span><span class="sxs-lookup"><span data-stu-id="19bf1-108"><span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**WINHTTP\_QUERY\_ACCEPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-109">Ruft die zulässigen Medientypen für die Antwort ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-109">Retrieves the acceptable media types for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-110"><span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**Zeichensatz für WinHTTP- \_ Abfrage \_ Annahme \_**</span><span class="sxs-lookup"><span data-stu-id="19bf1-110"><span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP\_QUERY\_ACCEPT\_CHARSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-111">Ruft die zulässigen Zeichensätze für die Antwort ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-111">Retrieves the acceptable character sets for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-112"><span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**WinHTTP- \_ Abfrage \_ Accept- \_ Codierung**</span><span class="sxs-lookup"><span data-stu-id="19bf1-112"><span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**WINHTTP\_QUERY\_ACCEPT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-113">Ruft die zulässigen Content-Coding-Werte für die Antwort ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-113">Retrieves the acceptable content-coding values for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-114"><span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**WinHTTP \_ Query \_ Accept- \_ Sprache**</span><span class="sxs-lookup"><span data-stu-id="19bf1-114"><span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**WINHTTP\_QUERY\_ACCEPT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-115">Ruft die zulässigen natürlichen Sprachen für die Antwort ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-115">Retrieves the acceptable natural languages for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-116"><span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**Accept-Bereiche der WinHTTP- \_ Abfrage \_ \_**</span><span class="sxs-lookup"><span data-stu-id="19bf1-116"><span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**WINHTTP\_QUERY\_ACCEPT\_RANGES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-117">Ruft die Typen von Bereichs Anforderungen ab, die für eine Ressource akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="19bf1-117">Retrieves the types of range requests that are accepted for a resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-118"><span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**WinHTTP- \_ Abfrage \_ Alter**</span><span class="sxs-lookup"><span data-stu-id="19bf1-118"><span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**WINHTTP\_QUERY\_AGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-119">Ruft das Feld "Age Response-Header" ab, das die Schätzung des Absenders der Zeitspanne enthält, seit die Antwort auf dem Ursprungsserver generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="19bf1-119">Retrieves the Age response-header field, which contains the sender's estimate of the amount of time since the response was generated at the originating server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-120"><span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WinHTTP- \_ Abfrage \_ zulassen**</span><span class="sxs-lookup"><span data-stu-id="19bf1-120"><span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WINHTTP\_QUERY\_ALLOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-121">Empfängt die vom Server unterstützten [*http-Verb*](glossary.md)s.</span><span class="sxs-lookup"><span data-stu-id="19bf1-121">Receives the [*HTTP verb*](glossary.md)s supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-122"><span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**\_ \_ Authentifizierungs \_ Informationen für die WinHTTP-Abfrage**</span><span class="sxs-lookup"><span data-stu-id="19bf1-122"><span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**WINHTTP\_QUERY\_AUTHENTICATION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-123">Ruft den Authentication-Info-Header ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-123">Retrieves the Authentication-Info header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-124"><span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**WinHTTP- \_ Abfrage \_ Autorisierung**</span><span class="sxs-lookup"><span data-stu-id="19bf1-124"><span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**WINHTTP\_QUERY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-125">Ruft die Autorisierungs Anmelde Informationen ab, die für eine Anforderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19bf1-125">Retrieves the authorization credentials used for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-126"><span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**WinHTTP- \_ Abfrage \_ Cache- \_ Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="19bf1-126"><span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**WINHTTP\_QUERY\_CACHE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-127">Ruft die Cache Steuerungs Direktiven ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-127">Retrieves the cache control directives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-128"><span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**WinHTTP- \_ Abfrage \_ Verbindung**</span><span class="sxs-lookup"><span data-stu-id="19bf1-128"><span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**WINHTTP\_QUERY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-129">Ruft alle Optionen ab, die für eine bestimmte Verbindung angegeben werden und nicht von Proxys über weitere Verbindungen kommuniziert werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="19bf1-129">Retrieves any options that are specified for a particular connection and must not be communicated by proxies over further connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-130"><span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**Basis für WinHTTP- \_ Abfrage \_ Inhalt \_**</span><span class="sxs-lookup"><span data-stu-id="19bf1-130"><span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**WINHTTP\_QUERY\_CONTENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-131">Ruft den Basis Uniform Resource Identifier (URI) ab, um relative URLs innerhalb der Entität aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="19bf1-131">Retrieves the base Uniform Resource Identifier (URI) to resolve relative URLs within the entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-132"><span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**Beschreibung der WinHTTP- \_ Abfrage \_ Inhalte \_**</span><span class="sxs-lookup"><span data-stu-id="19bf1-132"><span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**WINHTTP\_QUERY\_CONTENT\_DESCRIPTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-133">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="19bf1-133">Obsolete.</span></span> <span data-ttu-id="19bf1-134">Wird für die Legacy Anwendungs Kompatibilität beibehalten.</span><span class="sxs-lookup"><span data-stu-id="19bf1-134">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-135"><span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**\_ \_ Inhalts \_ Disposition für WinHTTP-Abfrage**</span><span class="sxs-lookup"><span data-stu-id="19bf1-135"><span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**WINHTTP\_QUERY\_CONTENT\_DISPOSITION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-136">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="19bf1-136">Obsolete.</span></span> <span data-ttu-id="19bf1-137">Wird für die Legacy Anwendungs Kompatibilität beibehalten.</span><span class="sxs-lookup"><span data-stu-id="19bf1-137">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-138"><span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**Codierung von WinHTTP- \_ Abfrage \_ Inhalten \_**</span><span class="sxs-lookup"><span data-stu-id="19bf1-138"><span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**WINHTTP\_QUERY\_CONTENT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-139">Ruft zusätzliche Inhalts Codierungen ab, die auf die gesamte Ressource angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="19bf1-139">Retrieves additional content coding that has been applied to the entire resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-140"><span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**WinHTTP- \_ Abfrage \_ Inhalts- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="19bf1-140"><span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**WINHTTP\_QUERY\_CONTENT\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-141">Ruft die Inhalts Identifikation ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-141">Retrieves the content identification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-142"><span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**\_ \_ Inhalts \_ Sprache für WinHTTP-Abfrage**</span><span class="sxs-lookup"><span data-stu-id="19bf1-142"><span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**WINHTTP\_QUERY\_CONTENT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-143">Ruft die Sprache ab, in der der Inhalt geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="19bf1-143">Retrieves the language that the content is written in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-144"><span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**\_ \_ Inhalts \_ Länge der WinHTTP-Abfrage**</span><span class="sxs-lookup"><span data-stu-id="19bf1-144"><span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**WINHTTP\_QUERY\_CONTENT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-145">Ruft die Größe der Ressource in Bytes ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-145">Retrieves the size of the resource, in bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-146"><span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**Speicherort für WinHTTP- \_ Abfrage \_ Inhalt \_**</span><span class="sxs-lookup"><span data-stu-id="19bf1-146"><span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**WINHTTP\_QUERY\_CONTENT\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-147">Ruft den Ressourcen Speicherort für die in der Nachricht eingeschlossene Entität ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-147">Retrieves the resource location for the entity enclosed in the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-148"><span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**Inhalt der WinHTTP- \_ Abfrage \_ \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="19bf1-148"><span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**WINHTTP\_QUERY\_CONTENT\_MD5**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-149">Ruft einen MD5-Digest des Entitäts Texts ab, um eine End-to-End-Nachrichten Integritätsprüfung für den Entitäts Text bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="19bf1-149">Retrieves an MD5 digest of the entity body for the purpose of providing an end-to-end message integrity check for the entity body.</span></span> <span data-ttu-id="19bf1-150">Weitere Informationen finden Sie unter [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).</span><span class="sxs-lookup"><span data-stu-id="19bf1-150">For more information, see [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-151"><span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**\_ \_ Inhalts \_ Bereich der WinHTTP-Abfrage**</span><span class="sxs-lookup"><span data-stu-id="19bf1-151"><span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**WINHTTP\_QUERY\_CONTENT\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-152">Ruft den Speicherort im vollständigen Entitäts Text ab, in den der partielle Entitäts Text eingefügt werden soll, und die Gesamtgröße des vollständigen Entitäts Texts.</span><span class="sxs-lookup"><span data-stu-id="19bf1-152">Retrieves the location in the full entity body where the partial entity body should be inserted and the total size of the full entity body.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-153"><span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**Codierung der \_ \_ Inhalts \_ Übertragung \_ mit WinHTTP-Abfragen**</span><span class="sxs-lookup"><span data-stu-id="19bf1-153"><span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**WINHTTP\_QUERY\_CONTENT\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-154">Ruft eine Codierungs Transformation ab, die auf einen Entitäts Text anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="19bf1-154">Retrieves an encoding transformation applicable to an entity-body.</span></span> <span data-ttu-id="19bf1-155">Möglicherweise wurde Sie bereits angewendet, muss ggf. angewendet werden, oder Sie kann optional sein.</span><span class="sxs-lookup"><span data-stu-id="19bf1-155">It may already have been applied, may need to be applied, or may be optionally applicable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-156"><span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**WinHTTP \_ - \_ Abfrage \_ Inhaltstyp**</span><span class="sxs-lookup"><span data-stu-id="19bf1-156"><span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**WINHTTP\_QUERY\_CONTENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-157">Empfängt den Inhaltstyp der Ressource, z. b. Text oder HTML.</span><span class="sxs-lookup"><span data-stu-id="19bf1-157">Receives the content type of the resource, such as text or html.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-158"><span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**WinHTTP- \_ Abfrage \_ Cookie**</span><span class="sxs-lookup"><span data-stu-id="19bf1-158"><span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**WINHTTP\_QUERY\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-159">Ruft alle Cookies ab, die der Anforderung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="19bf1-159">Retrieves any cookies associated with the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-160"><span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**WinHTTP- \_ Abfrage \_ Kosten**</span><span class="sxs-lookup"><span data-stu-id="19bf1-160"><span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**WINHTTP\_QUERY\_COST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-161">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19bf1-161">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-162"><span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WinHTTP- \_ Abfrage \_ Benutzer definiert**</span><span class="sxs-lookup"><span data-stu-id="19bf1-162"><span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WINHTTP\_QUERY\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-163">Bewirkt, dass [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) nach dem im *pwszName* -Parameter angegebenen Header Namen sucht und die Header Informationen in *lpBuffer* speichert.</span><span class="sxs-lookup"><span data-stu-id="19bf1-163">Causes [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) to search for the header name specified in the *pwszName* parameter and store the header information in *lpBuffer*.</span></span> <span data-ttu-id="19bf1-164">Eine Anwendung kann das **Timeout für \_ das \_ empfangen \_ \_ der WinHTTP-Option** verwenden, um die maximale Zeit zu begrenzen, die diese Abfrage auf den Empfang aller Header wartet.</span><span class="sxs-lookup"><span data-stu-id="19bf1-164">An application can use **WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT** to limit the maximum time this query waits for all headers to be received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-165"><span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**Datum der WinHTTP- \_ Abfrage \_**</span><span class="sxs-lookup"><span data-stu-id="19bf1-165"><span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**WINHTTP\_QUERY\_DATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-166">Empfängt das Datum und die Uhrzeit, zu der die Nachricht stammt.</span><span class="sxs-lookup"><span data-stu-id="19bf1-166">Receives the date and time at which the message was originated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-167"><span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**\_ \_ von abgeleitete WinHTTP-Abfrage \_**</span><span class="sxs-lookup"><span data-stu-id="19bf1-167"><span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**WINHTTP\_QUERY\_DERIVED\_FROM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-168">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19bf1-168">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-169"><span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**WinHTTP- \_ Abfrage- \_ ETag**</span><span class="sxs-lookup"><span data-stu-id="19bf1-169"><span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**WINHTTP\_QUERY\_ETAG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-170">Ruft das Entitätstag der zugeordneten Entität ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-170">Retrieves the entity tag for the associated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-171"><span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WinHTTP- \_ Abfrage \_ erwartet**</span><span class="sxs-lookup"><span data-stu-id="19bf1-171"><span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WINHTTP\_QUERY\_EXPECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-172">Ruft den erwarteten Header ab, der angibt, ob die Client Anwendung Antworten auf 100-Reihen erwarten soll.</span><span class="sxs-lookup"><span data-stu-id="19bf1-172">Retrieves the Expect header, which indicates whether the client application should expect 100 series responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-173"><span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**WinHTTP- \_ Abfrage \_ läuft ab**</span><span class="sxs-lookup"><span data-stu-id="19bf1-173"><span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**WINHTTP\_QUERY\_EXPIRES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-174">Empfängt das Datum und die Uhrzeit, nach der die Ressource als veraltet betrachtet werden soll.</span><span class="sxs-lookup"><span data-stu-id="19bf1-174">Receives the date and time after which the resource should be considered outdated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-175"><span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**weitergeleitete WinHTTP- \_ Abfrage \_**</span><span class="sxs-lookup"><span data-stu-id="19bf1-175"><span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**WINHTTP\_QUERY\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-176">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="19bf1-176">Obsolete.</span></span> <span data-ttu-id="19bf1-177">Wird für die Legacy Anwendungs Kompatibilität beibehalten.</span><span class="sxs-lookup"><span data-stu-id="19bf1-177">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-178"><span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**WinHTTP- \_ Abfrage \_ aus**</span><span class="sxs-lookup"><span data-stu-id="19bf1-178"><span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**WINHTTP\_QUERY\_FROM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-179">Ruft die e-Mail-Adresse für den Benutzer ab, der den anfordernden [*Benutzer-Agent*](glossary.md) steuert, wenn der from-Header angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="19bf1-179">Retrieves the e-mail address for the user who controls the requesting [*user agent*](glossary.md) if the From header is given.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-180"><span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**WinHTTP- \_ Abfrage \_ Host**</span><span class="sxs-lookup"><span data-stu-id="19bf1-180"><span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**WINHTTP\_QUERY\_HOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-181">Ruft den Internet Host und die Portnummer der angeforderten Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-181">Retrieves the Internet host and port number of the resource being requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-182"><span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**WinHTTP- \_ Abfrage \_ bei \_ Treffer**</span><span class="sxs-lookup"><span data-stu-id="19bf1-182"><span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**WINHTTP\_QUERY\_IF\_MATCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-183">Ruft den Inhalt des If-Match Anforderungs Header Felds ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-183">Retrieves the contents of the If-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-184"><span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**WinHTTP- \_ Abfrage \_ bei \_ Änderung \_ seit**</span><span class="sxs-lookup"><span data-stu-id="19bf1-184"><span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**WINHTTP\_QUERY\_IF\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-185">Ruft den Inhalt des If-modified-since-Headers ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-185">Retrieves the contents of the If-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-186"><span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**WinHTTP- \_ Abfrage, \_ Wenn \_ keine \_ Entsprechung vorliegt**</span><span class="sxs-lookup"><span data-stu-id="19bf1-186"><span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**WINHTTP\_QUERY\_IF\_NONE\_MATCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-187">Ruft den Inhalt des Felds "If-None-Match Request-Header" ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-187">Retrieves the contents of the If-None-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-188"><span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**WinHTTP- \_ Abfrage, \_ Wenn \_ Bereich**</span><span class="sxs-lookup"><span data-stu-id="19bf1-188"><span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**WINHTTP\_QUERY\_IF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-189">Ruft den Inhalt des If-Range Anforderungs Header Felds ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-189">Retrieves the contents of the If-Range request-header field.</span></span> <span data-ttu-id="19bf1-190">Dieser Header ermöglicht der Client Anwendung, zu überprüfen, ob die Entität, die sich auf eine partielle Kopie der Entität im Cache der Client Anwendung bezieht, nicht aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="19bf1-190">This header allows the client application to check if the entity related to a partial copy of the entity in the client application's cache has not been updated.</span></span> <span data-ttu-id="19bf1-191">Wenn die Entität nicht aktualisiert wurde, senden Sie die Teile, die die Client Anwendung fehlt.</span><span class="sxs-lookup"><span data-stu-id="19bf1-191">If the entity has not been updated, send the parts that the client application is missing.</span></span> <span data-ttu-id="19bf1-192">Wenn die Entität aktualisiert wurde, senden Sie die gesamte aktualisierte Entität.</span><span class="sxs-lookup"><span data-stu-id="19bf1-192">If the entity has been updated, send the entire updated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-193"><span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**WinHTTP- \_ Abfrage, \_ Wenn \_ nicht geändert \_ seit**</span><span class="sxs-lookup"><span data-stu-id="19bf1-193"><span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**WINHTTP\_QUERY\_IF\_UNMODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-194">Ruft den Inhalt des Felds "If-Unmodified-Since" des Anforderungs Headers ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-194">Retrieves the contents of the If-Unmodified-Since request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-195"><span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**WinHTTP- \_ Abfrage \_ Link**</span><span class="sxs-lookup"><span data-stu-id="19bf1-195"><span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**WINHTTP\_QUERY\_LINK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-196">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="19bf1-196">Obsolete.</span></span> <span data-ttu-id="19bf1-197">Wird für die Legacy Anwendungs Kompatibilität beibehalten.</span><span class="sxs-lookup"><span data-stu-id="19bf1-197">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-198"><span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**\_ \_ Letzte \_ Änderung der WinHTTP-Abfrage**</span><span class="sxs-lookup"><span data-stu-id="19bf1-198"><span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**WINHTTP\_QUERY\_LAST\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-199">Empfängt das Datum und die Uhrzeit der letzten Änderung der Ressource.</span><span class="sxs-lookup"><span data-stu-id="19bf1-199">Receives the date and time at which the resource was last modified.</span></span> <span data-ttu-id="19bf1-200">Das Datum und die Uhrzeit werden vom Server bestimmt.</span><span class="sxs-lookup"><span data-stu-id="19bf1-200">The date and time are determined by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-201"><span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**WinHTTP- \_ Abfrage \_ Speicherort**</span><span class="sxs-lookup"><span data-stu-id="19bf1-201"><span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**WINHTTP\_QUERY\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-202">Ruft den absoluten URI ab, der in einem "Location"-Antwortheader verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="19bf1-202">Retrieves the absolute URI used in a Location response-header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-203"><span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**Max. WinHTTP- \_ Abfrage \_**</span><span class="sxs-lookup"><span data-stu-id="19bf1-203"><span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**WINHTTP\_QUERY\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-204">Gibt den maximalen Wert eines WinHTTP- \_ Abfrage \_ \* Werts an.</span><span class="sxs-lookup"><span data-stu-id="19bf1-204">Indicates the maximum value of a WINHTTP\_QUERY\_\* value.</span></span> <span data-ttu-id="19bf1-205">Kein abfrageflag.</span><span class="sxs-lookup"><span data-stu-id="19bf1-205">Not a query flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-206"><span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**maximale WinHTTP-Abfrage-Weiterleitung \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="19bf1-206"><span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**WINHTTP\_QUERY\_MAX\_FORWARDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-207">Ruft die Anzahl von Proxys oder Gateways ab, die die Anforderung an den nächsten eingehenden Server weiterleiten können.</span><span class="sxs-lookup"><span data-stu-id="19bf1-207">Retrieves the number of proxies or gateways that can forward the request to the next inbound server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-208"><span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**WinHTTP- \_ Abfrage nach \_ richten- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="19bf1-208"><span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**WINHTTP\_QUERY\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-209">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19bf1-209">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-210"><span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**WinHTTP \_ Query- \_ MIME- \_ Version**</span><span class="sxs-lookup"><span data-stu-id="19bf1-210"><span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**WINHTTP\_QUERY\_MIME\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-211">Empfängt die Version des Multipurpose Internet Mail Extensions (MIME)-Protokolls, das zum Erstellen der Nachricht verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="19bf1-211">Receives the version of the Multipurpose Internet Mail Extensions (MIME) protocol that was used to construct the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-212"><span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**URI für WinHTTP- \_ Abfrage- \_ \_ URI**</span><span class="sxs-lookup"><span data-stu-id="19bf1-212"><span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**WINHTTP\_QUERY\_ORIG\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-213">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="19bf1-213">Obsolete.</span></span> <span data-ttu-id="19bf1-214">Wird für die Legacy Anwendungs Kompatibilität beibehalten.</span><span class="sxs-lookup"><span data-stu-id="19bf1-214">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-215"><span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**WinHTTP- \_ Abfrage- \_ pragma**</span><span class="sxs-lookup"><span data-stu-id="19bf1-215"><span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**WINHTTP\_QUERY\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-216">Empfängt die Implementierungs spezifischen Direktiven, die ggf. für jeden Empfänger in der Anforderungs-/Antwortkette gelten.</span><span class="sxs-lookup"><span data-stu-id="19bf1-216">Receives the implementation-specific directives that might apply to any recipient along the request/response chain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-217"><span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**Authentifizieren des WinHTTP- \_ Abfrage \_ Proxys \_**</span><span class="sxs-lookup"><span data-stu-id="19bf1-217"><span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**WINHTTP\_QUERY\_PROXY\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-218">Ruft das vom Proxy zurückgegebene Authentifizierungsschema und den Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-218">Retrieves the authentication scheme and realm returned by the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-219"><span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**WinHTTP- \_ Abfrage \_ Proxy- \_ Autorisierung**</span><span class="sxs-lookup"><span data-stu-id="19bf1-219"><span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**WINHTTP\_QUERY\_PROXY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-220">Ruft den Header ab, der verwendet wird, um den Benutzer für einen Proxy zu identifizieren, für den eine Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="19bf1-220">Retrieves the header that is used to identify the user to a proxy that requires authentication.</span></span> <span data-ttu-id="19bf1-221">Dieser Header kann nur abgerufen werden, bevor die Anforderung an den Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="19bf1-221">This header can only be retrieved before the request is sent to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-222"><span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**WinHTTP- \_ Abfrage \_ Proxy \_ Verbindung**</span><span class="sxs-lookup"><span data-stu-id="19bf1-222"><span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**WINHTTP\_QUERY\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-223">Ruft den Proxy-Connection-Header ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-223">Retrieves the Proxy-Connection header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-224"><span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**Unterstützung für WinHTTP- \_ Abfrage \_ Proxy \_**</span><span class="sxs-lookup"><span data-stu-id="19bf1-224"><span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**WINHTTP\_QUERY\_PROXY\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-225">Ruft den Proxy-Support-Header ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-225">Retrieves the Proxy-Support header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-226"><span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**WinHTTP- \_ Abfrage \_ öffentlich**</span><span class="sxs-lookup"><span data-stu-id="19bf1-226"><span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**WINHTTP\_QUERY\_PUBLIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-227">Empfängt auf diesem Server verfügbare HTTP-Verben.</span><span class="sxs-lookup"><span data-stu-id="19bf1-227">Receives HTTP verbs available at this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-228"><span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**WinHTTP- \_ Abfrage \_ Bereich**</span><span class="sxs-lookup"><span data-stu-id="19bf1-228"><span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**WINHTTP\_QUERY\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-229">Ruft den Byte Bereich einer Entität ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-229">Retrieves the byte range of an entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-230"><span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**unformatierte WinHTTP- \_ Abfrage \_ \_ Header**</span><span class="sxs-lookup"><span data-stu-id="19bf1-230"><span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**WINHTTP\_QUERY\_RAW\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-231">Empfängt alle vom Server zurückgegebenen Header.</span><span class="sxs-lookup"><span data-stu-id="19bf1-231">Receives all the headers returned by the server.</span></span> <span data-ttu-id="19bf1-232">Jeder Header wird durch " \\ 0" beendet.</span><span class="sxs-lookup"><span data-stu-id="19bf1-232">Each header is terminated by "\\0".</span></span> <span data-ttu-id="19bf1-233">Eine zusätzliche " \\ 0" beendet die Liste der Header.</span><span class="sxs-lookup"><span data-stu-id="19bf1-233">An additional "\\0" terminates the list of headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-234"><span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**unformatierte WinHTTP- \_ Abfrage \_ \_ Header \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="19bf1-234"><span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**WINHTTP\_QUERY\_RAW\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-235">Empfängt alle vom Server zurückgegebenen Header.</span><span class="sxs-lookup"><span data-stu-id="19bf1-235">Receives all the headers returned by the server.</span></span> <span data-ttu-id="19bf1-236">Jeder Header wird durch eine Wagen Rücklauf/Zeilenvorschub-Sequenz (CR/LF) getrennt.</span><span class="sxs-lookup"><span data-stu-id="19bf1-236">Each header is separated by a carriage return/line feed (CR/LF) sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-237"><span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**WinHTTP- \_ Abfrage \_ Verweis**</span><span class="sxs-lookup"><span data-stu-id="19bf1-237"><span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**WINHTTP\_QUERY\_REFERER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-238">Empfängt den URI der Ressource, in der der angeforderte URI abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="19bf1-238">Receives the URI of the resource where the requested URI was obtained.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-239"><span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**WinHTTP- \_ Abfrage \_ Aktualisierung**</span><span class="sxs-lookup"><span data-stu-id="19bf1-239"><span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**WINHTTP\_QUERY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-240">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="19bf1-240">Obsolete.</span></span> <span data-ttu-id="19bf1-241">Wird für die Legacy Anwendungs Kompatibilität beibehalten.</span><span class="sxs-lookup"><span data-stu-id="19bf1-241">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-242"><span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**WinHTTP- \_ Abfrage \_ Anforderungs \_ Methode**</span><span class="sxs-lookup"><span data-stu-id="19bf1-242"><span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**WINHTTP\_QUERY\_REQUEST\_METHOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-243">Empfängt das HTTP-Verb, das in der Anforderung verwendet wird, in der Regel Get oder Post.</span><span class="sxs-lookup"><span data-stu-id="19bf1-243">Receives the HTTP verb that is being used in the request, typically GET or POST.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-244"><span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**WinHTTP- \_ Abfrage \_ Wiederholung \_ nach**</span><span class="sxs-lookup"><span data-stu-id="19bf1-244"><span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**WINHTTP\_QUERY\_RETRY\_AFTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-245">Ruft die Zeitspanne ab, die erwartet wird, dass der Dienst nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="19bf1-245">Retrieves the amount of time the service is expected to be unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-246"><span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**WinHTTP- \_ Abfrage \_ Server**</span><span class="sxs-lookup"><span data-stu-id="19bf1-246"><span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**WINHTTP\_QUERY\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-247">Ruft Informationen über die Software ab, die vom Ursprungsserver zum Verarbeiten der Anforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="19bf1-247">Retrieves information about the software used by the originating server to handle the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-248"><span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**WinHTTP- \_ Abfrage \_ Satz \_ Cookie**</span><span class="sxs-lookup"><span data-stu-id="19bf1-248"><span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**WINHTTP\_QUERY\_SET\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-249">Empfängt den Wert des Cookies, der für die Anforderung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="19bf1-249">Receives the value of the cookie set for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-250"><span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**WinHTTP- \_ Abfrage \_ Status \_ Code**</span><span class="sxs-lookup"><span data-stu-id="19bf1-250"><span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**WINHTTP\_QUERY\_STATUS\_CODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-251">Empfängt den vom Server zurückgegebenen Statuscode.</span><span class="sxs-lookup"><span data-stu-id="19bf1-251">Receives the status code returned by the server.</span></span> <span data-ttu-id="19bf1-252">Eine Liste möglicher Werte finden Sie unter [**http-Status Codes**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="19bf1-252">For a list of possible values, see [**HTTP Status Codes**](http-status-codes.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-253"><span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**Text des WinHTTP- \_ Abfrage \_ Status \_**</span><span class="sxs-lookup"><span data-stu-id="19bf1-253"><span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**WINHTTP\_QUERY\_STATUS\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-254">Empfängt zusätzlichen Text, der vom Server in der Antwort Zeile zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="19bf1-254">Receives additional text returned by the server on the response line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-255"><span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**WinHTTP- \_ Abfrage \_ Titel**</span><span class="sxs-lookup"><span data-stu-id="19bf1-255"><span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**WINHTTP\_QUERY\_TITLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-256">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="19bf1-256">Obsolete.</span></span> <span data-ttu-id="19bf1-257">Wird für die Legacy Anwendungs Kompatibilität beibehalten.</span><span class="sxs-lookup"><span data-stu-id="19bf1-257">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-258"><span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**Codieren von WinHTTP- \_ Abfrage \_ Übertragungen \_**</span><span class="sxs-lookup"><span data-stu-id="19bf1-258"><span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**WINHTTP\_QUERY\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-259">Ruft den Typ der Transformation ab, die auf den Nachrichtentext angewendet wurde, sodass er sicher zwischen dem Absender und dem Empfänger übertragen werden kann.</span><span class="sxs-lookup"><span data-stu-id="19bf1-259">Retrieves the type of transformation that has been applied to the message body so it can be safely transferred between the sender and recipient.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-260"><span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**WinHTTP- \_ Abfrage, \_ sofern nicht \_ geändert \_ seit**</span><span class="sxs-lookup"><span data-stu-id="19bf1-260"><span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**WINHTTP\_QUERY\_UNLESS\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-261">Ruft den-nicht-Modified-Since-Header ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-261">Retrieves the Unless-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-262"><span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**WinHTTP- \_ Abfrage \_ Upgrade**</span><span class="sxs-lookup"><span data-stu-id="19bf1-262"><span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**WINHTTP\_QUERY\_UPGRADE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-263">Ruft die zusätzlichen Kommunikationsprotokolle ab, die vom Server unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="19bf1-263">Retrieves the additional communication protocols that are supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-264"><span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**WinHTTP- \_ Abfrage- \_ URI**</span><span class="sxs-lookup"><span data-stu-id="19bf1-264"><span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**WINHTTP\_QUERY\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-265">Empfängt einen oder alle der URI, mit dem die Request-URI-Ressource identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="19bf1-265">Receives some or all of the URI by which the Request-URI resource can be identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-266"><span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**WinHTTP- \_ Abfrage \_ Benutzer- \_ Agent**</span><span class="sxs-lookup"><span data-stu-id="19bf1-266"><span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**WINHTTP\_QUERY\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-267">Ruft Informationen über den Benutzer-Agent ab, der die Anforderung vorgenommen hat.</span><span class="sxs-lookup"><span data-stu-id="19bf1-267">Retrieves information about the user agent that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-268"><span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**WinHTTP- \_ Abfrage \_ variiert**</span><span class="sxs-lookup"><span data-stu-id="19bf1-268"><span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**WINHTTP\_QUERY\_VARY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-269">Ruft den Header ab, der angibt, dass die Entität mithilfe einer servergesteuerten Aushandlung aus einer Reihe von verfügbaren Darstellungen der Antwort ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="19bf1-269">Retrieves the header that indicates that the entity was selected from a number of available representations of the response using server-driven negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-270"><span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**WinHTTP- \_ Abfrage \_ Version**</span><span class="sxs-lookup"><span data-stu-id="19bf1-270"><span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**WINHTTP\_QUERY\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-271">Ruft die HTTP-Version ab, die in der Statuszeile vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="19bf1-271">Retrieves the HTTP version that is present in the status line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-272"><span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**WinHTTP- \_ Abfrage \_ über**</span><span class="sxs-lookup"><span data-stu-id="19bf1-272"><span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**WINHTTP\_QUERY\_VIA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-273">Ruft die zwischen Protokolle und Empfänger zwischen dem Benutzer-Agent und dem Server bei Anforderungen sowie zwischen dem Ursprungsserver und dem Client bei Antworten ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-273">Retrieves the intermediate protocols and recipients between the user agent and the server on requests, and between the origin server and the client on responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-274"><span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**WinHTTP- \_ Abfrage \_ Warnung**</span><span class="sxs-lookup"><span data-stu-id="19bf1-274"><span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**WINHTTP\_QUERY\_WARNING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-275">Ruft zusätzliche Informationen über den Status einer Antwort ab, die möglicherweise nicht durch den Antwortstatus Code reflektiert werden.</span><span class="sxs-lookup"><span data-stu-id="19bf1-275">Retrieves additional information about the status of a response that might not be reflected by the response status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-276"><span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WinHTTP- \_ Abfrage \_ www- \_ Authentifizierung**</span><span class="sxs-lookup"><span data-stu-id="19bf1-276"><span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WINHTTP\_QUERY\_WWW\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-277">Ruft das vom Server zurückgegebene Authentifizierungsschema und den Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-277">Retrieves the authentication scheme and realm returned by the server.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="19bf1-278">Die Modifiziererflags werden zusammen mit einem attributflag verwendet, um die Anforderung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="19bf1-278">The modifier flags are used in conjunction with an attribute flag to modify the request.</span></span> <span data-ttu-id="19bf1-279">Modifiziererflags ändern entweder das Format der zurückgegebenen Daten oder geben an, wo die [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) -Funktion nach den Informationen suchen soll.</span><span class="sxs-lookup"><span data-stu-id="19bf1-279">Modifier flags either modify the format of the data returned or indicate where the [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) function should search for the information.</span></span>

<dl> <dt>

<span data-ttu-id="19bf1-280"><span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**WinHTTP \_ - \_ abfrageflagnummer \_**</span><span class="sxs-lookup"><span data-stu-id="19bf1-280"><span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**WINHTTP\_QUERY\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-281">Gibt die Daten als 32-Bit-Zahl für Header zurück, deren Wert eine Zahl ist, z. b. der Statuscode.</span><span class="sxs-lookup"><span data-stu-id="19bf1-281">Returns the data as a 32-bit number for headers whose value is a number, such as the status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-282"><span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**WinHTTP \_ - \_ abfrageflag- \_ Anforderungs \_ Header**</span><span class="sxs-lookup"><span data-stu-id="19bf1-282"><span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**WINHTTP\_QUERY\_FLAG\_REQUEST\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-283">Fragt nur Anforderungs Header ab.</span><span class="sxs-lookup"><span data-stu-id="19bf1-283">Queries request headers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19bf1-284"><span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**WinHTTP \_ - \_ abfrageflag \_ SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="19bf1-284"><span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**WINHTTP\_QUERY\_FLAG\_SYSTEMTIME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19bf1-285">Gibt den Header Wert als [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur zurück, die die Anwendung nicht benötigt, um die Daten zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="19bf1-285">Returns the header value as a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure, which does not require the application to parse the data.</span></span> <span data-ttu-id="19bf1-286">Verwenden Sie für Header, deren Wert eine Datums-/uhrzeitzeile ist, z. b. "Last-modified-time".</span><span class="sxs-lookup"><span data-stu-id="19bf1-286">Use for headers whose value is a date/time string, such as "Last-Modified-Time".</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19bf1-287">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19bf1-287">Requirements</span></span>



| <span data-ttu-id="19bf1-288">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19bf1-288">Requirement</span></span> | <span data-ttu-id="19bf1-289">Wert</span><span class="sxs-lookup"><span data-stu-id="19bf1-289">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="19bf1-290">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19bf1-290">Minimum supported client</span></span><br/> | <span data-ttu-id="19bf1-291">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19bf1-291">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="19bf1-292">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19bf1-292">Minimum supported server</span></span><br/> | <span data-ttu-id="19bf1-293">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19bf1-293">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>   |
| <span data-ttu-id="19bf1-294">Header</span><span class="sxs-lookup"><span data-stu-id="19bf1-294">Header</span></span><br/>                   | <dl> <span data-ttu-id="19bf1-295"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="19bf1-295"><dt>Winhttp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19bf1-296">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19bf1-296">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19bf1-297">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="19bf1-297">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

