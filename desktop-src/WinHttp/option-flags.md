---
Description: Die folgenden Optionsflags werden von WinHttpQueryOption und WinHttpSetOption unterstützt.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Optionsflags (Winhttp.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 91a9506225c53893990d4dcdc534293daa6c8e00
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262062"
---
# <a name="option-flags"></a><span data-ttu-id="47d74-103">Optionsflags</span><span class="sxs-lookup"><span data-stu-id="47d74-103">Option Flags</span></span>

<span data-ttu-id="47d74-104">Die folgenden Optionsflags werden von [**WinHttpQueryOption und**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) [**WinHttpSetOption unterstützt.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)</span><span class="sxs-lookup"><span data-stu-id="47d74-104">The following option flags are supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span>

<dl> <dt>

<span data-ttu-id="47d74-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**\_WINHTTP-OPTION \_ \_ GARANTIERTE NICHT \_ \_ BLOCKIERENDE RÜCKRUFE**</span><span class="sxs-lookup"><span data-stu-id="47d74-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-106">Der Standardwert lautet FALSE.</span><span class="sxs-lookup"><span data-stu-id="47d74-106">The default is FALSE.</span></span> <span data-ttu-id="47d74-107">Wenn der Status auf TRUE festgelegt ist, garantiert WinHTTP den Fortschritt nicht, wenn Statusrückrufe von der Clientanwendung blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-107">If set to TRUE, WinHTTP does not guarantee progress if status callbacks are blocked by the client application.</span></span>

<span data-ttu-id="47d74-108">Die Clientanwendung muss besonders darauf achten, minimale Vorgänge innerhalb des Rückrufs ohne Blockierung durchzuführen, so schnell wie möglich zurückzukehren und insbesondere nicht auf nachfolgende WinHTTP-Aufrufe zu warten.</span><span class="sxs-lookup"><span data-stu-id="47d74-108">The client application must take special care to perform minimal operations within the callback without blocking, returning as quickly as possible, and in particular must not wait for any subsequent WinHTTP calls.</span></span> <span data-ttu-id="47d74-109">Wenn sie diese Richtlinien nicht einfängt, ist es wahrscheinlich, dass es negative Auswirkungen auf die Leistung oder eine potenzielle Anwendung gibt, die nicht mehr funktioniert.</span><span class="sxs-lookup"><span data-stu-id="47d74-109">If it does not follow these guidelines, there is likely to be a negative performance impact or a potential application hang.</span></span> <span data-ttu-id="47d74-110">Wenn diese Option auf die vorgeschriebene Weise verwendet wird, kann sie die Leistung verbessern.</span><span class="sxs-lookup"><span data-stu-id="47d74-110">If used in the prescribed manner, this option may improve performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**RICHTLINIE FÜR \_ DIE AUTOMATISCHE ANMELDUNG DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-112">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Richtlinie für automatische [Anmeldung](authentication-in-winhttp.md) mit einem der folgenden Werte angibt.</span><span class="sxs-lookup"><span data-stu-id="47d74-112">Sets an unsigned long integer value that specifies the [Automatic Logon Policy](authentication-in-winhttp.md) with one of the following values.</span></span>

| <span data-ttu-id="47d74-113">Begriff</span><span class="sxs-lookup"><span data-stu-id="47d74-113">Term</span></span> | <span data-ttu-id="47d74-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47d74-114">Description</span></span> |
|-|-|
| <span data-ttu-id="47d74-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ HIGH</span><span class="sxs-lookup"><span data-stu-id="47d74-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH</span></span> | <span data-ttu-id="47d74-116">Standardanmeldeinformationen werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="47d74-116">Default credentials are not used.</span></span> <span data-ttu-id="47d74-117">Beachten Sie, dass dieses Flag nur wirksam wird, wenn Sie den Server mit dem tatsächlichen Computernamen angeben.</span><span class="sxs-lookup"><span data-stu-id="47d74-117">Note that this flag takes effect only if you specify the server by the actual machine name.</span></span> <span data-ttu-id="47d74-118">Sie wird nicht wirksam, wenn Sie den Server mit "localhost" oder IP-Adresse angeben.</span><span class="sxs-lookup"><span data-stu-id="47d74-118">It will not take effect, if you specify the server by "localhost" or IP address.</span></span> |
| <span data-ttu-id="47d74-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ LOW</span><span class="sxs-lookup"><span data-stu-id="47d74-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW</span></span> | <span data-ttu-id="47d74-120">Für alle Anforderungen wird eine authentifizierte Anmeldung mit den Standardanmeldeinformationen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="47d74-120">An authenticated log on using the default credentials is performed for all requests.</span></span> |
| <span data-ttu-id="47d74-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ MEDIUM</span><span class="sxs-lookup"><span data-stu-id="47d74-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM</span></span> | <span data-ttu-id="47d74-122">Eine authentifizierte Anmeldung mit den Standardanmeldeinformationen wird nur für Anforderungen im lokalen Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47d74-122">An authenticated log on using the default credentials is performed only for requests on the local Intranet.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="47d74-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**\_ \_ WINHTTP-OPTIONSRÜCKRUF**</span><span class="sxs-lookup"><span data-stu-id="47d74-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-124">Ruft den Zeiger auf den Rückruffunktionssatz mit [**WinHttpSetStatusCallback ab.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)</span><span class="sxs-lookup"><span data-stu-id="47d74-124">Retrieves the pointer to the callback function set with [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP \_ OPTION \_ CLIENT \_ CERT \_ CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="47d74-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-126">Legt den Clientzertifikatkontext fest.</span><span class="sxs-lookup"><span data-stu-id="47d74-126">Sets the client certificate context.</span></span> <span data-ttu-id="47d74-127">Wenn eine Anwendung [**DEN FEHLER \_ WINHTTP CLIENT \_ \_ AUTH \_ CERT \_ NEEDED**](error-messages.md)empfängt, muss sie [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) aufrufen, um ein Zertifikat zur Verfügung zu stellen, bevor die Anforderung erneut ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47d74-127">If an application receives [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md), it must call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="47d74-128">Im Rahmen der Verarbeitung dieser Option ruft WinHttp [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) im vom Aufrufer bereitgestellten Zertifikatkontext auf, damit der Zertifikatkontext unabhängig vom Aufrufer freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="47d74-128">As a part of processing this option, WinHttp calls [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) on the caller-provided certificate context so that the certificate context can be independently released by the caller.</span></span>

> [!Note]
> <span data-ttu-id="47d74-129">Die Anwendung sollte nicht versuchen, den Zertifikatspeicher mit dem Flag CERT CLOSE STORE FORCE FLAG im Aufruf von \_ \_ \_ \_ [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) in dem Zertifikatspeicher zu schließen, aus dem der Zertifikatkontext abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="47d74-129">The application should not attempt to close the certificate store with the CERT\_CLOSE\_STORE\_FORCE\_FLAG flag in the call to [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) on the certificate store from which the certificate context was retrieved.</span></span> <span data-ttu-id="47d74-130">Es kann zu einer Zugriffsverletzung kommen.</span><span class="sxs-lookup"><span data-stu-id="47d74-130">An access violation may occur.</span></span>

<span data-ttu-id="47d74-131">Wenn der Server ein Clientzertifikat anfordert, [**gibt WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)oder [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) einen [**ERROR \_ WINHTTP CLIENT \_ \_ AUTH \_ CERT \_ NEEDED-Fehler**](error-messages.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="47d74-131">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md) error.</span></span> <span data-ttu-id="47d74-132">Wenn der Server das Zertifikat an fordert, es aber nicht erfordert, kann die Anwendung diese Option angeben, um anzugeben, dass er kein Zertifikat hat.</span><span class="sxs-lookup"><span data-stu-id="47d74-132">If the server requests the certificate but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="47d74-133">Der Server kann ein anderes Authentifizierungsschema auswählen oder anonymen Zugriff auf den Server zulassen.</span><span class="sxs-lookup"><span data-stu-id="47d74-133">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="47d74-134">Die Anwendung stellt das **WINHTTP \_ NO CLIENT \_ \_ CERT \_ CONTEXT-Makro** im *lpBuffer-Parameter* von [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) wie im folgenden Codebeispiel gezeigt zur Anwendung.</span><span class="sxs-lookup"><span data-stu-id="47d74-134">The application provides the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

<span data-ttu-id="47d74-135">Wenn der Server ein Clientzertifikat erfordert, kann er als Antwort den HTTP-Statuscode 403 senden.</span><span class="sxs-lookup"><span data-stu-id="47d74-135">If the server requires a client certificate, it may send a 403 HTTP status code in response.</span></span> <span data-ttu-id="47d74-136">Weitere Informationen finden Sie unter DER **OPTION WINHTTP \_ OPTION CLIENT \_ \_ CERT ISSUER \_ \_ LIST.**</span><span class="sxs-lookup"><span data-stu-id="47d74-136">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**\_WINHTTP-OPTION \_ \_ CLIENTZERTIFIKATAUSSTELLERLISTE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-138">Ruft eine [**SecPkgContext \_ IssuerListInfoEx-Struktur**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) ab, wenn der Fehler aus [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) oder [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) **ERROR \_ WINHTTP CLIENT \_ \_ AUTH \_ CERT NEEDED \_ lautet.**</span><span class="sxs-lookup"><span data-stu-id="47d74-138">Retrieves a [**SecPkgContext\_IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure when the error from [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) is **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="47d74-139">Die Ausstellerliste in der Struktur enthält eine Liste der zulässigen Zertifizierungsstellen (Certificate Authorities, CA) vom Server.</span><span class="sxs-lookup"><span data-stu-id="47d74-139">The issuer list in the structure contains a list of acceptable Certificate Authorities (CA) from the server.</span></span> <span data-ttu-id="47d74-140">Die Clientanwendung kann die Zertifizierungsstellenliste filtern, um das Clientzertifikat für die SSL-Authentifizierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="47d74-140">The client application can filter the CA list to retrieve the client certificate for SSL authentication.</span></span>

<span data-ttu-id="47d74-141">Alternativ kann die Anwendung [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit der OPTION **WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ CONTEXT** aufrufen, wenn der Server das Clientzertifikat an fordert, es aber nicht erfordert.</span><span class="sxs-lookup"><span data-stu-id="47d74-141">Alternately, if the server requests the client certificate, but does not require it, the application can call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="47d74-142">Weitere Informationen finden Sie unter DER **OPTION WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ CONTEXT.**</span><span class="sxs-lookup"><span data-stu-id="47d74-142">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**\_ \_ WINHTTP-OPTIONSCODEPAGE**</span><span class="sxs-lookup"><span data-stu-id="47d74-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-144">Legt die [*Codepage fest,*](glossary.md) die zum Verarbeiten der URL verwendet wird (d. h. Abfragezeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="47d74-144">Sets the [*code page*](glossary.md) that is used to process the URL (that is, query string).</span></span> <span data-ttu-id="47d74-145">Der Standardwert ist UTF8.</span><span class="sxs-lookup"><span data-stu-id="47d74-145">The default is UTF8.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_WINHTTP-OPTION: \_ \_ KONFIGURIEREN DER \_ PASSPORT-AUTHENTIFIZIERUNG**</span><span class="sxs-lookup"><span data-stu-id="47d74-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-147">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, ob [die Passport-Authentifizierung in der WinHTTP-Authentifizierung](passport-authentication-in-winhttp.md) aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="47d74-147">Sets an unsigned long integer value that specifies whether [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md) authentication is enabled.</span></span> <span data-ttu-id="47d74-148">Der Wert kann in folgenden Formen vorliegen:</span><span class="sxs-lookup"><span data-stu-id="47d74-148">The value can be one of the following:</span></span>

| <span data-ttu-id="47d74-149">Begriff</span><span class="sxs-lookup"><span data-stu-id="47d74-149">Term</span></span> | <span data-ttu-id="47d74-150">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47d74-150">Description</span></span> |
|-|-|
| <span data-ttu-id="47d74-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ DEAKTIVIEREN \_ DER \_ PASSPORT-AUTHENTIFIZIERUNG</span><span class="sxs-lookup"><span data-stu-id="47d74-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP\_DISABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="47d74-152">Microsoft Passport Authentifizierung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="47d74-152">Microsoft Passport authentication is disabled.</span></span> <span data-ttu-id="47d74-153">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="47d74-153">This is the default.</span></span> |
| <span data-ttu-id="47d74-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ DEAKTIVIEREN VON PASSPORT \_ \_ KEYRING</span><span class="sxs-lookup"><span data-stu-id="47d74-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP\_DISABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="47d74-155">Der Passport-Schlüsselring ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="47d74-155">The Passport keyring is disabled.</span></span> <span data-ttu-id="47d74-156">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="47d74-156">This is the default.</span></span> |
| <span data-ttu-id="47d74-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ AUTH</span><span class="sxs-lookup"><span data-stu-id="47d74-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP\_ENABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="47d74-158">Die Passport-Authentifizierung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="47d74-158">Passport authentication is enabled.</span></span> |
| <span data-ttu-id="47d74-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ KEYRING</span><span class="sxs-lookup"><span data-stu-id="47d74-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP\_ENABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="47d74-160">Der Passport-Schlüsselring ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="47d74-160">The Passport keyring is enabled.</span></span> |

</dl> </dd> <dt>

<span data-ttu-id="47d74-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**\_WINHTTP-OPTION \_ – \_ VERBINDUNGS-RETRIES**</span><span class="sxs-lookup"><span data-stu-id="47d74-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-162">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Anzahl der Versuche vonWinHTTP enthält, eine Verbindung mit einem Host herzustellen, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="47d74-162">Sets or retrieves an unsigned long integer value that contains the number of timesWinHTTP attempts to connect to a host.</span></span> <span data-ttu-id="47d74-163">Microsoft Windows HTTP Services (WinHTTP) versucht nur einmal pro IP-Adresse (InternetProtokoll).</span><span class="sxs-lookup"><span data-stu-id="47d74-163">Microsoft Windows HTTP Services (WinHTTP) only attempts once per Internet Protocol (IP) address.</span></span> <span data-ttu-id="47d74-164">Wenn Sie beispielsweise versuchen, eine Verbindung mit einem mehrfach vernetzten Host herzustellen, der über 10 IP-Adressen verfügt und **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** auf 7 festgelegt ist, versucht WinHTTP nur, eine Verbindung mit den ersten sieben IP-Adressen herzustellen.</span><span class="sxs-lookup"><span data-stu-id="47d74-164">For example, if you attempt to connect to a multihomed host that has 10 IP addresses and **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 7, then WinHTTP only attempts to connect to the first seven IP address.</span></span> <span data-ttu-id="47d74-165">Wenn **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** auf 20 festgelegt ist, versucht WinHTTP bei 10 IP-Adressen nur einmal, jede der zehn IP-Adressen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="47d74-165">Given the same set of 10 IP addresses, if **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 20, WinHTTP attempts each of the 10 only once.</span></span> <span data-ttu-id="47d74-166">Wenn ein Verbindungsversuch nach der angegebenen Anzahl von Versuchen weiterhin fehlschlägt oder das Verbindungszeitout vor diesem Zeitpunkt abgelaufen ist, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="47d74-166">If a connection attempt still fails after the specified number of attempts, or if the connect timeout expired before then, the request is canceled.</span></span> <span data-ttu-id="47d74-167">Der Standardwert für **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** ist fünf Versuche.</span><span class="sxs-lookup"><span data-stu-id="47d74-167">The default value for **WINHTTP\_OPTION\_CONNECT\_RETRIES** is five attempts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP \_ OPTION \_ CONNECT \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="47d74-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-169">Legt einen ganzzahligen Wert ohne Vorzeichen, der den Time out-Wert enthält, in Millisekunden fest oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="47d74-169">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds.</span></span> <span data-ttu-id="47d74-170">Wenn Sie diese Option auf unendlich (0xFFFFFFFF) festlegen, wird dieser Timer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="47d74-170">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="47d74-171">Wenn eine TCP-Verbindungsanforderung länger als dieser Time out-Wert dauert, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="47d74-171">If a TCP connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="47d74-172">Das Standard-Timeout beträgt 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="47d74-172">The default timeout is 60 seconds.</span></span> <span data-ttu-id="47d74-173">Wenn Sie versuchen, eine Verbindung mit mehreren IP-Adressen für einen einzelnen Host (einen mehrfach vernetzten Host) herzustellen, gilt das Timeoutlimit für jede einzelne Verbindung.</span><span class="sxs-lookup"><span data-stu-id="47d74-173">When you are attempting to connect to multiple IP addresses for a single host (a multihomed host), the timeout limit is for each individual connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**VERBINDUNGSINFORMATIONEN \_ ZUR WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP\_OPTION\_CONNECTION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-175">Ruft die Quell- und Ziel-IP-Adresse und den Port der Anforderung ab, die die Antwort generiert hat, wenn [**WinHttpReceiveResponse zurückgegeben**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) wird.</span><span class="sxs-lookup"><span data-stu-id="47d74-175">Retrieves the source and destination IP address, and port of the request that generated the response when [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns.</span></span> <span data-ttu-id="47d74-176">Die Anwendung ruft [**WinHttpQueryOption mit**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) der **OPTION WINHTTP OPTION CONNECTION \_ \_ \_ INFO** auf und stellt die [**WINHTTP CONNECTION \_ \_ INFO-Struktur**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) im *lpBuffer-Parameter* zur Auswahl.</span><span class="sxs-lookup"><span data-stu-id="47d74-176">The application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CONNECTION\_INFO** option, and provides the [**WINHTTP\_CONNECTION\_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) structure in the *lpBuffer* parameter.</span></span> <span data-ttu-id="47d74-177">Weitere Informationen finden Sie unter **WINHTTP \_ CONNECTION \_ INFO**.</span><span class="sxs-lookup"><span data-stu-id="47d74-177">For more information, see **WINHTTP\_CONNECTION\_INFO**.</span></span>

<span data-ttu-id="47d74-178">**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="47d74-178">**Windows Server 2003 with SP1 and Windows XP with SP2:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V0**</span><span class="sxs-lookup"><span data-stu-id="47d74-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V0**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-180">Retreives die [**TCP \_ INFO \_ v0-Struktur**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) für die zugrunde liegende Verbindung, die von der Anforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="47d74-180">Retreives the [**TCP\_INFO\_v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="47d74-181">Die zurückgegebene Struktur kann Statistiken aus vorherigen Anforderungen enthalten, die über dieselbe Verbindung gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="47d74-181">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>

> [!Note]
> <span data-ttu-id="47d74-182">Diese Option wurde durch **WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1 ersetzt.**</span><span class="sxs-lookup"><span data-stu-id="47d74-182">This option has been superseded by **WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1**</span><span class="sxs-lookup"><span data-stu-id="47d74-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-184">Retreives die [**TCP \_ INFO \_ v1-Struktur**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) für die zugrunde liegende Verbindung, die von der Anforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="47d74-184">Retreives the [**TCP\_INFO\_v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="47d74-185">Die zurückgegebene Struktur kann Statistiken aus vorherigen Anforderungen enthalten, die über dieselbe Verbindung gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="47d74-185">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**KONTEXTWERT \_ DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-187">Legt eine **\_ DWORD-PTR fest** oder ruft sie ab, die einen Zeiger auf den Kontextwert enthält, der diesem [HINTERNET-Handle zugeordnet](hinternet-handles-in-winhttp.md) ist.</span><span class="sxs-lookup"><span data-stu-id="47d74-187">Sets or retrieves a **DWORD\_PTR** that contains a pointer to the context value associated with this [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span> <span data-ttu-id="47d74-188">Der im Puffer gespeicherte Wert wird verwendet, und dem **Optionsflag WINHTTP \_ OPTION CONTEXT \_ \_ VALUE** wird ein neuer Wert zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="47d74-188">The value stored in the buffer is used and the **WINHTTP\_OPTION\_CONTEXT\_VALUE** option flag is assigned a new value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**DEKOMPRIMIERUNG \_ DER WINHTTP-OPTION \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP\_OPTION\_DECOMPRESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-190">Legt ein DWORD von Flags fest, die bestimmen, ob WinHTTP Antwortkörper automatisch mit komprimierten Inhaltscodierungen dekomprimiert.</span><span class="sxs-lookup"><span data-stu-id="47d74-190">Sets a DWORD of flags which determine whether WinHTTP will automatically decompress response bodies with compressed Content-Encodings.</span></span> <span data-ttu-id="47d74-191">WinHTTP wird auch einen geeigneten Accept-Encoding festlegen und alle vom Aufrufer bereitgestellten überschreiben.</span><span class="sxs-lookup"><span data-stu-id="47d74-191">WinHTTP will also set an appropriate Accept-Encoding header, overriding any supplied by the caller.</span></span> <span data-ttu-id="47d74-192">Diese Werte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="47d74-192">Supported values are:</span></span>

| <span data-ttu-id="47d74-193">Begriff</span><span class="sxs-lookup"><span data-stu-id="47d74-193">Term</span></span> | <span data-ttu-id="47d74-194">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47d74-194">Description</span></span> |
|-|-|
| <span data-ttu-id="47d74-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>\_WINHTTP-DEKOMPRIMIERUNGSFLAG \_ \_ GZIP</span><span class="sxs-lookup"><span data-stu-id="47d74-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP\_DECOMPRESSION\_FLAG\_GZIP</span></span> | <span data-ttu-id="47d74-196">Dekomprimieren der Inhaltscodierung: gzip-Antworten.</span><span class="sxs-lookup"><span data-stu-id="47d74-196">Decompress Content-Encoding: gzip responses.</span></span> |
| <span data-ttu-id="47d74-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>DEFLATE DES \_ WINHTTP-DEKOMPRIMIERUNGSFLAGS \_ \_</span><span class="sxs-lookup"><span data-stu-id="47d74-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP\_DECOMPRESSION\_FLAG\_DEFLATE</span></span> | <span data-ttu-id="47d74-198">Dekomprimieren der Inhaltscodierung: Verfeinern von Antworten.</span><span class="sxs-lookup"><span data-stu-id="47d74-198">Decompress Content-Encoding: deflate responses.</span></span> |
| <span data-ttu-id="47d74-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>\_WINHTTP-DEKOMPRIMIERUNGSFLAG \_ \_ ALL</span><span class="sxs-lookup"><span data-stu-id="47d74-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP\_DECOMPRESSION\_FLAG\_ALL</span></span> | <span data-ttu-id="47d74-200">Dekomprimieren Sie Antworten mit allen unterstützten Inhaltscodierungen.</span><span class="sxs-lookup"><span data-stu-id="47d74-200">Decompress responses with any supported Content-Encoding.</span></span> |

<span data-ttu-id="47d74-201">Standardmäßig liefert WinHTTP komprimierte Antworten unverändert an den Aufrufer.</span><span class="sxs-lookup"><span data-stu-id="47d74-201">By default, WinHTTP will deliver compressed responses to the caller unmodified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**FUNKTION \_ "WINHTTP-OPTION \_ \_ DEAKTIVIEREN"**</span><span class="sxs-lookup"><span data-stu-id="47d74-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP\_OPTION\_DISABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-203">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, welche Features mit mindestens einem der folgenden Flags deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-203">Sets an unsigned long integer value that specifies which features are disabled with one or more of the following flags.</span></span> <span data-ttu-id="47d74-204">Beachten Sie, dass dieses Feature nur bei Anforderungshandles an [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) übergeben werden sollte, nachdem das Anforderungshandles mit [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellt wurde und bevor die Anforderung mit [**WinHttpSendRequest gesendet wird.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="47d74-204">Be aware that this feature should only be passed to [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) on request handles after the request handle is created with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), and before the request is sent with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

| <span data-ttu-id="47d74-205">Begriff</span><span class="sxs-lookup"><span data-stu-id="47d74-205">Term</span></span> | <span data-ttu-id="47d74-206">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47d74-206">Description</span></span> |
|-|-|
| <span data-ttu-id="47d74-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP \_ DISABLE \_ AUTHENTICATION</span><span class="sxs-lookup"><span data-stu-id="47d74-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP\_DISABLE\_AUTHENTICATION</span></span> | <span data-ttu-id="47d74-208">Die automatische Authentifizierung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="47d74-208">Automatic authentication is disabled.</span></span> |
| <span data-ttu-id="47d74-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP \_ DEAKTIVIEREN VON \_ COOKIES</span><span class="sxs-lookup"><span data-stu-id="47d74-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP\_DISABLE\_COOKIES</span></span> | <span data-ttu-id="47d74-210">Das automatische Hinzufügen von Cookieheadern zu Anforderungen ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="47d74-210">Automatic addition of cookie headers to requests is disabled.</span></span> <span data-ttu-id="47d74-211">Außerdem werden zurückgegebene Cookies nicht automatisch zur Cookiedatenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="47d74-211">Also, returned cookies are not automatically added to the cookie database.</span></span> <span data-ttu-id="47d74-212">Das Deaktivieren von Cookies kann zu einer schlechten Leistung bei der Passport-Authentifizierung führen.</span><span class="sxs-lookup"><span data-stu-id="47d74-212">Disabling cookies can result in poor performance for Passport authentication.</span></span> |
| <span data-ttu-id="47d74-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ DISABLE \_ KEEP \_ ALIVE</span><span class="sxs-lookup"><span data-stu-id="47d74-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP\_DISABLE\_KEEP\_ALIVE</span></span> | <span data-ttu-id="47d74-214">Deaktiviert die Keep-Alive-Semantik für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="47d74-214">Disables keep-alive semantics for the connection.</span></span> <span data-ttu-id="47d74-215">Keep-Alive-Semantik ist für MSN, NTLM und andere Authentifizierungstypen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="47d74-215">Keep-alive semantics are required for MSN, NTLM, and other types of authentication.</span></span> |
| <span data-ttu-id="47d74-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>\_WINHTTP: DEAKTIVIEREN \_ VON UMLEITUNGEN</span><span class="sxs-lookup"><span data-stu-id="47d74-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP\_DISABLE\_REDIRECTS</span></span> | <span data-ttu-id="47d74-217">Die automatische Umleitung ist deaktiviert, wenn Anforderungen mit [**WinHttpSendRequest gesendet werden.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="47d74-217">Automatic redirection is disabled when sending requests with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="47d74-218">Wenn die automatische Umleitung deaktiviert ist, muss eine Anwendung eine Rückruffunktion registrieren, damit die Passport-Authentifizierung erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="47d74-218">If automatic redirection is disabled, an application must register a callback function in order for Passport authentication to succeed.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="47d74-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**\_WINHTTP-OPTION: \_ DEAKTIVIEREN DES \_ \_ \_ FALLBACKS DES SICHEREN PROTOKOLLS**</span><span class="sxs-lookup"><span data-stu-id="47d74-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-220">Verhindert, dass WinHTTP eine Verbindung mit einer niedrigeren Version des Sicherheitsprotokolls erneut versucht, wenn die erste Protokollaushandlung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="47d74-220">Prevents WinHTTP from retrying a connection with a lower version of the security protocol when the initial protocol negotiation fails.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP-OPTION \_ \_ \_ STREAMWARTESCHLANGE \_ DEAKTIVIEREN**</span><span class="sxs-lookup"><span data-stu-id="47d74-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-222">Ermöglicht es neuen Anforderungen, eine zusätzliche HTTP/2-Verbindung zu öffnen, wenn die maximale Anzahl gleichzeitiger Streams erreicht ist, anstatt auf den nächsten verfügbaren Stream für eine vorhandene Verbindung zu warten.</span><span class="sxs-lookup"><span data-stu-id="47d74-222">Allows new requests to open an additional HTTP/2 connection when the maximum concurrent stream limit is reached, rather than waiting for the next available stream on an existing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**FEATURE \_ "WINHTTP-OPTION \_ \_ AKTIVIEREN"**</span><span class="sxs-lookup"><span data-stu-id="47d74-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP\_OPTION\_ENABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-224">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die derzeit aktivierten Funktionen angibt.</span><span class="sxs-lookup"><span data-stu-id="47d74-224">Sets an unsigned long integer value that specifies the features currently enabled.</span></span> <span data-ttu-id="47d74-225">Kann einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="47d74-225">Can be one of the following values.</span></span>

| <span data-ttu-id="47d74-226">Begriff</span><span class="sxs-lookup"><span data-stu-id="47d74-226">Term</span></span> | <span data-ttu-id="47d74-227">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47d74-227">Description</span></span> |
|-|-|
| <span data-ttu-id="47d74-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVERT \_ IMPERSONATION</span><span class="sxs-lookup"><span data-stu-id="47d74-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP\_ENABLE\_SSL\_REVERT\_IMPERSONATION</span></span> | <span data-ttu-id="47d74-229">Wenn diese Option aktiviert ist, wird der Clientwechsel für die Dauer von SSL-Zertifikatauthentifizierungsvorgängen vorübergehend von WinHTTP rückgängig machen.</span><span class="sxs-lookup"><span data-stu-id="47d74-229">If enabled, WinHTTP temporarily reverts client impersonation for the duration of SSL certificate authentication operations.</span></span> <span data-ttu-id="47d74-230">Dieser Wert kann nur für das Sitzungshand handle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-230">This value can be set only on the session handle.</span></span> |
| <span data-ttu-id="47d74-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ AKTIVIEREN DER \_ \_ SSL-SPERRUNG</span><span class="sxs-lookup"><span data-stu-id="47d74-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP\_ENABLE\_SSL\_REVOCATION</span></span> | <span data-ttu-id="47d74-232">Wenn diese Option aktiviert ist, lässt WinHTTP die SSL-Sperrung zu.</span><span class="sxs-lookup"><span data-stu-id="47d74-232">If enabled, WinHTTP allows SSL revocation.</span></span> <span data-ttu-id="47d74-233">Dieser Wert kann nur für das Anforderungshand handle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-233">This value can be set only on the request handle.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP-OPTION \_ \_ \_ HTTP-PROTOKOLL \_ AKTIVIEREN**</span><span class="sxs-lookup"><span data-stu-id="47d74-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-235">Legt eine DWORD-Bitmaske zulässiger erweiterter HTTP-Versionen fest.</span><span class="sxs-lookup"><span data-stu-id="47d74-235">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="47d74-236">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="47d74-236">Possible values are:</span></span>

| <span data-ttu-id="47d74-237">Begriff</span><span class="sxs-lookup"><span data-stu-id="47d74-237">Term</span></span> | <span data-ttu-id="47d74-238">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47d74-238">Description</span></span> |
|-|-|
| <span data-ttu-id="47d74-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>\_ \_ WINHTTP-PROTOKOLLFLAG \_ HTTP2 (0x1)</span><span class="sxs-lookup"><span data-stu-id="47d74-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP\_PROTOCOL\_FLAG\_HTTP2 (0x1)</span></span> | <span data-ttu-id="47d74-240">Aktiviert HTTP/2 für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="47d74-240">Enables HTTP/2 for the request.</span></span> |
| <span data-ttu-id="47d74-241">Keine (0x0)</span><span class="sxs-lookup"><span data-stu-id="47d74-241">None (0x0)</span></span> | <span data-ttu-id="47d74-242">Schränkt die Anforderung auf HTTP/1.1 und früher ein.</span><span class="sxs-lookup"><span data-stu-id="47d74-242">Restricts the request to HTTP/1.1 and prior.</span></span> |

<span data-ttu-id="47d74-243">Ältere Versionen von HTTP (1.1 und früher) können mit dieser Option nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-243">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="47d74-244">Der Standardwert ist 0x0.</span><span class="sxs-lookup"><span data-stu-id="47d74-244">The default is 0x0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-245"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**\_WINHTTP-OPTION \_ \_ HTTP2 \_ PLUS CLIENT \_ \_ CERT AKTIVIEREN**</span><span class="sxs-lookup"><span data-stu-id="47d74-245"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="47d74-246">Diese Option kann für ein WinHttp-Sitzungshand handle festgelegt werden, damit WinHttp den vom Aufrufer bereitgestellten Clientzertifikatkontext verwenden kann, wenn HTTP/2 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="47d74-246">This option can be set on a WinHttp session handle to allow WinHttp to use the caller-provided client certificate context when HTTP/2 is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-247"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**\_WINHTTP-OPTION \_ ENABLETRACING**</span><span class="sxs-lookup"><span data-stu-id="47d74-247"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP\_OPTION\_ENABLETRACING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-248">Legt einen **BOOL-Wert** fest, der angibt, ob die Ablaufverfolgung derzeit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="47d74-248">Sets a **BOOL** value that specifies whether tracing is currently enabled.</span></span> <span data-ttu-id="47d74-249">Weitere Informationen zur Ablaufverfolgungseinrichtung in WinHTTP finden Sie unter [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="47d74-249">For more information about the trace facility in WinHTTP, see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span> <span data-ttu-id="47d74-250">Diese Option kann nur für ein **NULL** **HINTERNET-Handle festgelegt** werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-250">This option can only be set on a **NULL** **HINTERNET** handle.</span></span>


</dt> </dl> </dd>

<dt>

<span data-ttu-id="47d74-251"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP \_ OPTION \_ ENCODE \_ EXTRA**</span><span class="sxs-lookup"><span data-stu-id="47d74-251"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-252">Aktiviert die URL-Prozentcodierung für Pfad und Abfragezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="47d74-252">Enables URL percent encoding for path and query string.</span></span>

<span data-ttu-id="47d74-253">Alternativ können Sie vor dem Aufrufen von WinHttp prozentweise codieren.</span><span class="sxs-lookup"><span data-stu-id="47d74-253">Alternatively, you can percent encode before calling WinHttp.</span></span>

</dt> </dl> </dd>

<dt>

<span data-ttu-id="47d74-254"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP-OPTION \_ \_ VERBINDUNG \_ ABLAUFEN**</span><span class="sxs-lookup"><span data-stu-id="47d74-254"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP\_OPTION\_EXPIRE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-255">Diese Option kann nur für ein Anforderungshand handle festgelegt werden, das noch aktiv ist (senden oder empfangen).</span><span class="sxs-lookup"><span data-stu-id="47d74-255">This option can only be set on a request handle which is still active (sending or receiving).</span></span> <span data-ttu-id="47d74-256">Wenn Sie diese Option festlegen, wird WinHttp dazu veranschlagen, die Verarbeiten von Anforderungen für die Verbindung zu beenden, die dem übergebenen Anforderungshand handle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="47d74-256">Setting this option will tell WinHttp to stop serving requests on the connection associated with the request handle passed in.</span></span> <span data-ttu-id="47d74-257">Die Verbindung wird geschlossen, nachdem das Anforderungshand handle, mit dem diese Option aufgerufen wird, abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="47d74-257">The connection will be closed after the request handle this option is called with is completed.</span></span> <span data-ttu-id="47d74-258">Bei dieser Option werden keine Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="47d74-258">This option does not take any parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-259"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**ERWEITERTER \_ FEHLER DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-259"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-260">Ruft einen ganzzahligen Wert ohne Vorzeichen ab, der einen Microsoft Windows Sockets-Fehlercode enthält, der den ZULETZT in diesem Threadkontext zurückgegebenen \_ ERROR WINHTTP-Fehlermeldungen \_ \* zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="47d74-260">Retrieves an unsigned long integer value that contains a Microsoft Windows Sockets error code that was mapped to the ERROR\_WINHTTP\_\* error messages last returned in this thread context.</span></span> <span data-ttu-id="47d74-261">Sie können **NULL als** Handlewert übergeben.</span><span class="sxs-lookup"><span data-stu-id="47d74-261">You can pass **NULL** as the handle value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-262"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**GLOBALE \_ PROXY-ANMELDEINFORMATIONEN FÜR DIE \_ \_ \_ WINHTTP-OPTION**</span><span class="sxs-lookup"><span data-stu-id="47d74-262"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-263">Verwendet einen Zeiger auf eine [**WINHTTP \_ CREDS \_ EX-Struktur,**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) bei der der *hInternet-Funktionsparameter* auf **NULL festgelegt ist.**</span><span class="sxs-lookup"><span data-stu-id="47d74-263">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="47d74-264">Diese Option erfordert den Registrierungsschlüssel **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="47d74-264">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="47d74-265">Wenn dieser Registrierungsschlüssel nicht festgelegt ist, gibt WinHTTP den Fehler **\_ ERROR WINHTTP INVALID OPTION \_ \_ zurück.**</span><span class="sxs-lookup"><span data-stu-id="47d74-265">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="47d74-266">Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="47d74-266">This registry key is not present by default.</span></span> <span data-ttu-id="47d74-267">Wenn sie festgelegt ist, sendet WinINet Anmeldeinformationen an WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="47d74-267">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="47d74-268">Wenn WinHttp eine Authentifizierungsforderung erhält und keine Anmeldeinformationen für das aktuelle Handle festgelegt sind, werden die von WinINet bereitgestellten Anmeldeinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="47d74-268">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="47d74-269">Um Serveranmeldeinformationen zusätzlich zu Proxyanmeldeinformationen gemeinsam zu verwenden, müssen Benutzer **WINHTTP \_ OPTION USE GLOBAL SERVER CREDENTIALS \_ \_ \_ (GLOBALE SERVERANMELDEINFORMATIONEN \_ VERWENDEN) festlegen.**</span><span class="sxs-lookup"><span data-stu-id="47d74-269">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-270"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**\_WINHTTP-OPTION \_ : GLOBALE \_ \_ SERVER-ANMELDEINFORMATIONEN**</span><span class="sxs-lookup"><span data-stu-id="47d74-270"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-271">Verwendet einen Zeiger auf eine [**WINHTTP \_ CREDS \_ EX-Struktur,**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) bei der der *hInternet-Funktionsparameter* auf **NULL festgelegt ist.**</span><span class="sxs-lookup"><span data-stu-id="47d74-271">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="47d74-272">Diese Option erfordert den Registrierungsschlüssel **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="47d74-272">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="47d74-273">Wenn dieser Registrierungsschlüssel nicht festgelegt ist, gibt WinHTTP den Fehler **\_ ERROR WINHTTP INVALID OPTION \_ \_ zurück.**</span><span class="sxs-lookup"><span data-stu-id="47d74-273">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="47d74-274">Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="47d74-274">This registry key is not present by default.</span></span> <span data-ttu-id="47d74-275">Wenn sie festgelegt ist, sendet WinINet Anmeldeinformationen an WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="47d74-275">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="47d74-276">Wenn WinHttp eine Authentifizierungsforderung erhält und keine Anmeldeinformationen für das aktuelle Handle festgelegt sind, werden die von WinINet bereitgestellten Anmeldeinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="47d74-276">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="47d74-277">Um Serveranmeldeinformationen zusätzlich zu Proxyanmeldeinformationen gemeinsam zu verwenden, müssen Benutzer **WINHTTP \_ OPTION USE GLOBAL SERVER CREDENTIALS \_ \_ \_ (GLOBALE SERVERANMELDEINFORMATIONEN \_ VERWENDEN) festlegen.**</span><span class="sxs-lookup"><span data-stu-id="47d74-277">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-278"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**HANDLETYP \_ DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-278"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-279">Ruft einen ganzzahligen Wert ohne Vorzeichen ab, der den Typ des übergebenen [HINTERNET-Handles](hinternet-handles-in-winhttp.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="47d74-279">Retrieves an unsigned long integer value that contains the type of the [HINTERNET](hinternet-handles-in-winhttp.md) handle passed in.</span></span> <span data-ttu-id="47d74-280">Einer der folgenden Werte kann zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="47d74-280">The return value can be one of the following:</span></span>

| <span data-ttu-id="47d74-281">Begriff</span><span class="sxs-lookup"><span data-stu-id="47d74-281">Term</span></span> | <span data-ttu-id="47d74-282">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47d74-282">Description</span></span> |
|-|-|
| <span data-ttu-id="47d74-283"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP \_ HANDLE \_ TYPE \_ CONNECT</span><span class="sxs-lookup"><span data-stu-id="47d74-283"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP\_HANDLE\_TYPE\_CONNECT</span></span> | <span data-ttu-id="47d74-284">Das Handle ist ein Verbindungshand handle.</span><span class="sxs-lookup"><span data-stu-id="47d74-284">The handle is a connection handle.</span></span> |
| <span data-ttu-id="47d74-285"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>\_ \_ WINHTTP-HANDLETYPANFORDERUNG \_</span><span class="sxs-lookup"><span data-stu-id="47d74-285"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP\_HANDLE\_TYPE\_REQUEST</span></span> | <span data-ttu-id="47d74-286">Das Handle ist ein Anforderungshand handle.</span><span class="sxs-lookup"><span data-stu-id="47d74-286">The handle is a request handle.</span></span> |
| <span data-ttu-id="47d74-287"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>SITZUNG MIT \_ \_ WINHTTP-HANDLETYP \_</span><span class="sxs-lookup"><span data-stu-id="47d74-287"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP\_HANDLE\_TYPE\_SESSION</span></span> | <span data-ttu-id="47d74-288">Das Handle ist ein Sitzungshand handle.</span><span class="sxs-lookup"><span data-stu-id="47d74-288">The handle is a session handle.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="47d74-289"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**\_WINHTTP-OPTION \_ \_ HTTP-PROTOKOLL \_ ERFORDERLICH**</span><span class="sxs-lookup"><span data-stu-id="47d74-289"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-290">Verhindert, dass andere Protokollversionen als die von **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL** aktivierten für die Anforderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-290">Prevents protocol versions other than those enabled by **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL** from being used for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-291"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**VERWENDETES \_ \_ HTTP-PROTOKOLL DER \_ WINHTTP-OPTION \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-291"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-292">Ruft ein DWORD ab, das angibt, welche erweiterte HTTP-Version für eine bestimmte Anforderung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="47d74-292">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="47d74-293">Eine Liste der möglichen Werte finden Sie unter **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL**.</span><span class="sxs-lookup"><span data-stu-id="47d74-293">For a list of possible values, see **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-294"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**\_HTTP-VERSION DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-294"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-295">Legt eine HTTP-VERSIONSinformationsstruktur fest, die die unterstützte HTTP-Version enthält, oder ruft sie ab. [**\_ \_**](/windows/win32/api/winhttp/ns-winhttp-http_version_info)</span><span class="sxs-lookup"><span data-stu-id="47d74-295">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) structure that contains the HTTP version being supported.</span></span> <span data-ttu-id="47d74-296">Dies ist eine prozessweite Option. Verwenden **Sie NULL** für das Handle.</span><span class="sxs-lookup"><span data-stu-id="47d74-296">This is a process-wide option; use **NULL** for the handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-297"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**\_WINHTTP-OPTION \_ HTTP2 \_ KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="47d74-297"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**WINHTTP\_OPTION\_HTTP2\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="47d74-298">Diese Option kann für ein Sitzungshand handle so festgelegt werden, dass WinHttp HTTP/2-PING-Frames als Keepalive-Mechanismus verwendet.</span><span class="sxs-lookup"><span data-stu-id="47d74-298">This option can be set on a session handle to have WinHttp use HTTP/2 PING frames as a keepalive mechanism.</span></span> <span data-ttu-id="47d74-299">Aufrufer geben ein Timeout in Millisekunden an, und wenn für diesen Timeoutzeitraum keine Aktivität für eine Verbindung besteht, beginnt WinHttp mit dem Senden von HTTP/2-PING-Frames.</span><span class="sxs-lookup"><span data-stu-id="47d74-299">Callers specify a timeout in milliseconds, and after there is no activity on a connection for that timeout period, WinHttp will begin to send HTTP/2 PING frames.</span></span> <span data-ttu-id="47d74-300">Aufrufer können keinen Timeoutwert von weniger als 5.000 Millisekunden festlegen.</span><span class="sxs-lookup"><span data-stu-id="47d74-300">Callers cannot set a timeout value less than 5000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-301"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**WINHTTP-OPTION \_ \_ HTTP2 \_ PLUS \_ \_ ÜBERTRAGUNGSCODIERUNG**</span><span class="sxs-lookup"><span data-stu-id="47d74-301"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="47d74-302">Diese Option kann für ein WinHttp-Anforderungshand handle festgelegt werden, um das Verhalten von WinHttp zu steuern, wenn eine HTTP/2-Antwort einen "Transfer-Encoding"-Header enthält.</span><span class="sxs-lookup"><span data-stu-id="47d74-302">This option can be set on a WinHttp request handle to control how WinHttp behaves when an HTTP/2 response contains a "Transfer-Encoding" header.</span></span> <span data-ttu-id="47d74-303">In diesem Fall gibt WinHttp einen Fehler zurück, wenn diese Option auf **FALSE festgelegt ist.**</span><span class="sxs-lookup"><span data-stu-id="47d74-303">In such a case, WinHttp will return an error if this option is set to **FALSE**.</span></span>


</dt> </dl> </dd> <dt>


<span data-ttu-id="47d74-304"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP-OPTION \_ \_ \_ ZERTIFIKATSPERRUNG \_ \_ OFFLINE IGNORIEREN**</span><span class="sxs-lookup"><span data-stu-id="47d74-304"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-305">Ermöglicht sicheren Verbindungen die Verwendung von Sicherheitszertifikaten, für die die Zertifikatsperrliste nicht heruntergeladen werden konnte.</span><span class="sxs-lookup"><span data-stu-id="47d74-305">Allows secure connections to use security certificates for which the certificate revocation list could not be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-306"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP-OPTION \_ \_ IPV6 \_ – SCHNELLER \_ FALLBACK**</span><span class="sxs-lookup"><span data-stu-id="47d74-306"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-307">Aktiviert schnelles IPv6-Fallback (Brillenbrillen) für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="47d74-307">Enables IPv6 fast fallback (Happier Eyeballs) for the connection.</span></span> <span data-ttu-id="47d74-308">Dieses Verhalten ähnelt dem In RFC [6555](https://tools.ietf.org/html/rfc6555) beschriebenen Verhalten von Happy Eyeballs zur Verbesserung der Verbindungszeiten in Netzwerken, in denen IPv6 unzuverlässig ist.</span><span class="sxs-lookup"><span data-stu-id="47d74-308">This behavior is similar to the Happy Eyeballs behavior described in [RFC 6555](https://tools.ietf.org/html/rfc6555) for improving connection times on networks where IPv6 is unreliable.</span></span>
- <span data-ttu-id="47d74-309">Wenn sowohl IPv6- als auch IPv4-Adressen für einen bestimmten Host aufgelöst werden, beginnt WinHttp mit dem Herstellen einer Verbindung mit der ersten aufgelösten IPv6-Adresse mit einem kurzen Timeout (300 ms).</span><span class="sxs-lookup"><span data-stu-id="47d74-309">If both IPv6 and IPv4 addresses are resolved for a given host, WinHttp will begin by connecting to the first resolved IPv6 address with a short (300ms) timeout.</span></span>
- <span data-ttu-id="47d74-310">Sollte diese Verbindung fehlschlagen, versucht WinHttp, eine Verbindung mit der ersten aufgelösten IPv4-Adresse mit dem Standard-Timeout herzustellen.</span><span class="sxs-lookup"><span data-stu-id="47d74-310">Should that connection fail, WinHttp will attempt to connect to the first resolved IPv4 address with the standard timeout.</span></span>
- <span data-ttu-id="47d74-311">Sollte bei der zweiten Verbindung ein Fehler auftäussen, wird von WinHttp die erste aufgelöste IPv6-Adresse mit dem Standard-Timeout erneut verwendet.</span><span class="sxs-lookup"><span data-stu-id="47d74-311">Should the second connection fail, WinHttp will retry the first resolved IPv6 address with the standard timeout.</span></span>
- <span data-ttu-id="47d74-312">Sollte die dritte Verbindung fehlschlagen, wird WinHttp auf das Standardverhalten für alle verbleibenden Adressen zurückverwendet und versucht, eine Verbindung mit jeder Adresse mit dem Standard-Timeout herzustellen, bis eine Verbindung hergestellt wird oder keine Adressen mehr bestehen.</span><span class="sxs-lookup"><span data-stu-id="47d74-312">Should the third connection fail, WinHttp will revert to the default behavior for any remaining addresses, attempting a connection to each one with the standard timeout until a connection is made or no addresses remain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-313"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**\_WINHTTP-OPTION \_ IST PROXY \_ \_ \_ CONNECT-ANTWORT**</span><span class="sxs-lookup"><span data-stu-id="47d74-313"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-314">Ruft ab, ob eine Proxy Return Connect-Antwort abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="47d74-314">Gets whether or not a Proxy Return Connect Response can be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-315"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**\_WINHTTP-OPTION \_ \_ MAX. CONNS \_ PRO \_ 1 \_ 0 \_ SERVER**</span><span class="sxs-lookup"><span data-stu-id="47d74-315"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-316">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die maximale Anzahl von Verbindungen enthält, die pro HTTP/1.0-Server zulässig sind, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="47d74-316">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="47d74-317">Der Standardwert ist **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="47d74-317">The default value is **INFINITE**.</span></span>

<span data-ttu-id="47d74-318">**Windows Vista mit SP1 und Windows Server 2008:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="47d74-318">**Windows Vista with SP1 and Windows Server 2008:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-319"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**\_WINHTTP-OPTION \_ \_ MAX. CONNS \_ PRO \_ SERVER**</span><span class="sxs-lookup"><span data-stu-id="47d74-319"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-320">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die maximal zulässige Anzahl von Verbindungen pro Server enthält, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="47d74-320">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="47d74-321">Der Standardwert ist **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="47d74-321">The default value is **INFINITE**.</span></span>

<span data-ttu-id="47d74-322">Wenn diese Option auf 0 (null) festgelegt ist, legt WinHTTP den Grenzwert für die Anzahl von Verbindungen auf 2 fest.</span><span class="sxs-lookup"><span data-stu-id="47d74-322">When this option is set to zero, WinHTTP sets the limit on the number of connections to 2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-323"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP-OPTION \_ \_ \_ MAX. AUTOMATISCHE \_ \_ HTTP-UMLEITUNGEN**</span><span class="sxs-lookup"><span data-stu-id="47d74-323"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-324">Legt die maximale Anzahl von Umleitungen fest, auf die WinHTTP folgt. Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="47d74-324">Sets the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="47d74-325">Dieser Grenzwert verhindert, dass nicht autorisierte Websites den WinHTTP-Client nach einer großen Anzahl von Umleitungen anhalten.</span><span class="sxs-lookup"><span data-stu-id="47d74-325">This limit prevents unauthorized sites from making the WinHTTP client pause following a large number of redirects.</span></span>

<span data-ttu-id="47d74-326">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="47d74-326">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-327"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**\_WINHTTP-OPTION \_ \_ MAX. \_ HTTP-STATUS \_ CONTINUE**</span><span class="sxs-lookup"><span data-stu-id="47d74-327"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-328">Die maximale Anzahl von 100-199 Statuscodeantworten, die ignoriert wurden, bevor der endgültige Statuscode an den WinHTTP-Client zurücksendet.</span><span class="sxs-lookup"><span data-stu-id="47d74-328">The maximum number of Informational 100-199 status code responses ignored before returning the final status code to the WinHTTP client.</span></span> <span data-ttu-id="47d74-329">Informationsstatuscodes vom Status 100-199 können vom Server vor dem endgültigen Statuscode gesendet werden und werden in der Spezifikation für HTTP/1.1 beschrieben (weitere Informationen finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span><span class="sxs-lookup"><span data-stu-id="47d74-329">Informational 100-199 status codes can be sent by the server before the final status code, and are described in the specification for HTTP/1.1 (for more information, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span></span> <span data-ttu-id="47d74-330">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="47d74-330">The default is 10.</span></span>

<span data-ttu-id="47d74-331">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="47d74-331">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-332"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP \_ OPTION \_ MAX \_ RESPONSE \_ DRAIN \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="47d74-332"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-333">Eine Grenze für die Menge der Daten, die aus Antworten entleert werden, um eine Verbindung wiederzuverwenden, die in Bytes angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="47d74-333">A bound on the amount of data drained from responses in order to reuse a connection, specified in bytes.</span></span> <span data-ttu-id="47d74-334">Der Standardwert ist 1 MB.</span><span class="sxs-lookup"><span data-stu-id="47d74-334">The default is 1MB.</span></span>

<span data-ttu-id="47d74-335">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="47d74-335">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-336"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**MAXIMALE GRÖßE DES \_ \_ \_ \_ ANTWORTHEADERS DER \_ WINHTTP-OPTION**</span><span class="sxs-lookup"><span data-stu-id="47d74-336"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-337">Ein gebundener Satz für die maximale Größe des Headerbereichs der Serverantwort, angegeben in Bytes.</span><span class="sxs-lookup"><span data-stu-id="47d74-337">A bound set on the maximum size of the header portion of the server response, specified in bytes.</span></span> <span data-ttu-id="47d74-338">Diese Gebundene schützt den Client vor einem nicht autorisierten Server, der versucht, den Client zu verhindern, indem eine Antwort mit einer unendlichen Menge von Headerdaten gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="47d74-338">This bound protects the client from an unauthorized server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="47d74-339">Der Standardwert ist 64 KB.</span><span class="sxs-lookup"><span data-stu-id="47d74-339">The default value is 64KB.</span></span>

<span data-ttu-id="47d74-340">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="47d74-340">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-341"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**ÜBERGEORDNETES \_ HANDLE DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-341"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-342">Ruft das übergeordnete Handle für dieses Handle ab.</span><span class="sxs-lookup"><span data-stu-id="47d74-342">Retrieves the parent handle to this handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-343"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**\_WINHTTP-OPTION \_ \_ PASSPORT-COBRANDINGTEXT \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-343"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-344">Ruft eine Zeichenfolge ab, die den [*cobranding-Text*](glossary.md) enthält, der vom Passport-Anmeldeserver bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="47d74-344">Retrieves a string that contains the [*cobranding*](glossary.md) text provided by the Passport logon server.</span></span> <span data-ttu-id="47d74-345">Diese Option sollte sofort abgerufen werden, nachdem der Anmeldeserver mit dem Statuscode 401 reagiert hat.</span><span class="sxs-lookup"><span data-stu-id="47d74-345">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="47d74-346">Eine Anwendung sollte eine Puffergröße in Bytes übergeben, die groß genug ist, um die zurückgegebene Zeichenfolge zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="47d74-346">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-347"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**\_WINHTTP-OPTION \_ \_ PASSPORT-COBRANDING-URL \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-347"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-348">Ruft eine Zeichenfolge ab, die eine URL für eine [*Cobrandinggrafik*](glossary.md) enthält, die vom Passport-Anmeldeserver bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="47d74-348">Retrieves a string that contains a URL for a [*cobranding*](glossary.md) graphic provided by the Passport logon server.</span></span> <span data-ttu-id="47d74-349">Diese Option sollte sofort abgerufen werden, nachdem der Anmeldeserver mit dem Statuscode 401 reagiert hat.</span><span class="sxs-lookup"><span data-stu-id="47d74-349">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="47d74-350">Eine Anwendung sollte eine Puffergröße in Bytes übergeben, die groß genug ist, um die zurückgegebene Zeichenfolge zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="47d74-350">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-351"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**\_WINHTTP-OPTION \_ \_ \_ PASSPORT-RÜCKGABE-URL**</span><span class="sxs-lookup"><span data-stu-id="47d74-351"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-352">Legt eine schreibgeschützte Option für ein Anforderungshandles fest, das die Passport-Rückgabe-URL abruft.</span><span class="sxs-lookup"><span data-stu-id="47d74-352">Sets a read-only option on a request handle that retrieves the Passport return URL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-353"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**\_WINHTTP-OPTION \_ \_ \_ PASSPORT-ABMELDE**</span><span class="sxs-lookup"><span data-stu-id="47d74-353"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-354">Legt die Option für ein Sitzungshand handle zum Abmelden von Passport-Anmeldungen fest.</span><span class="sxs-lookup"><span data-stu-id="47d74-354">Sets the option on a session handle to sign out of any Passport logins.</span></span> <span data-ttu-id="47d74-355">Eine Anwendung sollte die Passport-Rückgabe-URL übergeben, die mit **WINHTTP \_ OPTION PASSPORT RETURN URL abgerufen \_ \_ \_ wurde.**</span><span class="sxs-lookup"><span data-stu-id="47d74-355">An application should pass in the Passport return URL that was retrieved with **WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**.</span></span> <span data-ttu-id="47d74-356">Alle Cookies im Zusammenhang mit der Rückgabe-URL werden wieder löschen.</span><span class="sxs-lookup"><span data-stu-id="47d74-356">All cookies related to the return URL are cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-357"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**\_ \_ WINHTTP-OPTIONSKENNWORT**</span><span class="sxs-lookup"><span data-stu-id="47d74-357"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-358">Legt einen Zeichenfolgenwert fest, der das einem Anforderungshand handle zugeordnete Kennwort enthält, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="47d74-358">Sets or retrieves a string value that contains the password associated with a request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-359"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**\_WINHTTP-OPTIONSPROXY \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-359"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-360">Legt eine [**WINHTTP PROXY \_ \_ INFO-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) fest, die die Proxydaten auf einem vorhandenen Sitzungshand handle oder Anforderungshand handle enthält, oder ruft sie ab.</span><span class="sxs-lookup"><span data-stu-id="47d74-360">Sets or retrieves an [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure that contains the proxy data on an existing session handle or request handle.</span></span> <span data-ttu-id="47d74-361">Beim Abrufen von Proxydaten muss eine Anwendung die in dieser Struktur enthaltenen **lpszProxy-** und **lpszProxyBypass-Zeichenfolgen** (wenn sie nicht NULL **sind)** mithilfe der [**GlobalFree-Funktion**](/windows/desktop/api/winbase/nf-winbase-globalfree) frei geben.</span><span class="sxs-lookup"><span data-stu-id="47d74-361">When retrieving proxy data, an application must free the **lpszProxy** and **lpszProxyBypass** strings contained in this structure (if they are non-**NULL**) using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="47d74-362">Eine Anwendung kann die globalen Proxydaten (den Standardproxy) abfragen, indem sie ein **NULL-Handle** übergibt.</span><span class="sxs-lookup"><span data-stu-id="47d74-362">An application can query for the global proxy data (the default proxy) by passing a **NULL** handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-363"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**\_PROXYKENNWORT \_ FÜR WINHTTP-OPTION \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-363"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-364">Legt einen Zeichenfolgenwert fest, der das Kennwort für den Zugriff auf den Proxy enthält, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="47d74-364">Sets or retrieves a string value that contains the password used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-365"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**VERWENDETER \_ \_ WINHTTP-OPTIONSPROXY-SPN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-365"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WINHTTP\_OPTION\_PROXY\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-366">Ruft den Proxyserverprinzipalnamen ab, den WinHTTP während der Authentifizierung an SSPI übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="47d74-366">Gets the proxy Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="47d74-367">Dieser Zeichenfolgenwert wird verwendet, um nach einem [**Authentifizierungsfehler an SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="47d74-367">This string value is usefor passing to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-368"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**\_PROXYBENUTZERNAME DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-368"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-369">Legt einen Zeichenfolgenwert fest, der den Benutzernamen enthält, der für den Zugriff auf den Proxy verwendet wird, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="47d74-369">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-370"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**\_WINHTTP-OPTION \_ READ BUFFER \_ \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="47d74-370"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-371">Diese Option ist veraltet. es hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="47d74-371">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-372"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP-OPTION \_ \_ "PROXY \_ \_ CONNECT-ANTWORT \_ EMPFANGEN"**</span><span class="sxs-lookup"><span data-stu-id="47d74-372"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-373">Legt fest, ob die Proxyantwortentität abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="47d74-373">Sets whether or not the proxy response entity can be retrieved.</span></span> <span data-ttu-id="47d74-374">Diese Option ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="47d74-374">This option is disabled by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-375"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP-OPTION \_ \_ \_ \_ EMPFANGSANTWORT-TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="47d74-375"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-376">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Timeoutwert in Millisekunden enthält, um auf den Empfang aller Antwortheader für eine Anforderung zu warten, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="47d74-376">Sets or retrieves an unsigned long integer value that contains the timeout value, in milliseconds, to wait to receive all response headers to a request.</span></span> <span data-ttu-id="47d74-377">Wenn WinHTTP nicht alle Header innerhalb dieses Timeoutzeitraums empfangen kann, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="47d74-377">If WinHTTP fails to receive all the headers within this timeout period, the request is canceled.</span></span> <span data-ttu-id="47d74-378">Der Standardwert für das Timeout beträgt 90 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="47d74-378">The default timeout value is 90 seconds.</span></span>

<span data-ttu-id="47d74-379">Dieses Timeout wird nur überprüft, wenn Daten vom Socket empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-379">This timeout is checked only when data is received from the socket.</span></span> <span data-ttu-id="47d74-380">Wenn das Timeout abläuft, wird die Clientanwendung daher erst benachrichtigt, wenn weitere Daten vom Server eintreffen.</span><span class="sxs-lookup"><span data-stu-id="47d74-380">As a result, when the timeout expires the client application is not notified until more data arrives from the server.</span></span> <span data-ttu-id="47d74-381">Wenn keine Daten vom Server eintreffen, kann die Verzögerung zwischen dem Ablauf des Timeouts und der Benachrichtigung der Clientanwendung so groß sein wie der Timeoutwert, der mit dem *dwReceiveTimeout-Parameter* der [**WinHttpSetTimeouts-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="47d74-381">If no data arrives from the server, the delay between the timeout expiration and notification of the client application could be as large as the timeout value set using the *dwReceiveTimeout* parameter of the [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-382"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**\_EMPFANGSZEITÜBERSCHREITUNG DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-382"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-383">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, um eine Teilantwort auf eine Anforderung zu empfangen oder einige Daten zu lesen, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="47d74-383">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a partial response to a request or read some data.</span></span> <span data-ttu-id="47d74-384">Wenn die Antwort länger als dieser Time out-Wert dauert, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="47d74-384">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="47d74-385">Der Standard-Timeoutwert beträgt 30 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="47d74-385">The default timeout value is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-386"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**UMLEITUNGSRICHTLINIE \_ FÜR WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-386"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP\_OPTION\_REDIRECT\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-387">Legt das Verhalten von WinHTTP in Bezug auf die Behandlung eines 30-fachen HTTP-Umleitungsstatuscodes fest.</span><span class="sxs-lookup"><span data-stu-id="47d74-387">Sets the behavior of WinHTTP regarding the handling of a 30x HTTP redirect status code.</span></span> <span data-ttu-id="47d74-388">Diese Option kann für ein Sitzungs- oder Anforderungshand handle auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="47d74-388">This option can be set on a session or request handle to one of the following values:</span></span>

| <span data-ttu-id="47d74-389">Begriff</span><span class="sxs-lookup"><span data-stu-id="47d74-389">Term</span></span> | <span data-ttu-id="47d74-390">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47d74-390">Description</span></span> |
|-|-|
| <span data-ttu-id="47d74-391"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>RICHTLINIE FÜR DIE UMLEITUNG \_ DER WINHTTP-OPTION \_ \_ \_ IMMER</span><span class="sxs-lookup"><span data-stu-id="47d74-391"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_ALWAYS</span></span> | <span data-ttu-id="47d74-392">Alle Umleitungen werden automatisch befolgt.</span><span class="sxs-lookup"><span data-stu-id="47d74-392">All redirects are followed automatically.</span></span> |
| <span data-ttu-id="47d74-393"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>UMLEITUNGSRICHTLINIE \_ FÜR \_ WINHTTP-OPTION: \_ HTTPS ZU HTTP NICHT \_ \_ \_ \_ ZU</span><span class="sxs-lookup"><span data-stu-id="47d74-393"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_DISALLOW\_HTTPS\_TO\_HTTP</span></span> | <span data-ttu-id="47d74-394">Alle Umleitungen werden befolgt, mit Ausnahme der Umleitungen, die von einer sicheren URL (https) zu einer unsicheren URL (HTTP) stammen.</span><span class="sxs-lookup"><span data-stu-id="47d74-394">All redirects are followed, except those that originate from a secure (https) URL to an unsecure (http) URL.</span></span> <span data-ttu-id="47d74-395">Dies ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="47d74-395">This is the default setting.</span></span> |
| <span data-ttu-id="47d74-396"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>UMLEITUNGSRICHTLINIE \_ FÜR WINHTTP-OPTION \_ \_ \_ NIE</span><span class="sxs-lookup"><span data-stu-id="47d74-396"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_NEVER</span></span> | <span data-ttu-id="47d74-397">Umleitungen werden nie befolgt.</span><span class="sxs-lookup"><span data-stu-id="47d74-397">Redirects are never followed.</span></span> <span data-ttu-id="47d74-398">Der 30-fache Status wird an die Anwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47d74-398">The 30x status is returned to the application.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-399"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**\_WINHTTP-OPTION \_ BENUTZER IN URL \_ \_ \_ ABLEHNENPWD**</span><span class="sxs-lookup"><span data-stu-id="47d74-399"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-400">Lehnt URLs ab, die einen Benutzernamen und ein Kennwort enthalten.</span><span class="sxs-lookup"><span data-stu-id="47d74-400">Rejects URLs that contain a username and password.</span></span> <span data-ttu-id="47d74-401">Diese Option lehnt auch URLs ab, die *die Semantik username:password* enthalten, auch wenn kein Benutzername oder Kennwort angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="47d74-401">This option also rejects URLs that contain *username:password* semantics, even if no username or password is specified.</span></span> <span data-ttu-id="47d74-402">Beispielsweise würde " u:p@hostname ", " :@hostname ", " u:@hostname ", " " und " :p@hostname " alle als ungültig gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-402">For example, "u:p@hostname", ":@hostname", "u:@hostname", and ":p@hostname" would all be flagged as invalid.</span></span> <span data-ttu-id="47d74-403">Wenn eine ungültige URL an die Funktion übergeben wird, wird [ERROR \_ WINHTTP \_ INVALID URL \_ zurückgegeben.](error-messages.md)</span><span class="sxs-lookup"><span data-stu-id="47d74-403">If an invalid URL is passed to the function, it returns [ERROR\_WINHTTP\_INVALID\_URL](error-messages.md).</span></span> <span data-ttu-id="47d74-404">Standardmäßig ist diese Option deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="47d74-404">This option is turned off by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-405"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**\_WINHTTP-OPTION \_ – \_ ANFORDERUNGSPRIORITÄT**</span><span class="sxs-lookup"><span data-stu-id="47d74-405"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-406">Diese Option ist veraltet. es hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="47d74-406">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-407"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**\_ \_ WINHTTP-OPTIONSANFORDERUNGSSTATISTIKEN \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-407"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP\_OPTION\_REQUEST\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-408">Retreives-Statistiken für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="47d74-408">Retreives statistics for the request.</span></span>  <span data-ttu-id="47d74-409">Eine Liste der verfügbaren Statistiken finden Sie unter [**WINHTTP \_ REQUEST \_ STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span><span class="sxs-lookup"><span data-stu-id="47d74-409">For a list of the available statistics, see [**WINHTTP\_REQUEST\_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-410"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**ANFORDERUNGSZEITEN \_ DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-410"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP\_OPTION\_REQUEST\_TIMES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-411">Sucht nach Zeitsteuerungsinformationen für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="47d74-411">Retreives timing information for the request.</span></span> <span data-ttu-id="47d74-412">Eine Liste der verfügbaren Zeitsteuerungen finden Sie unter [**WINHTTP \_ REQUEST \_ TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span><span class="sxs-lookup"><span data-stu-id="47d74-412">For a list of the available timings, see [**WINHTTP\_REQUEST\_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-413"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**\_WINHTTP-OPTION \_ " \_ STREAMENDE \_ ERFORDERLICH"**</span><span class="sxs-lookup"><span data-stu-id="47d74-413"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**WINHTTP\_OPTION\_REQUIRE\_STREAM\_END**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="47d74-414">Diese Option weist WinHttp an, "Content-Length"-Antwortheader zu ignorieren und weiterhin in einem Stream zu empfangen, bis das END_STREAM empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="47d74-414">This option tells WinHttp to ignore "Content-Length" response headers, and continue receiving on a stream until the END_STREAM flag is received.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-415"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**HOSTNAME \_ DER WINHTTP-OPTIONSAUFLÖSUNG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-415"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="47d74-416">Diese Option kann für ein WinHttp-Anforderungshand handle festgelegt werden, bevor es gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="47d74-416">This option can be set on a WinHttp request handle before it has been sent.</span></span> <span data-ttu-id="47d74-417">Wenn festgelegt, verwendet WinHttp die vom Aufrufer bereitgestellte Zeichenfolge als Hostnamen für die DNS-Auflösung.</span><span class="sxs-lookup"><span data-stu-id="47d74-417">If set, WinHttp will use the caller-provided string as the hostname for DNS resolution.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-418"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP-OPTION \_ \_ \_ TIMEOUT AUFLÖSEN**</span><span class="sxs-lookup"><span data-stu-id="47d74-418"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP\_OPTION\_RESOLVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-419">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, um einen Hostnamen aufzulösen, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="47d74-419">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to resolve a host name.</span></span> <span data-ttu-id="47d74-420">Der Standardwert für das Timeout ist **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="47d74-420">The default timeout value is **INFINITE**.</span></span> <span data-ttu-id="47d74-421">Wenn ein nicht standardmäßiger Wert angegeben wird, verursacht dies einen Mehraufwand von einer Threaderstellung pro Namensauflösung.</span><span class="sxs-lookup"><span data-stu-id="47d74-421">If a non-default value is specified, there is an overhead of one thread-creation per name resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-422"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**SICHERE PROTOKOLLE \_ DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-422"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP\_OPTION\_SECURE\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-423">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, welche sicheren Protokolle zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="47d74-423">Sets an unsigned long integer value that specifies which secure protocols are acceptable.</span></span> <span data-ttu-id="47d74-424">Standardmäßig sind nur SSL3 und TLS1 in Windows 7 und Windows 8.</span><span class="sxs-lookup"><span data-stu-id="47d74-424">By default only SSL3 and TLS1 are enabled in Windows 7 and Windows 8.</span></span> <span data-ttu-id="47d74-425">Standardmäßig sind nur SSL3, TLS1.0, TLS1.1 und TLS1.2 in Windows 8.1 und Windows 10.</span><span class="sxs-lookup"><span data-stu-id="47d74-425">By default only SSL3, TLS1.0, TLS1.1, and TLS1.2 are enabled in Windows 8.1 and Windows 10.</span></span> <span data-ttu-id="47d74-426">Der Wert kann eine Kombination aus mindestens einem der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="47d74-426">The value can be a combination of one or more of the following values.</span></span>

| <span data-ttu-id="47d74-427">Begriff</span><span class="sxs-lookup"><span data-stu-id="47d74-427">Term</span></span> | <span data-ttu-id="47d74-428">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47d74-428">Description</span></span> |
|-|-|
| <span data-ttu-id="47d74-429"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ ALL</span><span class="sxs-lookup"><span data-stu-id="47d74-429"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_ALL</span></span> | <span data-ttu-id="47d74-430">Die protokolle Secure Sockets Layer (SSL) 2.0, SSL 3.0 und Transport Layer Security (TLS) 1.0 können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-430">The Secure Sockets Layer (SSL) 2.0, SSL 3.0, and Transport Layer Security (TLS) 1.0 protocols can be used.</span></span> |
| <span data-ttu-id="47d74-431"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP-FLAG \_ \_ SECURE PROTOCOL \_ \_ SSL2</span><span class="sxs-lookup"><span data-stu-id="47d74-431"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL2</span></span> | <span data-ttu-id="47d74-432">Das SSL 2.0-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-432">The SSL 2.0 protocol can be used.</span></span> |
| <span data-ttu-id="47d74-433"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP-FLAG \_ \_ SECURE PROTOCOL \_ \_ SSL3</span><span class="sxs-lookup"><span data-stu-id="47d74-433"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL3</span></span> | <span data-ttu-id="47d74-434">Das SSL 3.0-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-434">The SSL 3.0 protocol can be used.</span></span> |
| <span data-ttu-id="47d74-435"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP-FLAG \_ \_ SECURE PROTOCOL \_ \_ TLS1</span><span class="sxs-lookup"><span data-stu-id="47d74-435"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1</span></span> | <span data-ttu-id="47d74-436">Das TLS 1.0-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-436">The TLS 1.0 protocol can be used.</span></span> |
| <span data-ttu-id="47d74-437"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP-FLAG \_ \_ SECURE PROTOCOL \_ \_ TLS1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="47d74-437"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_1</span></span> | <span data-ttu-id="47d74-438">Das TLS 1.1-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-438">The TLS 1.1 protocol can be used.</span></span> |
| <span data-ttu-id="47d74-439"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP-FLAG \_ \_ SECURE PROTOCOL \_ \_ TLS1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="47d74-439"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_2</span></span> | <span data-ttu-id="47d74-440">Das TLS 1.2-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-440">The TLS 1.2 protocol can be used.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="47d74-441"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**\_SICHERHEITSZERTIFIKATSTRUKTUR DER WINHTTP-OPTION \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-441"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-442">Ruft das Zertifikat für einen SSL/TLS-Server in der [**WINHTTP \_ CERTIFICATE \_ INFO-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) ab.</span><span class="sxs-lookup"><span data-stu-id="47d74-442">Retrieves the certificate for a SSL/TLS server into the [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="47d74-443">Die Anwendung muss die **Member lpszSubjectInfo** und **lpszIssuerInfo mit** [**LocalFree frei geben.**](/windows/desktop/api/winbase/nf-winbase-localfree)</span><span class="sxs-lookup"><span data-stu-id="47d74-443">The application must free the **lpszSubjectInfo** and **lpszIssuerInfo** members with [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-444"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**\_SICHERHEITSFLAGS FÜR DIE WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-444"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-445">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Sicherheitsflags für ein Handle enthält, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="47d74-445">Sets or retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="47d74-446">Dabei kann es sich um eine Kombination dieser Werte handelt:</span><span class="sxs-lookup"><span data-stu-id="47d74-446">It can be a combination of these values:</span></span>

| <span data-ttu-id="47d74-447">Begriff</span><span class="sxs-lookup"><span data-stu-id="47d74-447">Term</span></span> | <span data-ttu-id="47d74-448">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47d74-448">Description</span></span> |
|-|-|
| <span data-ttu-id="47d74-449"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>\_ \_ SICHERHEITSFLAG \_ \_ ZERTIFIKAT-CN IGNORIEREN \_ UNGÜLTIG</span><span class="sxs-lookup"><span data-stu-id="47d74-449"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span> |<span data-ttu-id="47d74-450">Lässt einen ungültigen allgemeinen Namen in einem Zertifikat zu. Das heißt, der von der Anwendung angegebene Servername ist nicht mit dem allgemeinen Namen im Zertifikat übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="47d74-450">Allows an invalid common name in a certificate; that is, the server name specified by the application does not match the common name in the certificate.</span></span> <span data-ttu-id="47d74-451">Wenn dieses Flag festgelegt ist, erhält die Anwendung keinen **WINHTTP \_ CALLBACK \_ STATUS FLAG \_ \_ CERT \_ CN \_ INVALID-Rückruf.**</span><span class="sxs-lookup"><span data-stu-id="47d74-451">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_CN\_INVALID** callback.</span></span> |
| <span data-ttu-id="47d74-452"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY \_ FLAG \_ IGNORE \_ CERT \_ DATE \_ INVALID</span><span class="sxs-lookup"><span data-stu-id="47d74-452"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span> |<span data-ttu-id="47d74-453">Lässt ein ungültiges Zertifikatdatum zu, d. b. ein abgelaufenes oder noch nicht effektives Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="47d74-453">Allows an invalid certificate date, that is, an expired or not-yet-effective certificate.</span></span> <span data-ttu-id="47d74-454">Wenn dieses Flag festgelegt ist, erhält die Anwendung keinen **WINHTTP \_ CALLBACK \_ STATUS FLAG \_ \_ CERT DATE \_ \_ INVALID-Rückruf.**</span><span class="sxs-lookup"><span data-stu-id="47d74-454">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_DATE\_INVALID** callback.</span></span> |
| <span data-ttu-id="47d74-455"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>\_ \_ SICHERHEITSFLAG UNBEKANNTE \_ ZERTIFIZIERUNGSSTELLE \_ IGNORIEREN</span><span class="sxs-lookup"><span data-stu-id="47d74-455"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span> | <span data-ttu-id="47d74-456">Lässt eine ungültige Zertifizierungsstelle zu.</span><span class="sxs-lookup"><span data-stu-id="47d74-456">Allows an invalid certificate authority.</span></span> <span data-ttu-id="47d74-457">Wenn dieses Flag festgelegt ist, erhält die Anwendung keinen **WINHTTP \_ CALLBACK \_ STATUS FLAG INVALID \_ \_ \_ CA-Rückruf.**</span><span class="sxs-lookup"><span data-stu-id="47d74-457">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_INVALID\_CA** callback.</span></span> |
| <span data-ttu-id="47d74-458"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>\_SICHERHEITSFLAG : FALSCHE VERWENDUNG DES \_ \_ \_ ZERTIFIKATS \_ IGNORIEREN</span><span class="sxs-lookup"><span data-stu-id="47d74-458"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_CERT\_WRONG\_USAGE</span></span> | <span data-ttu-id="47d74-459">Ermöglicht das Herstellen der Identität eines Servers mit einem Nicht-Serverzertifikat (z. B. einem Clientzertifikat).</span><span class="sxs-lookup"><span data-stu-id="47d74-459">Allows the identity of a server to be established with a non-server certificate (for example, a client certificate).</span></span> |
| <span data-ttu-id="47d74-460"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>\_ \_ SICHERHEITSFLAG SCHWACHE SIGNATUR \_ \_ IGNORIEREN</span><span class="sxs-lookup"><span data-stu-id="47d74-460"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span> | <span data-ttu-id="47d74-461">Ermöglicht das Ignorieren einer schwachen Signatur.</span><span class="sxs-lookup"><span data-stu-id="47d74-461">Allows a weak signature to be ignored.</span></span><br/><span data-ttu-id="47d74-462">Dieses Flag ist im Rollupupdate für jedes Betriebssystem ab Windows 7 und Windows Server 2008 R2 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="47d74-462">This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.</span></span> |
| <span data-ttu-id="47d74-463"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>\_SICHERHEITSFLAG \_ SICHER</span><span class="sxs-lookup"><span data-stu-id="47d74-463"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span> | <span data-ttu-id="47d74-464">Verwendet sichere Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="47d74-464">Uses secure transfers.</span></span> <span data-ttu-id="47d74-465">Dies wird nur in einem Aufruf von [**WinHttpQueryOption zurückgegeben.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="47d74-465">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="47d74-466"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>\_ \_ SICHERHEITSFLAGSTÄRKE \_ MITTEL</span><span class="sxs-lookup"><span data-stu-id="47d74-466"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span> | <span data-ttu-id="47d74-467">Verwendet eine mittlere (56-Bit)-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="47d74-467">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="47d74-468">Dies wird nur in einem Aufruf von [**WinHttpQueryOption zurückgegeben.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="47d74-468">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="47d74-469"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>\_ \_ SICHERHEITSFLAGSTÄRKE \_ STARK</span><span class="sxs-lookup"><span data-stu-id="47d74-469"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span> | <span data-ttu-id="47d74-470">Verwendet eine starke Verschlüsselung (128 Bit).</span><span class="sxs-lookup"><span data-stu-id="47d74-470">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="47d74-471">Dies wird nur in einem Aufruf von [**WinHttpQueryOption zurückgegeben.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="47d74-471">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="47d74-472"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>\_ \_ SICHERHEITSFLAGSTÄRKE \_ SCHWACH</span><span class="sxs-lookup"><span data-stu-id="47d74-472"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span> | <span data-ttu-id="47d74-473">Verwendet eine schwache (40-Bit)-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="47d74-473">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="47d74-474">Dies wird nur in einem Aufruf von [**WinHttpQueryOption zurückgegeben.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="47d74-474">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="47d74-475"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**SICHERHEITSINFORMATIONEN \_ ZUR WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-475"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP\_OPTION\_SECURITY\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-476">Sucht die SChannel-Verbindung und Verschlüsselungsinformationen für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="47d74-476">Retreives the SChannel connection and cipher information for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-477"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**\_WINHTTP-OPTION \_ \_ \_ SICHERHEITSSCHLÜSSELBITNESS**</span><span class="sxs-lookup"><span data-stu-id="47d74-477"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-478">Ruft einen ganzzahligen Wert ohne Vorzeichen ab, der die Verschlüsselungsstärke des Verschlüsselungsschlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="47d74-478">Retrieves an unsigned long integer value that contains the cipher strength of the encryption key.</span></span> <span data-ttu-id="47d74-479">Eine größere Zahl gibt eine stärkere Verschlüsselung mit Verschlüsselungsstärke an.</span><span class="sxs-lookup"><span data-stu-id="47d74-479">A larger number indicates stronger cipher strength encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-480"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**TIMEOUT \_ BEIM SENDEN DER \_ \_ WINHTTP-OPTION**</span><span class="sxs-lookup"><span data-stu-id="47d74-480"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-481">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, um eine Anforderung zu senden oder Daten zu schreiben, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="47d74-481">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to send a request or write some data.</span></span> <span data-ttu-id="47d74-482">Wenn das Senden der Anforderung länger als das Timeout dauert, wird der Sendevorgang abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="47d74-482">If sending the request takes longer than the timeout, the send operation is canceled.</span></span> <span data-ttu-id="47d74-483">Der Standardzeitraum bis zum Timeout beträgt 30 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="47d74-483">The default timeout is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-484"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP \_ OPTION \_ SERVER \_ CBT**</span><span class="sxs-lookup"><span data-stu-id="47d74-484"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP\_OPTION\_SERVER\_CBT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-485">Ruft einen Zeiger auf die [**SecPkgContext-Bindungsstruktur \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) ab, die ein Kanalbindungstoken (Channel Binding Token, CBT) angibt.</span><span class="sxs-lookup"><span data-stu-id="47d74-485">Gets a pointer to [**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) structure that specifies a Channel Binding Token (CBT).</span></span>

<span data-ttu-id="47d74-486">Ein Kanalbindungstoken ist eine Eigenschaft eines sicheren Transportkanals und wird verwendet, um einen Authentifizierungskanal an den sicheren Transportkanal zu binden.</span><span class="sxs-lookup"><span data-stu-id="47d74-486">A Channel Binding Token is a property of a secure transport channel and is used to bind an authentication channel to the secure transport channel.</span></span> <span data-ttu-id="47d74-487">Dieses Token kann von dieser Option nur nach dem Herstellen einer SSL-Verbindung erhalten werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-487">This token can only be obtained by this option after an SSL connection has been established.</span></span>

> [!Note]
> <span data-ttu-id="47d74-488">Die Übergabe dieser  Option und eines NULL-Werts für *lpBuffer* an [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) gibt ERROR INSUFFICIENT BUFFER und die erforderliche Bytegröße für den Puffer im \_ \_ *lpdwBufferLength-Parameter* zurück.</span><span class="sxs-lookup"><span data-stu-id="47d74-488">Passing this option and a **null** value for *lpBuffer* to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) will return ERROR\_INSUFFICIENT\_BUFFER and the required byte size for the buffer in the *lpdwBufferLength* parameter.</span></span> <span data-ttu-id="47d74-489">Dieser zurückgegebene Puffergrößenwert kann in einem nachfolgenden Aufruf zur Abfrage des Kanalbindungstokens übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-489">This returned buffer size value can be passed in a subsequent call to query for the Channel Binding Token.</span></span> <span data-ttu-id="47d74-490">Diese Schritte sind erforderlich, wenn Sie WINHTTP CALLBACK STATUS REQUEST behandeln, wenn Sie Anforderungsheader basierend auf dem \_ \_ \_ Kanalbindungstoken ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="47d74-490">These steps are necessary when handling WINHTTP\_CALLBACK\_STATUS\_REQUEST if you want to modify request headers based on the Channel Binding Token.</span></span> <span data-ttu-id="47d74-491">Beachten Sie, dass Windows XP und Vista das Ändern von Anforderungsheadern während dieses Rückrufs nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="47d74-491">Note that Windows XP and Vista do not support modifying request headers during this callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-492"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CHAIN \_ CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="47d74-492"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-493">Ruft den Kontext der Serverzertifizierungskette ab.</span><span class="sxs-lookup"><span data-stu-id="47d74-493">Retrieves the server certification chain context.</span></span> <span data-ttu-id="47d74-494">**WINHTTP \_ OPTION \_ SERVER \_ CERT CHAIN \_ \_ CONTEXT** kann übergeben werden, um einen duplizierten Zeiger auf **den CERT CHAIN \_ \_ CONTEXT** für eine Serverzertifikatkette zu erhalten, die während einer ausgehandelten SSL-Verbindung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="47d74-494">**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT** can be passed to obtain a duplicated pointer to the **CERT\_CHAIN\_CONTEXT** for a server certificate chain received during a negotiated SSL connection.</span></span> <span data-ttu-id="47d74-495">Der Client muss [**CertFreeCertificateContext für**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) den zurückgegebenen PCCERT CONTEXT-Zeiger aufrufen, \_ der in den Puffer gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="47d74-495">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-496"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="47d74-496"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-497">Ruft den Serverzertifizierungskontext ab.</span><span class="sxs-lookup"><span data-stu-id="47d74-497">Retrieves the server certification context.</span></span> <span data-ttu-id="47d74-498">**WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CONTEXT** kann übergeben werden, um einen duplizierten Zeiger auf [**den CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) für ein Serverzertifikat zu erhalten, das während einer ausgehandelten SSL-Verbindung empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="47d74-498">**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT** can be passed to obtain a duplicated pointer to the [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) for a server certificate received during a negotiated SSL connection.</span></span> <span data-ttu-id="47d74-499">Der Client muss [**CertFreeCertificateContext für**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) den zurückgegebenen PCCERT CONTEXT-Zeiger aufrufen, \_ der in den Puffer gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="47d74-499">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-500"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**VERWENDETER \_ \_ WINHTTP-OPTIONSSERVER-SPN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-500"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WINHTTP\_OPTION\_SERVER\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-501">Ruft den Serverprinzipalnamen ab, den WinHTTP während der Authentifizierung für SSPI bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="47d74-501">Gets the server Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="47d74-502">Dieser Zeichenfolgenwert kann nach einem Authentifizierungsfehler [**an SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-502">This string value can be passed to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-503"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**\_ \_ WINHTTP-OPTIONS-SPN**</span><span class="sxs-lookup"><span data-stu-id="47d74-503"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP\_OPTION\_SPN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-504">Schließt die Serverportnummer ein oder entfernt sie, wenn der SPN (Dienstprinzipalname) für die Kerberos- oder Negotiate Kerberos-Authentifizierung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="47d74-504">Includes or removes the server port number when the SPN (service principal name) is built for Kerberos or Negotiate Kerberos authentication.</span></span> <span data-ttu-id="47d74-505">Dieses Flag ist einer der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="47d74-505">This flag is one of the following values:</span></span>

| <span data-ttu-id="47d74-506">Begriff</span><span class="sxs-lookup"><span data-stu-id="47d74-506">Term</span></span> | <span data-ttu-id="47d74-507">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47d74-507">Description</span></span> |
|-|-|
| <span data-ttu-id="47d74-508"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>\_WINHTTP: \_ DEAKTIVIEREN DES SPN-SERVERPORTS \_ \_</span><span class="sxs-lookup"><span data-stu-id="47d74-508"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP\_DISABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="47d74-509">Entfernt die Serverportnummer.</span><span class="sxs-lookup"><span data-stu-id="47d74-509">Removes the server port number.</span></span> |
| <span data-ttu-id="47d74-510"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP \_ ENABLE \_ SPN \_ SERVER \_ PORT</span><span class="sxs-lookup"><span data-stu-id="47d74-510"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP\_ENABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="47d74-511">Schließt die Serverportnummer ein.</span><span class="sxs-lookup"><span data-stu-id="47d74-511">Includes the server port number.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="47d74-512"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**\_ \_ WINHTTP-OPTIONSSTREAMFEHLERCODE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-512"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**WINHTTP\_OPTION\_STREAM\_ERROR\_CODE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="47d74-513">Diese Option kann für ein WinHttp-Anforderungshand handle abgefragt werden und gibt den Fehlercode zurück, der durch einen RST_STREAM für einen HTTP-Stream empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="47d74-513">This option can be queried on a WinHttp request handle, and will return the error code indicated by a RST_STREAM frame received on an HTTP stream.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-514"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP-OPTION \_ \_ TCP FAST \_ \_ OPEN**</span><span class="sxs-lookup"><span data-stu-id="47d74-514"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP\_OPTION\_TCP\_FAST\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-515">Aktiviert TCP Fast Open für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="47d74-515">Enables TCP Fast Open for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-516"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**\_WINHTTP-OPTION \_ TCP \_ KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="47d74-516"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**WINHTTP\_OPTION\_TCP\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-517">Diese Option kann für ein WinHttp-Sitzungshand handle festgelegt werden, um das TCP-Keep-Alive-Verhalten für den zugrunde liegenden Socket zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="47d74-517">This option can be set on a WinHttp session handle to enable TCP keep-alive behavior on the underlying socket.</span></span> <span data-ttu-id="47d74-518">Übernimmt eine [**\_ tcp-Keepalive-Struktur.**](/windows/win32/winsock/sio-keepalive-vals)</span><span class="sxs-lookup"><span data-stu-id="47d74-518">Takes a [**tcp\_keepalive**](/windows/win32/winsock/sio-keepalive-vals) struct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-519"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP-OPTION \_ \_ TLS FALSE \_ \_ START**</span><span class="sxs-lookup"><span data-stu-id="47d74-519"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP\_OPTION\_TLS\_FALSE\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-520">Aktiviert TLS False Start für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="47d74-520">Enables TLS False Start for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-521"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**UNSICHERER \_ \_ \_ FALLBACK DES TLS-PROTOKOLLS DER \_ WINHTTP-OPTION \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-521"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-522">Diese Option kann für ein WinHttp-Sitzungshand handle festgelegt werden, um zu steuern, ob ein Fallback auf TLS 1.0 zulässig ist, wenn ein TLS-Handshakefehler mit einer neueren Protokollversion vorgibt.</span><span class="sxs-lookup"><span data-stu-id="47d74-522">This option can be set on a WinHttp session handle to control whether fallback to TLS 1.0 is allowed if there is a TLS handshake failure with a newer protocol version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-523"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP-OPTION \_ \_ \_ ENTLADEBENACHRICHTIGUNGSEREIGNIS \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-523"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-524">Nimmt ein Ereignis an, das festgelegt wird, wenn der letzte Rückruf für eine bestimmte Sitzung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="47d74-524">Takes an event that will be set when the last callback has completed for a particular session.</span></span> <span data-ttu-id="47d74-525">Dieses Flag muss für ein Sitzungshand handle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-525">This flag must be must be used on a session handle.</span></span> <span data-ttu-id="47d74-526">Das Ereignis kann erst geschlossen werden, nachdem es von WinHTTP festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="47d74-526">The event cannot be closed until after it has been set by WinHTTP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-527"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP \_ OPTION \_ UNSAFE \_ HEADER \_ PARSING**</span><span class="sxs-lookup"><span data-stu-id="47d74-527"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-528">Diese Option ist für die interne Verwendung reserviert und sollte nicht aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-528">This option is reserved for internal use and should not be called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-529"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**UPGRADE DER \_ \_ WINHTTP-OPTION \_ AUF \_ \_ WEBSOCKET**</span><span class="sxs-lookup"><span data-stu-id="47d74-529"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-530">Weist den Stapel an, einen WebSocket-Handshakeprozess mit [**WinHttpSendRequest zu starten.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="47d74-530">Instructs the stack to start a WebSocket handshake process with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="47d74-531">Für diese Option werden keine Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="47d74-531">This option takes no parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-532"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**URL DER \_ \_ WINHTTP-OPTION**</span><span class="sxs-lookup"><span data-stu-id="47d74-532"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-533">Ruft einen Zeichenfolgenwert ab, der die vollständige URL einer heruntergeladenen Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="47d74-533">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="47d74-534">Wenn die ursprüngliche URL zusätzliche Daten enthält, z. B. Suchzeichenfolgen oder Anker, oder wenn der Aufruf umgeleitet wurde, unterscheidet sich die zurückgegebene URL von der ursprünglichen URL.</span><span class="sxs-lookup"><span data-stu-id="47d74-534">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="47d74-535">Die Anwendung sollte einen Puffer in Bytegröße übergeben, der groß genug ist, um die zurückgegebene URL in wide char zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="47d74-535">The application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-536"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**\_WINHTTP-OPTION \_ GLOBALE \_ SERVERANMELDEINFORMATIONEN \_ \_ VERWENDEN**</span><span class="sxs-lookup"><span data-stu-id="47d74-536"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-537">Verwendet eine **BOOL** und kann nur für ein Sitzungshandl festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-537">Takes a **BOOL** and can be set only a session handle.</span></span> <span data-ttu-id="47d74-538">Sie wird nur an Handles, die aus dem Sitzungshandles erstellt wurden, nach dem Festlegen der Option weiter.</span><span class="sxs-lookup"><span data-stu-id="47d74-538">It will only propagate down to handles created from the session handle after the option has been set.</span></span> <span data-ttu-id="47d74-539">True **gibt an,** dass diese Option als letztes Mittel die Verwendung globaler Serveranmeldeinformationen verursacht, die von WinInet übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="47d74-539">If **TRUE**, this option causes as a last resort the use of global server credentials that were pushed down from WinInet.</span></span> <span data-ttu-id="47d74-540">Der Standardwert für diese Option ist **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="47d74-540">The default for this option is **FALSE**.</span></span> <span data-ttu-id="47d74-541">Diese Option erfordert den Registrierungsschlüssel **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="47d74-541">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="47d74-542">Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="47d74-542">This registry key is not present by default.</span></span> <span data-ttu-id="47d74-543">Wenn sie festgelegt ist, sendet WinINet Anmeldeinformationen an WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="47d74-543">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="47d74-544">Wenn WinHttp eine Authentifizierungsforderung erhält und keine Anmeldeinformationen für das aktuelle Handle festgelegt sind, werden die von WinINet bereitgestellten Anmeldeinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="47d74-544">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-545"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**\_BENUTZER-AGENT DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-545"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-546">Legt die Benutzer-Agent-Zeichenfolge für handles fest, die von [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) bereitgestellt und in [**nachfolgenden WinHttpSendRequest-Funktionen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) verwendet wird, oder ruft sie ab, solange sie nicht durch einen Header überschrieben wird, der von [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) oder **WinHttpSendRequest hinzugefügt** wurde. [](glossary.md)</span><span class="sxs-lookup"><span data-stu-id="47d74-546">Sets or retrieves the [*user agent*](glossary.md) string on handles supplied by [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) and used in subsequent [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) functions, as long as it is not overridden by a header added by [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) or **WinHttpSendRequest**.</span></span> <span data-ttu-id="47d74-547">Beim Abrufen eines Benutzer-Agents sollte die Anwendung einen Puffer in Bytegröße übergeben, der groß genug ist, um die zurückgegebene URL in wide char zu speichern.</span><span class="sxs-lookup"><span data-stu-id="47d74-547">When retrieving a user agent, the application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span> <span data-ttu-id="47d74-548">Beim Festlegen des Benutzer-Agents ist die Puffergröße die Länge der Zeichenfolge in Zeichen plus **das NULL-Abschlusszeichen.**</span><span class="sxs-lookup"><span data-stu-id="47d74-548">When setting the user agent, the buffer size is the length of the string, in characters, plus the **NULL** terminator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-549"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**\_ \_ WINHTTP-OPTIONSBENUTZERNAME**</span><span class="sxs-lookup"><span data-stu-id="47d74-549"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-550">Legt eine Zeichenfolge fest, die den Benutzernamen enthält, oder ruft sie ab.</span><span class="sxs-lookup"><span data-stu-id="47d74-550">Sets or retrieves a string that contains the user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-551"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**\_WINHTTP-OPTION: \_ \_ TIMEOUT BEIM \_ SCHLIEßEN DES WEBSOCKET \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-551"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-552">Legt die Zeit in Millisekunden fest, die [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) warten soll, bis der schließende Handshake abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="47d74-552">Sets the time, in milliseconds, that [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) should wait to complete the close handshake.</span></span> <span data-ttu-id="47d74-553">Die Standardeinstellung beträgt 10 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="47d74-553">The default is 10 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-554"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP-OPTION \_ \_ WEB SOCKET \_ \_ KEEPALIVE \_ INTERVAL**</span><span class="sxs-lookup"><span data-stu-id="47d74-554"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-555">Legt das Intervall in Millisekunden fest, um ein Keep-Alive-Paket über die Verbindung zu senden.</span><span class="sxs-lookup"><span data-stu-id="47d74-555">Sets the interval, in milliseconds, to send a keep-alive packet over the connection.</span></span> <span data-ttu-id="47d74-556">Das Standardintervall ist 30.000 (30 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="47d74-556">The default interval is 30000 (30 seconds).</span></span> <span data-ttu-id="47d74-557">Das Mindestintervall beträgt 15.000 (15 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="47d74-557">The minimum interval is 15000 (15 seconds).</span></span> <span data-ttu-id="47d74-558">Die [**Verwendung von WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) zum Festlegen eines Werts unter 15000 gibt mit **ERROR INVALID PARAMETER \_ \_ zurück.**</span><span class="sxs-lookup"><span data-stu-id="47d74-558">Using [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to set a value lower than 15000 will return with **ERROR\_INVALID\_PARAMETER**.</span></span>

> [!Note]
> <span data-ttu-id="47d74-559">Der Standardwert für **WINHTTP \_ OPTION WEB SOCKET \_ \_ \_ KEEPALIVE \_ INTERVAL** wird aus **HKLM: \\ SOFTWARE Microsoft \\ \\ WebSocket \\ KeepaliveInterval gelesen.**</span><span class="sxs-lookup"><span data-stu-id="47d74-559">The default value for **WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL** is read from **HKLM:\\SOFTWARE\\Microsoft\\WebSocket\\KeepaliveInterval**.</span></span> <span data-ttu-id="47d74-560">Wenn kein Wert festgelegt ist, wird der Standardwert 30000 verwendet.</span><span class="sxs-lookup"><span data-stu-id="47d74-560">If a value is not set, the default value of 30000 will be used.</span></span> <span data-ttu-id="47d74-561">Es ist nicht möglich, ein niedrigeres Keepalive-Intervall als 15.000 Millisekunden zu haben.</span><span class="sxs-lookup"><span data-stu-id="47d74-561">It is not possible to have a lower keepalive interval than 15000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-562"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP-OPTION \_ \_ \_ WEBSOCKET \_ \_ \_ EMPFANGSPUFFERGRÖßE**</span><span class="sxs-lookup"><span data-stu-id="47d74-562"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-563">Legt ein DWORD fest oder ruft es ab, das die Empfangspuffergröße angibt, die für WebSocket-Verbindungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="47d74-563">Sets or retrieves a DWORD which specifies the receive buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-564"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP-OPTION \_ \_ \_ WEBSOCKET- \_ \_ \_ SENDEPUFFERGRÖßE**</span><span class="sxs-lookup"><span data-stu-id="47d74-564"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-565">Legt ein DWORD fest oder ruft es ab, das die Sendepuffergröße angibt, die für WebSocket-Verbindungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="47d74-565">Sets or retrieves a DWORD which specifies the send buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-566"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**ANZAHL DER \_ \_ ARBEITSTHREADS \_ DER WINHTTP-OPTION \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-566"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-567">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Anzahl der Arbeitsthreads angibt, die der Threadpool für asynchrone Vervollständigungen verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="47d74-567">Sets an unsigned long integer value that specifies the number of worker threads the thread pool should use for asynchronous completions.</span></span> <span data-ttu-id="47d74-568">Der Standardwert dieser Option ist 0 (null), was angibt, dass die Anzahl der Arbeitsthreads der Anzahl von CPUs im System entspricht.</span><span class="sxs-lookup"><span data-stu-id="47d74-568">The default value of this option is zero, which specifies that the number of worker threads is equal to the number of CPUs on the system.</span></span> <span data-ttu-id="47d74-569">Diese Option kann nur für ein **NULL**  [HINTERNET-Handle festgelegt](hinternet-handles-in-winhttp.md) werden, bevor ein asynchroner Vorgang ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="47d74-569">This option can only be set on a **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) handle before an asynchronous operation has occurred.</span></span> <span data-ttu-id="47d74-570">Diese Option kann nur einmal festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="47d74-570">This option can only be set once.</span></span>

<span data-ttu-id="47d74-571">**Windows Server 2008 R2 und Windows 7:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="47d74-571">**Windows Server 2008 R2 and Windows 7:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="47d74-572"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**\_WINHTTP-OPTION: \_ \_ \_ SCHREIBPUFFERGRÖßE**</span><span class="sxs-lookup"><span data-stu-id="47d74-572"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="47d74-573">Diese Option ist veraltet. es hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="47d74-573">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47d74-574">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47d74-574">Remarks</span></span>

<span data-ttu-id="47d74-575">In der folgenden Tabelle werden die Optionsflags aufgeführt, indem angegeben wird, auf welche Handles sie angewendet werden können, ob sie abgefragt und festgelegt werden können und welcher Datentyp verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="47d74-575">The following table lists the option flags by specifying which handles they can act upon, whether they can be queried and set, and the data type used.</span></span> <span data-ttu-id="47d74-576">Ein "X" gibt an, dass das Optionsflag für die Verwendung mit der Funktion oder dem Handle gültig ist, während ein "-" angibt, dass das Optionsflag ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="47d74-576">An "X" indicates that the option flag is valid for use with the function or handle, while a "-" specifies that the option flag is invalid.</span></span>

<span data-ttu-id="47d74-577">Der Versuch, ein Optionsflag für eine Windows-Version, in der es nicht unterstützt wird, zu festlegen oder abfragt, führt zu **ERROR \_ WINHTTP \_ INVALID \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="47d74-577">Attempting to set or query an option flag on a Windows version where it is not supported will result in **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span>

| <span data-ttu-id="47d74-578">Optionsflag und Datentyp</span><span class="sxs-lookup"><span data-stu-id="47d74-578">Option flag, and data type</span></span> | <span data-ttu-id="47d74-579">Sitzungshand handle</span><span class="sxs-lookup"><span data-stu-id="47d74-579">Session handle</span></span> | <span data-ttu-id="47d74-580">Anforderungshand handle</span><span class="sxs-lookup"><span data-stu-id="47d74-580">Request handle</span></span> | <span data-ttu-id="47d74-581">Abfrageoption</span><span class="sxs-lookup"><span data-stu-id="47d74-581">Query option</span></span> | <span data-ttu-id="47d74-582">SET-Option</span><span class="sxs-lookup"><span data-stu-id="47d74-582">Set option</span></span> | <span data-ttu-id="47d74-583">Mindestversion von Windows</span><span class="sxs-lookup"><span data-stu-id="47d74-583">Minimum Windows Version</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="47d74-584">\_WINHTTP-OPTION \_ \_ GARANTIERTE NICHT \_ \_ BLOCKIERENDE RÜCKRUFE</span><span class="sxs-lookup"><span data-stu-id="47d74-584">WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS</span></span><br/><span data-ttu-id="47d74-585">**Bool**</span><span class="sxs-lookup"><span data-stu-id="47d74-585">**BOOL**</span></span> | <span data-ttu-id="47d74-586">X</span><span class="sxs-lookup"><span data-stu-id="47d74-586">X</span></span> | \- | \- | <span data-ttu-id="47d74-587">X</span><span class="sxs-lookup"><span data-stu-id="47d74-587">X</span></span> | \- |
| <span data-ttu-id="47d74-588">RICHTLINIE FÜR \_ DIE AUTOMATISCHE ANMELDUNG DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="47d74-588">WINHTTP\_OPTION\_AUTOLOGON\_POLICY</span></span><br/><span data-ttu-id="47d74-589">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-589">**DWORD**</span></span> | \- | <span data-ttu-id="47d74-590">X</span><span class="sxs-lookup"><span data-stu-id="47d74-590">X</span></span> | \- | <span data-ttu-id="47d74-591">X</span><span class="sxs-lookup"><span data-stu-id="47d74-591">X</span></span> | \- |
| <span data-ttu-id="47d74-592">\_ \_ WINHTTP-OPTIONSRÜCKRUF</span><span class="sxs-lookup"><span data-stu-id="47d74-592">WINHTTP\_OPTION\_CALLBACK</span></span><br/><span data-ttu-id="47d74-593">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="47d74-593">**LPVOID**</span></span> | <span data-ttu-id="47d74-594">X</span><span class="sxs-lookup"><span data-stu-id="47d74-594">X</span></span> | <span data-ttu-id="47d74-595">X</span><span class="sxs-lookup"><span data-stu-id="47d74-595">X</span></span> | <span data-ttu-id="47d74-596">X</span><span class="sxs-lookup"><span data-stu-id="47d74-596">X</span></span> | <span data-ttu-id="47d74-597">X</span><span class="sxs-lookup"><span data-stu-id="47d74-597">X</span></span> | \- |
| <span data-ttu-id="47d74-598">WINHTTP \_ OPTION \_ CLIENT \_ CERT \_ CONTEXT</span><span class="sxs-lookup"><span data-stu-id="47d74-598">WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="47d74-599">**\_CERT-KONTEXT**</span><span class="sxs-lookup"><span data-stu-id="47d74-599">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="47d74-600">X</span><span class="sxs-lookup"><span data-stu-id="47d74-600">X</span></span> | \- | <span data-ttu-id="47d74-601">X</span><span class="sxs-lookup"><span data-stu-id="47d74-601">X</span></span> | <span data-ttu-id="47d74-602">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47d74-602">Windows Vista</span></span> |
| <span data-ttu-id="47d74-603">WINHTTP \_ OPTION \_ CLIENT \_ CERT \_ ISSUER \_ LIST</span><span class="sxs-lookup"><span data-stu-id="47d74-603">WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST</span></span><br/>[<span data-ttu-id="47d74-604">**SecPkgContext \_ IssuerListInfoEx**</span><span class="sxs-lookup"><span data-stu-id="47d74-604">**SecPkgContext\_IssuerListInfoEx**</span></span>](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | <span data-ttu-id="47d74-605">X</span><span class="sxs-lookup"><span data-stu-id="47d74-605">X</span></span> | <span data-ttu-id="47d74-606">X</span><span class="sxs-lookup"><span data-stu-id="47d74-606">X</span></span> | \- | <span data-ttu-id="47d74-607">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47d74-607">Windows Vista</span></span> |
| <span data-ttu-id="47d74-608">WINHTTP \_ OPTION \_ CODEPAGE</span><span class="sxs-lookup"><span data-stu-id="47d74-608">WINHTTP\_OPTION\_CODEPAGE</span></span><br/><span data-ttu-id="47d74-609">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-609">**DWORD**</span></span> | <span data-ttu-id="47d74-610">X</span><span class="sxs-lookup"><span data-stu-id="47d74-610">X</span></span> | \- | \- | <span data-ttu-id="47d74-611">X</span><span class="sxs-lookup"><span data-stu-id="47d74-611">X</span></span> | \- |
| <span data-ttu-id="47d74-612">\_WINHTTP-OPTION \_ : KONFIGURIEREN DER \_ \_ PASSPORT-AUTHENTIFIZIERUNG</span><span class="sxs-lookup"><span data-stu-id="47d74-612">WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH</span></span><br/><span data-ttu-id="47d74-613">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-613">**DWORD**</span></span> | <span data-ttu-id="47d74-614">X</span><span class="sxs-lookup"><span data-stu-id="47d74-614">X</span></span> | \- | \- | <span data-ttu-id="47d74-615">X</span><span class="sxs-lookup"><span data-stu-id="47d74-615">X</span></span> | \- |
| <span data-ttu-id="47d74-616">WINHTTP \_ OPTION \_ \_ CONNECT-WIEDERHOLUNGEN</span><span class="sxs-lookup"><span data-stu-id="47d74-616">WINHTTP\_OPTION\_CONNECT\_RETRIES</span></span><br/><span data-ttu-id="47d74-617">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-617">**DWORD**</span></span> | <span data-ttu-id="47d74-618">X</span><span class="sxs-lookup"><span data-stu-id="47d74-618">X</span></span> | <span data-ttu-id="47d74-619">X</span><span class="sxs-lookup"><span data-stu-id="47d74-619">X</span></span> | <span data-ttu-id="47d74-620">X</span><span class="sxs-lookup"><span data-stu-id="47d74-620">X</span></span> | <span data-ttu-id="47d74-621">X</span><span class="sxs-lookup"><span data-stu-id="47d74-621">X</span></span> | \- |
| <span data-ttu-id="47d74-622">WINHTTP \_ OPTION \_ CONNECT \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="47d74-622">WINHTTP\_OPTION\_CONNECT\_TIMEOUT</span></span><br/><span data-ttu-id="47d74-623">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-623">**DWORD**</span></span> | <span data-ttu-id="47d74-624">X</span><span class="sxs-lookup"><span data-stu-id="47d74-624">X</span></span> | <span data-ttu-id="47d74-625">X</span><span class="sxs-lookup"><span data-stu-id="47d74-625">X</span></span> | <span data-ttu-id="47d74-626">X</span><span class="sxs-lookup"><span data-stu-id="47d74-626">X</span></span> | <span data-ttu-id="47d74-627">X</span><span class="sxs-lookup"><span data-stu-id="47d74-627">X</span></span> | \- |
| <span data-ttu-id="47d74-628">VERBINDUNGSINFORMATIONEN ZUR \_ WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="47d74-628">WINHTTP\_OPTION\_CONNECTION\_INFO</span></span><br/>[<span data-ttu-id="47d74-629">**\_WINHTTP-VERBINDUNGSINFORMATIONEN \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-629">**WINHTTP\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | <span data-ttu-id="47d74-630">X</span><span class="sxs-lookup"><span data-stu-id="47d74-630">X</span></span> | <span data-ttu-id="47d74-631">X</span><span class="sxs-lookup"><span data-stu-id="47d74-631">X</span></span> | \- | \- |
| <span data-ttu-id="47d74-632">WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V0</span><span class="sxs-lookup"><span data-stu-id="47d74-632">WINHTTP\_OPTION\_CONNECTION\_STATS\_V0</span></span><br/>[<span data-ttu-id="47d74-633">**TCP \_ INFO \_ v0**</span><span class="sxs-lookup"><span data-stu-id="47d74-633">**TCP\_INFO\_v0**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | <span data-ttu-id="47d74-634">X</span><span class="sxs-lookup"><span data-stu-id="47d74-634">X</span></span> | <span data-ttu-id="47d74-635">X</span><span class="sxs-lookup"><span data-stu-id="47d74-635">X</span></span> | \- | <span data-ttu-id="47d74-636">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="47d74-636">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="47d74-637">WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1</span><span class="sxs-lookup"><span data-stu-id="47d74-637">WINHTTP\_OPTION\_CONNECTION\_STATS\_V1</span></span><br/>[<span data-ttu-id="47d74-638">**TCP \_ INFO \_ v1**</span><span class="sxs-lookup"><span data-stu-id="47d74-638">**TCP\_INFO\_v1**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | <span data-ttu-id="47d74-639">X</span><span class="sxs-lookup"><span data-stu-id="47d74-639">X</span></span> | <span data-ttu-id="47d74-640">X</span><span class="sxs-lookup"><span data-stu-id="47d74-640">X</span></span> | \- | <span data-ttu-id="47d74-641">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="47d74-641">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="47d74-642">\_ \_ WINHTTP-OPTIONSKONTEXTWERT \_</span><span class="sxs-lookup"><span data-stu-id="47d74-642">WINHTTP\_OPTION\_CONTEXT\_VALUE</span></span><br/><span data-ttu-id="47d74-643">**DWORD \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="47d74-643">**DWORD\_PTR**</span></span> | <span data-ttu-id="47d74-644">X</span><span class="sxs-lookup"><span data-stu-id="47d74-644">X</span></span> | <span data-ttu-id="47d74-645">X</span><span class="sxs-lookup"><span data-stu-id="47d74-645">X</span></span> | <span data-ttu-id="47d74-646">X</span><span class="sxs-lookup"><span data-stu-id="47d74-646">X</span></span> | <span data-ttu-id="47d74-647">X</span><span class="sxs-lookup"><span data-stu-id="47d74-647">X</span></span> | \- |
| <span data-ttu-id="47d74-648">WINHTTP \_ OPTION \_ DEKOMPRIMIERUNG</span><span class="sxs-lookup"><span data-stu-id="47d74-648">WINHTTP\_OPTION\_DECOMPRESSION</span></span><br/><span data-ttu-id="47d74-649">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-649">**DWORD**</span></span> | <span data-ttu-id="47d74-650">X</span><span class="sxs-lookup"><span data-stu-id="47d74-650">X</span></span> | <span data-ttu-id="47d74-651">X</span><span class="sxs-lookup"><span data-stu-id="47d74-651">X</span></span> | \- | <span data-ttu-id="47d74-652">X</span><span class="sxs-lookup"><span data-stu-id="47d74-652">X</span></span> | <span data-ttu-id="47d74-653">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="47d74-653">Windows 8.1</span></span> |
| <span data-ttu-id="47d74-654">WINHTTP \_ OPTION \_ DISABLE \_ FEATURE</span><span class="sxs-lookup"><span data-stu-id="47d74-654">WINHTTP\_OPTION\_DISABLE\_FEATURE</span></span><br/><span data-ttu-id="47d74-655">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-655">**DWORD**</span></span> | \- | <span data-ttu-id="47d74-656">X</span><span class="sxs-lookup"><span data-stu-id="47d74-656">X</span></span> | \- | <span data-ttu-id="47d74-657">X</span><span class="sxs-lookup"><span data-stu-id="47d74-657">X</span></span> | \- |
| <span data-ttu-id="47d74-658">WINHTTP \_ OPTION \_ DISABLE \_ SECURE \_ PROTOCOL \_ FALLBACK</span><span class="sxs-lookup"><span data-stu-id="47d74-658">WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK</span></span><br/><span data-ttu-id="47d74-659">**Bool**</span><span class="sxs-lookup"><span data-stu-id="47d74-659">**BOOL**</span></span> | <span data-ttu-id="47d74-660">X</span><span class="sxs-lookup"><span data-stu-id="47d74-660">X</span></span> | \- | \- | <span data-ttu-id="47d74-661">X</span><span class="sxs-lookup"><span data-stu-id="47d74-661">X</span></span> | <span data-ttu-id="47d74-662">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="47d74-662">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="47d74-663">\_WINHTTP-OPTION \_ : DEAKTIVIEREN DER \_ \_ STREAMWARTESCHLANGE</span><span class="sxs-lookup"><span data-stu-id="47d74-663">WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE</span></span><br/><span data-ttu-id="47d74-664">**Bool**</span><span class="sxs-lookup"><span data-stu-id="47d74-664">**BOOL**</span></span> | <span data-ttu-id="47d74-665">X</span><span class="sxs-lookup"><span data-stu-id="47d74-665">X</span></span> | <span data-ttu-id="47d74-666">X</span><span class="sxs-lookup"><span data-stu-id="47d74-666">X</span></span> | \- | <span data-ttu-id="47d74-667">X</span><span class="sxs-lookup"><span data-stu-id="47d74-667">X</span></span> | <span data-ttu-id="47d74-668">Windows 10 Version 1809</span><span class="sxs-lookup"><span data-stu-id="47d74-668">Windows 10 Version 1809</span></span> |
| <span data-ttu-id="47d74-669">FEATURE \_ "WINHTTP-OPTION \_ \_ AKTIVIEREN"</span><span class="sxs-lookup"><span data-stu-id="47d74-669">WINHTTP\_OPTION\_ENABLE\_FEATURE</span></span><br/><span data-ttu-id="47d74-670">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-670">**DWORD**</span></span> | \* | \* | \- | <span data-ttu-id="47d74-671">X</span><span class="sxs-lookup"><span data-stu-id="47d74-671">X</span></span> | \- |
| <span data-ttu-id="47d74-672">WINHTTP \_ OPTION \_ ENABLE \_ HTTP \_ PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="47d74-672">WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL</span></span><br/><span data-ttu-id="47d74-673">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-673">**DWORD**</span></span> | <span data-ttu-id="47d74-674">X</span><span class="sxs-lookup"><span data-stu-id="47d74-674">X</span></span> | <span data-ttu-id="47d74-675">X</span><span class="sxs-lookup"><span data-stu-id="47d74-675">X</span></span> | \- | <span data-ttu-id="47d74-676">X</span><span class="sxs-lookup"><span data-stu-id="47d74-676">X</span></span> | <span data-ttu-id="47d74-677">Windows 10, Version 1607</span><span class="sxs-lookup"><span data-stu-id="47d74-677">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="47d74-678">\_WINHTTP-OPTION \_ AKTIVIEREN DES \_ HTTP2 \_ \_ PLUS-CLIENTZERTIFIKATKONTEXTS \_ \_</span><span class="sxs-lookup"><span data-stu-id="47d74-678">WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT\_CONTEXT</span></span><br/><span data-ttu-id="47d74-679">**Bool**</span><span class="sxs-lookup"><span data-stu-id="47d74-679">**BOOL**</span></span> | <span data-ttu-id="47d74-680">X</span><span class="sxs-lookup"><span data-stu-id="47d74-680">X</span></span> | \- | \- | <span data-ttu-id="47d74-681">X</span><span class="sxs-lookup"><span data-stu-id="47d74-681">X</span></span> | <span data-ttu-id="47d74-682">Windows 10 Version 21H1</span><span class="sxs-lookup"><span data-stu-id="47d74-682">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="47d74-683">\_WINHTTP-OPTION \_ ENABLETRACING</span><span class="sxs-lookup"><span data-stu-id="47d74-683">WINHTTP\_OPTION\_ENABLETRACING</span></span><br/><span data-ttu-id="47d74-684">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-684">**DWORD**</span></span> | \- | \- | <span data-ttu-id="47d74-685">X</span><span class="sxs-lookup"><span data-stu-id="47d74-685">X</span></span> | <span data-ttu-id="47d74-686">X</span><span class="sxs-lookup"><span data-stu-id="47d74-686">X</span></span> | \- |
| <span data-ttu-id="47d74-687">WINHTTP \_ OPTION \_ ENCODE \_ EXTRA</span><span class="sxs-lookup"><span data-stu-id="47d74-687">WINHTTP\_OPTION\_ENCODE\_EXTRA</span></span><br/><span data-ttu-id="47d74-688">**Bool**</span><span class="sxs-lookup"><span data-stu-id="47d74-688">**BOOL**</span></span> | <span data-ttu-id="47d74-689">X</span><span class="sxs-lookup"><span data-stu-id="47d74-689">X</span></span> | <span data-ttu-id="47d74-690">X</span><span class="sxs-lookup"><span data-stu-id="47d74-690">X</span></span> | \- | <span data-ttu-id="47d74-691">X</span><span class="sxs-lookup"><span data-stu-id="47d74-691">X</span></span> | <span data-ttu-id="47d74-692">Windows 10 Version 1803</span><span class="sxs-lookup"><span data-stu-id="47d74-692">Windows 10 Version 1803</span></span> |
| <span data-ttu-id="47d74-693">\_WINHTTP-OPTION \_ LÄUFT VERBINDUNG AB \_</span><span class="sxs-lookup"><span data-stu-id="47d74-693">WINHTTP\_OPTION\_EXPIRE\_CONNECTION</span></span><br/><span data-ttu-id="47d74-694">–</span><span class="sxs-lookup"><span data-stu-id="47d74-694">N/A</span></span> | \- | <span data-ttu-id="47d74-695">X</span><span class="sxs-lookup"><span data-stu-id="47d74-695">X</span></span> | \- | <span data-ttu-id="47d74-696">X</span><span class="sxs-lookup"><span data-stu-id="47d74-696">X</span></span> | <span data-ttu-id="47d74-697">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="47d74-697">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="47d74-698">\_ \_ ERWEITERTER \_ WINHTTP-OPTION-FEHLER</span><span class="sxs-lookup"><span data-stu-id="47d74-698">WINHTTP\_OPTION\_EXTENDED\_ERROR</span></span><br/><span data-ttu-id="47d74-699">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-699">**DWORD**</span></span> | <span data-ttu-id="47d74-700">X</span><span class="sxs-lookup"><span data-stu-id="47d74-700">X</span></span> | <span data-ttu-id="47d74-701">X</span><span class="sxs-lookup"><span data-stu-id="47d74-701">X</span></span> | <span data-ttu-id="47d74-702">X</span><span class="sxs-lookup"><span data-stu-id="47d74-702">X</span></span> | \- | \- |
| <span data-ttu-id="47d74-703">WINHTTP \_ OPTION \_ GLOBAL \_ PROXY \_ CREDS</span><span class="sxs-lookup"><span data-stu-id="47d74-703">WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS</span></span><br/>[<span data-ttu-id="47d74-704">**WINHTTP \_ CREDS**</span><span class="sxs-lookup"><span data-stu-id="47d74-704">**WINHTTP\_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | <span data-ttu-id="47d74-705">X</span><span class="sxs-lookup"><span data-stu-id="47d74-705">X</span></span> | <span data-ttu-id="47d74-706">X</span><span class="sxs-lookup"><span data-stu-id="47d74-706">X</span></span> | \- | <span data-ttu-id="47d74-707">X</span><span class="sxs-lookup"><span data-stu-id="47d74-707">X</span></span> | \- |
| <span data-ttu-id="47d74-708">WINHTTP \_ OPTION \_ GLOBAL \_ SERVER \_ CREDS</span><span class="sxs-lookup"><span data-stu-id="47d74-708">WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS</span></span><br/>[<span data-ttu-id="47d74-709">**WINHTTP \_ CREDS \_ EX**</span><span class="sxs-lookup"><span data-stu-id="47d74-709">**WINHTTP\_CREDS\_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | <span data-ttu-id="47d74-710">X</span><span class="sxs-lookup"><span data-stu-id="47d74-710">X</span></span> | <span data-ttu-id="47d74-711">X</span><span class="sxs-lookup"><span data-stu-id="47d74-711">X</span></span> | \- | <span data-ttu-id="47d74-712">X</span><span class="sxs-lookup"><span data-stu-id="47d74-712">X</span></span> | \- |
| <span data-ttu-id="47d74-713">TYP DES \_ WINHTTP-OPTIONSHANDLE \_ \_</span><span class="sxs-lookup"><span data-stu-id="47d74-713">WINHTTP\_OPTION\_HANDLE\_TYPE</span></span><br/><span data-ttu-id="47d74-714">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-714">**DWORD**</span></span> | <span data-ttu-id="47d74-715">X</span><span class="sxs-lookup"><span data-stu-id="47d74-715">X</span></span> | <span data-ttu-id="47d74-716">X</span><span class="sxs-lookup"><span data-stu-id="47d74-716">X</span></span> | <span data-ttu-id="47d74-717">X</span><span class="sxs-lookup"><span data-stu-id="47d74-717">X</span></span> | \- | \- |
| <span data-ttu-id="47d74-718">WINHTTP \_ OPTION HTTP PROTOCOL \_ \_ \_ ERFORDERLICH</span><span class="sxs-lookup"><span data-stu-id="47d74-718">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED</span></span><br/><span data-ttu-id="47d74-719">**Bool**</span><span class="sxs-lookup"><span data-stu-id="47d74-719">**BOOL**</span></span> | <span data-ttu-id="47d74-720">X</span><span class="sxs-lookup"><span data-stu-id="47d74-720">X</span></span> | <span data-ttu-id="47d74-721">X</span><span class="sxs-lookup"><span data-stu-id="47d74-721">X</span></span> | \- | <span data-ttu-id="47d74-722">X</span><span class="sxs-lookup"><span data-stu-id="47d74-722">X</span></span> | <span data-ttu-id="47d74-723">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="47d74-723">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="47d74-724">VERWENDETES \_ \_ \_ HTTP-PROTOKOLL DER WINHTTP-OPTION \_</span><span class="sxs-lookup"><span data-stu-id="47d74-724">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED</span></span><br/><span data-ttu-id="47d74-725">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-725">**DWORD**</span></span> | \- | <span data-ttu-id="47d74-726">X</span><span class="sxs-lookup"><span data-stu-id="47d74-726">X</span></span> | <span data-ttu-id="47d74-727">X</span><span class="sxs-lookup"><span data-stu-id="47d74-727">X</span></span> | \- | <span data-ttu-id="47d74-728">Windows 10, Version 1607</span><span class="sxs-lookup"><span data-stu-id="47d74-728">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="47d74-729">WINHTTP \_ OPTION \_ \_ HTTP-VERSION</span><span class="sxs-lookup"><span data-stu-id="47d74-729">WINHTTP\_OPTION\_HTTP\_VERSION</span></span><br/>[<span data-ttu-id="47d74-730">**\_ \_ HTTP-VERSIONSINFORMATIONEN**</span><span class="sxs-lookup"><span data-stu-id="47d74-730">**HTTP\_VERSION\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | <span data-ttu-id="47d74-731">X</span><span class="sxs-lookup"><span data-stu-id="47d74-731">X</span></span> | <span data-ttu-id="47d74-732">X</span><span class="sxs-lookup"><span data-stu-id="47d74-732">X</span></span> | <span data-ttu-id="47d74-733">X</span><span class="sxs-lookup"><span data-stu-id="47d74-733">X</span></span> | <span data-ttu-id="47d74-734">X</span><span class="sxs-lookup"><span data-stu-id="47d74-734">X</span></span> | \- |
| <span data-ttu-id="47d74-735">\_WINHTTP-OPTION \_ HTTP2 \_ KEEPALIVE</span><span class="sxs-lookup"><span data-stu-id="47d74-735">WINHTTP\_OPTION\_HTTP2\_KEEPALIVE</span></span><br/><span data-ttu-id="47d74-736">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-736">**DWORD**</span></span> | <span data-ttu-id="47d74-737">X</span><span class="sxs-lookup"><span data-stu-id="47d74-737">X</span></span> | \- | \- | <span data-ttu-id="47d74-738">X</span><span class="sxs-lookup"><span data-stu-id="47d74-738">X</span></span> | <span data-ttu-id="47d74-739">Windows 10 Version 21H1</span><span class="sxs-lookup"><span data-stu-id="47d74-739">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="47d74-740">\_WINHTTP-OPTION \_ HTTP2 \_ PLUS \_ \_ ÜBERTRAGUNGSCODIERUNG</span><span class="sxs-lookup"><span data-stu-id="47d74-740">WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING</span></span><br/><span data-ttu-id="47d74-741">**Bool**</span><span class="sxs-lookup"><span data-stu-id="47d74-741">**BOOL**</span></span> | <span data-ttu-id="47d74-742">X</span><span class="sxs-lookup"><span data-stu-id="47d74-742">X</span></span> | <span data-ttu-id="47d74-743">X</span><span class="sxs-lookup"><span data-stu-id="47d74-743">X</span></span> | \- | <span data-ttu-id="47d74-744">X</span><span class="sxs-lookup"><span data-stu-id="47d74-744">X</span></span> | <span data-ttu-id="47d74-745">Windows 10 Version 21H1</span><span class="sxs-lookup"><span data-stu-id="47d74-745">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="47d74-746">WINHTTP \_ OPTION \_ IGNORE \_ CERT \_ REVOCATION \_ OFFLINE</span><span class="sxs-lookup"><span data-stu-id="47d74-746">WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE</span></span><br/><span data-ttu-id="47d74-747">**Bool**</span><span class="sxs-lookup"><span data-stu-id="47d74-747">**BOOL**</span></span> | \- | <span data-ttu-id="47d74-748">X</span><span class="sxs-lookup"><span data-stu-id="47d74-748">X</span></span> | \- | <span data-ttu-id="47d74-749">X</span><span class="sxs-lookup"><span data-stu-id="47d74-749">X</span></span> | <span data-ttu-id="47d74-750">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="47d74-750">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="47d74-751">WINHTTP \_ OPTION \_ IPV6 \_ FAST \_ FALLBACK</span><span class="sxs-lookup"><span data-stu-id="47d74-751">WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK</span></span><br/><span data-ttu-id="47d74-752">**Bool**</span><span class="sxs-lookup"><span data-stu-id="47d74-752">**BOOL**</span></span> | <span data-ttu-id="47d74-753">X</span><span class="sxs-lookup"><span data-stu-id="47d74-753">X</span></span> | \- | \- | <span data-ttu-id="47d74-754">X</span><span class="sxs-lookup"><span data-stu-id="47d74-754">X</span></span> | <span data-ttu-id="47d74-755">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="47d74-755">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="47d74-756">\_WINHTTP-OPTION: \_ \_ PROXY \_ \_ CONNECT-ANTWORT</span><span class="sxs-lookup"><span data-stu-id="47d74-756">WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="47d74-757">**Bool**</span><span class="sxs-lookup"><span data-stu-id="47d74-757">**BOOL**</span></span> | <span data-ttu-id="47d74-758">X</span><span class="sxs-lookup"><span data-stu-id="47d74-758">X</span></span> | <span data-ttu-id="47d74-759">X</span><span class="sxs-lookup"><span data-stu-id="47d74-759">X</span></span> | <span data-ttu-id="47d74-760">X</span><span class="sxs-lookup"><span data-stu-id="47d74-760">X</span></span> | \- | \- |
| <span data-ttu-id="47d74-761">WINHTTP \_ OPTION \_ \_ MAX. CONNS \_ PRO \_ 1 \_ 0 \_ SERVER</span><span class="sxs-lookup"><span data-stu-id="47d74-761">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER</span></span><br/><span data-ttu-id="47d74-762">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-762">**DWORD**</span></span> | <span data-ttu-id="47d74-763">X</span><span class="sxs-lookup"><span data-stu-id="47d74-763">X</span></span> | \- | <span data-ttu-id="47d74-764">X</span><span class="sxs-lookup"><span data-stu-id="47d74-764">X</span></span> | <span data-ttu-id="47d74-765">X</span><span class="sxs-lookup"><span data-stu-id="47d74-765">X</span></span> | \- |
| <span data-ttu-id="47d74-766">WINHTTP \_ OPTION \_ \_ MAX. ANZAHL VON CONNS \_ PRO \_ SERVER</span><span class="sxs-lookup"><span data-stu-id="47d74-766">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER</span></span><br/><span data-ttu-id="47d74-767">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-767">**DWORD**</span></span> | <span data-ttu-id="47d74-768">X</span><span class="sxs-lookup"><span data-stu-id="47d74-768">X</span></span> | \- | <span data-ttu-id="47d74-769">X</span><span class="sxs-lookup"><span data-stu-id="47d74-769">X</span></span> | <span data-ttu-id="47d74-770">X</span><span class="sxs-lookup"><span data-stu-id="47d74-770">X</span></span> | \- |
| <span data-ttu-id="47d74-771">WINHTTP \_ OPTION \_ \_ MAX. AUTOMATISCHE \_ \_ HTTP-UMLEITUNGEN</span><span class="sxs-lookup"><span data-stu-id="47d74-771">WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS</span></span><br/><span data-ttu-id="47d74-772">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-772">**DWORD**</span></span> | <span data-ttu-id="47d74-773">X</span><span class="sxs-lookup"><span data-stu-id="47d74-773">X</span></span> | <span data-ttu-id="47d74-774">X</span><span class="sxs-lookup"><span data-stu-id="47d74-774">X</span></span> | <span data-ttu-id="47d74-775">X</span><span class="sxs-lookup"><span data-stu-id="47d74-775">X</span></span> | <span data-ttu-id="47d74-776">X</span><span class="sxs-lookup"><span data-stu-id="47d74-776">X</span></span> | \- |
| <span data-ttu-id="47d74-777">WINHTTP \_ OPTION \_ MAX \_ HTTP \_ STATUS \_ CONTINUE</span><span class="sxs-lookup"><span data-stu-id="47d74-777">WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE</span></span><br/><span data-ttu-id="47d74-778">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-778">**DWORD**</span></span> | <span data-ttu-id="47d74-779">X</span><span class="sxs-lookup"><span data-stu-id="47d74-779">X</span></span> | <span data-ttu-id="47d74-780">X</span><span class="sxs-lookup"><span data-stu-id="47d74-780">X</span></span> | <span data-ttu-id="47d74-781">X</span><span class="sxs-lookup"><span data-stu-id="47d74-781">X</span></span> | <span data-ttu-id="47d74-782">X</span><span class="sxs-lookup"><span data-stu-id="47d74-782">X</span></span> | \- |
| <span data-ttu-id="47d74-783">WINHTTP \_ OPTION \_ MAX \_ RESPONSE \_ DRAIN \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="47d74-783">WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE</span></span><br/><span data-ttu-id="47d74-784">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-784">**DWORD**</span></span> | <span data-ttu-id="47d74-785">X</span><span class="sxs-lookup"><span data-stu-id="47d74-785">X</span></span> | <span data-ttu-id="47d74-786">X</span><span class="sxs-lookup"><span data-stu-id="47d74-786">X</span></span> | <span data-ttu-id="47d74-787">X</span><span class="sxs-lookup"><span data-stu-id="47d74-787">X</span></span> | <span data-ttu-id="47d74-788">X</span><span class="sxs-lookup"><span data-stu-id="47d74-788">X</span></span> | \- |
| <span data-ttu-id="47d74-789">MAXIMALE \_ \_ \_ \_ ANTWORTHEADERGRÖßE \_ DER WINHTTP-OPTION</span><span class="sxs-lookup"><span data-stu-id="47d74-789">WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE</span></span><br/><span data-ttu-id="47d74-790">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-790">**DWORD**</span></span> | <span data-ttu-id="47d74-791">X</span><span class="sxs-lookup"><span data-stu-id="47d74-791">X</span></span> | <span data-ttu-id="47d74-792">X</span><span class="sxs-lookup"><span data-stu-id="47d74-792">X</span></span> | <span data-ttu-id="47d74-793">X</span><span class="sxs-lookup"><span data-stu-id="47d74-793">X</span></span> | <span data-ttu-id="47d74-794">X</span><span class="sxs-lookup"><span data-stu-id="47d74-794">X</span></span> | \- |
| <span data-ttu-id="47d74-795">\_ \_ ÜBERGEORDNETES WINHTTP-OPTIONSHANDLE \_</span><span class="sxs-lookup"><span data-stu-id="47d74-795">WINHTTP\_OPTION\_PARENT\_HANDLE</span></span><br/>[<span data-ttu-id="47d74-796">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="47d74-796">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="47d74-797">X</span><span class="sxs-lookup"><span data-stu-id="47d74-797">X</span></span> | <span data-ttu-id="47d74-798">X</span><span class="sxs-lookup"><span data-stu-id="47d74-798">X</span></span> | <span data-ttu-id="47d74-799">X</span><span class="sxs-lookup"><span data-stu-id="47d74-799">X</span></span> | \- | \- |
| <span data-ttu-id="47d74-800">WINHTTP \_ OPTION \_ PASSPORT \_ COBRANDING \_ TEXT</span><span class="sxs-lookup"><span data-stu-id="47d74-800">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT</span></span><br/><span data-ttu-id="47d74-801">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="47d74-801">**LPWSTR**</span></span> | \- | <span data-ttu-id="47d74-802">X</span><span class="sxs-lookup"><span data-stu-id="47d74-802">X</span></span> | <span data-ttu-id="47d74-803">X</span><span class="sxs-lookup"><span data-stu-id="47d74-803">X</span></span> | \- | \- |
| <span data-ttu-id="47d74-804">WINHTTP \_ OPTION \_ PASSPORT \_ COBRANDING \_ URL</span><span class="sxs-lookup"><span data-stu-id="47d74-804">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL</span></span><br/><span data-ttu-id="47d74-805">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="47d74-805">**LPWSTR**</span></span> | \- | <span data-ttu-id="47d74-806">X</span><span class="sxs-lookup"><span data-stu-id="47d74-806">X</span></span> | <span data-ttu-id="47d74-807">X</span><span class="sxs-lookup"><span data-stu-id="47d74-807">X</span></span> | \- | \- |
| <span data-ttu-id="47d74-808">WINHTTP \_ OPTION \_ PASSPORT \_ RETURN \_ URL</span><span class="sxs-lookup"><span data-stu-id="47d74-808">WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL</span></span><br/><span data-ttu-id="47d74-809">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="47d74-809">**LPVOID**</span></span> | \- | <span data-ttu-id="47d74-810">X</span><span class="sxs-lookup"><span data-stu-id="47d74-810">X</span></span> | <span data-ttu-id="47d74-811">X</span><span class="sxs-lookup"><span data-stu-id="47d74-811">X</span></span> | \- | \- |
| <span data-ttu-id="47d74-812">WINHTTP \_ OPTION \_ PASSPORT \_ SIGN \_ OUT</span><span class="sxs-lookup"><span data-stu-id="47d74-812">WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT</span></span><br/><span data-ttu-id="47d74-813">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="47d74-813">**LPVOID**</span></span> | <span data-ttu-id="47d74-814">X</span><span class="sxs-lookup"><span data-stu-id="47d74-814">X</span></span> | \- | \- | <span data-ttu-id="47d74-815">X</span><span class="sxs-lookup"><span data-stu-id="47d74-815">X</span></span> | \- |
| <span data-ttu-id="47d74-816">\_ \_ WINHTTP-OPTIONSKENNWORT</span><span class="sxs-lookup"><span data-stu-id="47d74-816">WINHTTP\_OPTION\_PASSWORD</span></span><br/><span data-ttu-id="47d74-817">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="47d74-817">**LPWSTR**</span></span> | \- | <span data-ttu-id="47d74-818">X</span><span class="sxs-lookup"><span data-stu-id="47d74-818">X</span></span> | <span data-ttu-id="47d74-819">X</span><span class="sxs-lookup"><span data-stu-id="47d74-819">X</span></span> | <span data-ttu-id="47d74-820">X</span><span class="sxs-lookup"><span data-stu-id="47d74-820">X</span></span> | \- |
| <span data-ttu-id="47d74-821">\_WINHTTP-OPTIONSPROXY \_</span><span class="sxs-lookup"><span data-stu-id="47d74-821">WINHTTP\_OPTION\_PROXY</span></span><br/>[<span data-ttu-id="47d74-822">**\_WINHTTP-PROXYINFORMATIONEN \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-822">**WINHTTP\_PROXY\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | <span data-ttu-id="47d74-823">X</span><span class="sxs-lookup"><span data-stu-id="47d74-823">X</span></span> | <span data-ttu-id="47d74-824">X</span><span class="sxs-lookup"><span data-stu-id="47d74-824">X</span></span> | <span data-ttu-id="47d74-825">X</span><span class="sxs-lookup"><span data-stu-id="47d74-825">X</span></span> | <span data-ttu-id="47d74-826">X</span><span class="sxs-lookup"><span data-stu-id="47d74-826">X</span></span> | \- |
| <span data-ttu-id="47d74-827">WINHTTP \_ OPTION \_ PROXY \_ PASSWORD</span><span class="sxs-lookup"><span data-stu-id="47d74-827">WINHTTP\_OPTION\_PROXY\_PASSWORD</span></span><br/><span data-ttu-id="47d74-828">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="47d74-828">**LPWSTR**</span></span> | \- | <span data-ttu-id="47d74-829">X</span><span class="sxs-lookup"><span data-stu-id="47d74-829">X</span></span> | <span data-ttu-id="47d74-830">X</span><span class="sxs-lookup"><span data-stu-id="47d74-830">X</span></span> | <span data-ttu-id="47d74-831">X</span><span class="sxs-lookup"><span data-stu-id="47d74-831">X</span></span> | \- |
| <span data-ttu-id="47d74-832">VERWENDETER \_ \_ WINHTTP-OPTIONSPROXY-SPN \_ \_</span><span class="sxs-lookup"><span data-stu-id="47d74-832">WINHTTP\_OPTION\_PROXY\_SPN\_USED</span></span><br/><span data-ttu-id="47d74-833">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="47d74-833">**LPWSTR**</span></span> | \- | <span data-ttu-id="47d74-834">X</span><span class="sxs-lookup"><span data-stu-id="47d74-834">X</span></span> | <span data-ttu-id="47d74-835">X</span><span class="sxs-lookup"><span data-stu-id="47d74-835">X</span></span> | \- | \- |
| <span data-ttu-id="47d74-836">\_WINHTTP-OPTION \_ \_ PROXYBENUTZERNAME</span><span class="sxs-lookup"><span data-stu-id="47d74-836">WINHTTP\_OPTION\_PROXY\_USERNAME</span></span><br/><span data-ttu-id="47d74-837">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="47d74-837">**LPWSTR**</span></span> | \- | <span data-ttu-id="47d74-838">X</span><span class="sxs-lookup"><span data-stu-id="47d74-838">X</span></span> | <span data-ttu-id="47d74-839">X</span><span class="sxs-lookup"><span data-stu-id="47d74-839">X</span></span> | <span data-ttu-id="47d74-840">X</span><span class="sxs-lookup"><span data-stu-id="47d74-840">X</span></span> | \- |
| <span data-ttu-id="47d74-841">WINHTTP \_ OPTION \_ READ \_ BUFFER \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="47d74-841">WINHTTP\_OPTION\_READ\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="47d74-842">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-842">**DWORD**</span></span> | \- | <span data-ttu-id="47d74-843">X</span><span class="sxs-lookup"><span data-stu-id="47d74-843">X</span></span> | <span data-ttu-id="47d74-844">X</span><span class="sxs-lookup"><span data-stu-id="47d74-844">X</span></span> | <span data-ttu-id="47d74-845">X</span><span class="sxs-lookup"><span data-stu-id="47d74-845">X</span></span> | \- |
| <span data-ttu-id="47d74-846">\_WINHTTP-OPTION \_ " PROXY \_ \_ \_ CONNECT-ANTWORT EMPFANGEN"</span><span class="sxs-lookup"><span data-stu-id="47d74-846">WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="47d74-847">**Bool**</span><span class="sxs-lookup"><span data-stu-id="47d74-847">**BOOL**</span></span> | <span data-ttu-id="47d74-848">X</span><span class="sxs-lookup"><span data-stu-id="47d74-848">X</span></span> | <span data-ttu-id="47d74-849">X</span><span class="sxs-lookup"><span data-stu-id="47d74-849">X</span></span> | \- | <span data-ttu-id="47d74-850">X</span><span class="sxs-lookup"><span data-stu-id="47d74-850">X</span></span> | \- |
| <span data-ttu-id="47d74-851">WINHTTP \_ OPTION \_ RECEIVE \_ RESPONSE \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="47d74-851">WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT</span></span><br/><span data-ttu-id="47d74-852">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-852">**DWORD**</span></span> | <span data-ttu-id="47d74-853">X</span><span class="sxs-lookup"><span data-stu-id="47d74-853">X</span></span> | <span data-ttu-id="47d74-854">X</span><span class="sxs-lookup"><span data-stu-id="47d74-854">X</span></span> | <span data-ttu-id="47d74-855">X</span><span class="sxs-lookup"><span data-stu-id="47d74-855">X</span></span> | <span data-ttu-id="47d74-856">X</span><span class="sxs-lookup"><span data-stu-id="47d74-856">X</span></span> | \- |
| <span data-ttu-id="47d74-857">WINHTTP \_ OPTION \_ RECEIVE \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="47d74-857">WINHTTP\_OPTION\_RECEIVE\_TIMEOUT</span></span><br/><span data-ttu-id="47d74-858">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-858">**DWORD**</span></span> | <span data-ttu-id="47d74-859">X</span><span class="sxs-lookup"><span data-stu-id="47d74-859">X</span></span> | <span data-ttu-id="47d74-860">X</span><span class="sxs-lookup"><span data-stu-id="47d74-860">X</span></span> | <span data-ttu-id="47d74-861">X</span><span class="sxs-lookup"><span data-stu-id="47d74-861">X</span></span> | <span data-ttu-id="47d74-862">X</span><span class="sxs-lookup"><span data-stu-id="47d74-862">X</span></span> | \- |
| <span data-ttu-id="47d74-863">UMLEITUNGSRICHTLINIE FÜR \_ WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="47d74-863">WINHTTP\_OPTION\_REDIRECT\_POLICY</span></span><br/><span data-ttu-id="47d74-864">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-864">**DWORD**</span></span> | <span data-ttu-id="47d74-865">X</span><span class="sxs-lookup"><span data-stu-id="47d74-865">X</span></span> | <span data-ttu-id="47d74-866">X</span><span class="sxs-lookup"><span data-stu-id="47d74-866">X</span></span> | <span data-ttu-id="47d74-867">X</span><span class="sxs-lookup"><span data-stu-id="47d74-867">X</span></span> | <span data-ttu-id="47d74-868">X</span><span class="sxs-lookup"><span data-stu-id="47d74-868">X</span></span> | \- |
| <span data-ttu-id="47d74-869">\_WINHTTP-OPTION \_ \_ : USERPWD \_ IN \_ URL ABLEHNEN</span><span class="sxs-lookup"><span data-stu-id="47d74-869">WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL</span></span><br/><span data-ttu-id="47d74-870">**Bool**</span><span class="sxs-lookup"><span data-stu-id="47d74-870">**BOOL**</span></span> | \- | <span data-ttu-id="47d74-871">X</span><span class="sxs-lookup"><span data-stu-id="47d74-871">X</span></span> | \- | <span data-ttu-id="47d74-872">X</span><span class="sxs-lookup"><span data-stu-id="47d74-872">X</span></span> | \- |
| <span data-ttu-id="47d74-873">\_ANFORDERUNGSPRIORITÄT DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="47d74-873">WINHTTP\_OPTION\_REQUEST\_PRIORITY</span></span><br/><span data-ttu-id="47d74-874">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-874">**DWORD**</span></span> | \- | <span data-ttu-id="47d74-875">X</span><span class="sxs-lookup"><span data-stu-id="47d74-875">X</span></span> | <span data-ttu-id="47d74-876">X</span><span class="sxs-lookup"><span data-stu-id="47d74-876">X</span></span> | <span data-ttu-id="47d74-877">X</span><span class="sxs-lookup"><span data-stu-id="47d74-877">X</span></span> | \- |
| <span data-ttu-id="47d74-878">WINHTTP \_ OPTION \_ REQUEST \_ STATS</span><span class="sxs-lookup"><span data-stu-id="47d74-878">WINHTTP\_OPTION\_REQUEST\_STATS</span></span><br/>[<span data-ttu-id="47d74-879">**WINHTTP \_ REQUEST \_ STATS**</span><span class="sxs-lookup"><span data-stu-id="47d74-879">**WINHTTP\_REQUEST\_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | <span data-ttu-id="47d74-880">X</span><span class="sxs-lookup"><span data-stu-id="47d74-880">X</span></span> | <span data-ttu-id="47d74-881">X</span><span class="sxs-lookup"><span data-stu-id="47d74-881">X</span></span> | \- | <span data-ttu-id="47d74-882">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="47d74-882">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="47d74-883">ANFORDERUNGSZEITEN DER \_ WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="47d74-883">WINHTTP\_OPTION\_REQUEST\_TIMES</span></span><br/>[<span data-ttu-id="47d74-884">**\_WINHTTP-ANFORDERUNGSZEITEN \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-884">**WINHTTP\_REQUEST\_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | <span data-ttu-id="47d74-885">X</span><span class="sxs-lookup"><span data-stu-id="47d74-885">X</span></span> | <span data-ttu-id="47d74-886">X</span><span class="sxs-lookup"><span data-stu-id="47d74-886">X</span></span> | \- | <span data-ttu-id="47d74-887">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="47d74-887">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="47d74-888">WINHTTP \_ OPTION \_ REQUIRE \_ STREAM \_ END</span><span class="sxs-lookup"><span data-stu-id="47d74-888">WINHTTP\_OPTION\_REQUIRE\_STREAM\_END</span></span><br/><span data-ttu-id="47d74-889">**Bool**</span><span class="sxs-lookup"><span data-stu-id="47d74-889">**BOOL**</span></span> | <span data-ttu-id="47d74-890">X</span><span class="sxs-lookup"><span data-stu-id="47d74-890">X</span></span> | <span data-ttu-id="47d74-891">X</span><span class="sxs-lookup"><span data-stu-id="47d74-891">X</span></span> | \- | <span data-ttu-id="47d74-892">X</span><span class="sxs-lookup"><span data-stu-id="47d74-892">X</span></span> | <span data-ttu-id="47d74-893">Windows 10 Version 21H1</span><span class="sxs-lookup"><span data-stu-id="47d74-893">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="47d74-894">WINHTTP \_ OPTION \_ RESOLUTION \_ HOSTNAME</span><span class="sxs-lookup"><span data-stu-id="47d74-894">WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME</span></span><br/><span data-ttu-id="47d74-895">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="47d74-895">**LPWSTR**</span></span> | \- | <span data-ttu-id="47d74-896">X</span><span class="sxs-lookup"><span data-stu-id="47d74-896">X</span></span> | \- | <span data-ttu-id="47d74-897">X</span><span class="sxs-lookup"><span data-stu-id="47d74-897">X</span></span> | <span data-ttu-id="47d74-898">Windows 10 Version 21H1</span><span class="sxs-lookup"><span data-stu-id="47d74-898">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="47d74-899">TIMEOUT FÜR AUFLÖSUNG DER \_ WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="47d74-899">WINHTTP\_OPTION\_RESOLVE\_TIMEOUT</span></span><br/><span data-ttu-id="47d74-900">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-900">**DWORD**</span></span> | <span data-ttu-id="47d74-901">X</span><span class="sxs-lookup"><span data-stu-id="47d74-901">X</span></span> | <span data-ttu-id="47d74-902">X</span><span class="sxs-lookup"><span data-stu-id="47d74-902">X</span></span> | <span data-ttu-id="47d74-903">X</span><span class="sxs-lookup"><span data-stu-id="47d74-903">X</span></span> | <span data-ttu-id="47d74-904">X</span><span class="sxs-lookup"><span data-stu-id="47d74-904">X</span></span> | \- |
| <span data-ttu-id="47d74-905">SICHERE PROTOKOLLE \_ DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="47d74-905">WINHTTP\_OPTION\_SECURE\_PROTOCOLS</span></span><br/><span data-ttu-id="47d74-906">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-906">**DWORD**</span></span> | <span data-ttu-id="47d74-907">X</span><span class="sxs-lookup"><span data-stu-id="47d74-907">X</span></span> | \- | \- | <span data-ttu-id="47d74-908">X</span><span class="sxs-lookup"><span data-stu-id="47d74-908">X</span></span> | \- |
| <span data-ttu-id="47d74-909">\_SICHERHEITSZERTIFIKATSTRUKTUR DER WINHTTP-OPTION \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="47d74-909">WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT</span></span><br/>[<span data-ttu-id="47d74-910">**\_WINHTTP-ZERTIFIKATINFORMATIONEN \_**</span><span class="sxs-lookup"><span data-stu-id="47d74-910">**WINHTTP\_CERTIFICATE\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | <span data-ttu-id="47d74-911">X</span><span class="sxs-lookup"><span data-stu-id="47d74-911">X</span></span> | <span data-ttu-id="47d74-912">X</span><span class="sxs-lookup"><span data-stu-id="47d74-912">X</span></span> | \- | \- |
| <span data-ttu-id="47d74-913">\_SICHERHEITSFLAGS FÜR DIE WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="47d74-913">WINHTTP\_OPTION\_SECURITY\_FLAGS</span></span><br/><span data-ttu-id="47d74-914">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-914">**DWORD**</span></span> | \- | <span data-ttu-id="47d74-915">X</span><span class="sxs-lookup"><span data-stu-id="47d74-915">X</span></span> | <span data-ttu-id="47d74-916">X</span><span class="sxs-lookup"><span data-stu-id="47d74-916">X</span></span> | <span data-ttu-id="47d74-917">X</span><span class="sxs-lookup"><span data-stu-id="47d74-917">X</span></span> | \- |
| <span data-ttu-id="47d74-918">SICHERHEITSINFORMATIONEN \_ ZUR WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="47d74-918">WINHTTP\_OPTION\_SECURITY\_INFO</span></span><br/>[<span data-ttu-id="47d74-919">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="47d74-919">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | <span data-ttu-id="47d74-920">X</span><span class="sxs-lookup"><span data-stu-id="47d74-920">X</span></span> | <span data-ttu-id="47d74-921">X</span><span class="sxs-lookup"><span data-stu-id="47d74-921">X</span></span> | \- | <span data-ttu-id="47d74-922">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="47d74-922">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="47d74-923">\_WINHTTP-OPTION \_ \_ \_ SICHERHEITSSCHLÜSSELBITNESS</span><span class="sxs-lookup"><span data-stu-id="47d74-923">WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS</span></span><br/><span data-ttu-id="47d74-924">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-924">**DWORD**</span></span> | \- | <span data-ttu-id="47d74-925">X</span><span class="sxs-lookup"><span data-stu-id="47d74-925">X</span></span> | <span data-ttu-id="47d74-926">X</span><span class="sxs-lookup"><span data-stu-id="47d74-926">X</span></span> | \- | \- |
| <span data-ttu-id="47d74-927">TIMEOUT \_ BEIM SENDEN DER \_ \_ WINHTTP-OPTION</span><span class="sxs-lookup"><span data-stu-id="47d74-927">WINHTTP\_OPTION\_SEND\_TIMEOUT</span></span><br/><span data-ttu-id="47d74-928">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-928">**DWORD**</span></span> | <span data-ttu-id="47d74-929">X</span><span class="sxs-lookup"><span data-stu-id="47d74-929">X</span></span> | <span data-ttu-id="47d74-930">X</span><span class="sxs-lookup"><span data-stu-id="47d74-930">X</span></span> | <span data-ttu-id="47d74-931">X</span><span class="sxs-lookup"><span data-stu-id="47d74-931">X</span></span> | <span data-ttu-id="47d74-932">X</span><span class="sxs-lookup"><span data-stu-id="47d74-932">X</span></span> | \- |
| <span data-ttu-id="47d74-933">WINHTTP \_ OPTION \_ SERVER \_ CBT</span><span class="sxs-lookup"><span data-stu-id="47d74-933">WINHTTP\_OPTION\_SERVER\_CBT</span></span><br/><span data-ttu-id="47d74-934">[**\_SecPkgContext-Bindungen**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span><span class="sxs-lookup"><span data-stu-id="47d74-934">[**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span></span> | \- | <span data-ttu-id="47d74-935">X</span><span class="sxs-lookup"><span data-stu-id="47d74-935">X</span></span> | <span data-ttu-id="47d74-936">X</span><span class="sxs-lookup"><span data-stu-id="47d74-936">X</span></span> | \- | \- |
| <span data-ttu-id="47d74-937">WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CHAIN \_ CONTEXT</span><span class="sxs-lookup"><span data-stu-id="47d74-937">WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT</span></span><br/>[<span data-ttu-id="47d74-938">**CERT_CHAIN_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="47d74-938">**CERT_CHAIN_CONTEXT**</span></span>](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | <span data-ttu-id="47d74-939">X</span><span class="sxs-lookup"><span data-stu-id="47d74-939">X</span></span> | <span data-ttu-id="47d74-940">X</span><span class="sxs-lookup"><span data-stu-id="47d74-940">X</span></span> | \- | <span data-ttu-id="47d74-941">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="47d74-941">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="47d74-942">WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CONTEXT</span><span class="sxs-lookup"><span data-stu-id="47d74-942">WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="47d74-943">**CERT-KONTEXT**</span><span class="sxs-lookup"><span data-stu-id="47d74-943">**CERT CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="47d74-944">X</span><span class="sxs-lookup"><span data-stu-id="47d74-944">X</span></span> | <span data-ttu-id="47d74-945">X</span><span class="sxs-lookup"><span data-stu-id="47d74-945">X</span></span> | \- | \- |
| <span data-ttu-id="47d74-946">VERWENDETER \_ \_ WINHTTP-OPTIONSSERVER-SPN \_ \_</span><span class="sxs-lookup"><span data-stu-id="47d74-946">WINHTTP\_OPTION\_SERVER\_SPN\_USED</span></span><br/><span data-ttu-id="47d74-947">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="47d74-947">**LPWSTR**</span></span> | \- | <span data-ttu-id="47d74-948">X</span><span class="sxs-lookup"><span data-stu-id="47d74-948">X</span></span> | <span data-ttu-id="47d74-949">X</span><span class="sxs-lookup"><span data-stu-id="47d74-949">X</span></span> | \- | \- |
| <span data-ttu-id="47d74-950">\_ \_ WINHTTP-OPTIONS-SPN</span><span class="sxs-lookup"><span data-stu-id="47d74-950">WINHTTP\_OPTION\_SPN</span></span><br/><span data-ttu-id="47d74-951">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-951">**DWORD**</span></span> | \- | <span data-ttu-id="47d74-952">X</span><span class="sxs-lookup"><span data-stu-id="47d74-952">X</span></span> | \- | <span data-ttu-id="47d74-953">X</span><span class="sxs-lookup"><span data-stu-id="47d74-953">X</span></span> | \- |
| <span data-ttu-id="47d74-954">\_ \_ WINHTTP-OPTIONSSTREAMFEHLERCODE \_ \_</span><span class="sxs-lookup"><span data-stu-id="47d74-954">WINHTTP\_OPTION\_STREAM\_ERROR\_CODE</span></span><br/><span data-ttu-id="47d74-955">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-955">**DWORD**</span></span> | \- | <span data-ttu-id="47d74-956">X</span><span class="sxs-lookup"><span data-stu-id="47d74-956">X</span></span> | <span data-ttu-id="47d74-957">X</span><span class="sxs-lookup"><span data-stu-id="47d74-957">X</span></span> | \- | <span data-ttu-id="47d74-958">Windows 10 Version 21H1</span><span class="sxs-lookup"><span data-stu-id="47d74-958">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="47d74-959">WINHTTP-OPTION \_ \_ TCP FAST \_ \_ OPEN</span><span class="sxs-lookup"><span data-stu-id="47d74-959">WINHTTP\_OPTION\_TCP\_FAST\_OPEN</span></span><br/><span data-ttu-id="47d74-960">**Bool**</span><span class="sxs-lookup"><span data-stu-id="47d74-960">**BOOL**</span></span> | <span data-ttu-id="47d74-961">X</span><span class="sxs-lookup"><span data-stu-id="47d74-961">X</span></span> | \- | \- | <span data-ttu-id="47d74-962">X</span><span class="sxs-lookup"><span data-stu-id="47d74-962">X</span></span> | <span data-ttu-id="47d74-963">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="47d74-963">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="47d74-964">\_WINHTTP-OPTION \_ TCP \_ KEEPALIVE</span><span class="sxs-lookup"><span data-stu-id="47d74-964">WINHTTP\_OPTION\_TCP\_KEEPALIVE</span></span><br/>[<span data-ttu-id="47d74-965">**tcp \_ keepalive**</span><span class="sxs-lookup"><span data-stu-id="47d74-965">**tcp\_keepalive**</span></span>](/windows/win32/winsock/sio-keepalive-vals) | <span data-ttu-id="47d74-966">X</span><span class="sxs-lookup"><span data-stu-id="47d74-966">X</span></span> | \- | \- | <span data-ttu-id="47d74-967">X</span><span class="sxs-lookup"><span data-stu-id="47d74-967">X</span></span> | <span data-ttu-id="47d74-968">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="47d74-968">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="47d74-969">WINHTTP-OPTION \_ \_ TLS FALSE \_ \_ START</span><span class="sxs-lookup"><span data-stu-id="47d74-969">WINHTTP\_OPTION\_TLS\_FALSE\_START</span></span><br/><span data-ttu-id="47d74-970">**Bool**</span><span class="sxs-lookup"><span data-stu-id="47d74-970">**BOOL**</span></span> | <span data-ttu-id="47d74-971">X</span><span class="sxs-lookup"><span data-stu-id="47d74-971">X</span></span> | \- | \- | <span data-ttu-id="47d74-972">X</span><span class="sxs-lookup"><span data-stu-id="47d74-972">X</span></span> | <span data-ttu-id="47d74-973">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="47d74-973">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="47d74-974">UNSICHERER \_ \_ \_ FALLBACK DES TLS-PROTOKOLLS DER \_ WINHTTP-OPTION \_</span><span class="sxs-lookup"><span data-stu-id="47d74-974">WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK</span></span><br/><span data-ttu-id="47d74-975">**Bool**</span><span class="sxs-lookup"><span data-stu-id="47d74-975">**BOOL**</span></span> | <span data-ttu-id="47d74-976">X</span><span class="sxs-lookup"><span data-stu-id="47d74-976">X</span></span> | \- | \- | <span data-ttu-id="47d74-977">X</span><span class="sxs-lookup"><span data-stu-id="47d74-977">X</span></span> | <span data-ttu-id="47d74-978">Windows 10 Version 21H1</span><span class="sxs-lookup"><span data-stu-id="47d74-978">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="47d74-979">WINHTTP-OPTION \_ \_ \_ ENTLADEBENACHRICHTIGUNGSEREIGNIS \_</span><span class="sxs-lookup"><span data-stu-id="47d74-979">WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT</span></span><br/>[<span data-ttu-id="47d74-980">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="47d74-980">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="47d74-981">X</span><span class="sxs-lookup"><span data-stu-id="47d74-981">X</span></span> | \- | \- | <span data-ttu-id="47d74-982">X</span><span class="sxs-lookup"><span data-stu-id="47d74-982">X</span></span> | \- |
| <span data-ttu-id="47d74-983">WINHTTP \_ OPTION \_ UNSAFE \_ HEADER \_ PARSING</span><span class="sxs-lookup"><span data-stu-id="47d74-983">WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING</span></span><br/><span data-ttu-id="47d74-984">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-984">**DWORD**</span></span> | \- | <span data-ttu-id="47d74-985">X</span><span class="sxs-lookup"><span data-stu-id="47d74-985">X</span></span> | \- | <span data-ttu-id="47d74-986">X</span><span class="sxs-lookup"><span data-stu-id="47d74-986">X</span></span> | \- |
| <span data-ttu-id="47d74-987">UPGRADE DER \_ \_ WINHTTP-OPTION \_ AUF \_ \_ WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="47d74-987">WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET</span></span><br/><span data-ttu-id="47d74-988">–</span><span class="sxs-lookup"><span data-stu-id="47d74-988">N/A</span></span> | \- | <span data-ttu-id="47d74-989">X</span><span class="sxs-lookup"><span data-stu-id="47d74-989">X</span></span> | \- | <span data-ttu-id="47d74-990">X</span><span class="sxs-lookup"><span data-stu-id="47d74-990">X</span></span> | \- |
| <span data-ttu-id="47d74-991">URL DER \_ \_ WINHTTP-OPTION</span><span class="sxs-lookup"><span data-stu-id="47d74-991">WINHTTP\_OPTION\_URL</span></span><br/><span data-ttu-id="47d74-992">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="47d74-992">**LPWSTR**</span></span> | \- | <span data-ttu-id="47d74-993">X</span><span class="sxs-lookup"><span data-stu-id="47d74-993">X</span></span> | <span data-ttu-id="47d74-994">X</span><span class="sxs-lookup"><span data-stu-id="47d74-994">X</span></span> | \- | \- |
| <span data-ttu-id="47d74-995">\_WINHTTP-OPTION \_ GLOBALE \_ SERVERANMELDEINFORMATIONEN \_ \_ VERWENDEN</span><span class="sxs-lookup"><span data-stu-id="47d74-995">WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS</span></span><br/><span data-ttu-id="47d74-996">**Bool**</span><span class="sxs-lookup"><span data-stu-id="47d74-996">**BOOL**</span></span> | <span data-ttu-id="47d74-997">X</span><span class="sxs-lookup"><span data-stu-id="47d74-997">X</span></span> | <span data-ttu-id="47d74-998">X</span><span class="sxs-lookup"><span data-stu-id="47d74-998">X</span></span> | \- | <span data-ttu-id="47d74-999">X</span><span class="sxs-lookup"><span data-stu-id="47d74-999">X</span></span> | \- |
| <span data-ttu-id="47d74-1000">\_BENUTZER-AGENT DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="47d74-1000">WINHTTP\_OPTION\_USER\_AGENT</span></span><br/><span data-ttu-id="47d74-1001">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="47d74-1001">**LPWSTR**</span></span> | <span data-ttu-id="47d74-1002">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1002">X</span></span> | \- | <span data-ttu-id="47d74-1003">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1003">X</span></span> | <span data-ttu-id="47d74-1004">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1004">X</span></span> | \- |
| <span data-ttu-id="47d74-1005">\_ \_ WINHTTP-OPTIONSBENUTZERNAME</span><span class="sxs-lookup"><span data-stu-id="47d74-1005">WINHTTP\_OPTION\_USERNAME</span></span><br/><span data-ttu-id="47d74-1006">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="47d74-1006">**LPWSTR**</span></span> | \- | <span data-ttu-id="47d74-1007">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1007">X</span></span> | <span data-ttu-id="47d74-1008">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1008">X</span></span> | <span data-ttu-id="47d74-1009">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1009">X</span></span> | \- |
| <span data-ttu-id="47d74-1010">\_WINHTTP-OPTION: \_ \_ TIMEOUT BEIM \_ SCHLIEßEN DES WEBSOCKET \_</span><span class="sxs-lookup"><span data-stu-id="47d74-1010">WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT</span></span><br/><span data-ttu-id="47d74-1011">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-1011">**DWORD**</span></span> | \- | \- | <span data-ttu-id="47d74-1012">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1012">X</span></span> | <span data-ttu-id="47d74-1013">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1013">X</span></span> | \- |
| <span data-ttu-id="47d74-1014">WINHTTP-OPTION \_ \_ WEB SOCKET \_ \_ KEEPALIVE \_ INTERVAL</span><span class="sxs-lookup"><span data-stu-id="47d74-1014">WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL</span></span><br/><span data-ttu-id="47d74-1015">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-1015">**DWORD**</span></span> | \- | \- | <span data-ttu-id="47d74-1016">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1016">X</span></span> | <span data-ttu-id="47d74-1017">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1017">X</span></span> | \- |
| <span data-ttu-id="47d74-1018">WINHTTP-OPTION \_ \_ \_ WEBSOCKET \_ \_ \_ EMPFANGSPUFFERGRÖßE</span><span class="sxs-lookup"><span data-stu-id="47d74-1018">WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="47d74-1019">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-1019">**DWORD**</span></span> | <span data-ttu-id="47d74-1020">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1020">X</span></span> | <span data-ttu-id="47d74-1021">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1021">X</span></span> | <span data-ttu-id="47d74-1022">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1022">X</span></span> | <span data-ttu-id="47d74-1023">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1023">X</span></span> | <span data-ttu-id="47d74-1024">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="47d74-1024">Windows 8.1</span></span> |
| <span data-ttu-id="47d74-1025">WINHTTP-OPTION \_ \_ \_ WEBSOCKET- \_ \_ \_ SENDEPUFFERGRÖßE</span><span class="sxs-lookup"><span data-stu-id="47d74-1025">WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="47d74-1026">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-1026">**DWORD**</span></span> | <span data-ttu-id="47d74-1027">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1027">X</span></span> | <span data-ttu-id="47d74-1028">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1028">X</span></span> | <span data-ttu-id="47d74-1029">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1029">X</span></span> | <span data-ttu-id="47d74-1030">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1030">X</span></span> | <span data-ttu-id="47d74-1031">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="47d74-1031">Windows 8.1</span></span> |
| <span data-ttu-id="47d74-1032">ANZAHL DER \_ \_ ARBEITSTHREADS \_ DER WINHTTP-OPTION \_</span><span class="sxs-lookup"><span data-stu-id="47d74-1032">WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT</span></span><br/><span data-ttu-id="47d74-1033">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-1033">**DWORD**</span></span> | \- | \- | \- | <span data-ttu-id="47d74-1034">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1034">X</span></span> | \- |
| <span data-ttu-id="47d74-1035">\_WINHTTP-OPTION: \_ \_ \_ SCHREIBPUFFERGRÖßE</span><span class="sxs-lookup"><span data-stu-id="47d74-1035">WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="47d74-1036">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47d74-1036">**DWORD**</span></span> | \- | <span data-ttu-id="47d74-1037">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1037">X</span></span> | <span data-ttu-id="47d74-1038">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1038">X</span></span> | <span data-ttu-id="47d74-1039">X</span><span class="sxs-lookup"><span data-stu-id="47d74-1039">X</span></span> | \- |

> [!Note]
> <span data-ttu-id="47d74-1040">Informationen zu Windows XP und Windows 2000 finden Sie unter [Laufzeitanforderungen.](winhttp-start-page.md)</span><span class="sxs-lookup"><span data-stu-id="47d74-1040">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="47d74-1041">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="47d74-1041">Requirements</span></span>

| <span data-ttu-id="47d74-1042">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47d74-1042">Requirement</span></span> | <span data-ttu-id="47d74-1043">Wert</span><span class="sxs-lookup"><span data-stu-id="47d74-1043">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="47d74-1044">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47d74-1044">Minimum supported client</span></span> | <span data-ttu-id="47d74-1045">Nur Windows XP, Windows 2000 Professional mit \[ SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47d74-1045">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>            |
| <span data-ttu-id="47d74-1046">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47d74-1046">Minimum supported server</span></span> | <span data-ttu-id="47d74-1047">Nur Windows Server 2003, Windows 2000 Server mit \[ SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47d74-1047">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>         |
| <span data-ttu-id="47d74-1048">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="47d74-1048">Redistributable</span></span>          | <span data-ttu-id="47d74-1049">WinHTTP 5.0 und Internet Explorer 5.01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="47d74-1049">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span> |
| <span data-ttu-id="47d74-1050">Header</span><span class="sxs-lookup"><span data-stu-id="47d74-1050">Header</span></span>                   | <span data-ttu-id="47d74-1051">Winhttp.h</span><span class="sxs-lookup"><span data-stu-id="47d74-1051">Winhttp.h</span></span>                                                                       |

## <a name="see-also"></a><span data-ttu-id="47d74-1052">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47d74-1052">See also</span></span>

[<span data-ttu-id="47d74-1053">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="47d74-1053">WinHTTP Versions</span></span>](winhttp-versions.md)
