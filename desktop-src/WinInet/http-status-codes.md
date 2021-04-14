---
title: HTTP-Status Codes (WinInet. h)
description: In der folgenden Tabelle sind die Konstanten und entsprechenden Werte für die HTTP-Statuscodes enthalten, die von Servern im Internet zurückgegeben werden.
ms.assetid: 28a5e889-c8f3-4996-a1ca-c48866fa59d7
topic_type:
- apiref
api_name:
- HTTP_STATUS_CONTINUE
- HTTP_STATUS_SWITCH_PROTOCOLS
- HTTP_STATUS_OK
- HTTP_STATUS_CREATED
- HTTP_STATUS_ACCEPTED
- HTTP_STATUS_PARTIAL
- HTTP_STATUS_NO_CONTENT
- HTTP_STATUS_RESET_CONTENT
- HTTP_STATUS_PARTIAL_CONTENT
- HTTP_STATUS_AMBIGUOUS
- HTTP_STATUS_MOVED
- HTTP_STATUS_REDIRECT
- HTTP_STATUS_REDIRECT_METHOD
- HTTP_STATUS_NOT_MODIFIED
- HTTP_STATUS_USE_PROXY
- HTTP_STATUS_REDIRECT_KEEP_VERB
- HTTP_STATUS_BAD_REQUEST
- HTTP_STATUS_DENIED
- HTTP_STATUS_PAYMENT_REQ
- HTTP_STATUS_FORBIDDEN
- HTTP_STATUS_NOT_FOUND
- HTTP_STATUS_BAD_METHOD
- HTTP_STATUS_NONE_ACCEPTABLE
- HTTP_STATUS_PROXY_AUTH_REQ
- HTTP_STATUS_REQUEST_TIMEOUT
- HTTP_STATUS_CONFLICT
- HTTP_STATUS_GONE
- HTTP_STATUS_LENGTH_REQUIRED
- HTTP_STATUS_PRECOND_FAILED
- HTTP_STATUS_REQUEST_TOO_LARGE
- HTTP_STATUS_URI_TOO_LONG
- HTTP_STATUS_UNSUPPORTED_MEDIA
- HTTP_STATUS_RETRY_WITH
- HTTP_STATUS_SERVER_ERROR
- HTTP_STATUS_NOT_SUPPORTED
- HTTP_STATUS_BAD_GATEWAY
- HTTP_STATUS_SERVICE_UNAVAIL
- HTTP_STATUS_GATEWAY_TIMEOUT
- HTTP_STATUS_VERSION_NOT_SUP
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6933617b0488e059c029dd783af238a3ddbb3ecb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392195"
---
# <a name="http-status-codes-winineth"></a><span data-ttu-id="8cf7e-103">HTTP-Status Codes (WinInet. h)</span><span class="sxs-lookup"><span data-stu-id="8cf7e-103">HTTP Status Codes (Wininet.h)</span></span>

<span data-ttu-id="8cf7e-104">In der folgenden Tabelle sind die Konstanten und entsprechenden Werte für die HTTP-Statuscodes enthalten, die von Servern im Internet zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-104">The following table contains the constants and corresponding values for the HTTP status codes returned by servers on the Internet.</span></span>

<dl> <dt>

