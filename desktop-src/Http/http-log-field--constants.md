---
title: HTTP_LOG_FIELD_ Konstanten (http. h)
description: Definieren Sie die Felder im W3C-Protokoll und in den Fehlerprotokollen.
ms.assetid: 44307d5a-f413-4ee9-9f9c-586c824d5493
topic_type:
- apiref
api_name:
- HTTP_LOG_FIELD_DATE
- HTTP_LOG_FIELD_TIME
- HTTP_LOG_FIELD_CLIENT_IP
- HTTP_LOG_FIELD_USER_NAME
- HTTP_LOG_FIELD_SITE_NAME
- HTTP_LOG_FIELD_COMPUTER_NAME
- HTTP_LOG_FIELD_SERVER_IP
- HTTP_LOG_FIELD_METHOD
- HTTP_LOG_FIELD_URI_STEM
- HTTP_LOG_FIELD_URI_QUERY
- HTTP_LOG_FIELD_STATUS
- HTTP_LOG_FIELD_WIN32_STATUS
- HTTP_LOG_FIELD_BYTES_SENT
- HTTP_LOG_FIELD_BYTES_RECV
- HTTP_LOG_FIELD_TIME_TAKEN
- HTTP_LOG_FIELD_SERVER_PORT
- HTTP_LOG_FIELD_USER_AGENT
- HTTP_LOG_FIELD_COOKIE
- HTTP_LOG_FIELD_REFERER
- HTTP_LOG_FIELD_VERSION
- HTTP_LOG_FIELD_HOST
- HTTP_LOG_FIELD_SUB_STATUS
- HTTP_LOG_FIELD_CLIENT_PORT
- HTTP_LOG_FIELD_URI
- HTTP_LOG_FIELD_SITE_ID
- HTTP_LOG_FIELD_REASON
- HTTP_LOG_FIELD_QUEUE_NAME
- HTTP_LOG_FIELD_STREAMID
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9ab05a9126cb5ffb81b65a460e6a9d671c268bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340992"
---
# <a name="http_log_field_-constants"></a><span data-ttu-id="57bf7-103">HTTP- \_ Protokoll \_ Feld \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="57bf7-103">HTTP\_LOG\_FIELD\_ Constants</span></span>

<span data-ttu-id="57bf7-104">Die **http \_ - \_ Protokoll \_ Feld** Konstanten definieren die Felder im W3C-Protokoll und die Fehlerprotokolle.</span><span class="sxs-lookup"><span data-stu-id="57bf7-104">The **HTTP\_LOG\_FIELD\_** constants define the fields in the W3C log and the error logs.</span></span>

