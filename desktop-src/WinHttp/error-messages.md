---
description: Die in diesem Thema identifizierten Fehler Werte werden von GetLastError zurückgegeben, wenn eine der Microsoft Windows HTTP-Dienste (WinHTTP) fehlschlägt.
ms.assetid: c8a863cd-d36c-4ec8-ac49-0b714a5e4cc2
title: Fehlermeldungen (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccdc8be4b1e7c3cc7f9a03403c2f8778ddd19b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866232"
---
# <a name="error-messages-winhttph"></a><span data-ttu-id="cdb89-103">Fehlermeldungen (WinHTTP. h)</span><span class="sxs-lookup"><span data-stu-id="cdb89-103">Error Messages (Winhttp.h)</span></span>

<span data-ttu-id="cdb89-104">Die unten aufgeführten Fehler Werte werden von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) zurückgegeben, wenn eine der Microsoft Windows HTTP-Dienste (WinHTTP) fehlschlägt und auch in den unteren 16 Bits der [**HRESULT**](../com/structure-of-com-error-codes.md) -Fehler zurückgegeben wird, die vom [**WinHttpRequest**](winhttprequest.md) -Objekt zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cdb89-104">The error values listed below are returned by [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) when one of the Microsoft Windows HTTP Services (WinHTTP) functions fails, and are also returned in the lower 16 bits of [**HRESULT**](../com/structure-of-com-error-codes.md) error returns from the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

<span data-ttu-id="cdb89-105">Fehler Werte, deren Namen mit "Fehler- \_ WinHTTP \_ " beginnen, sind spezifisch für die WinHTTP-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="cdb89-105">Error values whose names begin with "ERROR\_WINHTTP\_" are specific to the WinHTTP functions.</span></span> <span data-ttu-id="cdb89-106">Die WinHTTP-Funktionen geben ggf. auch Windows-Fehlermeldungen zurück.</span><span class="sxs-lookup"><span data-stu-id="cdb89-106">The WinHTTP functions also return Windows error messages where appropriate.</span></span>

<dl> <dt>

