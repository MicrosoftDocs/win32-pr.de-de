---
title: Behandeln der Authentifizierung
description: Einige Proxys und Server erfordern eine Authentifizierung, bevor sie Zugriff auf Ressourcen im Internet gewähren.
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82d8cd93f1010c71560d856793ad06d8bc5d9d5
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380854"
---
# <a name="handling-authentication"></a><span data-ttu-id="e38f5-103">Behandeln der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="e38f5-103">Handling Authentication</span></span>

<span data-ttu-id="e38f5-104">Einige Proxys und Server erfordern eine Authentifizierung, bevor sie Zugriff auf Ressourcen im Internet gewähren.</span><span class="sxs-lookup"><span data-stu-id="e38f5-104">Some proxies and servers require authentication before granting access to resources on the Internet.</span></span> <span data-ttu-id="e38f5-105">Die WinINet-Funktionen unterstützen die Server- und Proxyauthentifizierung für HTTP-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="e38f5-105">The WinINet functions support server and proxy authentication for http sessions.</span></span> <span data-ttu-id="e38f5-106">Die Authentifizierung von FTP-Servern muss von der [**InternetConnect-Funktion verarbeitet**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) werden.</span><span class="sxs-lookup"><span data-stu-id="e38f5-106">Authentication of ftp servers must be handled by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function.</span></span> <span data-ttu-id="e38f5-107">Derzeit wird die FTP-Gatewayauthentifizierung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e38f5-107">Currently, FTP gateway authentication is not supported.</span></span>

## <a name="about-http-authentication"></a><span data-ttu-id="e38f5-108">Informationen zur HTTP-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="e38f5-108">About HTTP Authentication</span></span>

<span data-ttu-id="e38f5-109">Wenn eine Authentifizierung erforderlich ist, erhält die Clientanwendung den Statuscode 401, wenn der Server eine Authentifizierung erfordert, oder 407, wenn der Proxy eine Authentifizierung erfordert.</span><span class="sxs-lookup"><span data-stu-id="e38f5-109">If authentication is required, the client application receives a status code 401, if the server requires authentication, or 407, if the proxy requires authentication.</span></span> <span data-ttu-id="e38f5-110">Mit dem Statuscode sendet der Proxy oder Server einen oder mehrere Authentifizierungsantwortheader – Proxyauthentifizierung (für Proxyauthentifizierung) oder WWW-Authenticate (für Serverauthentifizierung).</span><span class="sxs-lookup"><span data-stu-id="e38f5-110">With the status code, the proxy or server sends one, or more, authenticate response headers—Proxy-Authenticate (for proxy authentication) or WWW-Authenticate (for server authentication).</span></span>

<span data-ttu-id="e38f5-111">Jeder Authentifizierungsantwortheader enthält ein verfügbares Authentifizierungsschema und einen Bereich.</span><span class="sxs-lookup"><span data-stu-id="e38f5-111">Each authenticate response header contains an available authentication scheme and a realm.</span></span> <span data-ttu-id="e38f5-112">Wenn mehrere Authentifizierungsschemas unterstützt werden, gibt der Server mehrere Authentifizierungsantwortheader zurück.</span><span class="sxs-lookup"><span data-stu-id="e38f5-112">If multiple authentication schemes are supported, the server returns multiple authenticate response headers.</span></span> <span data-ttu-id="e38f5-113">Beim Bereichswert wird die Kleinschreibung beachtet, und es wird ein Schutzbereich auf dem Proxy oder Server definiert.</span><span class="sxs-lookup"><span data-stu-id="e38f5-113">The realm value is case-sensitive and defines a protection space on the proxy or server.</span></span> <span data-ttu-id="e38f5-114">Der Header "WWW-Authenticate: Basic Realm="example"" wäre beispielsweise ein Beispiel für einen Header, der zurückgegeben wird, wenn eine Serverauthentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e38f5-114">For example, the header "WWW-Authenticate: Basic Realm="example"" would be an example of a header returned when server authentication is required.</span></span>

<span data-ttu-id="e38f5-115">Die Clientanwendung, die die Anforderung gesendet hat, kann sich selbst authentifizieren, indem sie ein Autorisierungsheaderfeld in die Anforderung einschleiert.</span><span class="sxs-lookup"><span data-stu-id="e38f5-115">The client application that sent the request can authenticate itself by including an Authorization header field with the request.</span></span> <span data-ttu-id="e38f5-116">Der Autorisierungsheader enthält das Authentifizierungsschema und die entsprechende Antwort, die für dieses Schema erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e38f5-116">The Authorization header would contain the authentication scheme and the appropriate response required by that scheme.</span></span> <span data-ttu-id="e38f5-117">Beispielsweise würde der Header "Authorization: Basic" der Anforderung hinzugefügt und erneut an den Server gesendet, wenn der Client den Authentifizierungsantwortheader \<username:password> "WWW-Authenticate: Basic Realm="example" erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="e38f5-117">For example, the header "Authorization: Basic \<username:password>" would be added to the request and re-sent to the server if the client received the authenticate response header "WWW-Authenticate: Basic Realm="example"".</span></span>

