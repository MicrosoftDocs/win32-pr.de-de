---
Description: Die folgenden Optionsflags werden von WinHttpQueryOption und WinHttpSetOption unterstützt.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Optionsflags (Winhttp.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: f9405d604318205b4e951d28d5b0c304a5f7ab71
ms.sourcegitcommit: d5f16b9d3d5d2e2080ba7b6837eb37250fa67a30
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/02/2021
ms.locfileid: "111349979"
---
# <a name="option-flags"></a><span data-ttu-id="a4cad-103">Optionsflags</span><span class="sxs-lookup"><span data-stu-id="a4cad-103">Option Flags</span></span>

<span data-ttu-id="a4cad-104">Die folgenden Optionsflags werden von [**WinHttpQueryOption und**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) [**WinHttpSetOption unterstützt.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)</span><span class="sxs-lookup"><span data-stu-id="a4cad-104">The following option flags are supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span>

<dl> <dt>

<span data-ttu-id="a4cad-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**\_WINHTTP-OPTION \_ \_ GARANTIERTE NICHT \_ \_ BLOCKIERENDE RÜCKRUFE**</span><span class="sxs-lookup"><span data-stu-id="a4cad-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-106">Der Standardwert lautet FALSE.</span><span class="sxs-lookup"><span data-stu-id="a4cad-106">The default is FALSE.</span></span> <span data-ttu-id="a4cad-107">Wenn der Status auf TRUE festgelegt ist, garantiert WinHTTP den Fortschritt nicht, wenn Statusrückrufe von der Clientanwendung blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-107">If set to TRUE, WinHTTP does not guarantee progress if status callbacks are blocked by the client application.</span></span>

<span data-ttu-id="a4cad-108">Die Clientanwendung muss besonders darauf achten, minimale Vorgänge innerhalb des Rückrufs ohne Blockierung durchzuführen, so schnell wie möglich zurückzukehren und insbesondere nicht auf nachfolgende WinHTTP-Aufrufe zu warten.</span><span class="sxs-lookup"><span data-stu-id="a4cad-108">The client application must take special care to perform minimal operations within the callback without blocking, returning as quickly as possible, and in particular must not wait for any subsequent WinHTTP calls.</span></span> <span data-ttu-id="a4cad-109">Wenn sie diese Richtlinien nicht einfängt, ist es wahrscheinlich, dass es negative Auswirkungen auf die Leistung oder eine potenzielle Anwendung gibt, die nicht mehr funktioniert.</span><span class="sxs-lookup"><span data-stu-id="a4cad-109">If it does not follow these guidelines, there is likely to be a negative performance impact or a potential application hang.</span></span> <span data-ttu-id="a4cad-110">Wenn diese Option auf die vorgeschriebene Weise verwendet wird, kann sie die Leistung verbessern.</span><span class="sxs-lookup"><span data-stu-id="a4cad-110">If used in the prescribed manner, this option may improve performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**RICHTLINIE FÜR \_ DIE AUTOMATISCHE ANMELDUNG DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-112">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Richtlinie für automatische [Anmeldung](authentication-in-winhttp.md) mit einem der folgenden Werte angibt.</span><span class="sxs-lookup"><span data-stu-id="a4cad-112">Sets an unsigned long integer value that specifies the [Automatic Logon Policy](authentication-in-winhttp.md) with one of the following values.</span></span>

| <span data-ttu-id="a4cad-113">Begriff</span><span class="sxs-lookup"><span data-stu-id="a4cad-113">Term</span></span> | <span data-ttu-id="a4cad-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4cad-114">Description</span></span> |
|-|-|
| <span data-ttu-id="a4cad-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ HIGH</span><span class="sxs-lookup"><span data-stu-id="a4cad-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH</span></span> | <span data-ttu-id="a4cad-116">Standardanmeldeinformationen werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4cad-116">Default credentials are not used.</span></span> <span data-ttu-id="a4cad-117">Beachten Sie, dass dieses Flag nur wirksam wird, wenn Sie den Server mit dem tatsächlichen Computernamen angeben.</span><span class="sxs-lookup"><span data-stu-id="a4cad-117">Note that this flag takes effect only if you specify the server by the actual machine name.</span></span> <span data-ttu-id="a4cad-118">Sie wird nicht wirksam, wenn Sie den Server mit "localhost" oder IP-Adresse angeben.</span><span class="sxs-lookup"><span data-stu-id="a4cad-118">It will not take effect, if you specify the server by "localhost" or IP address.</span></span> |
| <span data-ttu-id="a4cad-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ LOW</span><span class="sxs-lookup"><span data-stu-id="a4cad-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW</span></span> | <span data-ttu-id="a4cad-120">Für alle Anforderungen wird eine authentifizierte Anmeldung mit den Standardanmeldeinformationen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="a4cad-120">An authenticated log on using the default credentials is performed for all requests.</span></span> |
| <span data-ttu-id="a4cad-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ MEDIUM</span><span class="sxs-lookup"><span data-stu-id="a4cad-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM</span></span> | <span data-ttu-id="a4cad-122">Eine authentifizierte Anmeldung mit den Standardanmeldeinformationen wird nur für Anforderungen im lokalen Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a4cad-122">An authenticated log on using the default credentials is performed only for requests on the local Intranet.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a4cad-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**\_ \_ WINHTTP-OPTIONSRÜCKRUF**</span><span class="sxs-lookup"><span data-stu-id="a4cad-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-124">Ruft den Zeiger auf den Rückruffunktionssatz mit [**WinHttpSetStatusCallback ab.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)</span><span class="sxs-lookup"><span data-stu-id="a4cad-124">Retrieves the pointer to the callback function set with [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP \_ OPTION \_ CLIENT \_ CERT \_ CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="a4cad-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-126">Legt den Clientzertifikatkontext fest.</span><span class="sxs-lookup"><span data-stu-id="a4cad-126">Sets the client certificate context.</span></span> <span data-ttu-id="a4cad-127">Wenn eine Anwendung [**DEN FEHLER \_ WINHTTP CLIENT \_ \_ AUTH \_ CERT \_ NEEDED**](error-messages.md)empfängt, muss sie [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) aufrufen, um ein Zertifikat zur Verfügung zu stellen, bevor die Anforderung erneut ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4cad-127">If an application receives [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md), it must call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="a4cad-128">Im Rahmen der Verarbeitung dieser Option ruft WinHttp [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) im vom Aufrufer bereitgestellten Zertifikatkontext auf, damit der Zertifikatkontext unabhängig vom Aufrufer freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="a4cad-128">As a part of processing this option, WinHttp calls [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) on the caller-provided certificate context so that the certificate context can be independently released by the caller.</span></span>

> [!Note]
> <span data-ttu-id="a4cad-129">Die Anwendung sollte nicht versuchen, den Zertifikatspeicher mit dem Flag CERT CLOSE STORE FORCE FLAG im Aufruf von \_ \_ \_ \_ [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) in dem Zertifikatspeicher zu schließen, aus dem der Zertifikatkontext abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a4cad-129">The application should not attempt to close the certificate store with the CERT\_CLOSE\_STORE\_FORCE\_FLAG flag in the call to [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) on the certificate store from which the certificate context was retrieved.</span></span> <span data-ttu-id="a4cad-130">Es kann zu einer Zugriffsverletzung kommen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-130">An access violation may occur.</span></span>

<span data-ttu-id="a4cad-131">Wenn der Server ein Clientzertifikat anfordert, [**gibt WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)oder [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) einen [**ERROR \_ WINHTTP CLIENT \_ \_ AUTH \_ CERT \_ NEEDED-Fehler**](error-messages.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="a4cad-131">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md) error.</span></span> <span data-ttu-id="a4cad-132">Wenn der Server das Zertifikat an fordert, es aber nicht erfordert, kann die Anwendung diese Option angeben, um anzugeben, dass er kein Zertifikat hat.</span><span class="sxs-lookup"><span data-stu-id="a4cad-132">If the server requests the certificate but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="a4cad-133">Der Server kann ein anderes Authentifizierungsschema auswählen oder anonymen Zugriff auf den Server zulassen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-133">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="a4cad-134">Die Anwendung stellt das **WINHTTP \_ NO CLIENT \_ \_ CERT \_ CONTEXT-Makro** im *lpBuffer-Parameter* von [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) wie im folgenden Codebeispiel gezeigt zur Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a4cad-134">The application provides the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

<span data-ttu-id="a4cad-135">Wenn der Server ein Clientzertifikat erfordert, kann er als Antwort den HTTP-Statuscode 403 senden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-135">If the server requires a client certificate, it may send a 403 HTTP status code in response.</span></span> <span data-ttu-id="a4cad-136">Weitere Informationen finden Sie unter DER **OPTION WINHTTP \_ OPTION CLIENT \_ \_ CERT ISSUER \_ \_ LIST.**</span><span class="sxs-lookup"><span data-stu-id="a4cad-136">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**\_WINHTTP-OPTION \_ \_ CLIENTZERTIFIKATAUSSTELLERLISTE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-138">Ruft eine [**SecPkgContext \_ IssuerListInfoEx-Struktur**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) ab, wenn der Fehler aus [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) oder [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) **ERROR \_ WINHTTP CLIENT \_ \_ AUTH \_ CERT NEEDED \_ lautet.**</span><span class="sxs-lookup"><span data-stu-id="a4cad-138">Retrieves a [**SecPkgContext\_IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure when the error from [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) is **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="a4cad-139">Die Ausstellerliste in der Struktur enthält eine Liste der zulässigen Zertifizierungsstellen (Certificate Authorities, CA) vom Server.</span><span class="sxs-lookup"><span data-stu-id="a4cad-139">The issuer list in the structure contains a list of acceptable Certificate Authorities (CA) from the server.</span></span> <span data-ttu-id="a4cad-140">Die Clientanwendung kann die Zertifizierungsstellenliste filtern, um das Clientzertifikat für die SSL-Authentifizierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-140">The client application can filter the CA list to retrieve the client certificate for SSL authentication.</span></span>

<span data-ttu-id="a4cad-141">Alternativ kann die Anwendung [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit der OPTION **WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ CONTEXT** aufrufen, wenn der Server das Clientzertifikat an fordert, es aber nicht erfordert.</span><span class="sxs-lookup"><span data-stu-id="a4cad-141">Alternately, if the server requests the client certificate, but does not require it, the application can call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="a4cad-142">Weitere Informationen finden Sie unter DER **OPTION WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ CONTEXT.**</span><span class="sxs-lookup"><span data-stu-id="a4cad-142">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**\_ \_ WINHTTP-OPTIONSCODEPAGE**</span><span class="sxs-lookup"><span data-stu-id="a4cad-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-144">Legt die [*Codepage fest,*](glossary.md) die zum Verarbeiten der URL verwendet wird (d. h. Abfragezeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="a4cad-144">Sets the [*code page*](glossary.md) that is used to process the URL (that is, query string).</span></span> <span data-ttu-id="a4cad-145">Der Standardwert ist UTF8.</span><span class="sxs-lookup"><span data-stu-id="a4cad-145">The default is UTF8.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_WINHTTP-OPTION: \_ \_ KONFIGURIEREN DER \_ PASSPORT-AUTHENTIFIZIERUNG**</span><span class="sxs-lookup"><span data-stu-id="a4cad-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-147">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, ob [die Passport-Authentifizierung in der WinHTTP-Authentifizierung](passport-authentication-in-winhttp.md) aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a4cad-147">Sets an unsigned long integer value that specifies whether [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md) authentication is enabled.</span></span> <span data-ttu-id="a4cad-148">Der Wert kann in folgenden Formen vorliegen:</span><span class="sxs-lookup"><span data-stu-id="a4cad-148">The value can be one of the following:</span></span>

| <span data-ttu-id="a4cad-149">Begriff</span><span class="sxs-lookup"><span data-stu-id="a4cad-149">Term</span></span> | <span data-ttu-id="a4cad-150">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4cad-150">Description</span></span> |
|-|-|
| <span data-ttu-id="a4cad-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ DEAKTIVIEREN \_ DER \_ PASSPORT-AUTHENTIFIZIERUNG</span><span class="sxs-lookup"><span data-stu-id="a4cad-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP\_DISABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="a4cad-152">Microsoft Passport Authentifizierung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a4cad-152">Microsoft Passport authentication is disabled.</span></span> <span data-ttu-id="a4cad-153">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="a4cad-153">This is the default.</span></span> |
| <span data-ttu-id="a4cad-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ DEAKTIVIEREN VON PASSPORT \_ \_ KEYRING</span><span class="sxs-lookup"><span data-stu-id="a4cad-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP\_DISABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="a4cad-155">Der Passport-Schlüsselring ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a4cad-155">The Passport keyring is disabled.</span></span> <span data-ttu-id="a4cad-156">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="a4cad-156">This is the default.</span></span> |
| <span data-ttu-id="a4cad-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ AUTH</span><span class="sxs-lookup"><span data-stu-id="a4cad-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP\_ENABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="a4cad-158">Die Passport-Authentifizierung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a4cad-158">Passport authentication is enabled.</span></span> |
| <span data-ttu-id="a4cad-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ KEYRING</span><span class="sxs-lookup"><span data-stu-id="a4cad-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP\_ENABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="a4cad-160">Der Passport-Schlüsselring ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a4cad-160">The Passport keyring is enabled.</span></span> |

</dl> </dd> <dt>

<span data-ttu-id="a4cad-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**\_WINHTTP-OPTION \_ – \_ VERBINDUNGS-RETRIES**</span><span class="sxs-lookup"><span data-stu-id="a4cad-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-162">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Anzahl der Versuche vonWinHTTP enthält, eine Verbindung mit einem Host herzustellen, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="a4cad-162">Sets or retrieves an unsigned long integer value that contains the number of timesWinHTTP attempts to connect to a host.</span></span> <span data-ttu-id="a4cad-163">Microsoft Windows HTTP Services (WinHTTP) versucht nur einmal pro IP-Adresse (InternetProtokoll).</span><span class="sxs-lookup"><span data-stu-id="a4cad-163">Microsoft Windows HTTP Services (WinHTTP) only attempts once per Internet Protocol (IP) address.</span></span> <span data-ttu-id="a4cad-164">Wenn Sie beispielsweise versuchen, eine Verbindung mit einem mehrfach vernetzten Host herzustellen, der über 10 IP-Adressen verfügt und **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** auf 7 festgelegt ist, versucht WinHTTP nur, eine Verbindung mit den ersten sieben IP-Adressen herzustellen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-164">For example, if you attempt to connect to a multihomed host that has 10 IP addresses and **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 7, then WinHTTP only attempts to connect to the first seven IP address.</span></span> <span data-ttu-id="a4cad-165">Wenn **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** auf 20 festgelegt ist, versucht WinHTTP bei 10 IP-Adressen nur einmal, jede der zehn IP-Adressen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-165">Given the same set of 10 IP addresses, if **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 20, WinHTTP attempts each of the 10 only once.</span></span> <span data-ttu-id="a4cad-166">Wenn ein Verbindungsversuch nach der angegebenen Anzahl von Versuchen weiterhin fehlschlägt oder das Verbindungszeitout vor diesem Zeitpunkt abgelaufen ist, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-166">If a connection attempt still fails after the specified number of attempts, or if the connect timeout expired before then, the request is canceled.</span></span> <span data-ttu-id="a4cad-167">Der Standardwert für **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** ist fünf Versuche.</span><span class="sxs-lookup"><span data-stu-id="a4cad-167">The default value for **WINHTTP\_OPTION\_CONNECT\_RETRIES** is five attempts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP \_ OPTION \_ CONNECT \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="a4cad-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-169">Legt einen ganzzahligen Wert ohne Vorzeichen, der den Time out-Wert enthält, in Millisekunden fest oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="a4cad-169">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds.</span></span> <span data-ttu-id="a4cad-170">Wenn Sie diese Option auf unendlich (0xFFFFFFFF) festlegen, wird dieser Timer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a4cad-170">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="a4cad-171">Wenn eine TCP-Verbindungsanforderung länger als dieser Time out-Wert dauert, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-171">If a TCP connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="a4cad-172">Das Standard-Timeout beträgt 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-172">The default timeout is 60 seconds.</span></span> <span data-ttu-id="a4cad-173">Wenn Sie versuchen, eine Verbindung mit mehreren IP-Adressen für einen einzelnen Host (einen mehrfach vernetzten Host) herzustellen, gilt das Timeoutlimit für jede einzelne Verbindung.</span><span class="sxs-lookup"><span data-stu-id="a4cad-173">When you are attempting to connect to multiple IP addresses for a single host (a multihomed host), the timeout limit is for each individual connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**VERBINDUNGSINFORMATIONEN \_ ZUR WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP\_OPTION\_CONNECTION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-175">Ruft die Quell- und Ziel-IP-Adresse und den Port der Anforderung ab, die die Antwort generiert hat, wenn [**WinHttpReceiveResponse zurückgegeben**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) wird.</span><span class="sxs-lookup"><span data-stu-id="a4cad-175">Retrieves the source and destination IP address, and port of the request that generated the response when [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns.</span></span> <span data-ttu-id="a4cad-176">Die Anwendung ruft [**WinHttpQueryOption mit**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) der **OPTION WINHTTP OPTION CONNECTION \_ \_ \_ INFO** auf und stellt die [**WINHTTP CONNECTION \_ \_ INFO-Struktur**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) im *lpBuffer-Parameter* zur Auswahl.</span><span class="sxs-lookup"><span data-stu-id="a4cad-176">The application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CONNECTION\_INFO** option, and provides the [**WINHTTP\_CONNECTION\_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) structure in the *lpBuffer* parameter.</span></span> <span data-ttu-id="a4cad-177">Weitere Informationen finden Sie unter **WINHTTP \_ CONNECTION \_ INFO**.</span><span class="sxs-lookup"><span data-stu-id="a4cad-177">For more information, see **WINHTTP\_CONNECTION\_INFO**.</span></span>

<span data-ttu-id="a4cad-178">**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="a4cad-178">**Windows Server 2003 with SP1 and Windows XP with SP2:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V0**</span><span class="sxs-lookup"><span data-stu-id="a4cad-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V0**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-180">Retreives die [**TCP \_ INFO \_ v0-Struktur**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) für die zugrunde liegende Verbindung, die von der Anforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a4cad-180">Retreives the [**TCP\_INFO\_v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="a4cad-181">Die zurückgegebene Struktur kann Statistiken aus vorherigen Anforderungen enthalten, die über dieselbe Verbindung gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-181">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>

> [!Note]
> <span data-ttu-id="a4cad-182">Diese Option wurde durch **WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1 ersetzt.**</span><span class="sxs-lookup"><span data-stu-id="a4cad-182">This option has been superseded by **WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1**</span><span class="sxs-lookup"><span data-stu-id="a4cad-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-184">Retreives die [**TCP \_ INFO \_ v1-Struktur**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) für die zugrunde liegende Verbindung, die von der Anforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a4cad-184">Retreives the [**TCP\_INFO\_v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="a4cad-185">Die zurückgegebene Struktur kann Statistiken aus vorherigen Anforderungen enthalten, die über dieselbe Verbindung gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-185">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**KONTEXTWERT \_ DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-187">Legt eine **\_ DWORD-PTR fest** oder ruft sie ab, die einen Zeiger auf den Kontextwert enthält, der diesem [HINTERNET-Handle zugeordnet](hinternet-handles-in-winhttp.md) ist.</span><span class="sxs-lookup"><span data-stu-id="a4cad-187">Sets or retrieves a **DWORD\_PTR** that contains a pointer to the context value associated with this [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span> <span data-ttu-id="a4cad-188">Der im Puffer gespeicherte Wert wird verwendet, und dem **Optionsflag WINHTTP \_ OPTION CONTEXT \_ \_ VALUE** wird ein neuer Wert zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-188">The value stored in the buffer is used and the **WINHTTP\_OPTION\_CONTEXT\_VALUE** option flag is assigned a new value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**DEKOMPRIMIERUNG \_ DER WINHTTP-OPTION \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP\_OPTION\_DECOMPRESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-190">Legt ein DWORD von Flags fest, die bestimmen, ob WinHTTP Antwortkörper automatisch mit komprimierten Inhaltscodierungen dekomprimiert.</span><span class="sxs-lookup"><span data-stu-id="a4cad-190">Sets a DWORD of flags which determine whether WinHTTP will automatically decompress response bodies with compressed Content-Encodings.</span></span> <span data-ttu-id="a4cad-191">WinHTTP wird auch einen geeigneten Accept-Encoding festlegen und alle vom Aufrufer bereitgestellten überschreiben.</span><span class="sxs-lookup"><span data-stu-id="a4cad-191">WinHTTP will also set an appropriate Accept-Encoding header, overriding any supplied by the caller.</span></span> <span data-ttu-id="a4cad-192">Diese Werte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="a4cad-192">Supported values are:</span></span>

| <span data-ttu-id="a4cad-193">Begriff</span><span class="sxs-lookup"><span data-stu-id="a4cad-193">Term</span></span> | <span data-ttu-id="a4cad-194">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4cad-194">Description</span></span> |
|-|-|
| <span data-ttu-id="a4cad-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>\_WINHTTP-DEKOMPRIMIERUNGSFLAG \_ \_ GZIP</span><span class="sxs-lookup"><span data-stu-id="a4cad-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP\_DECOMPRESSION\_FLAG\_GZIP</span></span> | <span data-ttu-id="a4cad-196">Dekomprimieren der Inhaltscodierung: gzip-Antworten.</span><span class="sxs-lookup"><span data-stu-id="a4cad-196">Decompress Content-Encoding: gzip responses.</span></span> |
| <span data-ttu-id="a4cad-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>DEFLATE DES \_ WINHTTP-DEKOMPRIMIERUNGSFLAGS \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP\_DECOMPRESSION\_FLAG\_DEFLATE</span></span> | <span data-ttu-id="a4cad-198">Dekomprimieren der Inhaltscodierung: Verfeinern von Antworten.</span><span class="sxs-lookup"><span data-stu-id="a4cad-198">Decompress Content-Encoding: deflate responses.</span></span> |
| <span data-ttu-id="a4cad-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>\_WINHTTP-DEKOMPRIMIERUNGSFLAG \_ \_ ALL</span><span class="sxs-lookup"><span data-stu-id="a4cad-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP\_DECOMPRESSION\_FLAG\_ALL</span></span> | <span data-ttu-id="a4cad-200">Dekomprimieren Sie Antworten mit allen unterstützten Inhaltscodierungen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-200">Decompress responses with any supported Content-Encoding.</span></span> |

<span data-ttu-id="a4cad-201">Standardmäßig übermittelt WinHTTP komprimierte Antworten unverändert an den Aufrufer.</span><span class="sxs-lookup"><span data-stu-id="a4cad-201">By default, WinHTTP will deliver compressed responses to the caller unmodified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP \_ OPTION \_ DISABLE \_ FEATURE**</span><span class="sxs-lookup"><span data-stu-id="a4cad-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP\_OPTION\_DISABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-203">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, welche Features mit einem oder mehreren der folgenden Flags deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-203">Sets an unsigned long integer value that specifies which features are disabled with one or more of the following flags.</span></span> <span data-ttu-id="a4cad-204">Beachten Sie, dass dieses Feature nur bei Anforderungshandles an [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) übergeben werden sollte, nachdem das Anforderungshandle mit [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellt wurde und bevor die Anforderung mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a4cad-204">Be aware that this feature should only be passed to [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) on request handles after the request handle is created with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), and before the request is sent with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

| <span data-ttu-id="a4cad-205">Begriff</span><span class="sxs-lookup"><span data-stu-id="a4cad-205">Term</span></span> | <span data-ttu-id="a4cad-206">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4cad-206">Description</span></span> |
|-|-|
| <span data-ttu-id="a4cad-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP \_ DISABLE \_ AUTHENTICATION</span><span class="sxs-lookup"><span data-stu-id="a4cad-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP\_DISABLE\_AUTHENTICATION</span></span> | <span data-ttu-id="a4cad-208">Die automatische Authentifizierung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a4cad-208">Automatic authentication is disabled.</span></span> |
| <span data-ttu-id="a4cad-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP \_ DISABLE \_ COOKIES</span><span class="sxs-lookup"><span data-stu-id="a4cad-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP\_DISABLE\_COOKIES</span></span> | <span data-ttu-id="a4cad-210">Das automatische Hinzufügen von Cookieheadern zu Anforderungen ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a4cad-210">Automatic addition of cookie headers to requests is disabled.</span></span> <span data-ttu-id="a4cad-211">Außerdem werden zurückgegebene Cookies nicht automatisch zur Cookiedatenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a4cad-211">Also, returned cookies are not automatically added to the cookie database.</span></span> <span data-ttu-id="a4cad-212">Das Deaktivieren von Cookies kann zu einer schlechten Leistung bei der Passport-Authentifizierung führen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-212">Disabling cookies can result in poor performance for Passport authentication.</span></span> |
| <span data-ttu-id="a4cad-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ DISABLE \_ KEEP \_ ALIVE</span><span class="sxs-lookup"><span data-stu-id="a4cad-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP\_DISABLE\_KEEP\_ALIVE</span></span> | <span data-ttu-id="a4cad-214">Deaktiviert die Keep-Alive-Semantik für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="a4cad-214">Disables keep-alive semantics for the connection.</span></span> <span data-ttu-id="a4cad-215">Keep-Alive-Semantik ist für MSN, NTLM und andere Authentifizierungstypen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a4cad-215">Keep-alive semantics are required for MSN, NTLM, and other types of authentication.</span></span> |
| <span data-ttu-id="a4cad-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP \_ DISABLE \_ REDIRECTS</span><span class="sxs-lookup"><span data-stu-id="a4cad-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP\_DISABLE\_REDIRECTS</span></span> | <span data-ttu-id="a4cad-217">Die automatische Umleitung ist deaktiviert, wenn Anforderungen mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-217">Automatic redirection is disabled when sending requests with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="a4cad-218">Wenn die automatische Umleitung deaktiviert ist, muss eine Anwendung eine Rückruffunktion registrieren, damit die Passport-Authentifizierung erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a4cad-218">If automatic redirection is disabled, an application must register a callback function in order for Passport authentication to succeed.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a4cad-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**\_WINHTTP-OPTION \_ DISABLE SECURE \_ PROTOCOL \_ \_ FALLBACK**</span><span class="sxs-lookup"><span data-stu-id="a4cad-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-220">Verhindert, dass WinHTTP eine Verbindung mit einer niedrigeren Version des Sicherheitsprotokolls erneut versucht, wenn die anfängliche Protokollaushandlung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="a4cad-220">Prevents WinHTTP from retrying a connection with a lower version of the security protocol when the initial protocol negotiation fails.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**\_WINHTTP-OPTION \_ : DEAKTIVIEREN DER \_ \_ STREAMWARTESCHLANGE**</span><span class="sxs-lookup"><span data-stu-id="a4cad-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-222">Ermöglicht es neuen Anforderungen, eine zusätzliche HTTP/2-Verbindung zu öffnen, wenn der maximale Grenzwert für gleichzeitige Streams erreicht ist, anstatt auf den nächsten verfügbaren Stream auf einer vorhandenen Verbindung zu warten.</span><span class="sxs-lookup"><span data-stu-id="a4cad-222">Allows new requests to open an additional HTTP/2 connection when the maximum concurrent stream limit is reached, rather than waiting for the next available stream on an existing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP \_ OPTION \_ ENABLE \_ FEATURE**</span><span class="sxs-lookup"><span data-stu-id="a4cad-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP\_OPTION\_ENABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-224">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die derzeit aktivierten Features angibt.</span><span class="sxs-lookup"><span data-stu-id="a4cad-224">Sets an unsigned long integer value that specifies the features currently enabled.</span></span> <span data-ttu-id="a4cad-225">Kann einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="a4cad-225">Can be one of the following values.</span></span>

| <span data-ttu-id="a4cad-226">Begriff</span><span class="sxs-lookup"><span data-stu-id="a4cad-226">Term</span></span> | <span data-ttu-id="a4cad-227">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4cad-227">Description</span></span> |
|-|-|
| <span data-ttu-id="a4cad-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVERT \_ IMPERSONATION</span><span class="sxs-lookup"><span data-stu-id="a4cad-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP\_ENABLE\_SSL\_REVERT\_IMPERSONATION</span></span> | <span data-ttu-id="a4cad-229">Wenn diese Option aktiviert ist, stellt WinHTTP den Clientidentitätswechsel für die Dauer der Authentifizierungsvorgänge für SSL-Zertifikate vorübergehend wieder her.</span><span class="sxs-lookup"><span data-stu-id="a4cad-229">If enabled, WinHTTP temporarily reverts client impersonation for the duration of SSL certificate authentication operations.</span></span> <span data-ttu-id="a4cad-230">Dieser Wert kann nur für das Sitzungshandle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-230">This value can be set only on the session handle.</span></span> |
| <span data-ttu-id="a4cad-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVOCATION</span><span class="sxs-lookup"><span data-stu-id="a4cad-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP\_ENABLE\_SSL\_REVOCATION</span></span> | <span data-ttu-id="a4cad-232">Wenn diese Option aktiviert ist, lässt WinHTTP SSL-Sperrung zu.</span><span class="sxs-lookup"><span data-stu-id="a4cad-232">If enabled, WinHTTP allows SSL revocation.</span></span> <span data-ttu-id="a4cad-233">Dieser Wert kann nur für das Anforderungshandle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-233">This value can be set only on the request handle.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**\_WINHTTP-OPTION: \_ AKTIVIEREN DES \_ \_ HTTP-PROTOKOLLS**</span><span class="sxs-lookup"><span data-stu-id="a4cad-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-235">Legt eine DWORD-Bitmaske mit akzeptablen erweiterten HTTP-Versionen fest.</span><span class="sxs-lookup"><span data-stu-id="a4cad-235">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="a4cad-236">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="a4cad-236">Possible values are:</span></span>

| <span data-ttu-id="a4cad-237">Begriff</span><span class="sxs-lookup"><span data-stu-id="a4cad-237">Term</span></span> | <span data-ttu-id="a4cad-238">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4cad-238">Description</span></span> |
|-|-|
| <span data-ttu-id="a4cad-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>\_WINHTTP-PROTOKOLLFLAG \_ \_ HTTP2 (0x1)</span><span class="sxs-lookup"><span data-stu-id="a4cad-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP\_PROTOCOL\_FLAG\_HTTP2 (0x1)</span></span> | <span data-ttu-id="a4cad-240">Aktiviert HTTP/2 für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a4cad-240">Enables HTTP/2 for the request.</span></span> |
| <span data-ttu-id="a4cad-241">None (0x0)</span><span class="sxs-lookup"><span data-stu-id="a4cad-241">None (0x0)</span></span> | <span data-ttu-id="a4cad-242">Schränkt die Anforderung auf HTTP/1.1 und früher ein.</span><span class="sxs-lookup"><span data-stu-id="a4cad-242">Restricts the request to HTTP/1.1 and prior.</span></span> |

<span data-ttu-id="a4cad-243">Legacyversionen von HTTP (1.1 und früher) können mit dieser Option nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-243">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="a4cad-244">Der Standardwert ist 0x0.</span><span class="sxs-lookup"><span data-stu-id="a4cad-244">The default is 0x0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-245"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**\_WINHTTP-OPTION \_ ENABLETRACING**</span><span class="sxs-lookup"><span data-stu-id="a4cad-245"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP\_OPTION\_ENABLETRACING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-246">Legt einen **BOOL-Wert** fest, der angibt, ob die Ablaufverfolgung derzeit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a4cad-246">Sets a **BOOL** value that specifies whether tracing is currently enabled.</span></span> <span data-ttu-id="a4cad-247">Weitere Informationen zur Ablaufverfolgungsfunktion in WinHTTP finden Sie unter [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="a4cad-247">For more information about the trace facility in WinHTTP, see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span> <span data-ttu-id="a4cad-248">Diese Option kann nur für ein **NULL** **HINTERNET-Handle** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-248">This option can only be set on a **NULL** **HINTERNET** handle.</span></span>


</dt> </dl> </dd>

<dt>

<span data-ttu-id="a4cad-249"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP \_ OPTION \_ ENCODE \_ EXTRA**</span><span class="sxs-lookup"><span data-stu-id="a4cad-249"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-250">Aktiviert die URL-Prozentcodierung für Pfad und Abfragezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a4cad-250">Enables URL percent encoding for path and query string.</span></span>

<span data-ttu-id="a4cad-251">Alternativ können Sie vor dem Aufruf von WinHttp prozentweise codieren.</span><span class="sxs-lookup"><span data-stu-id="a4cad-251">Alternatively, you can percent encode before calling WinHttp.</span></span>

</dt> </dl> </dd>

<dt>

<span data-ttu-id="a4cad-252"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**\_WINHTTP-OPTION \_ LÄUFT VERBINDUNG AB \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-252"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP\_OPTION\_EXPIRE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-253">Diese Option kann nur für ein Anforderungshandle festgelegt werden, das noch aktiv ist (Senden oder Empfangen).</span><span class="sxs-lookup"><span data-stu-id="a4cad-253">This option can only be set on a request handle which is still active (sending or receiving).</span></span> <span data-ttu-id="a4cad-254">Wenn Sie diese Option festlegen, weist WinHttp an, die Verarbeitung von Anforderungen für die Verbindung zu beenden, die dem übergebenen Anforderungshandle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a4cad-254">Setting this option will tell WinHttp to stop serving requests on the connection associated with the request handle passed in.</span></span> <span data-ttu-id="a4cad-255">Die Verbindung wird geschlossen, nachdem das Anforderungshandle, mit dem diese Option aufgerufen wird, abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a4cad-255">The connection will be closed after the request handle this option is called with is completed.</span></span> <span data-ttu-id="a4cad-256">Diese Option verwendet keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a4cad-256">This option does not take any parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-257"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**\_ \_ ERWEITERTER \_ WINHTTP-OPTION-FEHLER**</span><span class="sxs-lookup"><span data-stu-id="a4cad-257"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-258">Ruft einen ganzzahligen Wert ohne Vorzeichen ab, der einen Microsoft Windows Sockets-Fehlercode enthält, der den ERROR WINHTTP-Fehlermeldungen zugeordnet wurde, die \_ \_ \* zuletzt in diesem Threadkontext zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-258">Retrieves an unsigned long integer value that contains a Microsoft Windows Sockets error code that was mapped to the ERROR\_WINHTTP\_\* error messages last returned in this thread context.</span></span> <span data-ttu-id="a4cad-259">Sie können **NULL** als Handlewert übergeben.</span><span class="sxs-lookup"><span data-stu-id="a4cad-259">You can pass **NULL** as the handle value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-260"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP \_ OPTION \_ GLOBAL \_ PROXY \_ CREDS**</span><span class="sxs-lookup"><span data-stu-id="a4cad-260"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-261">Verwendet einen Zeiger auf eine [**WINHTTP \_ CREDS \_ EX-Struktur,**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) wobei der *hInternet-Funktionsparameter* auf **NULL** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a4cad-261">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="a4cad-262">Diese Option erfordert den Registrierungsschlüssel **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="a4cad-262">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="a4cad-263">Wenn dieser Registrierungsschlüssel nicht festgelegt ist, gibt WinHTTP den Fehler **ERROR \_ WINHTTP \_ INVALID \_ OPTION** zurück.</span><span class="sxs-lookup"><span data-stu-id="a4cad-263">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="a4cad-264">Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-264">This registry key is not present by default.</span></span> <span data-ttu-id="a4cad-265">Wenn sie festgelegt ist, sendet WinINet Anmeldeinformationen an WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a4cad-265">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="a4cad-266">Wenn WinHttp eine Authentifizierungsaufforderung erhält und keine Anmeldeinformationen für das aktuelle Handle festgelegt sind, werden die von WinINet bereitgestellten Anmeldeinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4cad-266">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="a4cad-267">Um serveranmeldeinformationen zusätzlich zu Proxyanmeldeinformationen freizugeben, müssen Benutzer **WINHTTP OPTION USE GLOBAL SERVER CREDENTIALS (WINHTTP \_ OPTION USE GLOBAL SERVER \_ \_ \_ \_ CREDENTIALS)** festlegen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-267">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-268"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP \_ OPTION \_ GLOBAL \_ SERVER \_ CREDS**</span><span class="sxs-lookup"><span data-stu-id="a4cad-268"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-269">Verwendet einen Zeiger auf eine [**WINHTTP \_ CREDS \_ EX-Struktur,**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) wobei der *hInternet-Funktionsparameter* auf **NULL** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a4cad-269">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="a4cad-270">Diese Option erfordert den Registrierungsschlüssel **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="a4cad-270">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="a4cad-271">Wenn dieser Registrierungsschlüssel nicht festgelegt ist, gibt WinHTTP den Fehler **ERROR \_ WINHTTP \_ INVALID \_ OPTION** zurück.</span><span class="sxs-lookup"><span data-stu-id="a4cad-271">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="a4cad-272">Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-272">This registry key is not present by default.</span></span> <span data-ttu-id="a4cad-273">Wenn sie festgelegt ist, sendet WinINet Anmeldeinformationen an WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a4cad-273">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="a4cad-274">Wenn WinHttp eine Authentifizierungsaufforderung erhält und keine Anmeldeinformationen für das aktuelle Handle festgelegt sind, werden die von WinINet bereitgestellten Anmeldeinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4cad-274">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="a4cad-275">Um serveranmeldeinformationen zusätzlich zu Proxyanmeldeinformationen freizugeben, müssen Benutzer **WINHTTP OPTION USE GLOBAL SERVER CREDENTIALS (WINHTTP \_ OPTION USE GLOBAL SERVER \_ \_ \_ \_ CREDENTIALS)** festlegen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-275">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-276"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**TYP DES \_ WINHTTP-OPTIONSHANDLE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-276"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-277">Ruft einen ganzzahligen Wert ohne Vorzeichen ab, der den Typ des übergebenen [HINTERNET-Handles](hinternet-handles-in-winhttp.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="a4cad-277">Retrieves an unsigned long integer value that contains the type of the [HINTERNET](hinternet-handles-in-winhttp.md) handle passed in.</span></span> <span data-ttu-id="a4cad-278">Einer der folgenden Werte kann zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="a4cad-278">The return value can be one of the following:</span></span>

| <span data-ttu-id="a4cad-279">Begriff</span><span class="sxs-lookup"><span data-stu-id="a4cad-279">Term</span></span> | <span data-ttu-id="a4cad-280">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4cad-280">Description</span></span> |
|-|-|
| <span data-ttu-id="a4cad-281"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>\_WINHTTP-HANDLETYP \_ \_ CONNECT</span><span class="sxs-lookup"><span data-stu-id="a4cad-281"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP\_HANDLE\_TYPE\_CONNECT</span></span> | <span data-ttu-id="a4cad-282">Das Handle ist ein Verbindungshandle.</span><span class="sxs-lookup"><span data-stu-id="a4cad-282">The handle is a connection handle.</span></span> |
| <span data-ttu-id="a4cad-283"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>\_ \_ WINHTTP-HANDLETYPANFORDERUNG \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-283"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP\_HANDLE\_TYPE\_REQUEST</span></span> | <span data-ttu-id="a4cad-284">Das Handle ist ein Anforderungshandle.</span><span class="sxs-lookup"><span data-stu-id="a4cad-284">The handle is a request handle.</span></span> |
| <span data-ttu-id="a4cad-285"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>\_ \_ WINHTTP-HANDLETYPSITZUNG \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-285"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP\_HANDLE\_TYPE\_SESSION</span></span> | <span data-ttu-id="a4cad-286">Das Handle ist ein Sitzungshandle.</span><span class="sxs-lookup"><span data-stu-id="a4cad-286">The handle is a session handle.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a4cad-287"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP \_ OPTION HTTP PROTOCOL \_ \_ \_ ERFORDERLICH**</span><span class="sxs-lookup"><span data-stu-id="a4cad-287"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-288">Verhindert, dass andere Protokollversionen als die, die von **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL** aktiviert werden, für die Anforderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-288">Prevents protocol versions other than those enabled by **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL** from being used for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-289"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**VERWENDETES \_ \_ WINHTTP-OPTION-HTTP-PROTOKOLL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-289"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-290">Ruft ein DWORD ab, das angibt, welche erweiterte HTTP-Version für eine bestimmte Anforderung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="a4cad-290">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="a4cad-291">Eine Liste der möglichen Werte finden Sie unter **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL**.</span><span class="sxs-lookup"><span data-stu-id="a4cad-291">For a list of possible values, see **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-292"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP \_ OPTION \_ \_ HTTP-VERSION**</span><span class="sxs-lookup"><span data-stu-id="a4cad-292"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-293">Legt eine [**\_ \_ HTTP-VERSIONSINFORMATIONEN-Struktur**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) fest, die die unterstützte HTTP-Version enthält, oder ruft sie ab.</span><span class="sxs-lookup"><span data-stu-id="a4cad-293">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) structure that contains the HTTP version being supported.</span></span> <span data-ttu-id="a4cad-294">Dies ist eine prozessweite Option. Verwenden Sie **NULL** für das Handle.</span><span class="sxs-lookup"><span data-stu-id="a4cad-294">This is a process-wide option; use **NULL** for the handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-295"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP \_ OPTION \_ IGNORE \_ CERT \_ REVOCATION \_ OFFLINE**</span><span class="sxs-lookup"><span data-stu-id="a4cad-295"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-296">Ermöglicht sicheren Verbindungen die Verwendung von Sicherheitszertifikaten, für die die Zertifikatsperrliste nicht heruntergeladen werden konnte.</span><span class="sxs-lookup"><span data-stu-id="a4cad-296">Allows secure connections to use security certificates for which the certificate revocation list could not be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-297"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP \_ OPTION \_ IPV6 \_ FAST \_ FALLBACK**</span><span class="sxs-lookup"><span data-stu-id="a4cad-297"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-298">Aktiviert das schnelle IPv6-Fallback (Zieher-Eyeballs) für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="a4cad-298">Enables IPv6 fast fallback (Happier Eyeballs) for the connection.</span></span> <span data-ttu-id="a4cad-299">Dieses Verhalten ähnelt dem In [RFC 6555](https://tools.ietf.org/html/rfc6555) beschriebenen Verhalten von Happy Eyeballs, um die Verbindungszeiten in Netzwerken zu verbessern, in denen IPv6 unzuverlässig ist.</span><span class="sxs-lookup"><span data-stu-id="a4cad-299">This behavior is similar to the Happy Eyeballs behavior described in [RFC 6555](https://tools.ietf.org/html/rfc6555) for improving connection times on networks where IPv6 is unreliable.</span></span>
- <span data-ttu-id="a4cad-300">Wenn sowohl IPv6- als auch IPv4-Adressen für einen bestimmten Host aufgelöst werden, stellt WinHttp zunächst eine Verbindung mit der ersten aufgelösten IPv6-Adresse mit einem kurzen Timeout (300 ms) her.</span><span class="sxs-lookup"><span data-stu-id="a4cad-300">If both IPv6 and IPv4 addresses are resolved for a given host, WinHttp will begin by connecting to the first resolved IPv6 address with a short (300ms) timeout.</span></span>
- <span data-ttu-id="a4cad-301">Sollte diese Verbindung fehlschlagen, versucht WinHttp, eine Verbindung mit der ersten aufgelösten IPv4-Adresse mit dem Standard-Timeout herzustellen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-301">Should that connection fail, WinHttp will attempt to connect to the first resolved IPv4 address with the standard timeout.</span></span>
- <span data-ttu-id="a4cad-302">Sollte bei der zweiten Verbindung ein Fehler auftäussen, wird von WinHttp die erste aufgelöste IPv6-Adresse mit dem Standard-Timeout erneut verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4cad-302">Should the second connection fail, WinHttp will retry the first resolved IPv6 address with the standard timeout.</span></span>
- <span data-ttu-id="a4cad-303">Sollte die dritte Verbindung fehlschlagen, wird WinHttp auf das Standardverhalten für alle verbleibenden Adressen zurückverwendet und versucht, eine Verbindung mit jeder Adresse mit dem Standard-Timeout herzustellen, bis eine Verbindung hergestellt wird oder keine Adressen mehr bestehen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-303">Should the third connection fail, WinHttp will revert to the default behavior for any remaining addresses, attempting a connection to each one with the standard timeout until a connection is made or no addresses remain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-304"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**\_WINHTTP-OPTION \_ IST PROXY \_ \_ \_ CONNECT-ANTWORT**</span><span class="sxs-lookup"><span data-stu-id="a4cad-304"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-305">Ruft ab, ob eine Proxy Return Connect-Antwort abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a4cad-305">Gets whether or not a Proxy Return Connect Response can be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-306"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**\_WINHTTP-OPTION \_ \_ MAX. CONNS \_ PRO \_ 1 \_ 0 \_ SERVER**</span><span class="sxs-lookup"><span data-stu-id="a4cad-306"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-307">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die maximale Anzahl von Verbindungen enthält, die pro HTTP/1.0-Server zulässig sind, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="a4cad-307">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="a4cad-308">Der Standardwert ist **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="a4cad-308">The default value is **INFINITE**.</span></span>

<span data-ttu-id="a4cad-309">**Windows Vista mit SP1 und Windows Server 2008:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="a4cad-309">**Windows Vista with SP1 and Windows Server 2008:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-310"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**\_WINHTTP-OPTION \_ \_ MAX. CONNS \_ PRO \_ SERVER**</span><span class="sxs-lookup"><span data-stu-id="a4cad-310"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-311">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die maximal zulässige Anzahl von Verbindungen pro Server enthält, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="a4cad-311">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="a4cad-312">Der Standardwert ist **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="a4cad-312">The default value is **INFINITE**.</span></span>

<span data-ttu-id="a4cad-313">Wenn diese Option auf 0 (null) festgelegt ist, legt WinHTTP den Grenzwert für die Anzahl von Verbindungen auf 2 fest.</span><span class="sxs-lookup"><span data-stu-id="a4cad-313">When this option is set to zero, WinHTTP sets the limit on the number of connections to 2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-314"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP-OPTION \_ \_ \_ MAX. AUTOMATISCHE \_ \_ HTTP-UMLEITUNGEN**</span><span class="sxs-lookup"><span data-stu-id="a4cad-314"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-315">Legt die maximale Anzahl von Umleitungen fest, auf die WinHTTP folgt. Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="a4cad-315">Sets the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="a4cad-316">Dieser Grenzwert verhindert, dass nicht autorisierte Websites den WinHTTP-Client nach einer großen Anzahl von Umleitungen anhalten.</span><span class="sxs-lookup"><span data-stu-id="a4cad-316">This limit prevents unauthorized sites from making the WinHTTP client pause following a large number of redirects.</span></span>

<span data-ttu-id="a4cad-317">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="a4cad-317">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-318"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**\_WINHTTP-OPTION \_ \_ MAX. \_ HTTP-STATUS \_ CONTINUE**</span><span class="sxs-lookup"><span data-stu-id="a4cad-318"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-319">Die maximale Anzahl von 100-199 Statuscodeantworten, die ignoriert wurden, bevor der endgültige Statuscode an den WinHTTP-Client zurücksendet.</span><span class="sxs-lookup"><span data-stu-id="a4cad-319">The maximum number of Informational 100-199 status code responses ignored before returning the final status code to the WinHTTP client.</span></span> <span data-ttu-id="a4cad-320">Informationsstatuscodes vom Status 100-199 können vom Server vor dem endgültigen Statuscode gesendet werden und werden in der Spezifikation für HTTP/1.1 beschrieben (weitere Informationen finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span><span class="sxs-lookup"><span data-stu-id="a4cad-320">Informational 100-199 status codes can be sent by the server before the final status code, and are described in the specification for HTTP/1.1 (for more information, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span></span> <span data-ttu-id="a4cad-321">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="a4cad-321">The default is 10.</span></span>

<span data-ttu-id="a4cad-322">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="a4cad-322">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-323"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP \_ OPTION \_ MAX \_ RESPONSE \_ DRAIN \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="a4cad-323"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-324">Eine Grenze für die Menge der Daten, die aus Antworten entleert werden, um eine Verbindung wiederzuverwenden, die in Bytes angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a4cad-324">A bound on the amount of data drained from responses in order to reuse a connection, specified in bytes.</span></span> <span data-ttu-id="a4cad-325">Der Standardwert ist 1 MB.</span><span class="sxs-lookup"><span data-stu-id="a4cad-325">The default is 1MB.</span></span>

<span data-ttu-id="a4cad-326">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="a4cad-326">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-327"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**MAXIMALE GRÖßE DES \_ \_ \_ \_ ANTWORTHEADERS DER \_ WINHTTP-OPTION**</span><span class="sxs-lookup"><span data-stu-id="a4cad-327"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-328">Ein gebundener Satz für die maximale Größe des Headerbereichs der Serverantwort, angegeben in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a4cad-328">A bound set on the maximum size of the header portion of the server response, specified in bytes.</span></span> <span data-ttu-id="a4cad-329">Diese Gebundene schützt den Client vor einem nicht autorisierten Server, der versucht, den Client zu verhindern, indem eine Antwort mit einer unendlichen Menge von Headerdaten gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a4cad-329">This bound protects the client from an unauthorized server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="a4cad-330">Der Standardwert ist 64 KB.</span><span class="sxs-lookup"><span data-stu-id="a4cad-330">The default value is 64KB.</span></span>

<span data-ttu-id="a4cad-331">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="a4cad-331">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-332"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**ÜBERGEORDNETES \_ HANDLE DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-332"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-333">Ruft das übergeordnete Handle für dieses Handle ab.</span><span class="sxs-lookup"><span data-stu-id="a4cad-333">Retrieves the parent handle to this handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-334"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**\_WINHTTP-OPTION \_ \_ PASSPORT-COBRANDINGTEXT \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-334"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-335">Ruft eine Zeichenfolge ab, die den [*cobranding-Text*](glossary.md) enthält, der vom Passport-Anmeldeserver bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a4cad-335">Retrieves a string that contains the [*cobranding*](glossary.md) text provided by the Passport logon server.</span></span> <span data-ttu-id="a4cad-336">Diese Option sollte sofort abgerufen werden, nachdem der Anmeldeserver mit dem Statuscode 401 reagiert hat.</span><span class="sxs-lookup"><span data-stu-id="a4cad-336">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="a4cad-337">Eine Anwendung sollte eine Puffergröße in Bytes übergeben, die groß genug ist, um die zurückgegebene Zeichenfolge zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="a4cad-337">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-338"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**\_WINHTTP-OPTION \_ \_ PASSPORT-COBRANDING-URL \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-338"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-339">Ruft eine Zeichenfolge ab, die eine URL für eine [*Cobrandinggrafik*](glossary.md) enthält, die vom Passport-Anmeldeserver bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a4cad-339">Retrieves a string that contains a URL for a [*cobranding*](glossary.md) graphic provided by the Passport logon server.</span></span> <span data-ttu-id="a4cad-340">Diese Option sollte sofort abgerufen werden, nachdem der Anmeldeserver mit dem Statuscode 401 reagiert hat.</span><span class="sxs-lookup"><span data-stu-id="a4cad-340">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="a4cad-341">Eine Anwendung sollte eine Puffergröße in Bytes übergeben, die groß genug ist, um die zurückgegebene Zeichenfolge zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="a4cad-341">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-342"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**\_WINHTTP-OPTION \_ \_ \_ PASSPORT-RÜCKGABE-URL**</span><span class="sxs-lookup"><span data-stu-id="a4cad-342"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-343">Legt eine schreibgeschützte Option für ein Anforderungshandles fest, das die Passport-Rückgabe-URL abruft.</span><span class="sxs-lookup"><span data-stu-id="a4cad-343">Sets a read-only option on a request handle that retrieves the Passport return URL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-344"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**\_WINHTTP-OPTION \_ \_ \_ PASSPORT-ABMELDE**</span><span class="sxs-lookup"><span data-stu-id="a4cad-344"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-345">Legt die Option für ein Sitzungshand handle zum Abmelden von Passport-Anmeldungen fest.</span><span class="sxs-lookup"><span data-stu-id="a4cad-345">Sets the option on a session handle to sign out of any Passport logins.</span></span> <span data-ttu-id="a4cad-346">Eine Anwendung sollte die Passport-Rückgabe-URL übergeben, die mit **WINHTTP \_ OPTION PASSPORT RETURN URL abgerufen \_ \_ \_ wurde.**</span><span class="sxs-lookup"><span data-stu-id="a4cad-346">An application should pass in the Passport return URL that was retrieved with **WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**.</span></span> <span data-ttu-id="a4cad-347">Alle Cookies im Zusammenhang mit der Rückgabe-URL werden wieder löschen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-347">All cookies related to the return URL are cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-348"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**\_ \_ WINHTTP-OPTIONSKENNWORT**</span><span class="sxs-lookup"><span data-stu-id="a4cad-348"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-349">Legt einen Zeichenfolgenwert fest, der das einem Anforderungshand handle zugeordnete Kennwort enthält, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="a4cad-349">Sets or retrieves a string value that contains the password associated with a request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-350"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**\_WINHTTP-OPTIONSPROXY \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-350"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-351">Legt eine [**WINHTTP PROXY \_ \_ INFO-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) fest, die die Proxydaten auf einem vorhandenen Sitzungshand handle oder Anforderungshand handle enthält, oder ruft sie ab.</span><span class="sxs-lookup"><span data-stu-id="a4cad-351">Sets or retrieves an [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure that contains the proxy data on an existing session handle or request handle.</span></span> <span data-ttu-id="a4cad-352">Beim Abrufen von Proxydaten muss eine Anwendung die in dieser Struktur enthaltenen **lpszProxy-** und **lpszProxyBypass-Zeichenfolgen** (wenn sie nicht NULL **sind)** mithilfe der [**GlobalFree-Funktion**](/windows/desktop/api/winbase/nf-winbase-globalfree) frei geben.</span><span class="sxs-lookup"><span data-stu-id="a4cad-352">When retrieving proxy data, an application must free the **lpszProxy** and **lpszProxyBypass** strings contained in this structure (if they are non-**NULL**) using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="a4cad-353">Eine Anwendung kann die globalen Proxydaten (den Standardproxy) abfragen, indem sie ein **NULL-Handle** übergibt.</span><span class="sxs-lookup"><span data-stu-id="a4cad-353">An application can query for the global proxy data (the default proxy) by passing a **NULL** handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-354"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**\_PROXYKENNWORT \_ FÜR WINHTTP-OPTION \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-354"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-355">Legt einen Zeichenfolgenwert fest, der das Kennwort für den Zugriff auf den Proxy enthält, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="a4cad-355">Sets or retrieves a string value that contains the password used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-356"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**VERWENDETER \_ \_ WINHTTP-OPTIONSPROXY-SPN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-356"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WINHTTP\_OPTION\_PROXY\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-357">Ruft den Proxyserverprinzipalnamen ab, den WinHTTP während der Authentifizierung an SSPI übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="a4cad-357">Gets the proxy Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="a4cad-358">Dieser Zeichenfolgenwert wird verwendet, um nach einem [**Authentifizierungsfehler an SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="a4cad-358">This string value is usefor passing to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-359"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**\_PROXYBENUTZERNAME DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-359"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-360">Legt einen Zeichenfolgenwert fest, der den Benutzernamen enthält, der für den Zugriff auf den Proxy verwendet wird, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="a4cad-360">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-361"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**\_WINHTTP-OPTION \_ READ BUFFER \_ \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="a4cad-361"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-362">Diese Option ist veraltet. es hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-362">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-363"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP-OPTION \_ \_ "PROXY \_ \_ CONNECT-ANTWORT \_ EMPFANGEN"**</span><span class="sxs-lookup"><span data-stu-id="a4cad-363"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-364">Legt fest, ob die Proxyantwortentität abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a4cad-364">Sets whether or not the proxy response entity can be retrieved.</span></span> <span data-ttu-id="a4cad-365">Diese Option ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a4cad-365">This option is disabled by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-366"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP-OPTION \_ \_ \_ \_ EMPFANGSANTWORT-TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="a4cad-366"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-367">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Timeoutwert in Millisekunden enthält, um auf den Empfang aller Antwortheader für eine Anforderung zu warten, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="a4cad-367">Sets or retrieves an unsigned long integer value that contains the timeout value, in milliseconds, to wait to receive all response headers to a request.</span></span> <span data-ttu-id="a4cad-368">Wenn WinHTTP nicht alle Header innerhalb dieses Timeoutzeitraums empfangen kann, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-368">If WinHTTP fails to receive all the headers within this timeout period, the request is canceled.</span></span> <span data-ttu-id="a4cad-369">Der Standardwert für das Timeout beträgt 90 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-369">The default timeout value is 90 seconds.</span></span>

<span data-ttu-id="a4cad-370">Dieses Timeout wird nur überprüft, wenn Daten vom Socket empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-370">This timeout is checked only when data is received from the socket.</span></span> <span data-ttu-id="a4cad-371">Wenn das Timeout abläuft, wird die Clientanwendung daher erst benachrichtigt, wenn weitere Daten vom Server eintreffen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-371">As a result, when the timeout expires the client application is not notified until more data arrives from the server.</span></span> <span data-ttu-id="a4cad-372">Wenn keine Daten vom Server eintreffen, kann die Verzögerung zwischen dem Ablauf des Timeouts und der Benachrichtigung der Clientanwendung so groß sein wie der Timeoutwert, der mit dem *dwReceiveTimeout-Parameter* der [**WinHttpSetTimeouts-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="a4cad-372">If no data arrives from the server, the delay between the timeout expiration and notification of the client application could be as large as the timeout value set using the *dwReceiveTimeout* parameter of the [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-373"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**\_EMPFANGSZEITÜBERSCHREITUNG DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-373"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-374">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, um eine Teilantwort auf eine Anforderung zu empfangen oder einige Daten zu lesen, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="a4cad-374">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a partial response to a request or read some data.</span></span> <span data-ttu-id="a4cad-375">Wenn die Antwort länger als dieser Time out-Wert dauert, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-375">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="a4cad-376">Der Standard-Timeoutwert beträgt 30 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-376">The default timeout value is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-377"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**UMLEITUNGSRICHTLINIE \_ FÜR WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-377"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP\_OPTION\_REDIRECT\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-378">Legt das Verhalten von WinHTTP in Bezug auf die Behandlung eines 30-fachen HTTP-Umleitungsstatuscodes fest.</span><span class="sxs-lookup"><span data-stu-id="a4cad-378">Sets the behavior of WinHTTP regarding the handling of a 30x HTTP redirect status code.</span></span> <span data-ttu-id="a4cad-379">Diese Option kann für ein Sitzungs- oder Anforderungshand handle auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a4cad-379">This option can be set on a session or request handle to one of the following values:</span></span>

| <span data-ttu-id="a4cad-380">Begriff</span><span class="sxs-lookup"><span data-stu-id="a4cad-380">Term</span></span> | <span data-ttu-id="a4cad-381">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4cad-381">Description</span></span> |
|-|-|
| <span data-ttu-id="a4cad-382"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>RICHTLINIE FÜR DIE UMLEITUNG \_ DER WINHTTP-OPTION \_ \_ \_ IMMER</span><span class="sxs-lookup"><span data-stu-id="a4cad-382"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_ALWAYS</span></span> | <span data-ttu-id="a4cad-383">Alle Umleitungen werden automatisch befolgt.</span><span class="sxs-lookup"><span data-stu-id="a4cad-383">All redirects are followed automatically.</span></span> |
| <span data-ttu-id="a4cad-384"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>UMLEITUNGSRICHTLINIE \_ FÜR \_ WINHTTP-OPTION: \_ HTTPS ZU HTTP NICHT \_ \_ \_ \_ ZU</span><span class="sxs-lookup"><span data-stu-id="a4cad-384"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_DISALLOW\_HTTPS\_TO\_HTTP</span></span> | <span data-ttu-id="a4cad-385">Alle Umleitungen werden befolgt, mit Ausnahme der Umleitungen, die von einer sicheren URL (https) zu einer unsicheren URL (HTTP) stammen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-385">All redirects are followed, except those that originate from a secure (https) URL to an unsecure (http) URL.</span></span> <span data-ttu-id="a4cad-386">Dies ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="a4cad-386">This is the default setting.</span></span> |
| <span data-ttu-id="a4cad-387"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>UMLEITUNGSRICHTLINIE \_ FÜR WINHTTP-OPTION \_ \_ \_ NIE</span><span class="sxs-lookup"><span data-stu-id="a4cad-387"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_NEVER</span></span> | <span data-ttu-id="a4cad-388">Umleitungen werden nie befolgt.</span><span class="sxs-lookup"><span data-stu-id="a4cad-388">Redirects are never followed.</span></span> <span data-ttu-id="a4cad-389">Der 30-fache Status wird an die Anwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a4cad-389">The 30x status is returned to the application.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-390"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**\_WINHTTP-OPTION \_ BENUTZER IN URL \_ \_ \_ ABLEHNENPWD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-390"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-391">Lehnt URLs ab, die einen Benutzernamen und ein Kennwort enthalten.</span><span class="sxs-lookup"><span data-stu-id="a4cad-391">Rejects URLs that contain a username and password.</span></span> <span data-ttu-id="a4cad-392">Diese Option lehnt auch URLs ab, die *die Semantik username:password* enthalten, auch wenn kein Benutzername oder Kennwort angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a4cad-392">This option also rejects URLs that contain *username:password* semantics, even if no username or password is specified.</span></span> <span data-ttu-id="a4cad-393">Beispielsweise würde " u:p@hostname ", " :@hostname ", " u:@hostname ", " " und " :p@hostname " alle als ungültig gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-393">For example, "u:p@hostname", ":@hostname", "u:@hostname", and ":p@hostname" would all be flagged as invalid.</span></span> <span data-ttu-id="a4cad-394">Wenn eine ungültige URL an die Funktion übergeben wird, wird [ERROR \_ WINHTTP \_ INVALID URL \_ zurückgegeben.](error-messages.md)</span><span class="sxs-lookup"><span data-stu-id="a4cad-394">If an invalid URL is passed to the function, it returns [ERROR\_WINHTTP\_INVALID\_URL](error-messages.md).</span></span> <span data-ttu-id="a4cad-395">Standardmäßig ist diese Option deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a4cad-395">This option is turned off by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-396"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**\_WINHTTP-OPTION \_ – \_ ANFORDERUNGSPRIORITÄT**</span><span class="sxs-lookup"><span data-stu-id="a4cad-396"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-397">Diese Option ist veraltet. es hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-397">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-398"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**\_ \_ WINHTTP-OPTIONSANFORDERUNGSSTATISTIKEN \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-398"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP\_OPTION\_REQUEST\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-399">Retreives-Statistiken für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a4cad-399">Retreives statistics for the request.</span></span>  <span data-ttu-id="a4cad-400">Eine Liste der verfügbaren Statistiken finden Sie unter [**WINHTTP \_ REQUEST \_ STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span><span class="sxs-lookup"><span data-stu-id="a4cad-400">For a list of the available statistics, see [**WINHTTP\_REQUEST\_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-401"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**ANFORDERUNGSZEITEN DER \_ WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-401"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP\_OPTION\_REQUEST\_TIMES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-402">Retreives-Zeitsteuerungsinformationen für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a4cad-402">Retreives timing information for the request.</span></span> <span data-ttu-id="a4cad-403">Eine Liste der verfügbaren Zeitangaben finden Sie unter [**WINHTTP \_ REQUEST \_ TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span><span class="sxs-lookup"><span data-stu-id="a4cad-403">For a list of the available timings, see [**WINHTTP\_REQUEST\_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-404"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**TIMEOUT FÜR AUFLÖSUNG DER \_ WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-404"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP\_OPTION\_RESOLVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-405">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, um einen Hostnamen aufzulösen, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="a4cad-405">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to resolve a host name.</span></span> <span data-ttu-id="a4cad-406">Der Standardtimeoutwert ist **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="a4cad-406">The default timeout value is **INFINITE**.</span></span> <span data-ttu-id="a4cad-407">Wenn ein nicht standardmäßiger Wert angegeben wird, fällt ein Threaderstellungsaufwand pro Namensauflösung an.</span><span class="sxs-lookup"><span data-stu-id="a4cad-407">If a non-default value is specified, there is an overhead of one thread-creation per name resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-408"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**SICHERE \_ WINHTTP-OPTION \_ \_ – PROTOKOLLE**</span><span class="sxs-lookup"><span data-stu-id="a4cad-408"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP\_OPTION\_SECURE\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-409">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, welche sicheren Protokolle akzeptabel sind.</span><span class="sxs-lookup"><span data-stu-id="a4cad-409">Sets an unsigned long integer value that specifies which secure protocols are acceptable.</span></span> <span data-ttu-id="a4cad-410">Standardmäßig sind nur SSL3 und TLS1 in Windows 7 und Windows 8 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a4cad-410">By default only SSL3 and TLS1 are enabled in Windows 7 and Windows 8.</span></span> <span data-ttu-id="a4cad-411">Standardmäßig sind nur SSL3, TLS1.0, TLS1.1 und TLS1.2 in Windows 8.1 und Windows 10 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a4cad-411">By default only SSL3, TLS1.0, TLS1.1, and TLS1.2 are enabled in Windows 8.1 and Windows 10.</span></span> <span data-ttu-id="a4cad-412">Der Wert kann eine Kombination aus einem oder mehreren der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="a4cad-412">The value can be a combination of one or more of the following values.</span></span>

| <span data-ttu-id="a4cad-413">Begriff</span><span class="sxs-lookup"><span data-stu-id="a4cad-413">Term</span></span> | <span data-ttu-id="a4cad-414">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4cad-414">Description</span></span> |
|-|-|
| <span data-ttu-id="a4cad-415"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>\_WINHTTP-FLAG \_ SECURE PROTOCOL \_ \_ ALL</span><span class="sxs-lookup"><span data-stu-id="a4cad-415"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_ALL</span></span> | <span data-ttu-id="a4cad-416">Die Protokolle Secure Sockets Layer (SSL) 2.0, SSL 3.0 und Transport Layer Security (TLS) 1.0 können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-416">The Secure Sockets Layer (SSL) 2.0, SSL 3.0, and Transport Layer Security (TLS) 1.0 protocols can be used.</span></span> |
| <span data-ttu-id="a4cad-417"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>\_WINHTTP-FLAG \_ SECURE PROTOCOL \_ \_ SSL2</span><span class="sxs-lookup"><span data-stu-id="a4cad-417"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL2</span></span> | <span data-ttu-id="a4cad-418">Das SSL 2.0-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-418">The SSL 2.0 protocol can be used.</span></span> |
| <span data-ttu-id="a4cad-419"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ SSL3</span><span class="sxs-lookup"><span data-stu-id="a4cad-419"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL3</span></span> | <span data-ttu-id="a4cad-420">Das SSL 3.0-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-420">The SSL 3.0 protocol can be used.</span></span> |
| <span data-ttu-id="a4cad-421"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ TLS1</span><span class="sxs-lookup"><span data-stu-id="a4cad-421"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1</span></span> | <span data-ttu-id="a4cad-422">Das TLS 1.0-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-422">The TLS 1.0 protocol can be used.</span></span> |
| <span data-ttu-id="a4cad-423"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>\_WINHTTP-FLAG \_ SECURE PROTOCOL \_ \_ TLS1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a4cad-423"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_1</span></span> | <span data-ttu-id="a4cad-424">Das TLS 1.1-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-424">The TLS 1.1 protocol can be used.</span></span> |
| <span data-ttu-id="a4cad-425"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>\_WINHTTP-FLAG \_ SECURE PROTOCOL \_ \_ TLS1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="a4cad-425"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_2</span></span> | <span data-ttu-id="a4cad-426">Das TLS 1.2-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-426">The TLS 1.2 protocol can be used.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a4cad-427"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP \_ OPTION \_ SECURITY \_ CERTIFICATE \_ STRUCT**</span><span class="sxs-lookup"><span data-stu-id="a4cad-427"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-428">Ruft das Zertifikat für einen SSL/TLS-Server in die [**WINHTTP \_ CERTIFICATE \_ INFO-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) ab.</span><span class="sxs-lookup"><span data-stu-id="a4cad-428">Retrieves the certificate for a SSL/TLS server into the [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="a4cad-429">Die Anwendung muss die Member **lpszSubjectInfo** und **lpszIssuerInfo** mit [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)freigeben.</span><span class="sxs-lookup"><span data-stu-id="a4cad-429">The application must free the **lpszSubjectInfo** and **lpszIssuerInfo** members with [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-430"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**SICHERHEITSFLAGS DER WINHTTP-OPTION \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-430"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-431">Legt einen ganzzahligen Wert ohne Vorzeichen fest oder ruft diesen ab, der die Sicherheitsflags für ein Handle enthält.</span><span class="sxs-lookup"><span data-stu-id="a4cad-431">Sets or retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="a4cad-432">Dies kann eine Kombination dieser Werte sein:</span><span class="sxs-lookup"><span data-stu-id="a4cad-432">It can be a combination of these values:</span></span>

| <span data-ttu-id="a4cad-433">Begriff</span><span class="sxs-lookup"><span data-stu-id="a4cad-433">Term</span></span> | <span data-ttu-id="a4cad-434">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4cad-434">Description</span></span> |
|-|-|
| <span data-ttu-id="a4cad-435"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>\_SICHERHEITSFLAG \_ \_ CERT \_ CN \_ UNGÜLTIG IGNORIEREN</span><span class="sxs-lookup"><span data-stu-id="a4cad-435"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span> |<span data-ttu-id="a4cad-436">Lässt einen ungültigen allgemeinen Namen in einem Zertifikat zu. Das heißt, der von der Anwendung angegebene Servername stimmt nicht mit dem allgemeinen Namen im Zertifikat überein.</span><span class="sxs-lookup"><span data-stu-id="a4cad-436">Allows an invalid common name in a certificate; that is, the server name specified by the application does not match the common name in the certificate.</span></span> <span data-ttu-id="a4cad-437">Wenn dieses Flag festgelegt ist, erhält die Anwendung keinen **WINHTTP \_ CALLBACK \_ STATUS FLAG \_ \_ CERT \_ CN \_ INVALID-Rückruf.**</span><span class="sxs-lookup"><span data-stu-id="a4cad-437">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_CN\_INVALID** callback.</span></span> |
| <span data-ttu-id="a4cad-438"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>\_SICHERHEITSFLAG \_ IGNORE \_ CERT DATE \_ \_ INVALID</span><span class="sxs-lookup"><span data-stu-id="a4cad-438"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span> |<span data-ttu-id="a4cad-439">Lässt ein ungültiges Zertifikatdatum zu, d. h. ein abgelaufenes oder noch nicht gültiges Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="a4cad-439">Allows an invalid certificate date, that is, an expired or not-yet-effective certificate.</span></span> <span data-ttu-id="a4cad-440">Wenn dieses Flag festgelegt ist, erhält die Anwendung keinen **WINHTTP \_ CALLBACK \_ STATUS FLAG \_ \_ CERT DATE \_ \_ INVALID-Rückruf.**</span><span class="sxs-lookup"><span data-stu-id="a4cad-440">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_DATE\_INVALID** callback.</span></span> |
| <span data-ttu-id="a4cad-441"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>\_SICHERHEITSFLAG \_ UNBEKANNTE \_ \_ ZERTIFIZIERUNGSSTELLE IGNORIEREN</span><span class="sxs-lookup"><span data-stu-id="a4cad-441"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span> | <span data-ttu-id="a4cad-442">Lässt eine ungültige Zertifizierungsstelle zu.</span><span class="sxs-lookup"><span data-stu-id="a4cad-442">Allows an invalid certificate authority.</span></span> <span data-ttu-id="a4cad-443">Wenn dieses Flag festgelegt ist, erhält die Anwendung keinen **WINHTTP \_ CALLBACK \_ STATUS FLAG \_ INVALID \_ \_ CA-Rückruf.**</span><span class="sxs-lookup"><span data-stu-id="a4cad-443">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_INVALID\_CA** callback.</span></span> |
| <span data-ttu-id="a4cad-444"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>\_SICHERHEITSFLAG: \_ FALSCHE VERWENDUNG DES \_ ZERTIFIKATS IGNORIEREN \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-444"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_CERT\_WRONG\_USAGE</span></span> | <span data-ttu-id="a4cad-445">Ermöglicht die Einrichtung der Identität eines Servers mit einem Nicht-Serverzertifikat (z. B. einem Clientzertifikat).</span><span class="sxs-lookup"><span data-stu-id="a4cad-445">Allows the identity of a server to be established with a non-server certificate (for example, a client certificate).</span></span> |
| <span data-ttu-id="a4cad-446"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>\_SICHERHEITSFLAG: \_ SCHWACHE SIGNATUR IGNORIEREN \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-446"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span> | <span data-ttu-id="a4cad-447">Lässt zu, dass eine schwache Signatur ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="a4cad-447">Allows a weak signature to be ignored.</span></span><br/><span data-ttu-id="a4cad-448">Dieses Flag ist im Rollupupdate für jedes Betriebssystem ab Windows 7 und Windows Server 2008 R2 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a4cad-448">This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.</span></span> |
| <span data-ttu-id="a4cad-449"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>\_SICHERHEITSFLAG \_ "SICHER"</span><span class="sxs-lookup"><span data-stu-id="a4cad-449"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span> | <span data-ttu-id="a4cad-450">Verwendet sichere Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-450">Uses secure transfers.</span></span> <span data-ttu-id="a4cad-451">Dies wird nur in einem Aufruf von [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a4cad-451">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="a4cad-452"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>\_SICHERHEITSFLAGSTÄRKE \_ \_ MITTEL</span><span class="sxs-lookup"><span data-stu-id="a4cad-452"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span> | <span data-ttu-id="a4cad-453">Verwendet mittlere (56-Bit)-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="a4cad-453">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="a4cad-454">Dies wird nur in einem Aufruf von [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a4cad-454">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="a4cad-455"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>\_SICHERHEITSFLAGSTÄRKE \_ \_ STARK</span><span class="sxs-lookup"><span data-stu-id="a4cad-455"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span> | <span data-ttu-id="a4cad-456">Verwendet eine starke (128-Bit)-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="a4cad-456">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="a4cad-457">Dies wird nur in einem Aufruf von [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a4cad-457">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="a4cad-458"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>\_SICHERHEITSFLAGSTÄRKE \_ \_ SCHWACH</span><span class="sxs-lookup"><span data-stu-id="a4cad-458"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span> | <span data-ttu-id="a4cad-459">Verwendet schwache (40-Bit)-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="a4cad-459">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="a4cad-460">Dies wird nur in einem Aufruf von [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a4cad-460">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a4cad-461"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**SICHERHEITSINFORMATIONEN ZUR WINHTTP-OPTION \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-461"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP\_OPTION\_SECURITY\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-462">Retreives die SChannel-Verbindung und Verschlüsselungsinformationen für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a4cad-462">Retreives the SChannel connection and cipher information for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-463"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP \_ OPTION \_ SECURITY \_ KEY \_ BITNESS**</span><span class="sxs-lookup"><span data-stu-id="a4cad-463"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-464">Ruft einen ganzzahligen Wert ohne Vorzeichen ab, der die Verschlüsselungsstärke des Verschlüsselungsschlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="a4cad-464">Retrieves an unsigned long integer value that contains the cipher strength of the encryption key.</span></span> <span data-ttu-id="a4cad-465">Eine größere Zahl weist auf eine stärkere Verschlüsselung der Verschlüsselungsstärke hin.</span><span class="sxs-lookup"><span data-stu-id="a4cad-465">A larger number indicates stronger cipher strength encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-466"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP \_ OPTION \_ SEND \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="a4cad-466"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-467">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, um eine Anforderung zu senden oder Einige Daten zu schreiben, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="a4cad-467">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to send a request or write some data.</span></span> <span data-ttu-id="a4cad-468">Wenn das Senden der Anforderung länger als das Timeout dauert, wird der Sendevorgang abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-468">If sending the request takes longer than the timeout, the send operation is canceled.</span></span> <span data-ttu-id="a4cad-469">Der Standardzeitraum bis zum Timeout beträgt 30 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-469">The default timeout is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-470"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP \_ OPTION \_ SERVER \_ CBT**</span><span class="sxs-lookup"><span data-stu-id="a4cad-470"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP\_OPTION\_SERVER\_CBT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-471">Ruft einen Zeiger auf die [**SecPkgContext-Bindungsstruktur \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) ab, die ein Channel Binding Token (CBT) angibt.</span><span class="sxs-lookup"><span data-stu-id="a4cad-471">Gets a pointer to [**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) structure that specifies a Channel Binding Token (CBT).</span></span>

<span data-ttu-id="a4cad-472">Ein Kanalbindungstoken ist eine Eigenschaft eines sicheren Transportkanals und wird verwendet, um einen Authentifizierungskanal an den sicheren Transportkanal zu binden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-472">A Channel Binding Token is a property of a secure transport channel and is used to bind an authentication channel to the secure transport channel.</span></span> <span data-ttu-id="a4cad-473">Dieses Token kann von dieser Option erst abgerufen werden, nachdem eine SSL-Verbindung hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a4cad-473">This token can only be obtained by this option after an SSL connection has been established.</span></span>

> [!Note]
> <span data-ttu-id="a4cad-474">Wenn Sie diese Option und einen **NULL-Wert** für *lpBuffer* an [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) übergeben, werden ERROR \_ INSUFFICIENT BUFFER und die erforderliche \_ Bytegröße für den Puffer im *lpdwBufferLength-Parameter* zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a4cad-474">Passing this option and a **null** value for *lpBuffer* to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) will return ERROR\_INSUFFICIENT\_BUFFER and the required byte size for the buffer in the *lpdwBufferLength* parameter.</span></span> <span data-ttu-id="a4cad-475">Dieser zurückgegebene Puffergrößenwert kann in einem nachfolgenden Aufruf zur Abfrage des Kanalbindungstokens übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-475">This returned buffer size value can be passed in a subsequent call to query for the Channel Binding Token.</span></span> <span data-ttu-id="a4cad-476">Diese Schritte sind bei der Behandlung von WINHTTP \_ CALLBACK \_ STATUS REQUEST \_ erforderlich, wenn Sie Anforderungsheader basierend auf dem Kanalbindungstoken ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="a4cad-476">These steps are necessary when handling WINHTTP\_CALLBACK\_STATUS\_REQUEST if you want to modify request headers based on the Channel Binding Token.</span></span> <span data-ttu-id="a4cad-477">Beachten Sie, dass Windows XP und Vista das Ändern von Anforderungsheadern während dieses Rückrufs nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-477">Note that Windows XP and Vista do not support modifying request headers during this callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-478"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CHAIN \_ CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="a4cad-478"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-479">Ruft den Kontext der Serverzertifizierungskette ab.</span><span class="sxs-lookup"><span data-stu-id="a4cad-479">Retrieves the server certification chain context.</span></span> <span data-ttu-id="a4cad-480">**WINHTTP \_ OPTION \_ SERVER \_ CERT CHAIN \_ \_ CONTEXT** kann übergeben werden, um einen duplizierten Zeiger auf den **CERT CHAIN \_ \_ CONTEXT** für eine Serverzertifikatkette zu erhalten, die während einer ausgehandelten SSL-Verbindung empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="a4cad-480">**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT** can be passed to obtain a duplicated pointer to the **CERT\_CHAIN\_CONTEXT** for a server certificate chain received during a negotiated SSL connection.</span></span> <span data-ttu-id="a4cad-481">Der Client muss [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) für den zurückgegebenen PCCERT \_ CONTEXT-Zeiger aufrufen, der in den Puffer gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="a4cad-481">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-482"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="a4cad-482"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-483">Ruft den Serverzertifizierungskontext ab.</span><span class="sxs-lookup"><span data-stu-id="a4cad-483">Retrieves the server certification context.</span></span> <span data-ttu-id="a4cad-484">**WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CONTEXT** kann übergeben werden, um einen duplizierten Zeiger auf den [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) für ein Serverzertifikat abzurufen, das während einer ausgehandelten SSL-Verbindung empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="a4cad-484">**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT** can be passed to obtain a duplicated pointer to the [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) for a server certificate received during a negotiated SSL connection.</span></span> <span data-ttu-id="a4cad-485">Der Client muss [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) für den zurückgegebenen PCCERT \_ CONTEXT-Zeiger aufrufen, der in den Puffer gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="a4cad-485">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-486"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**VERWENDETER \_ \_ WINHTTP-OPTIONSERVER-SPN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-486"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WINHTTP\_OPTION\_SERVER\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-487">Ruft den Serverprinzipalnamen ab, den WinHTTP während der Authentifizierung für SSPI bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="a4cad-487">Gets the server Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="a4cad-488">Dieser Zeichenfolgenwert kann nach einem Authentifizierungsfehler an [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-488">This string value can be passed to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-489"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP \_ OPTION \_ SPN**</span><span class="sxs-lookup"><span data-stu-id="a4cad-489"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP\_OPTION\_SPN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-490">Schließt die Serverportnummer ein oder entfernt sie, wenn der SPN (Dienstprinzipalname) für die Kerberos- oder Negotiate Kerberos-Authentifizierung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a4cad-490">Includes or removes the server port number when the SPN (service principal name) is built for Kerberos or Negotiate Kerberos authentication.</span></span> <span data-ttu-id="a4cad-491">Dieses Flag ist einer der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="a4cad-491">This flag is one of the following values:</span></span>

| <span data-ttu-id="a4cad-492">Begriff</span><span class="sxs-lookup"><span data-stu-id="a4cad-492">Term</span></span> | <span data-ttu-id="a4cad-493">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4cad-493">Description</span></span> |
|-|-|
| <span data-ttu-id="a4cad-494"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ \_ \_ SPN-SERVERPORT DEAKTIVIEREN \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-494"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP\_DISABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="a4cad-495">Entfernt die Serverportnummer.</span><span class="sxs-lookup"><span data-stu-id="a4cad-495">Removes the server port number.</span></span> |
| <span data-ttu-id="a4cad-496"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP \_ \_ \_ SPN-SERVERPORT AKTIVIEREN \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-496"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP\_ENABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="a4cad-497">Enthält die Serverportnummer.</span><span class="sxs-lookup"><span data-stu-id="a4cad-497">Includes the server port number.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a4cad-498"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP \_ OPTION \_ TCP \_ FAST \_ OPEN**</span><span class="sxs-lookup"><span data-stu-id="a4cad-498"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP\_OPTION\_TCP\_FAST\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-499">Aktiviert TCP Fast Open für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="a4cad-499">Enables TCP Fast Open for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-500"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP \_ OPTION \_ TLS \_ FALSE \_ START**</span><span class="sxs-lookup"><span data-stu-id="a4cad-500"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP\_OPTION\_TLS\_FALSE\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-501">Aktiviert TLS False Start für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="a4cad-501">Enables TLS False Start for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-502"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP-OPTION \_ \_ \_ ENTLADEBENACHRICHTIGUNGSEREIGNIS \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-502"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-503">Nimmt ein Ereignis an, das festgelegt wird, wenn der letzte Rückruf für eine bestimmte Sitzung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a4cad-503">Takes an event that will be set when the last callback has completed for a particular session.</span></span> <span data-ttu-id="a4cad-504">Dieses Flag muss für ein Sitzungshand handle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-504">This flag must be must be used on a session handle.</span></span> <span data-ttu-id="a4cad-505">Das Ereignis kann erst geschlossen werden, nachdem es von WinHTTP festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="a4cad-505">The event cannot be closed until after it has been set by WinHTTP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-506"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP \_ OPTION \_ UNSAFE \_ HEADER \_ PARSING**</span><span class="sxs-lookup"><span data-stu-id="a4cad-506"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-507">Diese Option ist für die interne Verwendung reserviert und sollte nicht aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-507">This option is reserved for internal use and should not be called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-508"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**UPGRADE DER \_ \_ WINHTTP-OPTION \_ AUF \_ \_ WEBSOCKET**</span><span class="sxs-lookup"><span data-stu-id="a4cad-508"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-509">Weist den Stapel an, einen WebSocket-Handshakeprozess mit [**WinHttpSendRequest zu starten.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="a4cad-509">Instructs the stack to start a WebSocket handshake process with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="a4cad-510">Für diese Option werden keine Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4cad-510">This option takes no parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-511"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**URL DER \_ \_ WINHTTP-OPTION**</span><span class="sxs-lookup"><span data-stu-id="a4cad-511"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-512">Ruft einen Zeichenfolgenwert ab, der die vollständige URL einer heruntergeladenen Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="a4cad-512">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="a4cad-513">Wenn die ursprüngliche URL zusätzliche Daten enthält, z. B. Suchzeichenfolgen oder Anker, oder wenn der Aufruf umgeleitet wurde, unterscheidet sich die zurückgegebene URL von der ursprünglichen URL.</span><span class="sxs-lookup"><span data-stu-id="a4cad-513">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="a4cad-514">Die Anwendung sollte einen Puffer in Bytegröße übergeben, der groß genug ist, um die zurückgegebene URL in wide char zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="a4cad-514">The application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-515"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**\_WINHTTP-OPTION \_ GLOBALE \_ SERVERANMELDEINFORMATIONEN \_ \_ VERWENDEN**</span><span class="sxs-lookup"><span data-stu-id="a4cad-515"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-516">Verwendet eine **BOOL** und kann nur für ein Sitzungshandl festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-516">Takes a **BOOL** and can be set only a session handle.</span></span> <span data-ttu-id="a4cad-517">Sie wird nur an Handles, die aus dem Sitzungshandles erstellt wurden, nach dem Festlegen der Option weiter.</span><span class="sxs-lookup"><span data-stu-id="a4cad-517">It will only propagate down to handles created from the session handle after the option has been set.</span></span> <span data-ttu-id="a4cad-518">True **gibt an,** dass diese Option als letztes Mittel die Verwendung globaler Serveranmeldeinformationen verursacht, die von WinInet übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-518">If **TRUE**, this option causes as a last resort the use of global server credentials that were pushed down from WinInet.</span></span> <span data-ttu-id="a4cad-519">Der Standardwert für diese Option ist **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="a4cad-519">The default for this option is **FALSE**.</span></span> <span data-ttu-id="a4cad-520">Diese Option erfordert den Registrierungsschlüssel **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="a4cad-520">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="a4cad-521">Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-521">This registry key is not present by default.</span></span> <span data-ttu-id="a4cad-522">Wenn sie festgelegt ist, sendet WinINet Anmeldeinformationen an WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a4cad-522">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="a4cad-523">Wenn WinHttp eine Authentifizierungsforderung erhält und keine Anmeldeinformationen für das aktuelle Handle festgelegt sind, werden die von WinINet bereitgestellten Anmeldeinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4cad-523">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-524"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**\_BENUTZER-AGENT DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-524"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-525">Legt die Benutzer-Agent-Zeichenfolge für handles fest, die von [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) bereitgestellt und in [**nachfolgenden WinHttpSendRequest-Funktionen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) verwendet wird, oder ruft sie ab, solange sie nicht durch einen Header überschrieben wird, der von [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) oder **WinHttpSendRequest hinzugefügt** wurde. [](glossary.md)</span><span class="sxs-lookup"><span data-stu-id="a4cad-525">Sets or retrieves the [*user agent*](glossary.md) string on handles supplied by [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) and used in subsequent [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) functions, as long as it is not overridden by a header added by [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) or **WinHttpSendRequest**.</span></span> <span data-ttu-id="a4cad-526">Beim Abrufen eines Benutzer-Agents sollte die Anwendung einen Puffer in Bytegröße übergeben, der groß genug ist, um die zurückgegebene URL in wide char zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a4cad-526">When retrieving a user agent, the application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span> <span data-ttu-id="a4cad-527">Beim Festlegen des Benutzer-Agents ist die Puffergröße die Länge der Zeichenfolge in Zeichen plus **das NULL-Abschlusszeichen.**</span><span class="sxs-lookup"><span data-stu-id="a4cad-527">When setting the user agent, the buffer size is the length of the string, in characters, plus the **NULL** terminator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-528"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**\_ \_ WINHTTP-OPTIONSBENUTZERNAME**</span><span class="sxs-lookup"><span data-stu-id="a4cad-528"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-529">Legt eine Zeichenfolge fest, die den Benutzernamen enthält, oder ruft sie ab.</span><span class="sxs-lookup"><span data-stu-id="a4cad-529">Sets or retrieves a string that contains the user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-530"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**\_WINHTTP-OPTION: \_ \_ TIMEOUT BEIM \_ SCHLIEßEN DES WEBSOCKET \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-530"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-531">Legt die Zeit in Millisekunden fest, die [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) warten soll, bis der schließende Handshake abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a4cad-531">Sets the time, in milliseconds, that [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) should wait to complete the close handshake.</span></span> <span data-ttu-id="a4cad-532">Die Standardeinstellung beträgt 10 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-532">The default is 10 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-533"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP-OPTION \_ \_ WEB SOCKET \_ \_ KEEPALIVE \_ INTERVAL**</span><span class="sxs-lookup"><span data-stu-id="a4cad-533"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-534">Legt das Intervall in Millisekunden fest, um ein Keep-Alive-Paket über die Verbindung zu senden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-534">Sets the interval, in milliseconds, to send a keep-alive packet over the connection.</span></span> <span data-ttu-id="a4cad-535">Das Standardintervall ist 30.000 (30 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="a4cad-535">The default interval is 30000 (30 seconds).</span></span> <span data-ttu-id="a4cad-536">Das Mindestintervall beträgt 15.000 (15 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="a4cad-536">The minimum interval is 15000 (15 seconds).</span></span> <span data-ttu-id="a4cad-537">Die [**Verwendung von WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) zum Festlegen eines Werts unter 15000 gibt mit **ERROR INVALID PARAMETER \_ \_ zurück.**</span><span class="sxs-lookup"><span data-stu-id="a4cad-537">Using [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to set a value lower than 15000 will return with **ERROR\_INVALID\_PARAMETER**.</span></span>

> [!Note]
> <span data-ttu-id="a4cad-538">Der Standardwert für **WINHTTP \_ OPTION WEB SOCKET \_ \_ \_ KEEPALIVE \_ INTERVAL** wird aus **HKLM: \\ SOFTWARE Microsoft \\ \\ WebSocket \\ KeepaliveInterval gelesen.**</span><span class="sxs-lookup"><span data-stu-id="a4cad-538">The default value for **WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL** is read from **HKLM:\\SOFTWARE\\Microsoft\\WebSocket\\KeepaliveInterval**.</span></span> <span data-ttu-id="a4cad-539">Wenn kein Wert festgelegt ist, wird der Standardwert 30000 verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4cad-539">If a value is not set, the default value of 30000 will be used.</span></span> <span data-ttu-id="a4cad-540">Es ist nicht möglich, ein niedrigeres Keepalive-Intervall als 15.000 Millisekunden zu haben.</span><span class="sxs-lookup"><span data-stu-id="a4cad-540">It is not possible to have a lower keepalive interval than 15000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-541"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP-OPTION \_ \_ \_ WEBSOCKET \_ \_ \_ EMPFANGSPUFFERGRÖßE**</span><span class="sxs-lookup"><span data-stu-id="a4cad-541"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-542">Legt ein DWORD fest oder ruft es ab, das die Empfangspuffergröße angibt, die für WebSocket-Verbindungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4cad-542">Sets or retrieves a DWORD which specifies the receive buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-543"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP-OPTION \_ \_ \_ WEBSOCKET- \_ \_ \_ SENDEPUFFERGRÖßE**</span><span class="sxs-lookup"><span data-stu-id="a4cad-543"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-544">Legt ein DWORD fest oder ruft es ab, das die Sendepuffergröße angibt, die für WebSocket-Verbindungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4cad-544">Sets or retrieves a DWORD which specifies the send buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-545"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**ANZAHL DER \_ \_ ARBEITSTHREADS \_ DER WINHTTP-OPTION \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-545"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-546">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Anzahl der Arbeitsthreads angibt, die der Threadpool für asynchrone Vervollständigungen verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="a4cad-546">Sets an unsigned long integer value that specifies the number of worker threads the thread pool should use for asynchronous completions.</span></span> <span data-ttu-id="a4cad-547">Der Standardwert dieser Option ist 0 (null), was angibt, dass die Anzahl der Arbeitsthreads der Anzahl von CPUs im System entspricht.</span><span class="sxs-lookup"><span data-stu-id="a4cad-547">The default value of this option is zero, which specifies that the number of worker threads is equal to the number of CPUs on the system.</span></span> <span data-ttu-id="a4cad-548">Diese Option kann nur für ein **NULL**  [HINTERNET-Handle festgelegt](hinternet-handles-in-winhttp.md) werden, bevor ein asynchroner Vorgang ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a4cad-548">This option can only be set on a **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) handle before an asynchronous operation has occurred.</span></span> <span data-ttu-id="a4cad-549">Diese Option kann nur einmal festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a4cad-549">This option can only be set once.</span></span>

<span data-ttu-id="a4cad-550">**Windows Server 2008 R2 und Windows 7:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="a4cad-550">**Windows Server 2008 R2 and Windows 7:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a4cad-551"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**\_WINHTTP-OPTION: \_ \_ \_ SCHREIBPUFFERGRÖßE**</span><span class="sxs-lookup"><span data-stu-id="a4cad-551"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a4cad-552">Diese Option ist veraltet. es hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="a4cad-552">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4cad-553">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a4cad-553">Remarks</span></span>

<span data-ttu-id="a4cad-554">In der folgenden Tabelle werden die Optionsflags aufgeführt, indem angegeben wird, auf welche Handles sie angewendet werden können, ob sie abgefragt und festgelegt werden können und welcher Datentyp verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a4cad-554">The following table lists the option flags by specifying which handles they can act upon, whether they can be queried and set, and the data type used.</span></span> <span data-ttu-id="a4cad-555">Ein "X" gibt an, dass das Optionsflag für die Verwendung mit der Funktion oder dem Handle gültig ist, während ein "-" angibt, dass das Optionsflag ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="a4cad-555">An "X" indicates that the option flag is valid for use with the function or handle, while a "-" specifies that the option flag is invalid.</span></span>

<span data-ttu-id="a4cad-556">Der Versuch, ein Optionsflag für eine Windows-Version, in der es nicht unterstützt wird, zu festlegen oder abfragt, führt zu **ERROR \_ WINHTTP \_ INVALID \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="a4cad-556">Attempting to set or query an option flag on a Windows version where it is not supported will result in **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span>

| <span data-ttu-id="a4cad-557">Optionsflag und Datentyp</span><span class="sxs-lookup"><span data-stu-id="a4cad-557">Option flag, and data type</span></span> | <span data-ttu-id="a4cad-558">Sitzungshand handle</span><span class="sxs-lookup"><span data-stu-id="a4cad-558">Session handle</span></span> | <span data-ttu-id="a4cad-559">Anforderungshand handle</span><span class="sxs-lookup"><span data-stu-id="a4cad-559">Request handle</span></span> | <span data-ttu-id="a4cad-560">Abfrageoption</span><span class="sxs-lookup"><span data-stu-id="a4cad-560">Query option</span></span> | <span data-ttu-id="a4cad-561">SET-Option</span><span class="sxs-lookup"><span data-stu-id="a4cad-561">Set option</span></span> | <span data-ttu-id="a4cad-562">Mindestversion von Windows</span><span class="sxs-lookup"><span data-stu-id="a4cad-562">Minimum Windows Version</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="a4cad-563">\_WINHTTP-OPTION \_ \_ GARANTIERTE NICHT \_ \_ BLOCKIERENDE RÜCKRUFE</span><span class="sxs-lookup"><span data-stu-id="a4cad-563">WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS</span></span><br/><span data-ttu-id="a4cad-564">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a4cad-564">**BOOL**</span></span> | <span data-ttu-id="a4cad-565">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-565">X</span></span> | \- | \- | <span data-ttu-id="a4cad-566">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-566">X</span></span> | \- |
| <span data-ttu-id="a4cad-567">RICHTLINIE FÜR \_ DIE AUTOMATISCHE ANMELDUNG DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-567">WINHTTP\_OPTION\_AUTOLOGON\_POLICY</span></span><br/><span data-ttu-id="a4cad-568">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-568">**DWORD**</span></span> | \- | <span data-ttu-id="a4cad-569">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-569">X</span></span> | \- | <span data-ttu-id="a4cad-570">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-570">X</span></span> | \- |
| <span data-ttu-id="a4cad-571">\_ \_ WINHTTP-OPTIONSRÜCKRUF</span><span class="sxs-lookup"><span data-stu-id="a4cad-571">WINHTTP\_OPTION\_CALLBACK</span></span><br/><span data-ttu-id="a4cad-572">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="a4cad-572">**LPVOID**</span></span> | <span data-ttu-id="a4cad-573">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-573">X</span></span> | <span data-ttu-id="a4cad-574">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-574">X</span></span> | <span data-ttu-id="a4cad-575">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-575">X</span></span> | <span data-ttu-id="a4cad-576">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-576">X</span></span> | \- |
| <span data-ttu-id="a4cad-577">WINHTTP \_ OPTION \_ CLIENT \_ CERT \_ CONTEXT</span><span class="sxs-lookup"><span data-stu-id="a4cad-577">WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="a4cad-578">**\_CERT-KONTEXT**</span><span class="sxs-lookup"><span data-stu-id="a4cad-578">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="a4cad-579">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-579">X</span></span> | \- | <span data-ttu-id="a4cad-580">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-580">X</span></span> | <span data-ttu-id="a4cad-581">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4cad-581">Windows Vista</span></span> |
| <span data-ttu-id="a4cad-582">\_WINHTTP-OPTION \_ \_ CLIENTZERTIFIKATAUSSTELLERLISTE \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-582">WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST</span></span><br/>[<span data-ttu-id="a4cad-583">**SecPkgContext \_ IssuerListInfoEx**</span><span class="sxs-lookup"><span data-stu-id="a4cad-583">**SecPkgContext\_IssuerListInfoEx**</span></span>](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | <span data-ttu-id="a4cad-584">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-584">X</span></span> | <span data-ttu-id="a4cad-585">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-585">X</span></span> | \- | <span data-ttu-id="a4cad-586">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4cad-586">Windows Vista</span></span> |
| <span data-ttu-id="a4cad-587">\_ \_ WINHTTP-OPTIONSCODEPAGE</span><span class="sxs-lookup"><span data-stu-id="a4cad-587">WINHTTP\_OPTION\_CODEPAGE</span></span><br/><span data-ttu-id="a4cad-588">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-588">**DWORD**</span></span> | <span data-ttu-id="a4cad-589">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-589">X</span></span> | \- | \- | <span data-ttu-id="a4cad-590">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-590">X</span></span> | \- |
| <span data-ttu-id="a4cad-591">\_WINHTTP-OPTION: \_ \_ KONFIGURIEREN DER \_ PASSPORT-AUTHENTIFIZIERUNG</span><span class="sxs-lookup"><span data-stu-id="a4cad-591">WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH</span></span><br/><span data-ttu-id="a4cad-592">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-592">**DWORD**</span></span> | <span data-ttu-id="a4cad-593">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-593">X</span></span> | \- | \- | <span data-ttu-id="a4cad-594">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-594">X</span></span> | \- |
| <span data-ttu-id="a4cad-595">\_WINHTTP-OPTION \_ – \_ VERBINDUNGS-RETRIES</span><span class="sxs-lookup"><span data-stu-id="a4cad-595">WINHTTP\_OPTION\_CONNECT\_RETRIES</span></span><br/><span data-ttu-id="a4cad-596">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-596">**DWORD**</span></span> | <span data-ttu-id="a4cad-597">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-597">X</span></span> | <span data-ttu-id="a4cad-598">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-598">X</span></span> | <span data-ttu-id="a4cad-599">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-599">X</span></span> | <span data-ttu-id="a4cad-600">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-600">X</span></span> | \- |
| <span data-ttu-id="a4cad-601">WINHTTP \_ OPTION \_ CONNECT \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a4cad-601">WINHTTP\_OPTION\_CONNECT\_TIMEOUT</span></span><br/><span data-ttu-id="a4cad-602">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-602">**DWORD**</span></span> | <span data-ttu-id="a4cad-603">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-603">X</span></span> | <span data-ttu-id="a4cad-604">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-604">X</span></span> | <span data-ttu-id="a4cad-605">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-605">X</span></span> | <span data-ttu-id="a4cad-606">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-606">X</span></span> | \- |
| <span data-ttu-id="a4cad-607">VERBINDUNGSINFORMATIONEN ZUR \_ WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-607">WINHTTP\_OPTION\_CONNECTION\_INFO</span></span><br/>[<span data-ttu-id="a4cad-608">**\_WINHTTP-VERBINDUNGSINFORMATIONEN \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-608">**WINHTTP\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | <span data-ttu-id="a4cad-609">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-609">X</span></span> | <span data-ttu-id="a4cad-610">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-610">X</span></span> | \- | \- |
| <span data-ttu-id="a4cad-611">WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V0</span><span class="sxs-lookup"><span data-stu-id="a4cad-611">WINHTTP\_OPTION\_CONNECTION\_STATS\_V0</span></span><br/>[<span data-ttu-id="a4cad-612">**TCP \_ INFO \_ v0**</span><span class="sxs-lookup"><span data-stu-id="a4cad-612">**TCP\_INFO\_v0**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | <span data-ttu-id="a4cad-613">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-613">X</span></span> | <span data-ttu-id="a4cad-614">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-614">X</span></span> | \- | <span data-ttu-id="a4cad-615">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="a4cad-615">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a4cad-616">WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1</span><span class="sxs-lookup"><span data-stu-id="a4cad-616">WINHTTP\_OPTION\_CONNECTION\_STATS\_V1</span></span><br/>[<span data-ttu-id="a4cad-617">**TCP \_ INFO \_ v1**</span><span class="sxs-lookup"><span data-stu-id="a4cad-617">**TCP\_INFO\_v1**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | <span data-ttu-id="a4cad-618">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-618">X</span></span> | <span data-ttu-id="a4cad-619">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-619">X</span></span> | \- | <span data-ttu-id="a4cad-620">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="a4cad-620">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a4cad-621">\_ \_ WINHTTP-OPTIONSKONTEXTWERT \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-621">WINHTTP\_OPTION\_CONTEXT\_VALUE</span></span><br/><span data-ttu-id="a4cad-622">**DWORD \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="a4cad-622">**DWORD\_PTR**</span></span> | <span data-ttu-id="a4cad-623">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-623">X</span></span> | <span data-ttu-id="a4cad-624">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-624">X</span></span> | <span data-ttu-id="a4cad-625">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-625">X</span></span> | <span data-ttu-id="a4cad-626">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-626">X</span></span> | \- |
| <span data-ttu-id="a4cad-627">WINHTTP \_ OPTION \_ DEKOMPRIMIERUNG</span><span class="sxs-lookup"><span data-stu-id="a4cad-627">WINHTTP\_OPTION\_DECOMPRESSION</span></span><br/><span data-ttu-id="a4cad-628">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-628">**DWORD**</span></span> | <span data-ttu-id="a4cad-629">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-629">X</span></span> | <span data-ttu-id="a4cad-630">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-630">X</span></span> | \- | <span data-ttu-id="a4cad-631">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-631">X</span></span> | <span data-ttu-id="a4cad-632">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a4cad-632">Windows 8.1</span></span> |
| <span data-ttu-id="a4cad-633">WINHTTP \_ OPTION \_ DISABLE \_ FEATURE</span><span class="sxs-lookup"><span data-stu-id="a4cad-633">WINHTTP\_OPTION\_DISABLE\_FEATURE</span></span><br/><span data-ttu-id="a4cad-634">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-634">**DWORD**</span></span> | \- | <span data-ttu-id="a4cad-635">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-635">X</span></span> | \- | <span data-ttu-id="a4cad-636">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-636">X</span></span> | \- |
| <span data-ttu-id="a4cad-637">\_WINHTTP-OPTION \_ DISABLE SECURE \_ PROTOCOL \_ \_ FALLBACK</span><span class="sxs-lookup"><span data-stu-id="a4cad-637">WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK</span></span><br/><span data-ttu-id="a4cad-638">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a4cad-638">**BOOL**</span></span> | <span data-ttu-id="a4cad-639">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-639">X</span></span> | \- | \- | <span data-ttu-id="a4cad-640">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-640">X</span></span> | <span data-ttu-id="a4cad-641">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="a4cad-641">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a4cad-642">\_WINHTTP-OPTION \_ : DEAKTIVIEREN DER \_ \_ STREAMWARTESCHLANGE</span><span class="sxs-lookup"><span data-stu-id="a4cad-642">WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE</span></span><br/><span data-ttu-id="a4cad-643">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a4cad-643">**BOOL**</span></span> | <span data-ttu-id="a4cad-644">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-644">X</span></span> | <span data-ttu-id="a4cad-645">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-645">X</span></span> | \- | <span data-ttu-id="a4cad-646">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-646">X</span></span> | <span data-ttu-id="a4cad-647">Windows 10 Version 1809</span><span class="sxs-lookup"><span data-stu-id="a4cad-647">Windows 10 Version 1809</span></span> |
| <span data-ttu-id="a4cad-648">WINHTTP \_ OPTION \_ ENABLE \_ FEATURE</span><span class="sxs-lookup"><span data-stu-id="a4cad-648">WINHTTP\_OPTION\_ENABLE\_FEATURE</span></span><br/><span data-ttu-id="a4cad-649">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-649">**DWORD**</span></span> | \* | \* | \- | <span data-ttu-id="a4cad-650">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-650">X</span></span> | \- |
| <span data-ttu-id="a4cad-651">\_WINHTTP-OPTION: \_ AKTIVIEREN DES \_ \_ HTTP-PROTOKOLLS</span><span class="sxs-lookup"><span data-stu-id="a4cad-651">WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL</span></span><br/><span data-ttu-id="a4cad-652">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-652">**DWORD**</span></span> | <span data-ttu-id="a4cad-653">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-653">X</span></span> | <span data-ttu-id="a4cad-654">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-654">X</span></span> | \- | <span data-ttu-id="a4cad-655">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-655">X</span></span> | <span data-ttu-id="a4cad-656">Windows 10, Version 1607</span><span class="sxs-lookup"><span data-stu-id="a4cad-656">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="a4cad-657">\_WINHTTP-OPTION \_ ENABLETRACING</span><span class="sxs-lookup"><span data-stu-id="a4cad-657">WINHTTP\_OPTION\_ENABLETRACING</span></span><br/><span data-ttu-id="a4cad-658">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-658">**DWORD**</span></span> | \- | \- | <span data-ttu-id="a4cad-659">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-659">X</span></span> | <span data-ttu-id="a4cad-660">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-660">X</span></span> | \- |
| <span data-ttu-id="a4cad-661">WINHTTP \_ OPTION \_ ENCODE \_ EXTRA</span><span class="sxs-lookup"><span data-stu-id="a4cad-661">WINHTTP\_OPTION\_ENCODE\_EXTRA</span></span><br/><span data-ttu-id="a4cad-662">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a4cad-662">**BOOL**</span></span> | <span data-ttu-id="a4cad-663">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-663">X</span></span> | <span data-ttu-id="a4cad-664">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-664">X</span></span> | \- | <span data-ttu-id="a4cad-665">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-665">X</span></span> | <span data-ttu-id="a4cad-666">Windows 10 Version 1803</span><span class="sxs-lookup"><span data-stu-id="a4cad-666">Windows 10 Version 1803</span></span> |
| <span data-ttu-id="a4cad-667">\_WINHTTP-OPTION \_ LÄUFT VERBINDUNG AB \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-667">WINHTTP\_OPTION\_EXPIRE\_CONNECTION</span></span><br/><span data-ttu-id="a4cad-668">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="a4cad-668">N/A</span></span> | \- | <span data-ttu-id="a4cad-669">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-669">X</span></span> | \- | <span data-ttu-id="a4cad-670">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-670">X</span></span> | <span data-ttu-id="a4cad-671">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="a4cad-671">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a4cad-672">\_ \_ ERWEITERTER \_ WINHTTP-OPTION-FEHLER</span><span class="sxs-lookup"><span data-stu-id="a4cad-672">WINHTTP\_OPTION\_EXTENDED\_ERROR</span></span><br/><span data-ttu-id="a4cad-673">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-673">**DWORD**</span></span> | <span data-ttu-id="a4cad-674">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-674">X</span></span> | <span data-ttu-id="a4cad-675">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-675">X</span></span> | <span data-ttu-id="a4cad-676">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-676">X</span></span> | \- | \- |
| <span data-ttu-id="a4cad-677">WINHTTP \_ OPTION \_ GLOBAL \_ PROXY \_ CREDS</span><span class="sxs-lookup"><span data-stu-id="a4cad-677">WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS</span></span><br/>[<span data-ttu-id="a4cad-678">**WINHTTP \_ CREDS**</span><span class="sxs-lookup"><span data-stu-id="a4cad-678">**WINHTTP\_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | <span data-ttu-id="a4cad-679">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-679">X</span></span> | <span data-ttu-id="a4cad-680">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-680">X</span></span> | \- | <span data-ttu-id="a4cad-681">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-681">X</span></span> | \- |
| <span data-ttu-id="a4cad-682">WINHTTP \_ OPTION \_ GLOBAL \_ SERVER \_ CREDS</span><span class="sxs-lookup"><span data-stu-id="a4cad-682">WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS</span></span><br/>[<span data-ttu-id="a4cad-683">**WINHTTP \_ CREDS \_ EX**</span><span class="sxs-lookup"><span data-stu-id="a4cad-683">**WINHTTP\_CREDS\_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | <span data-ttu-id="a4cad-684">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-684">X</span></span> | <span data-ttu-id="a4cad-685">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-685">X</span></span> | \- | <span data-ttu-id="a4cad-686">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-686">X</span></span> | \- |
| <span data-ttu-id="a4cad-687">TYP DES \_ WINHTTP-OPTIONSHANDLE \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-687">WINHTTP\_OPTION\_HANDLE\_TYPE</span></span><br/><span data-ttu-id="a4cad-688">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-688">**DWORD**</span></span> | <span data-ttu-id="a4cad-689">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-689">X</span></span> | <span data-ttu-id="a4cad-690">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-690">X</span></span> | <span data-ttu-id="a4cad-691">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-691">X</span></span> | \- | \- |
| <span data-ttu-id="a4cad-692">WINHTTP \_ OPTION HTTP PROTOCOL \_ \_ \_ ERFORDERLICH</span><span class="sxs-lookup"><span data-stu-id="a4cad-692">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED</span></span><br/><span data-ttu-id="a4cad-693">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a4cad-693">**BOOL**</span></span> | <span data-ttu-id="a4cad-694">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-694">X</span></span> | <span data-ttu-id="a4cad-695">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-695">X</span></span> | \- | <span data-ttu-id="a4cad-696">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-696">X</span></span> | <span data-ttu-id="a4cad-697">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="a4cad-697">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a4cad-698">VERWENDETES \_ \_ WINHTTP-OPTION-HTTP-PROTOKOLL \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-698">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED</span></span><br/><span data-ttu-id="a4cad-699">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-699">**DWORD**</span></span> | \- | <span data-ttu-id="a4cad-700">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-700">X</span></span> | <span data-ttu-id="a4cad-701">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-701">X</span></span> | \- | <span data-ttu-id="a4cad-702">Windows 10, Version 1607</span><span class="sxs-lookup"><span data-stu-id="a4cad-702">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="a4cad-703">\_HTTP-VERSION DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-703">WINHTTP\_OPTION\_HTTP\_VERSION</span></span><br/>[<span data-ttu-id="a4cad-704">**\_ \_ HTTP-VERSIONSINFORMATIONEN**</span><span class="sxs-lookup"><span data-stu-id="a4cad-704">**HTTP\_VERSION\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | <span data-ttu-id="a4cad-705">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-705">X</span></span> | <span data-ttu-id="a4cad-706">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-706">X</span></span> | <span data-ttu-id="a4cad-707">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-707">X</span></span> | <span data-ttu-id="a4cad-708">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-708">X</span></span> | \- |
| <span data-ttu-id="a4cad-709">WINHTTP-OPTION \_ \_ \_ ZERTIFIKATSPERRUNG \_ \_ OFFLINE IGNORIEREN</span><span class="sxs-lookup"><span data-stu-id="a4cad-709">WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE</span></span><br/><span data-ttu-id="a4cad-710">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a4cad-710">**BOOL**</span></span> | \- | <span data-ttu-id="a4cad-711">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-711">X</span></span> | \- | <span data-ttu-id="a4cad-712">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-712">X</span></span> | <span data-ttu-id="a4cad-713">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="a4cad-713">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a4cad-714">WINHTTP-OPTION \_ \_ IPV6 \_ – SCHNELLER \_ FALLBACK</span><span class="sxs-lookup"><span data-stu-id="a4cad-714">WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK</span></span><br/><span data-ttu-id="a4cad-715">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a4cad-715">**BOOL**</span></span> | <span data-ttu-id="a4cad-716">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-716">X</span></span> | \- | \- | <span data-ttu-id="a4cad-717">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-717">X</span></span> | <span data-ttu-id="a4cad-718">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="a4cad-718">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a4cad-719">\_WINHTTP-OPTION \_ IST PROXY \_ \_ \_ CONNECT-ANTWORT</span><span class="sxs-lookup"><span data-stu-id="a4cad-719">WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="a4cad-720">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a4cad-720">**BOOL**</span></span> | <span data-ttu-id="a4cad-721">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-721">X</span></span> | <span data-ttu-id="a4cad-722">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-722">X</span></span> | <span data-ttu-id="a4cad-723">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-723">X</span></span> | \- | \- |
| <span data-ttu-id="a4cad-724">\_WINHTTP-OPTION \_ \_ MAX. CONNS \_ PRO \_ 1 \_ 0 \_ SERVER</span><span class="sxs-lookup"><span data-stu-id="a4cad-724">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER</span></span><br/><span data-ttu-id="a4cad-725">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-725">**DWORD**</span></span> | <span data-ttu-id="a4cad-726">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-726">X</span></span> | \- | <span data-ttu-id="a4cad-727">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-727">X</span></span> | <span data-ttu-id="a4cad-728">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-728">X</span></span> | \- |
| <span data-ttu-id="a4cad-729">\_WINHTTP-OPTION \_ \_ MAX. CONNS \_ PRO \_ SERVER</span><span class="sxs-lookup"><span data-stu-id="a4cad-729">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER</span></span><br/><span data-ttu-id="a4cad-730">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-730">**DWORD**</span></span> | <span data-ttu-id="a4cad-731">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-731">X</span></span> | \- | <span data-ttu-id="a4cad-732">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-732">X</span></span> | <span data-ttu-id="a4cad-733">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-733">X</span></span> | \- |
| <span data-ttu-id="a4cad-734">WINHTTP-OPTION \_ \_ \_ MAX. AUTOMATISCHE \_ \_ HTTP-UMLEITUNGEN</span><span class="sxs-lookup"><span data-stu-id="a4cad-734">WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS</span></span><br/><span data-ttu-id="a4cad-735">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-735">**DWORD**</span></span> | <span data-ttu-id="a4cad-736">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-736">X</span></span> | <span data-ttu-id="a4cad-737">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-737">X</span></span> | <span data-ttu-id="a4cad-738">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-738">X</span></span> | <span data-ttu-id="a4cad-739">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-739">X</span></span> | \- |
| <span data-ttu-id="a4cad-740">\_WINHTTP-OPTION \_ \_ MAX. \_ HTTP-STATUS \_ CONTINUE</span><span class="sxs-lookup"><span data-stu-id="a4cad-740">WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE</span></span><br/><span data-ttu-id="a4cad-741">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-741">**DWORD**</span></span> | <span data-ttu-id="a4cad-742">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-742">X</span></span> | <span data-ttu-id="a4cad-743">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-743">X</span></span> | <span data-ttu-id="a4cad-744">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-744">X</span></span> | <span data-ttu-id="a4cad-745">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-745">X</span></span> | \- |
| <span data-ttu-id="a4cad-746">WINHTTP \_ OPTION \_ MAX \_ RESPONSE \_ DRAIN \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="a4cad-746">WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE</span></span><br/><span data-ttu-id="a4cad-747">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-747">**DWORD**</span></span> | <span data-ttu-id="a4cad-748">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-748">X</span></span> | <span data-ttu-id="a4cad-749">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-749">X</span></span> | <span data-ttu-id="a4cad-750">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-750">X</span></span> | <span data-ttu-id="a4cad-751">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-751">X</span></span> | \- |
| <span data-ttu-id="a4cad-752">MAXIMALE GRÖßE DES \_ \_ \_ \_ ANTWORTHEADERS DER \_ WINHTTP-OPTION</span><span class="sxs-lookup"><span data-stu-id="a4cad-752">WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE</span></span><br/><span data-ttu-id="a4cad-753">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-753">**DWORD**</span></span> | <span data-ttu-id="a4cad-754">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-754">X</span></span> | <span data-ttu-id="a4cad-755">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-755">X</span></span> | <span data-ttu-id="a4cad-756">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-756">X</span></span> | <span data-ttu-id="a4cad-757">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-757">X</span></span> | \- |
| <span data-ttu-id="a4cad-758">ÜBERGEORDNETES \_ HANDLE DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-758">WINHTTP\_OPTION\_PARENT\_HANDLE</span></span><br/>[<span data-ttu-id="a4cad-759">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="a4cad-759">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="a4cad-760">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-760">X</span></span> | <span data-ttu-id="a4cad-761">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-761">X</span></span> | <span data-ttu-id="a4cad-762">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-762">X</span></span> | \- | \- |
| <span data-ttu-id="a4cad-763">\_WINHTTP-OPTION \_ \_ PASSPORT-COBRANDINGTEXT \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-763">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT</span></span><br/><span data-ttu-id="a4cad-764">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="a4cad-764">**LPWSTR**</span></span> | \- | <span data-ttu-id="a4cad-765">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-765">X</span></span> | <span data-ttu-id="a4cad-766">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-766">X</span></span> | \- | \- |
| <span data-ttu-id="a4cad-767">\_WINHTTP-OPTION \_ \_ PASSPORT-COBRANDING-URL \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-767">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL</span></span><br/><span data-ttu-id="a4cad-768">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="a4cad-768">**LPWSTR**</span></span> | \- | <span data-ttu-id="a4cad-769">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-769">X</span></span> | <span data-ttu-id="a4cad-770">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-770">X</span></span> | \- | \- |
| <span data-ttu-id="a4cad-771">\_WINHTTP-OPTION \_ \_ \_ PASSPORT-RÜCKGABE-URL</span><span class="sxs-lookup"><span data-stu-id="a4cad-771">WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL</span></span><br/><span data-ttu-id="a4cad-772">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="a4cad-772">**LPVOID**</span></span> | \- | <span data-ttu-id="a4cad-773">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-773">X</span></span> | <span data-ttu-id="a4cad-774">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-774">X</span></span> | \- | \- |
| <span data-ttu-id="a4cad-775">\_WINHTTP-OPTION \_ \_ \_ PASSPORT-ABMELDE</span><span class="sxs-lookup"><span data-stu-id="a4cad-775">WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT</span></span><br/><span data-ttu-id="a4cad-776">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="a4cad-776">**LPVOID**</span></span> | <span data-ttu-id="a4cad-777">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-777">X</span></span> | \- | \- | <span data-ttu-id="a4cad-778">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-778">X</span></span> | \- |
| <span data-ttu-id="a4cad-779">\_ \_ WINHTTP-OPTIONSKENNWORT</span><span class="sxs-lookup"><span data-stu-id="a4cad-779">WINHTTP\_OPTION\_PASSWORD</span></span><br/><span data-ttu-id="a4cad-780">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="a4cad-780">**LPWSTR**</span></span> | \- | <span data-ttu-id="a4cad-781">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-781">X</span></span> | <span data-ttu-id="a4cad-782">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-782">X</span></span> | <span data-ttu-id="a4cad-783">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-783">X</span></span> | \- |
| <span data-ttu-id="a4cad-784">\_WINHTTP-OPTIONSPROXY \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-784">WINHTTP\_OPTION\_PROXY</span></span><br/>[<span data-ttu-id="a4cad-785">**\_WINHTTP-PROXYINFORMATIONEN \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-785">**WINHTTP\_PROXY\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | <span data-ttu-id="a4cad-786">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-786">X</span></span> | <span data-ttu-id="a4cad-787">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-787">X</span></span> | <span data-ttu-id="a4cad-788">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-788">X</span></span> | <span data-ttu-id="a4cad-789">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-789">X</span></span> | \- |
| <span data-ttu-id="a4cad-790">\_PROXYKENNWORT \_ FÜR WINHTTP-OPTION \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-790">WINHTTP\_OPTION\_PROXY\_PASSWORD</span></span><br/><span data-ttu-id="a4cad-791">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="a4cad-791">**LPWSTR**</span></span> | \- | <span data-ttu-id="a4cad-792">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-792">X</span></span> | <span data-ttu-id="a4cad-793">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-793">X</span></span> | <span data-ttu-id="a4cad-794">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-794">X</span></span> | \- |
| <span data-ttu-id="a4cad-795">VERWENDETER \_ \_ WINHTTP-OPTIONSPROXY-SPN \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-795">WINHTTP\_OPTION\_PROXY\_SPN\_USED</span></span><br/><span data-ttu-id="a4cad-796">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="a4cad-796">**LPWSTR**</span></span> | \- | <span data-ttu-id="a4cad-797">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-797">X</span></span> | <span data-ttu-id="a4cad-798">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-798">X</span></span> | \- | \- |
| <span data-ttu-id="a4cad-799">\_PROXYBENUTZERNAME DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-799">WINHTTP\_OPTION\_PROXY\_USERNAME</span></span><br/><span data-ttu-id="a4cad-800">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="a4cad-800">**LPWSTR**</span></span> | \- | <span data-ttu-id="a4cad-801">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-801">X</span></span> | <span data-ttu-id="a4cad-802">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-802">X</span></span> | <span data-ttu-id="a4cad-803">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-803">X</span></span> | \- |
| <span data-ttu-id="a4cad-804">\_WINHTTP-OPTION \_ READ BUFFER \_ \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="a4cad-804">WINHTTP\_OPTION\_READ\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="a4cad-805">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-805">**DWORD**</span></span> | \- | <span data-ttu-id="a4cad-806">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-806">X</span></span> | <span data-ttu-id="a4cad-807">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-807">X</span></span> | <span data-ttu-id="a4cad-808">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-808">X</span></span> | \- |
| <span data-ttu-id="a4cad-809">WINHTTP-OPTION \_ \_ "PROXY \_ \_ CONNECT-ANTWORT \_ EMPFANGEN"</span><span class="sxs-lookup"><span data-stu-id="a4cad-809">WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="a4cad-810">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a4cad-810">**BOOL**</span></span> | <span data-ttu-id="a4cad-811">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-811">X</span></span> | <span data-ttu-id="a4cad-812">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-812">X</span></span> | \- | <span data-ttu-id="a4cad-813">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-813">X</span></span> | \- |
| <span data-ttu-id="a4cad-814">WINHTTP-OPTION \_ \_ \_ \_ EMPFANGSANTWORT-TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a4cad-814">WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT</span></span><br/><span data-ttu-id="a4cad-815">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-815">**DWORD**</span></span> | <span data-ttu-id="a4cad-816">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-816">X</span></span> | <span data-ttu-id="a4cad-817">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-817">X</span></span> | <span data-ttu-id="a4cad-818">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-818">X</span></span> | <span data-ttu-id="a4cad-819">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-819">X</span></span> | \- |
| <span data-ttu-id="a4cad-820">\_EMPFANGSZEITÜBERSCHREITUNG DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-820">WINHTTP\_OPTION\_RECEIVE\_TIMEOUT</span></span><br/><span data-ttu-id="a4cad-821">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-821">**DWORD**</span></span> | <span data-ttu-id="a4cad-822">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-822">X</span></span> | <span data-ttu-id="a4cad-823">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-823">X</span></span> | <span data-ttu-id="a4cad-824">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-824">X</span></span> | <span data-ttu-id="a4cad-825">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-825">X</span></span> | \- |
| <span data-ttu-id="a4cad-826">UMLEITUNGSRICHTLINIE \_ FÜR WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-826">WINHTTP\_OPTION\_REDIRECT\_POLICY</span></span><br/><span data-ttu-id="a4cad-827">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-827">**DWORD**</span></span> | <span data-ttu-id="a4cad-828">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-828">X</span></span> | <span data-ttu-id="a4cad-829">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-829">X</span></span> | <span data-ttu-id="a4cad-830">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-830">X</span></span> | <span data-ttu-id="a4cad-831">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-831">X</span></span> | \- |
| <span data-ttu-id="a4cad-832">\_WINHTTP-OPTION \_ BENUTZER IN URL \_ \_ \_ ABLEHNENPWD</span><span class="sxs-lookup"><span data-stu-id="a4cad-832">WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL</span></span><br/><span data-ttu-id="a4cad-833">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a4cad-833">**BOOL**</span></span> | \- | <span data-ttu-id="a4cad-834">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-834">X</span></span> | \- | <span data-ttu-id="a4cad-835">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-835">X</span></span> | \- |
| <span data-ttu-id="a4cad-836">\_WINHTTP-OPTION \_ – \_ ANFORDERUNGSPRIORITÄT</span><span class="sxs-lookup"><span data-stu-id="a4cad-836">WINHTTP\_OPTION\_REQUEST\_PRIORITY</span></span><br/><span data-ttu-id="a4cad-837">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-837">**DWORD**</span></span> | \- | <span data-ttu-id="a4cad-838">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-838">X</span></span> | <span data-ttu-id="a4cad-839">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-839">X</span></span> | <span data-ttu-id="a4cad-840">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-840">X</span></span> | \- |
| <span data-ttu-id="a4cad-841">\_ \_ WINHTTP-OPTIONSANFORDERUNGSSTATISTIKEN \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-841">WINHTTP\_OPTION\_REQUEST\_STATS</span></span><br/>[<span data-ttu-id="a4cad-842">**\_ \_ WINHTTP-ANFORDERUNGSSTATISTIKEN**</span><span class="sxs-lookup"><span data-stu-id="a4cad-842">**WINHTTP\_REQUEST\_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | <span data-ttu-id="a4cad-843">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-843">X</span></span> | <span data-ttu-id="a4cad-844">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-844">X</span></span> | \- | <span data-ttu-id="a4cad-845">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="a4cad-845">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a4cad-846">ANFORDERUNGSZEITEN \_ DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-846">WINHTTP\_OPTION\_REQUEST\_TIMES</span></span><br/>[<span data-ttu-id="a4cad-847">**\_WINHTTP-ANFORDERUNGSZEITEN \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-847">**WINHTTP\_REQUEST\_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | <span data-ttu-id="a4cad-848">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-848">X</span></span> | <span data-ttu-id="a4cad-849">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-849">X</span></span> | \- | <span data-ttu-id="a4cad-850">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="a4cad-850">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a4cad-851">WINHTTP-OPTION \_ \_ \_ TIMEOUT AUFLÖSEN</span><span class="sxs-lookup"><span data-stu-id="a4cad-851">WINHTTP\_OPTION\_RESOLVE\_TIMEOUT</span></span><br/><span data-ttu-id="a4cad-852">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-852">**DWORD**</span></span> | <span data-ttu-id="a4cad-853">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-853">X</span></span> | <span data-ttu-id="a4cad-854">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-854">X</span></span> | <span data-ttu-id="a4cad-855">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-855">X</span></span> | <span data-ttu-id="a4cad-856">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-856">X</span></span> | \- |
| <span data-ttu-id="a4cad-857">SICHERE PROTOKOLLE \_ DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-857">WINHTTP\_OPTION\_SECURE\_PROTOCOLS</span></span><br/><span data-ttu-id="a4cad-858">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-858">**DWORD**</span></span> | <span data-ttu-id="a4cad-859">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-859">X</span></span> | \- | \- | <span data-ttu-id="a4cad-860">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-860">X</span></span> | \- |
| <span data-ttu-id="a4cad-861">\_SICHERHEITSZERTIFIKATSTRUKTUR DER WINHTTP-OPTION \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-861">WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT</span></span><br/>[<span data-ttu-id="a4cad-862">**\_WINHTTP-ZERTIFIKATINFORMATIONEN \_**</span><span class="sxs-lookup"><span data-stu-id="a4cad-862">**WINHTTP\_CERTIFICATE\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | <span data-ttu-id="a4cad-863">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-863">X</span></span> | <span data-ttu-id="a4cad-864">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-864">X</span></span> | \- | \- |
| <span data-ttu-id="a4cad-865">\_SICHERHEITSFLAGS FÜR DIE WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-865">WINHTTP\_OPTION\_SECURITY\_FLAGS</span></span><br/><span data-ttu-id="a4cad-866">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-866">**DWORD**</span></span> | \- | <span data-ttu-id="a4cad-867">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-867">X</span></span> | <span data-ttu-id="a4cad-868">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-868">X</span></span> | <span data-ttu-id="a4cad-869">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-869">X</span></span> | \- |
| <span data-ttu-id="a4cad-870">SICHERHEITSINFORMATIONEN \_ ZUR WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-870">WINHTTP\_OPTION\_SECURITY\_INFO</span></span><br/>[<span data-ttu-id="a4cad-871">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="a4cad-871">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | <span data-ttu-id="a4cad-872">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-872">X</span></span> | <span data-ttu-id="a4cad-873">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-873">X</span></span> | \- | <span data-ttu-id="a4cad-874">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="a4cad-874">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a4cad-875">\_WINHTTP-OPTION \_ \_ \_ SICHERHEITSSCHLÜSSELBITNESS</span><span class="sxs-lookup"><span data-stu-id="a4cad-875">WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS</span></span><br/><span data-ttu-id="a4cad-876">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-876">**DWORD**</span></span> | \- | <span data-ttu-id="a4cad-877">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-877">X</span></span> | <span data-ttu-id="a4cad-878">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-878">X</span></span> | \- | \- |
| <span data-ttu-id="a4cad-879">TIMEOUT \_ BEIM SENDEN DER \_ \_ WINHTTP-OPTION</span><span class="sxs-lookup"><span data-stu-id="a4cad-879">WINHTTP\_OPTION\_SEND\_TIMEOUT</span></span><br/><span data-ttu-id="a4cad-880">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-880">**DWORD**</span></span> | <span data-ttu-id="a4cad-881">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-881">X</span></span> | <span data-ttu-id="a4cad-882">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-882">X</span></span> | <span data-ttu-id="a4cad-883">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-883">X</span></span> | <span data-ttu-id="a4cad-884">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-884">X</span></span> | \- |
| <span data-ttu-id="a4cad-885">WINHTTP \_ OPTION \_ SERVER \_ CBT</span><span class="sxs-lookup"><span data-stu-id="a4cad-885">WINHTTP\_OPTION\_SERVER\_CBT</span></span><br/><span data-ttu-id="a4cad-886">[**\_SecPkgContext-Bindungen**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span><span class="sxs-lookup"><span data-stu-id="a4cad-886">[**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span></span> | \- | <span data-ttu-id="a4cad-887">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-887">X</span></span> | <span data-ttu-id="a4cad-888">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-888">X</span></span> | \- | \- |
| <span data-ttu-id="a4cad-889">WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CHAIN \_ CONTEXT</span><span class="sxs-lookup"><span data-stu-id="a4cad-889">WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT</span></span><br/>[<span data-ttu-id="a4cad-890">**CERT_CHAIN_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="a4cad-890">**CERT_CHAIN_CONTEXT**</span></span>](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | <span data-ttu-id="a4cad-891">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-891">X</span></span> | <span data-ttu-id="a4cad-892">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-892">X</span></span> | \- | <span data-ttu-id="a4cad-893">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="a4cad-893">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a4cad-894">WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CONTEXT</span><span class="sxs-lookup"><span data-stu-id="a4cad-894">WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="a4cad-895">**CERT-KONTEXT**</span><span class="sxs-lookup"><span data-stu-id="a4cad-895">**CERT CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="a4cad-896">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-896">X</span></span> | <span data-ttu-id="a4cad-897">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-897">X</span></span> | \- | \- |
| <span data-ttu-id="a4cad-898">VERWENDETER \_ \_ WINHTTP-OPTIONSSERVER-SPN \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-898">WINHTTP\_OPTION\_SERVER\_SPN\_USED</span></span><br/><span data-ttu-id="a4cad-899">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="a4cad-899">**LPWSTR**</span></span> | \- | <span data-ttu-id="a4cad-900">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-900">X</span></span> | <span data-ttu-id="a4cad-901">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-901">X</span></span> | \- | \- |
| <span data-ttu-id="a4cad-902">\_ \_ WINHTTP-OPTIONS-SPN</span><span class="sxs-lookup"><span data-stu-id="a4cad-902">WINHTTP\_OPTION\_SPN</span></span><br/><span data-ttu-id="a4cad-903">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-903">**DWORD**</span></span> | \- | <span data-ttu-id="a4cad-904">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-904">X</span></span> | \- | <span data-ttu-id="a4cad-905">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-905">X</span></span> | \- |
| <span data-ttu-id="a4cad-906">WINHTTP-OPTION \_ \_ TCP FAST \_ \_ OPEN</span><span class="sxs-lookup"><span data-stu-id="a4cad-906">WINHTTP\_OPTION\_TCP\_FAST\_OPEN</span></span><br/><span data-ttu-id="a4cad-907">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a4cad-907">**BOOL**</span></span> | <span data-ttu-id="a4cad-908">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-908">X</span></span> | \- | \- | <span data-ttu-id="a4cad-909">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-909">X</span></span> | <span data-ttu-id="a4cad-910">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="a4cad-910">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a4cad-911">WINHTTP-OPTION \_ \_ TLS FALSE \_ \_ START</span><span class="sxs-lookup"><span data-stu-id="a4cad-911">WINHTTP\_OPTION\_TLS\_FALSE\_START</span></span><br/><span data-ttu-id="a4cad-912">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a4cad-912">**BOOL**</span></span> | <span data-ttu-id="a4cad-913">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-913">X</span></span> | \- | \- | <span data-ttu-id="a4cad-914">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-914">X</span></span> | <span data-ttu-id="a4cad-915">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="a4cad-915">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a4cad-916">WINHTTP-OPTION \_ \_ \_ ENTLADEBENACHRICHTIGUNGSEREIGNIS \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-916">WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT</span></span><br/>[<span data-ttu-id="a4cad-917">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="a4cad-917">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="a4cad-918">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-918">X</span></span> | \- | \- | <span data-ttu-id="a4cad-919">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-919">X</span></span> | \- |
| <span data-ttu-id="a4cad-920">WINHTTP \_ OPTION \_ UNSAFE \_ HEADER \_ PARSING</span><span class="sxs-lookup"><span data-stu-id="a4cad-920">WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING</span></span><br/><span data-ttu-id="a4cad-921">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-921">**DWORD**</span></span> | \- | <span data-ttu-id="a4cad-922">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-922">X</span></span> | \- | <span data-ttu-id="a4cad-923">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-923">X</span></span> | \- |
| <span data-ttu-id="a4cad-924">UPGRADE DER \_ \_ WINHTTP-OPTION \_ AUF \_ \_ WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="a4cad-924">WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET</span></span><br/><span data-ttu-id="a4cad-925">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="a4cad-925">N/A</span></span> | \- | <span data-ttu-id="a4cad-926">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-926">X</span></span> | \- | <span data-ttu-id="a4cad-927">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-927">X</span></span> | \- |
| <span data-ttu-id="a4cad-928">URL DER \_ \_ WINHTTP-OPTION</span><span class="sxs-lookup"><span data-stu-id="a4cad-928">WINHTTP\_OPTION\_URL</span></span><br/><span data-ttu-id="a4cad-929">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="a4cad-929">**LPWSTR**</span></span> | \- | <span data-ttu-id="a4cad-930">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-930">X</span></span> | <span data-ttu-id="a4cad-931">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-931">X</span></span> | \- | \- |
| <span data-ttu-id="a4cad-932">\_WINHTTP-OPTION \_ GLOBALE \_ SERVERANMELDEINFORMATIONEN \_ \_ VERWENDEN</span><span class="sxs-lookup"><span data-stu-id="a4cad-932">WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS</span></span><br/><span data-ttu-id="a4cad-933">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a4cad-933">**BOOL**</span></span> | <span data-ttu-id="a4cad-934">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-934">X</span></span> | <span data-ttu-id="a4cad-935">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-935">X</span></span> | \- | <span data-ttu-id="a4cad-936">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-936">X</span></span> | \- |
| <span data-ttu-id="a4cad-937">\_BENUTZER-AGENT DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-937">WINHTTP\_OPTION\_USER\_AGENT</span></span><br/><span data-ttu-id="a4cad-938">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="a4cad-938">**LPWSTR**</span></span> | <span data-ttu-id="a4cad-939">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-939">X</span></span> | \- | <span data-ttu-id="a4cad-940">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-940">X</span></span> | <span data-ttu-id="a4cad-941">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-941">X</span></span> | \- |
| <span data-ttu-id="a4cad-942">\_ \_ WINHTTP-OPTIONSBENUTZERNAME</span><span class="sxs-lookup"><span data-stu-id="a4cad-942">WINHTTP\_OPTION\_USERNAME</span></span><br/><span data-ttu-id="a4cad-943">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="a4cad-943">**LPWSTR**</span></span> | \- | <span data-ttu-id="a4cad-944">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-944">X</span></span> | <span data-ttu-id="a4cad-945">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-945">X</span></span> | <span data-ttu-id="a4cad-946">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-946">X</span></span> | \- |
| <span data-ttu-id="a4cad-947">\_WINHTTP-OPTION: \_ \_ TIMEOUT BEIM \_ SCHLIEßEN DES WEBSOCKET \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-947">WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT</span></span><br/><span data-ttu-id="a4cad-948">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-948">**DWORD**</span></span> | \- | \- | <span data-ttu-id="a4cad-949">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-949">X</span></span> | <span data-ttu-id="a4cad-950">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-950">X</span></span> | \- |
| <span data-ttu-id="a4cad-951">WINHTTP-OPTION \_ \_ WEB SOCKET \_ \_ KEEPALIVE \_ INTERVAL</span><span class="sxs-lookup"><span data-stu-id="a4cad-951">WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL</span></span><br/><span data-ttu-id="a4cad-952">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-952">**DWORD**</span></span> | \- | \- | <span data-ttu-id="a4cad-953">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-953">X</span></span> | <span data-ttu-id="a4cad-954">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-954">X</span></span> | \- |
| <span data-ttu-id="a4cad-955">WINHTTP-OPTION \_ \_ \_ WEBSOCKET \_ \_ \_ EMPFANGSPUFFERGRÖßE</span><span class="sxs-lookup"><span data-stu-id="a4cad-955">WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="a4cad-956">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-956">**DWORD**</span></span> | <span data-ttu-id="a4cad-957">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-957">X</span></span> | <span data-ttu-id="a4cad-958">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-958">X</span></span> | <span data-ttu-id="a4cad-959">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-959">X</span></span> | <span data-ttu-id="a4cad-960">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-960">X</span></span> | <span data-ttu-id="a4cad-961">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a4cad-961">Windows 8.1</span></span> |
| <span data-ttu-id="a4cad-962">WINHTTP-OPTION \_ \_ \_ WEBSOCKET- \_ \_ \_ SENDEPUFFERGRÖßE</span><span class="sxs-lookup"><span data-stu-id="a4cad-962">WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="a4cad-963">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-963">**DWORD**</span></span> | <span data-ttu-id="a4cad-964">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-964">X</span></span> | <span data-ttu-id="a4cad-965">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-965">X</span></span> | <span data-ttu-id="a4cad-966">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-966">X</span></span> | <span data-ttu-id="a4cad-967">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-967">X</span></span> | <span data-ttu-id="a4cad-968">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a4cad-968">Windows 8.1</span></span> |
| <span data-ttu-id="a4cad-969">ANZAHL DER \_ \_ ARBEITSTHREADS \_ DER WINHTTP-OPTION \_</span><span class="sxs-lookup"><span data-stu-id="a4cad-969">WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT</span></span><br/><span data-ttu-id="a4cad-970">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-970">**DWORD**</span></span> | \- | \- | \- | <span data-ttu-id="a4cad-971">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-971">X</span></span> | \- |
| <span data-ttu-id="a4cad-972">\_WINHTTP-OPTION: \_ \_ \_ SCHREIBPUFFERGRÖßE</span><span class="sxs-lookup"><span data-stu-id="a4cad-972">WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="a4cad-973">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a4cad-973">**DWORD**</span></span> | \- | <span data-ttu-id="a4cad-974">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-974">X</span></span> | <span data-ttu-id="a4cad-975">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-975">X</span></span> | <span data-ttu-id="a4cad-976">X</span><span class="sxs-lookup"><span data-stu-id="a4cad-976">X</span></span> | \- |

> [!Note]
> <span data-ttu-id="a4cad-977">Informationen zu Windows XP und Windows 2000 finden Sie unter [Laufzeitanforderungen.](winhttp-start-page.md)</span><span class="sxs-lookup"><span data-stu-id="a4cad-977">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4cad-978">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a4cad-978">Requirements</span></span>

| <span data-ttu-id="a4cad-979">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4cad-979">Requirement</span></span> | <span data-ttu-id="a4cad-980">Wert</span><span class="sxs-lookup"><span data-stu-id="a4cad-980">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="a4cad-981">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4cad-981">Minimum supported client</span></span> | <span data-ttu-id="a4cad-982">Nur Windows XP, Windows 2000 Professional mit \[ SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4cad-982">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>            |
| <span data-ttu-id="a4cad-983">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4cad-983">Minimum supported server</span></span> | <span data-ttu-id="a4cad-984">Nur Windows Server 2003, Windows 2000 Server mit \[ SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4cad-984">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>         |
| <span data-ttu-id="a4cad-985">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="a4cad-985">Redistributable</span></span>          | <span data-ttu-id="a4cad-986">WinHTTP 5.0 und Internet Explorer 5.01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a4cad-986">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span> |
| <span data-ttu-id="a4cad-987">Header</span><span class="sxs-lookup"><span data-stu-id="a4cad-987">Header</span></span>                   | <span data-ttu-id="a4cad-988">Winhttp.h</span><span class="sxs-lookup"><span data-stu-id="a4cad-988">Winhttp.h</span></span>                                                                       |

## <a name="see-also"></a><span data-ttu-id="a4cad-989">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4cad-989">See also</span></span>

[<span data-ttu-id="a4cad-990">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="a4cad-990">WinHTTP Versions</span></span>](winhttp-versions.md)