<span data-ttu-id="cdb89-107"><span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**Fehler beim \_ WinHTTP- \_ automatischen \_ Proxy \_ Dienst \_ .**</span><span class="sxs-lookup"><span data-stu-id="cdb89-107"><span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**ERROR\_WINHTTP\_AUTO\_PROXY\_SERVICE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-108">12178</span><span class="sxs-lookup"><span data-stu-id="cdb89-108">12178</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-109">Wird von [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) zurückgegeben, wenn ein Proxy für die angegebene URL nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="cdb89-109">Returned by [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) when a proxy for the specified URL cannot be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-110"><span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**Fehler beim \_ WinHTTP- \_ Autoerkennungs-Fehler. \_**</span><span class="sxs-lookup"><span data-stu-id="cdb89-110"><span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**ERROR\_WINHTTP\_AUTODETECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-111">12180</span><span class="sxs-lookup"><span data-stu-id="cdb89-111">12180</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-112">Wird von [**winhttpdetectautoproxyconfigurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) zurückgegeben, wenn WinHTTP die URL der PAC-Datei (Proxy Auto-Configuration) nicht ermitteln konnte.</span><span class="sxs-lookup"><span data-stu-id="cdb89-112">Returned by [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) if WinHTTP was unable to discover the URL of the Proxy Auto-Configuration (PAC) file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-113"><span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**Fehler \_ WinHTTP-fehlerhaftes \_ \_ \_ autoproxyskript \_**</span><span class="sxs-lookup"><span data-stu-id="cdb89-113"><span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**ERROR\_WINHTTP\_BAD\_AUTO\_PROXY\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-114">12166</span><span class="sxs-lookup"><span data-stu-id="cdb89-114">12166</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-115">Fehler beim Ausführen des Skriptcodes in der PAC-Datei (Proxy Auto-Configuration).</span><span class="sxs-lookup"><span data-stu-id="cdb89-115">An error occurred executing the script code in the Proxy Auto-Configuration (PAC) file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-116"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**Fehler \_ WinHTTP \_ kann \_ \_ nach dem \_ Öffnen nicht aufgerufen werden.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-116"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_AFTER\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-117">12103</span><span class="sxs-lookup"><span data-stu-id="cdb89-117">12103</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-118">Wird vom [**HttpRequest**](winhttprequest.md) -Objekt zurückgegeben, wenn eine angegebene Option nicht angefordert werden kann, nachdem die [**Open**](iwinhttprequest-open.md) -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="cdb89-118">Returned by the [**HttpRequest**](winhttprequest.md) object if a specified option cannot be requested after the [**Open**](iwinhttprequest-open.md) method has been called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-119"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**Fehler \_ WinHTTP \_ kann \_ \_ nach dem \_ Senden nicht aufgerufen werden.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-119"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_AFTER\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-120">12102</span><span class="sxs-lookup"><span data-stu-id="cdb89-120">12102</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-121">Wird vom [**HttpRequest**](winhttprequest.md) -Objekt zurückgegeben, wenn ein angeforderter Vorgang nach dem Aufrufen der [**Send**](iwinhttprequest-send.md) -Methode nicht ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cdb89-121">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed after calling the [**Send**](iwinhttprequest-send.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-122"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**Fehler \_ WinHTTP \_ kann \_ nicht \_ vor dem \_ Öffnen aufgerufen werden**</span><span class="sxs-lookup"><span data-stu-id="cdb89-122"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_BEFORE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-123">12100</span><span class="sxs-lookup"><span data-stu-id="cdb89-123">12100</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-124">Wird vom [**HttpRequest**](winhttprequest.md) -Objekt zurückgegeben, wenn ein angeforderter Vorgang vor dem Aufrufen der [**Open**](iwinhttprequest-open.md) -Methode nicht ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cdb89-124">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed before calling the [**Open**](iwinhttprequest-open.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-125"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**Fehler \_ WinHTTP \_ kann \_ nicht \_ vor dem \_ senden aufgerufen werden**</span><span class="sxs-lookup"><span data-stu-id="cdb89-125"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_BEFORE\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-126">12101</span><span class="sxs-lookup"><span data-stu-id="cdb89-126">12101</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-127">Wird vom [**HttpRequest**](winhttprequest.md) -Objekt zurückgegeben, wenn ein angeforderter Vorgang vor dem Aufrufen der [**Send**](iwinhttprequest-send.md) -Methode nicht ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cdb89-127">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed before calling the [**Send**](iwinhttprequest-send.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-128"><span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**Fehler beim \_ \_ Herstellen einer Verbindung mit WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="cdb89-128"><span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**ERROR\_WINHTTP\_CANNOT\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-129">12029</span><span class="sxs-lookup"><span data-stu-id="cdb89-129">12029</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-130">Wird zurückgegeben, wenn die Verbindung zum Server fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="cdb89-130">Returned if connection to the server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-131"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**Fehler beim \_ WinHTTP- \_ Client Authentifizierungs \_ \_ Zertifikat. \_**</span><span class="sxs-lookup"><span data-stu-id="cdb89-131"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cdb89-132">Der Server erfordert eine SSL-Client Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="cdb89-132">The server requires SSL client Authentication.</span></span> <span data-ttu-id="cdb89-133">Die Anwendung ruft die Liste der Zertifikat Aussteller durch Aufrufen von [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) mit der Option **WinHTTP- \_ Option \_ Client \_ Zertifikat \_ Aussteller \_ Liste** ab.</span><span class="sxs-lookup"><span data-stu-id="cdb89-133">The application retrieves the list of certificate issuers by calling [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span> <span data-ttu-id="cdb89-134">Weitere Informationen finden Sie in der Option **WinHTTP- \_ Option \_ Client \_ Zertifikat \_ Aussteller \_ Liste** .</span><span class="sxs-lookup"><span data-stu-id="cdb89-134">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>

<span data-ttu-id="cdb89-135">Wenn der Server das Client Zertifikat anfordert, jedoch nicht erforderlich ist, kann die Anwendung [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) alternativ mit der **\_ Option \_ Client \_ CERT- \_ Kontext Option WinHTTP-Option** aufruft.</span><span class="sxs-lookup"><span data-stu-id="cdb89-135">If the server requests the client certificate, but does not require it, the application can alternately call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="cdb89-136">In diesem Fall gibt die Anwendung das WinHTTP- \_ \_ Kontext Makro "No Client \_ CERT" \_ im *lpBuffer* -Parameter von " **WinHttpSetOption**" an.</span><span class="sxs-lookup"><span data-stu-id="cdb89-136">In this case, the application specifies the WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT macro in the *lpBuffer* parameter of **WinHttpSetOption**.</span></span> <span data-ttu-id="cdb89-137">Weitere Informationen finden Sie unter der **WinHTTP- \_ Option \_ Client CERT- \_ \_ Kontext** Option.</span><span class="sxs-lookup"><span data-stu-id="cdb89-137">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>

<span data-ttu-id="cdb89-138">**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieser Fehler wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cdb89-138">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-139"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**Fehler \_ WinHTTP \_ Client \_ CERT \_ No \_ Access \_ private \_ Key**</span><span class="sxs-lookup"><span data-stu-id="cdb89-139"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**ERROR\_WINHTTP\_CLIENT\_CERT\_NO\_ACCESS\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cdb89-140">Die Anwendung verfügt nicht über die erforderlichen Berechtigungen für den Zugriff auf den privaten Schlüssel, der dem Client Zertifikat zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cdb89-140">The application does not have the required privileges to access the private key associated with the client certificate.</span></span>

<span data-ttu-id="cdb89-141">**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieser Fehler wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cdb89-141">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-142"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**Fehler \_ WinHTTP \_ Client \_ CERT \_ kein \_ privater \_ Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="cdb89-142"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**ERROR\_WINHTTP\_CLIENT\_CERT\_NO\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cdb89-143">Dem Kontext für das SSL-Client Zertifikat ist kein privater Schlüssel zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cdb89-143">The context for the SSL client certificate does not have a private key associated with it.</span></span> <span data-ttu-id="cdb89-144">Das Client Zertifikat wurde möglicherweise ohne den privaten Schlüssel auf den Computer importiert.</span><span class="sxs-lookup"><span data-stu-id="cdb89-144">The client certificate may have been imported to the computer without the private key.</span></span>

<span data-ttu-id="cdb89-145">**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieser Fehler wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cdb89-145">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-146"><span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**Fehler bei WinHTTP-segmentierter \_ \_ \_ Codierungs \_ Header \_ Größe. \_ Überlauf**</span><span class="sxs-lookup"><span data-stu-id="cdb89-146"><span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**ERROR\_WINHTTP\_CHUNKED\_ENCODING\_HEADER\_SIZE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-147">12183</span><span class="sxs-lookup"><span data-stu-id="cdb89-147">12183</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-148">Wird von [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) zurückgegeben, wenn beim Analysieren der segmentierten Codierung eine Überlauf Bedingung auftritt.</span><span class="sxs-lookup"><span data-stu-id="cdb89-148">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when an overflow condition is encountered in the course of parsing chunked encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-149"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**Fehler beim \_ WinHTTP- \_ Client Authentifizierungs \_ \_ Zertifikat. \_**</span><span class="sxs-lookup"><span data-stu-id="cdb89-149"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-150">12044</span><span class="sxs-lookup"><span data-stu-id="cdb89-150">12044</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-151">Wird von [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) zurückgegeben, wenn der Server die Client Authentifizierung anfordert.</span><span class="sxs-lookup"><span data-stu-id="cdb89-151">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when the server requests client authentication.</span></span>

<span data-ttu-id="cdb89-152">**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieser Fehler wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cdb89-152">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-153"><span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**Fehler beim \_ WinHTTP- \_ Verbindungs \_ Fehler.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-153"><span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**ERROR\_WINHTTP\_CONNECTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-154">12030</span><span class="sxs-lookup"><span data-stu-id="cdb89-154">12030</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-155">Die Verbindung mit dem Server wurde zurückgesetzt oder beendet, oder es wurde ein nicht kompatibles SSL-Protokoll gefunden.</span><span class="sxs-lookup"><span data-stu-id="cdb89-155">The connection with the server has been reset or terminated, or an incompatible SSL protocol was encountered.</span></span> <span data-ttu-id="cdb89-156">Beispielsweise unterstützt die WinHTTP-Version 5,1 nicht SSL2 verwendet, es sei denn, der Client aktiviert Sie ausdrücklich.</span><span class="sxs-lookup"><span data-stu-id="cdb89-156">For example, WinHTTP version 5.1 does not support SSL2 unless the client specifically enables it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-157"><span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**\_WinHTTP-Fehler \_ Header ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-157"><span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**ERROR\_WINHTTP\_HEADER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-158">12155</span><span class="sxs-lookup"><span data-stu-id="cdb89-158">12155</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-159">Veralteten nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="cdb89-159">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-160"><span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**Fehler bei \_ WinHTTP- \_ Header \_ Anzahl \_ überschritten.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-160"><span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**ERROR\_WINHTTP\_HEADER\_COUNT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-161">12181</span><span class="sxs-lookup"><span data-stu-id="cdb89-161">12181</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-162">Wird von [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) zurückgegeben, wenn eine größere Anzahl von Headern in einer Antwort vorhanden war, als WinHTTP empfangen konnte.</span><span class="sxs-lookup"><span data-stu-id="cdb89-162">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when a larger number of headers were present in a response than WinHTTP could receive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-163"><span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**Fehler beim \_ WinHTTP- \_ Header \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-163"><span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**ERROR\_WINHTTP\_HEADER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-164">12150</span><span class="sxs-lookup"><span data-stu-id="cdb89-164">12150</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-165">Der angeforderte Header wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="cdb89-165">The requested header cannot be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-166"><span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**Fehler bei \_ WinHTTP- \_ Header \_ Größen \_ Überlauf.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-166"><span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**ERROR\_WINHTTP\_HEADER\_SIZE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-167">12182</span><span class="sxs-lookup"><span data-stu-id="cdb89-167">12182</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-168">Wird von [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) zurückgegeben, wenn die empfangene Header Größe den Grenzwert für das Anforderungs handle überschreitet.</span><span class="sxs-lookup"><span data-stu-id="cdb89-168">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when the size of headers received exceeds the limit for the request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-169"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**Fehler \_ WinHTTP- \_ fehlerhafter \_ handle- \_ Zustand**</span><span class="sxs-lookup"><span data-stu-id="cdb89-169"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**ERROR\_WINHTTP\_INCORRECT\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-170">12019</span><span class="sxs-lookup"><span data-stu-id="cdb89-170">12019</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-171">Der angeforderte Vorgang kann nicht ausgeführt werden, da das angegebene Handle nicht den richtigen Status aufweist.</span><span class="sxs-lookup"><span data-stu-id="cdb89-171">The requested operation cannot be carried out because the handle supplied is not in the correct state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-172"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**\_fehlerhafter WinHTTP- \_ \_ handle- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="cdb89-172"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**ERROR\_WINHTTP\_INCORRECT\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-173">12018</span><span class="sxs-lookup"><span data-stu-id="cdb89-173">12018</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-174">Der angegebene Handlertyp ist für diesen Vorgang falsch.</span><span class="sxs-lookup"><span data-stu-id="cdb89-174">The type of handle supplied is incorrect for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-175"><span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**Fehler bei \_ WinHTTP- \_ interner \_ Fehler.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-175"><span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**ERROR\_WINHTTP\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-176">12004</span><span class="sxs-lookup"><span data-stu-id="cdb89-176">12004</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-177">Ein interner Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="cdb89-177">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-178"><span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**Fehler bei \_ WinHTTP- \_ \_ Option ungültig**</span><span class="sxs-lookup"><span data-stu-id="cdb89-178"><span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**ERROR\_WINHTTP\_INVALID\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-179">12009</span><span class="sxs-lookup"><span data-stu-id="cdb89-179">12009</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-180">Eine Anforderung an " [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) " oder " [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) " hat einen ungültigen Optionswert angegeben.</span><span class="sxs-lookup"><span data-stu-id="cdb89-180">A request to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) or [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) specified an invalid option value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-181"><span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**Fehler bei \_ WinHTTP- \_ \_ Abfrage \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="cdb89-181"><span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**ERROR\_WINHTTP\_INVALID\_QUERY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-182">12154</span><span class="sxs-lookup"><span data-stu-id="cdb89-182">12154</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-183">Veralteten nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="cdb89-183">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-184"><span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**Fehler \_ WinHTTP \_ - \_ Antwort auf ungültige Server \_**</span><span class="sxs-lookup"><span data-stu-id="cdb89-184"><span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**ERROR\_WINHTTP\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-185">12152</span><span class="sxs-lookup"><span data-stu-id="cdb89-185">12152</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-186">Die Serverantwort kann nicht analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="cdb89-186">The server response cannot be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-187"><span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**Fehler \_ WinHTTP- \_ ungültige \_ URL**</span><span class="sxs-lookup"><span data-stu-id="cdb89-187"><span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**ERROR\_WINHTTP\_INVALID\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-188">12005</span><span class="sxs-lookup"><span data-stu-id="cdb89-188">12005</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-189">Die URL ist nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="cdb89-189">The URL is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-190"><span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**Fehler beim \_ WinHTTP- \_ Anmelde \_ Fehler.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-190"><span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**ERROR\_WINHTTP\_LOGIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-191">12015</span><span class="sxs-lookup"><span data-stu-id="cdb89-191">12015</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-192">Der Anmeldeversuch ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="cdb89-192">The login attempt failed.</span></span> <span data-ttu-id="cdb89-193">Wenn dieser Fehler auftritt, sollte das Anforderungs Handle mit [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="cdb89-193">When this error is encountered, the request handle should be closed with [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle).</span></span> <span data-ttu-id="cdb89-194">Ein neues Anforderungs Handle muss erstellt werden, bevor die Funktion erneut versucht wird, die den Fehler ursprünglich erzeugt hat.</span><span class="sxs-lookup"><span data-stu-id="cdb89-194">A new request handle must be created before retrying the function that originally produced this error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-195"><span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**\_WinHTTP-Fehler \_ Name wurde \_ nicht \_ aufgelöst.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-195"><span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**ERROR\_WINHTTP\_NAME\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-196">12007</span><span class="sxs-lookup"><span data-stu-id="cdb89-196">12007</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-197">Der Servername kann nicht aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="cdb89-197">The server name cannot be resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-198"><span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**Fehler \_ WinHTTP wurde \_ nicht \_ initialisiert.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-198"><span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**ERROR\_WINHTTP\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-199">12172</span><span class="sxs-lookup"><span data-stu-id="cdb89-199">12172</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-200">Veralteten nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="cdb89-200">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-201"><span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**Fehler beim \_ WinHTTP- \_ Vorgang. \_**</span><span class="sxs-lookup"><span data-stu-id="cdb89-201"><span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**ERROR\_WINHTTP\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-202">12017</span><span class="sxs-lookup"><span data-stu-id="cdb89-202">12017</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-203">Der Vorgang wurde abgebrochen, in der Regel, weil das Handle, für das die Anforderung ausgeführt wurde, vor dem Abschluss des Vorgangs geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="cdb89-203">The operation was canceled, usually because the handle on which the request was operating was closed before the operation completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-204"><span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**Fehler bei \_ WinHTTP- \_ Option \_ nicht \_ feststellbar.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-204"><span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**ERROR\_WINHTTP\_OPTION\_NOT\_SETTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-205">12011</span><span class="sxs-lookup"><span data-stu-id="cdb89-205">12011</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-206">Die angeforderte Option kann nicht festgelegt werden, sondern nur abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="cdb89-206">The requested option cannot be set, only queried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-207"><span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**Fehler bei \_ WinHTTP- \_ \_ über \_ griffen**</span><span class="sxs-lookup"><span data-stu-id="cdb89-207"><span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**ERROR\_WINHTTP\_OUT\_OF\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-208">12001</span><span class="sxs-lookup"><span data-stu-id="cdb89-208">12001</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-209">Veralteten nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="cdb89-209">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-210"><span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**Fehler bei \_ WinHTTP- \_ Umleitung. \_**</span><span class="sxs-lookup"><span data-stu-id="cdb89-210"><span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**ERROR\_WINHTTP\_REDIRECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-211">12156</span><span class="sxs-lookup"><span data-stu-id="cdb89-211">12156</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-212">Die Umleitung ist fehlgeschlagen, da entweder das Schema geändert wurde oder alle Versuche zum Umleiten fehlgeschlagen sind (standardmäßig fünf Versuche).</span><span class="sxs-lookup"><span data-stu-id="cdb89-212">The redirection failed because either the scheme changed or all attempts made to redirect failed (default is five attempts).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-213"><span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**Fehler bei \_ WinHTTP- \_ Anforderung zum erneuten senden. \_**</span><span class="sxs-lookup"><span data-stu-id="cdb89-213"><span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**ERROR\_WINHTTP\_RESEND\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-214">12032</span><span class="sxs-lookup"><span data-stu-id="cdb89-214">12032</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-215">Die WinHTTP-Funktion konnte nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cdb89-215">The WinHTTP function failed.</span></span> <span data-ttu-id="cdb89-216">Die gewünschte Funktion kann auf demselben Anforderungs handle wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="cdb89-216">The desired function can be retried on the same request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-217"><span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**Fehler beim \_ WinHTTP- \_ Antwort- \_ \_ Überlauf Überlauf.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-217"><span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**ERROR\_WINHTTP\_RESPONSE\_DRAIN\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-218">12184</span><span class="sxs-lookup"><span data-stu-id="cdb89-218">12184</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-219">Wird zurückgegeben, wenn eine eingehende Antwort eine interne WinHTTP-Größenbeschränkung überschreitet.</span><span class="sxs-lookup"><span data-stu-id="cdb89-219">Returned when an incoming response exceeds an internal WinHTTP size limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-220"><span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**Fehler beim \_ Ausführen des WinHTTP- \_ Skripts. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cdb89-220"><span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**ERROR\_WINHTTP\_SCRIPT\_EXECUTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-221">12177</span><span class="sxs-lookup"><span data-stu-id="cdb89-221">12177</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-222">Beim Ausführen eines Skripts ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="cdb89-222">An error was encountered while executing a script.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-223"><span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**Fehler " \_ WinHTTP \_ Secure \_ CERT CN" ist \_ \_ ungültig.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-223"><span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-224">12038</span><span class="sxs-lookup"><span data-stu-id="cdb89-224">12038</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-225">Wird zurückgegeben, wenn der CN-Name des Zertifikats nicht mit dem übergebenen Wert übereinstimmt (entspricht dem Fehler " **CERT \_ E \_ CN \_ No \_ Match** ").</span><span class="sxs-lookup"><span data-stu-id="cdb89-225">Returned when a certificate CN name does not match the passed value (equivalent to a **CERT\_E\_CN\_NO\_MATCH** error).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-226"><span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**Fehler " \_ WinHTTP \_ Secure \_ CERT Date" ist \_ \_ ungültig.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-226"><span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-227">12037</span><span class="sxs-lookup"><span data-stu-id="cdb89-227">12037</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-228">Gibt an, dass ein erforderliches Zertifikat nicht innerhalb seines Gültigkeits Zeitraums liegt, wenn die aktuelle Systemuhr oder der Zeitstempel in der signierten Datei überprüft wird, oder dass die Gültigkeits Zeiträume der Zertifizierungs Kette nicht ordnungsgemäß geschachtelt werden (äquivalent zu einem **Zertifikat \_ e \_** oder einem **CERT \_ e \_ validityperiodnist** -Fehler).</span><span class="sxs-lookup"><span data-stu-id="cdb89-228">Indicates that a required certificate is not within its validity period when verifying against the current system clock or the timestamp in the signed file, or that the validity periods of the certification chain do not nest correctly (equivalent to a **CERT\_E\_EXPIRED** or a **CERT\_E\_VALIDITYPERIODNESTING** error).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-229"><span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**Fehler bei \_ WinHTTP \_ Secure \_ CERT \_ Rev \_ .**</span><span class="sxs-lookup"><span data-stu-id="cdb89-229"><span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_REV\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-230">12057</span><span class="sxs-lookup"><span data-stu-id="cdb89-230">12057</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-231">Gibt an, dass die Sperrung nicht geprüft werden kann, weil der Sperr Server offline war (äquivalent zur Sperre von **crypt \_ E, \_ \_ Offline**).</span><span class="sxs-lookup"><span data-stu-id="cdb89-231">Indicates that revocation cannot be checked because the revocation server was offline (equivalent to **CRYPT\_E\_REVOCATION\_OFFLINE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-232"><span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**Fehler " \_ WinHTTP \_ Secure \_ CERT \_ " wurde gesperrt.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-232"><span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-233">12170</span><span class="sxs-lookup"><span data-stu-id="cdb89-233">12170</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-234">Gibt an, dass ein Zertifikat widerrufen wurde (äquivalent zu **crypt \_ E \_ widerrufen**).</span><span class="sxs-lookup"><span data-stu-id="cdb89-234">Indicates that a certificate has been revoked (equivalent to **CRYPT\_E\_REVOKED**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-235"><span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**Fehler bei \_ WinHTTP \_ Secure \_ CERT \_ falsche \_ Verwendung**</span><span class="sxs-lookup"><span data-stu-id="cdb89-235"><span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_WRONG\_USAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-236">12179</span><span class="sxs-lookup"><span data-stu-id="cdb89-236">12179</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-237">Gibt an, dass ein Zertifikat für die angeforderte Verwendung ungültig ist (äquivalent zur **\_ \_ falschen \_ Verwendung von CERT E**).</span><span class="sxs-lookup"><span data-stu-id="cdb89-237">Indicates that a certificate is not valid for the requested usage (equivalent to **CERT\_E\_WRONG\_USAGE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-238"><span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**Fehler bei WinHTTP-Fehler des \_ \_ sicheren \_ Kanals \_**</span><span class="sxs-lookup"><span data-stu-id="cdb89-238"><span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**ERROR\_WINHTTP\_SECURE\_CHANNEL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-239">12157</span><span class="sxs-lookup"><span data-stu-id="cdb89-239">12157</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-240">Gibt an, dass ein Fehler mit einem sicheren Kanal aufgetreten ist (äquivalent zu Fehlercodes, die mit "sec \_ E \_ " beginnen, und "s \_ I \_ ", die in der Header Datei "Winerror. h" aufgeführt sind).</span><span class="sxs-lookup"><span data-stu-id="cdb89-240">Indicates that an error occurred having to do with a secure channel (equivalent to error codes that begin with "SEC\_E\_" and "SEC\_I\_" listed in the "winerror.h" header file).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-241"><span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**Fehler beim \_ WinHTTP- \_ sicheren \_ Fehler.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-241"><span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**ERROR\_WINHTTP\_SECURE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-242">12175</span><span class="sxs-lookup"><span data-stu-id="cdb89-242">12175</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-243">Es wurde mindestens ein Fehler im vom Server gesendeten Secure Sockets Layer (SSL)-Zertifikat gefunden.</span><span class="sxs-lookup"><span data-stu-id="cdb89-243">One or more errors were found in the Secure Sockets Layer (SSL) certificate sent by the server.</span></span> <span data-ttu-id="cdb89-244">Um zu ermitteln, welche Art von Fehler aufgetreten ist, überprüfen Sie, ob in einer Status Rückruffunktion eine Benachrichtigung über den [**WinHTTP- \_ Rückruf \_ Status \_ sicherer \_ Fehler**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) vorliegt.</span><span class="sxs-lookup"><span data-stu-id="cdb89-244">To determine what type of error was encountered, check for a [**WINHTTP\_CALLBACK\_STATUS\_SECURE\_FAILURE**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) notification in a status callback function.</span></span> <span data-ttu-id="cdb89-245">Weitere Informationen finden Sie unter [**WinHTTP- \_ Status \_ Rückruf**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).</span><span class="sxs-lookup"><span data-stu-id="cdb89-245">For more information, see [**WINHTTP\_STATUS\_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-246"><span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**Fehler \_ WinHTTP- \_ sichere \_ ungültige \_ Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="cdb89-246"><span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**ERROR\_WINHTTP\_SECURE\_INVALID\_CA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-247">12045</span><span class="sxs-lookup"><span data-stu-id="cdb89-247">12045</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-248">Gibt an, dass eine Zertifikat Kette verarbeitet, aber in einem Stamm Zertifikat beendet wurde, das vom Vertrauens Anbieter nicht als vertrauenswürdig eingestuft wird (äquivalent zu **CERT \_ E \_ untrustdroot**).</span><span class="sxs-lookup"><span data-stu-id="cdb89-248">Indicates that a certificate chain was processed, but terminated in a root certificate that is not trusted by the trust provider (equivalent to **CERT\_E\_UNTRUSTEDROOT**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-249"><span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**Fehler \_ WinHTTP \_ Secure \_ ungültiges \_ Zertifikat**</span><span class="sxs-lookup"><span data-stu-id="cdb89-249"><span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**ERROR\_WINHTTP\_SECURE\_INVALID\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-250">12169</span><span class="sxs-lookup"><span data-stu-id="cdb89-250">12169</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-251">Gibt an, dass ein Zertifikat ungültig ist (äquivalent zu Fehlern wie " **CERT \_ e \_ Role**", " **CERT e \_ \_ pathlenconst**", " **CERT \_ e \_ Critical**", " **CERT \_ e \_ Purpose**", " **CERT \_ e \_ issuerchaining**", " **CERT \_ e \_ falsch** formatiert" und " **CERT \_ e \_ Chaining**</span><span class="sxs-lookup"><span data-stu-id="cdb89-251">Indicates that a certificate is invalid (equivalent to errors such as **CERT\_E\_ROLE**, **CERT\_E\_PATHLENCONST**, **CERT\_E\_CRITICAL**, **CERT\_E\_PURPOSE**, **CERT\_E\_ISSUERCHAINING**, **CERT\_E\_MALFORMED** and **CERT\_E\_CHAINING**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-252"><span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**Fehler beim Herunterfahren von \_ WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="cdb89-252"><span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**ERROR\_WINHTTP\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-253">12012</span><span class="sxs-lookup"><span data-stu-id="cdb89-253">12012</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-254">Die Unterstützung der WinHTTP-Funktion wird heruntergefahren oder entladen.</span><span class="sxs-lookup"><span data-stu-id="cdb89-254">The WinHTTP function support is being shut down or unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-255"><span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**Fehler beim \_ WinHTTP- \_ Timeout.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-255"><span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**ERROR\_WINHTTP\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-256">12002</span><span class="sxs-lookup"><span data-stu-id="cdb89-256">12002</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-257">Timeout für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cdb89-257">The request has timed out.</span></span>

<span data-ttu-id="cdb89-258">Dieser Fehler kann aufgrund eines TCP/IP-Timeout Verhaltens zurückgegeben werden, unabhängig davon, welche Timeout Werte in Windows HTTP-Diensten festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="cdb89-258">This error can be returned as a result of TCP/IP time-out behavior, regardless of time-out values set in Windows HTTP Services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-259"><span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**Fehler \_ WinHTTP \_ kann \_ \_ Skript nicht herunterladen \_**</span><span class="sxs-lookup"><span data-stu-id="cdb89-259"><span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**ERROR\_WINHTTP\_UNABLE\_TO\_DOWNLOAD\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-260">12167</span><span class="sxs-lookup"><span data-stu-id="cdb89-260">12167</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-261">Die PAC-Datei kann nicht heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="cdb89-261">The PAC file cannot be downloaded.</span></span> <span data-ttu-id="cdb89-262">Beispielsweise ist der Server, auf den die PAC-URL verweist, möglicherweise nicht erreichbar, oder der Server hat die Antwort "404 nicht gefunden" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cdb89-262">For example, the server referenced by the PAC URL may not have been reachable, or the server returned a 404 NOT FOUND response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-263"><span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**Fehler bei \_ WinHTTP- \_ unbehandeltem \_ \_ Skripttyp**</span><span class="sxs-lookup"><span data-stu-id="cdb89-263"><span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**ERROR\_WINHTTP\_UNHANDLED\_SCRIPT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-264">12176</span><span class="sxs-lookup"><span data-stu-id="cdb89-264">12176</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-265">Der Skripttyp wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cdb89-265">The script type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-266"><span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**Fehler beim nicht \_ erkannten WinHTTP- \_ \_ Schema**</span><span class="sxs-lookup"><span data-stu-id="cdb89-266"><span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**ERROR\_WINHTTP\_UNRECOGNIZED\_SCHEME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb89-267">12006</span><span class="sxs-lookup"><span data-stu-id="cdb89-267">12006</span></span>
</dt> <dt>



<span data-ttu-id="cdb89-268">Die URL hat ein anderes Schema als "http:" oder "https:" angegeben.</span><span class="sxs-lookup"><span data-stu-id="cdb89-268">The URL specified a scheme other than "http:" or "https:".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-269"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="cdb89-269"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cdb89-270">Es war nicht genügend Arbeitsspeicher verfügbar, um den angeforderten Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="cdb89-270">Not enough memory was available to complete the requested operation.</span></span>

<span data-ttu-id="cdb89-271">**Header:** In "Winerror. h" deklariert</span><span class="sxs-lookup"><span data-stu-id="cdb89-271">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-272"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**Fehler \_ beim \_ Puffer.**</span><span class="sxs-lookup"><span data-stu-id="cdb89-272"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cdb89-273">Die Größe (in Bytes) des Puffers, der für eine Funktion angegeben wurde, war nicht ausreichend, um die zurückgegebenen Daten zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="cdb89-273">The size, in bytes, of the buffer supplied to a function was insufficient to contain the returned data.</span></span> <span data-ttu-id="cdb89-274">Weitere Informationen finden Sie in der jeweiligen Funktion.</span><span class="sxs-lookup"><span data-stu-id="cdb89-274">For more information, see the specific function.</span></span>

<span data-ttu-id="cdb89-275">**Header:** In "Winerror. h" deklariert</span><span class="sxs-lookup"><span data-stu-id="cdb89-275">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-276"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**Fehler bei \_ ungültigem \_ handle**</span><span class="sxs-lookup"><span data-stu-id="cdb89-276"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cdb89-277">Das an die API (Application Programming Interface) über gegebene Handle wurde entweder ungültig oder wurde geschlossen.</span><span class="sxs-lookup"><span data-stu-id="cdb89-277">The handle passed to the application programming interface (API) has been either invalidated or closed.</span></span>

<span data-ttu-id="cdb89-278">**Header:** In "Winerror. h" deklariert</span><span class="sxs-lookup"><span data-stu-id="cdb89-278">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-279"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**Fehler \_ keine \_ weiteren \_ Dateien**</span><span class="sxs-lookup"><span data-stu-id="cdb89-279"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cdb89-280">Es wurden keine weiteren Dateien gefunden.</span><span class="sxs-lookup"><span data-stu-id="cdb89-280">No more files have been found.</span></span>

<span data-ttu-id="cdb89-281">**Header:** In "Winerror. h" deklariert</span><span class="sxs-lookup"><span data-stu-id="cdb89-281">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-282"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**Fehler \_ keine \_ weiteren \_ Elemente**</span><span class="sxs-lookup"><span data-stu-id="cdb89-282"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cdb89-283">Es wurden keine weiteren Elemente gefunden.</span><span class="sxs-lookup"><span data-stu-id="cdb89-283">No more items have been found.</span></span>

<span data-ttu-id="cdb89-284">**Header:** In "Winerror. h" deklariert</span><span class="sxs-lookup"><span data-stu-id="cdb89-284">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdb89-285"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**Fehler \_ nicht \_ unterstützt**</span><span class="sxs-lookup"><span data-stu-id="cdb89-285"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cdb89-286">Der erforderliche Protokollstapel ist nicht geladen, und die Anwendung kann Winsock nicht starten.</span><span class="sxs-lookup"><span data-stu-id="cdb89-286">The required protocol stack is not loaded and the application cannot start WinSock.</span></span>

<span data-ttu-id="cdb89-287">**Header:** In "Winerror. h" deklariert</span><span class="sxs-lookup"><span data-stu-id="cdb89-287">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cdb89-288">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdb89-288">Remarks</span></span>

<span data-ttu-id="cdb89-289">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Startseite.</span><span class="sxs-lookup"><span data-stu-id="cdb89-289">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdb89-290">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdb89-290">Requirements</span></span>



| <span data-ttu-id="cdb89-291">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cdb89-291">Requirement</span></span> | <span data-ttu-id="cdb89-292">Wert</span><span class="sxs-lookup"><span data-stu-id="cdb89-292">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb89-293">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cdb89-293">Minimum supported client</span></span><br/> | <span data-ttu-id="cdb89-294">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cdb89-294">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="cdb89-295">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cdb89-295">Minimum supported server</span></span><br/> | <span data-ttu-id="cdb89-296">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cdb89-296">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="cdb89-297">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="cdb89-297">Redistributable</span></span><br/>          | <span data-ttu-id="cdb89-298">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="cdb89-298">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="cdb89-299">Header</span><span class="sxs-lookup"><span data-stu-id="cdb89-299">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdb89-300"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdb89-300"><dt>Winhttp.h</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="cdb89-301">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdb89-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdb89-302">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="cdb89-302">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