<span data-ttu-id="e38f5-118">Es gibt zwei allgemeine Arten von Authentifizierungsschemas:</span><span class="sxs-lookup"><span data-stu-id="e38f5-118">There are two general types of authentication schemes:</span></span>

-   <span data-ttu-id="e38f5-119">Standardauthentifizierungsschema, bei dem Benutzername und Kennwort in Klartext an den Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e38f5-119">Basic authentication scheme, where the user name and password are sent in cleartext to the server.</span></span>
-   <span data-ttu-id="e38f5-120">Challenge-Response-Schemas, die ein Challenge-Response-Format ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e38f5-120">Challenge-response schemes, which allow for a challenge-response format.</span></span>

<span data-ttu-id="e38f5-121">Das Standardauthentifizierungsschema basiert auf dem Modell, das ein Client sich mit einem Benutzernamen und kennwort für jeden Bereich authentifizieren muss.</span><span class="sxs-lookup"><span data-stu-id="e38f5-121">The Basic authentication scheme is based on the model that a client must authenticate itself with a user name and password for each realm.</span></span> <span data-ttu-id="e38f5-122">Der Server wartet die Anforderung, wenn er erneut mit einem Autorisierungsheader gesendet wird, der einen gültigen Benutzernamen und ein gültiges Kennwort enthält.</span><span class="sxs-lookup"><span data-stu-id="e38f5-122">The server services the request if it is resent with an Authorization header that includes a valid user name and password.</span></span>

<span data-ttu-id="e38f5-123">Abfrage-Antwort-Schemas ermöglichen eine sicherere Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="e38f5-123">Challenge-response schemes enable more secure authentication.</span></span> <span data-ttu-id="e38f5-124">Wenn eine Anforderung eine Authentifizierung mithilfe eines Abfrage-/Antwortschemas erfordert, werden der entsprechende Statuscode und die Authenticate-Header an den Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e38f5-124">If a request requires authentication using a challenge-response scheme, the appropriate status code and Authenticate headers are returned to the client.</span></span> <span data-ttu-id="e38f5-125">Der Client muss dann die Anforderung mit einer Aushandlung erneut senden.</span><span class="sxs-lookup"><span data-stu-id="e38f5-125">The client must then to resend the request with a negotiate.</span></span> <span data-ttu-id="e38f5-126">Der Server gibt einen entsprechenden Statuscode mit einer Abfrage zurück, und der Client müsste die Anforderung dann mit der richtigen Antwort erneut senden, um den angeforderten Dienst abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e38f5-126">The server would return an appropriate status code with a challenge, and the client would then require to resend the request with the proper response to get the requested service.</span></span>

<span data-ttu-id="e38f5-127">In der folgenden Tabelle sind die Authentifizierungsschemas, der Authentifizierungstyp, die DLL, die sie unterstützt, und eine Beschreibung des Schemas aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e38f5-127">The following table lists authentication schemes, the authentication type, the DLL that supports them, and a description of the scheme.</span></span>



