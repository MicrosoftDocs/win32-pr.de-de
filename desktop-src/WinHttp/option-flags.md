---
Description: Die folgenden Optionsflags werden von WinHttpQueryOption und WinHttpSetOption unterstützt.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Optionsflags (Winhttp.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: f9ca6b7c74d484a6bcac235b2396b2005c8c3260
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386679"
---
# <a name="option-flags"></a><span data-ttu-id="48149-103">Optionsflags</span><span class="sxs-lookup"><span data-stu-id="48149-103">Option Flags</span></span>

<span data-ttu-id="48149-104">Die folgenden Optionsflags werden von [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) und [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="48149-104">The following option flags are supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span>

<dl> <dt>

<span data-ttu-id="48149-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**\_WINHTTP-OPTION \_ GARANTIERT NICHT \_ \_ BLOCKIERENDE \_ RÜCKRUFE**</span><span class="sxs-lookup"><span data-stu-id="48149-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-106">Der Standardwert lautet FALSE.</span><span class="sxs-lookup"><span data-stu-id="48149-106">The default is FALSE.</span></span> <span data-ttu-id="48149-107">Wenn diese Einstellung auf TRUE festgelegt ist, garantiert WinHTTP nicht den Fortschritt, wenn Statusrückrufe von der Clientanwendung blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="48149-107">If set to TRUE, WinHTTP does not guarantee progress if status callbacks are blocked by the client application.</span></span>

<span data-ttu-id="48149-108">Die Clientanwendung muss besonders darauf achten, minimale Vorgänge innerhalb des Rückrufs ohne Blockierung auszuführen, so schnell wie möglich zurückzugeben und insbesondere nicht auf nachfolgende WinHTTP-Aufrufe zu warten.</span><span class="sxs-lookup"><span data-stu-id="48149-108">The client application must take special care to perform minimal operations within the callback without blocking, returning as quickly as possible, and in particular must not wait for any subsequent WinHTTP calls.</span></span> <span data-ttu-id="48149-109">Wenn diese Richtlinien nicht befolgt werden, kann dies negative Auswirkungen auf die Leistung haben oder eine anwendung hängen bleiben.</span><span class="sxs-lookup"><span data-stu-id="48149-109">If it does not follow these guidelines, there is likely to be a negative performance impact or a potential application hang.</span></span> <span data-ttu-id="48149-110">Wenn diese Option auf vorgeschriebene Weise verwendet wird, kann die Leistung verbessert werden.</span><span class="sxs-lookup"><span data-stu-id="48149-110">If used in the prescribed manner, this option may improve performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP \_ OPTION \_ AUTOLOGON \_ POLICY**</span><span class="sxs-lookup"><span data-stu-id="48149-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-112">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Richtlinie für automatische [Anmeldung](authentication-in-winhttp.md) mit einem der folgenden Werte angibt.</span><span class="sxs-lookup"><span data-stu-id="48149-112">Sets an unsigned long integer value that specifies the [Automatic Logon Policy](authentication-in-winhttp.md) with one of the following values.</span></span>

| <span data-ttu-id="48149-113">Begriff</span><span class="sxs-lookup"><span data-stu-id="48149-113">Term</span></span> | <span data-ttu-id="48149-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48149-114">Description</span></span> |
|-|-|
| <span data-ttu-id="48149-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ HIGH</span><span class="sxs-lookup"><span data-stu-id="48149-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH</span></span> | <span data-ttu-id="48149-116">Standardanmeldeinformationen werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="48149-116">Default credentials are not used.</span></span> <span data-ttu-id="48149-117">Beachten Sie, dass dieses Flag nur wirksam wird, wenn Sie den Server anhand des tatsächlichen Computernamens angeben.</span><span class="sxs-lookup"><span data-stu-id="48149-117">Note that this flag takes effect only if you specify the server by the actual machine name.</span></span> <span data-ttu-id="48149-118">Sie wird nicht wirksam, wenn Sie den Server nach "localhost" oder IP-Adresse angeben.</span><span class="sxs-lookup"><span data-stu-id="48149-118">It will not take effect, if you specify the server by "localhost" or IP address.</span></span> |
| <span data-ttu-id="48149-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ LOW</span><span class="sxs-lookup"><span data-stu-id="48149-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW</span></span> | <span data-ttu-id="48149-120">Eine authentifizierte Anmeldung mit den Standardanmeldeinformationen wird für alle Anforderungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="48149-120">An authenticated log on using the default credentials is performed for all requests.</span></span> |
| <span data-ttu-id="48149-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ MEDIUM</span><span class="sxs-lookup"><span data-stu-id="48149-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM</span></span> | <span data-ttu-id="48149-122">Eine authentifizierte Anmeldung mit den Standardanmeldeinformationen wird nur für Anforderungen im lokalen Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="48149-122">An authenticated log on using the default credentials is performed only for requests on the local Intranet.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="48149-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**\_ \_ WINHTTP-OPTIONSRÜCKRUF**</span><span class="sxs-lookup"><span data-stu-id="48149-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-124">Ruft den Zeiger auf die Rückruffunktion ab, die mit [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="48149-124">Retrieves the pointer to the callback function set with [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP \_ OPTION \_ CLIENT \_ CERT \_ CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="48149-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-126">Legt den Clientzertifikatkontext fest.</span><span class="sxs-lookup"><span data-stu-id="48149-126">Sets the client certificate context.</span></span> <span data-ttu-id="48149-127">Wenn eine Anwendung [**ERROR \_ WINHTTP CLIENT \_ \_ AUTH \_ CERT \_ NEEDED**](error-messages.md)empfängt, muss sie [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) aufrufen, um ein Zertifikat anzugeben, bevor die Anforderung erneut versucht wird.</span><span class="sxs-lookup"><span data-stu-id="48149-127">If an application receives [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md), it must call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="48149-128">Im Rahmen der Verarbeitung dieser Option ruft WinHttp [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) für den vom Aufrufer bereitgestellten Zertifikatkontext auf, sodass der Zertifikatkontext unabhängig vom Aufrufer freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="48149-128">As a part of processing this option, WinHttp calls [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) on the caller-provided certificate context so that the certificate context can be independently released by the caller.</span></span>

> [!Note]
> <span data-ttu-id="48149-129">Die Anwendung sollte nicht versuchen, den Zertifikatspeicher mit dem Flag CERT \_ CLOSE STORE FORCE FLAG im Aufruf von \_ \_ \_ [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) für den Zertifikatspeicher zu schließen, aus dem der Zertifikatkontext abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="48149-129">The application should not attempt to close the certificate store with the CERT\_CLOSE\_STORE\_FORCE\_FLAG flag in the call to [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) on the certificate store from which the certificate context was retrieved.</span></span> <span data-ttu-id="48149-130">Es kann zu einer Zugriffsverletzung kommen.</span><span class="sxs-lookup"><span data-stu-id="48149-130">An access violation may occur.</span></span>

<span data-ttu-id="48149-131">Wenn der Server ein Clientzertifikat anfordert, gibt [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)oder [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) einen [**ERROR \_ WINHTTP \_ CLIENT \_ \_ AUTH CERT \_ NEEDED-Fehler**](error-messages.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="48149-131">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md) error.</span></span> <span data-ttu-id="48149-132">Wenn der Server das Zertifikat anfordert, es aber nicht benötigt, kann die Anwendung diese Option angeben, um anzugeben, dass es kein Zertifikat besitzt.</span><span class="sxs-lookup"><span data-stu-id="48149-132">If the server requests the certificate but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="48149-133">Der Server kann ein anderes Authentifizierungsschema auswählen oder anonymen Zugriff auf den Server zulassen.</span><span class="sxs-lookup"><span data-stu-id="48149-133">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="48149-134">Die Anwendung stellt das **WINHTTP \_ NO CLIENT \_ \_ CERT \_ CONTEXT-Makro** im *lpBuffer-Parameter* von [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) bereit, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="48149-134">The application provides the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

<span data-ttu-id="48149-135">Wenn der Server ein Clientzertifikat erfordert, sendet er möglicherweise als Antwort den HTTP-Statuscode 403.</span><span class="sxs-lookup"><span data-stu-id="48149-135">If the server requires a client certificate, it may send a 403 HTTP status code in response.</span></span> <span data-ttu-id="48149-136">Weitere Informationen finden Sie unter der OPTION **WINHTTP \_ OPTION CLIENT \_ \_ CERT ISSUER \_ \_ LIST.**</span><span class="sxs-lookup"><span data-stu-id="48149-136">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP \_ OPTION \_ CLIENT \_ CERT \_ ISSUER \_ LIST**</span><span class="sxs-lookup"><span data-stu-id="48149-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-138">Ruft eine [**SecPkgContext \_ IssuerListInfoEx-Struktur**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) ab, wenn der Fehler von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) oder [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) **ERROR \_ WINHTTP CLIENT \_ \_ \_ AUTH CERT \_ NEEDED** lautet.</span><span class="sxs-lookup"><span data-stu-id="48149-138">Retrieves a [**SecPkgContext\_IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure when the error from [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) is **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="48149-139">Die Ausstellerliste in der -Struktur enthält eine Liste zulässiger Zertifizierungsstellen vom Server.</span><span class="sxs-lookup"><span data-stu-id="48149-139">The issuer list in the structure contains a list of acceptable Certificate Authorities (CA) from the server.</span></span> <span data-ttu-id="48149-140">Die Clientanwendung kann die Liste der Zertifizierungsstellen filtern, um das Clientzertifikat für die SSL-Authentifizierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="48149-140">The client application can filter the CA list to retrieve the client certificate for SSL authentication.</span></span>

<span data-ttu-id="48149-141">Wenn der Server das Clientzertifikat anfordert, es jedoch nicht benötigt, kann die Anwendung [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit der OPTION **WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ CONTEXT** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="48149-141">Alternately, if the server requests the client certificate, but does not require it, the application can call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="48149-142">Weitere Informationen finden Sie unter der OPTION **WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ CONTEXT.**</span><span class="sxs-lookup"><span data-stu-id="48149-142">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP \_ OPTION \_ CODEPAGE**</span><span class="sxs-lookup"><span data-stu-id="48149-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-144">Legt die [*Codepage*](glossary.md) fest, die zum Verarbeiten der URL verwendet wird (d.b. Abfragezeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="48149-144">Sets the [*code page*](glossary.md) that is used to process the URL (that is, query string).</span></span> <span data-ttu-id="48149-145">Der Standardwert ist UTF8.</span><span class="sxs-lookup"><span data-stu-id="48149-145">The default is UTF8.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_WINHTTP-OPTION \_ : KONFIGURIEREN DER \_ \_ PASSPORT-AUTHENTIFIZIERUNG**</span><span class="sxs-lookup"><span data-stu-id="48149-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-147">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, ob die [Passport-Authentifizierung in der WinHTTP-Authentifizierung](passport-authentication-in-winhttp.md) aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="48149-147">Sets an unsigned long integer value that specifies whether [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md) authentication is enabled.</span></span> <span data-ttu-id="48149-148">Der Wert kann in folgenden Formen vorliegen:</span><span class="sxs-lookup"><span data-stu-id="48149-148">The value can be one of the following:</span></span>

| <span data-ttu-id="48149-149">Begriff</span><span class="sxs-lookup"><span data-stu-id="48149-149">Term</span></span> | <span data-ttu-id="48149-150">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48149-150">Description</span></span> |
|-|-|
| <span data-ttu-id="48149-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>\_WINHTTP: DEAKTIVIEREN DER \_ \_ PASSPORT-AUTHENTIFIZIERUNG</span><span class="sxs-lookup"><span data-stu-id="48149-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP\_DISABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="48149-152">Microsoft Passport Authentifizierung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="48149-152">Microsoft Passport authentication is disabled.</span></span> <span data-ttu-id="48149-153">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="48149-153">This is the default.</span></span> |
| <span data-ttu-id="48149-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>\_WINHTTP: DEAKTIVIEREN DES \_ \_ PASSPORT-SCHLÜSSELBUNDS</span><span class="sxs-lookup"><span data-stu-id="48149-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP\_DISABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="48149-155">Der Passport-Schlüsselbund ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="48149-155">The Passport keyring is disabled.</span></span> <span data-ttu-id="48149-156">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="48149-156">This is the default.</span></span> |
| <span data-ttu-id="48149-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ AUTH</span><span class="sxs-lookup"><span data-stu-id="48149-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP\_ENABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="48149-158">Die Passport-Authentifizierung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="48149-158">Passport authentication is enabled.</span></span> |
| <span data-ttu-id="48149-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ KEYRING</span><span class="sxs-lookup"><span data-stu-id="48149-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP\_ENABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="48149-160">Der Passport-Schlüsselbund ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="48149-160">The Passport keyring is enabled.</span></span> |

</dl> </dd> <dt>

<span data-ttu-id="48149-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP \_ OPTION \_ \_ CONNECT-WIEDERHOLUNGEN**</span><span class="sxs-lookup"><span data-stu-id="48149-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-162">Legt einen ganzzahligen Wert ohne Vorzeichen fest oder ruft diesen ab, der die Anzahl der Versuche vonWinHTTP enthält, eine Verbindung mit einem Host herzustellen.</span><span class="sxs-lookup"><span data-stu-id="48149-162">Sets or retrieves an unsigned long integer value that contains the number of timesWinHTTP attempts to connect to a host.</span></span> <span data-ttu-id="48149-163">Microsoft Windows HTTP Services (WinHTTP) versucht nur einmal pro IP-Adresse (Internetprotokoll).</span><span class="sxs-lookup"><span data-stu-id="48149-163">Microsoft Windows HTTP Services (WinHTTP) only attempts once per Internet Protocol (IP) address.</span></span> <span data-ttu-id="48149-164">Wenn Sie beispielsweise versuchen, eine Verbindung mit einem mehrfach vernetzten Host herzustellen, der über 10 IP-Adressen verfügt, und **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** auf 7 festgelegt ist, versucht WinHTTP nur, eine Verbindung mit den ersten sieben IP-Adressen herzustellen.</span><span class="sxs-lookup"><span data-stu-id="48149-164">For example, if you attempt to connect to a multihomed host that has 10 IP addresses and **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 7, then WinHTTP only attempts to connect to the first seven IP address.</span></span> <span data-ttu-id="48149-165">Wenn **winHTTP \_ OPTION CONNECT \_ \_ RETRIES** auf 20 festgelegt ist, versucht WinHTTP bei gleichem Satz von 10 IP-Adressen jede der 10 nur einmal.</span><span class="sxs-lookup"><span data-stu-id="48149-165">Given the same set of 10 IP addresses, if **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 20, WinHTTP attempts each of the 10 only once.</span></span> <span data-ttu-id="48149-166">Wenn ein Verbindungsversuch nach der angegebenen Anzahl von Versuchen weiterhin fehlschlägt oder das Verbindungstimeout vor diesem Zeitpunkt abgelaufen ist, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="48149-166">If a connection attempt still fails after the specified number of attempts, or if the connect timeout expired before then, the request is canceled.</span></span> <span data-ttu-id="48149-167">Der Standardwert für **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** beträgt fünf Versuche.</span><span class="sxs-lookup"><span data-stu-id="48149-167">The default value for **WINHTTP\_OPTION\_CONNECT\_RETRIES** is five attempts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP \_ OPTION \_ CONNECT \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="48149-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-169">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="48149-169">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds.</span></span> <span data-ttu-id="48149-170">Wenn Sie diese Option auf infinite (0xFFFFFFFF) festlegen, wird dieser Timer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="48149-170">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="48149-171">Wenn eine TCP-Verbindungsanforderung länger als dieser Time out-Wert dauert, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="48149-171">If a TCP connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="48149-172">Das Standardtimeout beträgt 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="48149-172">The default timeout is 60 seconds.</span></span> <span data-ttu-id="48149-173">Wenn Sie versuchen, eine Verbindung mit mehreren IP-Adressen für einen einzelnen Host (einen mehrfach vernetzten Host) herzustellen, gilt das Timeoutlimit für jede einzelne Verbindung.</span><span class="sxs-lookup"><span data-stu-id="48149-173">When you are attempting to connect to multiple IP addresses for a single host (a multihomed host), the timeout limit is for each individual connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**VERBINDUNGSINFORMATIONEN ZUR \_ WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48149-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP\_OPTION\_CONNECTION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-175">Ruft die Quell- und Ziel-IP-Adresse sowie den Port der Anforderung ab, die die Antwort generiert hat, wenn [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="48149-175">Retrieves the source and destination IP address, and port of the request that generated the response when [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns.</span></span> <span data-ttu-id="48149-176">Die Anwendung ruft [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) mit der OPTION **WINHTTP \_ OPTION CONNECTION \_ \_ INFO** auf und stellt die [**WINHTTP CONNECTION \_ \_ INFO-Struktur**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) im *lpBuffer-Parameter* bereit.</span><span class="sxs-lookup"><span data-stu-id="48149-176">The application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CONNECTION\_INFO** option, and provides the [**WINHTTP\_CONNECTION\_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) structure in the *lpBuffer* parameter.</span></span> <span data-ttu-id="48149-177">Weitere Informationen finden Sie unter **WINHTTP \_ CONNECTION \_ INFO**.</span><span class="sxs-lookup"><span data-stu-id="48149-177">For more information, see **WINHTTP\_CONNECTION\_INFO**.</span></span>

<span data-ttu-id="48149-178">**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="48149-178">**Windows Server 2003 with SP1 and Windows XP with SP2:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V0**</span><span class="sxs-lookup"><span data-stu-id="48149-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V0**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-180">Leitet die [**TCP \_ INFO \_ v0-Struktur**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) für die zugrunde liegende Verbindung ab, die von der Anforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="48149-180">Retreives the [**TCP\_INFO\_v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="48149-181">Die zurückgegebene Struktur kann Statistiken aus früheren Anforderungen enthalten, die über dieselbe Verbindung gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="48149-181">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>

> [!Note]
> <span data-ttu-id="48149-182">Diese Option wurde durch **WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="48149-182">This option has been superseded by **WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1**</span><span class="sxs-lookup"><span data-stu-id="48149-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-184">Leitet die [**TCP \_ INFO \_ v1-Struktur**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) für die zugrunde liegende Verbindung ab, die von der Anforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="48149-184">Retreives the [**TCP\_INFO\_v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="48149-185">Die zurückgegebene Struktur kann Statistiken aus früheren Anforderungen enthalten, die über dieselbe Verbindung gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="48149-185">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**\_ \_ WINHTTP-OPTIONSKONTEXTWERT \_**</span><span class="sxs-lookup"><span data-stu-id="48149-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-187">Legt einen **\_ DWORD-PTR** fest oder ruft diesen ab, der einen Zeiger auf den Kontextwert enthält, der diesem [HINTERNET-Handle](hinternet-handles-in-winhttp.md) zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="48149-187">Sets or retrieves a **DWORD\_PTR** that contains a pointer to the context value associated with this [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span> <span data-ttu-id="48149-188">Der im Puffer gespeicherte Wert wird verwendet, und dem **Optionsflag WINHTTP \_ OPTION CONTEXT \_ \_ VALUE** wird ein neuer Wert zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="48149-188">The value stored in the buffer is used and the **WINHTTP\_OPTION\_CONTEXT\_VALUE** option flag is assigned a new value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP \_ OPTION \_ DEKOMPRIMIERUNG**</span><span class="sxs-lookup"><span data-stu-id="48149-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP\_OPTION\_DECOMPRESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-190">Legt ein DWORD mit Flags fest, die bestimmen, ob WinHTTP Antwortkörper mit komprimierten Inhaltscodierungen automatisch dekomprimiert.</span><span class="sxs-lookup"><span data-stu-id="48149-190">Sets a DWORD of flags which determine whether WinHTTP will automatically decompress response bodies with compressed Content-Encodings.</span></span> <span data-ttu-id="48149-191">WinHTTP legt auch einen geeigneten Accept-Encoding-Header fest, der alle vom Aufrufer bereitgestellten überschreibt.</span><span class="sxs-lookup"><span data-stu-id="48149-191">WinHTTP will also set an appropriate Accept-Encoding header, overriding any supplied by the caller.</span></span> <span data-ttu-id="48149-192">Diese Werte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="48149-192">Supported values are:</span></span>

| <span data-ttu-id="48149-193">Begriff</span><span class="sxs-lookup"><span data-stu-id="48149-193">Term</span></span> | <span data-ttu-id="48149-194">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48149-194">Description</span></span> |
|-|-|
| <span data-ttu-id="48149-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP \_ DECOMPRESSION \_ FLAG \_ GZIP</span><span class="sxs-lookup"><span data-stu-id="48149-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP\_DECOMPRESSION\_FLAG\_GZIP</span></span> | <span data-ttu-id="48149-196">Dekomprimieren von Content-Encoding: gzip-Antworten.</span><span class="sxs-lookup"><span data-stu-id="48149-196">Decompress Content-Encoding: gzip responses.</span></span> |
| <span data-ttu-id="48149-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP \_ DECOMPRESSION \_ FLAG \_ DEFLATE</span><span class="sxs-lookup"><span data-stu-id="48149-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP\_DECOMPRESSION\_FLAG\_DEFLATE</span></span> | <span data-ttu-id="48149-198">Dekomprimieren der Inhaltscodierung: Deflate-Antworten.</span><span class="sxs-lookup"><span data-stu-id="48149-198">Decompress Content-Encoding: deflate responses.</span></span> |
| <span data-ttu-id="48149-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP \_ DECOMPRESSION \_ FLAG \_ ALL</span><span class="sxs-lookup"><span data-stu-id="48149-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP\_DECOMPRESSION\_FLAG\_ALL</span></span> | <span data-ttu-id="48149-200">Dekomprimieren Sie Antworten mit jeder unterstützten Inhaltscodierung.</span><span class="sxs-lookup"><span data-stu-id="48149-200">Decompress responses with any supported Content-Encoding.</span></span> |

<span data-ttu-id="48149-201">Standardmäßig liefert WinHTTP komprimierte Antworten unverändert an den Aufrufer.</span><span class="sxs-lookup"><span data-stu-id="48149-201">By default, WinHTTP will deliver compressed responses to the caller unmodified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**FUNKTION \_ "WINHTTP-OPTION \_ \_ DEAKTIVIEREN"**</span><span class="sxs-lookup"><span data-stu-id="48149-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP\_OPTION\_DISABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-203">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, welche Features mit mindestens einem der folgenden Flags deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="48149-203">Sets an unsigned long integer value that specifies which features are disabled with one or more of the following flags.</span></span> <span data-ttu-id="48149-204">Beachten Sie, dass dieses Feature nur bei Anforderungshandles an [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) übergeben werden sollte, nachdem das Anforderungshandles mit [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellt wurde und bevor die Anforderung mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="48149-204">Be aware that this feature should only be passed to [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) on request handles after the request handle is created with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), and before the request is sent with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

| <span data-ttu-id="48149-205">Begriff</span><span class="sxs-lookup"><span data-stu-id="48149-205">Term</span></span> | <span data-ttu-id="48149-206">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48149-206">Description</span></span> |
|-|-|
| <span data-ttu-id="48149-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP \_ DISABLE \_ AUTHENTICATION</span><span class="sxs-lookup"><span data-stu-id="48149-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP\_DISABLE\_AUTHENTICATION</span></span> | <span data-ttu-id="48149-208">Die automatische Authentifizierung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="48149-208">Automatic authentication is disabled.</span></span> |
| <span data-ttu-id="48149-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP \_ DEAKTIVIEREN VON \_ COOKIES</span><span class="sxs-lookup"><span data-stu-id="48149-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP\_DISABLE\_COOKIES</span></span> | <span data-ttu-id="48149-210">Das automatische Hinzufügen von Cookieheadern zu Anforderungen ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="48149-210">Automatic addition of cookie headers to requests is disabled.</span></span> <span data-ttu-id="48149-211">Außerdem werden zurückgegebene Cookies nicht automatisch zur Cookiedatenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="48149-211">Also, returned cookies are not automatically added to the cookie database.</span></span> <span data-ttu-id="48149-212">Das Deaktivieren von Cookies kann zu einer schlechten Leistung bei der Passport-Authentifizierung führen.</span><span class="sxs-lookup"><span data-stu-id="48149-212">Disabling cookies can result in poor performance for Passport authentication.</span></span> |
| <span data-ttu-id="48149-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ DISABLE \_ KEEP \_ ALIVE</span><span class="sxs-lookup"><span data-stu-id="48149-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP\_DISABLE\_KEEP\_ALIVE</span></span> | <span data-ttu-id="48149-214">Deaktiviert die Keep-Alive-Semantik für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="48149-214">Disables keep-alive semantics for the connection.</span></span> <span data-ttu-id="48149-215">Keep-Alive-Semantik ist für MSN, NTLM und andere Authentifizierungstypen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="48149-215">Keep-alive semantics are required for MSN, NTLM, and other types of authentication.</span></span> |
| <span data-ttu-id="48149-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>\_WINHTTP: DEAKTIVIEREN \_ VON UMLEITUNGEN</span><span class="sxs-lookup"><span data-stu-id="48149-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP\_DISABLE\_REDIRECTS</span></span> | <span data-ttu-id="48149-217">Die automatische Umleitung ist deaktiviert, wenn Anforderungen mit [**WinHttpSendRequest gesendet werden.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="48149-217">Automatic redirection is disabled when sending requests with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="48149-218">Wenn die automatische Umleitung deaktiviert ist, muss eine Anwendung eine Rückruffunktion registrieren, damit die Passport-Authentifizierung erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="48149-218">If automatic redirection is disabled, an application must register a callback function in order for Passport authentication to succeed.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="48149-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**\_WINHTTP-OPTION: \_ DEAKTIVIEREN DES \_ \_ \_ FALLBACKS DES SICHEREN PROTOKOLLS**</span><span class="sxs-lookup"><span data-stu-id="48149-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-220">Verhindert, dass WinHTTP eine Verbindung mit einer niedrigeren Version des Sicherheitsprotokolls erneut versucht, wenn die anfängliche Protokollaushandlung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="48149-220">Prevents WinHTTP from retrying a connection with a lower version of the security protocol when the initial protocol negotiation fails.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP-OPTION \_ \_ \_ STREAMWARTESCHLANGE \_ DEAKTIVIEREN**</span><span class="sxs-lookup"><span data-stu-id="48149-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-222">Ermöglicht es neuen Anforderungen, eine zusätzliche HTTP/2-Verbindung zu öffnen, wenn die maximale Anzahl gleichzeitiger Streams erreicht ist, anstatt auf den nächsten verfügbaren Stream für eine vorhandene Verbindung zu warten.</span><span class="sxs-lookup"><span data-stu-id="48149-222">Allows new requests to open an additional HTTP/2 connection when the maximum concurrent stream limit is reached, rather than waiting for the next available stream on an existing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**FEATURE \_ "WINHTTP-OPTION \_ \_ AKTIVIEREN"**</span><span class="sxs-lookup"><span data-stu-id="48149-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP\_OPTION\_ENABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-224">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die derzeit aktivierten Funktionen angibt.</span><span class="sxs-lookup"><span data-stu-id="48149-224">Sets an unsigned long integer value that specifies the features currently enabled.</span></span> <span data-ttu-id="48149-225">Kann einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="48149-225">Can be one of the following values.</span></span>

| <span data-ttu-id="48149-226">Begriff</span><span class="sxs-lookup"><span data-stu-id="48149-226">Term</span></span> | <span data-ttu-id="48149-227">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48149-227">Description</span></span> |
|-|-|
| <span data-ttu-id="48149-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVERT \_ IMPERSONATION</span><span class="sxs-lookup"><span data-stu-id="48149-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP\_ENABLE\_SSL\_REVERT\_IMPERSONATION</span></span> | <span data-ttu-id="48149-229">Wenn diese Option aktiviert ist, wird der Clientwechsel von WinHTTP vorübergehend für die Dauer von SSL-Zertifikatauthentifizierungsvorgängen rückgängig machen.</span><span class="sxs-lookup"><span data-stu-id="48149-229">If enabled, WinHTTP temporarily reverts client impersonation for the duration of SSL certificate authentication operations.</span></span> <span data-ttu-id="48149-230">Dieser Wert kann nur für das Sitzungshand handle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="48149-230">This value can be set only on the session handle.</span></span> |
| <span data-ttu-id="48149-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVOCATION</span><span class="sxs-lookup"><span data-stu-id="48149-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP\_ENABLE\_SSL\_REVOCATION</span></span> | <span data-ttu-id="48149-232">Wenn diese Option aktiviert ist, lässt WinHTTP SSL-Sperrvorgänge zu.</span><span class="sxs-lookup"><span data-stu-id="48149-232">If enabled, WinHTTP allows SSL revocation.</span></span> <span data-ttu-id="48149-233">Dieser Wert kann nur für das Anforderungshand handle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="48149-233">This value can be set only on the request handle.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP-OPTION \_ \_ \_ HTTP-PROTOKOLL \_ AKTIVIEREN**</span><span class="sxs-lookup"><span data-stu-id="48149-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-235">Legt eine DWORD-Bitmaske zulässiger erweiterter HTTP-Versionen fest.</span><span class="sxs-lookup"><span data-stu-id="48149-235">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="48149-236">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="48149-236">Possible values are:</span></span>

| <span data-ttu-id="48149-237">Begriff</span><span class="sxs-lookup"><span data-stu-id="48149-237">Term</span></span> | <span data-ttu-id="48149-238">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48149-238">Description</span></span> |
|-|-|
| <span data-ttu-id="48149-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>\_ \_ WINHTTP-PROTOKOLLFLAG \_ HTTP2 (0x1)</span><span class="sxs-lookup"><span data-stu-id="48149-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP\_PROTOCOL\_FLAG\_HTTP2 (0x1)</span></span> | <span data-ttu-id="48149-240">Aktiviert HTTP/2 für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="48149-240">Enables HTTP/2 for the request.</span></span> |
| <span data-ttu-id="48149-241">Keine (0x0)</span><span class="sxs-lookup"><span data-stu-id="48149-241">None (0x0)</span></span> | <span data-ttu-id="48149-242">Schränkt die Anforderung auf HTTP/1.1 und früher ein.</span><span class="sxs-lookup"><span data-stu-id="48149-242">Restricts the request to HTTP/1.1 and prior.</span></span> |

<span data-ttu-id="48149-243">Ältere Versionen von HTTP (1.1 und früher) können mit dieser Option nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="48149-243">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="48149-244">Der Standardwert ist 0x0.</span><span class="sxs-lookup"><span data-stu-id="48149-244">The default is 0x0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-245"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**\_WINHTTP-OPTION \_ ENABLETRACING**</span><span class="sxs-lookup"><span data-stu-id="48149-245"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP\_OPTION\_ENABLETRACING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-246">Legt einen **BOOL-Wert** fest, der angibt, ob die Ablaufverfolgung derzeit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="48149-246">Sets a **BOOL** value that specifies whether tracing is currently enabled.</span></span> <span data-ttu-id="48149-247">Weitere Informationen zur Ablaufverfolgungseinrichtung in WinHTTP finden Sie unter [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="48149-247">For more information about the trace facility in WinHTTP, see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span> <span data-ttu-id="48149-248">Diese Option kann nur für ein **NULL** **HINTERNET-Handle festgelegt** werden.</span><span class="sxs-lookup"><span data-stu-id="48149-248">This option can only be set on a **NULL** **HINTERNET** handle.</span></span>


</dt> </dl> </dd>

<dt>

<span data-ttu-id="48149-249"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP \_ OPTION \_ ENCODE \_ EXTRA**</span><span class="sxs-lookup"><span data-stu-id="48149-249"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-250">Aktiviert die URL-Prozentcodierung für Pfad und Abfragezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="48149-250">Enables URL percent encoding for path and query string.</span></span>

<span data-ttu-id="48149-251">Alternativ können Sie vor dem Aufrufen von WinHttp prozentweise codieren.</span><span class="sxs-lookup"><span data-stu-id="48149-251">Alternatively, you can percent encode before calling WinHttp.</span></span>

</dt> </dl> </dd>

<dt>

<span data-ttu-id="48149-252"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP-OPTION \_ \_ VERBINDUNG \_ ABLAUFEN**</span><span class="sxs-lookup"><span data-stu-id="48149-252"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP\_OPTION\_EXPIRE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-253">Diese Option kann nur für ein Anforderungshand handle festgelegt werden, das noch aktiv ist (senden oder empfangen).</span><span class="sxs-lookup"><span data-stu-id="48149-253">This option can only be set on a request handle which is still active (sending or receiving).</span></span> <span data-ttu-id="48149-254">Wenn Sie diese Option festlegen, wird WinHttp dazu veranschlagen, die Verarbeiten von Anforderungen für die Verbindung zu beenden, die dem übergebenen Anforderungshand handle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="48149-254">Setting this option will tell WinHttp to stop serving requests on the connection associated with the request handle passed in.</span></span> <span data-ttu-id="48149-255">Die Verbindung wird geschlossen, nachdem das Anforderungshand handle, mit dem diese Option aufgerufen wird, abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="48149-255">The connection will be closed after the request handle this option is called with is completed.</span></span> <span data-ttu-id="48149-256">Bei dieser Option werden keine Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="48149-256">This option does not take any parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-257"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**ERWEITERTER FEHLER \_ DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48149-257"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-258">Ruft einen ganzzahligen Wert ohne Vorzeichen ab, der einen Microsoft Windows Sockets-Fehlercode enthält, der den ZULETZT in diesem Threadkontext zurückgegebenen \_ ERROR WINHTTP-Fehlermeldungen \_ \* zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="48149-258">Retrieves an unsigned long integer value that contains a Microsoft Windows Sockets error code that was mapped to the ERROR\_WINHTTP\_\* error messages last returned in this thread context.</span></span> <span data-ttu-id="48149-259">Sie können **NULL als** Handlewert übergeben.</span><span class="sxs-lookup"><span data-stu-id="48149-259">You can pass **NULL** as the handle value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-260"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**GLOBALE \_ PROXY-ANMELDEINFORMATIONEN FÜR DIE \_ \_ \_ WINHTTP-OPTION**</span><span class="sxs-lookup"><span data-stu-id="48149-260"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-261">Verwendet einen Zeiger auf eine [**WINHTTP \_ CREDS \_ EX-Struktur,**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) bei der der *hInternet-Funktionsparameter* auf **NULL festgelegt ist.**</span><span class="sxs-lookup"><span data-stu-id="48149-261">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="48149-262">Diese Option erfordert den Registrierungsschlüssel **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="48149-262">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="48149-263">Wenn dieser Registrierungsschlüssel nicht festgelegt ist, gibt WinHTTP den Fehler **\_ ERROR WINHTTP INVALID OPTION \_ \_ zurück.**</span><span class="sxs-lookup"><span data-stu-id="48149-263">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="48149-264">Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="48149-264">This registry key is not present by default.</span></span> <span data-ttu-id="48149-265">Wenn sie festgelegt ist, sendet WinINet Anmeldeinformationen an WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="48149-265">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="48149-266">Wenn WinHttp eine Authentifizierungsforderung erhält und keine Anmeldeinformationen für das aktuelle Handle festgelegt sind, werden die von WinINet bereitgestellten Anmeldeinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="48149-266">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="48149-267">Um Serveranmeldeinformationen zusätzlich zu Proxyanmeldeinformationen gemeinsam zu verwenden, müssen Benutzer **WINHTTP \_ OPTION USE GLOBAL SERVER CREDENTIALS \_ \_ \_ (GLOBALE SERVERANMELDEINFORMATIONEN \_ VERWENDEN) festlegen.**</span><span class="sxs-lookup"><span data-stu-id="48149-267">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-268"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**\_WINHTTP-OPTION \_ : GLOBALE \_ \_ SERVER-ANMELDEINFORMATIONEN**</span><span class="sxs-lookup"><span data-stu-id="48149-268"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-269">Verwendet einen Zeiger auf eine [**WINHTTP \_ CREDS \_ EX-Struktur,**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) bei der der *hInternet-Funktionsparameter* auf **NULL festgelegt ist.**</span><span class="sxs-lookup"><span data-stu-id="48149-269">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="48149-270">Diese Option erfordert den Registrierungsschlüssel **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="48149-270">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="48149-271">Wenn dieser Registrierungsschlüssel nicht festgelegt ist, gibt WinHTTP den Fehler **\_ ERROR WINHTTP INVALID OPTION \_ \_ zurück.**</span><span class="sxs-lookup"><span data-stu-id="48149-271">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="48149-272">Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="48149-272">This registry key is not present by default.</span></span> <span data-ttu-id="48149-273">Wenn sie festgelegt ist, sendet WinINet Anmeldeinformationen an WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="48149-273">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="48149-274">Wenn WinHttp eine Authentifizierungsforderung erhält und keine Anmeldeinformationen für das aktuelle Handle festgelegt sind, werden die von WinINet bereitgestellten Anmeldeinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="48149-274">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="48149-275">Um Serveranmeldeinformationen zusätzlich zu Proxyanmeldeinformationen gemeinsam zu verwenden, müssen Benutzer **WINHTTP \_ OPTION USE GLOBAL SERVER CREDENTIALS \_ \_ \_ (GLOBALE SERVERANMELDEINFORMATIONEN \_ VERWENDEN) festlegen.**</span><span class="sxs-lookup"><span data-stu-id="48149-275">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-276"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**HANDLETYP \_ DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48149-276"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-277">Ruft einen ganzzahligen Wert ohne Vorzeichen ab, der den Typ des übergebenen [HINTERNET-Handles](hinternet-handles-in-winhttp.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="48149-277">Retrieves an unsigned long integer value that contains the type of the [HINTERNET](hinternet-handles-in-winhttp.md) handle passed in.</span></span> <span data-ttu-id="48149-278">Einer der folgenden Werte kann zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="48149-278">The return value can be one of the following:</span></span>

| <span data-ttu-id="48149-279">Begriff</span><span class="sxs-lookup"><span data-stu-id="48149-279">Term</span></span> | <span data-ttu-id="48149-280">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48149-280">Description</span></span> |
|-|-|
| <span data-ttu-id="48149-281"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP \_ HANDLE \_ TYPE \_ CONNECT</span><span class="sxs-lookup"><span data-stu-id="48149-281"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP\_HANDLE\_TYPE\_CONNECT</span></span> | <span data-ttu-id="48149-282">Das Handle ist ein Verbindungshand handle.</span><span class="sxs-lookup"><span data-stu-id="48149-282">The handle is a connection handle.</span></span> |
| <span data-ttu-id="48149-283"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>\_ \_ WINHTTP-HANDLETYPANFORDERUNG \_</span><span class="sxs-lookup"><span data-stu-id="48149-283"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP\_HANDLE\_TYPE\_REQUEST</span></span> | <span data-ttu-id="48149-284">Das Handle ist ein Anforderungshand handle.</span><span class="sxs-lookup"><span data-stu-id="48149-284">The handle is a request handle.</span></span> |
| <span data-ttu-id="48149-285"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>SITZUNG MIT \_ \_ WINHTTP-HANDLETYP \_</span><span class="sxs-lookup"><span data-stu-id="48149-285"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP\_HANDLE\_TYPE\_SESSION</span></span> | <span data-ttu-id="48149-286">Das Handle ist ein Sitzungshand handle.</span><span class="sxs-lookup"><span data-stu-id="48149-286">The handle is a session handle.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="48149-287"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**\_WINHTTP-OPTION \_ \_ HTTP-PROTOKOLL \_ ERFORDERLICH**</span><span class="sxs-lookup"><span data-stu-id="48149-287"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-288">Verhindert, dass andere Protokollversionen als die von **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL** aktivierten für die Anforderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48149-288">Prevents protocol versions other than those enabled by **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL** from being used for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-289"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**VERWENDETES \_ \_ HTTP-PROTOKOLL DER \_ WINHTTP-OPTION \_**</span><span class="sxs-lookup"><span data-stu-id="48149-289"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-290">Ruft ein DWORD ab, das angibt, welche erweiterte HTTP-Version für eine bestimmte Anforderung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="48149-290">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="48149-291">Eine Liste der möglichen Werte finden Sie unter **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL**.</span><span class="sxs-lookup"><span data-stu-id="48149-291">For a list of possible values, see **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-292"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**\_HTTP-VERSION DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48149-292"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-293">Legt eine HTTP-VERSIONSINFORMATIONsstruktur fest, die die unterstützte HTTP-Version enthält, oder ruft sie ab. [**\_ \_**](/windows/win32/api/winhttp/ns-winhttp-http_version_info)</span><span class="sxs-lookup"><span data-stu-id="48149-293">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) structure that contains the HTTP version being supported.</span></span> <span data-ttu-id="48149-294">Dies ist eine prozessweite Option. Verwenden **Sie NULL** für das Handle.</span><span class="sxs-lookup"><span data-stu-id="48149-294">This is a process-wide option; use **NULL** for the handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-295"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP-OPTION \_ \_ \_ ZERTIFIKATSPERRUNG \_ \_ OFFLINE IGNORIEREN**</span><span class="sxs-lookup"><span data-stu-id="48149-295"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-296">Ermöglicht sicheren Verbindungen die Verwendung von Sicherheitszertifikaten, für die die Zertifikatsperrliste nicht heruntergeladen werden konnte.</span><span class="sxs-lookup"><span data-stu-id="48149-296">Allows secure connections to use security certificates for which the certificate revocation list could not be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-297"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP-OPTION \_ \_ IPV6 \_ – SCHNELLER \_ FALLBACK**</span><span class="sxs-lookup"><span data-stu-id="48149-297"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-298">Aktiviert schnelles IPv6-Fallback (Brillenbrillen) für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="48149-298">Enables IPv6 fast fallback (Happier Eyeballs) for the connection.</span></span> <span data-ttu-id="48149-299">Dieses Verhalten ähnelt dem In RFC [6555](https://tools.ietf.org/html/rfc6555) beschriebenen Verhalten von Happy Eyeballs zur Verbesserung der Verbindungszeiten in Netzwerken, in denen IPv6 unzuverlässig ist.</span><span class="sxs-lookup"><span data-stu-id="48149-299">This behavior is similar to the Happy Eyeballs behavior described in [RFC 6555](https://tools.ietf.org/html/rfc6555) for improving connection times on networks where IPv6 is unreliable.</span></span>
- <span data-ttu-id="48149-300">Wenn sowohl IPv6- als auch IPv4-Adressen für einen bestimmten Host aufgelöst werden, beginnt WinHttp mit dem Herstellen einer Verbindung mit der ersten aufgelösten IPv6-Adresse mit einem kurzen Timeout (300 ms).</span><span class="sxs-lookup"><span data-stu-id="48149-300">If both IPv6 and IPv4 addresses are resolved for a given host, WinHttp will begin by connecting to the first resolved IPv6 address with a short (300ms) timeout.</span></span>
- <span data-ttu-id="48149-301">Sollte diese Verbindung fehlschlagen, versucht WinHttp, eine Verbindung mit der ersten aufgelösten IPv4-Adresse mit dem Standardtimeout herzustellen.</span><span class="sxs-lookup"><span data-stu-id="48149-301">Should that connection fail, WinHttp will attempt to connect to the first resolved IPv4 address with the standard timeout.</span></span>
- <span data-ttu-id="48149-302">Wenn die zweite Verbindung fehlschlägt, versucht WinHttp erneut, die erste aufgelöste IPv6-Adresse mit dem Standardtimeout zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="48149-302">Should the second connection fail, WinHttp will retry the first resolved IPv6 address with the standard timeout.</span></span>
- <span data-ttu-id="48149-303">Sollte bei der dritten Verbindung ein Fehler auftreten, wird winHttp auf das Standardverhalten für alle verbleibenden Adressen zurückgesetzt, wobei versucht wird, eine Verbindung mit jeder Adresse mit dem Standardtimeout herzustellen, bis eine Verbindung hergestellt wird oder keine Adressen mehr vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="48149-303">Should the third connection fail, WinHttp will revert to the default behavior for any remaining addresses, attempting a connection to each one with the standard timeout until a connection is made or no addresses remain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-304"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**\_WINHTTP-OPTION: \_ \_ PROXY \_ \_ CONNECT-ANTWORT**</span><span class="sxs-lookup"><span data-stu-id="48149-304"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-305">Ruft ab, ob eine Proxy Return Connect-Antwort abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="48149-305">Gets whether or not a Proxy Return Connect Response can be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-306"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP \_ OPTION \_ \_ MAX. CONNS \_ PRO \_ 1 \_ 0 \_ SERVER**</span><span class="sxs-lookup"><span data-stu-id="48149-306"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-307">Legt einen ganzzahligen Wert ohne Vorzeichen fest oder ruft diesen ab, der die maximale Anzahl von Verbindungen enthält, die pro HTTP/1.0-Server zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="48149-307">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="48149-308">Der Standardwert ist **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="48149-308">The default value is **INFINITE**.</span></span>

<span data-ttu-id="48149-309">**Windows Vista mit SP1 und Windows Server 2008:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="48149-309">**Windows Vista with SP1 and Windows Server 2008:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-310"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP \_ OPTION \_ \_ MAX. CONNS \_ PRO \_ SERVER**</span><span class="sxs-lookup"><span data-stu-id="48149-310"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-311">Legt einen ganzzahligen Wert ohne Vorzeichen fest oder ruft diesen ab, der die maximale Anzahl der pro Server zulässigen Verbindungen enthält.</span><span class="sxs-lookup"><span data-stu-id="48149-311">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="48149-312">Der Standardwert ist **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="48149-312">The default value is **INFINITE**.</span></span>

<span data-ttu-id="48149-313">Wenn diese Option auf 0 (null) festgelegt ist, legt WinHTTP den Grenzwert für die Anzahl der Verbindungen auf 2 fest.</span><span class="sxs-lookup"><span data-stu-id="48149-313">When this option is set to zero, WinHTTP sets the limit on the number of connections to 2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-314"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP \_ OPTION \_ \_ MAX. AUTOMATISCHE HTTP-UMLEITUNGEN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48149-314"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-315">Legt die maximale Anzahl von Umleitungen fest, denen WinHTTP folgt. der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="48149-315">Sets the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="48149-316">Dieser Grenzwert verhindert, dass nicht autorisierte Websites den WinHTTP-Client nach einer großen Anzahl von Umleitungen anhalten.</span><span class="sxs-lookup"><span data-stu-id="48149-316">This limit prevents unauthorized sites from making the WinHTTP client pause following a large number of redirects.</span></span>

<span data-ttu-id="48149-317">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="48149-317">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-318"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP \_ OPTION \_ MAX \_ HTTP \_ STATUS \_ CONTINUE**</span><span class="sxs-lookup"><span data-stu-id="48149-318"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-319">Die maximale Anzahl von Informational 100-199-Statuscodeantworten, die ignoriert werden, bevor der endgültige Statuscode an den WinHTTP-Client zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="48149-319">The maximum number of Informational 100-199 status code responses ignored before returning the final status code to the WinHTTP client.</span></span> <span data-ttu-id="48149-320">Die Statuscodes 100-199 können vom Server vor dem endgültigen Statuscode gesendet werden und werden in der Spezifikation für HTTP/1.1 beschrieben (weitere Informationen finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span><span class="sxs-lookup"><span data-stu-id="48149-320">Informational 100-199 status codes can be sent by the server before the final status code, and are described in the specification for HTTP/1.1 (for more information, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span></span> <span data-ttu-id="48149-321">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="48149-321">The default is 10.</span></span>

<span data-ttu-id="48149-322">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="48149-322">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-323"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP \_ OPTION \_ MAX \_ RESPONSE \_ DRAIN \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="48149-323"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-324">Ein , der an die Menge der Daten gebunden ist, die aus Antworten entladen wurden, um eine In Bytes angegebene Verbindung wiederzuverwenden.</span><span class="sxs-lookup"><span data-stu-id="48149-324">A bound on the amount of data drained from responses in order to reuse a connection, specified in bytes.</span></span> <span data-ttu-id="48149-325">Der Standardwert ist 1 MB.</span><span class="sxs-lookup"><span data-stu-id="48149-325">The default is 1MB.</span></span>

<span data-ttu-id="48149-326">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="48149-326">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-327"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**MAXIMALE \_ \_ \_ \_ ANTWORTHEADERGRÖßE \_ DER WINHTTP-OPTION**</span><span class="sxs-lookup"><span data-stu-id="48149-327"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-328">Ein gebundener Satz für die maximale Größe des Headerteils der Serverantwort, angegeben in Bytes.</span><span class="sxs-lookup"><span data-stu-id="48149-328">A bound set on the maximum size of the header portion of the server response, specified in bytes.</span></span> <span data-ttu-id="48149-329">Diese Grenze schützt den Client vor einem nicht autorisierten Server, der versucht, den Client zu lahmen, indem eine Antwort mit einer unendlichen Menge an Headerdaten gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="48149-329">This bound protects the client from an unauthorized server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="48149-330">Der Standardwert ist 64 KB.</span><span class="sxs-lookup"><span data-stu-id="48149-330">The default value is 64KB.</span></span>

<span data-ttu-id="48149-331">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="48149-331">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-332"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**\_ \_ ÜBERGEORDNETES WINHTTP-OPTIONSHANDLE \_**</span><span class="sxs-lookup"><span data-stu-id="48149-332"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-333">Ruft das übergeordnete Handle für dieses Handle ab.</span><span class="sxs-lookup"><span data-stu-id="48149-333">Retrieves the parent handle to this handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-334"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP \_ OPTION \_ PASSPORT \_ COBRANDING \_ TEXT**</span><span class="sxs-lookup"><span data-stu-id="48149-334"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-335">Ruft eine Zeichenfolge ab, die den vom Passport-Anmeldeserver [*bereitgestellten Cobrandingtext*](glossary.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="48149-335">Retrieves a string that contains the [*cobranding*](glossary.md) text provided by the Passport logon server.</span></span> <span data-ttu-id="48149-336">Diese Option sollte sofort abgerufen werden, nachdem der Anmeldeserver mit dem Statuscode 401 reagiert hat.</span><span class="sxs-lookup"><span data-stu-id="48149-336">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="48149-337">Eine Anwendung sollte eine Puffergröße in Bytes übergeben, die groß genug ist, um die zurückgegebene Zeichenfolge zu speichern.</span><span class="sxs-lookup"><span data-stu-id="48149-337">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-338"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP \_ OPTION \_ PASSPORT \_ COBRANDING \_ URL**</span><span class="sxs-lookup"><span data-stu-id="48149-338"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-339">Ruft eine Zeichenfolge ab, die eine URL für eine [*cobranding-Grafik enthält,*](glossary.md) die vom Passport-Anmeldeserver bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="48149-339">Retrieves a string that contains a URL for a [*cobranding*](glossary.md) graphic provided by the Passport logon server.</span></span> <span data-ttu-id="48149-340">Diese Option sollte sofort abgerufen werden, nachdem der Anmeldeserver mit dem Statuscode 401 reagiert hat.</span><span class="sxs-lookup"><span data-stu-id="48149-340">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="48149-341">Eine Anwendung sollte eine Puffergröße in Bytes übergeben, die groß genug ist, um die zurückgegebene Zeichenfolge zu speichern.</span><span class="sxs-lookup"><span data-stu-id="48149-341">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-342"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP \_ OPTION \_ PASSPORT \_ RETURN \_ URL**</span><span class="sxs-lookup"><span data-stu-id="48149-342"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-343">Legt eine schreibgeschützte Option für ein Anforderungshandle fest, das die Passport-Rückgabe-URL abruft.</span><span class="sxs-lookup"><span data-stu-id="48149-343">Sets a read-only option on a request handle that retrieves the Passport return URL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-344"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP \_ OPTION \_ PASSPORT \_ SIGN \_ OUT**</span><span class="sxs-lookup"><span data-stu-id="48149-344"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-345">Legt die Option für ein Sitzungshandle fest, um sich von passport-Anmeldungen abzumelden.</span><span class="sxs-lookup"><span data-stu-id="48149-345">Sets the option on a session handle to sign out of any Passport logins.</span></span> <span data-ttu-id="48149-346">Eine Anwendung sollte die Passport-Rückgabe-URL übergeben, die mit **WINHTTP \_ OPTION PASSPORT RETURN \_ \_ \_ URL** abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="48149-346">An application should pass in the Passport return URL that was retrieved with **WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**.</span></span> <span data-ttu-id="48149-347">Alle Cookies im Zusammenhang mit der Rückgabe-URL werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="48149-347">All cookies related to the return URL are cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-348"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**\_ \_ WINHTTP-OPTIONSKENNWORT**</span><span class="sxs-lookup"><span data-stu-id="48149-348"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-349">Legt einen Zeichenfolgenwert fest, der das einem Anforderungshandle zugeordnete Kennwort enthält, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="48149-349">Sets or retrieves a string value that contains the password associated with a request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-350"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**\_WINHTTP-OPTIONSPROXY \_**</span><span class="sxs-lookup"><span data-stu-id="48149-350"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-351">Legt eine [**WINHTTP \_ PROXY \_ INFO-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) fest, die die Proxydaten für ein vorhandenes Sitzungshandle oder Anforderungshandle enthält, oder ruft sie ab.</span><span class="sxs-lookup"><span data-stu-id="48149-351">Sets or retrieves an [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure that contains the proxy data on an existing session handle or request handle.</span></span> <span data-ttu-id="48149-352">Beim Abrufen von Proxydaten muss eine Anwendung die in dieser Struktur **enthaltenen LpszProxy-** und **lpszProxyBypass-Zeichenfolgen** (wenn sie ungleich **NULL** sind) mithilfe der [**GlobalFree-Funktion**](/windows/desktop/api/winbase/nf-winbase-globalfree) freigeben.</span><span class="sxs-lookup"><span data-stu-id="48149-352">When retrieving proxy data, an application must free the **lpszProxy** and **lpszProxyBypass** strings contained in this structure (if they are non-**NULL**) using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="48149-353">Eine Anwendung kann die globalen Proxydaten (den Standardproxy) abfragen, indem sie ein **NULL-Handle** übergibt.</span><span class="sxs-lookup"><span data-stu-id="48149-353">An application can query for the global proxy data (the default proxy) by passing a **NULL** handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-354"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP \_ OPTION \_ PROXY \_ PASSWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-354"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-355">Legt einen Zeichenfolgenwert fest, der das Kennwort für den Zugriff auf den Proxy enthält, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="48149-355">Sets or retrieves a string value that contains the password used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-356"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**VERWENDETER \_ \_ WINHTTP-OPTIONSPROXY-SPN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48149-356"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WINHTTP\_OPTION\_PROXY\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-357">Ruft den Proxyserverprinzipalnamen ab, den WinHTTP während der Authentifizierung für SSPI bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="48149-357">Gets the proxy Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="48149-358">Dieser Zeichenfolgenwert wird für die Übergabe an [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) nach einem Authentifizierungsfehler verwendet.</span><span class="sxs-lookup"><span data-stu-id="48149-358">This string value is usefor passing to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-359"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**\_WINHTTP-OPTION \_ \_ PROXYBENUTZERNAME**</span><span class="sxs-lookup"><span data-stu-id="48149-359"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-360">Legt einen Zeichenfolgenwert fest, der den Benutzernamen für den Zugriff auf den Proxy enthält, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="48149-360">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-361"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP \_ OPTION \_ READ \_ BUFFER \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="48149-361"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-362">Diese Option ist veraltet. sie hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="48149-362">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-363"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**\_WINHTTP-OPTION \_ " PROXY \_ \_ \_ CONNECT-ANTWORT EMPFANGEN"**</span><span class="sxs-lookup"><span data-stu-id="48149-363"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-364">Legt fest, ob die Proxyantwortentität abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="48149-364">Sets whether or not the proxy response entity can be retrieved.</span></span> <span data-ttu-id="48149-365">Diese Option ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="48149-365">This option is disabled by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-366"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP \_ OPTION \_ RECEIVE \_ RESPONSE \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="48149-366"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-367">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Timeoutwert in Millisekunden enthält, um auf den Empfang aller Antwortheader einer Anforderung zu warten, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="48149-367">Sets or retrieves an unsigned long integer value that contains the timeout value, in milliseconds, to wait to receive all response headers to a request.</span></span> <span data-ttu-id="48149-368">Wenn WinHTTP nicht alle Header innerhalb dieses Timeoutzeitraums empfangen kann, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="48149-368">If WinHTTP fails to receive all the headers within this timeout period, the request is canceled.</span></span> <span data-ttu-id="48149-369">Der Standardtimeoutwert beträgt 90 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="48149-369">The default timeout value is 90 seconds.</span></span>

<span data-ttu-id="48149-370">Dieses Timeout wird nur überprüft, wenn Daten vom Socket empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="48149-370">This timeout is checked only when data is received from the socket.</span></span> <span data-ttu-id="48149-371">Daher wird die Clientanwendung nach Ablauf des Timeouts erst benachrichtigt, wenn weitere Daten vom Server eintreffen.</span><span class="sxs-lookup"><span data-stu-id="48149-371">As a result, when the timeout expires the client application is not notified until more data arrives from the server.</span></span> <span data-ttu-id="48149-372">Wenn keine Daten vom Server eingehen, kann die Verzögerung zwischen dem Timeoutablauf und der Benachrichtigung der Clientanwendung so groß sein wie der Timeoutwert, der mit dem *dwReceiveTimeout-Parameter* der [**WinHttpSetTimeouts-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="48149-372">If no data arrives from the server, the delay between the timeout expiration and notification of the client application could be as large as the timeout value set using the *dwReceiveTimeout* parameter of the [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-373"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP \_ OPTION \_ RECEIVE \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="48149-373"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-374">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, um eine Teilantwort auf eine Anforderung zu erhalten oder einige Daten zu lesen, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="48149-374">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a partial response to a request or read some data.</span></span> <span data-ttu-id="48149-375">Wenn die Antwort länger als dieser Time out-Wert dauert, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="48149-375">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="48149-376">Der Standard-Timeoutwert beträgt 30 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="48149-376">The default timeout value is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-377"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**UMLEITUNGSRICHTLINIE FÜR \_ WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48149-377"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP\_OPTION\_REDIRECT\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-378">Legt das Verhalten von WinHTTP in Bezug auf die Behandlung eines 30-fachen HTTP-Umleitungsstatuscodes fest.</span><span class="sxs-lookup"><span data-stu-id="48149-378">Sets the behavior of WinHTTP regarding the handling of a 30x HTTP redirect status code.</span></span> <span data-ttu-id="48149-379">Diese Option kann für eine Sitzung oder ein Anforderungshandle auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="48149-379">This option can be set on a session or request handle to one of the following values:</span></span>

| <span data-ttu-id="48149-380">Begriff</span><span class="sxs-lookup"><span data-stu-id="48149-380">Term</span></span> | <span data-ttu-id="48149-381">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48149-381">Description</span></span> |
|-|-|
| <span data-ttu-id="48149-382"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>UMLEITUNGSRICHTLINIE \_ FÜR WINHTTP-OPTION \_ \_ \_ IMMER</span><span class="sxs-lookup"><span data-stu-id="48149-382"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_ALWAYS</span></span> | <span data-ttu-id="48149-383">Alle Umleitungen werden automatisch befolgt.</span><span class="sxs-lookup"><span data-stu-id="48149-383">All redirects are followed automatically.</span></span> |
| <span data-ttu-id="48149-384"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP \_ OPTION \_ REDIRECT \_ POLICY \_ DISALLOW \_ HTTPS \_ TO \_ HTTP</span><span class="sxs-lookup"><span data-stu-id="48149-384"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_DISALLOW\_HTTPS\_TO\_HTTP</span></span> | <span data-ttu-id="48149-385">Alle Umleitungen werden befolgt, mit Ausnahme derjenigen, die von einer sicheren URL (https) zu einer unsicheren URL (HTTP) stammen.</span><span class="sxs-lookup"><span data-stu-id="48149-385">All redirects are followed, except those that originate from a secure (https) URL to an unsecure (http) URL.</span></span> <span data-ttu-id="48149-386">Dies ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="48149-386">This is the default setting.</span></span> |
| <span data-ttu-id="48149-387"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>UMLEITUNGSRICHTLINIE \_ FÜR WINHTTP-OPTION \_ \_ \_ NIE</span><span class="sxs-lookup"><span data-stu-id="48149-387"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_NEVER</span></span> | <span data-ttu-id="48149-388">Umleitungen werden nie befolgt.</span><span class="sxs-lookup"><span data-stu-id="48149-388">Redirects are never followed.</span></span> <span data-ttu-id="48149-389">Der 30-fache Status wird an die Anwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="48149-389">The 30x status is returned to the application.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-390"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**\_WINHTTP-OPTION \_ \_ : USERPWD \_ IN \_ URL ABLEHNEN**</span><span class="sxs-lookup"><span data-stu-id="48149-390"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-391">Lehnt URLs ab, die einen Benutzernamen und ein Kennwort enthalten.</span><span class="sxs-lookup"><span data-stu-id="48149-391">Rejects URLs that contain a username and password.</span></span> <span data-ttu-id="48149-392">Diese Option lehnt auch URLs ab, die *username:password-Semantik* enthalten, auch wenn kein Benutzername oder Kennwort angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="48149-392">This option also rejects URLs that contain *username:password* semantics, even if no username or password is specified.</span></span> <span data-ttu-id="48149-393">Beispielsweise würden u:p@hostname " ", :@hostname " ", " u:@hostname " " und " " alle als ungültig gekennzeichnet :p@hostname werden.</span><span class="sxs-lookup"><span data-stu-id="48149-393">For example, "u:p@hostname", ":@hostname", "u:@hostname", and ":p@hostname" would all be flagged as invalid.</span></span> <span data-ttu-id="48149-394">Wenn eine ungültige URL an die Funktion übergeben wird, wird [ERROR \_ WINHTTP \_ INVALID \_ URL](error-messages.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="48149-394">If an invalid URL is passed to the function, it returns [ERROR\_WINHTTP\_INVALID\_URL](error-messages.md).</span></span> <span data-ttu-id="48149-395">Standardmäßig ist diese Option deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="48149-395">This option is turned off by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-396"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**\_ANFORDERUNGSPRIORITÄT DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48149-396"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-397">Diese Option ist veraltet. sie hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="48149-397">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-398"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP \_ OPTION \_ REQUEST \_ STATS**</span><span class="sxs-lookup"><span data-stu-id="48149-398"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP\_OPTION\_REQUEST\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-399">Erstellt Statistiken für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="48149-399">Retreives statistics for the request.</span></span>  <span data-ttu-id="48149-400">Eine Liste der verfügbaren Statistiken finden Sie unter [**WINHTTP \_ REQUEST \_ STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span><span class="sxs-lookup"><span data-stu-id="48149-400">For a list of the available statistics, see [**WINHTTP\_REQUEST\_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-401"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**ANFORDERUNGSZEITEN \_ DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48149-401"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP\_OPTION\_REQUEST\_TIMES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-402">Sucht nach Zeitsteuerungsinformationen für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="48149-402">Retreives timing information for the request.</span></span> <span data-ttu-id="48149-403">Eine Liste der verfügbaren Zeitsteuerungen finden Sie unter [**WINHTTP \_ REQUEST \_ TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span><span class="sxs-lookup"><span data-stu-id="48149-403">For a list of the available timings, see [**WINHTTP\_REQUEST\_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-404"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**TIMEOUT \_ FÜR AUFLÖSUNG DER \_ \_ WINHTTP-OPTION**</span><span class="sxs-lookup"><span data-stu-id="48149-404"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP\_OPTION\_RESOLVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-405">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, um einen Hostnamen aufzulösen, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="48149-405">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to resolve a host name.</span></span> <span data-ttu-id="48149-406">Der Standardwert für das Timeout ist **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="48149-406">The default timeout value is **INFINITE**.</span></span> <span data-ttu-id="48149-407">Wenn ein nicht standardmäßiger Wert angegeben wird, verursacht dies einen Mehraufwand von einer Threaderstellung pro Namensauflösung.</span><span class="sxs-lookup"><span data-stu-id="48149-407">If a non-default value is specified, there is an overhead of one thread-creation per name resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-408"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**SICHERE PROTOKOLLE \_ DER WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48149-408"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP\_OPTION\_SECURE\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-409">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, welche sicheren Protokolle zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="48149-409">Sets an unsigned long integer value that specifies which secure protocols are acceptable.</span></span> <span data-ttu-id="48149-410">Standardmäßig sind nur SSL3 und TLS1 in Windows 7 und Windows 8.</span><span class="sxs-lookup"><span data-stu-id="48149-410">By default only SSL3 and TLS1 are enabled in Windows 7 and Windows 8.</span></span> <span data-ttu-id="48149-411">Standardmäßig sind nur SSL3, TLS1.0, TLS1.1 und TLS1.2 in Windows 8.1 und Windows 10.</span><span class="sxs-lookup"><span data-stu-id="48149-411">By default only SSL3, TLS1.0, TLS1.1, and TLS1.2 are enabled in Windows 8.1 and Windows 10.</span></span> <span data-ttu-id="48149-412">Der Wert kann eine Kombination aus mindestens einem der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="48149-412">The value can be a combination of one or more of the following values.</span></span>

| <span data-ttu-id="48149-413">Begriff</span><span class="sxs-lookup"><span data-stu-id="48149-413">Term</span></span> | <span data-ttu-id="48149-414">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48149-414">Description</span></span> |
|-|-|
| <span data-ttu-id="48149-415"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ ALL</span><span class="sxs-lookup"><span data-stu-id="48149-415"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_ALL</span></span> | <span data-ttu-id="48149-416">Die protokolle Secure Sockets Layer (SSL) 2.0, SSL 3.0 und Transport Layer Security (TLS) 1.0 können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48149-416">The Secure Sockets Layer (SSL) 2.0, SSL 3.0, and Transport Layer Security (TLS) 1.0 protocols can be used.</span></span> |
| <span data-ttu-id="48149-417"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP-FLAG \_ \_ SECURE PROTOCOL \_ \_ SSL2</span><span class="sxs-lookup"><span data-stu-id="48149-417"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL2</span></span> | <span data-ttu-id="48149-418">Das SSL 2.0-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48149-418">The SSL 2.0 protocol can be used.</span></span> |
| <span data-ttu-id="48149-419"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP-FLAG \_ \_ SECURE PROTOCOL \_ \_ SSL3</span><span class="sxs-lookup"><span data-stu-id="48149-419"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL3</span></span> | <span data-ttu-id="48149-420">Das SSL 3.0-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48149-420">The SSL 3.0 protocol can be used.</span></span> |
| <span data-ttu-id="48149-421"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP-FLAG \_ \_ SECURE PROTOCOL \_ \_ TLS1</span><span class="sxs-lookup"><span data-stu-id="48149-421"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1</span></span> | <span data-ttu-id="48149-422">Das TLS 1.0-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48149-422">The TLS 1.0 protocol can be used.</span></span> |
| <span data-ttu-id="48149-423"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP-FLAG \_ \_ SECURE PROTOCOL \_ \_ TLS1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="48149-423"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_1</span></span> | <span data-ttu-id="48149-424">Das TLS 1.1-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48149-424">The TLS 1.1 protocol can be used.</span></span> |
| <span data-ttu-id="48149-425"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP FLAG \_ \_ SECURE PROTOCOL \_ \_ TLS1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="48149-425"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_2</span></span> | <span data-ttu-id="48149-426">Das TLS 1.2-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48149-426">The TLS 1.2 protocol can be used.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="48149-427"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**\_SICHERHEITSZERTIFIKATSTRUKTUR DER \_ \_ \_ WINHTTP-OPTION**</span><span class="sxs-lookup"><span data-stu-id="48149-427"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-428">Ruft das Zertifikat für einen SSL/TLS-Server in der [**WINHTTP \_ CERTIFICATE \_ INFO-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) ab.</span><span class="sxs-lookup"><span data-stu-id="48149-428">Retrieves the certificate for a SSL/TLS server into the [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="48149-429">Die Anwendung muss die **Member lpszSubjectInfo** und **lpszIssuerInfo mit** [**LocalFree frei geben.**](/windows/desktop/api/winbase/nf-winbase-localfree)</span><span class="sxs-lookup"><span data-stu-id="48149-429">The application must free the **lpszSubjectInfo** and **lpszIssuerInfo** members with [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-430"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**\_SICHERHEITSFLAGS FÜR DIE WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48149-430"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-431">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Sicherheitsflags für ein Handle enthält, oder ruft diesen wert ab.</span><span class="sxs-lookup"><span data-stu-id="48149-431">Sets or retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="48149-432">Dabei kann es sich um eine Kombination dieser Werte handelt:</span><span class="sxs-lookup"><span data-stu-id="48149-432">It can be a combination of these values:</span></span>

| <span data-ttu-id="48149-433">Begriff</span><span class="sxs-lookup"><span data-stu-id="48149-433">Term</span></span> | <span data-ttu-id="48149-434">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48149-434">Description</span></span> |
|-|-|
| <span data-ttu-id="48149-435"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>\_ \_ SICHERHEITSFLAG \_ \_ ZERTIFIKAT-CN IGNORIEREN \_ UNGÜLTIG</span><span class="sxs-lookup"><span data-stu-id="48149-435"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span> |<span data-ttu-id="48149-436">Lässt einen ungültigen allgemeinen Namen in einem Zertifikat zu. Das heißt, der von der Anwendung angegebene Servername ist nicht mit dem allgemeinen Namen im Zertifikat übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="48149-436">Allows an invalid common name in a certificate; that is, the server name specified by the application does not match the common name in the certificate.</span></span> <span data-ttu-id="48149-437">Wenn dieses Flag festgelegt ist, erhält die Anwendung keinen **WINHTTP \_ CALLBACK \_ STATUS FLAG \_ \_ CERT \_ CN \_ INVALID-Rückruf.**</span><span class="sxs-lookup"><span data-stu-id="48149-437">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_CN\_INVALID** callback.</span></span> |
| <span data-ttu-id="48149-438"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY \_ FLAG \_ IGNORE \_ CERT \_ DATE \_ INVALID</span><span class="sxs-lookup"><span data-stu-id="48149-438"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span> |<span data-ttu-id="48149-439">Lässt ein ungültiges Zertifikatdatum zu, d. b. ein abgelaufenes oder noch nicht effektives Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="48149-439">Allows an invalid certificate date, that is, an expired or not-yet-effective certificate.</span></span> <span data-ttu-id="48149-440">Wenn dieses Flag festgelegt ist, erhält die Anwendung keinen **WINHTTP \_ CALLBACK \_ STATUS FLAG \_ \_ CERT DATE \_ \_ INVALID-Rückruf.**</span><span class="sxs-lookup"><span data-stu-id="48149-440">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_DATE\_INVALID** callback.</span></span> |
| <span data-ttu-id="48149-441"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>\_ \_ SICHERHEITSFLAG UNBEKANNTE \_ ZERTIFIZIERUNGSSTELLE \_ IGNORIEREN</span><span class="sxs-lookup"><span data-stu-id="48149-441"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span> | <span data-ttu-id="48149-442">Lässt eine ungültige Zertifizierungsstelle zu.</span><span class="sxs-lookup"><span data-stu-id="48149-442">Allows an invalid certificate authority.</span></span> <span data-ttu-id="48149-443">Wenn dieses Flag festgelegt ist, erhält die Anwendung keinen **WINHTTP \_ CALLBACK \_ STATUS FLAG INVALID \_ \_ \_ CA-Rückruf.**</span><span class="sxs-lookup"><span data-stu-id="48149-443">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_INVALID\_CA** callback.</span></span> |
| <span data-ttu-id="48149-444"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>\_SICHERHEITSFLAG : FALSCHE VERWENDUNG DES \_ \_ \_ ZERTIFIKATS \_ IGNORIEREN</span><span class="sxs-lookup"><span data-stu-id="48149-444"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_CERT\_WRONG\_USAGE</span></span> | <span data-ttu-id="48149-445">Ermöglicht das Herstellen der Identität eines Servers mit einem Nicht-Serverzertifikat (z. B. einem Clientzertifikat).</span><span class="sxs-lookup"><span data-stu-id="48149-445">Allows the identity of a server to be established with a non-server certificate (for example, a client certificate).</span></span> |
| <span data-ttu-id="48149-446"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>\_ \_ SICHERHEITSFLAG SCHWACHE SIGNATUR \_ \_ IGNORIEREN</span><span class="sxs-lookup"><span data-stu-id="48149-446"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span> | <span data-ttu-id="48149-447">Ermöglicht das Ignorieren einer schwachen Signatur.</span><span class="sxs-lookup"><span data-stu-id="48149-447">Allows a weak signature to be ignored.</span></span><br/><span data-ttu-id="48149-448">Dieses Flag ist im Rollupupdate für jedes Betriebssystem ab Windows 7 und Windows Server 2008 R2 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="48149-448">This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.</span></span> |
| <span data-ttu-id="48149-449"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>\_SICHERHEITSFLAG \_ SICHER</span><span class="sxs-lookup"><span data-stu-id="48149-449"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span> | <span data-ttu-id="48149-450">Verwendet sichere Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="48149-450">Uses secure transfers.</span></span> <span data-ttu-id="48149-451">Dies wird nur in einem Aufruf von [**WinHttpQueryOption zurückgegeben.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="48149-451">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="48149-452"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>\_ \_ SICHERHEITSFLAGSTÄRKE \_ MITTEL</span><span class="sxs-lookup"><span data-stu-id="48149-452"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span> | <span data-ttu-id="48149-453">Verwendet mittlere (56-Bit)-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="48149-453">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="48149-454">Dies wird nur in einem Aufruf von [**WinHttpQueryOption zurückgegeben.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="48149-454">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="48149-455"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>\_ \_ SICHERHEITSFLAGSTÄRKE \_ STARK</span><span class="sxs-lookup"><span data-stu-id="48149-455"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span> | <span data-ttu-id="48149-456">Verwendet eine starke Verschlüsselung (128 Bit).</span><span class="sxs-lookup"><span data-stu-id="48149-456">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="48149-457">Dies wird nur in einem Aufruf von [**WinHttpQueryOption zurückgegeben.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="48149-457">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="48149-458"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>\_ \_ SICHERHEITSFLAGSTÄRKE \_ SCHWACH</span><span class="sxs-lookup"><span data-stu-id="48149-458"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span> | <span data-ttu-id="48149-459">Verwendet eine schwache (40-Bit)-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="48149-459">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="48149-460">Dies wird nur in einem Aufruf von [**WinHttpQueryOption zurückgegeben.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="48149-460">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="48149-461"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**SICHERHEITSINFORMATIONEN \_ ZUR WINHTTP-OPTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48149-461"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP\_OPTION\_SECURITY\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-462">Sucht die SChannel-Verbindung und Verschlüsselungsinformationen für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="48149-462">Retreives the SChannel connection and cipher information for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-463"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**\_WINHTTP-OPTION \_ \_ \_ SICHERHEITSSCHLÜSSELBITNESS**</span><span class="sxs-lookup"><span data-stu-id="48149-463"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-464">Ruft einen ganzzahligen Wert ohne Vorzeichen ab, der die Verschlüsselungsstärke des Verschlüsselungsschlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="48149-464">Retrieves an unsigned long integer value that contains the cipher strength of the encryption key.</span></span> <span data-ttu-id="48149-465">Eine größere Zahl gibt eine stärkere Verschlüsselung mit Verschlüsselungsstärke an.</span><span class="sxs-lookup"><span data-stu-id="48149-465">A larger number indicates stronger cipher strength encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-466"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**TIMEOUT \_ BEIM SENDEN DER \_ \_ WINHTTP-OPTION**</span><span class="sxs-lookup"><span data-stu-id="48149-466"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-467">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, um eine Anforderung zu senden oder Daten zu schreiben, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="48149-467">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to send a request or write some data.</span></span> <span data-ttu-id="48149-468">Wenn das Senden der Anforderung länger als das Timeout dauert, wird der Sendevorgang abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="48149-468">If sending the request takes longer than the timeout, the send operation is canceled.</span></span> <span data-ttu-id="48149-469">Der Standardzeitraum bis zum Timeout beträgt 30 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="48149-469">The default timeout is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-470"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP \_ OPTION \_ SERVER \_ CBT**</span><span class="sxs-lookup"><span data-stu-id="48149-470"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP\_OPTION\_SERVER\_CBT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-471">Ruft einen Zeiger auf die [**SecPkgContext-Bindungsstruktur \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) ab, die ein Kanalbindungstoken (Channel Binding Token, CBT) angibt.</span><span class="sxs-lookup"><span data-stu-id="48149-471">Gets a pointer to [**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) structure that specifies a Channel Binding Token (CBT).</span></span>

<span data-ttu-id="48149-472">Ein Kanalbindungstoken ist eine Eigenschaft eines sicheren Transportkanals und wird verwendet, um einen Authentifizierungskanal an den sicheren Transportkanal zu binden.</span><span class="sxs-lookup"><span data-stu-id="48149-472">A Channel Binding Token is a property of a secure transport channel and is used to bind an authentication channel to the secure transport channel.</span></span> <span data-ttu-id="48149-473">Dieses Token kann von dieser Option nur nach dem Herstellen einer SSL-Verbindung erhalten werden.</span><span class="sxs-lookup"><span data-stu-id="48149-473">This token can only be obtained by this option after an SSL connection has been established.</span></span>

> [!Note]
> <span data-ttu-id="48149-474">Die Übergabe dieser  Option und eines NULL-Werts für *lpBuffer* an [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) gibt ERROR INSUFFICIENT BUFFER und die erforderliche Bytegröße für den Puffer im \_ \_ *lpdwBufferLength-Parameter* zurück.</span><span class="sxs-lookup"><span data-stu-id="48149-474">Passing this option and a **null** value for *lpBuffer* to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) will return ERROR\_INSUFFICIENT\_BUFFER and the required byte size for the buffer in the *lpdwBufferLength* parameter.</span></span> <span data-ttu-id="48149-475">Dieser zurückgegebene Puffergrößenwert kann in einem nachfolgenden Aufruf zur Abfrage des Kanalbindungstokens übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="48149-475">This returned buffer size value can be passed in a subsequent call to query for the Channel Binding Token.</span></span> <span data-ttu-id="48149-476">Diese Schritte sind erforderlich, wenn Sie WINHTTP CALLBACK STATUS REQUEST behandeln, wenn Sie Anforderungsheader basierend auf dem \_ \_ \_ Kanalbindungstoken ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="48149-476">These steps are necessary when handling WINHTTP\_CALLBACK\_STATUS\_REQUEST if you want to modify request headers based on the Channel Binding Token.</span></span> <span data-ttu-id="48149-477">Beachten Sie, dass Windows XP und Vista das Ändern von Anforderungsheadern während dieses Rückrufs nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="48149-477">Note that Windows XP and Vista do not support modifying request headers during this callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-478"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CHAIN \_ CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="48149-478"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-479">Ruft den Kontext der Serverzertifizierungskette ab.</span><span class="sxs-lookup"><span data-stu-id="48149-479">Retrieves the server certification chain context.</span></span> <span data-ttu-id="48149-480">**WINHTTP \_ OPTION \_ SERVER \_ CERT CHAIN \_ \_ CONTEXT** kann übergeben werden, um einen duplizierten Zeiger auf **den CERT CHAIN \_ \_ CONTEXT** für eine Serverzertifikatkette zu erhalten, die während einer ausgehandelten SSL-Verbindung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="48149-480">**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT** can be passed to obtain a duplicated pointer to the **CERT\_CHAIN\_CONTEXT** for a server certificate chain received during a negotiated SSL connection.</span></span> <span data-ttu-id="48149-481">Der Client muss [**CertFreeCertificateContext für**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) den zurückgegebenen PCCERT CONTEXT-Zeiger aufrufen, \_ der in den Puffer gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="48149-481">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-482"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="48149-482"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-483">Ruft den Serverzertifizierungskontext ab.</span><span class="sxs-lookup"><span data-stu-id="48149-483">Retrieves the server certification context.</span></span> <span data-ttu-id="48149-484">**WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CONTEXT** kann übergeben werden, um einen duplizierten Zeiger auf [**den CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) für ein Serverzertifikat zu erhalten, das während einer ausgehandelten SSL-Verbindung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="48149-484">**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT** can be passed to obtain a duplicated pointer to the [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) for a server certificate received during a negotiated SSL connection.</span></span> <span data-ttu-id="48149-485">Der Client muss [**CertFreeCertificateContext für**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) den zurückgegebenen PCCERT CONTEXT-Zeiger aufrufen, \_ der in den Puffer gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="48149-485">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-486"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**VERWENDETER \_ \_ WINHTTP-OPTIONSSERVER-SPN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48149-486"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WINHTTP\_OPTION\_SERVER\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-487">Ruft den Serverprinzipalnamen ab, den WinHTTP während der Authentifizierung für SSPI bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="48149-487">Gets the server Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="48149-488">Dieser Zeichenfolgenwert kann nach einem Authentifizierungsfehler [**an SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="48149-488">This string value can be passed to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-489"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**\_ \_ WINHTTP-OPTIONS-SPN**</span><span class="sxs-lookup"><span data-stu-id="48149-489"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP\_OPTION\_SPN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-490">Schließt die Serverportnummer ein oder entfernt sie, wenn der SPN (Dienstprinzipalname) für die Kerberos- oder Negotiate Kerberos-Authentifizierung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="48149-490">Includes or removes the server port number when the SPN (service principal name) is built for Kerberos or Negotiate Kerberos authentication.</span></span> <span data-ttu-id="48149-491">Dieses Flag ist einer der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="48149-491">This flag is one of the following values:</span></span>

| <span data-ttu-id="48149-492">Begriff</span><span class="sxs-lookup"><span data-stu-id="48149-492">Term</span></span> | <span data-ttu-id="48149-493">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48149-493">Description</span></span> |
|-|-|
| <span data-ttu-id="48149-494"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>\_WINHTTP: \_ DEAKTIVIEREN DES SPN-SERVERPORTS \_ \_</span><span class="sxs-lookup"><span data-stu-id="48149-494"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP\_DISABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="48149-495">Entfernt die Serverportnummer.</span><span class="sxs-lookup"><span data-stu-id="48149-495">Removes the server port number.</span></span> |
| <span data-ttu-id="48149-496"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP \_ ENABLE \_ SPN \_ SERVER \_ PORT</span><span class="sxs-lookup"><span data-stu-id="48149-496"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP\_ENABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="48149-497">Schließt die Serverportnummer ein.</span><span class="sxs-lookup"><span data-stu-id="48149-497">Includes the server port number.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="48149-498"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP-OPTION \_ \_ TCP FAST \_ \_ OPEN**</span><span class="sxs-lookup"><span data-stu-id="48149-498"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP\_OPTION\_TCP\_FAST\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-499">Aktiviert TCP Fast Open für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="48149-499">Enables TCP Fast Open for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-500"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**\_WINHTTP-OPTION \_ TCP \_ KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="48149-500"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**WINHTTP\_OPTION\_TCP\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-501">Diese Option kann für ein WinHttp-Sitzungshandle festgelegt werden, um TCP-Keep-Alive-Verhalten für den zugrunde liegenden Socket zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="48149-501">This option can be set on a WinHttp session handle to enable TCP keep-alive behavior on the underlying socket.</span></span> <span data-ttu-id="48149-502">Übernimmt eine [**\_ tcp-Keepalive-Struktur.**](/windows/win32/winsock/sio-keepalive-vals)</span><span class="sxs-lookup"><span data-stu-id="48149-502">Takes a [**tcp\_keepalive**](/windows/win32/winsock/sio-keepalive-vals) struct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-503"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**\_WINHTTP-OPTION \_ TLS FALSE \_ \_ START**</span><span class="sxs-lookup"><span data-stu-id="48149-503"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP\_OPTION\_TLS\_FALSE\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-504">Aktiviert TLS False Start für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="48149-504">Enables TLS False Start for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-505"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP \_ OPTION \_ UNLOAD \_ NOTIFY \_ EVENT**</span><span class="sxs-lookup"><span data-stu-id="48149-505"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-506">Nimmt ein Ereignis an, das festgelegt wird, wenn der letzte Rückruf für eine bestimmte Sitzung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="48149-506">Takes an event that will be set when the last callback has completed for a particular session.</span></span> <span data-ttu-id="48149-507">Dieses Flag muss für ein Sitzungshandle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48149-507">This flag must be must be used on a session handle.</span></span> <span data-ttu-id="48149-508">Das Ereignis kann erst geschlossen werden, nachdem es von WinHTTP festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="48149-508">The event cannot be closed until after it has been set by WinHTTP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-509"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP \_ OPTION \_ UNSAFE \_ HEADER \_ PARSING**</span><span class="sxs-lookup"><span data-stu-id="48149-509"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-510">Diese Option ist für die interne Verwendung reserviert und sollte nicht aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="48149-510">This option is reserved for internal use and should not be called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-511"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**UPGRADE DER \_ WINHTTP-OPTION \_ AUF \_ \_ \_ WEBSOCKET**</span><span class="sxs-lookup"><span data-stu-id="48149-511"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-512">Weist den Stapel an, einen WebSocket-Handshakeprozess mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)zu starten.</span><span class="sxs-lookup"><span data-stu-id="48149-512">Instructs the stack to start a WebSocket handshake process with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="48149-513">Diese Option nimmt keine Parameter an.</span><span class="sxs-lookup"><span data-stu-id="48149-513">This option takes no parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-514"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**\_ \_ WINHTTP-OPTIONS-URL**</span><span class="sxs-lookup"><span data-stu-id="48149-514"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-515">Ruft einen Zeichenfolgenwert ab, der die vollständige URL einer heruntergeladenen Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="48149-515">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="48149-516">Wenn die ursprüngliche URL zusätzliche Daten enthielt, z. B. Suchzeichenfolgen oder Anker, oder wenn der Aufruf umgeleitet wurde, unterscheidet sich die zurückgegebene URL vom ursprünglichen.</span><span class="sxs-lookup"><span data-stu-id="48149-516">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="48149-517">Die Anwendung sollte einen Puffer in Bytes übergeben, der groß genug ist, um die zurückgegebene URL in wide char zu speichern.</span><span class="sxs-lookup"><span data-stu-id="48149-517">The application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-518"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**\_WINHTTP-OPTION \_ VERWENDEN VON \_ \_ ANMELDEINFORMATIONEN FÜR GLOBALEN SERVER \_**</span><span class="sxs-lookup"><span data-stu-id="48149-518"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-519">Übernimmt eine **BOOL** und kann nur ein Sitzungshandle festlegen.</span><span class="sxs-lookup"><span data-stu-id="48149-519">Takes a **BOOL** and can be set only a session handle.</span></span> <span data-ttu-id="48149-520">Er wird nur an Handles weiter gegeben, die aus dem Sitzungshandle erstellt wurden, nachdem die Option festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="48149-520">It will only propagate down to handles created from the session handle after the option has been set.</span></span> <span data-ttu-id="48149-521">True gibt an, dass diese Option als letzte Möglichkeit die Verwendung globaler Serveranmeldeinformationen bewirkt, die von WinInet gepusht wurden.</span><span class="sxs-lookup"><span data-stu-id="48149-521">If **TRUE**, this option causes as a last resort the use of global server credentials that were pushed down from WinInet.</span></span> <span data-ttu-id="48149-522">Der Standardwert für diese Option ist **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="48149-522">The default for this option is **FALSE**.</span></span> <span data-ttu-id="48149-523">Diese Option erfordert den Registrierungsschlüssel **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="48149-523">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="48149-524">Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="48149-524">This registry key is not present by default.</span></span> <span data-ttu-id="48149-525">Wenn sie festgelegt ist, sendet WinINet Anmeldeinformationen an WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="48149-525">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="48149-526">Wenn WinHttp eine Authentifizierungsaufforderung erhält und keine Anmeldeinformationen für das aktuelle Handle festgelegt sind, werden die von WinINet bereitgestellten Anmeldeinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="48149-526">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-527"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP \_ OPTION \_ USER \_ AGENT**</span><span class="sxs-lookup"><span data-stu-id="48149-527"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-528">Legt die Zeichenfolge des [*Benutzer-Agents*](glossary.md) auf Handles fest, die von [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) bereitgestellt und in nachfolgenden [**WinHttpSendRequest-Funktionen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) verwendet werden, oder ruft sie ab, solange sie nicht durch einen header überschrieben wird, der von [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) oder **WinHttpSendRequest** hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="48149-528">Sets or retrieves the [*user agent*](glossary.md) string on handles supplied by [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) and used in subsequent [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) functions, as long as it is not overridden by a header added by [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) or **WinHttpSendRequest**.</span></span> <span data-ttu-id="48149-529">Beim Abrufen eines Benutzer-Agents sollte die Anwendung einen Puffer in Bytes übergeben, der groß genug ist, um die zurückgegebene URL in wide char zu speichern.</span><span class="sxs-lookup"><span data-stu-id="48149-529">When retrieving a user agent, the application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span> <span data-ttu-id="48149-530">Beim Festlegen des Benutzer-Agents entspricht die Puffergröße der Länge der Zeichenfolge in Zeichen sowie dem **NULL-Abschlusszeichen.**</span><span class="sxs-lookup"><span data-stu-id="48149-530">When setting the user agent, the buffer size is the length of the string, in characters, plus the **NULL** terminator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-531"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP \_ OPTION \_ USERNAME**</span><span class="sxs-lookup"><span data-stu-id="48149-531"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-532">Legt eine Zeichenfolge fest, die den Benutzernamen enthält, oder ruft sie ab.</span><span class="sxs-lookup"><span data-stu-id="48149-532">Sets or retrieves a string that contains the user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-533"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ CLOSE \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="48149-533"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-534">Legt die Zeit in Millisekunden fest, die [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) auf den Abschluss des schließenden Handshakes warten soll.</span><span class="sxs-lookup"><span data-stu-id="48149-534">Sets the time, in milliseconds, that [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) should wait to complete the close handshake.</span></span> <span data-ttu-id="48149-535">Die Standardeinstellung beträgt 10 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="48149-535">The default is 10 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-536"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ KEEPALIVE \_ INTERVAL**</span><span class="sxs-lookup"><span data-stu-id="48149-536"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-537">Legt das Intervall in Millisekunden fest, um ein Keep-Alive-Paket über die Verbindung zu senden.</span><span class="sxs-lookup"><span data-stu-id="48149-537">Sets the interval, in milliseconds, to send a keep-alive packet over the connection.</span></span> <span data-ttu-id="48149-538">Das Standardintervall ist 30000 (30 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="48149-538">The default interval is 30000 (30 seconds).</span></span> <span data-ttu-id="48149-539">Das Mindestintervall beträgt 15.000 (15 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="48149-539">The minimum interval is 15000 (15 seconds).</span></span> <span data-ttu-id="48149-540">Wenn [**Sie WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) verwenden, um einen Wert unter 15000 festzulegen, wird mit **ERROR INVALID \_ \_ PARAMETER** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="48149-540">Using [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to set a value lower than 15000 will return with **ERROR\_INVALID\_PARAMETER**.</span></span>

> [!Note]
> <span data-ttu-id="48149-541">Der Standardwert für **WINHTTP \_ OPTION WEB SOCKET \_ \_ \_ KEEPALIVE \_ INTERVAL** wird aus **HKLM: \\ SOFTWARE Microsoft \\ \\ WebSocket \\ KeepaliveInterval** gelesen.</span><span class="sxs-lookup"><span data-stu-id="48149-541">The default value for **WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL** is read from **HKLM:\\SOFTWARE\\Microsoft\\WebSocket\\KeepaliveInterval**.</span></span> <span data-ttu-id="48149-542">Wenn kein Wert festgelegt ist, wird der Standardwert 30000 verwendet.</span><span class="sxs-lookup"><span data-stu-id="48149-542">If a value is not set, the default value of 30000 will be used.</span></span> <span data-ttu-id="48149-543">Es ist nicht möglich, ein niedrigeres Keepalive-Intervall als 15.000 Millisekunden zu haben.</span><span class="sxs-lookup"><span data-stu-id="48149-543">It is not possible to have a lower keepalive interval than 15000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-544"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ RECEIVE \_ BUFFER \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="48149-544"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-545">Legt ein DWORD fest oder ruft es ab, das die Empfangspuffergröße angibt, die für WebSocket-Verbindungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="48149-545">Sets or retrieves a DWORD which specifies the receive buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-546"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ SEND \_ BUFFER \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="48149-546"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-547">Legt ein DWORD fest oder ruft es ab, das die Sendepuffergröße angibt, die für WebSocket-Verbindungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="48149-547">Sets or retrieves a DWORD which specifies the send buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-548"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**ANZAHL VON \_ \_ WINHTTP-OPTION-WORKERTHREADS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48149-548"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-549">Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Anzahl der Arbeitsthreads angibt, die der Threadpool für asynchrone Vervollständigungen verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="48149-549">Sets an unsigned long integer value that specifies the number of worker threads the thread pool should use for asynchronous completions.</span></span> <span data-ttu-id="48149-550">Der Standardwert dieser Option ist 0 (null), was angibt, dass die Anzahl der Arbeitsthreads der Anzahl der CPUs im System entspricht.</span><span class="sxs-lookup"><span data-stu-id="48149-550">The default value of this option is zero, which specifies that the number of worker threads is equal to the number of CPUs on the system.</span></span> <span data-ttu-id="48149-551">Diese Option kann nur für ein **NULL**  [HINTERNET-Handle](hinternet-handles-in-winhttp.md) festgelegt werden, bevor ein asynchroner Vorgang aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="48149-551">This option can only be set on a **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) handle before an asynchronous operation has occurred.</span></span> <span data-ttu-id="48149-552">Diese Option kann nur einmal festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="48149-552">This option can only be set once.</span></span>

<span data-ttu-id="48149-553">**Windows Server 2008 R2 und Windows 7:** Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="48149-553">**Windows Server 2008 R2 and Windows 7:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48149-554"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP \_ OPTION \_ WRITE \_ BUFFER \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="48149-554"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48149-555">Diese Option ist veraltet. sie hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="48149-555">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48149-556">Hinweise</span><span class="sxs-lookup"><span data-stu-id="48149-556">Remarks</span></span>

<span data-ttu-id="48149-557">In der folgenden Tabelle werden die Optionsflags aufgelistet, indem angegeben wird, auf welche Handles sie reagieren können, ob sie abgefragt und festgelegt werden können und welcher Datentyp verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="48149-557">The following table lists the option flags by specifying which handles they can act upon, whether they can be queried and set, and the data type used.</span></span> <span data-ttu-id="48149-558">Ein "X" gibt an, dass das Optionsflag für die Verwendung mit der Funktion oder dem Handle gültig ist, während ein "-" angibt, dass das Optionsflag ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="48149-558">An "X" indicates that the option flag is valid for use with the function or handle, while a "-" specifies that the option flag is invalid.</span></span>

<span data-ttu-id="48149-559">Der Versuch, ein Optionsflag für eine Windows-Version festzulegen oder abzufragen, bei der es nicht unterstützt wird, führt zu **ERROR \_ WINHTTP \_ INVALID \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="48149-559">Attempting to set or query an option flag on a Windows version where it is not supported will result in **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span>

| <span data-ttu-id="48149-560">Optionsflag und Datentyp</span><span class="sxs-lookup"><span data-stu-id="48149-560">Option flag, and data type</span></span> | <span data-ttu-id="48149-561">Sitzungshandle</span><span class="sxs-lookup"><span data-stu-id="48149-561">Session handle</span></span> | <span data-ttu-id="48149-562">Anforderungshandle</span><span class="sxs-lookup"><span data-stu-id="48149-562">Request handle</span></span> | <span data-ttu-id="48149-563">Abfrageoption</span><span class="sxs-lookup"><span data-stu-id="48149-563">Query option</span></span> | <span data-ttu-id="48149-564">SET-Option</span><span class="sxs-lookup"><span data-stu-id="48149-564">Set option</span></span> | <span data-ttu-id="48149-565">Windows-Mindestversion</span><span class="sxs-lookup"><span data-stu-id="48149-565">Minimum Windows Version</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="48149-566">\_WINHTTP-OPTION \_ : \_ GESICHERTE, NICHT \_ BLOCKIERENDE \_ RÜCKRUFE</span><span class="sxs-lookup"><span data-stu-id="48149-566">WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS</span></span><br/><span data-ttu-id="48149-567">**Bool**</span><span class="sxs-lookup"><span data-stu-id="48149-567">**BOOL**</span></span> | <span data-ttu-id="48149-568">X</span><span class="sxs-lookup"><span data-stu-id="48149-568">X</span></span> | \- | \- | <span data-ttu-id="48149-569">X</span><span class="sxs-lookup"><span data-stu-id="48149-569">X</span></span> | \- |
| <span data-ttu-id="48149-570">WINHTTP \_ OPTION \_ AUTOLOGON \_ POLICY</span><span class="sxs-lookup"><span data-stu-id="48149-570">WINHTTP\_OPTION\_AUTOLOGON\_POLICY</span></span><br/><span data-ttu-id="48149-571">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-571">**DWORD**</span></span> | \- | <span data-ttu-id="48149-572">X</span><span class="sxs-lookup"><span data-stu-id="48149-572">X</span></span> | \- | <span data-ttu-id="48149-573">X</span><span class="sxs-lookup"><span data-stu-id="48149-573">X</span></span> | \- |
| <span data-ttu-id="48149-574">\_ \_ WINHTTP-OPTIONSRÜCKRUF</span><span class="sxs-lookup"><span data-stu-id="48149-574">WINHTTP\_OPTION\_CALLBACK</span></span><br/><span data-ttu-id="48149-575">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="48149-575">**LPVOID**</span></span> | <span data-ttu-id="48149-576">X</span><span class="sxs-lookup"><span data-stu-id="48149-576">X</span></span> | <span data-ttu-id="48149-577">X</span><span class="sxs-lookup"><span data-stu-id="48149-577">X</span></span> | <span data-ttu-id="48149-578">X</span><span class="sxs-lookup"><span data-stu-id="48149-578">X</span></span> | <span data-ttu-id="48149-579">X</span><span class="sxs-lookup"><span data-stu-id="48149-579">X</span></span> | \- |
| <span data-ttu-id="48149-580">WINHTTP \_ OPTION \_ CLIENT \_ CERT \_ CONTEXT</span><span class="sxs-lookup"><span data-stu-id="48149-580">WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="48149-581">**\_CERT-KONTEXT**</span><span class="sxs-lookup"><span data-stu-id="48149-581">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="48149-582">X</span><span class="sxs-lookup"><span data-stu-id="48149-582">X</span></span> | \- | <span data-ttu-id="48149-583">X</span><span class="sxs-lookup"><span data-stu-id="48149-583">X</span></span> | <span data-ttu-id="48149-584">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48149-584">Windows Vista</span></span> |
| <span data-ttu-id="48149-585">WINHTTP \_ OPTION \_ CLIENT \_ CERT \_ ISSUER \_ LIST</span><span class="sxs-lookup"><span data-stu-id="48149-585">WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST</span></span><br/>[<span data-ttu-id="48149-586">**SecPkgContext \_ IssuerListInfoEx**</span><span class="sxs-lookup"><span data-stu-id="48149-586">**SecPkgContext\_IssuerListInfoEx**</span></span>](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | <span data-ttu-id="48149-587">X</span><span class="sxs-lookup"><span data-stu-id="48149-587">X</span></span> | <span data-ttu-id="48149-588">X</span><span class="sxs-lookup"><span data-stu-id="48149-588">X</span></span> | \- | <span data-ttu-id="48149-589">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48149-589">Windows Vista</span></span> |
| <span data-ttu-id="48149-590">WINHTTP \_ OPTION \_ CODEPAGE</span><span class="sxs-lookup"><span data-stu-id="48149-590">WINHTTP\_OPTION\_CODEPAGE</span></span><br/><span data-ttu-id="48149-591">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-591">**DWORD**</span></span> | <span data-ttu-id="48149-592">X</span><span class="sxs-lookup"><span data-stu-id="48149-592">X</span></span> | \- | \- | <span data-ttu-id="48149-593">X</span><span class="sxs-lookup"><span data-stu-id="48149-593">X</span></span> | \- |
| <span data-ttu-id="48149-594">\_WINHTTP-OPTION \_ : KONFIGURIEREN DER \_ \_ PASSPORT-AUTHENTIFIZIERUNG</span><span class="sxs-lookup"><span data-stu-id="48149-594">WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH</span></span><br/><span data-ttu-id="48149-595">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-595">**DWORD**</span></span> | <span data-ttu-id="48149-596">X</span><span class="sxs-lookup"><span data-stu-id="48149-596">X</span></span> | \- | \- | <span data-ttu-id="48149-597">X</span><span class="sxs-lookup"><span data-stu-id="48149-597">X</span></span> | \- |
| <span data-ttu-id="48149-598">WINHTTP \_ OPTION \_ \_ CONNECT-WIEDERHOLUNGEN</span><span class="sxs-lookup"><span data-stu-id="48149-598">WINHTTP\_OPTION\_CONNECT\_RETRIES</span></span><br/><span data-ttu-id="48149-599">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-599">**DWORD**</span></span> | <span data-ttu-id="48149-600">X</span><span class="sxs-lookup"><span data-stu-id="48149-600">X</span></span> | <span data-ttu-id="48149-601">X</span><span class="sxs-lookup"><span data-stu-id="48149-601">X</span></span> | <span data-ttu-id="48149-602">X</span><span class="sxs-lookup"><span data-stu-id="48149-602">X</span></span> | <span data-ttu-id="48149-603">X</span><span class="sxs-lookup"><span data-stu-id="48149-603">X</span></span> | \- |
| <span data-ttu-id="48149-604">WINHTTP \_ OPTION \_ CONNECT \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="48149-604">WINHTTP\_OPTION\_CONNECT\_TIMEOUT</span></span><br/><span data-ttu-id="48149-605">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-605">**DWORD**</span></span> | <span data-ttu-id="48149-606">X</span><span class="sxs-lookup"><span data-stu-id="48149-606">X</span></span> | <span data-ttu-id="48149-607">X</span><span class="sxs-lookup"><span data-stu-id="48149-607">X</span></span> | <span data-ttu-id="48149-608">X</span><span class="sxs-lookup"><span data-stu-id="48149-608">X</span></span> | <span data-ttu-id="48149-609">X</span><span class="sxs-lookup"><span data-stu-id="48149-609">X</span></span> | \- |
| <span data-ttu-id="48149-610">\_ \_ WINHTTP-OPTIONSVERBINDUNGSINFORMATIONEN \_</span><span class="sxs-lookup"><span data-stu-id="48149-610">WINHTTP\_OPTION\_CONNECTION\_INFO</span></span><br/>[<span data-ttu-id="48149-611">**\_WINHTTP-VERBINDUNGSINFORMATIONEN \_**</span><span class="sxs-lookup"><span data-stu-id="48149-611">**WINHTTP\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | <span data-ttu-id="48149-612">X</span><span class="sxs-lookup"><span data-stu-id="48149-612">X</span></span> | <span data-ttu-id="48149-613">X</span><span class="sxs-lookup"><span data-stu-id="48149-613">X</span></span> | \- | \- |
| <span data-ttu-id="48149-614">WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V0</span><span class="sxs-lookup"><span data-stu-id="48149-614">WINHTTP\_OPTION\_CONNECTION\_STATS\_V0</span></span><br/>[<span data-ttu-id="48149-615">**TCP \_ INFO \_ v0**</span><span class="sxs-lookup"><span data-stu-id="48149-615">**TCP\_INFO\_v0**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | <span data-ttu-id="48149-616">X</span><span class="sxs-lookup"><span data-stu-id="48149-616">X</span></span> | <span data-ttu-id="48149-617">X</span><span class="sxs-lookup"><span data-stu-id="48149-617">X</span></span> | \- | <span data-ttu-id="48149-618">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="48149-618">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="48149-619">WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1</span><span class="sxs-lookup"><span data-stu-id="48149-619">WINHTTP\_OPTION\_CONNECTION\_STATS\_V1</span></span><br/>[<span data-ttu-id="48149-620">**TCP \_ INFO \_ v1**</span><span class="sxs-lookup"><span data-stu-id="48149-620">**TCP\_INFO\_v1**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | <span data-ttu-id="48149-621">X</span><span class="sxs-lookup"><span data-stu-id="48149-621">X</span></span> | <span data-ttu-id="48149-622">X</span><span class="sxs-lookup"><span data-stu-id="48149-622">X</span></span> | \- | <span data-ttu-id="48149-623">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="48149-623">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="48149-624">\_ \_ WINHTTP-OPTIONSKONTEXTWERT \_</span><span class="sxs-lookup"><span data-stu-id="48149-624">WINHTTP\_OPTION\_CONTEXT\_VALUE</span></span><br/><span data-ttu-id="48149-625">**DWORD \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="48149-625">**DWORD\_PTR**</span></span> | <span data-ttu-id="48149-626">X</span><span class="sxs-lookup"><span data-stu-id="48149-626">X</span></span> | <span data-ttu-id="48149-627">X</span><span class="sxs-lookup"><span data-stu-id="48149-627">X</span></span> | <span data-ttu-id="48149-628">X</span><span class="sxs-lookup"><span data-stu-id="48149-628">X</span></span> | <span data-ttu-id="48149-629">X</span><span class="sxs-lookup"><span data-stu-id="48149-629">X</span></span> | \- |
| <span data-ttu-id="48149-630">WINHTTP \_ OPTION \_ DEKOMPRIMIERUNG</span><span class="sxs-lookup"><span data-stu-id="48149-630">WINHTTP\_OPTION\_DECOMPRESSION</span></span><br/><span data-ttu-id="48149-631">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-631">**DWORD**</span></span> | <span data-ttu-id="48149-632">X</span><span class="sxs-lookup"><span data-stu-id="48149-632">X</span></span> | <span data-ttu-id="48149-633">X</span><span class="sxs-lookup"><span data-stu-id="48149-633">X</span></span> | \- | <span data-ttu-id="48149-634">X</span><span class="sxs-lookup"><span data-stu-id="48149-634">X</span></span> | <span data-ttu-id="48149-635">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="48149-635">Windows 8.1</span></span> |
| <span data-ttu-id="48149-636">WINHTTP \_ OPTION \_ DISABLE \_ FEATURE</span><span class="sxs-lookup"><span data-stu-id="48149-636">WINHTTP\_OPTION\_DISABLE\_FEATURE</span></span><br/><span data-ttu-id="48149-637">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-637">**DWORD**</span></span> | \- | <span data-ttu-id="48149-638">X</span><span class="sxs-lookup"><span data-stu-id="48149-638">X</span></span> | \- | <span data-ttu-id="48149-639">X</span><span class="sxs-lookup"><span data-stu-id="48149-639">X</span></span> | \- |
| <span data-ttu-id="48149-640">\_WINHTTP-OPTION \_ DISABLE SECURE \_ PROTOCOL \_ \_ FALLBACK</span><span class="sxs-lookup"><span data-stu-id="48149-640">WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK</span></span><br/><span data-ttu-id="48149-641">**Bool**</span><span class="sxs-lookup"><span data-stu-id="48149-641">**BOOL**</span></span> | <span data-ttu-id="48149-642">X</span><span class="sxs-lookup"><span data-stu-id="48149-642">X</span></span> | \- | \- | <span data-ttu-id="48149-643">X</span><span class="sxs-lookup"><span data-stu-id="48149-643">X</span></span> | <span data-ttu-id="48149-644">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="48149-644">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="48149-645">\_WINHTTP-OPTION \_ : DEAKTIVIEREN DER \_ \_ STREAMWARTESCHLANGE</span><span class="sxs-lookup"><span data-stu-id="48149-645">WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE</span></span><br/><span data-ttu-id="48149-646">**Bool**</span><span class="sxs-lookup"><span data-stu-id="48149-646">**BOOL**</span></span> | <span data-ttu-id="48149-647">X</span><span class="sxs-lookup"><span data-stu-id="48149-647">X</span></span> | <span data-ttu-id="48149-648">X</span><span class="sxs-lookup"><span data-stu-id="48149-648">X</span></span> | \- | <span data-ttu-id="48149-649">X</span><span class="sxs-lookup"><span data-stu-id="48149-649">X</span></span> | <span data-ttu-id="48149-650">Windows 10 Version 1809</span><span class="sxs-lookup"><span data-stu-id="48149-650">Windows 10 Version 1809</span></span> |
| <span data-ttu-id="48149-651">WINHTTP \_ OPTION \_ ENABLE \_ FEATURE</span><span class="sxs-lookup"><span data-stu-id="48149-651">WINHTTP\_OPTION\_ENABLE\_FEATURE</span></span><br/><span data-ttu-id="48149-652">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-652">**DWORD**</span></span> | \* | \* | \- | <span data-ttu-id="48149-653">X</span><span class="sxs-lookup"><span data-stu-id="48149-653">X</span></span> | \- |
| <span data-ttu-id="48149-654">\_WINHTTP-OPTION: \_ AKTIVIEREN DES \_ \_ HTTP-PROTOKOLLS</span><span class="sxs-lookup"><span data-stu-id="48149-654">WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL</span></span><br/><span data-ttu-id="48149-655">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-655">**DWORD**</span></span> | <span data-ttu-id="48149-656">X</span><span class="sxs-lookup"><span data-stu-id="48149-656">X</span></span> | <span data-ttu-id="48149-657">X</span><span class="sxs-lookup"><span data-stu-id="48149-657">X</span></span> | \- | <span data-ttu-id="48149-658">X</span><span class="sxs-lookup"><span data-stu-id="48149-658">X</span></span> | <span data-ttu-id="48149-659">Windows 10, Version 1607</span><span class="sxs-lookup"><span data-stu-id="48149-659">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="48149-660">\_WINHTTP-OPTION \_ ENABLETRACING</span><span class="sxs-lookup"><span data-stu-id="48149-660">WINHTTP\_OPTION\_ENABLETRACING</span></span><br/><span data-ttu-id="48149-661">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-661">**DWORD**</span></span> | \- | \- | <span data-ttu-id="48149-662">X</span><span class="sxs-lookup"><span data-stu-id="48149-662">X</span></span> | <span data-ttu-id="48149-663">X</span><span class="sxs-lookup"><span data-stu-id="48149-663">X</span></span> | \- |
| <span data-ttu-id="48149-664">WINHTTP \_ OPTION \_ ENCODE \_ EXTRA</span><span class="sxs-lookup"><span data-stu-id="48149-664">WINHTTP\_OPTION\_ENCODE\_EXTRA</span></span><br/><span data-ttu-id="48149-665">**Bool**</span><span class="sxs-lookup"><span data-stu-id="48149-665">**BOOL**</span></span> | <span data-ttu-id="48149-666">X</span><span class="sxs-lookup"><span data-stu-id="48149-666">X</span></span> | <span data-ttu-id="48149-667">X</span><span class="sxs-lookup"><span data-stu-id="48149-667">X</span></span> | \- | <span data-ttu-id="48149-668">X</span><span class="sxs-lookup"><span data-stu-id="48149-668">X</span></span> | <span data-ttu-id="48149-669">Windows 10 Version 1803</span><span class="sxs-lookup"><span data-stu-id="48149-669">Windows 10 Version 1803</span></span> |
| <span data-ttu-id="48149-670">\_WINHTTP-OPTION \_ LÄUFT VERBINDUNG AB \_</span><span class="sxs-lookup"><span data-stu-id="48149-670">WINHTTP\_OPTION\_EXPIRE\_CONNECTION</span></span><br/><span data-ttu-id="48149-671">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48149-671">N/A</span></span> | \- | <span data-ttu-id="48149-672">X</span><span class="sxs-lookup"><span data-stu-id="48149-672">X</span></span> | \- | <span data-ttu-id="48149-673">X</span><span class="sxs-lookup"><span data-stu-id="48149-673">X</span></span> | <span data-ttu-id="48149-674">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="48149-674">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="48149-675">\_ \_ ERWEITERTER \_ WINHTTP-OPTION-FEHLER</span><span class="sxs-lookup"><span data-stu-id="48149-675">WINHTTP\_OPTION\_EXTENDED\_ERROR</span></span><br/><span data-ttu-id="48149-676">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-676">**DWORD**</span></span> | <span data-ttu-id="48149-677">X</span><span class="sxs-lookup"><span data-stu-id="48149-677">X</span></span> | <span data-ttu-id="48149-678">X</span><span class="sxs-lookup"><span data-stu-id="48149-678">X</span></span> | <span data-ttu-id="48149-679">X</span><span class="sxs-lookup"><span data-stu-id="48149-679">X</span></span> | \- | \- |
| <span data-ttu-id="48149-680">WINHTTP \_ OPTION \_ GLOBAL \_ PROXY \_ CREDS</span><span class="sxs-lookup"><span data-stu-id="48149-680">WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS</span></span><br/>[<span data-ttu-id="48149-681">**WINHTTP \_ CREDS**</span><span class="sxs-lookup"><span data-stu-id="48149-681">**WINHTTP\_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | <span data-ttu-id="48149-682">X</span><span class="sxs-lookup"><span data-stu-id="48149-682">X</span></span> | <span data-ttu-id="48149-683">X</span><span class="sxs-lookup"><span data-stu-id="48149-683">X</span></span> | \- | <span data-ttu-id="48149-684">X</span><span class="sxs-lookup"><span data-stu-id="48149-684">X</span></span> | \- |
| <span data-ttu-id="48149-685">WINHTTP \_ OPTION \_ GLOBAL \_ SERVER \_ CREDS</span><span class="sxs-lookup"><span data-stu-id="48149-685">WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS</span></span><br/>[<span data-ttu-id="48149-686">**WINHTTP \_ CREDS \_ EX**</span><span class="sxs-lookup"><span data-stu-id="48149-686">**WINHTTP\_CREDS\_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | <span data-ttu-id="48149-687">X</span><span class="sxs-lookup"><span data-stu-id="48149-687">X</span></span> | <span data-ttu-id="48149-688">X</span><span class="sxs-lookup"><span data-stu-id="48149-688">X</span></span> | \- | <span data-ttu-id="48149-689">X</span><span class="sxs-lookup"><span data-stu-id="48149-689">X</span></span> | \- |
| <span data-ttu-id="48149-690">TYP DES \_ WINHTTP-OPTIONSHANDLE \_ \_</span><span class="sxs-lookup"><span data-stu-id="48149-690">WINHTTP\_OPTION\_HANDLE\_TYPE</span></span><br/><span data-ttu-id="48149-691">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-691">**DWORD**</span></span> | <span data-ttu-id="48149-692">X</span><span class="sxs-lookup"><span data-stu-id="48149-692">X</span></span> | <span data-ttu-id="48149-693">X</span><span class="sxs-lookup"><span data-stu-id="48149-693">X</span></span> | <span data-ttu-id="48149-694">X</span><span class="sxs-lookup"><span data-stu-id="48149-694">X</span></span> | \- | \- |
| <span data-ttu-id="48149-695">WINHTTP \_ OPTION HTTP PROTOCOL \_ \_ \_ ERFORDERLICH</span><span class="sxs-lookup"><span data-stu-id="48149-695">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED</span></span><br/><span data-ttu-id="48149-696">**Bool**</span><span class="sxs-lookup"><span data-stu-id="48149-696">**BOOL**</span></span> | <span data-ttu-id="48149-697">X</span><span class="sxs-lookup"><span data-stu-id="48149-697">X</span></span> | <span data-ttu-id="48149-698">X</span><span class="sxs-lookup"><span data-stu-id="48149-698">X</span></span> | \- | <span data-ttu-id="48149-699">X</span><span class="sxs-lookup"><span data-stu-id="48149-699">X</span></span> | <span data-ttu-id="48149-700">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="48149-700">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="48149-701">VERWENDETES \_ \_ HTTP-PROTOKOLL DER \_ WINHTTP-OPTION \_</span><span class="sxs-lookup"><span data-stu-id="48149-701">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED</span></span><br/><span data-ttu-id="48149-702">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-702">**DWORD**</span></span> | \- | <span data-ttu-id="48149-703">X</span><span class="sxs-lookup"><span data-stu-id="48149-703">X</span></span> | <span data-ttu-id="48149-704">X</span><span class="sxs-lookup"><span data-stu-id="48149-704">X</span></span> | \- | <span data-ttu-id="48149-705">Windows 10, Version 1607</span><span class="sxs-lookup"><span data-stu-id="48149-705">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="48149-706">\_HTTP-VERSION DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="48149-706">WINHTTP\_OPTION\_HTTP\_VERSION</span></span><br/>[<span data-ttu-id="48149-707">**\_ \_ HTTP-VERSIONSINFORMATIONEN**</span><span class="sxs-lookup"><span data-stu-id="48149-707">**HTTP\_VERSION\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | <span data-ttu-id="48149-708">X</span><span class="sxs-lookup"><span data-stu-id="48149-708">X</span></span> | <span data-ttu-id="48149-709">X</span><span class="sxs-lookup"><span data-stu-id="48149-709">X</span></span> | <span data-ttu-id="48149-710">X</span><span class="sxs-lookup"><span data-stu-id="48149-710">X</span></span> | <span data-ttu-id="48149-711">X</span><span class="sxs-lookup"><span data-stu-id="48149-711">X</span></span> | \- |
| <span data-ttu-id="48149-712">WINHTTP-OPTION \_ \_ \_ ZERTIFIKATSPERRUNG \_ \_ OFFLINE IGNORIEREN</span><span class="sxs-lookup"><span data-stu-id="48149-712">WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE</span></span><br/><span data-ttu-id="48149-713">**Bool**</span><span class="sxs-lookup"><span data-stu-id="48149-713">**BOOL**</span></span> | \- | <span data-ttu-id="48149-714">X</span><span class="sxs-lookup"><span data-stu-id="48149-714">X</span></span> | \- | <span data-ttu-id="48149-715">X</span><span class="sxs-lookup"><span data-stu-id="48149-715">X</span></span> | <span data-ttu-id="48149-716">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="48149-716">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="48149-717">WINHTTP-OPTION \_ \_ IPV6 \_ – SCHNELLER \_ FALLBACK</span><span class="sxs-lookup"><span data-stu-id="48149-717">WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK</span></span><br/><span data-ttu-id="48149-718">**Bool**</span><span class="sxs-lookup"><span data-stu-id="48149-718">**BOOL**</span></span> | <span data-ttu-id="48149-719">X</span><span class="sxs-lookup"><span data-stu-id="48149-719">X</span></span> | \- | \- | <span data-ttu-id="48149-720">X</span><span class="sxs-lookup"><span data-stu-id="48149-720">X</span></span> | <span data-ttu-id="48149-721">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="48149-721">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="48149-722">\_WINHTTP-OPTION \_ IST PROXY \_ \_ \_ CONNECT-ANTWORT</span><span class="sxs-lookup"><span data-stu-id="48149-722">WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="48149-723">**Bool**</span><span class="sxs-lookup"><span data-stu-id="48149-723">**BOOL**</span></span> | <span data-ttu-id="48149-724">X</span><span class="sxs-lookup"><span data-stu-id="48149-724">X</span></span> | <span data-ttu-id="48149-725">X</span><span class="sxs-lookup"><span data-stu-id="48149-725">X</span></span> | <span data-ttu-id="48149-726">X</span><span class="sxs-lookup"><span data-stu-id="48149-726">X</span></span> | \- | \- |
| <span data-ttu-id="48149-727">\_WINHTTP-OPTION \_ \_ MAX. CONNS \_ PRO \_ 1 \_ 0 \_ SERVER</span><span class="sxs-lookup"><span data-stu-id="48149-727">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER</span></span><br/><span data-ttu-id="48149-728">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-728">**DWORD**</span></span> | <span data-ttu-id="48149-729">X</span><span class="sxs-lookup"><span data-stu-id="48149-729">X</span></span> | \- | <span data-ttu-id="48149-730">X</span><span class="sxs-lookup"><span data-stu-id="48149-730">X</span></span> | <span data-ttu-id="48149-731">X</span><span class="sxs-lookup"><span data-stu-id="48149-731">X</span></span> | \- |
| <span data-ttu-id="48149-732">\_WINHTTP-OPTION \_ \_ MAX. CONNS \_ PRO \_ SERVER</span><span class="sxs-lookup"><span data-stu-id="48149-732">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER</span></span><br/><span data-ttu-id="48149-733">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-733">**DWORD**</span></span> | <span data-ttu-id="48149-734">X</span><span class="sxs-lookup"><span data-stu-id="48149-734">X</span></span> | \- | <span data-ttu-id="48149-735">X</span><span class="sxs-lookup"><span data-stu-id="48149-735">X</span></span> | <span data-ttu-id="48149-736">X</span><span class="sxs-lookup"><span data-stu-id="48149-736">X</span></span> | \- |
| <span data-ttu-id="48149-737">WINHTTP-OPTION \_ \_ \_ MAX. AUTOMATISCHE \_ \_ HTTP-UMLEITUNGEN</span><span class="sxs-lookup"><span data-stu-id="48149-737">WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS</span></span><br/><span data-ttu-id="48149-738">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-738">**DWORD**</span></span> | <span data-ttu-id="48149-739">X</span><span class="sxs-lookup"><span data-stu-id="48149-739">X</span></span> | <span data-ttu-id="48149-740">X</span><span class="sxs-lookup"><span data-stu-id="48149-740">X</span></span> | <span data-ttu-id="48149-741">X</span><span class="sxs-lookup"><span data-stu-id="48149-741">X</span></span> | <span data-ttu-id="48149-742">X</span><span class="sxs-lookup"><span data-stu-id="48149-742">X</span></span> | \- |
| <span data-ttu-id="48149-743">\_WINHTTP-OPTION \_ \_ MAX. \_ HTTP-STATUS \_ CONTINUE</span><span class="sxs-lookup"><span data-stu-id="48149-743">WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE</span></span><br/><span data-ttu-id="48149-744">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-744">**DWORD**</span></span> | <span data-ttu-id="48149-745">X</span><span class="sxs-lookup"><span data-stu-id="48149-745">X</span></span> | <span data-ttu-id="48149-746">X</span><span class="sxs-lookup"><span data-stu-id="48149-746">X</span></span> | <span data-ttu-id="48149-747">X</span><span class="sxs-lookup"><span data-stu-id="48149-747">X</span></span> | <span data-ttu-id="48149-748">X</span><span class="sxs-lookup"><span data-stu-id="48149-748">X</span></span> | \- |
| <span data-ttu-id="48149-749">WINHTTP \_ OPTION \_ MAX \_ RESPONSE \_ DRAIN \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="48149-749">WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE</span></span><br/><span data-ttu-id="48149-750">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-750">**DWORD**</span></span> | <span data-ttu-id="48149-751">X</span><span class="sxs-lookup"><span data-stu-id="48149-751">X</span></span> | <span data-ttu-id="48149-752">X</span><span class="sxs-lookup"><span data-stu-id="48149-752">X</span></span> | <span data-ttu-id="48149-753">X</span><span class="sxs-lookup"><span data-stu-id="48149-753">X</span></span> | <span data-ttu-id="48149-754">X</span><span class="sxs-lookup"><span data-stu-id="48149-754">X</span></span> | \- |
| <span data-ttu-id="48149-755">MAXIMALE GRÖßE DES \_ \_ \_ \_ ANTWORTHEADERS DER \_ WINHTTP-OPTION</span><span class="sxs-lookup"><span data-stu-id="48149-755">WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE</span></span><br/><span data-ttu-id="48149-756">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-756">**DWORD**</span></span> | <span data-ttu-id="48149-757">X</span><span class="sxs-lookup"><span data-stu-id="48149-757">X</span></span> | <span data-ttu-id="48149-758">X</span><span class="sxs-lookup"><span data-stu-id="48149-758">X</span></span> | <span data-ttu-id="48149-759">X</span><span class="sxs-lookup"><span data-stu-id="48149-759">X</span></span> | <span data-ttu-id="48149-760">X</span><span class="sxs-lookup"><span data-stu-id="48149-760">X</span></span> | \- |
| <span data-ttu-id="48149-761">ÜBERGEORDNETES \_ HANDLE DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="48149-761">WINHTTP\_OPTION\_PARENT\_HANDLE</span></span><br/>[<span data-ttu-id="48149-762">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="48149-762">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="48149-763">X</span><span class="sxs-lookup"><span data-stu-id="48149-763">X</span></span> | <span data-ttu-id="48149-764">X</span><span class="sxs-lookup"><span data-stu-id="48149-764">X</span></span> | <span data-ttu-id="48149-765">X</span><span class="sxs-lookup"><span data-stu-id="48149-765">X</span></span> | \- | \- |
| <span data-ttu-id="48149-766">\_WINHTTP-OPTION \_ \_ PASSPORT-COBRANDINGTEXT \_</span><span class="sxs-lookup"><span data-stu-id="48149-766">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT</span></span><br/><span data-ttu-id="48149-767">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="48149-767">**LPWSTR**</span></span> | \- | <span data-ttu-id="48149-768">X</span><span class="sxs-lookup"><span data-stu-id="48149-768">X</span></span> | <span data-ttu-id="48149-769">X</span><span class="sxs-lookup"><span data-stu-id="48149-769">X</span></span> | \- | \- |
| <span data-ttu-id="48149-770">\_WINHTTP-OPTION \_ \_ PASSPORT-COBRANDING-URL \_</span><span class="sxs-lookup"><span data-stu-id="48149-770">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL</span></span><br/><span data-ttu-id="48149-771">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="48149-771">**LPWSTR**</span></span> | \- | <span data-ttu-id="48149-772">X</span><span class="sxs-lookup"><span data-stu-id="48149-772">X</span></span> | <span data-ttu-id="48149-773">X</span><span class="sxs-lookup"><span data-stu-id="48149-773">X</span></span> | \- | \- |
| <span data-ttu-id="48149-774">\_WINHTTP-OPTION \_ \_ \_ PASSPORT-RÜCKGABE-URL</span><span class="sxs-lookup"><span data-stu-id="48149-774">WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL</span></span><br/><span data-ttu-id="48149-775">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="48149-775">**LPVOID**</span></span> | \- | <span data-ttu-id="48149-776">X</span><span class="sxs-lookup"><span data-stu-id="48149-776">X</span></span> | <span data-ttu-id="48149-777">X</span><span class="sxs-lookup"><span data-stu-id="48149-777">X</span></span> | \- | \- |
| <span data-ttu-id="48149-778">\_WINHTTP-OPTION \_ \_ \_ PASSPORT-ABMELDEN</span><span class="sxs-lookup"><span data-stu-id="48149-778">WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT</span></span><br/><span data-ttu-id="48149-779">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="48149-779">**LPVOID**</span></span> | <span data-ttu-id="48149-780">X</span><span class="sxs-lookup"><span data-stu-id="48149-780">X</span></span> | \- | \- | <span data-ttu-id="48149-781">X</span><span class="sxs-lookup"><span data-stu-id="48149-781">X</span></span> | \- |
| <span data-ttu-id="48149-782">\_ \_ WINHTTP-OPTIONSKENNWORT</span><span class="sxs-lookup"><span data-stu-id="48149-782">WINHTTP\_OPTION\_PASSWORD</span></span><br/><span data-ttu-id="48149-783">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="48149-783">**LPWSTR**</span></span> | \- | <span data-ttu-id="48149-784">X</span><span class="sxs-lookup"><span data-stu-id="48149-784">X</span></span> | <span data-ttu-id="48149-785">X</span><span class="sxs-lookup"><span data-stu-id="48149-785">X</span></span> | <span data-ttu-id="48149-786">X</span><span class="sxs-lookup"><span data-stu-id="48149-786">X</span></span> | \- |
| <span data-ttu-id="48149-787">\_WINHTTP-OPTIONSPROXY \_</span><span class="sxs-lookup"><span data-stu-id="48149-787">WINHTTP\_OPTION\_PROXY</span></span><br/>[<span data-ttu-id="48149-788">**\_WINHTTP-PROXYINFORMATIONEN \_**</span><span class="sxs-lookup"><span data-stu-id="48149-788">**WINHTTP\_PROXY\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | <span data-ttu-id="48149-789">X</span><span class="sxs-lookup"><span data-stu-id="48149-789">X</span></span> | <span data-ttu-id="48149-790">X</span><span class="sxs-lookup"><span data-stu-id="48149-790">X</span></span> | <span data-ttu-id="48149-791">X</span><span class="sxs-lookup"><span data-stu-id="48149-791">X</span></span> | <span data-ttu-id="48149-792">X</span><span class="sxs-lookup"><span data-stu-id="48149-792">X</span></span> | \- |
| <span data-ttu-id="48149-793">\_PROXYKENNWORT \_ FÜR WINHTTP-OPTION \_</span><span class="sxs-lookup"><span data-stu-id="48149-793">WINHTTP\_OPTION\_PROXY\_PASSWORD</span></span><br/><span data-ttu-id="48149-794">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="48149-794">**LPWSTR**</span></span> | \- | <span data-ttu-id="48149-795">X</span><span class="sxs-lookup"><span data-stu-id="48149-795">X</span></span> | <span data-ttu-id="48149-796">X</span><span class="sxs-lookup"><span data-stu-id="48149-796">X</span></span> | <span data-ttu-id="48149-797">X</span><span class="sxs-lookup"><span data-stu-id="48149-797">X</span></span> | \- |
| <span data-ttu-id="48149-798">VERWENDETER \_ \_ WINHTTP-OPTIONSPROXY-SPN \_ \_</span><span class="sxs-lookup"><span data-stu-id="48149-798">WINHTTP\_OPTION\_PROXY\_SPN\_USED</span></span><br/><span data-ttu-id="48149-799">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="48149-799">**LPWSTR**</span></span> | \- | <span data-ttu-id="48149-800">X</span><span class="sxs-lookup"><span data-stu-id="48149-800">X</span></span> | <span data-ttu-id="48149-801">X</span><span class="sxs-lookup"><span data-stu-id="48149-801">X</span></span> | \- | \- |
| <span data-ttu-id="48149-802">\_PROXYBENUTZERNAME DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="48149-802">WINHTTP\_OPTION\_PROXY\_USERNAME</span></span><br/><span data-ttu-id="48149-803">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="48149-803">**LPWSTR**</span></span> | \- | <span data-ttu-id="48149-804">X</span><span class="sxs-lookup"><span data-stu-id="48149-804">X</span></span> | <span data-ttu-id="48149-805">X</span><span class="sxs-lookup"><span data-stu-id="48149-805">X</span></span> | <span data-ttu-id="48149-806">X</span><span class="sxs-lookup"><span data-stu-id="48149-806">X</span></span> | \- |
| <span data-ttu-id="48149-807">WINHTTP-OPTION \_ \_ READ BUFFER \_ \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="48149-807">WINHTTP\_OPTION\_READ\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="48149-808">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-808">**DWORD**</span></span> | \- | <span data-ttu-id="48149-809">X</span><span class="sxs-lookup"><span data-stu-id="48149-809">X</span></span> | <span data-ttu-id="48149-810">X</span><span class="sxs-lookup"><span data-stu-id="48149-810">X</span></span> | <span data-ttu-id="48149-811">X</span><span class="sxs-lookup"><span data-stu-id="48149-811">X</span></span> | \- |
| <span data-ttu-id="48149-812">WINHTTP-OPTION \_ \_ "PROXY \_ \_ CONNECT-ANTWORT \_ EMPFANGEN"</span><span class="sxs-lookup"><span data-stu-id="48149-812">WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="48149-813">**Bool**</span><span class="sxs-lookup"><span data-stu-id="48149-813">**BOOL**</span></span> | <span data-ttu-id="48149-814">X</span><span class="sxs-lookup"><span data-stu-id="48149-814">X</span></span> | <span data-ttu-id="48149-815">X</span><span class="sxs-lookup"><span data-stu-id="48149-815">X</span></span> | \- | <span data-ttu-id="48149-816">X</span><span class="sxs-lookup"><span data-stu-id="48149-816">X</span></span> | \- |
| <span data-ttu-id="48149-817">WINHTTP-OPTION \_ \_ \_ \_ EMPFANGSANTWORTZEITÜBERSCHREITUNG</span><span class="sxs-lookup"><span data-stu-id="48149-817">WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT</span></span><br/><span data-ttu-id="48149-818">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-818">**DWORD**</span></span> | <span data-ttu-id="48149-819">X</span><span class="sxs-lookup"><span data-stu-id="48149-819">X</span></span> | <span data-ttu-id="48149-820">X</span><span class="sxs-lookup"><span data-stu-id="48149-820">X</span></span> | <span data-ttu-id="48149-821">X</span><span class="sxs-lookup"><span data-stu-id="48149-821">X</span></span> | <span data-ttu-id="48149-822">X</span><span class="sxs-lookup"><span data-stu-id="48149-822">X</span></span> | \- |
| <span data-ttu-id="48149-823">\_EMPFANGSZEITÜBERSCHREITUNG DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="48149-823">WINHTTP\_OPTION\_RECEIVE\_TIMEOUT</span></span><br/><span data-ttu-id="48149-824">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-824">**DWORD**</span></span> | <span data-ttu-id="48149-825">X</span><span class="sxs-lookup"><span data-stu-id="48149-825">X</span></span> | <span data-ttu-id="48149-826">X</span><span class="sxs-lookup"><span data-stu-id="48149-826">X</span></span> | <span data-ttu-id="48149-827">X</span><span class="sxs-lookup"><span data-stu-id="48149-827">X</span></span> | <span data-ttu-id="48149-828">X</span><span class="sxs-lookup"><span data-stu-id="48149-828">X</span></span> | \- |
| <span data-ttu-id="48149-829">UMLEITUNGSRICHTLINIE \_ FÜR WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="48149-829">WINHTTP\_OPTION\_REDIRECT\_POLICY</span></span><br/><span data-ttu-id="48149-830">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-830">**DWORD**</span></span> | <span data-ttu-id="48149-831">X</span><span class="sxs-lookup"><span data-stu-id="48149-831">X</span></span> | <span data-ttu-id="48149-832">X</span><span class="sxs-lookup"><span data-stu-id="48149-832">X</span></span> | <span data-ttu-id="48149-833">X</span><span class="sxs-lookup"><span data-stu-id="48149-833">X</span></span> | <span data-ttu-id="48149-834">X</span><span class="sxs-lookup"><span data-stu-id="48149-834">X</span></span> | \- |
| <span data-ttu-id="48149-835">\_WINHTTP-OPTION \_ BENUTZER IN URL \_ \_ \_ ABLEHNENPWD</span><span class="sxs-lookup"><span data-stu-id="48149-835">WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL</span></span><br/><span data-ttu-id="48149-836">**Bool**</span><span class="sxs-lookup"><span data-stu-id="48149-836">**BOOL**</span></span> | \- | <span data-ttu-id="48149-837">X</span><span class="sxs-lookup"><span data-stu-id="48149-837">X</span></span> | \- | <span data-ttu-id="48149-838">X</span><span class="sxs-lookup"><span data-stu-id="48149-838">X</span></span> | \- |
| <span data-ttu-id="48149-839">\_ \_ ANFORDERUNGSPRIORITÄT DER WINHTTP-OPTION \_</span><span class="sxs-lookup"><span data-stu-id="48149-839">WINHTTP\_OPTION\_REQUEST\_PRIORITY</span></span><br/><span data-ttu-id="48149-840">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-840">**DWORD**</span></span> | \- | <span data-ttu-id="48149-841">X</span><span class="sxs-lookup"><span data-stu-id="48149-841">X</span></span> | <span data-ttu-id="48149-842">X</span><span class="sxs-lookup"><span data-stu-id="48149-842">X</span></span> | <span data-ttu-id="48149-843">X</span><span class="sxs-lookup"><span data-stu-id="48149-843">X</span></span> | \- |
| <span data-ttu-id="48149-844">\_ \_ WINHTTP-OPTIONSANFORDERUNGSSTATISTIKEN \_</span><span class="sxs-lookup"><span data-stu-id="48149-844">WINHTTP\_OPTION\_REQUEST\_STATS</span></span><br/>[<span data-ttu-id="48149-845">**\_ \_ WINHTTP-ANFORDERUNGSSTATISTIKEN**</span><span class="sxs-lookup"><span data-stu-id="48149-845">**WINHTTP\_REQUEST\_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | <span data-ttu-id="48149-846">X</span><span class="sxs-lookup"><span data-stu-id="48149-846">X</span></span> | <span data-ttu-id="48149-847">X</span><span class="sxs-lookup"><span data-stu-id="48149-847">X</span></span> | \- | <span data-ttu-id="48149-848">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="48149-848">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="48149-849">ANFORDERUNGSZEITEN \_ DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="48149-849">WINHTTP\_OPTION\_REQUEST\_TIMES</span></span><br/>[<span data-ttu-id="48149-850">**\_WINHTTP-ANFORDERUNGSZEITEN \_**</span><span class="sxs-lookup"><span data-stu-id="48149-850">**WINHTTP\_REQUEST\_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | <span data-ttu-id="48149-851">X</span><span class="sxs-lookup"><span data-stu-id="48149-851">X</span></span> | <span data-ttu-id="48149-852">X</span><span class="sxs-lookup"><span data-stu-id="48149-852">X</span></span> | \- | <span data-ttu-id="48149-853">Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="48149-853">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="48149-854">WINHTTP-OPTION \_ \_ \_ TIMEOUT AUFLÖSEN</span><span class="sxs-lookup"><span data-stu-id="48149-854">WINHTTP\_OPTION\_RESOLVE\_TIMEOUT</span></span><br/><span data-ttu-id="48149-855">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-855">**DWORD**</span></span> | <span data-ttu-id="48149-856">X</span><span class="sxs-lookup"><span data-stu-id="48149-856">X</span></span> | <span data-ttu-id="48149-857">X</span><span class="sxs-lookup"><span data-stu-id="48149-857">X</span></span> | <span data-ttu-id="48149-858">X</span><span class="sxs-lookup"><span data-stu-id="48149-858">X</span></span> | <span data-ttu-id="48149-859">X</span><span class="sxs-lookup"><span data-stu-id="48149-859">X</span></span> | \- |
| <span data-ttu-id="48149-860">SICHERE PROTOKOLLE \_ DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="48149-860">WINHTTP\_OPTION\_SECURE\_PROTOCOLS</span></span><br/><span data-ttu-id="48149-861">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-861">**DWORD**</span></span> | <span data-ttu-id="48149-862">X</span><span class="sxs-lookup"><span data-stu-id="48149-862">X</span></span> | \- | \- | <span data-ttu-id="48149-863">X</span><span class="sxs-lookup"><span data-stu-id="48149-863">X</span></span> | \- |
| <span data-ttu-id="48149-864">\_SICHERHEITSZERTIFIKATSTRUKTUR DER WINHTTP-OPTION \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="48149-864">WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT</span></span><br/>[<span data-ttu-id="48149-865">**\_WINHTTP-ZERTIFIKATINFORMATIONEN \_**</span><span class="sxs-lookup"><span data-stu-id="48149-865">**WINHTTP\_CERTIFICATE\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | <span data-ttu-id="48149-866">X</span><span class="sxs-lookup"><span data-stu-id="48149-866">X</span></span> | <span data-ttu-id="48149-867">X</span><span class="sxs-lookup"><span data-stu-id="48149-867">X</span></span> | \- | \- |
| <span data-ttu-id="48149-868">\_SICHERHEITSFLAGS FÜR DIE WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="48149-868">WINHTTP\_OPTION\_SECURITY\_FLAGS</span></span><br/><span data-ttu-id="48149-869">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-869">**DWORD**</span></span> | \- | <span data-ttu-id="48149-870">X</span><span class="sxs-lookup"><span data-stu-id="48149-870">X</span></span> | <span data-ttu-id="48149-871">X</span><span class="sxs-lookup"><span data-stu-id="48149-871">X</span></span> | <span data-ttu-id="48149-872">X</span><span class="sxs-lookup"><span data-stu-id="48149-872">X</span></span> | \- |
| <span data-ttu-id="48149-873">SICHERHEITSINFORMATIONEN \_ ZUR WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="48149-873">WINHTTP\_OPTION\_SECURITY\_INFO</span></span><br/>[<span data-ttu-id="48149-874">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="48149-874">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | <span data-ttu-id="48149-875">X</span><span class="sxs-lookup"><span data-stu-id="48149-875">X</span></span> | <span data-ttu-id="48149-876">X</span><span class="sxs-lookup"><span data-stu-id="48149-876">X</span></span> | \- | <span data-ttu-id="48149-877">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="48149-877">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="48149-878">\_WINHTTP-OPTION \_ \_ \_ SICHERHEITSSCHLÜSSELBITNESS</span><span class="sxs-lookup"><span data-stu-id="48149-878">WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS</span></span><br/><span data-ttu-id="48149-879">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-879">**DWORD**</span></span> | \- | <span data-ttu-id="48149-880">X</span><span class="sxs-lookup"><span data-stu-id="48149-880">X</span></span> | <span data-ttu-id="48149-881">X</span><span class="sxs-lookup"><span data-stu-id="48149-881">X</span></span> | \- | \- |
| <span data-ttu-id="48149-882">TIMEOUT \_ BEIM SENDEN DER \_ \_ WINHTTP-OPTION</span><span class="sxs-lookup"><span data-stu-id="48149-882">WINHTTP\_OPTION\_SEND\_TIMEOUT</span></span><br/><span data-ttu-id="48149-883">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-883">**DWORD**</span></span> | <span data-ttu-id="48149-884">X</span><span class="sxs-lookup"><span data-stu-id="48149-884">X</span></span> | <span data-ttu-id="48149-885">X</span><span class="sxs-lookup"><span data-stu-id="48149-885">X</span></span> | <span data-ttu-id="48149-886">X</span><span class="sxs-lookup"><span data-stu-id="48149-886">X</span></span> | <span data-ttu-id="48149-887">X</span><span class="sxs-lookup"><span data-stu-id="48149-887">X</span></span> | \- |
| <span data-ttu-id="48149-888">WINHTTP \_ OPTION \_ SERVER \_ CBT</span><span class="sxs-lookup"><span data-stu-id="48149-888">WINHTTP\_OPTION\_SERVER\_CBT</span></span><br/><span data-ttu-id="48149-889">[**\_SecPkgContext-Bindungen**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span><span class="sxs-lookup"><span data-stu-id="48149-889">[**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span></span> | \- | <span data-ttu-id="48149-890">X</span><span class="sxs-lookup"><span data-stu-id="48149-890">X</span></span> | <span data-ttu-id="48149-891">X</span><span class="sxs-lookup"><span data-stu-id="48149-891">X</span></span> | \- | \- |
| <span data-ttu-id="48149-892">WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CHAIN \_ CONTEXT</span><span class="sxs-lookup"><span data-stu-id="48149-892">WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT</span></span><br/>[<span data-ttu-id="48149-893">**CERT_CHAIN_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="48149-893">**CERT_CHAIN_CONTEXT**</span></span>](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | <span data-ttu-id="48149-894">X</span><span class="sxs-lookup"><span data-stu-id="48149-894">X</span></span> | <span data-ttu-id="48149-895">X</span><span class="sxs-lookup"><span data-stu-id="48149-895">X</span></span> | \- | <span data-ttu-id="48149-896">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="48149-896">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="48149-897">WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CONTEXT</span><span class="sxs-lookup"><span data-stu-id="48149-897">WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="48149-898">**CERT-KONTEXT**</span><span class="sxs-lookup"><span data-stu-id="48149-898">**CERT CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="48149-899">X</span><span class="sxs-lookup"><span data-stu-id="48149-899">X</span></span> | <span data-ttu-id="48149-900">X</span><span class="sxs-lookup"><span data-stu-id="48149-900">X</span></span> | \- | \- |
| <span data-ttu-id="48149-901">VERWENDETER \_ \_ WINHTTP-OPTIONSSERVER-SPN \_ \_</span><span class="sxs-lookup"><span data-stu-id="48149-901">WINHTTP\_OPTION\_SERVER\_SPN\_USED</span></span><br/><span data-ttu-id="48149-902">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="48149-902">**LPWSTR**</span></span> | \- | <span data-ttu-id="48149-903">X</span><span class="sxs-lookup"><span data-stu-id="48149-903">X</span></span> | <span data-ttu-id="48149-904">X</span><span class="sxs-lookup"><span data-stu-id="48149-904">X</span></span> | \- | \- |
| <span data-ttu-id="48149-905">\_ \_ WINHTTP-OPTIONS-SPN</span><span class="sxs-lookup"><span data-stu-id="48149-905">WINHTTP\_OPTION\_SPN</span></span><br/><span data-ttu-id="48149-906">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-906">**DWORD**</span></span> | \- | <span data-ttu-id="48149-907">X</span><span class="sxs-lookup"><span data-stu-id="48149-907">X</span></span> | \- | <span data-ttu-id="48149-908">X</span><span class="sxs-lookup"><span data-stu-id="48149-908">X</span></span> | \- |
| <span data-ttu-id="48149-909">WINHTTP-OPTION \_ \_ TCP FAST \_ \_ OPEN</span><span class="sxs-lookup"><span data-stu-id="48149-909">WINHTTP\_OPTION\_TCP\_FAST\_OPEN</span></span><br/><span data-ttu-id="48149-910">**Bool**</span><span class="sxs-lookup"><span data-stu-id="48149-910">**BOOL**</span></span> | <span data-ttu-id="48149-911">X</span><span class="sxs-lookup"><span data-stu-id="48149-911">X</span></span> | \- | \- | <span data-ttu-id="48149-912">X</span><span class="sxs-lookup"><span data-stu-id="48149-912">X</span></span> | <span data-ttu-id="48149-913">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="48149-913">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="48149-914">\_WINHTTP-OPTION \_ TCP \_ KEEPALIVE</span><span class="sxs-lookup"><span data-stu-id="48149-914">WINHTTP\_OPTION\_TCP\_KEEPALIVE</span></span><br/>[<span data-ttu-id="48149-915">**tcp \_ keepalive**</span><span class="sxs-lookup"><span data-stu-id="48149-915">**tcp\_keepalive**</span></span>](/windows/win32/winsock/sio-keepalive-vals) | <span data-ttu-id="48149-916">X</span><span class="sxs-lookup"><span data-stu-id="48149-916">X</span></span> | \- | \- | <span data-ttu-id="48149-917">X</span><span class="sxs-lookup"><span data-stu-id="48149-917">X</span></span> | <span data-ttu-id="48149-918">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="48149-918">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="48149-919">WINHTTP-OPTION \_ \_ TLS FALSE \_ \_ START</span><span class="sxs-lookup"><span data-stu-id="48149-919">WINHTTP\_OPTION\_TLS\_FALSE\_START</span></span><br/><span data-ttu-id="48149-920">**Bool**</span><span class="sxs-lookup"><span data-stu-id="48149-920">**BOOL**</span></span> | <span data-ttu-id="48149-921">X</span><span class="sxs-lookup"><span data-stu-id="48149-921">X</span></span> | \- | \- | <span data-ttu-id="48149-922">X</span><span class="sxs-lookup"><span data-stu-id="48149-922">X</span></span> | <span data-ttu-id="48149-923">Windows 10 Version 2004</span><span class="sxs-lookup"><span data-stu-id="48149-923">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="48149-924">WINHTTP-OPTION \_ \_ \_ ENTLADEBENACHRICHTIGUNGSEREIGNIS \_</span><span class="sxs-lookup"><span data-stu-id="48149-924">WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT</span></span><br/>[<span data-ttu-id="48149-925">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="48149-925">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="48149-926">X</span><span class="sxs-lookup"><span data-stu-id="48149-926">X</span></span> | \- | \- | <span data-ttu-id="48149-927">X</span><span class="sxs-lookup"><span data-stu-id="48149-927">X</span></span> | \- |
| <span data-ttu-id="48149-928">WINHTTP \_ OPTION \_ UNSAFE \_ HEADER \_ PARSING</span><span class="sxs-lookup"><span data-stu-id="48149-928">WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING</span></span><br/><span data-ttu-id="48149-929">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-929">**DWORD**</span></span> | \- | <span data-ttu-id="48149-930">X</span><span class="sxs-lookup"><span data-stu-id="48149-930">X</span></span> | \- | <span data-ttu-id="48149-931">X</span><span class="sxs-lookup"><span data-stu-id="48149-931">X</span></span> | \- |
| <span data-ttu-id="48149-932">UPGRADE DER \_ \_ WINHTTP-OPTION \_ AUF \_ \_ WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="48149-932">WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET</span></span><br/><span data-ttu-id="48149-933">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48149-933">N/A</span></span> | \- | <span data-ttu-id="48149-934">X</span><span class="sxs-lookup"><span data-stu-id="48149-934">X</span></span> | \- | <span data-ttu-id="48149-935">X</span><span class="sxs-lookup"><span data-stu-id="48149-935">X</span></span> | \- |
| <span data-ttu-id="48149-936">URL DER \_ \_ WINHTTP-OPTION</span><span class="sxs-lookup"><span data-stu-id="48149-936">WINHTTP\_OPTION\_URL</span></span><br/><span data-ttu-id="48149-937">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="48149-937">**LPWSTR**</span></span> | \- | <span data-ttu-id="48149-938">X</span><span class="sxs-lookup"><span data-stu-id="48149-938">X</span></span> | <span data-ttu-id="48149-939">X</span><span class="sxs-lookup"><span data-stu-id="48149-939">X</span></span> | \- | \- |
| <span data-ttu-id="48149-940">WINHTTP-OPTION \_ \_ GLOBALE \_ SERVERANMELDEINFORMATIONEN \_ \_ VERWENDEN</span><span class="sxs-lookup"><span data-stu-id="48149-940">WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS</span></span><br/><span data-ttu-id="48149-941">**Bool**</span><span class="sxs-lookup"><span data-stu-id="48149-941">**BOOL**</span></span> | <span data-ttu-id="48149-942">X</span><span class="sxs-lookup"><span data-stu-id="48149-942">X</span></span> | <span data-ttu-id="48149-943">X</span><span class="sxs-lookup"><span data-stu-id="48149-943">X</span></span> | \- | <span data-ttu-id="48149-944">X</span><span class="sxs-lookup"><span data-stu-id="48149-944">X</span></span> | \- |
| <span data-ttu-id="48149-945">\_BENUTZER-AGENT DER WINHTTP-OPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="48149-945">WINHTTP\_OPTION\_USER\_AGENT</span></span><br/><span data-ttu-id="48149-946">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="48149-946">**LPWSTR**</span></span> | <span data-ttu-id="48149-947">X</span><span class="sxs-lookup"><span data-stu-id="48149-947">X</span></span> | \- | <span data-ttu-id="48149-948">X</span><span class="sxs-lookup"><span data-stu-id="48149-948">X</span></span> | <span data-ttu-id="48149-949">X</span><span class="sxs-lookup"><span data-stu-id="48149-949">X</span></span> | \- |
| <span data-ttu-id="48149-950">\_ \_ WINHTTP-OPTIONSBENUTZERNAME</span><span class="sxs-lookup"><span data-stu-id="48149-950">WINHTTP\_OPTION\_USERNAME</span></span><br/><span data-ttu-id="48149-951">**Lpwstr**</span><span class="sxs-lookup"><span data-stu-id="48149-951">**LPWSTR**</span></span> | \- | <span data-ttu-id="48149-952">X</span><span class="sxs-lookup"><span data-stu-id="48149-952">X</span></span> | <span data-ttu-id="48149-953">X</span><span class="sxs-lookup"><span data-stu-id="48149-953">X</span></span> | <span data-ttu-id="48149-954">X</span><span class="sxs-lookup"><span data-stu-id="48149-954">X</span></span> | \- |
| <span data-ttu-id="48149-955">\_WINHTTP-OPTION: \_ \_ TIMEOUT BEIM \_ SCHLIEßEN DES WEBSOCKET \_</span><span class="sxs-lookup"><span data-stu-id="48149-955">WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT</span></span><br/><span data-ttu-id="48149-956">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-956">**DWORD**</span></span> | \- | \- | <span data-ttu-id="48149-957">X</span><span class="sxs-lookup"><span data-stu-id="48149-957">X</span></span> | <span data-ttu-id="48149-958">X</span><span class="sxs-lookup"><span data-stu-id="48149-958">X</span></span> | \- |
| <span data-ttu-id="48149-959">WINHTTP-OPTION \_ \_ \_ WEBSOCKET \_ KEEPALIVE \_ INTERVAL</span><span class="sxs-lookup"><span data-stu-id="48149-959">WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL</span></span><br/><span data-ttu-id="48149-960">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-960">**DWORD**</span></span> | \- | \- | <span data-ttu-id="48149-961">X</span><span class="sxs-lookup"><span data-stu-id="48149-961">X</span></span> | <span data-ttu-id="48149-962">X</span><span class="sxs-lookup"><span data-stu-id="48149-962">X</span></span> | \- |
| <span data-ttu-id="48149-963">WINHTTP-OPTION \_ \_ \_ WEBSOCKET \_ \_ \_ EMPFANGSPUFFERGRÖßE</span><span class="sxs-lookup"><span data-stu-id="48149-963">WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="48149-964">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-964">**DWORD**</span></span> | <span data-ttu-id="48149-965">X</span><span class="sxs-lookup"><span data-stu-id="48149-965">X</span></span> | <span data-ttu-id="48149-966">X</span><span class="sxs-lookup"><span data-stu-id="48149-966">X</span></span> | <span data-ttu-id="48149-967">X</span><span class="sxs-lookup"><span data-stu-id="48149-967">X</span></span> | <span data-ttu-id="48149-968">X</span><span class="sxs-lookup"><span data-stu-id="48149-968">X</span></span> | <span data-ttu-id="48149-969">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="48149-969">Windows 8.1</span></span> |
| <span data-ttu-id="48149-970">WINHTTP-OPTION \_ \_ \_ WEBSOCKET- \_ \_ \_ SENDEPUFFERGRÖßE</span><span class="sxs-lookup"><span data-stu-id="48149-970">WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="48149-971">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-971">**DWORD**</span></span> | <span data-ttu-id="48149-972">X</span><span class="sxs-lookup"><span data-stu-id="48149-972">X</span></span> | <span data-ttu-id="48149-973">X</span><span class="sxs-lookup"><span data-stu-id="48149-973">X</span></span> | <span data-ttu-id="48149-974">X</span><span class="sxs-lookup"><span data-stu-id="48149-974">X</span></span> | <span data-ttu-id="48149-975">X</span><span class="sxs-lookup"><span data-stu-id="48149-975">X</span></span> | <span data-ttu-id="48149-976">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="48149-976">Windows 8.1</span></span> |
| <span data-ttu-id="48149-977">ANZAHL DER \_ \_ ARBEITSTHREADS \_ DER WINHTTP-OPTION \_</span><span class="sxs-lookup"><span data-stu-id="48149-977">WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT</span></span><br/><span data-ttu-id="48149-978">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-978">**DWORD**</span></span> | \- | \- | \- | <span data-ttu-id="48149-979">X</span><span class="sxs-lookup"><span data-stu-id="48149-979">X</span></span> | \- |
| <span data-ttu-id="48149-980">WINHTTP-OPTION \_ \_ \_ \_ SCHREIBPUFFERGRÖßE</span><span class="sxs-lookup"><span data-stu-id="48149-980">WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="48149-981">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="48149-981">**DWORD**</span></span> | \- | <span data-ttu-id="48149-982">X</span><span class="sxs-lookup"><span data-stu-id="48149-982">X</span></span> | <span data-ttu-id="48149-983">X</span><span class="sxs-lookup"><span data-stu-id="48149-983">X</span></span> | <span data-ttu-id="48149-984">X</span><span class="sxs-lookup"><span data-stu-id="48149-984">X</span></span> | \- |

> [!Note]
> <span data-ttu-id="48149-985">Informationen zu Windows XP und Windows 2000 finden Sie unter [Laufzeitanforderungen.](winhttp-start-page.md)</span><span class="sxs-lookup"><span data-stu-id="48149-985">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48149-986">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="48149-986">Requirements</span></span>

| <span data-ttu-id="48149-987">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48149-987">Requirement</span></span> | <span data-ttu-id="48149-988">Wert</span><span class="sxs-lookup"><span data-stu-id="48149-988">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="48149-989">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48149-989">Minimum supported client</span></span> | <span data-ttu-id="48149-990">Nur Windows XP, Windows 2000 Professional mit \[ SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48149-990">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>            |
| <span data-ttu-id="48149-991">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48149-991">Minimum supported server</span></span> | <span data-ttu-id="48149-992">Nur Windows Server 2003, Windows 2000 Server mit \[ SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48149-992">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>         |
| <span data-ttu-id="48149-993">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="48149-993">Redistributable</span></span>          | <span data-ttu-id="48149-994">WinHTTP 5.0 und Internet Explorer 5.01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="48149-994">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span> |
| <span data-ttu-id="48149-995">Header</span><span class="sxs-lookup"><span data-stu-id="48149-995">Header</span></span>                   | <span data-ttu-id="48149-996">Winhttp.h</span><span class="sxs-lookup"><span data-stu-id="48149-996">Winhttp.h</span></span>                                                                       |

## <a name="see-also"></a><span data-ttu-id="48149-997">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48149-997">See also</span></span>

[<span data-ttu-id="48149-998">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="48149-998">WinHTTP Versions</span></span>](winhttp-versions.md)
