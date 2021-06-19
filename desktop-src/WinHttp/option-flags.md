---
Description: Die folgenden Optionsflags werden von WinHttpQueryOption und WinHttpSetOption unterstützt.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Optionsflags (Winhttp.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 25049ee11c59c6b320b794c07bd65e5ec9b930c9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395415"
---
# <a name="option-flags"></a><span data-ttu-id="941fe-103">Optionsflags</span><span class="sxs-lookup"><span data-stu-id="941fe-103">Option Flags</span></span>

<span data-ttu-id="941fe-104">Die folgenden Optionsflags werden von [**WinHttpQueryOption und**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) [**WinHttpSetOption unterstützt.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)</span><span class="sxs-lookup"><span data-stu-id="941fe-104">The following option flags are supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span>

<dl> <dt>

<span data-ttu-id="941fe-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**\_WINHTTP-OPTION \_ \_ GARANTIERTE NICHT \_ \_ BLOCKIERENDE RÜCKRUFE**</span><span class="sxs-lookup"><span data-stu-id="941fe-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-106">Der Standardwert lautet FALSE.</span><span class="sxs-lookup"><span data-stu-id="941fe-106">The default is FALSE.</span></span> <span data-ttu-id="941fe-107">Wenn der Status auf TRUE festgelegt ist, garantiert WinHTTP den Fortschritt nicht, wenn Statusrückrufe von der Clientanwendung blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-107">If set to TRUE, WinHTTP does not guarantee progress if status callbacks are blocked by the client application.</span></span>

<span data-ttu-id="941fe-108">Die Clientanwendung muss besonders darauf achten, minimale Vorgänge innerhalb des Rückrufs ohne Blockierung durchzuführen, so schnell wie möglich zurückzukehren und insbesondere nicht auf nachfolgende WinHTTP-Aufrufe zu warten.</span><span class="sxs-lookup"><span data-stu-id="941fe-108">The client application must take special care to perform minimal operations within the callback without blocking, returning as quickly as possible, and in particular must not wait for any subsequent WinHTTP calls.</span></span> <span data-ttu-id="941fe-109">Wenn sie diese Richtlinien nicht einfängt, ist es wahrscheinlich, dass es negative Auswirkungen auf die Leistung oder eine potenzielle Anwendung gibt, die nicht mehr funktioniert.</span><span class="sxs-lookup"><span data-stu-id="941fe-109">If it does not follow these guidelines, there is likely to be a negative performance impact or a potential application hang.</span></span> <span data-ttu-id="941fe-110">Wenn diese Option auf die vorgeschriebene Weise verwendet wird, kann sie die Leistung verbessern.</span><span class="sxs-lookup"><span data-stu-id="941fe-110">If used in the prescribed manner, this option may improve performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**RICHTLINIE FÜR \_ DIE AUTOMATISCHE ANMELDUNG DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-112">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Richtlinie für automatische [Anmeldung](authentication-in-winhttp.md) mit einem der folgenden Werte angibt.</span><span class="sxs-lookup"><span data-stu-id="941fe-112">Sets an unsigned long integer value that specifies the [Automatic Logon Policy](authentication-in-winhttp.md) with one of the following values.</span></span>

| <span data-ttu-id="941fe-113">Begriff</span><span class="sxs-lookup"><span data-stu-id="941fe-113">Term</span></span> | <span data-ttu-id="941fe-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="941fe-114">Description</span></span> |
|-|-|
| <span data-ttu-id="941fe-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ HIGH</span><span class="sxs-lookup"><span data-stu-id="941fe-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH</span></span> | <span data-ttu-id="941fe-116">Standardanmeldeinformationen werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="941fe-116">Default credentials are not used.</span></span> <span data-ttu-id="941fe-117">Beachten Sie, dass dieses Flag nur wirksam wird, wenn Sie den Server mit dem tatsächlichen Computernamen angeben.</span><span class="sxs-lookup"><span data-stu-id="941fe-117">Note that this flag takes effect only if you specify the server by the actual machine name.</span></span> <span data-ttu-id="941fe-118">Sie wird nicht wirksam, wenn Sie den Server mit "localhost" oder IP-Adresse angeben.</span><span class="sxs-lookup"><span data-stu-id="941fe-118">It will not take effect, if you specify the server by "localhost" or IP address.</span></span> |
| <span data-ttu-id="941fe-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ LOW</span><span class="sxs-lookup"><span data-stu-id="941fe-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW</span></span> | <span data-ttu-id="941fe-120">Für alle Anforderungen wird eine authentifizierte Anmeldung mit den Standardanmeldeinformationen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="941fe-120">An authenticated log on using the default credentials is performed for all requests.</span></span> |
| <span data-ttu-id="941fe-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ MEDIUM</span><span class="sxs-lookup"><span data-stu-id="941fe-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM</span></span> | <span data-ttu-id="941fe-122">Eine authentifizierte Anmeldung mit den Standardanmeldeinformationen wird nur für Anforderungen im lokalen Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="941fe-122">An authenticated log on using the default credentials is performed only for requests on the local Intranet.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="941fe-123"><span id="WINHTTP_OPTION_BACKGROUND_CONNECTIONS"></span><span id="winhttp_option_background_connections"></span>**\_WINHTTP-OPTION \_ : \_ HINTERGRUNDVERBINDUNGEN**</span><span class="sxs-lookup"><span data-stu-id="941fe-123"><span id="WINHTTP_OPTION_BACKGROUND_CONNECTIONS"></span><span id="winhttp_option_background_connections"></span>**WINHTTP\_OPTION\_BACKGROUND\_CONNECTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="941fe-124">Wenn Sie diese Option für ein Sitzungshand handle festlegen, müssen Sie die Anzahl der Verbindungen übergeben, die Sie öffnen möchten.</span><span class="sxs-lookup"><span data-stu-id="941fe-124">When you set this option on a session handle, you must pass the number of connections you wish to open.</span></span> <span data-ttu-id="941fe-125">Anschließend öffnet WinHttp beim ersten Senden einer Anforderung eine Reihe von Verbindungen parallel, anstatt nur eine einzelne Verbindung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="941fe-125">Then, upon first sending a request, rather than opening only a single connection, WinHttp opens a number of connections in parallel.</span></span> <span data-ttu-id="941fe-126">Dies kann die Leistung nachfolgender Anforderungen an dasselbe Ziel verbessern, was nicht den Mehraufwand für die Verbindungseinrichtung mit sich bringen wird.</span><span class="sxs-lookup"><span data-stu-id="941fe-126">This can improve the performance of subsequent requests to the same destination, which won't have the overhead of connection establishment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-127"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**\_ \_ WINHTTP-OPTIONSRÜCKRUF**</span><span class="sxs-lookup"><span data-stu-id="941fe-127"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-128">Ruft den Zeiger auf den Rückruffunktionssatz mit [**WinHttpSetStatusCallback ab.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)</span><span class="sxs-lookup"><span data-stu-id="941fe-128">Retrieves the pointer to the callback function set with [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-129"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP \_ OPTION \_ CLIENT \_ CERT \_ CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="941fe-129"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-130">Legt den Clientzertifikatkontext fest.</span><span class="sxs-lookup"><span data-stu-id="941fe-130">Sets the client certificate context.</span></span> <span data-ttu-id="941fe-131">Wenn eine Anwendung [**DEN FEHLER \_ WINHTTP CLIENT \_ \_ AUTH \_ CERT \_ NEEDED**](error-messages.md)empfängt, muss sie [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) aufrufen, um ein Zertifikat zur Verfügung zu stellen, bevor die Anforderung erneut ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="941fe-131">If an application receives [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md), it must call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="941fe-132">Im Rahmen der Verarbeitung dieser Option ruft WinHttp [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) im vom Aufrufer bereitgestellten Zertifikatkontext auf, damit der Zertifikatkontext unabhängig vom Aufrufer freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="941fe-132">As a part of processing this option, WinHttp calls [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) on the caller-provided certificate context so that the certificate context can be independently released by the caller.</span></span>

> [!Note]
> <span data-ttu-id="941fe-133">Die Anwendung sollte nicht versuchen, den Zertifikatspeicher mit dem Flag CERT CLOSE STORE FORCE FLAG im Aufruf von \_ \_ \_ \_ [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) in dem Zertifikatspeicher zu schließen, aus dem der Zertifikatkontext abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="941fe-133">The application should not attempt to close the certificate store with the CERT\_CLOSE\_STORE\_FORCE\_FLAG flag in the call to [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) on the certificate store from which the certificate context was retrieved.</span></span> <span data-ttu-id="941fe-134">Es kann zu einer Zugriffsverletzung kommen.</span><span class="sxs-lookup"><span data-stu-id="941fe-134">An access violation may occur.</span></span>

<span data-ttu-id="941fe-135">Wenn der Server ein Clientzertifikat anfordert, [**gibt WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)oder [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) einen [**ERROR \_ WINHTTP CLIENT \_ \_ AUTH \_ CERT \_ NEEDED-Fehler**](error-messages.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="941fe-135">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md) error.</span></span> <span data-ttu-id="941fe-136">Wenn der Server das Zertifikat an fordert, es aber nicht erfordert, kann die Anwendung diese Option angeben, um anzugeben, dass er kein Zertifikat hat.</span><span class="sxs-lookup"><span data-stu-id="941fe-136">If the server requests the certificate but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="941fe-137">Der Server kann ein anderes Authentifizierungsschema auswählen oder anonymen Zugriff auf den Server zulassen.</span><span class="sxs-lookup"><span data-stu-id="941fe-137">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="941fe-138">Die Anwendung stellt das **WINHTTP \_ NO CLIENT \_ \_ CERT \_ CONTEXT-Makro** im *lpBuffer-Parameter* von [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) wie im folgenden Codebeispiel gezeigt zur Anwendung.</span><span class="sxs-lookup"><span data-stu-id="941fe-138">The application provides the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

<span data-ttu-id="941fe-139">Wenn der Server ein Clientzertifikat erfordert, kann er als Antwort den HTTP-Statuscode 403 senden.</span><span class="sxs-lookup"><span data-stu-id="941fe-139">If the server requires a client certificate, it may send a 403 HTTP status code in response.</span></span> <span data-ttu-id="941fe-140">Weitere Informationen finden Sie unter DER **OPTION WINHTTP \_ OPTION CLIENT \_ \_ CERT ISSUER \_ \_ LIST.**</span><span class="sxs-lookup"><span data-stu-id="941fe-140">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-141"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**\_WINHTTP-OPTION \_ \_ CLIENTZERTIFIKATAUSSTELLERLISTE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-141"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-142">Ruft eine [**SecPkgContext \_ IssuerListInfoEx-Struktur**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) ab, wenn der Fehler aus [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) oder [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) **ERROR \_ WINHTTP CLIENT \_ \_ AUTH \_ CERT NEEDED \_ lautet.**</span><span class="sxs-lookup"><span data-stu-id="941fe-142">Retrieves a [**SecPkgContext\_IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure when the error from [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) is **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="941fe-143">Die Ausstellerliste in der Struktur enthält eine Liste der zulässigen Zertifizierungsstellen (Certificate Authorities, CA) vom Server.</span><span class="sxs-lookup"><span data-stu-id="941fe-143">The issuer list in the structure contains a list of acceptable Certificate Authorities (CA) from the server.</span></span> <span data-ttu-id="941fe-144">Die Clientanwendung kann die Zertifizierungsstellenliste filtern, um das Clientzertifikat für die SSL-Authentifizierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="941fe-144">The client application can filter the CA list to retrieve the client certificate for SSL authentication.</span></span>

<span data-ttu-id="941fe-145">Alternativ kann die Anwendung [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit der OPTION **WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ CONTEXT** aufrufen, wenn der Server das Clientzertifikat an fordert, es aber nicht erfordert.</span><span class="sxs-lookup"><span data-stu-id="941fe-145">Alternately, if the server requests the client certificate, but does not require it, the application can call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="941fe-146">Weitere Informationen finden Sie unter DER **OPTION WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ CONTEXT.**</span><span class="sxs-lookup"><span data-stu-id="941fe-146">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-147"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**\_ \_ WINHTTP-OPTIONSCODEPAGE**</span><span class="sxs-lookup"><span data-stu-id="941fe-147"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-148">Legt die [*Codepage fest,*](glossary.md) die zum Verarbeiten der URL verwendet wird (d. h. Abfragezeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="941fe-148">Sets the [*code page*](glossary.md) that is used to process the URL (that is, query string).</span></span> <span data-ttu-id="941fe-149">Der Standardwert ist UTF8.</span><span class="sxs-lookup"><span data-stu-id="941fe-149">The default is UTF8.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-150"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_WINHTTP-OPTION: \_ KONFIGURIEREN DER \_ \_ PASSPORT-AUTHENTIFIZIERUNG**</span><span class="sxs-lookup"><span data-stu-id="941fe-150"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-151">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, ob [die Passport-Authentifizierung in der WinHTTP-Authentifizierung](passport-authentication-in-winhttp.md) aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="941fe-151">Sets an unsigned long integer value that specifies whether [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md) authentication is enabled.</span></span> <span data-ttu-id="941fe-152">Der Wert kann in folgenden Formen vorliegen:</span><span class="sxs-lookup"><span data-stu-id="941fe-152">The value can be one of the following:</span></span>

| <span data-ttu-id="941fe-153">Begriff</span><span class="sxs-lookup"><span data-stu-id="941fe-153">Term</span></span> | <span data-ttu-id="941fe-154">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="941fe-154">Description</span></span> |
|-|-|
| <span data-ttu-id="941fe-155"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ : \_ \_ PASSPORT-AUTHENTIFIZIERUNG DEAKTIVIEREN</span><span class="sxs-lookup"><span data-stu-id="941fe-155"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP\_DISABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="941fe-156">Microsoft Passport Authentifizierung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="941fe-156">Microsoft Passport authentication is disabled.</span></span> <span data-ttu-id="941fe-157">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="941fe-157">This is the default.</span></span> |
| <span data-ttu-id="941fe-158"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ : \_ \_ PASSPORT-SCHLÜSSELRING DEAKTIVIEREN</span><span class="sxs-lookup"><span data-stu-id="941fe-158"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP\_DISABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="941fe-159">Der Passport-Schlüsselring ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="941fe-159">The Passport keyring is disabled.</span></span> <span data-ttu-id="941fe-160">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="941fe-160">This is the default.</span></span> |
| <span data-ttu-id="941fe-161"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ AUTH</span><span class="sxs-lookup"><span data-stu-id="941fe-161"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP\_ENABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="941fe-162">Die Passport-Authentifizierung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="941fe-162">Passport authentication is enabled.</span></span> |
| <span data-ttu-id="941fe-163"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ KEYRING</span><span class="sxs-lookup"><span data-stu-id="941fe-163"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP\_ENABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="941fe-164">Der Passport-Schlüsselring ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="941fe-164">The Passport keyring is enabled.</span></span> |

</dl> </dd> <dt>

<span data-ttu-id="941fe-165"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**\_WINHTTP-OPTION \_ – \_ VERBINDUNGS-RETRIES**</span><span class="sxs-lookup"><span data-stu-id="941fe-165"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-166">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Anzahl der Versuche vonWinHTTP enthält, eine Verbindung mit einem Host herzustellen, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="941fe-166">Sets or retrieves an unsigned long integer value that contains the number of timesWinHTTP attempts to connect to a host.</span></span> <span data-ttu-id="941fe-167">Microsoft Windows HTTP Services (WinHTTP) versucht nur einmal pro IP-Adresse (InternetProtokoll).</span><span class="sxs-lookup"><span data-stu-id="941fe-167">Microsoft Windows HTTP Services (WinHTTP) only attempts once per Internet Protocol (IP) address.</span></span> <span data-ttu-id="941fe-168">Wenn Sie beispielsweise versuchen, eine Verbindung mit einem mehrfach vernetzten Host herzustellen, der über 10 IP-Adressen verfügt und **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** auf 7 festgelegt ist, versucht WinHTTP nur, eine Verbindung mit den ersten sieben IP-Adressen herzustellen.</span><span class="sxs-lookup"><span data-stu-id="941fe-168">For example, if you attempt to connect to a multihomed host that has 10 IP addresses and **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 7, then WinHTTP only attempts to connect to the first seven IP address.</span></span> <span data-ttu-id="941fe-169">Wenn **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** auf 20 festgelegt ist, versucht WinHTTP bei 10 IP-Adressen nur einmal, jede der zehn IP-Adressen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="941fe-169">Given the same set of 10 IP addresses, if **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 20, WinHTTP attempts each of the 10 only once.</span></span> <span data-ttu-id="941fe-170">Wenn ein Verbindungsversuch nach der angegebenen Anzahl von Versuchen weiterhin fehlschlägt oder das Verbindungszeitout vor diesem Zeitpunkt abgelaufen ist, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="941fe-170">If a connection attempt still fails after the specified number of attempts, or if the connect timeout expired before then, the request is canceled.</span></span> <span data-ttu-id="941fe-171">Der Standardwert für **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES ist** fünf Versuche.</span><span class="sxs-lookup"><span data-stu-id="941fe-171">The default value for **WINHTTP\_OPTION\_CONNECT\_RETRIES** is five attempts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-172"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP \_ OPTION \_ CONNECT \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="941fe-172"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-173">Legt einen ganzzahligen Wert ohne Vorzeichen, der den Time out-Wert enthält, in Millisekunden fest oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="941fe-173">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds.</span></span> <span data-ttu-id="941fe-174">Wenn Sie diese Option auf unendlich (0xFFFFFFFF) festlegen, wird dieser Timer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="941fe-174">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="941fe-175">Wenn eine TCP-Verbindungsanforderung länger als dieser Time out-Wert dauert, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="941fe-175">If a TCP connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="941fe-176">Das Standard-Timeout beträgt 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="941fe-176">The default timeout is 60 seconds.</span></span> <span data-ttu-id="941fe-177">Wenn Sie versuchen, eine Verbindung mit mehreren IP-Adressen für einen einzelnen Host (einen mehrfach vernetzten Host) herzustellen, gilt das Timeoutlimit für jede einzelne Verbindung.</span><span class="sxs-lookup"><span data-stu-id="941fe-177">When you are attempting to connect to multiple IP addresses for a single host (a multihomed host), the timeout limit is for each individual connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-178"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**VERBINDUNGSINFORMATIONEN \_ ZUR WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-178"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP\_OPTION\_CONNECTION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-179">Ruft die Quell- und Ziel-IP-Adresse und den Port der Anforderung ab, die die Antwort generiert hat, wenn [**WinHttpReceiveResponse zurückgegeben**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) wird.</span><span class="sxs-lookup"><span data-stu-id="941fe-179">Retrieves the source and destination IP address, and port of the request that generated the response when [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns.</span></span> <span data-ttu-id="941fe-180">Die Anwendung ruft [**WinHttpQueryOption mit**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) der **OPTION WINHTTP OPTION CONNECTION \_ \_ \_ INFO** auf und stellt die [**WINHTTP CONNECTION \_ \_ INFO-Struktur**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) im *lpBuffer-Parameter* zur Auswahl.</span><span class="sxs-lookup"><span data-stu-id="941fe-180">The application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CONNECTION\_INFO** option, and provides the [**WINHTTP\_CONNECTION\_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) structure in the *lpBuffer* parameter.</span></span> <span data-ttu-id="941fe-181">Weitere Informationen finden Sie unter **WINHTTP \_ CONNECTION \_ INFO**.</span><span class="sxs-lookup"><span data-stu-id="941fe-181">For more information, see **WINHTTP\_CONNECTION\_INFO**.</span></span>

<span data-ttu-id="941fe-182">**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="941fe-182">**Windows Server 2003 with SP1 and Windows XP with SP2:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V0**</span><span class="sxs-lookup"><span data-stu-id="941fe-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V0**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-184">Sucht die [**TCP \_ INFO \_ v0-Struktur**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) für die zugrunde liegende Verbindung, die von der Anforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="941fe-184">Retreives the [**TCP\_INFO\_v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="941fe-185">Die zurückgegebene Struktur kann Statistiken aus vorherigen Anforderungen enthalten, die über dieselbe Verbindung gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="941fe-185">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>

> [!Note]
> <span data-ttu-id="941fe-186">Diese Option wurde durch **WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1 ersetzt.**</span><span class="sxs-lookup"><span data-stu-id="941fe-186">This option has been superseded by **WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-187"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1**</span><span class="sxs-lookup"><span data-stu-id="941fe-187"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-188">Retreives die [**TCP \_ INFO \_ v1-Struktur**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) für die zugrunde liegende Verbindung, die von der Anforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="941fe-188">Retreives the [**TCP\_INFO\_v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="941fe-189">Die zurückgegebene Struktur kann Statistiken aus vorherigen Anforderungen enthalten, die über dieselbe Verbindung gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="941fe-189">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-190"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**KONTEXTWERT \_ DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-190"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-191">Legt eine **\_ DWORD-PTR fest** oder ruft sie ab, die einen Zeiger auf den Kontextwert enthält, der diesem [HINTERNET-Handle zugeordnet](hinternet-handles-in-winhttp.md) ist.</span><span class="sxs-lookup"><span data-stu-id="941fe-191">Sets or retrieves a **DWORD\_PTR** that contains a pointer to the context value associated with this [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span> <span data-ttu-id="941fe-192">Der im Puffer gespeicherte Wert wird verwendet, und dem **Optionsflag WINHTTP \_ OPTION CONTEXT \_ \_ VALUE** wird ein neuer Wert zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="941fe-192">The value stored in the buffer is used and the **WINHTTP\_OPTION\_CONTEXT\_VALUE** option flag is assigned a new value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-193"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**DEKOMPRIMIERUNG \_ DER WINHTTP-OPTION \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-193"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP\_OPTION\_DECOMPRESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-194">Legt ein DWORD von Flags fest, die bestimmen, ob WinHTTP Antwortkörper automatisch mit komprimierten Inhaltscodierungen dekomprimiert.</span><span class="sxs-lookup"><span data-stu-id="941fe-194">Sets a DWORD of flags which determine whether WinHTTP will automatically decompress response bodies with compressed Content-Encodings.</span></span> <span data-ttu-id="941fe-195">WinHTTP wird auch einen entsprechenden Accept-Encoding festlegen und alle vom Aufrufer bereitgestellten überschreiben.</span><span class="sxs-lookup"><span data-stu-id="941fe-195">WinHTTP will also set an appropriate Accept-Encoding header, overriding any supplied by the caller.</span></span> <span data-ttu-id="941fe-196">Diese Werte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="941fe-196">Supported values are:</span></span>

| <span data-ttu-id="941fe-197">Begriff</span><span class="sxs-lookup"><span data-stu-id="941fe-197">Term</span></span> | <span data-ttu-id="941fe-198">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="941fe-198">Description</span></span> |
|-|-|
| <span data-ttu-id="941fe-199"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>\_WINHTTP-DEKOMPRIMIERUNGSFLAG \_ \_ GZIP</span><span class="sxs-lookup"><span data-stu-id="941fe-199"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP\_DECOMPRESSION\_FLAG\_GZIP</span></span> | <span data-ttu-id="941fe-200">Dekomprimieren der Inhaltscodierung: gzip-Antworten.</span><span class="sxs-lookup"><span data-stu-id="941fe-200">Decompress Content-Encoding: gzip responses.</span></span> |
| <span data-ttu-id="941fe-201"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP \_ DECOMPRESSION \_ FLAG \_ DEFLATE</span><span class="sxs-lookup"><span data-stu-id="941fe-201"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP\_DECOMPRESSION\_FLAG\_DEFLATE</span></span> | <span data-ttu-id="941fe-202">Dekomprimieren der Inhaltscodierung: Verfeinern von Antworten.</span><span class="sxs-lookup"><span data-stu-id="941fe-202">Decompress Content-Encoding: deflate responses.</span></span> |
| <span data-ttu-id="941fe-203"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>\_WINHTTP-DEKOMPRIMIERUNGSFLAG \_ \_ ALL</span><span class="sxs-lookup"><span data-stu-id="941fe-203"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP\_DECOMPRESSION\_FLAG\_ALL</span></span> | <span data-ttu-id="941fe-204">Dekomprimieren Sie Antworten mit jeder unterstützten Inhaltscodierung.</span><span class="sxs-lookup"><span data-stu-id="941fe-204">Decompress responses with any supported Content-Encoding.</span></span> |

<span data-ttu-id="941fe-205">Standardmäßig liefert WinHTTP komprimierte Antworten unverändert an den Aufrufer.</span><span class="sxs-lookup"><span data-stu-id="941fe-205">By default, WinHTTP will deliver compressed responses to the caller unmodified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-206"><span id="WINHTTP_OPTION_DISABLE_CERT_CHAIN_BUILDING"></span><span id="winhttp_option_disable_cert_chain_building"></span>**WINHTTP-OPTION \_ \_ \_ CERT CHAIN \_ BUILDING \_ DEAKTIVIEREN**</span><span class="sxs-lookup"><span data-stu-id="941fe-206"><span id="WINHTTP_OPTION_DISABLE_CERT_CHAIN_BUILDING"></span><span id="winhttp_option_disable_cert_chain_building"></span>**WINHTTP\_OPTION\_DISABLE\_CERT\_CHAIN\_BUILDING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="941fe-207">Wenn Sie diese Option für ein WinHttp-Sitzungshand handle festlegen, können Sie aktivieren/deaktivieren, ob die Serverzertifikatkette erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="941fe-207">Setting this option on a WinHttp session handle allows you to enable/disable whether the server certificate chain is built.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-208"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**FUNKTION \_ "WINHTTP-OPTION \_ \_ DEAKTIVIEREN"**</span><span class="sxs-lookup"><span data-stu-id="941fe-208"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP\_OPTION\_DISABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-209">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, welche Features mit mindestens einem der folgenden Flags deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-209">Sets an unsigned long integer value that specifies which features are disabled with one or more of the following flags.</span></span> <span data-ttu-id="941fe-210">Beachten Sie, dass dieses Feature nur bei Anforderungshandles an [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) übergeben werden sollte, nachdem das Anforderungshandles mit [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellt wurde und bevor die Anforderung mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="941fe-210">Be aware that this feature should only be passed to [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) on request handles after the request handle is created with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), and before the request is sent with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

| <span data-ttu-id="941fe-211">Begriff</span><span class="sxs-lookup"><span data-stu-id="941fe-211">Term</span></span> | <span data-ttu-id="941fe-212">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="941fe-212">Description</span></span> |
|-|-|
| <span data-ttu-id="941fe-213"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>\_WINHTTP: DEAKTIVIEREN DER \_ AUTHENTIFIZIERUNG</span><span class="sxs-lookup"><span data-stu-id="941fe-213"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP\_DISABLE\_AUTHENTICATION</span></span> | <span data-ttu-id="941fe-214">Die automatische Authentifizierung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="941fe-214">Automatic authentication is disabled.</span></span> |
| <span data-ttu-id="941fe-215"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP \_ DEAKTIVIEREN VON \_ COOKIES</span><span class="sxs-lookup"><span data-stu-id="941fe-215"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP\_DISABLE\_COOKIES</span></span> | <span data-ttu-id="941fe-216">Das automatische Hinzufügen von Cookieheadern zu Anforderungen ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="941fe-216">Automatic addition of cookie headers to requests is disabled.</span></span> <span data-ttu-id="941fe-217">Außerdem werden zurückgegebene Cookies nicht automatisch zur Cookiedatenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="941fe-217">Also, returned cookies are not automatically added to the cookie database.</span></span> <span data-ttu-id="941fe-218">Das Deaktivieren von Cookies kann zu einer schlechten Leistung für die Passport-Authentifizierung führen.</span><span class="sxs-lookup"><span data-stu-id="941fe-218">Disabling cookies can result in poor performance for Passport authentication.</span></span> |
| <span data-ttu-id="941fe-219"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ DISABLE \_ KEEP \_ ALIVE</span><span class="sxs-lookup"><span data-stu-id="941fe-219"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP\_DISABLE\_KEEP\_ALIVE</span></span> | <span data-ttu-id="941fe-220">Deaktiviert die Keep-Alive-Semantik für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="941fe-220">Disables keep-alive semantics for the connection.</span></span> <span data-ttu-id="941fe-221">Keep-Alive-Semantik ist für MSN, NTLM und andere Authentifizierungstypen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="941fe-221">Keep-alive semantics are required for MSN, NTLM, and other types of authentication.</span></span> |
| <span data-ttu-id="941fe-222"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>\_WINHTTP: DEAKTIVIEREN \_ VON UMLEITUNGEN</span><span class="sxs-lookup"><span data-stu-id="941fe-222"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP\_DISABLE\_REDIRECTS</span></span> | <span data-ttu-id="941fe-223">Die automatische Umleitung ist deaktiviert, wenn Anforderungen mit [**WinHttpSendRequest gesendet werden.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="941fe-223">Automatic redirection is disabled when sending requests with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="941fe-224">Wenn die automatische Umleitung deaktiviert ist, muss eine Anwendung eine Rückruffunktion registrieren, damit die Passport-Authentifizierung erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="941fe-224">If automatic redirection is disabled, an application must register a callback function in order for Passport authentication to succeed.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="941fe-225"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**\_WINHTTP-OPTION: \_ DEAKTIVIEREN DES \_ \_ \_ FALLBACKS DES SICHEREN PROTOKOLLS**</span><span class="sxs-lookup"><span data-stu-id="941fe-225"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-226">Verhindert, dass WinHTTP eine Verbindung mit einer niedrigeren Version des Sicherheitsprotokolls erneut versucht, wenn die erste Protokollaushandlung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="941fe-226">Prevents WinHTTP from retrying a connection with a lower version of the security protocol when the initial protocol negotiation fails.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-227"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP-OPTION \_ \_ \_ STREAMWARTESCHLANGE \_ DEAKTIVIEREN**</span><span class="sxs-lookup"><span data-stu-id="941fe-227"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-228">Ermöglicht es neuen Anforderungen, eine zusätzliche HTTP/2-Verbindung zu öffnen, wenn die maximale Anzahl gleichzeitiger Streams erreicht ist, anstatt auf den nächsten verfügbaren Stream für eine vorhandene Verbindung zu warten.</span><span class="sxs-lookup"><span data-stu-id="941fe-228">Allows new requests to open an additional HTTP/2 connection when the maximum concurrent stream limit is reached, rather than waiting for the next available stream on an existing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-229"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**FEATURE \_ "WINHTTP-OPTION \_ \_ AKTIVIEREN"**</span><span class="sxs-lookup"><span data-stu-id="941fe-229"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP\_OPTION\_ENABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-230">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die derzeit aktivierten Funktionen angibt.</span><span class="sxs-lookup"><span data-stu-id="941fe-230">Sets an unsigned long integer value that specifies the features currently enabled.</span></span> <span data-ttu-id="941fe-231">Kann einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="941fe-231">Can be one of the following values.</span></span>

| <span data-ttu-id="941fe-232">Begriff</span><span class="sxs-lookup"><span data-stu-id="941fe-232">Term</span></span> | <span data-ttu-id="941fe-233">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="941fe-233">Description</span></span> |
|-|-|
| <span data-ttu-id="941fe-234"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVERT \_ IMPERSONATION</span><span class="sxs-lookup"><span data-stu-id="941fe-234"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP\_ENABLE\_SSL\_REVERT\_IMPERSONATION</span></span> | <span data-ttu-id="941fe-235">Wenn diese Option aktiviert ist, wird der Clientwechsel von WinHTTP vorübergehend für die Dauer von SSL-Zertifikatauthentifizierungsvorgängen rückgängig machen.</span><span class="sxs-lookup"><span data-stu-id="941fe-235">If enabled, WinHTTP temporarily reverts client impersonation for the duration of SSL certificate authentication operations.</span></span> <span data-ttu-id="941fe-236">Dieser Wert kann nur für das Sitzungshand handle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-236">This value can be set only on the session handle.</span></span> |
| <span data-ttu-id="941fe-237"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVOCATION</span><span class="sxs-lookup"><span data-stu-id="941fe-237"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP\_ENABLE\_SSL\_REVOCATION</span></span> | <span data-ttu-id="941fe-238">Wenn diese Option aktiviert ist, lässt WinHTTP SSL-Sperrvorgänge zu.</span><span class="sxs-lookup"><span data-stu-id="941fe-238">If enabled, WinHTTP allows SSL revocation.</span></span> <span data-ttu-id="941fe-239">Dieser Wert kann nur für das Anforderungshand handle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-239">This value can be set only on the request handle.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-240"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP-OPTION \_ \_ \_ HTTP-PROTOKOLL \_ AKTIVIEREN**</span><span class="sxs-lookup"><span data-stu-id="941fe-240"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-241">Legt eine DWORD-Bitmaske zulässiger erweiterter HTTP-Versionen fest.</span><span class="sxs-lookup"><span data-stu-id="941fe-241">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="941fe-242">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="941fe-242">Possible values are:</span></span>

| <span data-ttu-id="941fe-243">Begriff</span><span class="sxs-lookup"><span data-stu-id="941fe-243">Term</span></span> | <span data-ttu-id="941fe-244">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="941fe-244">Description</span></span> |
|-|-|
| <span data-ttu-id="941fe-245"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>\_ \_ WINHTTP-PROTOKOLLFLAG \_ HTTP2 (0x1)</span><span class="sxs-lookup"><span data-stu-id="941fe-245"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP\_PROTOCOL\_FLAG\_HTTP2 (0x1)</span></span> | <span data-ttu-id="941fe-246">Aktiviert HTTP/2 für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="941fe-246">Enables HTTP/2 for the request.</span></span> |
| <span data-ttu-id="941fe-247">Keine (0x0)</span><span class="sxs-lookup"><span data-stu-id="941fe-247">None (0x0)</span></span> | <span data-ttu-id="941fe-248">Schränkt die Anforderung auf HTTP/1.1 und früher ein.</span><span class="sxs-lookup"><span data-stu-id="941fe-248">Restricts the request to HTTP/1.1 and prior.</span></span> |

<span data-ttu-id="941fe-249">Ältere Versionen von HTTP (1.1 und früher) können mit dieser Option nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-249">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="941fe-250">Der Standardwert ist 0x0.</span><span class="sxs-lookup"><span data-stu-id="941fe-250">The default is 0x0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-251"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**\_WINHTTP-OPTION \_ \_ HTTP2 \_ PLUS CLIENT \_ \_ CERT AKTIVIEREN**</span><span class="sxs-lookup"><span data-stu-id="941fe-251"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="941fe-252">Diese Option kann für ein WinHttp-Sitzungshand handle festgelegt werden, damit WinHttp den vom Aufrufer bereitgestellten Clientzertifikatkontext verwenden kann, wenn HTTP/2 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="941fe-252">This option can be set on a WinHttp session handle to allow WinHttp to use the caller-provided client certificate context when HTTP/2 is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-253"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**\_WINHTTP-OPTION \_ ENABLETRACING**</span><span class="sxs-lookup"><span data-stu-id="941fe-253"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP\_OPTION\_ENABLETRACING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-254">Legt einen **BOOL-Wert** fest, der angibt, ob die Ablaufverfolgung derzeit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="941fe-254">Sets a **BOOL** value that specifies whether tracing is currently enabled.</span></span> <span data-ttu-id="941fe-255">Weitere Informationen zur Ablaufverfolgungseinrichtung in WinHTTP finden Sie unter [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="941fe-255">For more information about the trace facility in WinHTTP, see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span> <span data-ttu-id="941fe-256">Diese Option kann nur  für ein NULL **HINTERNET-Handle festgelegt** werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-256">This option can only be set on a **NULL** **HINTERNET** handle.</span></span>


</dt> </dl> </dd>

<dt>

<span data-ttu-id="941fe-257"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP \_ OPTION \_ ENCODE \_ EXTRA**</span><span class="sxs-lookup"><span data-stu-id="941fe-257"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-258">Aktiviert die URL-Prozentcodierung für Pfad und Abfragezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="941fe-258">Enables URL percent encoding for path and query string.</span></span>

<span data-ttu-id="941fe-259">Alternativ können Sie vor dem Aufrufen von WinHttp prozentweise codieren.</span><span class="sxs-lookup"><span data-stu-id="941fe-259">Alternatively, you can percent encode before calling WinHttp.</span></span>

</dt> </dl> </dd>

<dt>

<span data-ttu-id="941fe-260"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP-OPTION \_ \_ VERBINDUNG \_ ABLAUFEN**</span><span class="sxs-lookup"><span data-stu-id="941fe-260"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP\_OPTION\_EXPIRE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-261">Diese Option kann nur für ein Anforderungshand handle festgelegt werden, das noch aktiv ist (senden oder empfangen).</span><span class="sxs-lookup"><span data-stu-id="941fe-261">This option can only be set on a request handle which is still active (sending or receiving).</span></span> <span data-ttu-id="941fe-262">Wenn Sie diese Option festlegen, wird WinHttp dazu veranschlagen, die Verarbeiten von Anforderungen für die Verbindung zu beenden, die dem übergebenen Anforderungshand handle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="941fe-262">Setting this option will tell WinHttp to stop serving requests on the connection associated with the request handle passed in.</span></span> <span data-ttu-id="941fe-263">Die Verbindung wird geschlossen, nachdem das Anforderungshand handle, mit dem diese Option aufgerufen wird, abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="941fe-263">The connection will be closed after the request handle this option is called with is completed.</span></span> <span data-ttu-id="941fe-264">Bei dieser Option werden keine Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="941fe-264">This option does not take any parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-265"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**ERWEITERTER \_ FEHLER DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-265"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-266">Ruft einen ganzzahligen Wert ohne Vorzeichen ab, der einen Microsoft Windows Sockets-Fehlercode enthält, der den ZULETZT in diesem Threadkontext zurückgegebenen \_ ERROR WINHTTP-Fehlermeldungen \_ \* zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="941fe-266">Retrieves an unsigned long integer value that contains a Microsoft Windows Sockets error code that was mapped to the ERROR\_WINHTTP\_\* error messages last returned in this thread context.</span></span> <span data-ttu-id="941fe-267">Sie können **NULL als** Handlewert übergeben.</span><span class="sxs-lookup"><span data-stu-id="941fe-267">You can pass **NULL** as the handle value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-268"><span id="WINHTTP_OPTION_FIRST_AVAILABLE_CONNECTION"></span><span id="winhttp_option_first_available_connection"></span>**\_WINHTTP-OPTION \_ ERSTE VERFÜGBARE \_ \_ VERBINDUNG**</span><span class="sxs-lookup"><span data-stu-id="941fe-268"><span id="WINHTTP_OPTION_FIRST_AVAILABLE_CONNECTION"></span><span id="winhttp_option_first_available_connection"></span>**WINHTTP\_OPTION\_FIRST\_AVAILABLE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="941fe-269">Wenn WinHttp eine Anforderung sendet und keine Verbindungen zum Bedienen der Anforderung verfügbar sind, versucht WinHttp standardmäßig, eine neue Verbindung herzustellen, und die Anforderung wird an diese neue Verbindung gebunden.</span><span class="sxs-lookup"><span data-stu-id="941fe-269">By default, when WinHttp sends a request, if there are no available connections to serve the request, WinHttp will attempt to establish a new connection, and the request will be bound to this new connection.</span></span> <span data-ttu-id="941fe-270">Wenn Sie diese Option festlegen, wird eine solche Anforderung stattdessen für die erste verfügbare Verbindung und nicht notwendigerweise für die hergestellte Verbindung bedient.</span><span class="sxs-lookup"><span data-stu-id="941fe-270">When you set this option, such a request will instead be served on the first connection that becomes available, and not necessarily the one being established.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-271"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**GLOBALE \_ PROXY-ANMELDEINFORMATIONEN FÜR DIE \_ \_ \_ WINHTTP-OPTION**</span><span class="sxs-lookup"><span data-stu-id="941fe-271"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-272">Verwendet einen Zeiger auf eine [**WINHTTP \_ CREDS \_ EX-Struktur,**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) bei der der *hInternet-Funktionsparameter* auf **NULL festgelegt ist.**</span><span class="sxs-lookup"><span data-stu-id="941fe-272">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="941fe-273">Diese Option erfordert den Registrierungsschlüssel **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="941fe-273">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="941fe-274">Wenn dieser Registrierungsschlüssel nicht festgelegt ist, gibt WinHTTP den Fehler **\_ ERROR WINHTTP INVALID OPTION \_ \_ zurück.**</span><span class="sxs-lookup"><span data-stu-id="941fe-274">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="941fe-275">Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="941fe-275">This registry key is not present by default.</span></span> <span data-ttu-id="941fe-276">Wenn sie festgelegt ist, sendet WinINet Anmeldeinformationen an WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="941fe-276">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="941fe-277">Wenn WinHttp eine Authentifizierungsforderung erhält und keine Anmeldeinformationen für das aktuelle Handle festgelegt sind, werden die von WinINet bereitgestellten Anmeldeinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="941fe-277">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="941fe-278">Um Serveranmeldeinformationen zusätzlich zu Proxyanmeldeinformationen gemeinsam zu verwenden, müssen Benutzer **WINHTTP \_ OPTION USE GLOBAL SERVER CREDENTIALS \_ \_ \_ (GLOBALE SERVERANMELDEINFORMATIONEN \_ VERWENDEN) festlegen.**</span><span class="sxs-lookup"><span data-stu-id="941fe-278">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-279"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**\_WINHTTP-OPTION \_ : GLOBALE \_ \_ SERVER-ANMELDEINFORMATIONEN**</span><span class="sxs-lookup"><span data-stu-id="941fe-279"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-280">Verwendet einen Zeiger auf eine [**WINHTTP \_ CREDS \_ EX-Struktur,**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) bei der der *hInternet-Funktionsparameter* auf **NULL festgelegt ist.**</span><span class="sxs-lookup"><span data-stu-id="941fe-280">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="941fe-281">Diese Option erfordert den Registrierungsschlüssel **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="941fe-281">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="941fe-282">Wenn dieser Registrierungsschlüssel nicht festgelegt ist, gibt WinHTTP den Fehler **\_ ERROR WINHTTP INVALID OPTION \_ \_ zurück.**</span><span class="sxs-lookup"><span data-stu-id="941fe-282">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="941fe-283">Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="941fe-283">This registry key is not present by default.</span></span> <span data-ttu-id="941fe-284">Wenn sie festgelegt ist, sendet WinINet Anmeldeinformationen an WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="941fe-284">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="941fe-285">Wenn WinHttp eine Authentifizierungsforderung erhält und keine Anmeldeinformationen für das aktuelle Handle festgelegt sind, werden die von WinINet bereitgestellten Anmeldeinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="941fe-285">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="941fe-286">Um Serveranmeldeinformationen zusätzlich zu Proxyanmeldeinformationen gemeinsam zu verwenden, müssen Benutzer **WINHTTP \_ OPTION USE GLOBAL SERVER CREDENTIALS \_ \_ \_ (GLOBALE SERVERANMELDEINFORMATIONEN \_ VERWENDEN) festlegen.**</span><span class="sxs-lookup"><span data-stu-id="941fe-286">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-287"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**HANDLETYP \_ DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-287"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-288">Ruft einen ganzzahligen Wert ohne Vorzeichen ab, der den Typ des übergebenen [HINTERNET-Handles](hinternet-handles-in-winhttp.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="941fe-288">Retrieves an unsigned long integer value that contains the type of the [HINTERNET](hinternet-handles-in-winhttp.md) handle passed in.</span></span> <span data-ttu-id="941fe-289">Einer der folgenden Werte kann zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="941fe-289">The return value can be one of the following:</span></span>

| <span data-ttu-id="941fe-290">Begriff</span><span class="sxs-lookup"><span data-stu-id="941fe-290">Term</span></span> | <span data-ttu-id="941fe-291">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="941fe-291">Description</span></span> |
|-|-|
| <span data-ttu-id="941fe-292"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP \_ HANDLE \_ TYPE \_ CONNECT</span><span class="sxs-lookup"><span data-stu-id="941fe-292"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP\_HANDLE\_TYPE\_CONNECT</span></span> | <span data-ttu-id="941fe-293">Das Handle ist ein Verbindungshand handle.</span><span class="sxs-lookup"><span data-stu-id="941fe-293">The handle is a connection handle.</span></span> |
| <span data-ttu-id="941fe-294"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>\_ \_ WINHTTP-HANDLETYPANFORDERUNG \_</span><span class="sxs-lookup"><span data-stu-id="941fe-294"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP\_HANDLE\_TYPE\_REQUEST</span></span> | <span data-ttu-id="941fe-295">Das Handle ist ein Anforderungshand handle.</span><span class="sxs-lookup"><span data-stu-id="941fe-295">The handle is a request handle.</span></span> |
| <span data-ttu-id="941fe-296"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>SITZUNG MIT \_ \_ WINHTTP-HANDLETYP \_</span><span class="sxs-lookup"><span data-stu-id="941fe-296"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP\_HANDLE\_TYPE\_SESSION</span></span> | <span data-ttu-id="941fe-297">Das Handle ist ein Sitzungshand handle.</span><span class="sxs-lookup"><span data-stu-id="941fe-297">The handle is a session handle.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="941fe-298"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**\_WINHTTP-OPTION \_ \_ HTTP-PROTOKOLL \_ ERFORDERLICH**</span><span class="sxs-lookup"><span data-stu-id="941fe-298"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-299">Verhindert, dass andere Protokollversionen als die von **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL** aktivierten für die Anforderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-299">Prevents protocol versions other than those enabled by **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL** from being used for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-300"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**VERWENDETES \_ \_ HTTP-PROTOKOLL DER \_ WINHTTP-OPTION \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-300"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-301">Ruft ein DWORD ab, das angibt, welche erweiterte HTTP-Version für eine bestimmte Anforderung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="941fe-301">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="941fe-302">Eine Liste der möglichen Werte finden Sie unter **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL**.</span><span class="sxs-lookup"><span data-stu-id="941fe-302">For a list of possible values, see **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-303"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**\_HTTP-VERSION DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-303"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-304">Legt eine HTTP-VERSIONSINFORMATIONsstruktur fest, die die unterstützte HTTP-Version enthält, oder ruft sie ab. [**\_ \_**](/windows/win32/api/winhttp/ns-winhttp-http_version_info)</span><span class="sxs-lookup"><span data-stu-id="941fe-304">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) structure that contains the HTTP version being supported.</span></span> <span data-ttu-id="941fe-305">Dies ist eine prozessweite Option. Verwenden **Sie NULL** für das Handle.</span><span class="sxs-lookup"><span data-stu-id="941fe-305">This is a process-wide option; use **NULL** for the handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-306"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**\_WINHTTP-OPTION \_ HTTP2 \_ KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="941fe-306"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**WINHTTP\_OPTION\_HTTP2\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="941fe-307">Diese Option kann für ein Sitzungshand handle festgelegt werden, damit WinHttp HTTP/2-PING-Frames als Keepalive-Mechanismus verwendet.</span><span class="sxs-lookup"><span data-stu-id="941fe-307">This option can be set on a session handle to have WinHttp use HTTP/2 PING frames as a keepalive mechanism.</span></span> <span data-ttu-id="941fe-308">Aufrufer geben ein Timeout in Millisekunden an, und wenn für diesen Timeoutzeitraum keine Aktivität für eine Verbindung besteht, beginnt WinHttp mit dem Senden von HTTP/2-PING-Frames.</span><span class="sxs-lookup"><span data-stu-id="941fe-308">Callers specify a timeout in milliseconds, and after there is no activity on a connection for that timeout period, WinHttp will begin to send HTTP/2 PING frames.</span></span> <span data-ttu-id="941fe-309">Aufrufer können keinen Timeoutwert unter 5.000 Millisekunden festlegen.</span><span class="sxs-lookup"><span data-stu-id="941fe-309">Callers cannot set a timeout value less than 5000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-310"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**WINHTTP-OPTION \_ \_ HTTP2 \_ PLUS \_ \_ ÜBERTRAGUNGSCODIERUNG**</span><span class="sxs-lookup"><span data-stu-id="941fe-310"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="941fe-311">Diese Option kann für ein WinHttp-Anforderungshand handle festgelegt werden, um das Verhalten von WinHttp zu steuern, wenn eine HTTP/2-Antwort einen "Transfer-Encoding"-Header enthält.</span><span class="sxs-lookup"><span data-stu-id="941fe-311">This option can be set on a WinHttp request handle to control how WinHttp behaves when an HTTP/2 response contains a "Transfer-Encoding" header.</span></span> <span data-ttu-id="941fe-312">In diesem Fall gibt WinHttp einen Fehler zurück, wenn diese Option auf **FALSE festgelegt ist.**</span><span class="sxs-lookup"><span data-stu-id="941fe-312">In such a case, WinHttp will return an error if this option is set to **FALSE**.</span></span>


</dt> </dl> </dd> <dt>


<span data-ttu-id="941fe-313"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP-OPTION \_ \_ \_ ZERTIFIKATSPERRUNG \_ \_ OFFLINE IGNORIEREN**</span><span class="sxs-lookup"><span data-stu-id="941fe-313"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-314">Ermöglicht sicheren Verbindungen die Verwendung von Sicherheitszertifikaten, für die die Zertifikatsperrliste nicht heruntergeladen werden konnte.</span><span class="sxs-lookup"><span data-stu-id="941fe-314">Allows secure connections to use security certificates for which the certificate revocation list could not be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-315"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP-OPTION \_ \_ IPV6 \_ – SCHNELLER \_ FALLBACK**</span><span class="sxs-lookup"><span data-stu-id="941fe-315"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-316">Aktiviert schnelles IPv6-Fallback (Brillenbrillen) für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="941fe-316">Enables IPv6 fast fallback (Happier Eyeballs) for the connection.</span></span> <span data-ttu-id="941fe-317">Dieses Verhalten ähnelt dem In RFC [6555](https://tools.ietf.org/html/rfc6555) beschriebenen Verhalten von Happy Eyeballs zur Verbesserung der Verbindungszeiten in Netzwerken, in denen IPv6 unzuverlässig ist.</span><span class="sxs-lookup"><span data-stu-id="941fe-317">This behavior is similar to the Happy Eyeballs behavior described in [RFC 6555](https://tools.ietf.org/html/rfc6555) for improving connection times on networks where IPv6 is unreliable.</span></span>
- <span data-ttu-id="941fe-318">Wenn sowohl IPv6- als auch IPv4-Adressen für einen bestimmten Host aufgelöst werden, beginnt WinHttp mit dem Herstellen einer Verbindung mit der ersten aufgelösten IPv6-Adresse mit einem kurzen Timeout (300 ms).</span><span class="sxs-lookup"><span data-stu-id="941fe-318">If both IPv6 and IPv4 addresses are resolved for a given host, WinHttp will begin by connecting to the first resolved IPv6 address with a short (300ms) timeout.</span></span>
- <span data-ttu-id="941fe-319">Sollte diese Verbindung fehlschlagen, versucht WinHttp, eine Verbindung mit der ersten aufgelösten IPv4-Adresse mit dem Standard-Timeout herzustellen.</span><span class="sxs-lookup"><span data-stu-id="941fe-319">Should that connection fail, WinHttp will attempt to connect to the first resolved IPv4 address with the standard timeout.</span></span>
- <span data-ttu-id="941fe-320">Sollte bei der zweiten Verbindung ein Fehler auftäussen, wird von WinHttp die erste aufgelöste IPv6-Adresse mit dem Standard-Timeout erneut verwendet.</span><span class="sxs-lookup"><span data-stu-id="941fe-320">Should the second connection fail, WinHttp will retry the first resolved IPv6 address with the standard timeout.</span></span>
- <span data-ttu-id="941fe-321">Sollte bei der dritten Verbindung ein Fehler auftäussen, wird winHttp auf das Standardverhalten für alle verbleibenden Adressen zurückverwendet und versucht, eine Verbindung mit jeder Adresse mit dem Standard-Timeout herzustellen, bis eine Verbindung hergestellt wird oder keine Adressen mehr bestehen.</span><span class="sxs-lookup"><span data-stu-id="941fe-321">Should the third connection fail, WinHttp will revert to the default behavior for any remaining addresses, attempting a connection to each one with the standard timeout until a connection is made or no addresses remain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-322"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**\_WINHTTP-OPTION \_ IST PROXY \_ \_ \_ CONNECT-ANTWORT**</span><span class="sxs-lookup"><span data-stu-id="941fe-322"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-323">Ruft ab, ob eine Proxy Return Connect-Antwort abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="941fe-323">Gets whether or not a Proxy Return Connect Response can be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-324"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**\_WINHTTP-OPTION \_ \_ MAX. CONNS \_ PRO \_ 1 \_ 0 \_ SERVER**</span><span class="sxs-lookup"><span data-stu-id="941fe-324"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-325">Legt einen ganzzahligen Wert ohne Vorzeichen fest oder ruft diesen ab, der die maximale Anzahl von Verbindungen enthält, die pro HTTP/1.0-Server zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="941fe-325">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="941fe-326">Der Standardwert ist **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="941fe-326">The default value is **INFINITE**.</span></span>

<span data-ttu-id="941fe-327">**Windows Vista mit SP1 und Windows Server 2008:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="941fe-327">**Windows Vista with SP1 and Windows Server 2008:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-328"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**\_WINHTTP-OPTION \_ \_ MAX. CONNS \_ PRO \_ SERVER**</span><span class="sxs-lookup"><span data-stu-id="941fe-328"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-329">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die maximal zulässige Anzahl von Verbindungen pro Server enthält, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="941fe-329">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="941fe-330">Der Standardwert ist **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="941fe-330">The default value is **INFINITE**.</span></span>

<span data-ttu-id="941fe-331">Wenn diese Option auf 0 (null) festgelegt ist, legt WinHTTP den Grenzwert für die Anzahl von Verbindungen auf 2 fest.</span><span class="sxs-lookup"><span data-stu-id="941fe-331">When this option is set to zero, WinHTTP sets the limit on the number of connections to 2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-332"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP-OPTION \_ \_ \_ MAX. AUTOMATISCHE \_ \_ HTTP-UMLEITUNGEN**</span><span class="sxs-lookup"><span data-stu-id="941fe-332"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-333">Legt die maximale Anzahl von Umleitungen fest, auf die WinHTTP folgt. Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="941fe-333">Sets the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="941fe-334">Dieser Grenzwert verhindert, dass nicht autorisierte Websites den WinHTTP-Client nach einer großen Anzahl von Umleitungen anhalten.</span><span class="sxs-lookup"><span data-stu-id="941fe-334">This limit prevents unauthorized sites from making the WinHTTP client pause following a large number of redirects.</span></span>

<span data-ttu-id="941fe-335">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="941fe-335">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-336"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP-OPTION \_ \_ \_ MAX. \_ HTTP-STATUS \_ CONTINUE**</span><span class="sxs-lookup"><span data-stu-id="941fe-336"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-337">Die maximale Anzahl von Informationscodeantworten von 100 bis 199, die ignoriert wurden, bevor der endgültige Statuscode an den WinHTTP-Client zurückgezahlt wird.</span><span class="sxs-lookup"><span data-stu-id="941fe-337">The maximum number of Informational 100-199 status code responses ignored before returning the final status code to the WinHTTP client.</span></span> <span data-ttu-id="941fe-338">Informationsstatuscodes 100-199 können vom Server vor dem endgültigen Statuscode gesendet werden und werden in der Spezifikation für HTTP/1.1 beschrieben (weitere Informationen finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span><span class="sxs-lookup"><span data-stu-id="941fe-338">Informational 100-199 status codes can be sent by the server before the final status code, and are described in the specification for HTTP/1.1 (for more information, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span></span> <span data-ttu-id="941fe-339">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="941fe-339">The default is 10.</span></span>

<span data-ttu-id="941fe-340">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="941fe-340">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-341"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP \_ OPTION \_ MAX \_ RESPONSE \_ DRAIN \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="941fe-341"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-342">Eine Grenze für die Menge der Daten, die aus Antworten entleert werden, um eine Verbindung wiederzuverwenden, die in Bytes angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="941fe-342">A bound on the amount of data drained from responses in order to reuse a connection, specified in bytes.</span></span> <span data-ttu-id="941fe-343">Der Standardwert ist 1 MB.</span><span class="sxs-lookup"><span data-stu-id="941fe-343">The default is 1MB.</span></span>

<span data-ttu-id="941fe-344">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="941fe-344">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-345"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP-OPTION \_ \_ \_ MAX. GRÖßE DES \_ \_ ANTWORTHEADERS**</span><span class="sxs-lookup"><span data-stu-id="941fe-345"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-346">Ein gebundener Satz für die maximale Größe des Headerbereichs der Serverantwort, angegeben in Bytes.</span><span class="sxs-lookup"><span data-stu-id="941fe-346">A bound set on the maximum size of the header portion of the server response, specified in bytes.</span></span> <span data-ttu-id="941fe-347">Diese Gebundene schützt den Client vor einem nicht autorisierten Server, der versucht, den Client zu verhindern, indem eine Antwort mit einer unendlichen Menge von Headerdaten gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="941fe-347">This bound protects the client from an unauthorized server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="941fe-348">Der Standardwert ist 64 KB.</span><span class="sxs-lookup"><span data-stu-id="941fe-348">The default value is 64KB.</span></span>

<span data-ttu-id="941fe-349">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="941fe-349">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-350"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**ÜBERGEORDNETES \_ HANDLE DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-350"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-351">Ruft das übergeordnete Handle für dieses Handle ab.</span><span class="sxs-lookup"><span data-stu-id="941fe-351">Retrieves the parent handle to this handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-352"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**\_WINHTTP-OPTION \_ \_ PASSPORT-COBRANDINGTEXT \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-352"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-353">Ruft eine Zeichenfolge ab, die den [*cobranding-Text*](glossary.md) enthält, der vom Passport-Anmeldeserver bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="941fe-353">Retrieves a string that contains the [*cobranding*](glossary.md) text provided by the Passport logon server.</span></span> <span data-ttu-id="941fe-354">Diese Option sollte sofort abgerufen werden, nachdem der Anmeldeserver mit dem Statuscode 401 reagiert hat.</span><span class="sxs-lookup"><span data-stu-id="941fe-354">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="941fe-355">Eine Anwendung sollte eine Puffergröße in Bytes übergeben, die groß genug ist, um die zurückgegebene Zeichenfolge zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="941fe-355">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-356"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**\_WINHTTP-OPTION \_ \_ PASSPORT-COBRANDING-URL \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-356"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-357">Ruft eine Zeichenfolge ab, die eine URL für eine [*Cobrandinggrafik*](glossary.md) enthält, die vom Passport-Anmeldeserver bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="941fe-357">Retrieves a string that contains a URL for a [*cobranding*](glossary.md) graphic provided by the Passport logon server.</span></span> <span data-ttu-id="941fe-358">Diese Option sollte sofort abgerufen werden, nachdem der Anmeldeserver mit dem Statuscode 401 reagiert hat.</span><span class="sxs-lookup"><span data-stu-id="941fe-358">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="941fe-359">Eine Anwendung sollte eine Puffergröße in Bytes übergeben, die groß genug ist, um die zurückgegebene Zeichenfolge zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="941fe-359">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-360"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**\_WINHTTP-OPTION \_ \_ \_ PASSPORT-RÜCKGABE-URL**</span><span class="sxs-lookup"><span data-stu-id="941fe-360"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-361">Legt eine schreibgeschützte Option für ein Anforderungshandles fest, das die Passport-Rückgabe-URL abruft.</span><span class="sxs-lookup"><span data-stu-id="941fe-361">Sets a read-only option on a request handle that retrieves the Passport return URL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-362"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**\_WINHTTP-OPTION \_ \_ \_ PASSPORT-ABMELDEN**</span><span class="sxs-lookup"><span data-stu-id="941fe-362"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-363">Legt die Option für ein Sitzungshand handle zum Abmelden von Passport-Anmeldungen fest.</span><span class="sxs-lookup"><span data-stu-id="941fe-363">Sets the option on a session handle to sign out of any Passport logins.</span></span> <span data-ttu-id="941fe-364">Eine Anwendung sollte die Passport-Rückgabe-URL übergeben, die mit **WINHTTP \_ OPTION PASSPORT RETURN URL abgerufen \_ \_ \_ wurde.**</span><span class="sxs-lookup"><span data-stu-id="941fe-364">An application should pass in the Passport return URL that was retrieved with **WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**.</span></span> <span data-ttu-id="941fe-365">Alle Cookies im Zusammenhang mit der Rückgabe-URL werden wieder löschen.</span><span class="sxs-lookup"><span data-stu-id="941fe-365">All cookies related to the return URL are cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-366"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**\_ \_ WINHTTP-OPTIONSKENNWORT**</span><span class="sxs-lookup"><span data-stu-id="941fe-366"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-367">Legt einen Zeichenfolgenwert fest, der das einem Anforderungshand handle zugeordnete Kennwort enthält, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="941fe-367">Sets or retrieves a string value that contains the password associated with a request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-368"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**\_WINHTTP-OPTIONSPROXY \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-368"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-369">Legt eine [**WINHTTP PROXY \_ \_ INFO-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) fest, die die Proxydaten auf einem vorhandenen Sitzungshand handle oder Anforderungshand handle enthält, oder ruft sie ab.</span><span class="sxs-lookup"><span data-stu-id="941fe-369">Sets or retrieves an [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure that contains the proxy data on an existing session handle or request handle.</span></span> <span data-ttu-id="941fe-370">Beim Abrufen von Proxydaten muss eine Anwendung die in dieser Struktur enthaltenen **lpszProxy-** und **lpszProxyBypass-Zeichenfolgen** (wenn sie nicht NULL **sind)** mithilfe der [**GlobalFree-Funktion**](/windows/desktop/api/winbase/nf-winbase-globalfree) frei geben.</span><span class="sxs-lookup"><span data-stu-id="941fe-370">When retrieving proxy data, an application must free the **lpszProxy** and **lpszProxyBypass** strings contained in this structure (if they are non-**NULL**) using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="941fe-371">Eine Anwendung kann die globalen Proxydaten (den Standardproxy) abfragen, indem sie ein **NULL-Handle** übergibt.</span><span class="sxs-lookup"><span data-stu-id="941fe-371">An application can query for the global proxy data (the default proxy) by passing a **NULL** handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-372"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**\_PROXYKENNWORT \_ FÜR WINHTTP-OPTION \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-372"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-373">Legt einen Zeichenfolgenwert fest, der das Kennwort für den Zugriff auf den Proxy enthält, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="941fe-373">Sets or retrieves a string value that contains the password used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-374"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**VERWENDETER \_ \_ WINHTTP-OPTIONSPROXY-SPN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-374"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WINHTTP\_OPTION\_PROXY\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-375">Ruft den Proxyserverprinzipalnamen ab, den WinHTTP während der Authentifizierung an SSPI übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="941fe-375">Gets the proxy Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="941fe-376">Dieser Zeichenfolgenwert wird verwendet, um nach einem [**Authentifizierungsfehler an SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="941fe-376">This string value is usefor passing to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-377"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**\_PROXYBENUTZERNAME DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-377"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-378">Legt einen Zeichenfolgenwert fest, der den Benutzernamen enthält, der für den Zugriff auf den Proxy verwendet wird, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="941fe-378">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-379"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**\_WINHTTP-OPTION \_ READ BUFFER \_ \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="941fe-379"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-380">Diese Option ist veraltet. es hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="941fe-380">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-381"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP-OPTION \_ \_ "PROXY \_ \_ CONNECT-ANTWORT \_ EMPFANGEN"**</span><span class="sxs-lookup"><span data-stu-id="941fe-381"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-382">Legt fest, ob die Proxyantwortentität abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="941fe-382">Sets whether or not the proxy response entity can be retrieved.</span></span> <span data-ttu-id="941fe-383">Diese Option ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="941fe-383">This option is disabled by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-384"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP-OPTION \_ \_ \_ \_ EMPFANGSANTWORT-TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="941fe-384"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-385">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Timeoutwert in Millisekunden enthält, um auf den Empfang aller Antwortheader für eine Anforderung zu warten, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="941fe-385">Sets or retrieves an unsigned long integer value that contains the timeout value, in milliseconds, to wait to receive all response headers to a request.</span></span> <span data-ttu-id="941fe-386">Wenn WinHTTP nicht alle Header innerhalb dieses Timeoutzeitraums empfangen kann, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="941fe-386">If WinHTTP fails to receive all the headers within this timeout period, the request is canceled.</span></span> <span data-ttu-id="941fe-387">Der Standardwert für das Timeout beträgt 90 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="941fe-387">The default timeout value is 90 seconds.</span></span>

<span data-ttu-id="941fe-388">Dieses Timeout wird nur überprüft, wenn Daten vom Socket empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-388">This timeout is checked only when data is received from the socket.</span></span> <span data-ttu-id="941fe-389">Wenn das Timeout abläuft, wird die Clientanwendung daher erst benachrichtigt, wenn weitere Daten vom Server eintreffen.</span><span class="sxs-lookup"><span data-stu-id="941fe-389">As a result, when the timeout expires the client application is not notified until more data arrives from the server.</span></span> <span data-ttu-id="941fe-390">Wenn keine Daten vom Server eintreffen, kann die Verzögerung zwischen dem Ablauf des Timeouts und der Benachrichtigung der Clientanwendung so groß sein wie der Timeoutwert, der mit dem *dwReceiveTimeout-Parameter* der [**WinHttpSetTimeouts-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="941fe-390">If no data arrives from the server, the delay between the timeout expiration and notification of the client application could be as large as the timeout value set using the *dwReceiveTimeout* parameter of the [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-391"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**\_EMPFANGSZEITÜBERSCHREITUNG DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-391"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-392">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, um eine Teilantwort auf eine Anforderung zu empfangen oder einige Daten zu lesen, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="941fe-392">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a partial response to a request or read some data.</span></span> <span data-ttu-id="941fe-393">Wenn die Antwort länger als dieser Time out-Wert dauert, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="941fe-393">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="941fe-394">Der Standard-Timeoutwert beträgt 30 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="941fe-394">The default timeout value is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-395"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**UMLEITUNGSRICHTLINIE \_ FÜR WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-395"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP\_OPTION\_REDIRECT\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-396">Legt das Verhalten von WinHTTP in Bezug auf die Behandlung eines 30-fachen HTTP-Umleitungsstatuscodes fest.</span><span class="sxs-lookup"><span data-stu-id="941fe-396">Sets the behavior of WinHTTP regarding the handling of a 30x HTTP redirect status code.</span></span> <span data-ttu-id="941fe-397">Diese Option kann für ein Sitzungs- oder Anforderungshand handle auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="941fe-397">This option can be set on a session or request handle to one of the following values:</span></span>

| <span data-ttu-id="941fe-398">Begriff</span><span class="sxs-lookup"><span data-stu-id="941fe-398">Term</span></span> | <span data-ttu-id="941fe-399">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="941fe-399">Description</span></span> |
|-|-|
| <span data-ttu-id="941fe-400"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>RICHTLINIE FÜR DIE UMLEITUNG \_ DER WINHTTP-OPTION \_ \_ \_ IMMER</span><span class="sxs-lookup"><span data-stu-id="941fe-400"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_ALWAYS</span></span> | <span data-ttu-id="941fe-401">Alle Umleitungen werden automatisch befolgt.</span><span class="sxs-lookup"><span data-stu-id="941fe-401">All redirects are followed automatically.</span></span> |
| <span data-ttu-id="941fe-402"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP \_ OPTION \_ REDIRECT \_ POLICY \_ DISALLOW \_ HTTPS \_ TO \_ HTTP</span><span class="sxs-lookup"><span data-stu-id="941fe-402"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_DISALLOW\_HTTPS\_TO\_HTTP</span></span> | <span data-ttu-id="941fe-403">Alle Umleitungen werden befolgt, mit Ausnahme derjenigen, die von einer sicheren (HTTPS)-URL zu einer unsicheren (HTTP)-URL stammen.</span><span class="sxs-lookup"><span data-stu-id="941fe-403">All redirects are followed, except those that originate from a secure (https) URL to an unsecure (http) URL.</span></span> <span data-ttu-id="941fe-404">Dies ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="941fe-404">This is the default setting.</span></span> |
| <span data-ttu-id="941fe-405"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>UMLEITUNGSRICHTLINIE \_ FÜR WINHTTP-OPTION \_ \_ \_ NIE</span><span class="sxs-lookup"><span data-stu-id="941fe-405"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_NEVER</span></span> | <span data-ttu-id="941fe-406">Umleitungen werden nie befolgt.</span><span class="sxs-lookup"><span data-stu-id="941fe-406">Redirects are never followed.</span></span> <span data-ttu-id="941fe-407">Der 30-fache Status wird an die Anwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="941fe-407">The 30x status is returned to the application.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-408"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**\_WINHTTP-OPTION \_ \_ : USERPWD \_ IN \_ URL ABLEHNEN**</span><span class="sxs-lookup"><span data-stu-id="941fe-408"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-409">Lehnt URLs ab, die einen Benutzernamen und ein Kennwort enthalten.</span><span class="sxs-lookup"><span data-stu-id="941fe-409">Rejects URLs that contain a username and password.</span></span> <span data-ttu-id="941fe-410">Diese Option lehnt auch URLs ab, die *username:password-Semantik* enthalten, auch wenn kein Benutzername oder Kennwort angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="941fe-410">This option also rejects URLs that contain *username:password* semantics, even if no username or password is specified.</span></span> <span data-ttu-id="941fe-411">Beispielsweise würden u:p@hostname " ", :@hostname " ", " u:@hostname " " und " " alle als ungültig gekennzeichnet :p@hostname werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-411">For example, "u:p@hostname", ":@hostname", "u:@hostname", and ":p@hostname" would all be flagged as invalid.</span></span> <span data-ttu-id="941fe-412">Wenn eine ungültige URL an die Funktion übergeben wird, wird [ERROR \_ WINHTTP \_ INVALID \_ URL](error-messages.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="941fe-412">If an invalid URL is passed to the function, it returns [ERROR\_WINHTTP\_INVALID\_URL](error-messages.md).</span></span> <span data-ttu-id="941fe-413">Standardmäßig ist diese Option deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="941fe-413">This option is turned off by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-414"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**\_ANFORDERUNGSPRIORITÄT DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-414"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-415">Diese Option ist veraltet. sie hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="941fe-415">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-416"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP \_ OPTION \_ REQUEST \_ STATS**</span><span class="sxs-lookup"><span data-stu-id="941fe-416"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP\_OPTION\_REQUEST\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-417">Erstellt Statistiken für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="941fe-417">Retreives statistics for the request.</span></span>  <span data-ttu-id="941fe-418">Eine Liste der verfügbaren Statistiken finden Sie unter [**WINHTTP \_ REQUEST \_ STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span><span class="sxs-lookup"><span data-stu-id="941fe-418">For a list of the available statistics, see [**WINHTTP\_REQUEST\_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-419"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**ANFORDERUNGSZEITEN DER \_ WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-419"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP\_OPTION\_REQUEST\_TIMES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-420">Retreives-Zeitsteuerungsinformationen für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="941fe-420">Retreives timing information for the request.</span></span> <span data-ttu-id="941fe-421">Eine Liste der verfügbaren Zeitangaben finden Sie unter [**WINHTTP \_ REQUEST \_ TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span><span class="sxs-lookup"><span data-stu-id="941fe-421">For a list of the available timings, see [**WINHTTP\_REQUEST\_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-422"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**WINHTTP \_ OPTION \_ REQUIRE \_ STREAM \_ END**</span><span class="sxs-lookup"><span data-stu-id="941fe-422"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**WINHTTP\_OPTION\_REQUIRE\_STREAM\_END**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="941fe-423">Diese Option weist WinHttp an, "Content-Length"-Antwortheader zu ignorieren und den Empfang in einem Stream fortzusetzen, bis das flag END_STREAM empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="941fe-423">This option tells WinHttp to ignore "Content-Length" response headers, and continue receiving on a stream until the END_STREAM flag is received.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-424"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**WINHTTP \_ OPTION \_ RESOLUTION \_ HOSTNAME**</span><span class="sxs-lookup"><span data-stu-id="941fe-424"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="941fe-425">Diese Option kann für ein WinHttp-Anforderungshandle festgelegt werden, bevor es gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="941fe-425">This option can be set on a WinHttp request handle before it has been sent.</span></span> <span data-ttu-id="941fe-426">Wenn diese Einstellung festgelegt ist, verwendet WinHttp die vom Aufrufer bereitgestellte Zeichenfolge als Hostnamen für die DNS-Auflösung.</span><span class="sxs-lookup"><span data-stu-id="941fe-426">If set, WinHttp will use the caller-provided string as the hostname for DNS resolution.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-427"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**TIMEOUT FÜR AUFLÖSUNG DER \_ WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-427"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP\_OPTION\_RESOLVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-428">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, um einen Hostnamen aufzulösen, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="941fe-428">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to resolve a host name.</span></span> <span data-ttu-id="941fe-429">Der Standardtimeoutwert ist **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="941fe-429">The default timeout value is **INFINITE**.</span></span> <span data-ttu-id="941fe-430">Wenn ein nicht standardmäßiger Wert angegeben wird, fällt ein Threaderstellungsaufwand pro Namensauflösung an.</span><span class="sxs-lookup"><span data-stu-id="941fe-430">If a non-default value is specified, there is an overhead of one thread-creation per name resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-431"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**SICHERE \_ WINHTTP-OPTION \_ \_ – PROTOKOLLE**</span><span class="sxs-lookup"><span data-stu-id="941fe-431"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP\_OPTION\_SECURE\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-432">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, welche sicheren Protokolle akzeptabel sind.</span><span class="sxs-lookup"><span data-stu-id="941fe-432">Sets an unsigned long integer value that specifies which secure protocols are acceptable.</span></span> <span data-ttu-id="941fe-433">Standardmäßig sind nur SSL3 und TLS1 in Windows 7 und Windows 8 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="941fe-433">By default only SSL3 and TLS1 are enabled in Windows 7 and Windows 8.</span></span> <span data-ttu-id="941fe-434">Standardmäßig sind nur SSL3, TLS1.0, TLS1.1 und TLS1.2 in Windows 8.1 und Windows 10 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="941fe-434">By default only SSL3, TLS1.0, TLS1.1, and TLS1.2 are enabled in Windows 8.1 and Windows 10.</span></span> <span data-ttu-id="941fe-435">Der Wert kann eine Kombination aus einem oder mehreren der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="941fe-435">The value can be a combination of one or more of the following values.</span></span>

| <span data-ttu-id="941fe-436">Begriff</span><span class="sxs-lookup"><span data-stu-id="941fe-436">Term</span></span> | <span data-ttu-id="941fe-437">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="941fe-437">Description</span></span> |
|-|-|
| <span data-ttu-id="941fe-438"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>\_WINHTTP-FLAG \_ SECURE PROTOCOL \_ \_ ALL</span><span class="sxs-lookup"><span data-stu-id="941fe-438"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_ALL</span></span> | <span data-ttu-id="941fe-439">Die Protokolle Secure Sockets Layer (SSL) 2.0, SSL 3.0 und Transport Layer Security (TLS) 1.0 können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-439">The Secure Sockets Layer (SSL) 2.0, SSL 3.0, and Transport Layer Security (TLS) 1.0 protocols can be used.</span></span> |
| <span data-ttu-id="941fe-440"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>\_WINHTTP-FLAG \_ SECURE PROTOCOL \_ \_ SSL2</span><span class="sxs-lookup"><span data-stu-id="941fe-440"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL2</span></span> | <span data-ttu-id="941fe-441">Das SSL 2.0-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-441">The SSL 2.0 protocol can be used.</span></span> |
| <span data-ttu-id="941fe-442"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ SSL3</span><span class="sxs-lookup"><span data-stu-id="941fe-442"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL3</span></span> | <span data-ttu-id="941fe-443">Das SSL 3.0-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-443">The SSL 3.0 protocol can be used.</span></span> |
| <span data-ttu-id="941fe-444"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ TLS1</span><span class="sxs-lookup"><span data-stu-id="941fe-444"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1</span></span> | <span data-ttu-id="941fe-445">Das TLS 1.0-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-445">The TLS 1.0 protocol can be used.</span></span> |
| <span data-ttu-id="941fe-446"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>\_WINHTTP-FLAG \_ SECURE PROTOCOL \_ \_ TLS1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="941fe-446"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_1</span></span> | <span data-ttu-id="941fe-447">Das TLS 1.1-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-447">The TLS 1.1 protocol can be used.</span></span> |
| <span data-ttu-id="941fe-448"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>\_WINHTTP-FLAG \_ SECURE PROTOCOL \_ \_ TLS1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="941fe-448"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_2</span></span> | <span data-ttu-id="941fe-449">Das TLS 1.2-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-449">The TLS 1.2 protocol can be used.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="941fe-450"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP \_ OPTION \_ SECURITY \_ CERTIFICATE \_ STRUCT**</span><span class="sxs-lookup"><span data-stu-id="941fe-450"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-451">Ruft das Zertifikat für einen SSL/TLS-Server in die [**WINHTTP \_ CERTIFICATE \_ INFO-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) ab.</span><span class="sxs-lookup"><span data-stu-id="941fe-451">Retrieves the certificate for a SSL/TLS server into the [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="941fe-452">Die Anwendung muss die Member **lpszSubjectInfo** und **lpszIssuerInfo** mit [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)freigeben.</span><span class="sxs-lookup"><span data-stu-id="941fe-452">The application must free the **lpszSubjectInfo** and **lpszIssuerInfo** members with [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-453"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**SICHERHEITSFLAGS DER WINHTTP-OPTION \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-453"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-454">Legt einen ganzzahligen Wert ohne Vorzeichen fest oder ruft diesen ab, der die Sicherheitsflags für ein Handle enthält.</span><span class="sxs-lookup"><span data-stu-id="941fe-454">Sets or retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="941fe-455">Dies kann eine Kombination dieser Werte sein:</span><span class="sxs-lookup"><span data-stu-id="941fe-455">It can be a combination of these values:</span></span>

| <span data-ttu-id="941fe-456">Begriff</span><span class="sxs-lookup"><span data-stu-id="941fe-456">Term</span></span> | <span data-ttu-id="941fe-457">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="941fe-457">Description</span></span> |
|-|-|
| <span data-ttu-id="941fe-458"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>\_SICHERHEITSFLAG \_ \_ CERT \_ CN \_ UNGÜLTIG IGNORIEREN</span><span class="sxs-lookup"><span data-stu-id="941fe-458"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span> |<span data-ttu-id="941fe-459">Lässt einen ungültigen allgemeinen Namen in einem Zertifikat zu. Das heißt, der von der Anwendung angegebene Servername stimmt nicht mit dem allgemeinen Namen im Zertifikat überein.</span><span class="sxs-lookup"><span data-stu-id="941fe-459">Allows an invalid common name in a certificate; that is, the server name specified by the application does not match the common name in the certificate.</span></span> <span data-ttu-id="941fe-460">Wenn dieses Flag festgelegt ist, erhält die Anwendung keinen **WINHTTP \_ CALLBACK \_ STATUS FLAG \_ \_ CERT \_ CN \_ INVALID-Rückruf.**</span><span class="sxs-lookup"><span data-stu-id="941fe-460">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_CN\_INVALID** callback.</span></span> |
| <span data-ttu-id="941fe-461"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>\_SICHERHEITSFLAG \_ IGNORE \_ CERT DATE \_ \_ INVALID</span><span class="sxs-lookup"><span data-stu-id="941fe-461"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span> |<span data-ttu-id="941fe-462">Lässt ein ungültiges Zertifikatdatum zu, d. h. ein abgelaufenes oder noch nicht gültiges Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="941fe-462">Allows an invalid certificate date, that is, an expired or not-yet-effective certificate.</span></span> <span data-ttu-id="941fe-463">Wenn dieses Flag festgelegt ist, erhält die Anwendung keinen **WINHTTP \_ CALLBACK \_ STATUS FLAG \_ \_ CERT DATE \_ \_ INVALID-Rückruf.**</span><span class="sxs-lookup"><span data-stu-id="941fe-463">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_DATE\_INVALID** callback.</span></span> |
| <span data-ttu-id="941fe-464"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>\_SICHERHEITSFLAG \_ UNBEKANNTE \_ \_ ZERTIFIZIERUNGSSTELLE IGNORIEREN</span><span class="sxs-lookup"><span data-stu-id="941fe-464"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span> | <span data-ttu-id="941fe-465">Lässt eine ungültige Zertifizierungsstelle zu.</span><span class="sxs-lookup"><span data-stu-id="941fe-465">Allows an invalid certificate authority.</span></span> <span data-ttu-id="941fe-466">Wenn dieses Flag festgelegt ist, erhält die Anwendung keinen **WINHTTP \_ CALLBACK \_ STATUS FLAG \_ INVALID \_ \_ CA-Rückruf.**</span><span class="sxs-lookup"><span data-stu-id="941fe-466">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_INVALID\_CA** callback.</span></span> |
| <span data-ttu-id="941fe-467"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>\_SICHERHEITSFLAG: \_ FALSCHE VERWENDUNG DES \_ ZERTIFIKATS IGNORIEREN \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-467"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_CERT\_WRONG\_USAGE</span></span> | <span data-ttu-id="941fe-468">Ermöglicht die Einrichtung der Identität eines Servers mit einem Nicht-Serverzertifikat (z. B. einem Clientzertifikat).</span><span class="sxs-lookup"><span data-stu-id="941fe-468">Allows the identity of a server to be established with a non-server certificate (for example, a client certificate).</span></span> |
| <span data-ttu-id="941fe-469"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>\_SICHERHEITSFLAG: \_ SCHWACHE SIGNATUR IGNORIEREN \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-469"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span> | <span data-ttu-id="941fe-470">Lässt zu, dass eine schwache Signatur ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="941fe-470">Allows a weak signature to be ignored.</span></span><br/><span data-ttu-id="941fe-471">Dieses Flag ist im Rollupupdate für jedes Betriebssystem ab Windows 7 und Windows Server 2008 R2 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="941fe-471">This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.</span></span> |
| <span data-ttu-id="941fe-472"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>\_SICHERHEITSFLAG \_ "SICHER"</span><span class="sxs-lookup"><span data-stu-id="941fe-472"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span> | <span data-ttu-id="941fe-473">Verwendet sichere Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="941fe-473">Uses secure transfers.</span></span> <span data-ttu-id="941fe-474">Dies wird nur in einem Aufruf von [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="941fe-474">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="941fe-475"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>\_SICHERHEITSFLAGSTÄRKE \_ \_ MITTEL</span><span class="sxs-lookup"><span data-stu-id="941fe-475"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span> | <span data-ttu-id="941fe-476">Verwendet mittlere (56-Bit)-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="941fe-476">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="941fe-477">Dies wird nur in einem Aufruf von [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="941fe-477">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="941fe-478"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>\_SICHERHEITSFLAGSTÄRKE \_ \_ STARK</span><span class="sxs-lookup"><span data-stu-id="941fe-478"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span> | <span data-ttu-id="941fe-479">Verwendet eine starke (128-Bit)-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="941fe-479">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="941fe-480">Dies wird nur in einem Aufruf von [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="941fe-480">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="941fe-481"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>\_SICHERHEITSFLAGSTÄRKE \_ \_ SCHWACH</span><span class="sxs-lookup"><span data-stu-id="941fe-481"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span> | <span data-ttu-id="941fe-482">Verwendet schwache (40-Bit)-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="941fe-482">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="941fe-483">Dies wird nur in einem Aufruf von [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="941fe-483">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="941fe-484"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**SICHERHEITSINFORMATIONEN ZUR WINHTTP-OPTION \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-484"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP\_OPTION\_SECURITY\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-485">Retreives the SChannel connection and cipher information for a request. (Retreives die SChannel-Verbindung und Verschlüsselungsinformationen für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="941fe-485">Retreives the SChannel connection and cipher information for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-486"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP \_ OPTION \_ SECURITY \_ KEY \_ BITNESS**</span><span class="sxs-lookup"><span data-stu-id="941fe-486"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-487">Ruft einen ganzzahligen Wert ohne Vorzeichen ab, der die Verschlüsselungsstärke des Verschlüsselungsschlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="941fe-487">Retrieves an unsigned long integer value that contains the cipher strength of the encryption key.</span></span> <span data-ttu-id="941fe-488">Eine größere Zahl weist auf eine stärkere Verschlüsselung der Verschlüsselungsstärke hin.</span><span class="sxs-lookup"><span data-stu-id="941fe-488">A larger number indicates stronger cipher strength encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-489"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP \_ OPTION \_ SEND \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="941fe-489"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-490">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, um eine Anforderung zu senden oder Daten zu schreiben, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="941fe-490">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to send a request or write some data.</span></span> <span data-ttu-id="941fe-491">Wenn das Senden der Anforderung länger als das Timeout dauert, wird der Sendevorgang abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="941fe-491">If sending the request takes longer than the timeout, the send operation is canceled.</span></span> <span data-ttu-id="941fe-492">Der Standardzeitraum bis zum Timeout beträgt 30 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="941fe-492">The default timeout is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-493"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP \_ OPTION \_ SERVER \_ CBT**</span><span class="sxs-lookup"><span data-stu-id="941fe-493"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP\_OPTION\_SERVER\_CBT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-494">Ruft einen Zeiger auf die [**SecPkgContext-Bindungsstruktur \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) ab, die ein Channel Binding Token (CBT) angibt.</span><span class="sxs-lookup"><span data-stu-id="941fe-494">Gets a pointer to [**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) structure that specifies a Channel Binding Token (CBT).</span></span>

<span data-ttu-id="941fe-495">Ein Kanalbindungstoken ist eine Eigenschaft eines sicheren Transportkanals und wird verwendet, um einen Authentifizierungskanal an den sicheren Transportkanal zu binden.</span><span class="sxs-lookup"><span data-stu-id="941fe-495">A Channel Binding Token is a property of a secure transport channel and is used to bind an authentication channel to the secure transport channel.</span></span> <span data-ttu-id="941fe-496">Dieses Token kann von dieser Option erst abgerufen werden, nachdem eine SSL-Verbindung hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="941fe-496">This token can only be obtained by this option after an SSL connection has been established.</span></span>

> [!Note]
> <span data-ttu-id="941fe-497">Wenn Sie diese Option und einen **NULL-Wert** für *lpBuffer* an [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) übergeben, werden ERROR \_ INSUFFICIENT BUFFER und die erforderliche \_ Bytegröße für den Puffer im *lpdwBufferLength-Parameter* zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="941fe-497">Passing this option and a **null** value for *lpBuffer* to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) will return ERROR\_INSUFFICIENT\_BUFFER and the required byte size for the buffer in the *lpdwBufferLength* parameter.</span></span> <span data-ttu-id="941fe-498">Dieser zurückgegebene Puffergrößenwert kann in einem nachfolgenden Aufruf zur Abfrage des Kanalbindungstokens übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-498">This returned buffer size value can be passed in a subsequent call to query for the Channel Binding Token.</span></span> <span data-ttu-id="941fe-499">Diese Schritte sind bei der Behandlung von WINHTTP \_ CALLBACK \_ STATUS REQUEST \_ erforderlich, wenn Sie Anforderungsheader basierend auf dem Kanalbindungstoken ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="941fe-499">These steps are necessary when handling WINHTTP\_CALLBACK\_STATUS\_REQUEST if you want to modify request headers based on the Channel Binding Token.</span></span> <span data-ttu-id="941fe-500">Beachten Sie, dass Windows XP und Vista das Ändern von Anforderungsheadern während dieses Rückrufs nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="941fe-500">Note that Windows XP and Vista do not support modifying request headers during this callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-501"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CHAIN \_ CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="941fe-501"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-502">Ruft den Kontext der Serverzertifizierungskette ab.</span><span class="sxs-lookup"><span data-stu-id="941fe-502">Retrieves the server certification chain context.</span></span> <span data-ttu-id="941fe-503">**WINHTTP \_ OPTION \_ SERVER \_ CERT CHAIN \_ \_ CONTEXT** kann übergeben werden, um einen duplizierten Zeiger auf den **CERT CHAIN \_ \_ CONTEXT** für eine Serverzertifikatkette abzurufen, die während einer ausgehandelten SSL-Verbindung empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="941fe-503">**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT** can be passed to obtain a duplicated pointer to the **CERT\_CHAIN\_CONTEXT** for a server certificate chain received during a negotiated SSL connection.</span></span> <span data-ttu-id="941fe-504">Der Client muss [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) für den zurückgegebenen PCCERT \_ CONTEXT-Zeiger aufrufen, der in den Puffer gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="941fe-504">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-505"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="941fe-505"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-506">Ruft den Serverzertifizierungskontext ab.</span><span class="sxs-lookup"><span data-stu-id="941fe-506">Retrieves the server certification context.</span></span> <span data-ttu-id="941fe-507">**WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CONTEXT** kann übergeben werden, um einen duplizierten Zeiger auf den [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) für ein Serverzertifikat abzurufen, das während einer ausgehandelten SSL-Verbindung empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="941fe-507">**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT** can be passed to obtain a duplicated pointer to the [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) for a server certificate received during a negotiated SSL connection.</span></span> <span data-ttu-id="941fe-508">Der Client muss [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) für den zurückgegebenen PCCERT \_ CONTEXT-Zeiger aufrufen, der in den Puffer gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="941fe-508">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-509"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**VERWENDETER \_ \_ WINHTTP-OPTIONSERVER-SPN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-509"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WINHTTP\_OPTION\_SERVER\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-510">Ruft den Serverprinzipalnamen ab, den WinHTTP während der Authentifizierung für SSPI bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="941fe-510">Gets the server Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="941fe-511">Dieser Zeichenfolgenwert kann nach einem Authentifizierungsfehler an [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-511">This string value can be passed to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-512"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP \_ OPTION \_ SPN**</span><span class="sxs-lookup"><span data-stu-id="941fe-512"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP\_OPTION\_SPN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-513">Schließt die Serverportnummer ein oder entfernt sie, wenn der SPN (Dienstprinzipalname) für die Kerberos- oder Negotiate Kerberos-Authentifizierung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="941fe-513">Includes or removes the server port number when the SPN (service principal name) is built for Kerberos or Negotiate Kerberos authentication.</span></span> <span data-ttu-id="941fe-514">Dieses Flag ist einer der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="941fe-514">This flag is one of the following values:</span></span>

| <span data-ttu-id="941fe-515">Begriff</span><span class="sxs-lookup"><span data-stu-id="941fe-515">Term</span></span> | <span data-ttu-id="941fe-516">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="941fe-516">Description</span></span> |
|-|-|
| <span data-ttu-id="941fe-517"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ \_ \_ SPN-SERVERPORT DEAKTIVIEREN \_</span><span class="sxs-lookup"><span data-stu-id="941fe-517"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP\_DISABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="941fe-518">Entfernt die Serverportnummer.</span><span class="sxs-lookup"><span data-stu-id="941fe-518">Removes the server port number.</span></span> |
| <span data-ttu-id="941fe-519"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP \_ \_ \_ SPN-SERVERPORT AKTIVIEREN \_</span><span class="sxs-lookup"><span data-stu-id="941fe-519"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP\_ENABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="941fe-520">Enthält die Serverportnummer.</span><span class="sxs-lookup"><span data-stu-id="941fe-520">Includes the server port number.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="941fe-521"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**WINHTTP \_ OPTION \_ STREAM \_ ERROR \_ CODE**</span><span class="sxs-lookup"><span data-stu-id="941fe-521"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**WINHTTP\_OPTION\_STREAM\_ERROR\_CODE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="941fe-522">Diese Option kann für ein WinHttp-Anforderungshandle abgefragt werden und gibt den Fehlercode zurück, der durch einen RST_STREAM Frame angegeben wird, der in einem HTTP-Stream empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="941fe-522">This option can be queried on a WinHttp request handle, and will return the error code indicated by a RST_STREAM frame received on an HTTP stream.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-523"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP \_ OPTION \_ TCP \_ FAST \_ OPEN**</span><span class="sxs-lookup"><span data-stu-id="941fe-523"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP\_OPTION\_TCP\_FAST\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-524">Aktiviert TCP Fast Open für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="941fe-524">Enables TCP Fast Open for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-525"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**\_WINHTTP-OPTION \_ TCP \_ KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="941fe-525"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**WINHTTP\_OPTION\_TCP\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-526">Diese Option kann für ein WinHttp-Sitzungshandle festgelegt werden, um das TCP-Keep-Alive-Verhalten für den zugrunde liegenden Socket zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="941fe-526">This option can be set on a WinHttp session handle to enable TCP keep-alive behavior on the underlying socket.</span></span> <span data-ttu-id="941fe-527">Übernimmt eine [**\_ tcp-Keepalive-Struktur.**](/windows/win32/winsock/sio-keepalive-vals)</span><span class="sxs-lookup"><span data-stu-id="941fe-527">Takes a [**tcp\_keepalive**](/windows/win32/winsock/sio-keepalive-vals) struct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-528"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP \_ OPTION \_ TLS \_ FALSE \_ START**</span><span class="sxs-lookup"><span data-stu-id="941fe-528"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP\_OPTION\_TLS\_FALSE\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-529">Aktiviert TLS False Start für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="941fe-529">Enables TLS False Start for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-530"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**WINHTTP \_ OPTION \_ TLS \_ PROTOCOL \_ INSECURE \_ FALLBACK**</span><span class="sxs-lookup"><span data-stu-id="941fe-530"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-531">Diese Option kann für ein WinHttp-Sitzungshandle festgelegt werden, um zu steuern, ob ein Fallback auf TLS 1.0 zulässig ist, wenn ein TLS-Handshakefehler mit einer neueren Protokollversion vorliegt.</span><span class="sxs-lookup"><span data-stu-id="941fe-531">This option can be set on a WinHttp session handle to control whether fallback to TLS 1.0 is allowed if there is a TLS handshake failure with a newer protocol version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-532"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP \_ OPTION \_ UNLOAD \_ NOTIFY \_ EVENT**</span><span class="sxs-lookup"><span data-stu-id="941fe-532"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-533">Nimmt ein Ereignis an, das festgelegt wird, wenn der letzte Rückruf für eine bestimmte Sitzung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="941fe-533">Takes an event that will be set when the last callback has completed for a particular session.</span></span> <span data-ttu-id="941fe-534">Dieses Flag muss für ein Sitzungshandle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-534">This flag must be must be used on a session handle.</span></span> <span data-ttu-id="941fe-535">Das Ereignis kann erst geschlossen werden, nachdem es von WinHTTP festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="941fe-535">The event cannot be closed until after it has been set by WinHTTP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-536"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP \_ OPTION \_ UNSAFE \_ HEADER \_ PARSING**</span><span class="sxs-lookup"><span data-stu-id="941fe-536"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-537">Diese Option ist für die interne Verwendung reserviert und sollte nicht aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-537">This option is reserved for internal use and should not be called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-538"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**UPGRADE DER \_ WINHTTP-OPTION \_ AUF \_ \_ \_ WEBSOCKET**</span><span class="sxs-lookup"><span data-stu-id="941fe-538"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-539">Weist den Stapel an, einen WebSocket-Handshakeprozess mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)zu starten.</span><span class="sxs-lookup"><span data-stu-id="941fe-539">Instructs the stack to start a WebSocket handshake process with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="941fe-540">Diese Option nimmt keine Parameter an.</span><span class="sxs-lookup"><span data-stu-id="941fe-540">This option takes no parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-541"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**\_ \_ WINHTTP-OPTIONS-URL**</span><span class="sxs-lookup"><span data-stu-id="941fe-541"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-542">Ruft einen Zeichenfolgenwert ab, der die vollständige URL einer heruntergeladenen Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="941fe-542">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="941fe-543">Wenn die ursprüngliche URL zusätzliche Daten enthielt, z. B. Suchzeichenfolgen oder Anker, oder wenn der Aufruf umgeleitet wurde, unterscheidet sich die zurückgegebene URL vom ursprünglichen.</span><span class="sxs-lookup"><span data-stu-id="941fe-543">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="941fe-544">Die Anwendung sollte einen Puffer in Bytes übergeben, der groß genug ist, um die zurückgegebene URL in wide char zu speichern.</span><span class="sxs-lookup"><span data-stu-id="941fe-544">The application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-545"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**\_WINHTTP-OPTION \_ VERWENDEN VON \_ \_ ANMELDEINFORMATIONEN FÜR GLOBALEN SERVER \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-545"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-546">Übernimmt eine **BOOL** und kann nur ein Sitzungshandle festlegen.</span><span class="sxs-lookup"><span data-stu-id="941fe-546">Takes a **BOOL** and can be set only a session handle.</span></span> <span data-ttu-id="941fe-547">Er wird nur an Handles weiter gegeben, die aus dem Sitzungshandle erstellt wurden, nachdem die Option festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="941fe-547">It will only propagate down to handles created from the session handle after the option has been set.</span></span> <span data-ttu-id="941fe-548">True gibt an, dass diese Option als letzte Möglichkeit die Verwendung globaler Serveranmeldeinformationen bewirkt, die von WinInet gepusht wurden.</span><span class="sxs-lookup"><span data-stu-id="941fe-548">If **TRUE**, this option causes as a last resort the use of global server credentials that were pushed down from WinInet.</span></span> <span data-ttu-id="941fe-549">Der Standardwert für diese Option ist **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="941fe-549">The default for this option is **FALSE**.</span></span> <span data-ttu-id="941fe-550">Diese Option erfordert den Registrierungsschlüssel **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="941fe-550">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="941fe-551">Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="941fe-551">This registry key is not present by default.</span></span> <span data-ttu-id="941fe-552">Wenn sie festgelegt ist, sendet WinINet Anmeldeinformationen an WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="941fe-552">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="941fe-553">Wenn WinHttp eine Authentifizierungsaufforderung erhält und keine Anmeldeinformationen für das aktuelle Handle festgelegt sind, werden die von WinINet bereitgestellten Anmeldeinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="941fe-553">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-554"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP \_ OPTION \_ USER \_ AGENT**</span><span class="sxs-lookup"><span data-stu-id="941fe-554"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-555">Legt die Zeichenfolge des [*Benutzer-Agents*](glossary.md) auf Handles fest, die von [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) bereitgestellt und in nachfolgenden [**WinHttpSendRequest-Funktionen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) verwendet werden, oder ruft sie ab, solange sie nicht durch einen header überschrieben wird, der von [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) oder **WinHttpSendRequest** hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="941fe-555">Sets or retrieves the [*user agent*](glossary.md) string on handles supplied by [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) and used in subsequent [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) functions, as long as it is not overridden by a header added by [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) or **WinHttpSendRequest**.</span></span> <span data-ttu-id="941fe-556">Beim Abrufen eines Benutzer-Agents sollte die Anwendung einen Puffer in Bytes übergeben, der groß genug ist, um die zurückgegebene URL in wide char zu speichern.</span><span class="sxs-lookup"><span data-stu-id="941fe-556">When retrieving a user agent, the application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span> <span data-ttu-id="941fe-557">Beim Festlegen des Benutzer-Agents entspricht die Puffergröße der Länge der Zeichenfolge in Zeichen sowie dem **NULL-Abschlusszeichen.**</span><span class="sxs-lookup"><span data-stu-id="941fe-557">When setting the user agent, the buffer size is the length of the string, in characters, plus the **NULL** terminator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-558"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP \_ OPTION \_ USERNAME**</span><span class="sxs-lookup"><span data-stu-id="941fe-558"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-559">Legt eine Zeichenfolge fest, die den Benutzernamen enthält, oder ruft sie ab.</span><span class="sxs-lookup"><span data-stu-id="941fe-559">Sets or retrieves a string that contains the user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-560"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ CLOSE \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="941fe-560"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-561">Legt die Zeit in Millisekunden fest, die [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) auf den Abschluss des schließenden Handshakes warten soll.</span><span class="sxs-lookup"><span data-stu-id="941fe-561">Sets the time, in milliseconds, that [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) should wait to complete the close handshake.</span></span> <span data-ttu-id="941fe-562">Die Standardeinstellung beträgt 10 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="941fe-562">The default is 10 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-563"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ KEEPALIVE \_ INTERVAL**</span><span class="sxs-lookup"><span data-stu-id="941fe-563"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-564">Legt das Intervall in Millisekunden fest, um ein Keep-Alive-Paket über die Verbindung zu senden.</span><span class="sxs-lookup"><span data-stu-id="941fe-564">Sets the interval, in milliseconds, to send a keep-alive packet over the connection.</span></span> <span data-ttu-id="941fe-565">Das Standardintervall ist 30000 (30 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="941fe-565">The default interval is 30000 (30 seconds).</span></span> <span data-ttu-id="941fe-566">Das Mindestintervall beträgt 15.000 (15 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="941fe-566">The minimum interval is 15000 (15 seconds).</span></span> <span data-ttu-id="941fe-567">Wenn [**Sie WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) verwenden, um einen Wert unter 15000 festzulegen, wird mit **ERROR INVALID \_ \_ PARAMETER** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="941fe-567">Using [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to set a value lower than 15000 will return with **ERROR\_INVALID\_PARAMETER**.</span></span>

> [!Note]
> <span data-ttu-id="941fe-568">Der Standardwert für **WINHTTP \_ OPTION WEB SOCKET \_ \_ \_ KEEPALIVE \_ INTERVAL** wird aus **HKLM: \\ SOFTWARE Microsoft \\ \\ WebSocket \\ KeepaliveInterval** gelesen.</span><span class="sxs-lookup"><span data-stu-id="941fe-568">The default value for **WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL** is read from **HKLM:\\SOFTWARE\\Microsoft\\WebSocket\\KeepaliveInterval**.</span></span> <span data-ttu-id="941fe-569">Wenn kein Wert festgelegt ist, wird der Standardwert 30000 verwendet.</span><span class="sxs-lookup"><span data-stu-id="941fe-569">If a value is not set, the default value of 30000 will be used.</span></span> <span data-ttu-id="941fe-570">Es ist nicht möglich, ein niedrigeres Keepalive-Intervall als 15.000 Millisekunden zu haben.</span><span class="sxs-lookup"><span data-stu-id="941fe-570">It is not possible to have a lower keepalive interval than 15000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-571"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ RECEIVE \_ BUFFER \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="941fe-571"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-572">Legt ein DWORD fest oder ruft es ab, das die Empfangspuffergröße angibt, die für WebSocket-Verbindungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="941fe-572">Sets or retrieves a DWORD which specifies the receive buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-573"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ SEND \_ BUFFER \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="941fe-573"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-574">Legt ein DWORD fest oder ruft es ab, das die Sendepuffergröße angibt, die für WebSocket-Verbindungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="941fe-574">Sets or retrieves a DWORD which specifies the send buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-575"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**ANZAHL VON \_ \_ WINHTTP-OPTION-WORKERTHREADS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-575"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-576">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Anzahl der Arbeitsthreads angibt, die der Threadpool für asynchrone Vervollständigungen verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="941fe-576">Sets an unsigned long integer value that specifies the number of worker threads the thread pool should use for asynchronous completions.</span></span> <span data-ttu-id="941fe-577">Der Standardwert dieser Option ist 0 (null), was angibt, dass die Anzahl der Arbeitsthreads der Anzahl der CPUs im System entspricht.</span><span class="sxs-lookup"><span data-stu-id="941fe-577">The default value of this option is zero, which specifies that the number of worker threads is equal to the number of CPUs on the system.</span></span> <span data-ttu-id="941fe-578">Diese Option kann nur für ein **NULL**  [HINTERNET-Handle](hinternet-handles-in-winhttp.md) festgelegt werden, bevor ein asynchroner Vorgang aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="941fe-578">This option can only be set on a **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) handle before an asynchronous operation has occurred.</span></span> <span data-ttu-id="941fe-579">Diese Option kann nur einmal festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="941fe-579">This option can only be set once.</span></span>

<span data-ttu-id="941fe-580">**Windows Server 2008 R2 und Windows 7:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="941fe-580">**Windows Server 2008 R2 and Windows 7:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="941fe-581"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP \_ OPTION \_ WRITE \_ BUFFER \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="941fe-581"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="941fe-582">Diese Option ist veraltet. sie hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="941fe-582">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="941fe-583">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="941fe-583">Remarks</span></span>

<span data-ttu-id="941fe-584">In der folgenden Tabelle werden die Optionsflags aufgelistet, indem angegeben wird, auf welche Handles sie reagieren können, ob sie abgefragt und festgelegt werden können und welcher Datentyp verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="941fe-584">The following table lists the option flags by specifying which handles they can act upon, whether they can be queried and set, and the data type used.</span></span> <span data-ttu-id="941fe-585">Ein "X" gibt an, dass das Optionsflag für die Verwendung mit der Funktion oder dem Handle gültig ist, während ein "-" angibt, dass das Optionsflag ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="941fe-585">An "X" indicates that the option flag is valid for use with the function or handle, while a "-" specifies that the option flag is invalid.</span></span>

<span data-ttu-id="941fe-586">Der Versuch, ein Optionsflag für eine Windows-Version festzulegen oder abzufragen, bei der es nicht unterstützt wird, führt zu **ERROR \_ WINHTTP \_ INVALID \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="941fe-586">Attempting to set or query an option flag on a Windows version where it is not supported will result in **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span>

| <span data-ttu-id="941fe-587">Optionsflag und Datentyp</span><span class="sxs-lookup"><span data-stu-id="941fe-587">Option flag, and data type</span></span> | <span data-ttu-id="941fe-588">Sitzungshandle</span><span class="sxs-lookup"><span data-stu-id="941fe-588">Session handle</span></span> | <span data-ttu-id="941fe-589">Anforderungshandle</span><span class="sxs-lookup"><span data-stu-id="941fe-589">Request handle</span></span> | <span data-ttu-id="941fe-590">Abfrageoption</span><span class="sxs-lookup"><span data-stu-id="941fe-590">Query option</span></span> | <span data-ttu-id="941fe-591">SET-Option</span><span class="sxs-lookup"><span data-stu-id="941fe-591">Set option</span></span> | <span data-ttu-id="941fe-592">Windows-Mindestversion</span><span class="sxs-lookup"><span data-stu-id="941fe-592">Minimum Windows Version</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="941fe-593">\_WINHTTP-OPTION \_ GARANTIERT NICHT \_ \_ BLOCKIERENDE \_ RÜCKRUFE</span><span class="sxs-lookup"><span data-stu-id="941fe-593">WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS</span></span><br/><span data-ttu-id="941fe-594">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-594">**BOOL**</span></span> | <span data-ttu-id="941fe-595">X</span><span class="sxs-lookup"><span data-stu-id="941fe-595">X</span></span> | \- | \- | <span data-ttu-id="941fe-596">X</span><span class="sxs-lookup"><span data-stu-id="941fe-596">X</span></span> | \- |
| <span data-ttu-id="941fe-597">WINHTTP \_ OPTION \_ AUTOLOGON \_ POLICY</span><span class="sxs-lookup"><span data-stu-id="941fe-597">WINHTTP\_OPTION\_AUTOLOGON\_POLICY</span></span><br/><span data-ttu-id="941fe-598">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-598">**DWORD**</span></span> | \- | <span data-ttu-id="941fe-599">X</span><span class="sxs-lookup"><span data-stu-id="941fe-599">X</span></span> | \- | <span data-ttu-id="941fe-600">X</span><span class="sxs-lookup"><span data-stu-id="941fe-600">X</span></span> | \- |
| <span data-ttu-id="941fe-601">\_WINHTTP-OPTION \_ : \_ HINTERGRUNDVERBINDUNGEN</span><span class="sxs-lookup"><span data-stu-id="941fe-601">WINHTTP\_OPTION\_BACKGROUND\_CONNECTIONS</span></span><br/><span data-ttu-id="941fe-602">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-602">**DWORD**</span></span> | <span data-ttu-id="941fe-603">X</span><span class="sxs-lookup"><span data-stu-id="941fe-603">X</span></span> | \- | \- | <span data-ttu-id="941fe-604">X</span><span class="sxs-lookup"><span data-stu-id="941fe-604">X</span></span> | <span data-ttu-id="941fe-605">Windows 10 Version 21H1</span><span class="sxs-lookup"><span data-stu-id="941fe-605">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="941fe-606">\_ \_ WINHTTP-OPTIONSRÜCKRUF</span><span class="sxs-lookup"><span data-stu-id="941fe-606">WINHTTP\_OPTION\_CALLBACK</span></span><br/><span data-ttu-id="941fe-607">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="941fe-607">**LPVOID**</span></span> | <span data-ttu-id="941fe-608">X</span><span class="sxs-lookup"><span data-stu-id="941fe-608">X</span></span> | <span data-ttu-id="941fe-609">X</span><span class="sxs-lookup"><span data-stu-id="941fe-609">X</span></span> | <span data-ttu-id="941fe-610">X</span><span class="sxs-lookup"><span data-stu-id="941fe-610">X</span></span> | <span data-ttu-id="941fe-611">X</span><span class="sxs-lookup"><span data-stu-id="941fe-611">X</span></span> | \- |
| <span data-ttu-id="941fe-612">WINHTTP \_ OPTION \_ CLIENT \_ CERT \_ CONTEXT</span><span class="sxs-lookup"><span data-stu-id="941fe-612">WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="941fe-613">**\_CERT-KONTEXT**</span><span class="sxs-lookup"><span data-stu-id="941fe-613">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="941fe-614">X</span><span class="sxs-lookup"><span data-stu-id="941fe-614">X</span></span> | \- | <span data-ttu-id="941fe-615">X</span><span class="sxs-lookup"><span data-stu-id="941fe-615">X</span></span> | <span data-ttu-id="941fe-616">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="941fe-616">Windows Vista</span></span> |
| <span data-ttu-id="941fe-617">\_WINHTTP-OPTION \_ \_ CLIENTZERTIFIKATAUSSTELLERLISTE \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-617">WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST</span></span><br/>[<span data-ttu-id="941fe-618">**SecPkgContext \_ IssuerListInfoEx**</span><span class="sxs-lookup"><span data-stu-id="941fe-618">**SecPkgContext\_IssuerListInfoEx**</span></span>](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | <span data-ttu-id="941fe-619">X</span><span class="sxs-lookup"><span data-stu-id="941fe-619">X</span></span> | <span data-ttu-id="941fe-620">X</span><span class="sxs-lookup"><span data-stu-id="941fe-620">X</span></span> | \- | <span data-ttu-id="941fe-621">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="941fe-621">Windows Vista</span></span> |
| <span data-ttu-id="941fe-622">\_ \_ WINHTTP-OPTIONSCODEPAGE</span><span class="sxs-lookup"><span data-stu-id="941fe-622">WINHTTP\_OPTION\_CODEPAGE</span></span><br/><span data-ttu-id="941fe-623">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-623">**DWORD**</span></span> | <span data-ttu-id="941fe-624">X</span><span class="sxs-lookup"><span data-stu-id="941fe-624">X</span></span> | \- | \- | <span data-ttu-id="941fe-625">X</span><span class="sxs-lookup"><span data-stu-id="941fe-625">X</span></span> | \- |
| <span data-ttu-id="941fe-626">\_WINHTTP-OPTION: \_ \_ KONFIGURIEREN DER \_ PASSPORT-AUTHENTIFIZIERUNG</span><span class="sxs-lookup"><span data-stu-id="941fe-626">WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH</span></span><br/><span data-ttu-id="941fe-627">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-627">**DWORD**</span></span> | <span data-ttu-id="941fe-628">X</span><span class="sxs-lookup"><span data-stu-id="941fe-628">X</span></span> | \- | \- | <span data-ttu-id="941fe-629">X</span><span class="sxs-lookup"><span data-stu-id="941fe-629">X</span></span> | \- |
| <span data-ttu-id="941fe-630">\_WINHTTP-OPTION \_ – \_ VERBINDUNGS-RETRIES</span><span class="sxs-lookup"><span data-stu-id="941fe-630">WINHTTP\_OPTION\_CONNECT\_RETRIES</span></span><br/><span data-ttu-id="941fe-631">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-631">**DWORD**</span></span> | <span data-ttu-id="941fe-632">X</span><span class="sxs-lookup"><span data-stu-id="941fe-632">X</span></span> | <span data-ttu-id="941fe-633">X</span><span class="sxs-lookup"><span data-stu-id="941fe-633">X</span></span> | <span data-ttu-id="941fe-634">X</span><span class="sxs-lookup"><span data-stu-id="941fe-634">X</span></span> | <span data-ttu-id="941fe-635">X</span><span class="sxs-lookup"><span data-stu-id="941fe-635">X</span></span> | \- |
| <span data-ttu-id="941fe-636">WINHTTP \_ OPTION \_ CONNECT \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="941fe-636">WINHTTP\_OPTION\_CONNECT\_TIMEOUT</span></span><br/><span data-ttu-id="941fe-637">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-637">**DWORD**</span></span> | <span data-ttu-id="941fe-638">X</span><span class="sxs-lookup"><span data-stu-id="941fe-638">X</span></span> | <span data-ttu-id="941fe-639">X</span><span class="sxs-lookup"><span data-stu-id="941fe-639">X</span></span> | <span data-ttu-id="941fe-640">X</span><span class="sxs-lookup"><span data-stu-id="941fe-640">X</span></span> | <span data-ttu-id="941fe-641">X</span><span class="sxs-lookup"><span data-stu-id="941fe-641">X</span></span> | \- |
| <span data-ttu-id="941fe-642">VERBINDUNGSINFORMATIONEN \_ ZUR WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-642">WINHTTP\_OPTION\_CONNECTION\_INFO</span></span><br/>[<span data-ttu-id="941fe-643">**\_WINHTTP-VERBINDUNGSINFORMATIONEN \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-643">**WINHTTP\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | <span data-ttu-id="941fe-644">X</span><span class="sxs-lookup"><span data-stu-id="941fe-644">X</span></span> | <span data-ttu-id="941fe-645">X</span><span class="sxs-lookup"><span data-stu-id="941fe-645">X</span></span> | \- | \- |
| <span data-ttu-id="941fe-646">WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V0</span><span class="sxs-lookup"><span data-stu-id="941fe-646">WINHTTP\_OPTION\_CONNECTION\_STATS\_V0</span></span><br/>[<span data-ttu-id="941fe-647">**TCP \_ INFO \_ v0**</span><span class="sxs-lookup"><span data-stu-id="941fe-647">**TCP\_INFO\_v0**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | <span data-ttu-id="941fe-648">X</span><span class="sxs-lookup"><span data-stu-id="941fe-648">X</span></span> | <span data-ttu-id="941fe-649">X</span><span class="sxs-lookup"><span data-stu-id="941fe-649">X</span></span> | \- | <span data-ttu-id="941fe-650">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="941fe-650">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="941fe-651">WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1</span><span class="sxs-lookup"><span data-stu-id="941fe-651">WINHTTP\_OPTION\_CONNECTION\_STATS\_V1</span></span><br/>[<span data-ttu-id="941fe-652">**TCP \_ INFO \_ v1**</span><span class="sxs-lookup"><span data-stu-id="941fe-652">**TCP\_INFO\_v1**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | <span data-ttu-id="941fe-653">X</span><span class="sxs-lookup"><span data-stu-id="941fe-653">X</span></span> | <span data-ttu-id="941fe-654">X</span><span class="sxs-lookup"><span data-stu-id="941fe-654">X</span></span> | \- | <span data-ttu-id="941fe-655">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="941fe-655">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="941fe-656">KONTEXTWERT \_ DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-656">WINHTTP\_OPTION\_CONTEXT\_VALUE</span></span><br/><span data-ttu-id="941fe-657">**DWORD \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="941fe-657">**DWORD\_PTR**</span></span> | <span data-ttu-id="941fe-658">X</span><span class="sxs-lookup"><span data-stu-id="941fe-658">X</span></span> | <span data-ttu-id="941fe-659">X</span><span class="sxs-lookup"><span data-stu-id="941fe-659">X</span></span> | <span data-ttu-id="941fe-660">X</span><span class="sxs-lookup"><span data-stu-id="941fe-660">X</span></span> | <span data-ttu-id="941fe-661">X</span><span class="sxs-lookup"><span data-stu-id="941fe-661">X</span></span> | \- |
| <span data-ttu-id="941fe-662">DEKOMPRIMIERUNG \_ DER WINHTTP-OPTION \_</span><span class="sxs-lookup"><span data-stu-id="941fe-662">WINHTTP\_OPTION\_DECOMPRESSION</span></span><br/><span data-ttu-id="941fe-663">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-663">**DWORD**</span></span> | <span data-ttu-id="941fe-664">X</span><span class="sxs-lookup"><span data-stu-id="941fe-664">X</span></span> | <span data-ttu-id="941fe-665">X</span><span class="sxs-lookup"><span data-stu-id="941fe-665">X</span></span> | \- | <span data-ttu-id="941fe-666">X</span><span class="sxs-lookup"><span data-stu-id="941fe-666">X</span></span> | <span data-ttu-id="941fe-667">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="941fe-667">Windows 8.1</span></span> |
| <span data-ttu-id="941fe-668">WINHTTP-OPTION \_ \_ \_ CERT CHAIN \_ BUILDING \_ DEAKTIVIEREN</span><span class="sxs-lookup"><span data-stu-id="941fe-668">WINHTTP\_OPTION\_DISABLE\_CERT\_CHAIN\_BUILDING</span></span><br/><span data-ttu-id="941fe-669">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-669">**BOOL**</span></span> | <span data-ttu-id="941fe-670">X</span><span class="sxs-lookup"><span data-stu-id="941fe-670">X</span></span> | \- | \- | <span data-ttu-id="941fe-671">X</span><span class="sxs-lookup"><span data-stu-id="941fe-671">X</span></span> | <span data-ttu-id="941fe-672">Windows 10 Version 21H1</span><span class="sxs-lookup"><span data-stu-id="941fe-672">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="941fe-673">FUNKTION \_ "WINHTTP-OPTION \_ \_ DEAKTIVIEREN"</span><span class="sxs-lookup"><span data-stu-id="941fe-673">WINHTTP\_OPTION\_DISABLE\_FEATURE</span></span><br/><span data-ttu-id="941fe-674">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-674">**DWORD**</span></span> | \- | <span data-ttu-id="941fe-675">X</span><span class="sxs-lookup"><span data-stu-id="941fe-675">X</span></span> | \- | <span data-ttu-id="941fe-676">X</span><span class="sxs-lookup"><span data-stu-id="941fe-676">X</span></span> | \- |
| <span data-ttu-id="941fe-677">\_WINHTTP-OPTION: \_ DEAKTIVIEREN DES \_ \_ \_ FALLBACKS DES SICHEREN PROTOKOLLS</span><span class="sxs-lookup"><span data-stu-id="941fe-677">WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK</span></span><br/><span data-ttu-id="941fe-678">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-678">**BOOL**</span></span> | <span data-ttu-id="941fe-679">X</span><span class="sxs-lookup"><span data-stu-id="941fe-679">X</span></span> | \- | \- | <span data-ttu-id="941fe-680">X</span><span class="sxs-lookup"><span data-stu-id="941fe-680">X</span></span> | <span data-ttu-id="941fe-681">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="941fe-681">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="941fe-682">WINHTTP-OPTION \_ \_ \_ STREAMWARTESCHLANGE \_ DEAKTIVIEREN</span><span class="sxs-lookup"><span data-stu-id="941fe-682">WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE</span></span><br/><span data-ttu-id="941fe-683">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-683">**BOOL**</span></span> | <span data-ttu-id="941fe-684">X</span><span class="sxs-lookup"><span data-stu-id="941fe-684">X</span></span> | <span data-ttu-id="941fe-685">X</span><span class="sxs-lookup"><span data-stu-id="941fe-685">X</span></span> | \- | <span data-ttu-id="941fe-686">X</span><span class="sxs-lookup"><span data-stu-id="941fe-686">X</span></span> | <span data-ttu-id="941fe-687">Windows 10 Version 1809</span><span class="sxs-lookup"><span data-stu-id="941fe-687">Windows 10 Version 1809</span></span> |
| <span data-ttu-id="941fe-688">FEATURE \_ "WINHTTP-OPTION \_ \_ AKTIVIEREN"</span><span class="sxs-lookup"><span data-stu-id="941fe-688">WINHTTP\_OPTION\_ENABLE\_FEATURE</span></span><br/><span data-ttu-id="941fe-689">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-689">**DWORD**</span></span> | \* | \* | \- | <span data-ttu-id="941fe-690">X</span><span class="sxs-lookup"><span data-stu-id="941fe-690">X</span></span> | \- |
| <span data-ttu-id="941fe-691">WINHTTP-OPTION \_ \_ \_ HTTP-PROTOKOLL \_ AKTIVIEREN</span><span class="sxs-lookup"><span data-stu-id="941fe-691">WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL</span></span><br/><span data-ttu-id="941fe-692">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-692">**DWORD**</span></span> | <span data-ttu-id="941fe-693">X</span><span class="sxs-lookup"><span data-stu-id="941fe-693">X</span></span> | <span data-ttu-id="941fe-694">X</span><span class="sxs-lookup"><span data-stu-id="941fe-694">X</span></span> | \- | <span data-ttu-id="941fe-695">X</span><span class="sxs-lookup"><span data-stu-id="941fe-695">X</span></span> | <span data-ttu-id="941fe-696">Windows 10, Version 1607</span><span class="sxs-lookup"><span data-stu-id="941fe-696">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="941fe-697">\_WINHTTP-OPTION \_ \_ HTTP2 \_ PLUS \_ \_ CLIENTZERTIFIKATKONTEXT \_ AKTIVIEREN</span><span class="sxs-lookup"><span data-stu-id="941fe-697">WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT\_CONTEXT</span></span><br/><span data-ttu-id="941fe-698">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-698">**BOOL**</span></span> | <span data-ttu-id="941fe-699">X</span><span class="sxs-lookup"><span data-stu-id="941fe-699">X</span></span> | \- | \- | <span data-ttu-id="941fe-700">X</span><span class="sxs-lookup"><span data-stu-id="941fe-700">X</span></span> | <span data-ttu-id="941fe-701">Windows 10 Version 21H1</span><span class="sxs-lookup"><span data-stu-id="941fe-701">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="941fe-702">\_WINHTTP-OPTION \_ ENABLETRACING</span><span class="sxs-lookup"><span data-stu-id="941fe-702">WINHTTP\_OPTION\_ENABLETRACING</span></span><br/><span data-ttu-id="941fe-703">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-703">**DWORD**</span></span> | \- | \- | <span data-ttu-id="941fe-704">X</span><span class="sxs-lookup"><span data-stu-id="941fe-704">X</span></span> | <span data-ttu-id="941fe-705">X</span><span class="sxs-lookup"><span data-stu-id="941fe-705">X</span></span> | \- |
| <span data-ttu-id="941fe-706">WINHTTP \_ OPTION \_ ENCODE \_ EXTRA</span><span class="sxs-lookup"><span data-stu-id="941fe-706">WINHTTP\_OPTION\_ENCODE\_EXTRA</span></span><br/><span data-ttu-id="941fe-707">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-707">**BOOL**</span></span> | <span data-ttu-id="941fe-708">X</span><span class="sxs-lookup"><span data-stu-id="941fe-708">X</span></span> | <span data-ttu-id="941fe-709">X</span><span class="sxs-lookup"><span data-stu-id="941fe-709">X</span></span> | \- | <span data-ttu-id="941fe-710">X</span><span class="sxs-lookup"><span data-stu-id="941fe-710">X</span></span> | <span data-ttu-id="941fe-711">Windows 10 Version 1803</span><span class="sxs-lookup"><span data-stu-id="941fe-711">Windows 10 Version 1803</span></span> |
| <span data-ttu-id="941fe-712">\_WINHTTP-OPTION \_ LÄUFT VERBINDUNG AB \_</span><span class="sxs-lookup"><span data-stu-id="941fe-712">WINHTTP\_OPTION\_EXPIRE\_CONNECTION</span></span><br/><span data-ttu-id="941fe-713">–</span><span class="sxs-lookup"><span data-stu-id="941fe-713">N/A</span></span> | \- | <span data-ttu-id="941fe-714">X</span><span class="sxs-lookup"><span data-stu-id="941fe-714">X</span></span> | \- | <span data-ttu-id="941fe-715">X</span><span class="sxs-lookup"><span data-stu-id="941fe-715">X</span></span> | <span data-ttu-id="941fe-716">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="941fe-716">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="941fe-717">\_ \_ ERWEITERTER \_ WINHTTP-OPTION-FEHLER</span><span class="sxs-lookup"><span data-stu-id="941fe-717">WINHTTP\_OPTION\_EXTENDED\_ERROR</span></span><br/><span data-ttu-id="941fe-718">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-718">**DWORD**</span></span> | <span data-ttu-id="941fe-719">X</span><span class="sxs-lookup"><span data-stu-id="941fe-719">X</span></span> | <span data-ttu-id="941fe-720">X</span><span class="sxs-lookup"><span data-stu-id="941fe-720">X</span></span> | <span data-ttu-id="941fe-721">X</span><span class="sxs-lookup"><span data-stu-id="941fe-721">X</span></span> | \- | \- |
| <span data-ttu-id="941fe-722">WINHTTP \_ OPTION \_ FIRST \_ AVAILABLE \_ CONNECTION</span><span class="sxs-lookup"><span data-stu-id="941fe-722">WINHTTP\_OPTION\_FIRST\_AVAILABLE\_CONNECTION</span></span><br/><span data-ttu-id="941fe-723">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-723">**BOOL**</span></span> | <span data-ttu-id="941fe-724">X</span><span class="sxs-lookup"><span data-stu-id="941fe-724">X</span></span> | \- | \- | <span data-ttu-id="941fe-725">X</span><span class="sxs-lookup"><span data-stu-id="941fe-725">X</span></span> | <span data-ttu-id="941fe-726">Windows 10 Version 21H1</span><span class="sxs-lookup"><span data-stu-id="941fe-726">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="941fe-727">WINHTTP \_ OPTION \_ GLOBAL \_ PROXY \_ CREDS</span><span class="sxs-lookup"><span data-stu-id="941fe-727">WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS</span></span><br/>[<span data-ttu-id="941fe-728">**WINHTTP \_ CREDS**</span><span class="sxs-lookup"><span data-stu-id="941fe-728">**WINHTTP\_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | <span data-ttu-id="941fe-729">X</span><span class="sxs-lookup"><span data-stu-id="941fe-729">X</span></span> | <span data-ttu-id="941fe-730">X</span><span class="sxs-lookup"><span data-stu-id="941fe-730">X</span></span> | \- | <span data-ttu-id="941fe-731">X</span><span class="sxs-lookup"><span data-stu-id="941fe-731">X</span></span> | \- |
| <span data-ttu-id="941fe-732">WINHTTP \_ OPTION \_ GLOBAL \_ SERVER \_ CREDS</span><span class="sxs-lookup"><span data-stu-id="941fe-732">WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS</span></span><br/>[<span data-ttu-id="941fe-733">**WINHTTP \_ CREDS \_ EX**</span><span class="sxs-lookup"><span data-stu-id="941fe-733">**WINHTTP\_CREDS\_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | <span data-ttu-id="941fe-734">X</span><span class="sxs-lookup"><span data-stu-id="941fe-734">X</span></span> | <span data-ttu-id="941fe-735">X</span><span class="sxs-lookup"><span data-stu-id="941fe-735">X</span></span> | \- | <span data-ttu-id="941fe-736">X</span><span class="sxs-lookup"><span data-stu-id="941fe-736">X</span></span> | \- |
| <span data-ttu-id="941fe-737">TYP DES \_ WINHTTP-OPTIONSHANDLE \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-737">WINHTTP\_OPTION\_HANDLE\_TYPE</span></span><br/><span data-ttu-id="941fe-738">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-738">**DWORD**</span></span> | <span data-ttu-id="941fe-739">X</span><span class="sxs-lookup"><span data-stu-id="941fe-739">X</span></span> | <span data-ttu-id="941fe-740">X</span><span class="sxs-lookup"><span data-stu-id="941fe-740">X</span></span> | <span data-ttu-id="941fe-741">X</span><span class="sxs-lookup"><span data-stu-id="941fe-741">X</span></span> | \- | \- |
| <span data-ttu-id="941fe-742">WINHTTP \_ OPTION HTTP PROTOCOL \_ \_ \_ ERFORDERLICH</span><span class="sxs-lookup"><span data-stu-id="941fe-742">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED</span></span><br/><span data-ttu-id="941fe-743">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-743">**BOOL**</span></span> | <span data-ttu-id="941fe-744">X</span><span class="sxs-lookup"><span data-stu-id="941fe-744">X</span></span> | <span data-ttu-id="941fe-745">X</span><span class="sxs-lookup"><span data-stu-id="941fe-745">X</span></span> | \- | <span data-ttu-id="941fe-746">X</span><span class="sxs-lookup"><span data-stu-id="941fe-746">X</span></span> | <span data-ttu-id="941fe-747">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="941fe-747">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="941fe-748">VERWENDETES \_ \_ WINHTTP-OPTION-HTTP-PROTOKOLL \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-748">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED</span></span><br/><span data-ttu-id="941fe-749">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-749">**DWORD**</span></span> | \- | <span data-ttu-id="941fe-750">X</span><span class="sxs-lookup"><span data-stu-id="941fe-750">X</span></span> | <span data-ttu-id="941fe-751">X</span><span class="sxs-lookup"><span data-stu-id="941fe-751">X</span></span> | \- | <span data-ttu-id="941fe-752">Windows 10, Version 1607</span><span class="sxs-lookup"><span data-stu-id="941fe-752">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="941fe-753">WINHTTP \_ OPTION \_ \_ HTTP-VERSION</span><span class="sxs-lookup"><span data-stu-id="941fe-753">WINHTTP\_OPTION\_HTTP\_VERSION</span></span><br/>[<span data-ttu-id="941fe-754">**\_ \_ HTTP-VERSIONSINFORMATIONEN**</span><span class="sxs-lookup"><span data-stu-id="941fe-754">**HTTP\_VERSION\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | <span data-ttu-id="941fe-755">X</span><span class="sxs-lookup"><span data-stu-id="941fe-755">X</span></span> | <span data-ttu-id="941fe-756">X</span><span class="sxs-lookup"><span data-stu-id="941fe-756">X</span></span> | <span data-ttu-id="941fe-757">X</span><span class="sxs-lookup"><span data-stu-id="941fe-757">X</span></span> | <span data-ttu-id="941fe-758">X</span><span class="sxs-lookup"><span data-stu-id="941fe-758">X</span></span> | \- |
| <span data-ttu-id="941fe-759">\_WINHTTP-OPTION \_ HTTP2 \_ KEEPALIVE</span><span class="sxs-lookup"><span data-stu-id="941fe-759">WINHTTP\_OPTION\_HTTP2\_KEEPALIVE</span></span><br/><span data-ttu-id="941fe-760">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-760">**DWORD**</span></span> | <span data-ttu-id="941fe-761">X</span><span class="sxs-lookup"><span data-stu-id="941fe-761">X</span></span> | \- | \- | <span data-ttu-id="941fe-762">X</span><span class="sxs-lookup"><span data-stu-id="941fe-762">X</span></span> | <span data-ttu-id="941fe-763">Windows 10 Version 21H1</span><span class="sxs-lookup"><span data-stu-id="941fe-763">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="941fe-764">\_WINHTTP-OPTION \_ HTTP2 \_ PLUS \_ \_ ÜBERTRAGUNGSCODIERUNG</span><span class="sxs-lookup"><span data-stu-id="941fe-764">WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING</span></span><br/><span data-ttu-id="941fe-765">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-765">**BOOL**</span></span> | <span data-ttu-id="941fe-766">X</span><span class="sxs-lookup"><span data-stu-id="941fe-766">X</span></span> | <span data-ttu-id="941fe-767">X</span><span class="sxs-lookup"><span data-stu-id="941fe-767">X</span></span> | \- | <span data-ttu-id="941fe-768">X</span><span class="sxs-lookup"><span data-stu-id="941fe-768">X</span></span> | <span data-ttu-id="941fe-769">Windows 10 Version 21H1</span><span class="sxs-lookup"><span data-stu-id="941fe-769">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="941fe-770">WINHTTP \_ OPTION \_ IGNORE \_ CERT \_ REVOCATION \_ OFFLINE</span><span class="sxs-lookup"><span data-stu-id="941fe-770">WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE</span></span><br/><span data-ttu-id="941fe-771">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-771">**BOOL**</span></span> | \- | <span data-ttu-id="941fe-772">X</span><span class="sxs-lookup"><span data-stu-id="941fe-772">X</span></span> | \- | <span data-ttu-id="941fe-773">X</span><span class="sxs-lookup"><span data-stu-id="941fe-773">X</span></span> | <span data-ttu-id="941fe-774">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="941fe-774">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="941fe-775">WINHTTP \_ OPTION \_ IPV6 \_ FAST \_ FALLBACK</span><span class="sxs-lookup"><span data-stu-id="941fe-775">WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK</span></span><br/><span data-ttu-id="941fe-776">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-776">**BOOL**</span></span> | <span data-ttu-id="941fe-777">X</span><span class="sxs-lookup"><span data-stu-id="941fe-777">X</span></span> | \- | \- | <span data-ttu-id="941fe-778">X</span><span class="sxs-lookup"><span data-stu-id="941fe-778">X</span></span> | <span data-ttu-id="941fe-779">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="941fe-779">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="941fe-780">\_WINHTTP-OPTION: \_ \_ PROXY \_ \_ CONNECT-ANTWORT</span><span class="sxs-lookup"><span data-stu-id="941fe-780">WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="941fe-781">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-781">**BOOL**</span></span> | <span data-ttu-id="941fe-782">X</span><span class="sxs-lookup"><span data-stu-id="941fe-782">X</span></span> | <span data-ttu-id="941fe-783">X</span><span class="sxs-lookup"><span data-stu-id="941fe-783">X</span></span> | <span data-ttu-id="941fe-784">X</span><span class="sxs-lookup"><span data-stu-id="941fe-784">X</span></span> | \- | \- |
| <span data-ttu-id="941fe-785">WINHTTP \_ OPTION \_ \_ MAX. CONNS \_ PRO \_ 1 \_ 0 \_ SERVER</span><span class="sxs-lookup"><span data-stu-id="941fe-785">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER</span></span><br/><span data-ttu-id="941fe-786">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-786">**DWORD**</span></span> | <span data-ttu-id="941fe-787">X</span><span class="sxs-lookup"><span data-stu-id="941fe-787">X</span></span> | \- | <span data-ttu-id="941fe-788">X</span><span class="sxs-lookup"><span data-stu-id="941fe-788">X</span></span> | <span data-ttu-id="941fe-789">X</span><span class="sxs-lookup"><span data-stu-id="941fe-789">X</span></span> | \- |
| <span data-ttu-id="941fe-790">WINHTTP \_ OPTION \_ \_ MAX. CONNS \_ PRO \_ SERVER</span><span class="sxs-lookup"><span data-stu-id="941fe-790">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER</span></span><br/><span data-ttu-id="941fe-791">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-791">**DWORD**</span></span> | <span data-ttu-id="941fe-792">X</span><span class="sxs-lookup"><span data-stu-id="941fe-792">X</span></span> | \- | <span data-ttu-id="941fe-793">X</span><span class="sxs-lookup"><span data-stu-id="941fe-793">X</span></span> | <span data-ttu-id="941fe-794">X</span><span class="sxs-lookup"><span data-stu-id="941fe-794">X</span></span> | \- |
| <span data-ttu-id="941fe-795">WINHTTP \_ OPTION \_ \_ MAX. AUTOMATISCHE HTTP-UMLEITUNGEN \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-795">WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS</span></span><br/><span data-ttu-id="941fe-796">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-796">**DWORD**</span></span> | <span data-ttu-id="941fe-797">X</span><span class="sxs-lookup"><span data-stu-id="941fe-797">X</span></span> | <span data-ttu-id="941fe-798">X</span><span class="sxs-lookup"><span data-stu-id="941fe-798">X</span></span> | <span data-ttu-id="941fe-799">X</span><span class="sxs-lookup"><span data-stu-id="941fe-799">X</span></span> | <span data-ttu-id="941fe-800">X</span><span class="sxs-lookup"><span data-stu-id="941fe-800">X</span></span> | \- |
| <span data-ttu-id="941fe-801">WINHTTP-OPTION \_ \_ \_ MAX. \_ HTTP-STATUS \_ CONTINUE</span><span class="sxs-lookup"><span data-stu-id="941fe-801">WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE</span></span><br/><span data-ttu-id="941fe-802">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-802">**DWORD**</span></span> | <span data-ttu-id="941fe-803">X</span><span class="sxs-lookup"><span data-stu-id="941fe-803">X</span></span> | <span data-ttu-id="941fe-804">X</span><span class="sxs-lookup"><span data-stu-id="941fe-804">X</span></span> | <span data-ttu-id="941fe-805">X</span><span class="sxs-lookup"><span data-stu-id="941fe-805">X</span></span> | <span data-ttu-id="941fe-806">X</span><span class="sxs-lookup"><span data-stu-id="941fe-806">X</span></span> | \- |
| <span data-ttu-id="941fe-807">WINHTTP \_ OPTION \_ MAX \_ RESPONSE \_ DRAIN \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="941fe-807">WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE</span></span><br/><span data-ttu-id="941fe-808">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-808">**DWORD**</span></span> | <span data-ttu-id="941fe-809">X</span><span class="sxs-lookup"><span data-stu-id="941fe-809">X</span></span> | <span data-ttu-id="941fe-810">X</span><span class="sxs-lookup"><span data-stu-id="941fe-810">X</span></span> | <span data-ttu-id="941fe-811">X</span><span class="sxs-lookup"><span data-stu-id="941fe-811">X</span></span> | <span data-ttu-id="941fe-812">X</span><span class="sxs-lookup"><span data-stu-id="941fe-812">X</span></span> | \- |
| <span data-ttu-id="941fe-813">WINHTTP-OPTION \_ \_ \_ MAX. GRÖßE DES \_ \_ ANTWORTHEADERS</span><span class="sxs-lookup"><span data-stu-id="941fe-813">WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE</span></span><br/><span data-ttu-id="941fe-814">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-814">**DWORD**</span></span> | <span data-ttu-id="941fe-815">X</span><span class="sxs-lookup"><span data-stu-id="941fe-815">X</span></span> | <span data-ttu-id="941fe-816">X</span><span class="sxs-lookup"><span data-stu-id="941fe-816">X</span></span> | <span data-ttu-id="941fe-817">X</span><span class="sxs-lookup"><span data-stu-id="941fe-817">X</span></span> | <span data-ttu-id="941fe-818">X</span><span class="sxs-lookup"><span data-stu-id="941fe-818">X</span></span> | \- |
| <span data-ttu-id="941fe-819">ÜBERGEORDNETES \_ HANDLE DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-819">WINHTTP\_OPTION\_PARENT\_HANDLE</span></span><br/>[<span data-ttu-id="941fe-820">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="941fe-820">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="941fe-821">X</span><span class="sxs-lookup"><span data-stu-id="941fe-821">X</span></span> | <span data-ttu-id="941fe-822">X</span><span class="sxs-lookup"><span data-stu-id="941fe-822">X</span></span> | <span data-ttu-id="941fe-823">X</span><span class="sxs-lookup"><span data-stu-id="941fe-823">X</span></span> | \- | \- |
| <span data-ttu-id="941fe-824">\_WINHTTP-OPTION \_ \_ PASSPORT-COBRANDINGTEXT \_</span><span class="sxs-lookup"><span data-stu-id="941fe-824">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT</span></span><br/><span data-ttu-id="941fe-825">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="941fe-825">**LPWSTR**</span></span> | \- | <span data-ttu-id="941fe-826">X</span><span class="sxs-lookup"><span data-stu-id="941fe-826">X</span></span> | <span data-ttu-id="941fe-827">X</span><span class="sxs-lookup"><span data-stu-id="941fe-827">X</span></span> | \- | \- |
| <span data-ttu-id="941fe-828">\_WINHTTP-OPTION \_ \_ PASSPORT-COBRANDING-URL \_</span><span class="sxs-lookup"><span data-stu-id="941fe-828">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL</span></span><br/><span data-ttu-id="941fe-829">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="941fe-829">**LPWSTR**</span></span> | \- | <span data-ttu-id="941fe-830">X</span><span class="sxs-lookup"><span data-stu-id="941fe-830">X</span></span> | <span data-ttu-id="941fe-831">X</span><span class="sxs-lookup"><span data-stu-id="941fe-831">X</span></span> | \- | \- |
| <span data-ttu-id="941fe-832">\_WINHTTP-OPTION \_ \_ \_ PASSPORT-RÜCKGABE-URL</span><span class="sxs-lookup"><span data-stu-id="941fe-832">WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL</span></span><br/><span data-ttu-id="941fe-833">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="941fe-833">**LPVOID**</span></span> | \- | <span data-ttu-id="941fe-834">X</span><span class="sxs-lookup"><span data-stu-id="941fe-834">X</span></span> | <span data-ttu-id="941fe-835">X</span><span class="sxs-lookup"><span data-stu-id="941fe-835">X</span></span> | \- | \- |
| <span data-ttu-id="941fe-836">\_WINHTTP-OPTION \_ \_ \_ PASSPORT-ABMELDEN</span><span class="sxs-lookup"><span data-stu-id="941fe-836">WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT</span></span><br/><span data-ttu-id="941fe-837">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="941fe-837">**LPVOID**</span></span> | <span data-ttu-id="941fe-838">X</span><span class="sxs-lookup"><span data-stu-id="941fe-838">X</span></span> | \- | \- | <span data-ttu-id="941fe-839">X</span><span class="sxs-lookup"><span data-stu-id="941fe-839">X</span></span> | \- |
| <span data-ttu-id="941fe-840">\_ \_ WINHTTP-OPTIONSKENNWORT</span><span class="sxs-lookup"><span data-stu-id="941fe-840">WINHTTP\_OPTION\_PASSWORD</span></span><br/><span data-ttu-id="941fe-841">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="941fe-841">**LPWSTR**</span></span> | \- | <span data-ttu-id="941fe-842">X</span><span class="sxs-lookup"><span data-stu-id="941fe-842">X</span></span> | <span data-ttu-id="941fe-843">X</span><span class="sxs-lookup"><span data-stu-id="941fe-843">X</span></span> | <span data-ttu-id="941fe-844">X</span><span class="sxs-lookup"><span data-stu-id="941fe-844">X</span></span> | \- |
| <span data-ttu-id="941fe-845">\_WINHTTP-OPTIONSPROXY \_</span><span class="sxs-lookup"><span data-stu-id="941fe-845">WINHTTP\_OPTION\_PROXY</span></span><br/>[<span data-ttu-id="941fe-846">**\_WINHTTP-PROXYINFORMATIONEN \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-846">**WINHTTP\_PROXY\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | <span data-ttu-id="941fe-847">X</span><span class="sxs-lookup"><span data-stu-id="941fe-847">X</span></span> | <span data-ttu-id="941fe-848">X</span><span class="sxs-lookup"><span data-stu-id="941fe-848">X</span></span> | <span data-ttu-id="941fe-849">X</span><span class="sxs-lookup"><span data-stu-id="941fe-849">X</span></span> | <span data-ttu-id="941fe-850">X</span><span class="sxs-lookup"><span data-stu-id="941fe-850">X</span></span> | \- |
| <span data-ttu-id="941fe-851">\_PROXYKENNWORT \_ FÜR WINHTTP-OPTION \_</span><span class="sxs-lookup"><span data-stu-id="941fe-851">WINHTTP\_OPTION\_PROXY\_PASSWORD</span></span><br/><span data-ttu-id="941fe-852">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="941fe-852">**LPWSTR**</span></span> | \- | <span data-ttu-id="941fe-853">X</span><span class="sxs-lookup"><span data-stu-id="941fe-853">X</span></span> | <span data-ttu-id="941fe-854">X</span><span class="sxs-lookup"><span data-stu-id="941fe-854">X</span></span> | <span data-ttu-id="941fe-855">X</span><span class="sxs-lookup"><span data-stu-id="941fe-855">X</span></span> | \- |
| <span data-ttu-id="941fe-856">VERWENDETER \_ \_ WINHTTP-OPTIONSPROXY-SPN \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-856">WINHTTP\_OPTION\_PROXY\_SPN\_USED</span></span><br/><span data-ttu-id="941fe-857">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="941fe-857">**LPWSTR**</span></span> | \- | <span data-ttu-id="941fe-858">X</span><span class="sxs-lookup"><span data-stu-id="941fe-858">X</span></span> | <span data-ttu-id="941fe-859">X</span><span class="sxs-lookup"><span data-stu-id="941fe-859">X</span></span> | \- | \- |
| <span data-ttu-id="941fe-860">\_PROXYBENUTZERNAME DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-860">WINHTTP\_OPTION\_PROXY\_USERNAME</span></span><br/><span data-ttu-id="941fe-861">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="941fe-861">**LPWSTR**</span></span> | \- | <span data-ttu-id="941fe-862">X</span><span class="sxs-lookup"><span data-stu-id="941fe-862">X</span></span> | <span data-ttu-id="941fe-863">X</span><span class="sxs-lookup"><span data-stu-id="941fe-863">X</span></span> | <span data-ttu-id="941fe-864">X</span><span class="sxs-lookup"><span data-stu-id="941fe-864">X</span></span> | \- |
| <span data-ttu-id="941fe-865">\_WINHTTP-OPTION \_ READ BUFFER \_ \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="941fe-865">WINHTTP\_OPTION\_READ\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="941fe-866">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-866">**DWORD**</span></span> | \- | <span data-ttu-id="941fe-867">X</span><span class="sxs-lookup"><span data-stu-id="941fe-867">X</span></span> | <span data-ttu-id="941fe-868">X</span><span class="sxs-lookup"><span data-stu-id="941fe-868">X</span></span> | <span data-ttu-id="941fe-869">X</span><span class="sxs-lookup"><span data-stu-id="941fe-869">X</span></span> | \- |
| <span data-ttu-id="941fe-870">WINHTTP-OPTION \_ \_ "PROXY \_ \_ CONNECT-ANTWORT \_ EMPFANGEN"</span><span class="sxs-lookup"><span data-stu-id="941fe-870">WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="941fe-871">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-871">**BOOL**</span></span> | <span data-ttu-id="941fe-872">X</span><span class="sxs-lookup"><span data-stu-id="941fe-872">X</span></span> | <span data-ttu-id="941fe-873">X</span><span class="sxs-lookup"><span data-stu-id="941fe-873">X</span></span> | \- | <span data-ttu-id="941fe-874">X</span><span class="sxs-lookup"><span data-stu-id="941fe-874">X</span></span> | \- |
| <span data-ttu-id="941fe-875">WINHTTP-OPTION \_ \_ \_ \_ EMPFANGSANTWORT-TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="941fe-875">WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT</span></span><br/><span data-ttu-id="941fe-876">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-876">**DWORD**</span></span> | <span data-ttu-id="941fe-877">X</span><span class="sxs-lookup"><span data-stu-id="941fe-877">X</span></span> | <span data-ttu-id="941fe-878">X</span><span class="sxs-lookup"><span data-stu-id="941fe-878">X</span></span> | <span data-ttu-id="941fe-879">X</span><span class="sxs-lookup"><span data-stu-id="941fe-879">X</span></span> | <span data-ttu-id="941fe-880">X</span><span class="sxs-lookup"><span data-stu-id="941fe-880">X</span></span> | \- |
| <span data-ttu-id="941fe-881">\_EMPFANGSZEITÜBERSCHREITUNG DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-881">WINHTTP\_OPTION\_RECEIVE\_TIMEOUT</span></span><br/><span data-ttu-id="941fe-882">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-882">**DWORD**</span></span> | <span data-ttu-id="941fe-883">X</span><span class="sxs-lookup"><span data-stu-id="941fe-883">X</span></span> | <span data-ttu-id="941fe-884">X</span><span class="sxs-lookup"><span data-stu-id="941fe-884">X</span></span> | <span data-ttu-id="941fe-885">X</span><span class="sxs-lookup"><span data-stu-id="941fe-885">X</span></span> | <span data-ttu-id="941fe-886">X</span><span class="sxs-lookup"><span data-stu-id="941fe-886">X</span></span> | \- |
| <span data-ttu-id="941fe-887">UMLEITUNGSRICHTLINIE \_ FÜR WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-887">WINHTTP\_OPTION\_REDIRECT\_POLICY</span></span><br/><span data-ttu-id="941fe-888">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-888">**DWORD**</span></span> | <span data-ttu-id="941fe-889">X</span><span class="sxs-lookup"><span data-stu-id="941fe-889">X</span></span> | <span data-ttu-id="941fe-890">X</span><span class="sxs-lookup"><span data-stu-id="941fe-890">X</span></span> | <span data-ttu-id="941fe-891">X</span><span class="sxs-lookup"><span data-stu-id="941fe-891">X</span></span> | <span data-ttu-id="941fe-892">X</span><span class="sxs-lookup"><span data-stu-id="941fe-892">X</span></span> | \- |
| <span data-ttu-id="941fe-893">\_WINHTTP-OPTION \_ BENUTZER IN URL \_ \_ \_ ABLEHNENPWD</span><span class="sxs-lookup"><span data-stu-id="941fe-893">WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL</span></span><br/><span data-ttu-id="941fe-894">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-894">**BOOL**</span></span> | \- | <span data-ttu-id="941fe-895">X</span><span class="sxs-lookup"><span data-stu-id="941fe-895">X</span></span> | \- | <span data-ttu-id="941fe-896">X</span><span class="sxs-lookup"><span data-stu-id="941fe-896">X</span></span> | \- |
| <span data-ttu-id="941fe-897">\_ \_ ANFORDERUNGSPRIORITÄT DER WINHTTP-OPTION \_</span><span class="sxs-lookup"><span data-stu-id="941fe-897">WINHTTP\_OPTION\_REQUEST\_PRIORITY</span></span><br/><span data-ttu-id="941fe-898">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-898">**DWORD**</span></span> | \- | <span data-ttu-id="941fe-899">X</span><span class="sxs-lookup"><span data-stu-id="941fe-899">X</span></span> | <span data-ttu-id="941fe-900">X</span><span class="sxs-lookup"><span data-stu-id="941fe-900">X</span></span> | <span data-ttu-id="941fe-901">X</span><span class="sxs-lookup"><span data-stu-id="941fe-901">X</span></span> | \- |
| <span data-ttu-id="941fe-902">\_ \_ WINHTTP-OPTIONSANFORDERUNGSSTATISTIKEN \_</span><span class="sxs-lookup"><span data-stu-id="941fe-902">WINHTTP\_OPTION\_REQUEST\_STATS</span></span><br/>[<span data-ttu-id="941fe-903">**\_ \_ WINHTTP-ANFORDERUNGSSTATISTIKEN**</span><span class="sxs-lookup"><span data-stu-id="941fe-903">**WINHTTP\_REQUEST\_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | <span data-ttu-id="941fe-904">X</span><span class="sxs-lookup"><span data-stu-id="941fe-904">X</span></span> | <span data-ttu-id="941fe-905">X</span><span class="sxs-lookup"><span data-stu-id="941fe-905">X</span></span> | \- | <span data-ttu-id="941fe-906">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="941fe-906">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="941fe-907">ANFORDERUNGSZEITEN \_ DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-907">WINHTTP\_OPTION\_REQUEST\_TIMES</span></span><br/>[<span data-ttu-id="941fe-908">**\_WINHTTP-ANFORDERUNGSZEITEN \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-908">**WINHTTP\_REQUEST\_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | <span data-ttu-id="941fe-909">X</span><span class="sxs-lookup"><span data-stu-id="941fe-909">X</span></span> | <span data-ttu-id="941fe-910">X</span><span class="sxs-lookup"><span data-stu-id="941fe-910">X</span></span> | \- | <span data-ttu-id="941fe-911">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="941fe-911">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="941fe-912">\_WINHTTP-OPTION \_ " \_ STREAMENDE \_ ERFORDERLICH"</span><span class="sxs-lookup"><span data-stu-id="941fe-912">WINHTTP\_OPTION\_REQUIRE\_STREAM\_END</span></span><br/><span data-ttu-id="941fe-913">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-913">**BOOL**</span></span> | <span data-ttu-id="941fe-914">X</span><span class="sxs-lookup"><span data-stu-id="941fe-914">X</span></span> | <span data-ttu-id="941fe-915">X</span><span class="sxs-lookup"><span data-stu-id="941fe-915">X</span></span> | \- | <span data-ttu-id="941fe-916">X</span><span class="sxs-lookup"><span data-stu-id="941fe-916">X</span></span> | <span data-ttu-id="941fe-917">Windows 10 Version 21H1</span><span class="sxs-lookup"><span data-stu-id="941fe-917">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="941fe-918">HOSTNAME \_ DER WINHTTP-OPTIONSAUFLÖSUNG \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-918">WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME</span></span><br/><span data-ttu-id="941fe-919">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="941fe-919">**LPWSTR**</span></span> | \- | <span data-ttu-id="941fe-920">X</span><span class="sxs-lookup"><span data-stu-id="941fe-920">X</span></span> | \- | <span data-ttu-id="941fe-921">X</span><span class="sxs-lookup"><span data-stu-id="941fe-921">X</span></span> | <span data-ttu-id="941fe-922">Windows 10 Version 21H1</span><span class="sxs-lookup"><span data-stu-id="941fe-922">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="941fe-923">WINHTTP-OPTION \_ \_ \_ TIMEOUT AUFLÖSEN</span><span class="sxs-lookup"><span data-stu-id="941fe-923">WINHTTP\_OPTION\_RESOLVE\_TIMEOUT</span></span><br/><span data-ttu-id="941fe-924">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-924">**DWORD**</span></span> | <span data-ttu-id="941fe-925">X</span><span class="sxs-lookup"><span data-stu-id="941fe-925">X</span></span> | <span data-ttu-id="941fe-926">X</span><span class="sxs-lookup"><span data-stu-id="941fe-926">X</span></span> | <span data-ttu-id="941fe-927">X</span><span class="sxs-lookup"><span data-stu-id="941fe-927">X</span></span> | <span data-ttu-id="941fe-928">X</span><span class="sxs-lookup"><span data-stu-id="941fe-928">X</span></span> | \- |
| <span data-ttu-id="941fe-929">SICHERE PROTOKOLLE \_ DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-929">WINHTTP\_OPTION\_SECURE\_PROTOCOLS</span></span><br/><span data-ttu-id="941fe-930">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-930">**DWORD**</span></span> | <span data-ttu-id="941fe-931">X</span><span class="sxs-lookup"><span data-stu-id="941fe-931">X</span></span> | \- | \- | <span data-ttu-id="941fe-932">X</span><span class="sxs-lookup"><span data-stu-id="941fe-932">X</span></span> | \- |
| <span data-ttu-id="941fe-933">\_SICHERHEITSZERTIFIKATSTRUKTUR DER WINHTTP-OPTION \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-933">WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT</span></span><br/>[<span data-ttu-id="941fe-934">**\_WINHTTP-ZERTIFIKATINFORMATIONEN \_**</span><span class="sxs-lookup"><span data-stu-id="941fe-934">**WINHTTP\_CERTIFICATE\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | <span data-ttu-id="941fe-935">X</span><span class="sxs-lookup"><span data-stu-id="941fe-935">X</span></span> | <span data-ttu-id="941fe-936">X</span><span class="sxs-lookup"><span data-stu-id="941fe-936">X</span></span> | \- | \- |
| <span data-ttu-id="941fe-937">\_SICHERHEITSFLAGS FÜR DIE WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-937">WINHTTP\_OPTION\_SECURITY\_FLAGS</span></span><br/><span data-ttu-id="941fe-938">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-938">**DWORD**</span></span> | \- | <span data-ttu-id="941fe-939">X</span><span class="sxs-lookup"><span data-stu-id="941fe-939">X</span></span> | <span data-ttu-id="941fe-940">X</span><span class="sxs-lookup"><span data-stu-id="941fe-940">X</span></span> | <span data-ttu-id="941fe-941">X</span><span class="sxs-lookup"><span data-stu-id="941fe-941">X</span></span> | \- |
| <span data-ttu-id="941fe-942">SICHERHEITSINFORMATIONEN \_ ZUR WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-942">WINHTTP\_OPTION\_SECURITY\_INFO</span></span><br/>[<span data-ttu-id="941fe-943">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="941fe-943">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | <span data-ttu-id="941fe-944">X</span><span class="sxs-lookup"><span data-stu-id="941fe-944">X</span></span> | <span data-ttu-id="941fe-945">X</span><span class="sxs-lookup"><span data-stu-id="941fe-945">X</span></span> | \- | <span data-ttu-id="941fe-946">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="941fe-946">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="941fe-947">\_WINHTTP-OPTION \_ \_ \_ SICHERHEITSSCHLÜSSELBITNESS</span><span class="sxs-lookup"><span data-stu-id="941fe-947">WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS</span></span><br/><span data-ttu-id="941fe-948">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-948">**DWORD**</span></span> | \- | <span data-ttu-id="941fe-949">X</span><span class="sxs-lookup"><span data-stu-id="941fe-949">X</span></span> | <span data-ttu-id="941fe-950">X</span><span class="sxs-lookup"><span data-stu-id="941fe-950">X</span></span> | \- | \- |
| <span data-ttu-id="941fe-951">TIMEOUT \_ BEIM SENDEN DER \_ \_ WINHTTP-OPTION</span><span class="sxs-lookup"><span data-stu-id="941fe-951">WINHTTP\_OPTION\_SEND\_TIMEOUT</span></span><br/><span data-ttu-id="941fe-952">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-952">**DWORD**</span></span> | <span data-ttu-id="941fe-953">X</span><span class="sxs-lookup"><span data-stu-id="941fe-953">X</span></span> | <span data-ttu-id="941fe-954">X</span><span class="sxs-lookup"><span data-stu-id="941fe-954">X</span></span> | <span data-ttu-id="941fe-955">X</span><span class="sxs-lookup"><span data-stu-id="941fe-955">X</span></span> | <span data-ttu-id="941fe-956">X</span><span class="sxs-lookup"><span data-stu-id="941fe-956">X</span></span> | \- |
| <span data-ttu-id="941fe-957">WINHTTP \_ OPTION \_ SERVER \_ CBT</span><span class="sxs-lookup"><span data-stu-id="941fe-957">WINHTTP\_OPTION\_SERVER\_CBT</span></span><br/><span data-ttu-id="941fe-958">[**\_SecPkgContext-Bindungen**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span><span class="sxs-lookup"><span data-stu-id="941fe-958">[**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span></span> | \- | <span data-ttu-id="941fe-959">X</span><span class="sxs-lookup"><span data-stu-id="941fe-959">X</span></span> | <span data-ttu-id="941fe-960">X</span><span class="sxs-lookup"><span data-stu-id="941fe-960">X</span></span> | \- | \- |
| <span data-ttu-id="941fe-961">WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CHAIN \_ CONTEXT</span><span class="sxs-lookup"><span data-stu-id="941fe-961">WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT</span></span><br/>[<span data-ttu-id="941fe-962">**CERT_CHAIN_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="941fe-962">**CERT_CHAIN_CONTEXT**</span></span>](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | <span data-ttu-id="941fe-963">X</span><span class="sxs-lookup"><span data-stu-id="941fe-963">X</span></span> | <span data-ttu-id="941fe-964">X</span><span class="sxs-lookup"><span data-stu-id="941fe-964">X</span></span> | \- | <span data-ttu-id="941fe-965">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="941fe-965">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="941fe-966">WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CONTEXT</span><span class="sxs-lookup"><span data-stu-id="941fe-966">WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="941fe-967">**CERT-KONTEXT**</span><span class="sxs-lookup"><span data-stu-id="941fe-967">**CERT CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="941fe-968">X</span><span class="sxs-lookup"><span data-stu-id="941fe-968">X</span></span> | <span data-ttu-id="941fe-969">X</span><span class="sxs-lookup"><span data-stu-id="941fe-969">X</span></span> | \- | \- |
| <span data-ttu-id="941fe-970">VERWENDETER \_ \_ WINHTTP-OPTIONSSERVER-SPN \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-970">WINHTTP\_OPTION\_SERVER\_SPN\_USED</span></span><br/><span data-ttu-id="941fe-971">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="941fe-971">**LPWSTR**</span></span> | \- | <span data-ttu-id="941fe-972">X</span><span class="sxs-lookup"><span data-stu-id="941fe-972">X</span></span> | <span data-ttu-id="941fe-973">X</span><span class="sxs-lookup"><span data-stu-id="941fe-973">X</span></span> | \- | \- |
| <span data-ttu-id="941fe-974">\_ \_ WINHTTP-OPTIONS-SPN</span><span class="sxs-lookup"><span data-stu-id="941fe-974">WINHTTP\_OPTION\_SPN</span></span><br/><span data-ttu-id="941fe-975">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-975">**DWORD**</span></span> | \- | <span data-ttu-id="941fe-976">X</span><span class="sxs-lookup"><span data-stu-id="941fe-976">X</span></span> | \- | <span data-ttu-id="941fe-977">X</span><span class="sxs-lookup"><span data-stu-id="941fe-977">X</span></span> | \- |
| <span data-ttu-id="941fe-978">\_ \_ WINHTTP-OPTIONSSTREAMFEHLERCODE \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-978">WINHTTP\_OPTION\_STREAM\_ERROR\_CODE</span></span><br/><span data-ttu-id="941fe-979">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-979">**DWORD**</span></span> | \- | <span data-ttu-id="941fe-980">X</span><span class="sxs-lookup"><span data-stu-id="941fe-980">X</span></span> | <span data-ttu-id="941fe-981">X</span><span class="sxs-lookup"><span data-stu-id="941fe-981">X</span></span> | \- | <span data-ttu-id="941fe-982">Windows 10 Version 21H1</span><span class="sxs-lookup"><span data-stu-id="941fe-982">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="941fe-983">WINHTTP-OPTION \_ \_ TCP FAST \_ \_ OPEN</span><span class="sxs-lookup"><span data-stu-id="941fe-983">WINHTTP\_OPTION\_TCP\_FAST\_OPEN</span></span><br/><span data-ttu-id="941fe-984">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-984">**BOOL**</span></span> | <span data-ttu-id="941fe-985">X</span><span class="sxs-lookup"><span data-stu-id="941fe-985">X</span></span> | \- | \- | <span data-ttu-id="941fe-986">X</span><span class="sxs-lookup"><span data-stu-id="941fe-986">X</span></span> | <span data-ttu-id="941fe-987">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="941fe-987">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="941fe-988">\_WINHTTP-OPTION \_ TCP \_ KEEPALIVE</span><span class="sxs-lookup"><span data-stu-id="941fe-988">WINHTTP\_OPTION\_TCP\_KEEPALIVE</span></span><br/>[<span data-ttu-id="941fe-989">**tcp \_ keepalive**</span><span class="sxs-lookup"><span data-stu-id="941fe-989">**tcp\_keepalive**</span></span>](/windows/win32/winsock/sio-keepalive-vals) | <span data-ttu-id="941fe-990">X</span><span class="sxs-lookup"><span data-stu-id="941fe-990">X</span></span> | \- | \- | <span data-ttu-id="941fe-991">X</span><span class="sxs-lookup"><span data-stu-id="941fe-991">X</span></span> | <span data-ttu-id="941fe-992">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="941fe-992">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="941fe-993">WINHTTP-OPTION \_ \_ TLS FALSE \_ \_ START</span><span class="sxs-lookup"><span data-stu-id="941fe-993">WINHTTP\_OPTION\_TLS\_FALSE\_START</span></span><br/><span data-ttu-id="941fe-994">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-994">**BOOL**</span></span> | <span data-ttu-id="941fe-995">X</span><span class="sxs-lookup"><span data-stu-id="941fe-995">X</span></span> | \- | \- | <span data-ttu-id="941fe-996">X</span><span class="sxs-lookup"><span data-stu-id="941fe-996">X</span></span> | <span data-ttu-id="941fe-997">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="941fe-997">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="941fe-998">UNSICHERER \_ \_ \_ FALLBACK DES TLS-PROTOKOLLS DER \_ WINHTTP-OPTION \_</span><span class="sxs-lookup"><span data-stu-id="941fe-998">WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK</span></span><br/><span data-ttu-id="941fe-999">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-999">**BOOL**</span></span> | <span data-ttu-id="941fe-1000">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1000">X</span></span> | \- | \- | <span data-ttu-id="941fe-1001">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1001">X</span></span> | <span data-ttu-id="941fe-1002">Windows 10 Version 21H1</span><span class="sxs-lookup"><span data-stu-id="941fe-1002">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="941fe-1003">WINHTTP \_ OPTION \_ UNLOAD \_ NOTIFY \_ EVENT</span><span class="sxs-lookup"><span data-stu-id="941fe-1003">WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT</span></span><br/>[<span data-ttu-id="941fe-1004">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="941fe-1004">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="941fe-1005">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1005">X</span></span> | \- | \- | <span data-ttu-id="941fe-1006">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1006">X</span></span> | \- |
| <span data-ttu-id="941fe-1007">WINHTTP \_ OPTION \_ UNSAFE \_ HEADER \_ PARSING</span><span class="sxs-lookup"><span data-stu-id="941fe-1007">WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING</span></span><br/><span data-ttu-id="941fe-1008">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-1008">**DWORD**</span></span> | \- | <span data-ttu-id="941fe-1009">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1009">X</span></span> | \- | <span data-ttu-id="941fe-1010">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1010">X</span></span> | \- |
| <span data-ttu-id="941fe-1011">UPGRADE DER \_ WINHTTP-OPTION \_ AUF \_ \_ \_ WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="941fe-1011">WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET</span></span><br/><span data-ttu-id="941fe-1012">–</span><span class="sxs-lookup"><span data-stu-id="941fe-1012">N/A</span></span> | \- | <span data-ttu-id="941fe-1013">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1013">X</span></span> | \- | <span data-ttu-id="941fe-1014">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1014">X</span></span> | \- |
| <span data-ttu-id="941fe-1015">\_ \_ WINHTTP-OPTIONS-URL</span><span class="sxs-lookup"><span data-stu-id="941fe-1015">WINHTTP\_OPTION\_URL</span></span><br/><span data-ttu-id="941fe-1016">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="941fe-1016">**LPWSTR**</span></span> | \- | <span data-ttu-id="941fe-1017">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1017">X</span></span> | <span data-ttu-id="941fe-1018">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1018">X</span></span> | \- | \- |
| <span data-ttu-id="941fe-1019">WINHTTP \_ OPTION USE GLOBAL SERVER CREDENTIALS (WINHTTP-OPTION: \_ VERWENDEN VON \_ ANMELDEINFORMATIONEN FÜR GLOBALEN \_ SERVER) \_</span><span class="sxs-lookup"><span data-stu-id="941fe-1019">WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS</span></span><br/><span data-ttu-id="941fe-1020">**Bool**</span><span class="sxs-lookup"><span data-stu-id="941fe-1020">**BOOL**</span></span> | <span data-ttu-id="941fe-1021">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1021">X</span></span> | <span data-ttu-id="941fe-1022">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1022">X</span></span> | \- | <span data-ttu-id="941fe-1023">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1023">X</span></span> | \- |
| <span data-ttu-id="941fe-1024">WINHTTP \_ OPTION \_ USER \_ AGENT</span><span class="sxs-lookup"><span data-stu-id="941fe-1024">WINHTTP\_OPTION\_USER\_AGENT</span></span><br/><span data-ttu-id="941fe-1025">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="941fe-1025">**LPWSTR**</span></span> | <span data-ttu-id="941fe-1026">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1026">X</span></span> | \- | <span data-ttu-id="941fe-1027">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1027">X</span></span> | <span data-ttu-id="941fe-1028">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1028">X</span></span> | \- |
| <span data-ttu-id="941fe-1029">WINHTTP \_ OPTION \_ USERNAME</span><span class="sxs-lookup"><span data-stu-id="941fe-1029">WINHTTP\_OPTION\_USERNAME</span></span><br/><span data-ttu-id="941fe-1030">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="941fe-1030">**LPWSTR**</span></span> | \- | <span data-ttu-id="941fe-1031">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1031">X</span></span> | <span data-ttu-id="941fe-1032">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1032">X</span></span> | <span data-ttu-id="941fe-1033">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1033">X</span></span> | \- |
| <span data-ttu-id="941fe-1034">WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ CLOSE \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="941fe-1034">WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT</span></span><br/><span data-ttu-id="941fe-1035">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-1035">**DWORD**</span></span> | \- | \- | <span data-ttu-id="941fe-1036">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1036">X</span></span> | <span data-ttu-id="941fe-1037">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1037">X</span></span> | \- |
| <span data-ttu-id="941fe-1038">WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ KEEPALIVE \_ INTERVAL</span><span class="sxs-lookup"><span data-stu-id="941fe-1038">WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL</span></span><br/><span data-ttu-id="941fe-1039">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-1039">**DWORD**</span></span> | \- | \- | <span data-ttu-id="941fe-1040">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1040">X</span></span> | <span data-ttu-id="941fe-1041">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1041">X</span></span> | \- |
| <span data-ttu-id="941fe-1042">WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ RECEIVE \_ BUFFER \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="941fe-1042">WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="941fe-1043">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-1043">**DWORD**</span></span> | <span data-ttu-id="941fe-1044">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1044">X</span></span> | <span data-ttu-id="941fe-1045">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1045">X</span></span> | <span data-ttu-id="941fe-1046">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1046">X</span></span> | <span data-ttu-id="941fe-1047">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1047">X</span></span> | <span data-ttu-id="941fe-1048">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="941fe-1048">Windows 8.1</span></span> |
| <span data-ttu-id="941fe-1049">WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ SEND \_ BUFFER \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="941fe-1049">WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="941fe-1050">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-1050">**DWORD**</span></span> | <span data-ttu-id="941fe-1051">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1051">X</span></span> | <span data-ttu-id="941fe-1052">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1052">X</span></span> | <span data-ttu-id="941fe-1053">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1053">X</span></span> | <span data-ttu-id="941fe-1054">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1054">X</span></span> | <span data-ttu-id="941fe-1055">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="941fe-1055">Windows 8.1</span></span> |
| <span data-ttu-id="941fe-1056">ANZAHL VON \_ \_ WINHTTP-OPTION-WORKERTHREADS \_ \_</span><span class="sxs-lookup"><span data-stu-id="941fe-1056">WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT</span></span><br/><span data-ttu-id="941fe-1057">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-1057">**DWORD**</span></span> | \- | \- | \- | <span data-ttu-id="941fe-1058">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1058">X</span></span> | \- |
| <span data-ttu-id="941fe-1059">WINHTTP \_ OPTION \_ WRITE \_ BUFFER \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="941fe-1059">WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="941fe-1060">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="941fe-1060">**DWORD**</span></span> | \- | <span data-ttu-id="941fe-1061">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1061">X</span></span> | <span data-ttu-id="941fe-1062">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1062">X</span></span> | <span data-ttu-id="941fe-1063">X</span><span class="sxs-lookup"><span data-stu-id="941fe-1063">X</span></span> | \- |

> [!Note]
> <span data-ttu-id="941fe-1064">Informationen zu Windows XP und Windows 2000 finden Sie unter [Laufzeitanforderungen.](winhttp-start-page.md)</span><span class="sxs-lookup"><span data-stu-id="941fe-1064">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="941fe-1065">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="941fe-1065">Requirements</span></span>

| <span data-ttu-id="941fe-1066">Anforderung</span><span class="sxs-lookup"><span data-stu-id="941fe-1066">Requirement</span></span> | <span data-ttu-id="941fe-1067">Wert</span><span class="sxs-lookup"><span data-stu-id="941fe-1067">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="941fe-1068">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="941fe-1068">Minimum supported client</span></span> | <span data-ttu-id="941fe-1069">Nur Windows XP, Windows 2000 Professional mit \[ SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="941fe-1069">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>            |
| <span data-ttu-id="941fe-1070">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="941fe-1070">Minimum supported server</span></span> | <span data-ttu-id="941fe-1071">Nur Windows Server 2003, Windows 2000 Server mit \[ SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="941fe-1071">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>         |
| <span data-ttu-id="941fe-1072">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="941fe-1072">Redistributable</span></span>          | <span data-ttu-id="941fe-1073">WinHTTP 5.0 und Internet Explorer 5.01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="941fe-1073">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span> |
| <span data-ttu-id="941fe-1074">Header</span><span class="sxs-lookup"><span data-stu-id="941fe-1074">Header</span></span>                   | <span data-ttu-id="941fe-1075">Winhttp.h</span><span class="sxs-lookup"><span data-stu-id="941fe-1075">Winhttp.h</span></span>                                                                       |

## <a name="see-also"></a><span data-ttu-id="941fe-1076">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="941fe-1076">See also</span></span>

[<span data-ttu-id="941fe-1077">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="941fe-1077">WinHTTP Versions</span></span>](winhttp-versions.md)