| <span data-ttu-id="e38f5-128">Schema</span><span class="sxs-lookup"><span data-stu-id="e38f5-128">Scheme</span></span>                                    | <span data-ttu-id="e38f5-129">type</span><span class="sxs-lookup"><span data-stu-id="e38f5-129">Type</span></span>               | <span data-ttu-id="e38f5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e38f5-130">DLL</span></span>                  | <span data-ttu-id="e38f5-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e38f5-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e38f5-132">Basic (Klartext)</span><span class="sxs-lookup"><span data-stu-id="e38f5-132">Basic (cleartext)</span></span>                         | <span data-ttu-id="e38f5-133">basic</span><span class="sxs-lookup"><span data-stu-id="e38f5-133">basic</span></span>              | <span data-ttu-id="e38f5-134">Wininet.dll</span><span class="sxs-lookup"><span data-stu-id="e38f5-134">Wininet.dll</span></span>          | <span data-ttu-id="e38f5-135">Verwendet eine Base64-codierte Zeichenfolge, die den Benutzernamen und das Kennwort enthält.</span><span class="sxs-lookup"><span data-stu-id="e38f5-135">Uses a base64 encoded string that contains the user name and password.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="e38f5-136">Digest</span><span class="sxs-lookup"><span data-stu-id="e38f5-136">Digest</span></span>                                    | <span data-ttu-id="e38f5-137">Challenge-Response</span><span class="sxs-lookup"><span data-stu-id="e38f5-137">challenge-response</span></span> | <span data-ttu-id="e38f5-138">Digest.dll</span><span class="sxs-lookup"><span data-stu-id="e38f5-138">Digest.dll</span></span>           | <span data-ttu-id="e38f5-139">Ein Abfrage-Antwort-Schema, das die Verwendung eines Nonce-Werts (einer vom Server angegebenen Datenzeichenfolge) in Frage stellt.</span><span class="sxs-lookup"><span data-stu-id="e38f5-139">A challenge-response scheme that challenges using a nonce (a server-specified data string) value.</span></span> <span data-ttu-id="e38f5-140">Eine gültige Antwort enthält eine Prüfsumme des Benutzernamens, des Kennworts, des angegebenen Nonce-Werts, der HTTP-Methode und des angeforderten Uniform Resource Identifier (URI).</span><span class="sxs-lookup"><span data-stu-id="e38f5-140">A valid response contains a checksum of the user name, the password, the given nonce value, the HTTP method, and the requested Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="e38f5-141">Unterstützung der Digestauthentifizierung wurde in Microsoft Internet Explorer 5 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e38f5-141">Digest authentication support was introduced in Microsoft Internet Explorer 5.</span></span> |
| <span data-ttu-id="e38f5-142">NT LAN-Manager (NTLM)</span><span class="sxs-lookup"><span data-stu-id="e38f5-142">NT LAN Manager (NTLM)</span></span>                     | <span data-ttu-id="e38f5-143">Challenge-Response</span><span class="sxs-lookup"><span data-stu-id="e38f5-143">challenge-response</span></span> | <span data-ttu-id="e38f5-144">Winsspi.dll</span><span class="sxs-lookup"><span data-stu-id="e38f5-144">Winsspi.dll</span></span>          | <span data-ttu-id="e38f5-145">Ein Abfrage-Antwort-Schema, das die Abfrage auf dem Benutzernamen basiert.</span><span class="sxs-lookup"><span data-stu-id="e38f5-145">A challenge-response scheme that bases the challenge on the user name.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="e38f5-146">Microsoft Network (MSN)</span><span class="sxs-lookup"><span data-stu-id="e38f5-146">Microsoft Network (MSN)</span></span>                   | <span data-ttu-id="e38f5-147">Challenge-Response</span><span class="sxs-lookup"><span data-stu-id="e38f5-147">challenge-response</span></span> | <span data-ttu-id="e38f5-148">Msnsspc.dll</span><span class="sxs-lookup"><span data-stu-id="e38f5-148">Msnsspc.dll</span></span>          | <span data-ttu-id="e38f5-149">The Microsoft Network des Authentifizierungsschemas.</span><span class="sxs-lookup"><span data-stu-id="e38f5-149">The Microsoft Network's authentication scheme.</span></span>                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="e38f5-150">Verteilte Kennwortauthentifizierung (Distributed Password Authentication, DPA)</span><span class="sxs-lookup"><span data-stu-id="e38f5-150">Distributed Password Authentication (DPA)</span></span> | <span data-ttu-id="e38f5-151">Challenge-Response</span><span class="sxs-lookup"><span data-stu-id="e38f5-151">challenge-response</span></span> | <span data-ttu-id="e38f5-152">Msapsspc.dll</span><span class="sxs-lookup"><span data-stu-id="e38f5-152">Msapsspc.dll</span></span>         | <span data-ttu-id="e38f5-153">Ähnelt der MSN-Authentifizierung und wird auch vom Microsoft Network verwendet.</span><span class="sxs-lookup"><span data-stu-id="e38f5-153">Similar to MSN authentication and is also used by the Microsoft Network.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="e38f5-154">Remotepassphrase-Authentifizierung (RPA)</span><span class="sxs-lookup"><span data-stu-id="e38f5-154">Remote Passphrase Authentication (RPA)</span></span>    | <span data-ttu-id="e38f5-155">Compuserve</span><span class="sxs-lookup"><span data-stu-id="e38f5-155">CompuServe</span></span>         | <span data-ttu-id="e38f5-156">Rpawinet.dll, da.dll</span><span class="sxs-lookup"><span data-stu-id="e38f5-156">Rpawinet.dll, da.dll</span></span> | <span data-ttu-id="e38f5-157">CompuServe-Authentifizierungsschema.</span><span class="sxs-lookup"><span data-stu-id="e38f5-157">CompuServe authentication scheme.</span></span> <span data-ttu-id="e38f5-158">Weitere Informationen finden Sie unter [RPA Mechanism Specifications (RPA-Mechanismusspezifikationen).](https://www.compuserve.com/)</span><span class="sxs-lookup"><span data-stu-id="e38f5-158">For more information, see the [RPA Mechanism Specifications](https://www.compuserve.com/).</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="e38f5-159">Für alle Anderen als die Standardauthentifizierung müssen die Registrierungsschlüssel zusätzlich zur Installation der entsprechenden DLL eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="e38f5-159">For anything other than Basic authentication, the registry keys must be set up in addition to installing the appropriate DLL.</span></span>

