---
description: Diese Konstanten und entsprechenden Werte geben die von Servern im Internet zurückgegebenen HTTP-Statuscodes an.
ms.assetid: 3de6a35d-41e9-4fce-ab92-e970c7c07e55
title: HTTP-Status Codes (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcf4103cdc382bd5ab0d582fe99212083e2780ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216710"
---
# <a name="http-status-codes-winhttph"></a><span data-ttu-id="846b4-103">HTTP-Status Codes (WinHTTP. h)</span><span class="sxs-lookup"><span data-stu-id="846b4-103">HTTP Status Codes (Winhttp.h)</span></span>

<span data-ttu-id="846b4-104">Diese Konstanten und entsprechenden Werte geben die von Servern im Internet zurückgegebenen HTTP-Statuscodes an.</span><span class="sxs-lookup"><span data-stu-id="846b4-104">These constants and corresponding values indicate HTTP status codes returned by servers on the Internet.</span></span>

<dl> <dt>

<span data-ttu-id="846b4-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP- \_ Status \_ fortsetzen**</span><span class="sxs-lookup"><span data-stu-id="846b4-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-106">100</span><span class="sxs-lookup"><span data-stu-id="846b4-106">100</span></span>
</dt> <dt>



<span data-ttu-id="846b4-107">Die Anforderung kann fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="846b4-107">The request can be continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP- \_ Status \_ Schalter \_ Protokolle**</span><span class="sxs-lookup"><span data-stu-id="846b4-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP\_STATUS\_SWITCH\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-109">101</span><span class="sxs-lookup"><span data-stu-id="846b4-109">101</span></span>
</dt> <dt>



<span data-ttu-id="846b4-110">Der Server hat die Protokolle in einem Upgradeheader geändert.</span><span class="sxs-lookup"><span data-stu-id="846b4-110">The server has switched protocols in an upgrade header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP- \_ Status \_ OK**</span><span class="sxs-lookup"><span data-stu-id="846b4-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP\_STATUS\_OK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-112">200</span><span class="sxs-lookup"><span data-stu-id="846b4-112">200</span></span>
</dt> <dt>



<span data-ttu-id="846b4-113">Die Anforderung wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="846b4-113">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**HTTP- \_ Status \_ erstellt**</span><span class="sxs-lookup"><span data-stu-id="846b4-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**HTTP\_STATUS\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-115">201</span><span class="sxs-lookup"><span data-stu-id="846b4-115">201</span></span>
</dt> <dt>



<span data-ttu-id="846b4-116">Die Anforderung wurde erfüllt und führte zur Erstellung einer neuen Ressource.</span><span class="sxs-lookup"><span data-stu-id="846b4-116">The request has been fulfilled and resulted in the creation of a new resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP- \_ Status \_ akzeptiert**</span><span class="sxs-lookup"><span data-stu-id="846b4-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP\_STATUS\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-118">202</span><span class="sxs-lookup"><span data-stu-id="846b4-118">202</span></span>
</dt> <dt>



<span data-ttu-id="846b4-119">Die Anforderung wurde zur Verarbeitung angenommen, die Verarbeitung wurde jedoch noch nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="846b4-119">The request has been accepted for processing, but the processing has not been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP- \_ Status \_ partiell**</span><span class="sxs-lookup"><span data-stu-id="846b4-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP\_STATUS\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-121">203</span><span class="sxs-lookup"><span data-stu-id="846b4-121">203</span></span>
</dt> <dt>



<span data-ttu-id="846b4-122">Die zurückgegebenen Meta-Informationen im Entitäts Header sind nicht die definitive Menge, die auf dem Ursprungsserver verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="846b4-122">The returned meta information in the entity-header is not the definitive set available from the originating server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP- \_ Status " \_ kein \_ Inhalt"**</span><span class="sxs-lookup"><span data-stu-id="846b4-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP\_STATUS\_NO\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-124">204</span><span class="sxs-lookup"><span data-stu-id="846b4-124">204</span></span>
</dt> <dt>



<span data-ttu-id="846b4-125">Der Server hat die Anforderung erfüllt, aber es sind keine neuen Informationen zum Zurücksenden vorhanden.</span><span class="sxs-lookup"><span data-stu-id="846b4-125">The server has fulfilled the request, but there is no new information to send back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**Inhalt des HTTP- \_ Status \_ Zurücksetzen \_**</span><span class="sxs-lookup"><span data-stu-id="846b4-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**HTTP\_STATUS\_RESET\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-127">205</span><span class="sxs-lookup"><span data-stu-id="846b4-127">205</span></span>
</dt> <dt>



<span data-ttu-id="846b4-128">Die Anforderung wurde abgeschlossen, und das Client Programm sollte die Dokument Ansicht zurücksetzen, die bewirkt hat, dass die Anforderung gesendet wurde, damit der Benutzer problemlos eine andere Eingabe Aktion initiieren kann.</span><span class="sxs-lookup"><span data-stu-id="846b4-128">The request has been completed, and the client program should reset the document view that caused the request to be sent to allow the user to easily initiate another input action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**\_ \_ Teil \_ Inhalt des HTTP-Status**</span><span class="sxs-lookup"><span data-stu-id="846b4-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**HTTP\_STATUS\_PARTIAL\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-130">206</span><span class="sxs-lookup"><span data-stu-id="846b4-130">206</span></span>
</dt> <dt>



<span data-ttu-id="846b4-131">Der Server hat die partielle Get-Anforderung für die Ressource erfüllt.</span><span class="sxs-lookup"><span data-stu-id="846b4-131">The server has fulfilled the partial GET request for the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-132"><span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**HTTP- \_ Status \_ WebDAV- \_ \_ Multistatus**</span><span class="sxs-lookup"><span data-stu-id="846b4-132"><span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**HTTP\_STATUS\_WEBDAV\_MULTI\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-133">207</span><span class="sxs-lookup"><span data-stu-id="846b4-133">207</span></span>
</dt> <dt>



<span data-ttu-id="846b4-134">Während eines WebDAV-Vorgangs (World Wide Web verteilte Erstellung und Versionsverwaltung) gibt dies mehrere Statuscodes für eine einzelne Antwort an.</span><span class="sxs-lookup"><span data-stu-id="846b4-134">During a World Wide Web Distributed Authoring and Versioning (WebDAV) operation, this indicates multiple status codes for a single response.</span></span> <span data-ttu-id="846b4-135">Der Antworttext enthält Extensible Markup Language (XML), der die Statuscodes beschreibt.</span><span class="sxs-lookup"><span data-stu-id="846b4-135">The response body contains Extensible Markup Language (XML) that describes the status codes.</span></span> <span data-ttu-id="846b4-136">Weitere Informationen finden Sie unter [http Extensions for verteilte Authoring](../webdav/webdav-portal.md).</span><span class="sxs-lookup"><span data-stu-id="846b4-136">For more information, see [HTTP Extensions for Distributed Authoring](../webdav/webdav-portal.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-137"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP- \_ Status \_ mehrdeutig**</span><span class="sxs-lookup"><span data-stu-id="846b4-137"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP\_STATUS\_AMBIGUOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-138">300</span><span class="sxs-lookup"><span data-stu-id="846b4-138">300</span></span>
</dt> <dt>



<span data-ttu-id="846b4-139">Die angeforderte Ressource ist an einem oder mehreren Standorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="846b4-139">The requested resource is available at one or more locations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-140"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**HTTP- \_ Status \_ verschoben**</span><span class="sxs-lookup"><span data-stu-id="846b4-140"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**HTTP\_STATUS\_MOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-141">301</span><span class="sxs-lookup"><span data-stu-id="846b4-141">301</span></span>
</dt> <dt>



<span data-ttu-id="846b4-142">Die angeforderte Ressource wurde einem neuen permanenten Uniform Resource Identifier (URI) zugewiesen, und zukünftige Verweise auf diese Ressource sollten mithilfe eines der zurückgegebenen URIs durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="846b4-142">The requested resource has been assigned to a new permanent Uniform Resource Identifier (URI), and any future references to this resource should be done using one of the returned URIs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-143"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP- \_ Status \_ Umleitung**</span><span class="sxs-lookup"><span data-stu-id="846b4-143"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP\_STATUS\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-144">302</span><span class="sxs-lookup"><span data-stu-id="846b4-144">302</span></span>
</dt> <dt>



<span data-ttu-id="846b4-145">Die angeforderte Ressource befindet sich vorübergehend unter einem anderen URI.</span><span class="sxs-lookup"><span data-stu-id="846b4-145">The requested resource resides temporarily under a different URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-146"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP- \_ Status \_ Umleitungs \_ Methode**</span><span class="sxs-lookup"><span data-stu-id="846b4-146"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP\_STATUS\_REDIRECT\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-147">303</span><span class="sxs-lookup"><span data-stu-id="846b4-147">303</span></span>
</dt> <dt>



<span data-ttu-id="846b4-148">Die Antwort auf die Anforderung befindet sich unter einem anderen URI und sollte mit einem get [*http-Verb*](glossary.md) für diese Ressource abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="846b4-148">The response to the request can be found under a different URI and should be retrieved using a GET [*HTTP verb*](glossary.md) on that resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-149"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**HTTP- \_ Status \_ nicht \_ geändert**</span><span class="sxs-lookup"><span data-stu-id="846b4-149"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**HTTP\_STATUS\_NOT\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-150">304</span><span class="sxs-lookup"><span data-stu-id="846b4-150">304</span></span>
</dt> <dt>



<span data-ttu-id="846b4-151">Die angeforderte Ressource wurde nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="846b4-151">The requested resource has not been modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-152"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP \_ - \_ Status \_ Proxy verwenden**</span><span class="sxs-lookup"><span data-stu-id="846b4-152"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP\_STATUS\_USE\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-153">305</span><span class="sxs-lookup"><span data-stu-id="846b4-153">305</span></span>
</dt> <dt>



<span data-ttu-id="846b4-154">Der Zugriff auf die angeforderte Ressource muss über den Proxy erfolgen, der durch das Feld Speicherort angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="846b4-154">The requested resource must be accessed through the proxy given by the location field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-155"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**Keep-Verb für HTTP- \_ Status \_ Umleitung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="846b4-155"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**HTTP\_STATUS\_REDIRECT\_KEEP\_VERB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-156">307</span><span class="sxs-lookup"><span data-stu-id="846b4-156">307</span></span>
</dt> <dt>



<span data-ttu-id="846b4-157">Die umgeleitete Anforderung behält dasselbe [*http-Verb*](glossary.md)bei.</span><span class="sxs-lookup"><span data-stu-id="846b4-157">The redirected request keeps the same [*HTTP verb*](glossary.md).</span></span> <span data-ttu-id="846b4-158">HTTP/1.1-Verhalten.</span><span class="sxs-lookup"><span data-stu-id="846b4-158">HTTP/1.1 behavior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-159"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP-Status ungültige \_ \_ \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="846b4-159"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP\_STATUS\_BAD\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-160">400</span><span class="sxs-lookup"><span data-stu-id="846b4-160">400</span></span>
</dt> <dt>



<span data-ttu-id="846b4-161">Die Anforderung konnte vom Server aufgrund einer ungültigen Syntax nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="846b4-161">The request could not be processed by the server due to invalid syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-162"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP- \_ Status \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="846b4-162"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP\_STATUS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-163">401</span><span class="sxs-lookup"><span data-stu-id="846b4-163">401</span></span>
</dt> <dt>



<span data-ttu-id="846b4-164">Für die angeforderte Ressource ist eine Benutzerauthentifizierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="846b4-164">The requested resource requires user authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-165"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP- \_ Status \_ Zahlung \_ req**</span><span class="sxs-lookup"><span data-stu-id="846b4-165"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP\_STATUS\_PAYMENT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-166">402</span><span class="sxs-lookup"><span data-stu-id="846b4-166">402</span></span>
</dt> <dt>



<span data-ttu-id="846b4-167">Nicht im HTTP-Protokoll implementiert.</span><span class="sxs-lookup"><span data-stu-id="846b4-167">Not implemented in the HTTP protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-168"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP- \_ Status unzulässig \_**</span><span class="sxs-lookup"><span data-stu-id="846b4-168"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP\_STATUS\_FORBIDDEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-169">403</span><span class="sxs-lookup"><span data-stu-id="846b4-169">403</span></span>
</dt> <dt>



<span data-ttu-id="846b4-170">Der Server hat die Anforderung verstanden, kann Sie aber nicht erfüllen.</span><span class="sxs-lookup"><span data-stu-id="846b4-170">The server understood the request, but cannot fulfill it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-171"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**HTTP- \_ Status \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="846b4-171"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**HTTP\_STATUS\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-172">404</span><span class="sxs-lookup"><span data-stu-id="846b4-172">404</span></span>
</dt> <dt>



<span data-ttu-id="846b4-173">Der Server hat nichts gefunden, das mit dem angeforderten URI übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="846b4-173">The server has not found anything that matches the requested URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-174"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP-Status fehlerhafter \_ \_ \_ Methode**</span><span class="sxs-lookup"><span data-stu-id="846b4-174"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP\_STATUS\_BAD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-175">405</span><span class="sxs-lookup"><span data-stu-id="846b4-175">405</span></span>
</dt> <dt>



<span data-ttu-id="846b4-176">Das verwendete [*http-Verb*](glossary.md) ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="846b4-176">The [*HTTP verb*](glossary.md) used is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-177"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP- \_ Status \_ keine \_ akzeptabel**</span><span class="sxs-lookup"><span data-stu-id="846b4-177"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP\_STATUS\_NONE\_ACCEPTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-178">406</span><span class="sxs-lookup"><span data-stu-id="846b4-178">406</span></span>
</dt> <dt>



<span data-ttu-id="846b4-179">Es wurden keine für den Client akzeptablen Antworten gefunden.</span><span class="sxs-lookup"><span data-stu-id="846b4-179">No responses acceptable to the client were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-180"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP- \_ Status \_ Proxy Authentifizierung \_ \_ req**</span><span class="sxs-lookup"><span data-stu-id="846b4-180"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP\_STATUS\_PROXY\_AUTH\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-181">407</span><span class="sxs-lookup"><span data-stu-id="846b4-181">407</span></span>
</dt> <dt>



<span data-ttu-id="846b4-182">Proxy Authentifizierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="846b4-182">Proxy authentication required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-183"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**Timeout für HTTP- \_ Status \_ Anforderung \_**</span><span class="sxs-lookup"><span data-stu-id="846b4-183"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**HTTP\_STATUS\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-184">408</span><span class="sxs-lookup"><span data-stu-id="846b4-184">408</span></span>
</dt> <dt>



<span data-ttu-id="846b4-185">Das Zeitlimit wurde beim Warten auf die Anforderung vom Server überschritten.</span><span class="sxs-lookup"><span data-stu-id="846b4-185">The server timed out waiting for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-186"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP- \_ Status \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="846b4-186"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP\_STATUS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-187">409</span><span class="sxs-lookup"><span data-stu-id="846b4-187">409</span></span>
</dt> <dt>



<span data-ttu-id="846b4-188">Die Anforderung konnte aufgrund eines Konflikts mit dem aktuellen Zustand der Ressource nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="846b4-188">The request could not be completed due to a conflict with the current state of the resource.</span></span> <span data-ttu-id="846b4-189">Der Benutzer sollte erneut mit weiteren Informationen übermitteln.</span><span class="sxs-lookup"><span data-stu-id="846b4-189">The user should resubmit with more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-190"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP- \_ Status ist \_ abgelaufen**</span><span class="sxs-lookup"><span data-stu-id="846b4-190"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP\_STATUS\_GONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-191">410</span><span class="sxs-lookup"><span data-stu-id="846b4-191">410</span></span>
</dt> <dt>



<span data-ttu-id="846b4-192">Die angeforderte Ressource ist auf dem Server nicht mehr verfügbar, und es ist keine Weiterleitungsadresse bekannt.</span><span class="sxs-lookup"><span data-stu-id="846b4-192">The requested resource is no longer available at the server, and no forwarding address is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-193"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**HTTP- \_ Status \_ Länge \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="846b4-193"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**HTTP\_STATUS\_LENGTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-194">411</span><span class="sxs-lookup"><span data-stu-id="846b4-194">411</span></span>
</dt> <dt>



<span data-ttu-id="846b4-195">Der Server kann die Anforderung ohne definierte Inhalts Länge nicht akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="846b4-195">The server cannot accept the request without a defined content length.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-196"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**Fehler beim http \_ -Status " \_ pred". \_**</span><span class="sxs-lookup"><span data-stu-id="846b4-196"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**HTTP\_STATUS\_PRECOND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-197">412</span><span class="sxs-lookup"><span data-stu-id="846b4-197">412</span></span>
</dt> <dt>



<span data-ttu-id="846b4-198">Die Vorbedingung, die in mindestens einem Anforderungs Header Feld angegeben wurde, wurde beim Testen auf dem Server als "false" ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="846b4-198">The precondition given in one or more of the request header fields evaluated to false when it was tested on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-199"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP- \_ Status \_ Anforderung \_ zu \_ groß**</span><span class="sxs-lookup"><span data-stu-id="846b4-199"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP\_STATUS\_REQUEST\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-200">413</span><span class="sxs-lookup"><span data-stu-id="846b4-200">413</span></span>
</dt> <dt>



<span data-ttu-id="846b4-201">Der Server kann die Anforderung nicht verarbeiten, da die Anforderungs Entität größer ist, als der Server verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="846b4-201">The server cannot process the request because the request entity is larger than the server is able to process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-202"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP- \_ Status- \_ URI \_ zu \_ lang**</span><span class="sxs-lookup"><span data-stu-id="846b4-202"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP\_STATUS\_URI\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-203">414</span><span class="sxs-lookup"><span data-stu-id="846b4-203">414</span></span>
</dt> <dt>



<span data-ttu-id="846b4-204">Der Server kann die Anforderung nicht verarbeiten, da der Anforderungs-URI länger ist, als vom Server interpretiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="846b4-204">The server cannot service the request because the request URI is longer than the server can interpret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-205"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**\_ \_ nicht unterstützte HTTP-Status \_ Medien**</span><span class="sxs-lookup"><span data-stu-id="846b4-205"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**HTTP\_STATUS\_UNSUPPORTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-206">415</span><span class="sxs-lookup"><span data-stu-id="846b4-206">415</span></span>
</dt> <dt>



<span data-ttu-id="846b4-207">Der Server kann die Anforderung nicht bedienen, weil die Entität der Anforderung in einem Format vorliegt, das von der angeforderten Ressource für die angeforderte Methode nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="846b4-207">The server cannot service the request because the entity of the request is in a format not supported by the requested resource for the requested method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-208"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP- \_ Status \_ Wiederholung \_ mit**</span><span class="sxs-lookup"><span data-stu-id="846b4-208"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP\_STATUS\_RETRY\_WITH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-209">449</span><span class="sxs-lookup"><span data-stu-id="846b4-209">449</span></span>
</dt> <dt>



<span data-ttu-id="846b4-210">Die Anforderung sollte erneut versucht werden, nachdem Sie die entsprechende Aktion ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="846b4-210">The request should be retried after doing the appropriate action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-211"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP- \_ Status \_ Server \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="846b4-211"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP\_STATUS\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-212">500</span><span class="sxs-lookup"><span data-stu-id="846b4-212">500</span></span>
</dt> <dt>



<span data-ttu-id="846b4-213">Der Server hat eine unerwartete Bedingung feststellen, die die Erfüllung der Anforderung verhindert hat.</span><span class="sxs-lookup"><span data-stu-id="846b4-213">The server encountered an unexpected condition that prevented it from fulfilling the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-214"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**HTTP \_ - \_ Status \_ wird nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="846b4-214"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**HTTP\_STATUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-215">501</span><span class="sxs-lookup"><span data-stu-id="846b4-215">501</span></span>
</dt> <dt>



<span data-ttu-id="846b4-216">Der Server unterstützt die erforderliche Funktionalität zum erfüllen der Anforderung nicht.</span><span class="sxs-lookup"><span data-stu-id="846b4-216">The server does not support the functionality required to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-217"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP-Status ungültiges \_ \_ \_ Gateway**</span><span class="sxs-lookup"><span data-stu-id="846b4-217"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP\_STATUS\_BAD\_GATEWAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-218">502</span><span class="sxs-lookup"><span data-stu-id="846b4-218">502</span></span>
</dt> <dt>



<span data-ttu-id="846b4-219">Der Server hat beim fungieren als Gateway oder Proxy eine ungültige Antwort vom Upstreamserver empfangen, auf den er bei dem Versuch zugegriffen hat, die Anforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="846b4-219">The server, while acting as a gateway or proxy, received an invalid response from the upstream server it accessed in attempting to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-220"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP- \_ Status \_ Dienst \_ nicht erreichbar**</span><span class="sxs-lookup"><span data-stu-id="846b4-220"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP\_STATUS\_SERVICE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-221">503</span><span class="sxs-lookup"><span data-stu-id="846b4-221">503</span></span>
</dt> <dt>



<span data-ttu-id="846b4-222">Der Dienst ist zurzeit überlastet.</span><span class="sxs-lookup"><span data-stu-id="846b4-222">The service is temporarily overloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-223"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP- \_ Status \_ Gateway- \_ Timeout**</span><span class="sxs-lookup"><span data-stu-id="846b4-223"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP\_STATUS\_GATEWAY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-224">504</span><span class="sxs-lookup"><span data-stu-id="846b4-224">504</span></span>
</dt> <dt>



<span data-ttu-id="846b4-225">Bei der Anforderung ist eine Zeitüberschreitung aufgetreten, während auf ein Gateway gewartet wurde.</span><span class="sxs-lookup"><span data-stu-id="846b4-225">The request was timed out waiting for a gateway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="846b4-226"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP- \_ Status \_ Version \_ nicht \_ SUP**</span><span class="sxs-lookup"><span data-stu-id="846b4-226"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP\_STATUS\_VERSION\_NOT\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="846b4-227">505</span><span class="sxs-lookup"><span data-stu-id="846b4-227">505</span></span>
</dt> <dt>



<span data-ttu-id="846b4-228">Die in der Anforderungs Nachricht verwendete HTTP-Protokollversion wird vom Server nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="846b4-228">The server does not support the HTTP protocol version that was used in the request message.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="846b4-229">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="846b4-229">Requirements</span></span>



| <span data-ttu-id="846b4-230">Anforderung</span><span class="sxs-lookup"><span data-stu-id="846b4-230">Requirement</span></span> | <span data-ttu-id="846b4-231">Wert</span><span class="sxs-lookup"><span data-stu-id="846b4-231">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="846b4-232">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="846b4-232">Minimum supported client</span></span><br/> | <span data-ttu-id="846b4-233">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="846b4-233">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="846b4-234">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="846b4-234">Minimum supported server</span></span><br/> | <span data-ttu-id="846b4-235">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="846b4-235">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>   |
| <span data-ttu-id="846b4-236">Header</span><span class="sxs-lookup"><span data-stu-id="846b4-236">Header</span></span><br/>                   | <dl> <span data-ttu-id="846b4-237"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="846b4-237"><dt>Winhttp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="846b4-238">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="846b4-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="846b4-239">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="846b4-239">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