<span data-ttu-id="8cf7e-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP- \_ Status \_ fortsetzen**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-106">100</span><span class="sxs-lookup"><span data-stu-id="8cf7e-106">100</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-107">Die Anforderung kann fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-107">The request can be continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP- \_ Status \_ Schalter \_ Protokolle**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP\_STATUS\_SWITCH\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-109">101</span><span class="sxs-lookup"><span data-stu-id="8cf7e-109">101</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-110">Der Server hat die Protokolle in einem Upgradeheader geändert.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-110">The server has switched protocols in an upgrade header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP- \_ Status \_ OK**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP\_STATUS\_OK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-112">200</span><span class="sxs-lookup"><span data-stu-id="8cf7e-112">200</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-113">Die Anforderung wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-113">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**HTTP- \_ Status \_ erstellt**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**HTTP\_STATUS\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-115">201</span><span class="sxs-lookup"><span data-stu-id="8cf7e-115">201</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-116">Die Anforderung wurde erfüllt und führte zur Erstellung einer neuen Ressource.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-116">The request has been fulfilled and resulted in the creation of a new resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP- \_ Status \_ akzeptiert**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP\_STATUS\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-118">202</span><span class="sxs-lookup"><span data-stu-id="8cf7e-118">202</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-119">Die Anforderung wurde zur Verarbeitung angenommen, die Verarbeitung wurde jedoch noch nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-119">The request has been accepted for processing, but the processing has not been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP- \_ Status \_ partiell**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP\_STATUS\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-121">203</span><span class="sxs-lookup"><span data-stu-id="8cf7e-121">203</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-122">Die zurückgegebenen Meta-Informationen im Entitäts Header sind nicht die definitive Menge, die auf dem Ursprungsserver verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-122">The returned meta information in the entity-header is not the definitive set available from the origin server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP- \_ Status " \_ kein \_ Inhalt"**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP\_STATUS\_NO\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-124">204</span><span class="sxs-lookup"><span data-stu-id="8cf7e-124">204</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-125">Der Server hat die Anforderung erfüllt, aber es sind keine neuen Informationen zum Zurücksenden vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-125">The server has fulfilled the request, but there is no new information to send back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**Inhalt des HTTP- \_ Status \_ Zurücksetzen \_**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**HTTP\_STATUS\_RESET\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-127">205</span><span class="sxs-lookup"><span data-stu-id="8cf7e-127">205</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-128">Die Anforderung wurde abgeschlossen, und das Client Programm sollte die Dokument Ansicht zurücksetzen, die bewirkt hat, dass die Anforderung gesendet wurde, damit der Benutzer problemlos eine andere Eingabe Aktion initiieren kann.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-128">The request has been completed, and the client program should reset the document view that caused the request to be sent to allow the user to easily initiate another input action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**\_ \_ Teil \_ Inhalt des HTTP-Status**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**HTTP\_STATUS\_PARTIAL\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-130">206</span><span class="sxs-lookup"><span data-stu-id="8cf7e-130">206</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-131">Der Server hat die partielle Get-Anforderung für die Ressource erfüllt.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-131">The server has fulfilled the partial GET request for the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-132"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP- \_ Status \_ mehrdeutig**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-132"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP\_STATUS\_AMBIGUOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-133">300</span><span class="sxs-lookup"><span data-stu-id="8cf7e-133">300</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-134">Der Server konnte nicht entscheiden, was zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-134">The server couldn't decide what to return.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-135"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**HTTP- \_ Status \_ verschoben**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-135"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**HTTP\_STATUS\_MOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-136">301</span><span class="sxs-lookup"><span data-stu-id="8cf7e-136">301</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-137">Die angeforderte Ressource wurde einem neuen permanenten URI (Uniform Resource Identifier) zugewiesen, und zukünftige Verweise auf diese Ressource sollten mithilfe eines der zurückgegebenen URIs durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-137">The requested resource has been assigned to a new permanent URI (Uniform Resource Identifier), and any future references to this resource should be done using one of the returned URIs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-138"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP- \_ Status \_ Umleitung**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-138"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP\_STATUS\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-139">302</span><span class="sxs-lookup"><span data-stu-id="8cf7e-139">302</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-140">Die angeforderte Ressource befindet sich vorübergehend unter einem anderen URI (Uniform Resource Identifier).</span><span class="sxs-lookup"><span data-stu-id="8cf7e-140">The requested resource resides temporarily under a different URI (Uniform Resource Identifier).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-141"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP- \_ Status \_ Umleitungs \_ Methode**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-141"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP\_STATUS\_REDIRECT\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-142">303</span><span class="sxs-lookup"><span data-stu-id="8cf7e-142">303</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-143">Die Antwort auf die Anforderung befindet sich unter einem anderen URI (Uniform Resource Identifier) und sollte mit einem get http-Verb für diese Ressource abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-143">The response to the request can be found under a different URI (Uniform Resource Identifier) and should be retrieved using a GET HTTP verb on that resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-144"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**HTTP- \_ Status \_ nicht \_ geändert**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-144"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**HTTP\_STATUS\_NOT\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-145">304</span><span class="sxs-lookup"><span data-stu-id="8cf7e-145">304</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-146">Die angeforderte Ressource wurde nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-146">The requested resource has not been modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-147"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP \_ - \_ Status \_ Proxy verwenden**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-147"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP\_STATUS\_USE\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-148">305</span><span class="sxs-lookup"><span data-stu-id="8cf7e-148">305</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-149">Der Zugriff auf die angeforderte Ressource muss über den Proxy erfolgen, der durch das Feld Speicherort angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-149">The requested resource must be accessed through the proxy given by the location field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-150"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**Keep-Verb für HTTP- \_ Status \_ Umleitung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-150"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**HTTP\_STATUS\_REDIRECT\_KEEP\_VERB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-151">307</span><span class="sxs-lookup"><span data-stu-id="8cf7e-151">307</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-152">Die umgeleitete Anforderung behält dasselbe http-Verb bei.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-152">The redirected request keeps the same HTTP verb.</span></span> <span data-ttu-id="8cf7e-153">HTTP/1.1-Verhalten.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-153">HTTP/1.1 behavior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-154"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP-Status ungültige \_ \_ \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-154"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP\_STATUS\_BAD\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-155">400</span><span class="sxs-lookup"><span data-stu-id="8cf7e-155">400</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-156">Die Anforderung konnte vom Server aufgrund einer ungültigen Syntax nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-156">The request could not be processed by the server due to invalid syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-157"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP- \_ Status \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-157"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP\_STATUS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-158">401</span><span class="sxs-lookup"><span data-stu-id="8cf7e-158">401</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-159">Für die angeforderte Ressource ist eine Benutzerauthentifizierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-159">The requested resource requires user authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-160"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP- \_ Status \_ Zahlung \_ req**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-160"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP\_STATUS\_PAYMENT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-161">402</span><span class="sxs-lookup"><span data-stu-id="8cf7e-161">402</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-162">Derzeit nicht im HTTP-Protokoll implementiert.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-162">Not currently implemented in the HTTP protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-163"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP- \_ Status unzulässig \_**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-163"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP\_STATUS\_FORBIDDEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-164">403</span><span class="sxs-lookup"><span data-stu-id="8cf7e-164">403</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-165">Der Server hat die Anforderung verstanden, hat jedoch die Erfüllung der Anforderung verweigert.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-165">The server understood the request, but is refusing to fulfill it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-166"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**HTTP- \_ Status \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-166"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**HTTP\_STATUS\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-167">404</span><span class="sxs-lookup"><span data-stu-id="8cf7e-167">404</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-168">Der Server hat nichts gefunden, das mit dem angeforderten URI (Uniform Resource Identifier) übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-168">The server has not found anything matching the requested URI (Uniform Resource Identifier).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-169"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP-Status fehlerhafter \_ \_ \_ Methode**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-169"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP\_STATUS\_BAD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-170">405</span><span class="sxs-lookup"><span data-stu-id="8cf7e-170">405</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-171">Das verwendete HTTP-Verb ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-171">The HTTP verb used is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-172"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP- \_ Status \_ keine \_ akzeptabel**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-172"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP\_STATUS\_NONE\_ACCEPTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-173">406</span><span class="sxs-lookup"><span data-stu-id="8cf7e-173">406</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-174">Es wurden keine für den Client akzeptablen Antworten gefunden.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-174">No responses acceptable to the client were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-175"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP- \_ Status \_ Proxy Authentifizierung \_ \_ req**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-175"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP\_STATUS\_PROXY\_AUTH\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-176">407</span><span class="sxs-lookup"><span data-stu-id="8cf7e-176">407</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-177">Proxy Authentifizierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-177">Proxy authentication required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-178"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**Timeout für HTTP- \_ Status \_ Anforderung \_**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-178"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**HTTP\_STATUS\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-179">408</span><span class="sxs-lookup"><span data-stu-id="8cf7e-179">408</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-180">Das Zeitlimit wurde beim Warten auf die Anforderung vom Server überschritten.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-180">The server timed out waiting for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-181"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP- \_ Status \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-181"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP\_STATUS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-182">409</span><span class="sxs-lookup"><span data-stu-id="8cf7e-182">409</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-183">Die Anforderung konnte aufgrund eines Konflikts mit dem aktuellen Zustand der Ressource nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-183">The request could not be completed due to a conflict with the current state of the resource.</span></span> <span data-ttu-id="8cf7e-184">Der Benutzer sollte erneut mit weiteren Informationen übermitteln.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-184">The user should resubmit with more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-185"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP- \_ Status ist \_ abgelaufen**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-185"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP\_STATUS\_GONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-186">410</span><span class="sxs-lookup"><span data-stu-id="8cf7e-186">410</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-187">Die angeforderte Ressource ist auf dem Server nicht mehr verfügbar, und es ist keine Weiterleitungsadresse bekannt.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-187">The requested resource is no longer available at the server, and no forwarding address is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-188"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**HTTP- \_ Status \_ Länge \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-188"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**HTTP\_STATUS\_LENGTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-189">411</span><span class="sxs-lookup"><span data-stu-id="8cf7e-189">411</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-190">Der Server lehnt die Annahme der Anforderung ohne eine definierte Inhalts Länge ab.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-190">The server refuses to accept the request without a defined content length.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-191"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**Fehler beim http \_ -Status " \_ pred". \_**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-191"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**HTTP\_STATUS\_PRECOND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-192">412</span><span class="sxs-lookup"><span data-stu-id="8cf7e-192">412</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-193">Die Vorbedingung, die in mindestens einem Anforderungs Header Feld angegeben wurde, wurde beim Testen auf dem Server als "false" ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-193">The precondition given in one or more of the request header fields evaluated to false when it was tested on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-194"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP- \_ Status \_ Anforderung \_ zu \_ groß**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-194"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP\_STATUS\_REQUEST\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-195">413</span><span class="sxs-lookup"><span data-stu-id="8cf7e-195">413</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-196">Der Server hat die Verarbeitung einer Anforderung verweigert, da die Anforderungs Entität größer ist, als der Server bereit ist oder verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-196">The server is refusing to process a request because the request entity is larger than the server is willing or able to process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-197"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP- \_ Status- \_ URI \_ zu \_ lang**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-197"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP\_STATUS\_URI\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-198">414</span><span class="sxs-lookup"><span data-stu-id="8cf7e-198">414</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-199">Der Server kann die Anforderung nicht verarbeiten, da der Anforderungs-URI (Uniform Resource Identifier) länger ist, als der Server zur Interpretation bereit ist.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-199">The server is refusing to service the request because the request URI (Uniform Resource Identifier) is longer than the server is willing to interpret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-200"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**\_ \_ nicht unterstützte HTTP-Status \_ Medien**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-200"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**HTTP\_STATUS\_UNSUPPORTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-201">415</span><span class="sxs-lookup"><span data-stu-id="8cf7e-201">415</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-202">Der Server lehnt die Dienst Anforderung ab, da die Entität der Anforderung in einem Format vorliegt, das von der angeforderten Ressource für die angeforderte Methode nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-202">The server is refusing to service the request because the entity of the request is in a format not supported by the requested resource for the requested method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-203"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP- \_ Status \_ Wiederholung \_ mit**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-203"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP\_STATUS\_RETRY\_WITH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-204">449</span><span class="sxs-lookup"><span data-stu-id="8cf7e-204">449</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-205">Die Anforderung sollte erneut versucht werden, nachdem Sie die entsprechende Aktion ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-205">The request should be retried after doing the appropriate action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-206"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP- \_ Status \_ Server \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-206"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP\_STATUS\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-207">500</span><span class="sxs-lookup"><span data-stu-id="8cf7e-207">500</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-208">Der Server hat eine unerwartete Bedingung feststellen, die die Erfüllung der Anforderung verhindert hat.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-208">The server encountered an unexpected condition that prevented it from fulfilling the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-209"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**HTTP \_ - \_ Status \_ wird nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-209"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**HTTP\_STATUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-210">501</span><span class="sxs-lookup"><span data-stu-id="8cf7e-210">501</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-211">Der Server unterstützt die erforderliche Funktionalität zum erfüllen der Anforderung nicht.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-211">The server does not support the functionality required to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-212"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP-Status ungültiges \_ \_ \_ Gateway**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-212"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP\_STATUS\_BAD\_GATEWAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-213">502</span><span class="sxs-lookup"><span data-stu-id="8cf7e-213">502</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-214">Der Server hat beim fungieren als Gateway oder Proxy eine ungültige Antwort vom Upstreamserver empfangen, auf den er bei dem Versuch zugegriffen hat, die Anforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-214">The server, while acting as a gateway or proxy, received an invalid response from the upstream server it accessed in attempting to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-215"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP- \_ Status \_ Dienst \_ nicht erreichbar**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-215"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP\_STATUS\_SERVICE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-216">503</span><span class="sxs-lookup"><span data-stu-id="8cf7e-216">503</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-217">Der Dienst ist zurzeit überlastet.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-217">The service is temporarily overloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-218"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP- \_ Status \_ Gateway- \_ Timeout**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-218"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP\_STATUS\_GATEWAY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-219">504</span><span class="sxs-lookup"><span data-stu-id="8cf7e-219">504</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-220">Bei der Anforderung ist eine Zeitüberschreitung aufgetreten, während auf ein Gateway gewartet wurde.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-220">The request was timed out waiting for a gateway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf7e-221"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP- \_ Status \_ Version \_ nicht \_ SUP**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-221"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP\_STATUS\_VERSION\_NOT\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf7e-222">505</span><span class="sxs-lookup"><span data-stu-id="8cf7e-222">505</span></span>
</dt> <dt>