<span data-ttu-id="e38f5-160">Wenn eine Authentifizierung erforderlich ist, sollte [das FLAG INTERNET FLAG KEEP \_ \_ \_ CONNECTION](api-flags.md) im Aufruf von [**HttpOpenRequest verwendet werden.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)</span><span class="sxs-lookup"><span data-stu-id="e38f5-160">If authentication is required, the [INTERNET\_FLAG\_KEEP\_CONNECTION](api-flags.md) flag should be used in the call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="e38f5-161">Das FLAG INTERNET FLAG KEEP CONNECTION ist für NTLM und andere Authentifizierungstypen erforderlich, um die Verbindung während des Abschlusses des \_ \_ \_ Authentifizierungsprozesses zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="e38f5-161">The INTERNET\_FLAG\_KEEP\_CONNECTION flag is required for NTLM and other types of authentication in order to maintain the connection while completing the authentication process.</span></span> <span data-ttu-id="e38f5-162">Wenn die Verbindung nicht aufrechterhalten wird, muss der Authentifizierungsprozess mit dem Proxy oder Server neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="e38f5-162">If the connection is not maintained, the authentication process must be restarted with the proxy or server.</span></span>

<span data-ttu-id="e38f5-163">Die [**Funktionen InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) und [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) werden auch dann erfolgreich abgeschlossen, wenn eine Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e38f5-163">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) functions complete successfully even when authentication is required.</span></span> <span data-ttu-id="e38f5-164">Der Unterschied besteht in den in den Headerdateien zurückgegebenen Daten, und [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) erhält eine HTML-Seite, die den Benutzer über den Statuscode informiert.</span><span class="sxs-lookup"><span data-stu-id="e38f5-164">The difference is, the data returned in the header files and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) would receive an HTML page informing the user of the status code.</span></span>

### <a name="registering-authentication-keys"></a><span data-ttu-id="e38f5-165">Registrieren von Authentifizierungsschlüsseln</span><span class="sxs-lookup"><span data-stu-id="e38f5-165">Registering Authentication Keys</span></span>

<span data-ttu-id="e38f5-166">INTERNET \_ OPEN \_ TYPE \_ PRECONFIG untersucht die Registrierungswerte **ProxyEnable,** **ProxyServer** und **ProxyOverride.**</span><span class="sxs-lookup"><span data-stu-id="e38f5-166">INTERNET\_OPEN\_TYPE\_PRECONFIG looks at the registry values **ProxyEnable**, **ProxyServer**, and **ProxyOverride**.</span></span> <span data-ttu-id="e38f5-167">Diese Werte befinden sich unter **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** Internet \\ **Settings**.</span><span class="sxs-lookup"><span data-stu-id="e38f5-167">These values are located under **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Internet Settings**.</span></span>

<span data-ttu-id="e38f5-168">Bei anderen Authentifizierungsschemas als Basic muss der Registrierung unter **HKEY \_ LOCAL \_ MACHINE** SOFTWARE Microsoft Internet Explorer Security ein Schlüssel hinzugefügt \\  \\  \\  \\ werden.</span><span class="sxs-lookup"><span data-stu-id="e38f5-168">For authentication schemes other than Basic, a key must be added to the registry under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**.</span></span> <span data-ttu-id="e38f5-169">Der **DWORD-Wert** **Flags** sollte mit dem entsprechenden Wert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e38f5-169">A **DWORD** value, **Flags**, should be set with the appropriate value.</span></span> <span data-ttu-id="e38f5-170">Die folgende Liste zeigt die möglichen Werte für den **Flags-Wert.**</span><span class="sxs-lookup"><span data-stu-id="e38f5-170">The following list shows the possible values for the **Flags** value.</span></span>

