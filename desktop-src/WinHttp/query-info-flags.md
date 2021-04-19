---
description: Diese Attribute und Modifizierer werden von WinHttpQueryHeaders verwendet.
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: Abfrageinformationsflags (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32ba15c258a37627cdbdd79f13859761fd671385
ms.sourcegitcommit: df0933ad2b42f07031f4340330712c11cf712ff0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107385888"
---
# <a name="query-info-flags-winhttph"></a><span data-ttu-id="559ea-103">Abfrageinformationsflags (Winhttp.h)</span><span class="sxs-lookup"><span data-stu-id="559ea-103">Query Info Flags (Winhttp.h)</span></span>

<span data-ttu-id="559ea-104">Diese Attribute und Modifizierer werden von [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders)verwendet.</span><span class="sxs-lookup"><span data-stu-id="559ea-104">These attributes and modifiers are used by [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

<span data-ttu-id="559ea-105">Die Attributflags werden von [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) verwendet, um anzugeben, welche Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="559ea-105">The attribute flags are used by [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) to indicate what information to retrieve.</span></span> <span data-ttu-id="559ea-106">Die meisten Attributflags werden direkt einem bestimmten HTTP-Header zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="559ea-106">Most of the attribute flags map directly to a specific HTTP header.</span></span> <span data-ttu-id="559ea-107">Es gibt auch einige spezielle Flags, z. B. WINHTTP \_ QUERY \_ RAW \_ HEADERS, die nicht mit einem bestimmten Header verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="559ea-107">There are also some special flags, such as WINHTTP\_QUERY\_RAW\_HEADERS, that are not related to a specific header.</span></span>

<dl> <dt>

<span data-ttu-id="559ea-108"><span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**WINHTTP \_ QUERY \_ ACCEPT**</span><span class="sxs-lookup"><span data-stu-id="559ea-108"><span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**WINHTTP\_QUERY\_ACCEPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-109">Ruft die zulässigen Medientypen für die Antwort ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-109">Retrieves the acceptable media types for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-110"><span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP \_ QUERY \_ ACCEPT \_ CHARSET**</span><span class="sxs-lookup"><span data-stu-id="559ea-110"><span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP\_QUERY\_ACCEPT\_CHARSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-111">Ruft die zulässigen Zeichensätze für die Antwort ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-111">Retrieves the acceptable character sets for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-112"><span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**WINHTTP \_ QUERY \_ ACCEPT \_ ENCODING**</span><span class="sxs-lookup"><span data-stu-id="559ea-112"><span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**WINHTTP\_QUERY\_ACCEPT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-113">Ruft die zulässigen Werte für die Inhaltscodierung für die Antwort ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-113">Retrieves the acceptable content-coding values for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-114"><span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**WINHTTP \_ QUERY \_ ACCEPT \_ LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="559ea-114"><span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**WINHTTP\_QUERY\_ACCEPT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-115">Ruft die zulässigen natürlichen Sprachen für die Antwort ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-115">Retrieves the acceptable natural languages for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-116"><span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**WINHTTP \_ QUERY \_ ACCEPT \_ RANGES**</span><span class="sxs-lookup"><span data-stu-id="559ea-116"><span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**WINHTTP\_QUERY\_ACCEPT\_RANGES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-117">Ruft die Typen von Bereichsanforderungen ab, die für eine Ressource akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="559ea-117">Retrieves the types of range requests that are accepted for a resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-118"><span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**ALTER DER \_ WINHTTP-ABFRAGE \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-118"><span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**WINHTTP\_QUERY\_AGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-119">Ruft das Feld Age response-header ab, das die Schätzung des Absenders für den Zeitraum seit der Generierung der Antwort auf dem Ursprungsserver enthält.</span><span class="sxs-lookup"><span data-stu-id="559ea-119">Retrieves the Age response-header field, which contains the sender's estimate of the amount of time since the response was generated at the originating server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-120"><span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WINHTTP \_ QUERY \_ ALLOW**</span><span class="sxs-lookup"><span data-stu-id="559ea-120"><span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WINHTTP\_QUERY\_ALLOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-121">Empfängt die [**vom Server unterstützten**](glossary.md) HTTP-Verben.</span><span class="sxs-lookup"><span data-stu-id="559ea-121">Receives the [**HTTP verbs**](glossary.md) supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-122"><span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**\_ \_ WINHTTP-ABFRAGEAUTHENTIFIZIERUNGSINFORMATIONEN \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-122"><span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**WINHTTP\_QUERY\_AUTHENTICATION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-123">Ruft den Authentication-Info ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-123">Retrieves the Authentication-Info header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-124"><span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**\_ \_ WINHTTP-ABFRAGEAUTORISIERUNG**</span><span class="sxs-lookup"><span data-stu-id="559ea-124"><span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**WINHTTP\_QUERY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-125">Ruft die für eine Anforderung verwendeten Autorisierungsanmeldeinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-125">Retrieves the authorization credentials used for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-126"><span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**\_ \_ WINHTTP-ABFRAGECACHE-STEUERELEMENT \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-126"><span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**WINHTTP\_QUERY\_CACHE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-127">Ruft die Cachesteuerungs-Direktiven ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-127">Retrieves the cache control directives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-128"><span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**\_WINHTTP-ABFRAGEVERBINDUNG \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-128"><span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**WINHTTP\_QUERY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-129">Ruft alle Optionen ab, die für eine bestimmte Verbindung angegeben sind und nicht von Proxys über weitere Verbindungen kommuniziert werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="559ea-129">Retrieves any options that are specified for a particular connection and must not be communicated by proxies over further connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-130"><span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**\_ \_ WINHTTP-ABFRAGEINHALTSBASIS \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-130"><span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**WINHTTP\_QUERY\_CONTENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-131">Ruft den Basis-Uniform Resource Identifier (URI) ab, um relative URLs innerhalb der Entität aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="559ea-131">Retrieves the base Uniform Resource Identifier (URI) to resolve relative URLs within the entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-132"><span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**\_ \_ WINHTTP-ABFRAGEINHALTSBESCHREIBUNG \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-132"><span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**WINHTTP\_QUERY\_CONTENT\_DESCRIPTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-133">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="559ea-133">Obsolete.</span></span> <span data-ttu-id="559ea-134">Wird aus Kompatibilitäts- und Legacy-Anwendungskompatibilität verwaltet.</span><span class="sxs-lookup"><span data-stu-id="559ea-134">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-135"><span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**\_ \_ WINHTTP-ABFRAGEINHALTSDISPOSITION \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-135"><span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**WINHTTP\_QUERY\_CONTENT\_DISPOSITION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-136">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="559ea-136">Obsolete.</span></span> <span data-ttu-id="559ea-137">Wird aus Kompatibilitäts- und Legacy-Anwendungskompatibilität verwaltet.</span><span class="sxs-lookup"><span data-stu-id="559ea-137">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-138"><span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**\_ \_ WINHTTP-ABFRAGEINHALTSCODIERUNG \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-138"><span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**WINHTTP\_QUERY\_CONTENT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-139">Ruft zusätzliche Inhaltscodierung ab, die auf die gesamte Ressource angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="559ea-139">Retrieves additional content coding that has been applied to the entire resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-140"><span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**\_ \_ WINHTTP-ABFRAGEINHALTS-ID \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-140"><span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**WINHTTP\_QUERY\_CONTENT\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-141">Ruft die Inhaltsidentifikation ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-141">Retrieves the content identification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-142"><span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**\_ \_ WINHTTP-ABFRAGEINHALTSSPRACHE \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-142"><span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**WINHTTP\_QUERY\_CONTENT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-143">Ruft die Sprache ab, in der der Inhalt geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="559ea-143">Retrieves the language that the content is written in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-144"><span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**LÄNGE DES \_ WINHTTP-ABFRAGEINHALTS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-144"><span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**WINHTTP\_QUERY\_CONTENT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-145">Ruft die Größe der Ressource in Bytes ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-145">Retrieves the size of the resource, in bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-146"><span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**SPEICHERORT DES \_ WINHTTP-ABFRAGEINHALTS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-146"><span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**WINHTTP\_QUERY\_CONTENT\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-147">Ruft den Ressourcenspeicherort für die Entität ab, die in der Nachricht eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="559ea-147">Retrieves the resource location for the entity enclosed in the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-148"><span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**WINHTTP \_ QUERY \_ CONTENT \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="559ea-148"><span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**WINHTTP\_QUERY\_CONTENT\_MD5**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-149">Ruft einen MD5-Digest des Entitätstexts ab, um eine End-to-End-Überprüfung der Nachrichtenintegrität für den Entitätstext bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="559ea-149">Retrieves an MD5 digest of the entity body for the purpose of providing an end-to-end message integrity check for the entity body.</span></span> <span data-ttu-id="559ea-150">Weitere Informationen finden Sie unter [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).</span><span class="sxs-lookup"><span data-stu-id="559ea-150">For more information, see [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-151"><span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**\_ \_ WINHTTP-ABFRAGEINHALTSBEREICH \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-151"><span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**WINHTTP\_QUERY\_CONTENT\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-152">Ruft die Position im vollständigen Entitätstext ab, an der der Teilentitätstext eingefügt werden soll, und die Gesamtgröße des vollständigen Entitätstexts.</span><span class="sxs-lookup"><span data-stu-id="559ea-152">Retrieves the location in the full entity body where the partial entity body should be inserted and the total size of the full entity body.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-153"><span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**CODIERUNG DER \_ WINHTTP-ABFRAGEINHALTSÜBERTRAGUNG \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-153"><span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**WINHTTP\_QUERY\_CONTENT\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-154">Ruft eine Codierungstransformation ab, die auf einen Entitätstext anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="559ea-154">Retrieves an encoding transformation applicable to an entity-body.</span></span> <span data-ttu-id="559ea-155">Sie wurde möglicherweise bereits angewendet, muss möglicherweise angewendet werden oder ist optional anwendbar.</span><span class="sxs-lookup"><span data-stu-id="559ea-155">It may already have been applied, may need to be applied, or may be optionally applicable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-156"><span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**\_ \_ WINHTTP-ABFRAGEINHALTSTYP \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-156"><span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**WINHTTP\_QUERY\_CONTENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-157">Empfängt den Inhaltstyp der Ressource, z. B. text oder html.</span><span class="sxs-lookup"><span data-stu-id="559ea-157">Receives the content type of the resource, such as text or html.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-158"><span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**\_ \_ WINHTTP-ABFRAGECOOKIE**</span><span class="sxs-lookup"><span data-stu-id="559ea-158"><span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**WINHTTP\_QUERY\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-159">Ruft alle cookies ab, die der Anforderung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="559ea-159">Retrieves any cookies associated with the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-160"><span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**\_WINHTTP-ABFRAGEKOSTEN \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-160"><span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**WINHTTP\_QUERY\_COST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-161">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="559ea-161">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-162"><span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WINHTTP \_ QUERY \_ CUSTOM**</span><span class="sxs-lookup"><span data-stu-id="559ea-162"><span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WINHTTP\_QUERY\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-163">Bewirkt, dass [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) nach dem im *pwszName-Parameter angegebenen* Headernamen sucht und die Headerinformationen in *lpBuffer* speichert.</span><span class="sxs-lookup"><span data-stu-id="559ea-163">Causes [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) to search for the header name specified in the *pwszName* parameter and store the header information in *lpBuffer*.</span></span> <span data-ttu-id="559ea-164">Eine Anwendung kann **WINHTTP \_ OPTION RECEIVE \_ RESPONSE \_ \_ TIMEOUT** verwenden, um die maximale Zeit zu begrenzen, die diese Abfrage auf den Empfang aller Header wartet.</span><span class="sxs-lookup"><span data-stu-id="559ea-164">An application can use **WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT** to limit the maximum time this query waits for all headers to be received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-165"><span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**\_WINHTTP-ABFRAGEDATUM \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-165"><span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**WINHTTP\_QUERY\_DATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-166">Empfängt das Datum und die Uhrzeit, zu der die Nachricht stammt.</span><span class="sxs-lookup"><span data-stu-id="559ea-166">Receives the date and time at which the message was originated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-167"><span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**VON \_ \_ ABGELEITETE WINHTTP-ABFRAGE \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-167"><span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**WINHTTP\_QUERY\_DERIVED\_FROM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-168">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="559ea-168">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-169"><span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**\_ \_ WINHTTP-ABFRAGE-ETAG**</span><span class="sxs-lookup"><span data-stu-id="559ea-169"><span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**WINHTTP\_QUERY\_ETAG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-170">Ruft das Entitätstag für die zugeordnete Entität ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-170">Retrieves the entity tag for the associated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-171"><span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WINHTTP \_ QUERY \_ EXPECT**</span><span class="sxs-lookup"><span data-stu-id="559ea-171"><span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WINHTTP\_QUERY\_EXPECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-172">Ruft den Expect-Header ab, der angibt, ob die Clientanwendung Antworten der Serie 100 erwarten soll.</span><span class="sxs-lookup"><span data-stu-id="559ea-172">Retrieves the Expect header, which indicates whether the client application should expect 100 series responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-173"><span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**\_WINHTTP-ABFRAGE \_ LÄUFT AB**</span><span class="sxs-lookup"><span data-stu-id="559ea-173"><span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**WINHTTP\_QUERY\_EXPIRES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-174">Empfängt das Datum und die Uhrzeit, nach der die Ressource als veraltet betrachtet werden soll.</span><span class="sxs-lookup"><span data-stu-id="559ea-174">Receives the date and time after which the resource should be considered outdated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-175"><span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**\_WINHTTP-ABFRAGE \_ WEITERGELEITET**</span><span class="sxs-lookup"><span data-stu-id="559ea-175"><span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**WINHTTP\_QUERY\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-176">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="559ea-176">Obsolete.</span></span> <span data-ttu-id="559ea-177">Wird aus Kompatibilitäts- und Legacy-Anwendungskompatibilität verwaltet.</span><span class="sxs-lookup"><span data-stu-id="559ea-177">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-178"><span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**WINHTTP \_ QUERY \_ FROM**</span><span class="sxs-lookup"><span data-stu-id="559ea-178"><span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**WINHTTP\_QUERY\_FROM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-179">Ruft die E-Mail-Adresse für den Benutzer ab, der den anfordernden [*Benutzer-Agent*](glossary.md) steuert, wenn der From-Header angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="559ea-179">Retrieves the e-mail address for the user who controls the requesting [*user agent*](glossary.md) if the From header is given.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-180"><span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**\_WINHTTP-ABFRAGEHOST \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-180"><span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**WINHTTP\_QUERY\_HOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-181">Ruft den Internethost und die Portnummer der angeforderten Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-181">Retrieves the Internet host and port number of the resource being requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-182"><span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**WINHTTP \_ QUERY \_ IF \_ MATCH**</span><span class="sxs-lookup"><span data-stu-id="559ea-182"><span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**WINHTTP\_QUERY\_IF\_MATCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-183">Ruft den Inhalt des If-Match Anforderungsheaderfelds ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-183">Retrieves the contents of the If-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-184"><span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**\_WINHTTP-ABFRAGE, \_ WENN \_ SIE GEÄNDERT \_ WURDE**</span><span class="sxs-lookup"><span data-stu-id="559ea-184"><span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**WINHTTP\_QUERY\_IF\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-185">Ruft den Inhalt des If-Modified-Since-Headers ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-185">Retrieves the contents of the If-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-186"><span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**\_WINHTTP-ABFRAGE, \_ WENN \_ KEINE ÜBEREINSTIMMUNG \_ BESTEHT**</span><span class="sxs-lookup"><span data-stu-id="559ea-186"><span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**WINHTTP\_QUERY\_IF\_NONE\_MATCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-187">Ruft den Inhalt des Anforderungsheaderfelds If-None-Match ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-187">Retrieves the contents of the If-None-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-188"><span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**WINHTTP \_ QUERY \_ IF \_ RANGE**</span><span class="sxs-lookup"><span data-stu-id="559ea-188"><span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**WINHTTP\_QUERY\_IF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-189">Ruft den Inhalt des If-Range Anforderungsheaderfelds ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-189">Retrieves the contents of the If-Range request-header field.</span></span> <span data-ttu-id="559ea-190">Mit diesem Header kann die Clientanwendung überprüfen, ob die Entität, die mit einer Teilkopie der Entität im Cache der Clientanwendung verknüpft ist, nicht aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="559ea-190">This header allows the client application to check if the entity related to a partial copy of the entity in the client application's cache has not been updated.</span></span> <span data-ttu-id="559ea-191">Wenn die Entität nicht aktualisiert wurde, senden Sie die Teile, die in der Clientanwendung fehlen.</span><span class="sxs-lookup"><span data-stu-id="559ea-191">If the entity has not been updated, send the parts that the client application is missing.</span></span> <span data-ttu-id="559ea-192">Wenn die Entität aktualisiert wurde, senden Sie die gesamte aktualisierte Entität.</span><span class="sxs-lookup"><span data-stu-id="559ea-192">If the entity has been updated, send the entire updated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-193"><span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**\_WINHTTP-ABFRAGE, \_ WENN SEIT NICHT \_ GEÄNDERT \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-193"><span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**WINHTTP\_QUERY\_IF\_UNMODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-194">Ruft den Inhalt des Anforderungsheaderfelds If-Unmodified-Since ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-194">Retrieves the contents of the If-Unmodified-Since request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-195"><span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**\_WINHTTP-ABFRAGELINK \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-195"><span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**WINHTTP\_QUERY\_LINK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-196">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="559ea-196">Obsolete.</span></span> <span data-ttu-id="559ea-197">Wird aus Gründen der Kompatibilität von Legacyanwendungen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="559ea-197">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-198"><span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**\_WINHTTP-ABFRAGE \_ ZULETZT \_ GEÄNDERT**</span><span class="sxs-lookup"><span data-stu-id="559ea-198"><span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**WINHTTP\_QUERY\_LAST\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-199">Empfängt das Datum und die Uhrzeit der letzten Änderung der Ressource.</span><span class="sxs-lookup"><span data-stu-id="559ea-199">Receives the date and time at which the resource was last modified.</span></span> <span data-ttu-id="559ea-200">Datum und Uhrzeit werden vom Server bestimmt.</span><span class="sxs-lookup"><span data-stu-id="559ea-200">The date and time are determined by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-201"><span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**\_ \_ WINHTTP-ABFRAGESPEICHERORT**</span><span class="sxs-lookup"><span data-stu-id="559ea-201"><span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**WINHTTP\_QUERY\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-202">Ruft den absoluten URI ab, der in einem Location-Antwortheader verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="559ea-202">Retrieves the absolute URI used in a Location response-header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-203"><span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**WINHTTP \_ QUERY \_ MAX**</span><span class="sxs-lookup"><span data-stu-id="559ea-203"><span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**WINHTTP\_QUERY\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-204">Gibt den maximalen Wert eines WINHTTP \_ \_ \* QUERY-Werts an.</span><span class="sxs-lookup"><span data-stu-id="559ea-204">Indicates the maximum value of a WINHTTP\_QUERY\_\* value.</span></span> <span data-ttu-id="559ea-205">Kein Abfrageflag.</span><span class="sxs-lookup"><span data-stu-id="559ea-205">Not a query flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-206"><span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**WINHTTP \_ QUERY \_ MAX \_ FORWARDS**</span><span class="sxs-lookup"><span data-stu-id="559ea-206"><span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**WINHTTP\_QUERY\_MAX\_FORWARDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-207">Ruft die Anzahl der Proxys oder Gateways ab, die die Anforderung an den nächsten eingehenden Server weitergeleitet werden können.</span><span class="sxs-lookup"><span data-stu-id="559ea-207">Retrieves the number of proxies or gateways that can forward the request to the next inbound server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-208"><span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**\_ \_ WINHTTP-ABFRAGENACHRICHTEN-ID \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-208"><span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**WINHTTP\_QUERY\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-209">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="559ea-209">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-210"><span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**\_ \_ WINHTTP-ABFRAGE-MIME-VERSION \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-210"><span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**WINHTTP\_QUERY\_MIME\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-211">Empfängt die Version des MULTIPURPOSE INTERNET MAIL EXTENSIONS (MIME), das zum Erstellen der Nachricht verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="559ea-211">Receives the version of the Multipurpose Internet Mail Extensions (MIME) protocol that was used to construct the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-212"><span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**\_ \_ WINHTTP-ABFRAGE-ORIG-URI \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-212"><span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**WINHTTP\_QUERY\_ORIG\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-213">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="559ea-213">Obsolete.</span></span> <span data-ttu-id="559ea-214">Wird aus Kompatibilitäts- und Legacy-Anwendungskompatibilität verwaltet.</span><span class="sxs-lookup"><span data-stu-id="559ea-214">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-215"><span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**WINHTTP \_ QUERY \_ PRAGMA**</span><span class="sxs-lookup"><span data-stu-id="559ea-215"><span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**WINHTTP\_QUERY\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-216">Empfängt die implementierungsspezifischen Anweisungen, die für jeden Empfänger entlang der Anforderungs-/Antwortkette gelten können.</span><span class="sxs-lookup"><span data-stu-id="559ea-216">Receives the implementation-specific directives that might apply to any recipient along the request/response chain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-217"><span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**\_ \_ WINHTTP-ABFRAGEPROXYAUTHENTIFIZIERUNG \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-217"><span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**WINHTTP\_QUERY\_PROXY\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-218">Ruft das vom Proxy zurückgegebene Authentifizierungsschema und den Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-218">Retrieves the authentication scheme and realm returned by the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-219"><span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**\_ \_ WINHTTP-ABFRAGEPROXYAUTORISIERUNG \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-219"><span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**WINHTTP\_QUERY\_PROXY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-220">Ruft den Header ab, mit dem der Benutzer bei einem Proxy identifiziert wird, für den eine Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="559ea-220">Retrieves the header that is used to identify the user to a proxy that requires authentication.</span></span> <span data-ttu-id="559ea-221">Dieser Header kann nur abgerufen werden, bevor die Anforderung an den Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="559ea-221">This header can only be retrieved before the request is sent to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-222"><span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**\_ \_ WINHTTP-ABFRAGEPROXYVERBINDUNG \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-222"><span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**WINHTTP\_QUERY\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-223">Ruft den Proxy-Connection ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-223">Retrieves the Proxy-Connection header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-224"><span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**\_ \_ WINHTTP-ABFRAGEPROXYUNTERSTÜTZUNG \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-224"><span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**WINHTTP\_QUERY\_PROXY\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-225">Ruft den Proxy-Support ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-225">Retrieves the Proxy-Support header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-226"><span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**WINHTTP \_ QUERY \_ PUBLIC**</span><span class="sxs-lookup"><span data-stu-id="559ea-226"><span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**WINHTTP\_QUERY\_PUBLIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-227">Empfängt HTTP-Verben, die auf diesem Server verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="559ea-227">Receives HTTP verbs available at this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-228"><span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**\_WINHTTP-ABFRAGEBEREICH \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-228"><span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**WINHTTP\_QUERY\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-229">Ruft den Bytebereich einer Entität ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-229">Retrieves the byte range of an entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-230"><span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**\_ \_ UNFORMATIERTE WINHTTP-ABFRAGEHEADER \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-230"><span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**WINHTTP\_QUERY\_RAW\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-231">Empfängt alle vom Server zurückgegebenen Header.</span><span class="sxs-lookup"><span data-stu-id="559ea-231">Receives all the headers returned by the server.</span></span> <span data-ttu-id="559ea-232">Jeder Header wird mit \\ "0" beendet.</span><span class="sxs-lookup"><span data-stu-id="559ea-232">Each header is terminated by "\\0".</span></span> <span data-ttu-id="559ea-233">Ein \\ zusätzliches "0" beendet die Liste der Header.</span><span class="sxs-lookup"><span data-stu-id="559ea-233">An additional "\\0" terminates the list of headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-234"><span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**WINHTTP \_ QUERY \_ RAW \_ HEADERS \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="559ea-234"><span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**WINHTTP\_QUERY\_RAW\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-235">Empfängt alle vom Server zurückgegebenen Header.</span><span class="sxs-lookup"><span data-stu-id="559ea-235">Receives all the headers returned by the server.</span></span> <span data-ttu-id="559ea-236">Jeder Header wird durch eine CR/LF-Sequenz (Wagenrücklauf/Zeilenvorschub) getrennt.</span><span class="sxs-lookup"><span data-stu-id="559ea-236">Each header is separated by a carriage return/line feed (CR/LF) sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-237"><span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**\_WINHTTP-ABFRAGEREFERENZ \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-237"><span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**WINHTTP\_QUERY\_REFERER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-238">Empfängt den URI der Ressource, in der der angeforderte URI abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="559ea-238">Receives the URI of the resource where the requested URI was obtained.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-239"><span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**\_WINHTTP-ABFRAGEAKTUALISIERUNG \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-239"><span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**WINHTTP\_QUERY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-240">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="559ea-240">Obsolete.</span></span> <span data-ttu-id="559ea-241">Wird aus Gründen der Kompatibilität von Legacyanwendungen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="559ea-241">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-242"><span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**\_ \_ WINHTTP-ABFRAGEANFORDERUNGSMETHODE \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-242"><span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**WINHTTP\_QUERY\_REQUEST\_METHOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-243">Empfängt das HTTP-Verb, das in der Anforderung verwendet wird, in der Regel GET oder POST.</span><span class="sxs-lookup"><span data-stu-id="559ea-243">Receives the HTTP verb that is being used in the request, typically GET or POST.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-244"><span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**WINHTTP \_ QUERY \_ RETRY \_ AFTER**</span><span class="sxs-lookup"><span data-stu-id="559ea-244"><span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**WINHTTP\_QUERY\_RETRY\_AFTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-245">Ruft den Zeitraum ab, für den der Dienst voraussichtlich nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="559ea-245">Retrieves the amount of time the service is expected to be unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-246"><span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**\_WINHTTP-ABFRAGESERVER \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-246"><span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**WINHTTP\_QUERY\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-247">Ruft Informationen über die Software ab, die vom Ursprungsserver zum Verarbeiten der Anforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="559ea-247">Retrieves information about the software used by the originating server to handle the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-248"><span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**\_ \_ \_ WINHTTP-ABFRAGESATZCOOKIE**</span><span class="sxs-lookup"><span data-stu-id="559ea-248"><span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**WINHTTP\_QUERY\_SET\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-249">Empfängt den Wert des Für die Anforderung festgelegten Cookies.</span><span class="sxs-lookup"><span data-stu-id="559ea-249">Receives the value of the cookie set for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-250"><span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**\_ \_ WINHTTP-ABFRAGESTATUSCODE \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-250"><span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**WINHTTP\_QUERY\_STATUS\_CODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-251">Empfängt den vom Server zurückgegebenen Statuscode.</span><span class="sxs-lookup"><span data-stu-id="559ea-251">Receives the status code returned by the server.</span></span> <span data-ttu-id="559ea-252">Eine Liste der möglichen Werte finden Sie unter [**HTTP-Statuscodes**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="559ea-252">For a list of possible values, see [**HTTP Status Codes**](http-status-codes.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-253"><span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**\_ \_ WINHTTP-ABFRAGESTATUSTEXT \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-253"><span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**WINHTTP\_QUERY\_STATUS\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-254">Empfängt zusätzlichen Text, der vom Server in der Antwortzeile zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="559ea-254">Receives additional text returned by the server on the response line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-255"><span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**\_WINHTTP-ABFRAGETITEL \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-255"><span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**WINHTTP\_QUERY\_TITLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-256">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="559ea-256">Obsolete.</span></span> <span data-ttu-id="559ea-257">Wird aus Kompatibilitäts- und Legacy-Anwendungskompatibilität verwaltet.</span><span class="sxs-lookup"><span data-stu-id="559ea-257">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-258"><span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**\_ \_ WINHTTP-ABFRAGEÜBERTRAGUNGSCODIERUNG \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-258"><span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**WINHTTP\_QUERY\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-259">Ruft den Typ der Transformation ab, die auf den Nachrichtentext angewendet wurde, damit er sicher zwischen Absender und Empfänger übertragen werden kann.</span><span class="sxs-lookup"><span data-stu-id="559ea-259">Retrieves the type of transformation that has been applied to the message body so it can be safely transferred between the sender and recipient.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-260"><span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**\_WINHTTP-ABFRAGE, \_ ES SEI \_ DENN, SIE WURDE \_ GEÄNDERT.**</span><span class="sxs-lookup"><span data-stu-id="559ea-260"><span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**WINHTTP\_QUERY\_UNLESS\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-261">Ruft den Unless-Modified-Since-Header ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-261">Retrieves the Unless-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-262"><span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**\_ \_ WINHTTP-ABFRAGEUPGRADE**</span><span class="sxs-lookup"><span data-stu-id="559ea-262"><span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**WINHTTP\_QUERY\_UPGRADE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-263">Ruft die zusätzlichen Kommunikationsprotokolle ab, die vom Server unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="559ea-263">Retrieves the additional communication protocols that are supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-264"><span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**\_ \_ WINHTTP-ABFRAGE-URI**</span><span class="sxs-lookup"><span data-stu-id="559ea-264"><span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**WINHTTP\_QUERY\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-265">Empfängt einen Teil oder den ganzen URI, mit dem die Request-URI-Ressource identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="559ea-265">Receives some or all of the URI by which the Request-URI resource can be identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-266"><span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**\_ \_ WINHTTP-ABFRAGEBENUTZER-AGENT \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-266"><span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**WINHTTP\_QUERY\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-267">Ruft Informationen über den Benutzer-Agent ab, der die Anforderung gestellt hat.</span><span class="sxs-lookup"><span data-stu-id="559ea-267">Retrieves information about the user agent that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-268"><span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**\_WINHTTP-ABFRAGE \_ VARIIERT**</span><span class="sxs-lookup"><span data-stu-id="559ea-268"><span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**WINHTTP\_QUERY\_VARY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-269">Ruft den Header ab, der angibt, dass die Entität mithilfe einer servergesteuerten Aushandlung aus einer Reihe verfügbarer Darstellungen der Antwort ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="559ea-269">Retrieves the header that indicates that the entity was selected from a number of available representations of the response using server-driven negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-270"><span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**\_WINHTTP-ABFRAGEVERSION \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-270"><span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**WINHTTP\_QUERY\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-271">Ruft die HTTP-Version ab, die in der Statuszeile vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="559ea-271">Retrieves the HTTP version that is present in the status line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-272"><span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**\_WINHTTP-ABFRAGE \_ ÜBER**</span><span class="sxs-lookup"><span data-stu-id="559ea-272"><span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**WINHTTP\_QUERY\_VIA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-273">Ruft die Zwischenprotokolle und Empfänger zwischen dem Benutzer-Agent und dem Server bei Anforderungen sowie zwischen dem Ursprungsserver und dem Client bei Antworten ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-273">Retrieves the intermediate protocols and recipients between the user agent and the server on requests, and between the origin server and the client on responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-274"><span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**\_WINHTTP-ABFRAGEWARNUNG \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-274"><span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**WINHTTP\_QUERY\_WARNING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-275">Ruft zusätzliche Informationen zum Status einer Antwort ab, die möglicherweise nicht vom Antwortstatuscode widergespiegelt werden.</span><span class="sxs-lookup"><span data-stu-id="559ea-275">Retrieves additional information about the status of a response that might not be reflected by the response status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-276"><span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WINHTTP \_ QUERY \_ WWW \_ AUTHENTICATE**</span><span class="sxs-lookup"><span data-stu-id="559ea-276"><span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WINHTTP\_QUERY\_WWW\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-277">Ruft das vom Server zurückgegebene Authentifizierungsschema und den vom Server zurückgegebenen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-277">Retrieves the authentication scheme and realm returned by the server.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="559ea-278">Die Modifiziererflags werden zusammen mit einem Attributflag verwendet, um die Anforderung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="559ea-278">The modifier flags are used in conjunction with an attribute flag to modify the request.</span></span> <span data-ttu-id="559ea-279">Modifiziererflags ändern entweder das Format der zurückgegebenen Daten oder geben an, wo die [**WinHttpQueryHeaders-Funktion**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) nach den Informationen suchen soll.</span><span class="sxs-lookup"><span data-stu-id="559ea-279">Modifier flags either modify the format of the data returned or indicate where the [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) function should search for the information.</span></span>

<dl> <dt>

<span data-ttu-id="559ea-280"><span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**\_ \_ WINHTTP-ABFRAGEFLAGNUMMER \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-280"><span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**WINHTTP\_QUERY\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-281">Gibt die Daten als 32-Bit-Zahl für Header zurück, deren Wert eine Zahl ist, z. B. der Statuscode.</span><span class="sxs-lookup"><span data-stu-id="559ea-281">Returns the data as a 32-bit number for headers whose value is a number, such as the status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-282"><span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**\_ANFORDERUNGSHEADER FÜR WINHTTP-ABFRAGEFLAGS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="559ea-282"><span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**WINHTTP\_QUERY\_FLAG\_REQUEST\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-283">Fragt nur Anforderungsheader ab.</span><span class="sxs-lookup"><span data-stu-id="559ea-283">Queries request headers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="559ea-284"><span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**\_WINHTTP-ABFRAGEFLAG \_ \_ SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="559ea-284"><span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**WINHTTP\_QUERY\_FLAG\_SYSTEMTIME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="559ea-285">Gibt den Headerwert als [**SYSTEMTIME-Struktur**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) zurück, die keine Analyse der Daten durch die Anwendung erfordert.</span><span class="sxs-lookup"><span data-stu-id="559ea-285">Returns the header value as a [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure, which does not require the application to parse the data.</span></span> <span data-ttu-id="559ea-286">Verwenden Sie für Header, deren Wert eine Datums-/Uhrzeitzeichenfolge ist, z. B. "Last-Modified-Time".</span><span class="sxs-lookup"><span data-stu-id="559ea-286">Use for headers whose value is a date/time string, such as "Last-Modified-Time".</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="559ea-287">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="559ea-287">Requirements</span></span>

| <span data-ttu-id="559ea-288">Anforderung</span><span class="sxs-lookup"><span data-stu-id="559ea-288">Requirement</span></span> | <span data-ttu-id="559ea-289">Wert</span><span class="sxs-lookup"><span data-stu-id="559ea-289">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="559ea-290">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="559ea-290">Minimum supported client</span></span> | <span data-ttu-id="559ea-291">Nur Windows XP, Windows 2000 Professional mit \[ SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="559ea-291">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>      |
| <span data-ttu-id="559ea-292">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="559ea-292">Minimum supported server</span></span> | <span data-ttu-id="559ea-293">Nur Windows Server 2003, Windows 2000 Server mit \[ SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="559ea-293">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>   |
| <span data-ttu-id="559ea-294">Header</span><span class="sxs-lookup"><span data-stu-id="559ea-294">Header</span></span>                   | <dl> <span data-ttu-id="559ea-295"><dt>Winhttp.h</dt></span><span class="sxs-lookup"><span data-stu-id="559ea-295"><dt>Winhttp.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="559ea-296">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="559ea-296">See also</span></span>

* [<span data-ttu-id="559ea-297">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="559ea-297">WinHTTP Versions</span></span>](winhttp-versions.md)