<span data-ttu-id="57bf7-105">Diese Konstanten werden in der [**http- \_ Protokollierungs \_ Informations**](/windows/desktop/api/Http/ns-http-http_logging_info) Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="57bf7-105">These constants are used in the [**HTTP\_LOGGING\_INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="57bf7-106"><span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**\_ \_ Feld \_ Datum des HTTP-Protokolls**</span><span class="sxs-lookup"><span data-stu-id="57bf7-106"><span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**HTTP\_LOG\_FIELD\_DATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-107">Das Datum, an dem die Aktivität aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="57bf7-107">The date on which the activity occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-108"><span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**\_ \_ Feld \_ Zeit für HTTP-Protokoll**</span><span class="sxs-lookup"><span data-stu-id="57bf7-108"><span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**HTTP\_LOG\_FIELD\_TIME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-109">Die Uhrzeit in koordinierter Weltzeit (UTC), zu der die Aktivität aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="57bf7-109">The time, in coordinated universal time (UTC), at which the activity occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-110"><span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**HTTP \_ \_ -Protokollfeld \_ Client \_ -IP**</span><span class="sxs-lookup"><span data-stu-id="57bf7-110"><span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**HTTP\_LOG\_FIELD\_CLIENT\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-111">Die IP-Adresse des Clients, der die Anforderung gestellt hat.</span><span class="sxs-lookup"><span data-stu-id="57bf7-111">The IP address of the client that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-112"><span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**Benutzer Name für das HTTP- \_ Protokoll \_ Feld \_ \_**</span><span class="sxs-lookup"><span data-stu-id="57bf7-112"><span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**HTTP\_LOG\_FIELD\_USER\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-113">Der Name des authentifizierten Benutzers, der auf den Server zugegriffen hat.</span><span class="sxs-lookup"><span data-stu-id="57bf7-113">The name of the authenticated user who accessed your server.</span></span> <span data-ttu-id="57bf7-114">Anonyme Benutzer werden durch einen Bindestrich gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="57bf7-114">Anonymous users are indicated by a hyphen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-115"><span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**HTTP- \_ Protokoll \_ Feld- \_ Website \_ Name**</span><span class="sxs-lookup"><span data-stu-id="57bf7-115"><span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**HTTP\_LOG\_FIELD\_SITE\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-116">Der Name der Website, auf der der Protokolldatei Eintrag generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="57bf7-116">The name of the site on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-117"><span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span>**Http \_ \_ \_ Computer \_ Name für Protokollfeld**</span><span class="sxs-lookup"><span data-stu-id="57bf7-117"><span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span> **HTTP\_LOG\_FIELD\_COMPUTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-118">Der Name des Computers, auf dem der Protokolldatei Eintrag generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="57bf7-118">The name of the computer on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-119"><span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**HTTP \_ \_ -Protokollfeld \_ Server \_ -IP**</span><span class="sxs-lookup"><span data-stu-id="57bf7-119"><span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**HTTP\_LOG\_FIELD\_SERVER\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-120">Die IP-Adresse des Servers, auf dem der Protokolldatei Eintrag generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="57bf7-120">The IP address of the server on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-121"><span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**HTTP- \_ Protokoll \_ Feld \_ Methode**</span><span class="sxs-lookup"><span data-stu-id="57bf7-121"><span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**HTTP\_LOG\_FIELD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-122">Die angeforderte Aktion, z. b. eine Get-Methode.</span><span class="sxs-lookup"><span data-stu-id="57bf7-122">The requested action, for example, a get method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-123"><span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span>**Http \_ \_URI- \_ \_ Stamm des Protokoll Felds**</span><span class="sxs-lookup"><span data-stu-id="57bf7-123"><span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span> **HTTP\_LOG\_FIELD\_URI\_STEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-124">Das Ziel der Aktion, z. b. Default.htm.</span><span class="sxs-lookup"><span data-stu-id="57bf7-124">The target of the action, for example, Default.htm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-125"><span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**URI-Abfrage für HTTP- \_ Protokoll \_ Feld \_ \_**</span><span class="sxs-lookup"><span data-stu-id="57bf7-125"><span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**HTTP\_LOG\_FIELD\_URI\_QUERY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-126">Die Abfrage, die der Client auszuführen versucht hat, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="57bf7-126">The query, if any, that the client was trying to perform.</span></span> <span data-ttu-id="57bf7-127">Eine Abfrage-URI (Universal Resource Identifier) ist nur für dynamische Seiten erforderlich.</span><span class="sxs-lookup"><span data-stu-id="57bf7-127">A Universal Resource Identifier (URI) query is necessary only for dynamic pages.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-128"><span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**Status des HTTP- \_ Protokoll \_ Felds \_**</span><span class="sxs-lookup"><span data-stu-id="57bf7-128"><span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**HTTP\_LOG\_FIELD\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-129">Der HTTP-Statuscode.</span><span class="sxs-lookup"><span data-stu-id="57bf7-129">The HTTP status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-130"><span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**Win32-Status des HTTP- \_ Protokoll \_ Felds \_ \_**</span><span class="sxs-lookup"><span data-stu-id="57bf7-130"><span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**HTTP\_LOG\_FIELD\_WIN32\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-131">Der Windows-Statuscode.</span><span class="sxs-lookup"><span data-stu-id="57bf7-131">The Windows status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-132"><span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**\_gesendete HTTP-Protokoll \_ Feld \_ Bytes \_**</span><span class="sxs-lookup"><span data-stu-id="57bf7-132"><span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**HTTP\_LOG\_FIELD\_BYTES\_SENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-133">Die Nummer in Bytes, die vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="57bf7-133">The number, in bytes, sent by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-134"><span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**HTTP- \_ Protokoll \_ Feld ( \_ Bytes \_ )**</span><span class="sxs-lookup"><span data-stu-id="57bf7-134"><span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**HTTP\_LOG\_FIELD\_BYTES\_RECV**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-135">Die Nummer in Bytes, die vom Server empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="57bf7-135">The number, in bytes, received by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-136"><span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**Zeit für das HTTP- \_ Protokoll \_ Feld \_ \_**</span><span class="sxs-lookup"><span data-stu-id="57bf7-136"><span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**HTTP\_LOG\_FIELD\_TIME\_TAKEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-137">Die Zeit (in Millisekunden) der Aktion.</span><span class="sxs-lookup"><span data-stu-id="57bf7-137">The time, in milliseconds, of the action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-138"><span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**HTTP- \_ Protokoll \_ Feld- \_ \_ Serverport**</span><span class="sxs-lookup"><span data-stu-id="57bf7-138"><span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**HTTP\_LOG\_FIELD\_SERVER\_PORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-139">Die für den Dienst konfigurierte Server Portnummer.</span><span class="sxs-lookup"><span data-stu-id="57bf7-139">The server port number that is configured for the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-140"><span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span>**Http \_ Protokoll \_ Feld \_ Benutzer- \_ Agent**</span><span class="sxs-lookup"><span data-stu-id="57bf7-140"><span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span> **HTTP\_LOG\_FIELD\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-141">Die Anwendung, die vom Client verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="57bf7-141">The application that the client used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-142"><span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**HTTP- \_ Protokoll \_ Feld \_ Cookie**</span><span class="sxs-lookup"><span data-stu-id="57bf7-142"><span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**HTTP\_LOG\_FIELD\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-143">Der Inhalt des gesendeten oder empfangenen Cookies, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="57bf7-143">The content of the cookie sent or received, if any.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-144"><span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**HTTP- \_ Protokoll \_ Feld \_ Verweis**</span><span class="sxs-lookup"><span data-stu-id="57bf7-144"><span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**HTTP\_LOG\_FIELD\_REFERER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-145">Die Website, die der Benutzer zuletzt besucht hat.</span><span class="sxs-lookup"><span data-stu-id="57bf7-145">The site that the user last visited.</span></span> <span data-ttu-id="57bf7-146">Diese Website stellte eine Verknüpfung zur aktuellen Website her.</span><span class="sxs-lookup"><span data-stu-id="57bf7-146">This site provided a link to the current site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-147"><span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**HTTP- \_ Protokoll \_ Feld \_ Version**</span><span class="sxs-lookup"><span data-stu-id="57bf7-147"><span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**HTTP\_LOG\_FIELD\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-148">Die vom Client verwendete HTTP-Protokollversion.</span><span class="sxs-lookup"><span data-stu-id="57bf7-148">The HTTP protocol version that the client used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-149"><span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**HTTP- \_ Protokoll \_ Feld \_ Host**</span><span class="sxs-lookup"><span data-stu-id="57bf7-149"><span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**HTTP\_LOG\_FIELD\_HOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-150">Der Host Header Name (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="57bf7-150">The host header name, if any.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-151"><span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**unter Status des HTTP- \_ Protokoll \_ Felds \_ \_**</span><span class="sxs-lookup"><span data-stu-id="57bf7-151"><span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**HTTP\_LOG\_FIELD\_SUB\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-152">Der unter Status-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="57bf7-152">The substatus error code.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="57bf7-153">Die folgenden Konstanten werden für die HTTP-Fehler Protokollierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="57bf7-153">The following constants are used for HTTP error logging.</span></span>

<dl> <dt>

<span data-ttu-id="57bf7-154"><span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**HTTP- \_ Protokoll \_ Feld- \_ \_ ClientPort**</span><span class="sxs-lookup"><span data-stu-id="57bf7-154"><span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**HTTP\_LOG\_FIELD\_CLIENT\_PORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-155">Die Client Portnummer, von der die Anforderung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="57bf7-155">The client port number from which the request is received.</span></span> <span data-ttu-id="57bf7-156">Dieses Protokollfeld wird nur für die Fehler Protokollierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="57bf7-156">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-157"><span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**URI für HTTP- \_ Protokoll \_ Feld \_**</span><span class="sxs-lookup"><span data-stu-id="57bf7-157"><span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**HTTP\_LOG\_FIELD\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-158">Der in der Anforderung empfangene URI, einschließlich des Abfrage Teils.</span><span class="sxs-lookup"><span data-stu-id="57bf7-158">The URI received in the request including the query portion.</span></span> <span data-ttu-id="57bf7-159">Dieses Protokollfeld wird nur für die Fehler Protokollierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="57bf7-159">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-160"><span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**Website-ID für HTTP- \_ Protokoll \_ Feld \_ \_**</span><span class="sxs-lookup"><span data-stu-id="57bf7-160"><span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**HTTP\_LOG\_FIELD\_SITE\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-161">Die anwendungsspezifische numerische ID der URL-Gruppe, an die die Anforderung weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="57bf7-161">The application-specific numeric ID of the URL Group on which the request is routed.</span></span> <span data-ttu-id="57bf7-162">Dieses Protokollfeld wird nur für die Fehler Protokollierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="57bf7-162">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-163"><span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**Grund für HTTP- \_ Protokoll \_ Feld \_**</span><span class="sxs-lookup"><span data-stu-id="57bf7-163"><span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**HTTP\_LOG\_FIELD\_REASON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-164">Der Fehlerursachen Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="57bf7-164">The error reason phrase.</span></span> <span data-ttu-id="57bf7-165">Dieses Protokollfeld wird nur für die Fehler Protokollierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="57bf7-165">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-166"><span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**\_ \_ \_ Warteschlangen \_ Name für http-Protokollfeld**</span><span class="sxs-lookup"><span data-stu-id="57bf7-166"><span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**HTTP\_LOG\_FIELD\_QUEUE\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-167">Der Name der Anforderungs Warteschlange, an die die Anforderung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="57bf7-167">The name of the request queue to which the request is dispatched.</span></span> <span data-ttu-id="57bf7-168">Dieses Protokollfeld wird nur für die Fehler Protokollierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="57bf7-168">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57bf7-169"><span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**HTTP- \_ Protokoll \_ Feld- \_ streamid**</span><span class="sxs-lookup"><span data-stu-id="57bf7-169"><span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**HTTP\_LOG\_FIELD\_STREAMID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57bf7-170">Die Datenstrom-ID.</span><span class="sxs-lookup"><span data-stu-id="57bf7-170">The stream id.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="57bf7-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57bf7-171">Requirements</span></span>



| <span data-ttu-id="57bf7-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57bf7-172">Requirement</span></span> | <span data-ttu-id="57bf7-173">Wert</span><span class="sxs-lookup"><span data-stu-id="57bf7-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="57bf7-174">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57bf7-174">Minimum supported client</span></span><br/> | <span data-ttu-id="57bf7-175">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57bf7-175">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="57bf7-176">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57bf7-176">Minimum supported server</span></span><br/> | <span data-ttu-id="57bf7-177">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57bf7-177">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="57bf7-178">Header</span><span class="sxs-lookup"><span data-stu-id="57bf7-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="57bf7-179"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="57bf7-179"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57bf7-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57bf7-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57bf7-181">HTTP-Server-API, Version 2,0, Konstanten</span><span class="sxs-lookup"><span data-stu-id="57bf7-181">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="57bf7-182">**HTTP- \_ Protokollierungs \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="57bf7-182">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[<span data-ttu-id="57bf7-183">**Httptarturlgroupproperty**</span><span class="sxs-lookup"><span data-stu-id="57bf7-183">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="57bf7-184">**Httpsetserversessionproperty**</span><span class="sxs-lookup"><span data-stu-id="57bf7-184">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="57bf7-185">**Httpqueryurlgroupproperty**</span><span class="sxs-lookup"><span data-stu-id="57bf7-185">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="57bf7-186">**Httpqueryserversessionproperty**</span><span class="sxs-lookup"><span data-stu-id="57bf7-186">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