-   <span data-ttu-id="e38f5-171">PLUGIN \_ AUTH \_ FLAGS \_ UNIQUE CONTEXT PER \_ \_ \_ TCPIP (value=0x01)</span><span class="sxs-lookup"><span data-stu-id="e38f5-171">PLUGIN\_AUTH\_FLAGS\_UNIQUE\_CONTEXT\_PER\_TCPIP (value=0x01)</span></span>

    <span data-ttu-id="e38f5-172">Jeder TCP/IP-Socket (Transmission Control Protocol/Internet Protocol) enthält einen anderen Kontext.</span><span class="sxs-lookup"><span data-stu-id="e38f5-172">Each Transmission Control Protocol/Internet Protocol (TCP/IP) socket contains a different context.</span></span> <span data-ttu-id="e38f5-173">Andernfalls wird ein neuer Kontext für jede Bereichs- oder Block-URL-Vorlage übergeben.</span><span class="sxs-lookup"><span data-stu-id="e38f5-173">Otherwise, a new context is passed for each realm or block URL template.</span></span>

-   <span data-ttu-id="e38f5-174">PLUGIN \_ AUTH \_ FLAGS \_ CAN HANDLE UI \_ \_ (value=0x02)</span><span class="sxs-lookup"><span data-stu-id="e38f5-174">PLUGIN\_AUTH\_FLAGS\_CAN\_HANDLE\_UI (value=0x02)</span></span>

    <span data-ttu-id="e38f5-175">Diese DLL kann ihre eigenen Benutzereingaben verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e38f5-175">This DLL can handle its own user input.</span></span>