<span data-ttu-id="8cf7e-223">Der Server unterstützt die in der Anforderungs Nachricht verwendete HTTP-Protokollversion nicht oder lehnt sie ab.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-223">The server does not support, or refuses to support, the HTTP protocol version that was used in the request message.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cf7e-224">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8cf7e-224">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8cf7e-225">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-225">WinINet does not support server implementations.</span></span> <span data-ttu-id="8cf7e-226">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-226">In addition, it should not be used from a service.</span></span> <span data-ttu-id="8cf7e-227">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="8cf7e-227">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8cf7e-228">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cf7e-228">Requirements</span></span>



| <span data-ttu-id="8cf7e-229">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cf7e-229">Requirement</span></span> | <span data-ttu-id="8cf7e-230">Wert</span><span class="sxs-lookup"><span data-stu-id="8cf7e-230">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf7e-231">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8cf7e-231">Minimum supported client</span></span><br/> | <span data-ttu-id="8cf7e-232">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8cf7e-232">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8cf7e-233">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8cf7e-233">Minimum supported server</span></span><br/> | <span data-ttu-id="8cf7e-234">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8cf7e-234">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8cf7e-235">Header</span><span class="sxs-lookup"><span data-stu-id="8cf7e-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cf7e-236"><dt>Wininet. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cf7e-236"><dt>Wininet.h</dt></span></span> </dl> |



 