-   <span data-ttu-id="e38f5-176">PLUGIN \_ AUTH \_ FLAGS \_ CAN HANDLE \_ \_ NO \_ PASSWD (value=0x04) (PLUG-IN-AUTHENTIFIZIERUNGSFLAGS KÖNNEN KEIN PASSWD verarbeiten (value=0x04)</span><span class="sxs-lookup"><span data-stu-id="e38f5-176">PLUGIN\_AUTH\_FLAGS\_CAN\_HANDLE\_NO\_PASSWD (value=0x04)</span></span>

    <span data-ttu-id="e38f5-177">Diese DLL kann eine Authentifizierung durchführen, ohne den Benutzer zur Eingabe eines Kennworts aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="e38f5-177">This DLL might be capable of doing an authentication without prompting the user for a password.</span></span>

-   <span data-ttu-id="e38f5-178">PLUGIN \_ AUTH \_ FLAGS \_ NO REALM \_ (value=0x08)</span><span class="sxs-lookup"><span data-stu-id="e38f5-178">PLUGIN\_AUTH\_FLAGS\_NO\_REALM (value=0x08)</span></span>

    <span data-ttu-id="e38f5-179">Diese DLL verwendet keine standardmäßige HTTP-Bereichszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e38f5-179">This DLL does not use a standard http realm string.</span></span> <span data-ttu-id="e38f5-180">Alle Daten, die ein Bereich zu sein scheinen, sind schemaspezifische Daten.</span><span class="sxs-lookup"><span data-stu-id="e38f5-180">Any data that appears to be a realm is scheme-specific data.</span></span>

-   <span data-ttu-id="e38f5-181">\_PLUG-IN-AUTHENTIFIZIERUNGSFLAGS \_ KEEP ALIVE NOT REQUIRED \_ \_ \_ \_ (value=0x10)</span><span class="sxs-lookup"><span data-stu-id="e38f5-181">PLUGIN\_AUTH\_FLAGS\_KEEP\_ALIVE\_NOT\_REQUIRED (value=0x10)</span></span>

    <span data-ttu-id="e38f5-182">Diese DLL erfordert keine permanente Verbindung für die Abfrageantwortsequenz.</span><span class="sxs-lookup"><span data-stu-id="e38f5-182">This DLL does not require a persistent connection for its challenge-response sequence.</span></span>

<span data-ttu-id="e38f5-183">Um z. B. die NTLM-Authentifizierung hinzuzufügen, muss der Schlüssel NTLM **HKEY \_ LOCAL \_ MACHINE** SOFTWARE Microsoft Internet Explorer Security hinzugefügt \\  \\  \\  \\ werden.</span><span class="sxs-lookup"><span data-stu-id="e38f5-183">For example, to add NTLM authentication, the key NTLM must be added to **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**.</span></span> <span data-ttu-id="e38f5-184">Unter **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Internet Explorer** \\ **Security** \\ **NTLM** müssen der Zeichenfolgenwert **DLLFile** und der **DWORD-Wert** **Flags** hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e38f5-184">Under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**\\**NTLM**, the string value, **DLLFile**, and a **DWORD** value, **Flags**, must be added.</span></span> <span data-ttu-id="e38f5-185">**DLLFile** muss auf Winsspi.dll und **Flags** auf 0x08.</span><span class="sxs-lookup"><span data-stu-id="e38f5-185">**DLLFile** must be set to Winsspi.dll, and **Flags** must be set to 0x08.</span></span>

### <a name="server-authentication"></a><span data-ttu-id="e38f5-186">Serverauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="e38f5-186">Server Authentication</span></span>

<span data-ttu-id="e38f5-187">Wenn ein Server eine Anforderung empfängt, die eine Authentifizierung erfordert, gibt der Server die Statuscodemeldung 401 zurück.</span><span class="sxs-lookup"><span data-stu-id="e38f5-187">When a server receives a request that requires authentication, the server returns a 401 status code message.</span></span> <span data-ttu-id="e38f5-188">In dieser Meldung sollte der Server mindestens einen WWW-Authenticate-Antwortheader enthalten.</span><span class="sxs-lookup"><span data-stu-id="e38f5-188">In that message, the server should include one or more WWW-Authenticate response headers.</span></span> <span data-ttu-id="e38f5-189">Diese Header enthalten die Authentifizierungsmethoden, die der Server zur Verfügung hat.</span><span class="sxs-lookup"><span data-stu-id="e38f5-189">These headers include the authentication methods the server has available.</span></span> <span data-ttu-id="e38f5-190">WinINet wählt die erste Methode aus, die erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="e38f5-190">WinINet chooses the first method it recognizes.</span></span>

<span data-ttu-id="e38f5-191">Die Standardauthentifizierung bietet schwache Sicherheit, es sei denn, der Kanal wird zuerst mit SSL oder PCT linkverschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="e38f5-191">Basic authentication provides weak security unless the channel is first link-encrypted with SSL or PCT.</span></span>

<span data-ttu-id="e38f5-192">Die [**InternetErrorDlg-Funktion**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) kann verwendet werden, um die Benutzernamen- und Kennwortdaten vom Benutzer zu erhalten, oder eine benutzerdefinierte Benutzeroberfläche kann zum Abrufen der Daten entworfen werden.</span><span class="sxs-lookup"><span data-stu-id="e38f5-192">The [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) function can be used to obtain the user name and password data from the user, or a customized user interface can be designed to obtain the data.</span></span>

<span data-ttu-id="e38f5-193">Eine benutzerdefinierte Schnittstelle kann die [**InternetSetOption-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) verwenden, um die Werte [INTERNET OPTION \_ \_ PASSWORD](option-flags.md) und [INTERNET OPTION \_ \_ USERNAME](option-flags.md) festlegen und dann die Anforderung erneut an den Server senden.</span><span class="sxs-lookup"><span data-stu-id="e38f5-193">A custom interface can use the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function to set the [INTERNET\_OPTION\_PASSWORD](option-flags.md) and [INTERNET\_OPTION\_USERNAME](option-flags.md) values and then resend the request to the server.</span></span>

### <a name="proxy-authentication"></a><span data-ttu-id="e38f5-194">Proxyauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="e38f5-194">Proxy Authentication</span></span>

<span data-ttu-id="e38f5-195">Wenn ein Client versucht, einen Proxy zu verwenden, der eine Authentifizierung erfordert, gibt der Proxy eine 407-Statuscodemeldung an den Client zurück.</span><span class="sxs-lookup"><span data-stu-id="e38f5-195">When a client attempts to use a proxy that requires authentication, the proxy returns a 407 status code message to the client.</span></span> <span data-ttu-id="e38f5-196">In dieser Nachricht sollte der Proxy mindestens einen Proxy-Authenticate-Antwortheader enthalten.</span><span class="sxs-lookup"><span data-stu-id="e38f5-196">In that message, the proxy should include one or more Proxy-Authenticate response headers.</span></span> <span data-ttu-id="e38f5-197">Diese Header enthalten die vom Proxy verfügbaren Authentifizierungsmethoden.</span><span class="sxs-lookup"><span data-stu-id="e38f5-197">These headers include the authentication methods available from the proxy.</span></span> <span data-ttu-id="e38f5-198">WinINet wählt die erste Methode aus, die erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="e38f5-198">WinINet chooses the first method it recognizes.</span></span>

<span data-ttu-id="e38f5-199">Die [**InternetErrorDlg-Funktion**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) kann verwendet werden, um die Benutzernamen- und Kennwortdaten vom Benutzer zu erhalten, oder eine benutzerdefinierte Benutzeroberfläche kann entworfen werden.</span><span class="sxs-lookup"><span data-stu-id="e38f5-199">The [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) function can be used to obtain the user name and password data from the user, or a customized user interface can be designed.</span></span>

<span data-ttu-id="e38f5-200">Eine benutzerdefinierte Schnittstelle kann die [**InternetSetOption-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) verwenden, um die Werte [INTERNET OPTION PROXY \_ \_ \_ PASSWORD](option-flags.md) und [INTERNET OPTION PROXY \_ \_ \_ USERNAME](option-flags.md) festlegen und dann die Anforderung erneut an den Proxy senden.</span><span class="sxs-lookup"><span data-stu-id="e38f5-200">A custom interface can use the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function to set the [INTERNET\_OPTION\_PROXY\_PASSWORD](option-flags.md) and [INTERNET\_OPTION\_PROXY\_USERNAME](option-flags.md) values and then resend the request to the proxy.</span></span>

<span data-ttu-id="e38f5-201">Wenn kein Proxybenutzername und kein Kennwort festgelegt sind, versucht WinINet, den Benutzernamen und das Kennwort für den Server zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e38f5-201">If no proxy user name and password are set, WinINet attempts to use the user name and password for the server.</span></span> <span data-ttu-id="e38f5-202">Durch dieses Verhalten können Clients dieselbe benutzerdefinierte Benutzeroberfläche implementieren, die auch für die Serverauthentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e38f5-202">This behavior enables clients to implement the same customized user interface used to handle server authentication.</span></span>

## <a name="handling-http-authentication"></a><span data-ttu-id="e38f5-203">Behandeln der HTTP-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="e38f5-203">Handling HTTP Authentication</span></span>

<span data-ttu-id="e38f5-204">Die HTTP-Authentifizierung kann entweder mit [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) oder einer benutzerdefinierten Funktion verarbeitet werden, die [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) verwendet oder eigene Authentifizierungsheader hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="e38f5-204">HTTP authentication can be handled with either [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) or a customized function that uses [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) or adds its own authentication headers.</span></span> <span data-ttu-id="e38f5-205">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) kann die einem [**HINTERNET-Handle**](appendix-a-hinternet-handles.md) zugeordneten Header untersuchen, um ausgeblendete Fehler zu finden, z. B. Statuscodes von einem Proxy oder Server.</span><span class="sxs-lookup"><span data-stu-id="e38f5-205">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) can examine the headers associated with an [**HINTERNET**](appendix-a-hinternet-handles.md) handle to find hidden errors, such as status codes from a proxy or server.</span></span> <span data-ttu-id="e38f5-206">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) kann verwendet werden, um den Benutzernamen und das Kennwort für den Proxy und den Server festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e38f5-206">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) can be used to set the user name and password for the proxy and server.</span></span> <span data-ttu-id="e38f5-207">Für die MSN- und DPA-Authentifizierung muss [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) verwendet werden, um den Benutzernamen und das Kennwort festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e38f5-207">For MSN and DPA authentication, [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) must be used to set the user name and password.</span></span>

<span data-ttu-id="e38f5-208">Für jede benutzerdefinierte Funktion, die eigene WWW-Authenticate- oder Proxy-Authenticate-Header hinzufügt, sollte das [INTERNET \_ FLAG NO \_ \_ AUTH-Flag](api-flags.md) so festgelegt werden, dass die Authentifizierung deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="e38f5-208">For any customized function that adds its own WWW-Authenticate or Proxy-Authenticate headers, the [INTERNET\_FLAG\_NO\_AUTH](api-flags.md) flag should be set to disable authentication.</span></span>

<span data-ttu-id="e38f5-209">Das folgende Beispiel zeigt, wie [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) zur Behandlung der HTTP-Authentifizierung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e38f5-209">The following example shows how [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) can be used to handle HTTP authentication.</span></span>


```C++
HINTERNET hOpenHandle,  hConnectHandle, hResourceHandle;
DWORD dwError, dwErrorCode;
HWND hwnd = GetConsoleWindow();

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG, 
                           NULL, NULL, 0);

hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"), 
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL, 
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL, 
                                  INTERNET_FLAG_KEEP_CONNECTION, 0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

// dwErrorCode stores the error code associated with the call to
// HttpSendRequest.  

dwErrorCode = hResourceHandle ? ERROR_SUCCESS : GetLastError();

dwError = InternetErrorDlg(hwnd, hResourceHandle, dwErrorCode, 
                           FLAGS_ERROR_UI_FILTER_FOR_ERRORS | 
                           FLAGS_ERROR_UI_FLAGS_CHANGE_OPTIONS |
                           FLAGS_ERROR_UI_FLAGS_GENERATE_DATA,
                           NULL);

if (dwError == ERROR_INTERNET_FORCE_RETRY)
    goto resend;

// Insert code to read the data from the hResourceHandle
// at this point.

```



<span data-ttu-id="e38f5-210">Im Beispiel wird dwErrorCode verwendet, um alle Fehler zu speichern, die dem Aufruf von [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e38f5-210">In the example, dwErrorCode is used to store any errors associated with the call to [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="e38f5-211">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) wird erfolgreich abgeschlossen, auch wenn der Proxy oder Server eine Authentifizierung erfordert.</span><span class="sxs-lookup"><span data-stu-id="e38f5-211">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) completes successfully, even if the proxy or server requires authentication.</span></span> <span data-ttu-id="e38f5-212">Wenn das \_ FLAGS ERROR \_ UI FILTER FOR ERRORS \_ \_ \_ -Flag an [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)übergeben wird, überprüft die Funktion die Header auf ausgeblendete Fehler.</span><span class="sxs-lookup"><span data-stu-id="e38f5-212">When the FLAGS\_ERROR\_UI\_FILTER\_FOR\_ERRORS flag is passed to [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), the function checks the headers for any hidden errors.</span></span> <span data-ttu-id="e38f5-213">Zu diesen ausgeblendeten Fehlern gehören alle Anforderungen für die Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="e38f5-213">These hidden errors would include any requests for authentication.</span></span> <span data-ttu-id="e38f5-214">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) zeigt das entsprechende Dialogfeld an, um den Benutzer zur Eingabe der erforderlichen Daten aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="e38f5-214">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) displays the appropriate dialog box to prompt the user for the necessary data.</span></span> <span data-ttu-id="e38f5-215">Die Flags FLAGS \_ ERROR \_ UI \_ FLAGS GENERATE DATA und \_ \_ FLAGS ERROR UI \_ \_ \_ FLAGS CHANGE OPTIONS sollten ebenfalls an \_ \_ [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)übergeben werden, damit die Funktion die entsprechende Datenstruktur für den Fehler erstellt und die Ergebnisse des Dialogfelds im [**HINTERNET-Handle**](appendix-a-hinternet-handles.md) speichert.</span><span class="sxs-lookup"><span data-stu-id="e38f5-215">The FLAGS\_ERROR\_UI\_FLAGS\_GENERATE\_DATA and FLAGS\_ERROR\_UI\_FLAGS\_CHANGE\_OPTIONS flags should also be passed to [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), so that the function constructs the appropriate data structure for the error and stores the results of the dialog box in the [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>

<span data-ttu-id="e38f5-216">Der folgende Beispielcode zeigt, wie die Authentifizierung mit [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)behandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e38f5-216">The following example code shows how authentication could be handled using [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


```C++
HINTERNET hOpenHandle,  hResourceHandle, hConnectHandle;
DWORD dwStatus;
DWORD dwStatusSize = sizeof(dwStatus);
char strUsername[64], strPassword[64];

// Normally, hOpenHandle, hResourceHandle,
// and hConnectHandle need to be properly assigned.

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG,
                           NULL, NULL, 0);
hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"),
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL,
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL,
                                  INTERNET_FLAG_KEEP_CONNECTION,
                                  0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

HttpQueryInfo(hResourceHandle, HTTP_QUERY_FLAG_NUMBER |
              HTTP_QUERY_STATUS_CODE, &dwStatus, &dwStatusSize, NULL);

switch (dwStatus)
{
    // cchUserLength is the length of strUsername and
    // cchPasswordLength is the length of strPassword.
    DWORD cchUserLength, cchPasswordLength;

    case HTTP_STATUS_PROXY_AUTH_REQ: // Proxy Authentication Required
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert appropriate error handling code.
        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_USERNAME,
                          strUsername,
                          cchUserLength+1);

        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_PASSWORD,
                          strPassword,
                          cchPasswordLength+1);
        goto resend;
        break;

    case HTTP_STATUS_DENIED:     // Server Authentication Required.
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert error handling code as
        // appropriate.
        InternetSetOption(hResourceHandle, INTERNET_OPTION_USERNAME,
                          strUsername, cchUserLength+1);
        InternetSetOption(hResourceHandle, INTERNET_OPTION_PASSWORD,
                          strPassword, cchPasswordLength+1);
        goto resend;
        break;
}

// Insert code to read the data from the hResourceHandle
// at this point.

```



> [!Note]  
> <span data-ttu-id="e38f5-217">WinINet unterstützt keine Serverimplementierungen.</span><span class="sxs-lookup"><span data-stu-id="e38f5-217">WinINet does not support server implementations.</span></span> <span data-ttu-id="e38f5-218">Darüber hinaus sollte es nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e38f5-218">In addition, it should not be used from a service.</span></span> <span data-ttu-id="e38f5-219">Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP Services (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)</span><span class="sxs-lookup"><span data-stu-id="e38f5-219">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 