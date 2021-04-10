---
title: Behandeln der Authentifizierung
description: Einige Proxys und Server erfordern eine Authentifizierung, bevor Sie Zugriff auf Ressourcen im Internet gewähren.
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8eaa38f61f0d97f1f543e0623313aa196aab7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104039772"
---
# <a name="handling-authentication"></a><span data-ttu-id="cc135-103">Behandeln der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="cc135-103">Handling Authentication</span></span>

<span data-ttu-id="cc135-104">Einige Proxys und Server erfordern eine Authentifizierung, bevor Sie Zugriff auf Ressourcen im Internet gewähren.</span><span class="sxs-lookup"><span data-stu-id="cc135-104">Some proxies and servers require authentication before granting access to resources on the Internet.</span></span> <span data-ttu-id="cc135-105">Die WinInet-Funktionen unterstützen die Server-und Proxy Authentifizierung für HTTP-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="cc135-105">The WinINet functions support server and proxy authentication for http sessions.</span></span> <span data-ttu-id="cc135-106">Die Authentifizierung von FTP-Servern muss von der [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -Funktion verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="cc135-106">Authentication of ftp servers must be handled by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function.</span></span> <span data-ttu-id="cc135-107">Die FTP-Gatewayauthentifizierung wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cc135-107">Currently, FTP gateway authentication is not supported.</span></span>

## <a name="about-http-authentication"></a><span data-ttu-id="cc135-108">Informationen zur HTTP-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="cc135-108">About HTTP Authentication</span></span>

<span data-ttu-id="cc135-109">Wenn eine Authentifizierung erforderlich ist, empfängt die Client Anwendung den Statuscode 401, wenn der Server eine Authentifizierung erfordert, oder 407, wenn für den Proxy eine Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cc135-109">If authentication is required, the client application receives a status code 401, if the server requires authentication, or 407, if the proxy requires authentication.</span></span> <span data-ttu-id="cc135-110">Mit dem Statuscode sendet der Proxy oder Server mindestens einen authentifikatsantwortheader – Proxy-authentifizieren (für die Proxy Authentifizierung) oder WWW-Authenticate (für die Server Authentifizierung).</span><span class="sxs-lookup"><span data-stu-id="cc135-110">With the status code, the proxy or server sends one, or more, authenticate response headers—Proxy-Authenticate (for proxy authentication) or WWW-Authenticate (for server authentication).</span></span>

<span data-ttu-id="cc135-111">Jeder authentifizieren-Antwortheader enthält ein verfügbares Authentifizierungsschema und einen Bereich.</span><span class="sxs-lookup"><span data-stu-id="cc135-111">Each authenticate response header contains an available authentication scheme and a realm.</span></span> <span data-ttu-id="cc135-112">Wenn mehrere Authentifizierungs Schemas unterstützt werden, gibt der Server mehrere authentifizieren-Antwortheader zurück.</span><span class="sxs-lookup"><span data-stu-id="cc135-112">If multiple authentication schemes are supported, the server returns multiple authenticate response headers.</span></span> <span data-ttu-id="cc135-113">Beim Bereichs Wert wird die Groß-/Kleinschreibung beachtet, und es wird ein Schutzbereich auf dem Proxy oder Server definiert.</span><span class="sxs-lookup"><span data-stu-id="cc135-113">The realm value is case-sensitive and defines a protection space on the proxy or server.</span></span> <span data-ttu-id="cc135-114">Beispielsweise wäre der Header "www-Authenticate: Basic Realm =" example "" ein Beispiel für einen Header, der zurückgegeben wird, wenn eine Server Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cc135-114">For example, the header "WWW-Authenticate: Basic Realm="example"" would be an example of a header returned when server authentication is required.</span></span>

<span data-ttu-id="cc135-115">Die Client Anwendung, die die Anforderung gesendet hat, kann sich selbst authentifizieren, indem Sie ein Autorisierungs Header Feld mit der Anforderung einschließt.</span><span class="sxs-lookup"><span data-stu-id="cc135-115">The client application that sent the request can authenticate itself by including an Authorization header field with the request.</span></span> <span data-ttu-id="cc135-116">Der Autorisierungs Header würde das Authentifizierungsschema und die entsprechende Antwort enthalten, die für dieses Schema erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cc135-116">The Authorization header would contain the authentication scheme and the appropriate response required by that scheme.</span></span> <span data-ttu-id="cc135-117">Beispielsweise würde die Kopfzeile "Authorization: Basic <username: Password>" der Anforderung hinzugefügt und erneut an den Server gesendet, wenn der Client den authentifizieren-Antwortheader "www-authentifizieren: Basic Realm =" example "" empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="cc135-117">For example, the header "Authorization: Basic <username:password>" would be added to the request and re-sent to the server if the client received the authenticate response header "WWW-Authenticate: Basic Realm="example"".</span></span>

<span data-ttu-id="cc135-118">Es gibt zwei allgemeine Arten von Authentifizierungs Schemas:</span><span class="sxs-lookup"><span data-stu-id="cc135-118">There are two general types of authentication schemes:</span></span>

-   <span data-ttu-id="cc135-119">Standard Authentifizierungsschema, bei dem der Benutzername und das Kennwort in Klartext an den Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc135-119">Basic authentication scheme, where the user name and password are sent in cleartext to the server.</span></span>
-   <span data-ttu-id="cc135-120">Challenge-Response-Schemas, die ein Challenge-Response-Format ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="cc135-120">Challenge-response schemes, which allow for a challenge-response format.</span></span>

<span data-ttu-id="cc135-121">Das grundlegende Authentifizierungsschema basiert auf dem Modell, das ein Client selbst mit einem Benutzernamen und einem Kennwort für jeden Bereich authentifizieren muss.</span><span class="sxs-lookup"><span data-stu-id="cc135-121">The Basic authentication scheme is based on the model that a client must authenticate itself with a user name and password for each realm.</span></span> <span data-ttu-id="cc135-122">Der Server dient zum Verarbeiten der Anforderung, wenn Sie mit einem Autorisierungs Header mit einem gültigen Benutzernamen und Kennwort erneut gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc135-122">The server services the request if it is resent with an Authorization header that includes a valid user name and password.</span></span>

<span data-ttu-id="cc135-123">Mit Challenge-Response-Schemas wird eine sicherere Authentifizierung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="cc135-123">Challenge-response schemes enable more secure authentication.</span></span> <span data-ttu-id="cc135-124">Wenn eine Anforderung eine Authentifizierung mit einem Challenge-Response-Schema erfordert, werden der entsprechende Statuscode und die Authenticate-Header an den Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cc135-124">If a request requires authentication using a challenge-response scheme, the appropriate status code and Authenticate headers are returned to the client.</span></span> <span data-ttu-id="cc135-125">Der Client muss dann die Anforderung mit einem Aushandlungs Vorgang erneut senden.</span><span class="sxs-lookup"><span data-stu-id="cc135-125">The client must then to resend the request with a negotiate.</span></span> <span data-ttu-id="cc135-126">Der Server gibt einen entsprechenden Statuscode mit einer Herausforderung zurück, und der Client müsste dann die Anforderung mit der richtigen Antwort erneut senden, um den angeforderten Dienst zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cc135-126">The server would return an appropriate status code with a challenge, and the client would then require to resend the request with the proper response to get the requested service.</span></span>

<span data-ttu-id="cc135-127">In der folgenden Tabelle sind die Authentifizierungs Schemas, der Authentifizierungstyp, die dll, die Sie unterstützt, und eine Beschreibung des Schemas aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="cc135-127">The following table lists authentication schemes, the authentication type, the DLL that supports them, and a description of the scheme.</span></span>



| <span data-ttu-id="cc135-128">Schema</span><span class="sxs-lookup"><span data-stu-id="cc135-128">Scheme</span></span>                                    | <span data-ttu-id="cc135-129">type</span><span class="sxs-lookup"><span data-stu-id="cc135-129">Type</span></span>               | <span data-ttu-id="cc135-130">DLL</span><span class="sxs-lookup"><span data-stu-id="cc135-130">DLL</span></span>                  | <span data-ttu-id="cc135-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc135-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc135-132">Basic (cleartext)</span><span class="sxs-lookup"><span data-stu-id="cc135-132">Basic (cleartext)</span></span>                         | <span data-ttu-id="cc135-133">basic</span><span class="sxs-lookup"><span data-stu-id="cc135-133">basic</span></span>              | <span data-ttu-id="cc135-134">Wininet.dll</span><span class="sxs-lookup"><span data-stu-id="cc135-134">Wininet.dll</span></span>          | <span data-ttu-id="cc135-135">Verwendet eine Base64-codierte Zeichenfolge, die den Benutzernamen und das Kennwort enthält.</span><span class="sxs-lookup"><span data-stu-id="cc135-135">Uses a base64 encoded string that contains the user name and password.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="cc135-136">Digest</span><span class="sxs-lookup"><span data-stu-id="cc135-136">Digest</span></span>                                    | <span data-ttu-id="cc135-137">Challenge-Response</span><span class="sxs-lookup"><span data-stu-id="cc135-137">challenge-response</span></span> | <span data-ttu-id="cc135-138">Digest.dll</span><span class="sxs-lookup"><span data-stu-id="cc135-138">Digest.dll</span></span>           | <span data-ttu-id="cc135-139">Ein Challenge-Response-Schema, das die Verwendung eines Nonce-Werts (eine vom Server angegebene Daten Zeichenfolge) herausstellt.</span><span class="sxs-lookup"><span data-stu-id="cc135-139">A challenge-response scheme that challenges using a nonce (a server-specified data string) value.</span></span> <span data-ttu-id="cc135-140">Eine gültige Antwort enthält eine Prüfsumme aus dem Benutzernamen, dem Kennwort, dem angegebenen Nonce-Wert, der HTTP-Methode und dem angeforderten Uniform Resource Identifier (URI).</span><span class="sxs-lookup"><span data-stu-id="cc135-140">A valid response contains a checksum of the user name, the password, the given nonce value, the HTTP method, and the requested Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="cc135-141">Die Unterstützung für die Digest-Authentifizierung wurde in Microsoft Internet Explorer 5 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="cc135-141">Digest authentication support was introduced in Microsoft Internet Explorer 5.</span></span> |
| <span data-ttu-id="cc135-142">NT-LAN-Manager (NTLM)</span><span class="sxs-lookup"><span data-stu-id="cc135-142">NT LAN Manager (NTLM)</span></span>                     | <span data-ttu-id="cc135-143">Challenge-Response</span><span class="sxs-lookup"><span data-stu-id="cc135-143">challenge-response</span></span> | <span data-ttu-id="cc135-144">Winsspi.dll</span><span class="sxs-lookup"><span data-stu-id="cc135-144">Winsspi.dll</span></span>          | <span data-ttu-id="cc135-145">Ein Challenge-Response-Schema, das die Herausforderung auf den Benutzernamen stützt.</span><span class="sxs-lookup"><span data-stu-id="cc135-145">A challenge-response scheme that bases the challenge on the user name.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="cc135-146">Microsoft-Netzwerk (MSN)</span><span class="sxs-lookup"><span data-stu-id="cc135-146">Microsoft Network (MSN)</span></span>                   | <span data-ttu-id="cc135-147">Challenge-Response</span><span class="sxs-lookup"><span data-stu-id="cc135-147">challenge-response</span></span> | <span data-ttu-id="cc135-148">Msnsspc.dll</span><span class="sxs-lookup"><span data-stu-id="cc135-148">Msnsspc.dll</span></span>          | <span data-ttu-id="cc135-149">Das Authentifizierungsschema the Microsoft Network.</span><span class="sxs-lookup"><span data-stu-id="cc135-149">The Microsoft Network's authentication scheme.</span></span>                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="cc135-150">Authentifizierung verteilter Kenn Wörter (dpa)</span><span class="sxs-lookup"><span data-stu-id="cc135-150">Distributed Password Authentication (DPA)</span></span> | <span data-ttu-id="cc135-151">Challenge-Response</span><span class="sxs-lookup"><span data-stu-id="cc135-151">challenge-response</span></span> | <span data-ttu-id="cc135-152">Msapsspc.dll</span><span class="sxs-lookup"><span data-stu-id="cc135-152">Msapsspc.dll</span></span>         | <span data-ttu-id="cc135-153">Ähnelt der MSN-Authentifizierung und wird auch vom Microsoft-Netzwerk verwendet.</span><span class="sxs-lookup"><span data-stu-id="cc135-153">Similar to MSN authentication and is also used by the Microsoft Network.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="cc135-154">Remote Passphrase-Authentifizierung (RPA)</span><span class="sxs-lookup"><span data-stu-id="cc135-154">Remote Passphrase Authentication (RPA)</span></span>    | <span data-ttu-id="cc135-155">CompuServe</span><span class="sxs-lookup"><span data-stu-id="cc135-155">CompuServe</span></span>         | <span data-ttu-id="cc135-156">Rpawinet.dll da.dll</span><span class="sxs-lookup"><span data-stu-id="cc135-156">Rpawinet.dll, da.dll</span></span> | <span data-ttu-id="cc135-157">Compuservice-Authentifizierungsschema.</span><span class="sxs-lookup"><span data-stu-id="cc135-157">CompuServe authentication scheme.</span></span> <span data-ttu-id="cc135-158">Weitere Informationen finden Sie in den [Spezifikationen für den RPA-Mechanismus](https://www.compuserve.com/).</span><span class="sxs-lookup"><span data-stu-id="cc135-158">For more information, see the [RPA Mechanism Specifications](https://www.compuserve.com/).</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="cc135-159">Für andere als die Standard Authentifizierung müssen die Registrierungsschlüssel zusätzlich zur Installation der entsprechenden DLL eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="cc135-159">For anything other than Basic authentication, the registry keys must be set up in addition to installing the appropriate DLL.</span></span>

<span data-ttu-id="cc135-160">Wenn eine Authentifizierung erforderlich ist, sollte das [Internet \_ Flag \_ Keep \_ Connection](api-flags.md) -Flag im [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)-Befehl verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc135-160">If authentication is required, the [INTERNET\_FLAG\_KEEP\_CONNECTION](api-flags.md) flag should be used in the call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="cc135-161">Das \_ \_ \_ kennflag für die Verbindungsart "Internet" ist für NTLM und andere Arten der Authentifizierung erforderlich, um die Verbindung während des Authentifizierungs Vorgangs aufrechtzuerhalten.</span><span class="sxs-lookup"><span data-stu-id="cc135-161">The INTERNET\_FLAG\_KEEP\_CONNECTION flag is required for NTLM and other types of authentication in order to maintain the connection while completing the authentication process.</span></span> <span data-ttu-id="cc135-162">Wenn die Verbindung nicht beibehalten wird, muss der Authentifizierungs Vorgang mit dem Proxy oder dem Server neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="cc135-162">If the connection is not maintained, the authentication process must be restarted with the proxy or server.</span></span>

<span data-ttu-id="cc135-163">Die Funktionen [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) und [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) werden erfolgreich abgeschlossen, auch wenn eine Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cc135-163">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) functions complete successfully even when authentication is required.</span></span> <span data-ttu-id="cc135-164">Der Unterschied besteht darin, dass die in den Header Dateien und in der [**Datei "internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) " zurückgegebenen Daten eine HTML-Seite erhalten, in der der Benutzer über den Statuscode</span><span class="sxs-lookup"><span data-stu-id="cc135-164">The difference is, the data returned in the header files and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) would receive an HTML page informing the user of the status code.</span></span>

### <a name="registering-authentication-keys"></a><span data-ttu-id="cc135-165">Registrieren von authentifizierungsschlüsseln</span><span class="sxs-lookup"><span data-stu-id="cc135-165">Registering Authentication Keys</span></span>

<span data-ttu-id="cc135-166">Internet \_ Open \_ Type \_ preconfig prüft die Registrierungs Werte **ProxyEnable**, **Proxyserver** und **ProxyOverride**.</span><span class="sxs-lookup"><span data-stu-id="cc135-166">INTERNET\_OPEN\_TYPE\_PRECONFIG looks at the registry values **ProxyEnable**, **ProxyServer**, and **ProxyOverride**.</span></span> <span data-ttu-id="cc135-167">Diese Werte befinden sich unter **HKEY \_ Current \_ User** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Settings**.</span><span class="sxs-lookup"><span data-stu-id="cc135-167">These values are located under **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Internet Settings**.</span></span>

<span data-ttu-id="cc135-168">Für andere Authentifizierungs Schemas als Basic muss der Registrierung unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security** ein Schlüssel hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="cc135-168">For authentication schemes other than Basic, a key must be added to the registry under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**.</span></span> <span data-ttu-id="cc135-169">Ein **DWORD** -Wert, **Flags**, sollte mit dem entsprechenden Wert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc135-169">A **DWORD** value, **Flags**, should be set with the appropriate value.</span></span> <span data-ttu-id="cc135-170">In der folgenden Liste werden die möglichen Werte für den **Flags** -Wert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cc135-170">The following list shows the possible values for the **Flags** value.</span></span>

-   <span data-ttu-id="cc135-171">Eindeutiger \_ \_ \_ \_ Kontext \_ pro \_ tcpip (Wert = 0x01) für Plug-in-Authentifizierungsflags</span><span class="sxs-lookup"><span data-stu-id="cc135-171">PLUGIN\_AUTH\_FLAGS\_UNIQUE\_CONTEXT\_PER\_TCPIP (value=0x01)</span></span>

    <span data-ttu-id="cc135-172">Jeder TCP/IP-Socket (Transmission Control Protocol/Internet Protocol) enthält einen anderen Kontext.</span><span class="sxs-lookup"><span data-stu-id="cc135-172">Each Transmission Control Protocol/Internet Protocol (TCP/IP) socket contains a different context.</span></span> <span data-ttu-id="cc135-173">Andernfalls wird für jede Bereichs-oder Block-URL-Vorlage ein neuer Kontext übermittelt.</span><span class="sxs-lookup"><span data-stu-id="cc135-173">Otherwise, a new context is passed for each realm or block URL template.</span></span>

-   <span data-ttu-id="cc135-174">Plug-in- \_ Authentifizierungsflags \_ können die \_ \_ \_ Benutzeroberfläche verarbeiten (Wert = 0x02)</span><span class="sxs-lookup"><span data-stu-id="cc135-174">PLUGIN\_AUTH\_FLAGS\_CAN\_HANDLE\_UI (value=0x02)</span></span>

    <span data-ttu-id="cc135-175">Diese DLL kann Ihre eigene Benutzereingaben verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="cc135-175">This DLL can handle its own user input.</span></span>

-   <span data-ttu-id="cc135-176">Plug-in- \_ auth- \_ Flags \_ können \_ \_ keine \_ passwd verarbeiten (Wert = 0x04)</span><span class="sxs-lookup"><span data-stu-id="cc135-176">PLUGIN\_AUTH\_FLAGS\_CAN\_HANDLE\_NO\_PASSWD (value=0x04)</span></span>

    <span data-ttu-id="cc135-177">Diese DLL kann eine Authentifizierung durchgeführt werden, ohne dass der Benutzer zur Eingabe eines Kennworts aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="cc135-177">This DLL might be capable of doing an authentication without prompting the user for a password.</span></span>

-   <span data-ttu-id="cc135-178">Plug-in für die Plug-in-Authentifizierung \_ \_ \_ ohne \_ Bereich (Wert = 0x08)</span><span class="sxs-lookup"><span data-stu-id="cc135-178">PLUGIN\_AUTH\_FLAGS\_NO\_REALM (value=0x08)</span></span>

    <span data-ttu-id="cc135-179">Diese DLL verwendet keine Standard-HTTP-Bereichs Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cc135-179">This DLL does not use a standard http realm string.</span></span> <span data-ttu-id="cc135-180">Alle Daten, die als Bereich angezeigt werden, sind Schema spezifische Daten.</span><span class="sxs-lookup"><span data-stu-id="cc135-180">Any data that appears to be a realm is scheme-specific data.</span></span>

-   <span data-ttu-id="cc135-181">Plug-in- \_ auth- \_ Flags \_ bleiben \_ \_ nicht \_ erforderlich (Wert = 0x10)</span><span class="sxs-lookup"><span data-stu-id="cc135-181">PLUGIN\_AUTH\_FLAGS\_KEEP\_ALIVE\_NOT\_REQUIRED (value=0x10)</span></span>

    <span data-ttu-id="cc135-182">Diese DLL erfordert keine permanente Verbindung für Ihre Challenge-Response-Sequenz.</span><span class="sxs-lookup"><span data-stu-id="cc135-182">This DLL does not require a persistent connection for its challenge-response sequence.</span></span>

<span data-ttu-id="cc135-183">Wenn Sie z. b. die NTLM-Authentifizierung hinzufügen möchten, muss der Schlüssel NTLM der **lokalen HKEY- \_ \_ Computer** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security** hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="cc135-183">For example, to add NTLM authentication, the key NTLM must be added to **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**.</span></span> <span data-ttu-id="cc135-184">Unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security** \\ **NTLM** müssen der Zeichen folgen Wert, der **dllfile**-Wert und der **DWORD** -Wert **Flags** hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="cc135-184">Under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**\\**NTLM**, the string value, **DLLFile**, and a **DWORD** value, **Flags**, must be added.</span></span> <span data-ttu-id="cc135-185">**Dllfile** muss auf Winsspi.dll festgelegt werden, und **Flags** müssen auf 0x08 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc135-185">**DLLFile** must be set to Winsspi.dll, and **Flags** must be set to 0x08.</span></span>

### <a name="server-authentication"></a><span data-ttu-id="cc135-186">Serverauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="cc135-186">Server Authentication</span></span>

<span data-ttu-id="cc135-187">Wenn ein Server eine Anforderung empfängt, die eine Authentifizierung erfordert, gibt der Server eine 401-Statuscode Meldung zurück.</span><span class="sxs-lookup"><span data-stu-id="cc135-187">When a server receives a request that requires authentication, the server returns a 401 status code message.</span></span> <span data-ttu-id="cc135-188">In dieser Meldung sollte der Server mindestens einen WWW-Authenticate Antwortheader enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc135-188">In that message, the server should include one or more WWW-Authenticate response headers.</span></span> <span data-ttu-id="cc135-189">Diese Header enthalten die Authentifizierungsmethoden, die der Server zur Verfügung gestellt hat.</span><span class="sxs-lookup"><span data-stu-id="cc135-189">These headers include the authentication methods the server has available.</span></span> <span data-ttu-id="cc135-190">WinInet wählt die erste Methode aus, die er erkennt.</span><span class="sxs-lookup"><span data-stu-id="cc135-190">WinINet chooses the first method it recognizes.</span></span>

<span data-ttu-id="cc135-191">Die Standard Authentifizierung bietet eine schwache Sicherheit, es sei denn, der Channel ist erstmalig mit SSL oder PCT verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="cc135-191">Basic authentication provides weak security unless the channel is first link-encrypted with SSL or PCT.</span></span>

<span data-ttu-id="cc135-192">Die [**internetterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) -Funktion kann verwendet werden, um die Benutzernamen-und Kenn Wort Daten vom Benutzer abzurufen, oder es kann eine angepasste Benutzeroberfläche entworfen werden, um die Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cc135-192">The [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) function can be used to obtain the user name and password data from the user, or a customized user interface can be designed to obtain the data.</span></span>

<span data-ttu-id="cc135-193">Eine benutzerdefinierte Schnittstelle kann die [**internettoption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) -Funktion verwenden, um die [Internet \_ Option \_ Password](option-flags.md) -und [Internet \_ Option \_ username](option-flags.md) -Werte festzulegen und die Anforderung dann erneut an den Server zu senden.</span><span class="sxs-lookup"><span data-stu-id="cc135-193">A custom interface can use the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function to set the [INTERNET\_OPTION\_PASSWORD](option-flags.md) and [INTERNET\_OPTION\_USERNAME](option-flags.md) values and then resend the request to the server.</span></span>

### <a name="proxy-authentication"></a><span data-ttu-id="cc135-194">Proxyauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="cc135-194">Proxy Authentication</span></span>

<span data-ttu-id="cc135-195">Wenn ein Client versucht, einen Proxy zu verwenden, der eine Authentifizierung erfordert, gibt der Proxy eine 407-Statuscode Meldung an den Client zurück.</span><span class="sxs-lookup"><span data-stu-id="cc135-195">When a client attempts to use a proxy that requires authentication, the proxy returns a 407 status code message to the client.</span></span> <span data-ttu-id="cc135-196">In dieser Meldung sollte der Proxy mindestens einen Proxy-Authenticate Antwortheader enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc135-196">In that message, the proxy should include one or more Proxy-Authenticate response headers.</span></span> <span data-ttu-id="cc135-197">Diese Header enthalten die vom Proxy verfügbaren Authentifizierungsmethoden.</span><span class="sxs-lookup"><span data-stu-id="cc135-197">These headers include the authentication methods available from the proxy.</span></span> <span data-ttu-id="cc135-198">WinInet wählt die erste Methode aus, die er erkennt.</span><span class="sxs-lookup"><span data-stu-id="cc135-198">WinINet chooses the first method it recognizes.</span></span>

<span data-ttu-id="cc135-199">Die [**internetterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) -Funktion kann verwendet werden, um die Benutzernamen-und Kenn Wort Daten vom Benutzer zu erhalten, oder es kann eine angepasste Benutzeroberfläche entworfen werden.</span><span class="sxs-lookup"><span data-stu-id="cc135-199">The [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) function can be used to obtain the user name and password data from the user, or a customized user interface can be designed.</span></span>

<span data-ttu-id="cc135-200">Eine benutzerdefinierte Schnittstelle kann die [**internettoption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) -Funktion verwenden, um die [Internet \_ Option \_ Proxy \_ Kennwort](option-flags.md) und [Internet \_ options \_ Proxy- \_ Benutzernamen](option-flags.md) Werte festzulegen und die Anforderung dann erneut an den Proxy zu senden.</span><span class="sxs-lookup"><span data-stu-id="cc135-200">A custom interface can use the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function to set the [INTERNET\_OPTION\_PROXY\_PASSWORD](option-flags.md) and [INTERNET\_OPTION\_PROXY\_USERNAME](option-flags.md) values and then resend the request to the proxy.</span></span>

<span data-ttu-id="cc135-201">Wenn kein Proxy Benutzername und kein Kennwort festgelegt sind, versucht WinInet, den Benutzernamen und das Kennwort für den Server zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cc135-201">If no proxy user name and password are set, WinINet attempts to use the user name and password for the server.</span></span> <span data-ttu-id="cc135-202">Dieses Verhalten ermöglicht es Clients, dieselbe angepasste Benutzeroberfläche zu implementieren, die zum Verarbeiten der Server Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc135-202">This behavior enables clients to implement the same customized user interface used to handle server authentication.</span></span>

## <a name="handling-http-authentication"></a><span data-ttu-id="cc135-203">Behandeln der HTTP-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="cc135-203">Handling HTTP Authentication</span></span>

<span data-ttu-id="cc135-204">Die HTTP-Authentifizierung kann entweder mit " [**internetterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) " oder mit einer benutzerdefinierten Funktion durchgeführt werden, die " [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) " verwendet oder eigene Authentifizierungs Header hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="cc135-204">HTTP authentication can be handled with either [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) or a customized function that uses [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) or adds its own authentication headers.</span></span> <span data-ttu-id="cc135-205">[**Internetzterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) kann die mit einem [**hinternethandle**](appendix-a-hinternet-handles.md) verknüpften Header untersuchen, um verborgene Fehler, wie z. b. Statuscodes von einem Proxy oder Server, zu suchen.</span><span class="sxs-lookup"><span data-stu-id="cc135-205">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) can examine the headers associated with an [**HINTERNET**](appendix-a-hinternet-handles.md) handle to find hidden errors, such as status codes from a proxy or server.</span></span> <span data-ttu-id="cc135-206">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) kann verwendet werden, um den Benutzernamen und das Kennwort für den Proxy und den Server festzulegen.</span><span class="sxs-lookup"><span data-stu-id="cc135-206">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) can be used to set the user name and password for the proxy and server.</span></span> <span data-ttu-id="cc135-207">Bei der MSN-und DPA-Authentifizierung muss [**internetterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) verwendet werden, um den Benutzernamen und das Kennwort festzulegen.</span><span class="sxs-lookup"><span data-stu-id="cc135-207">For MSN and DPA authentication, [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) must be used to set the user name and password.</span></span>

<span data-ttu-id="cc135-208">Für jede benutzerdefinierte Funktion, die eigene WWW-Authenticate oder Proxy-Authenticate Header hinzufügt, sollte das [Internet \_ Flag \_ No \_ auth](api-flags.md) -Flag festgelegt werden, um die Authentifizierung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="cc135-208">For any customized function that adds its own WWW-Authenticate or Proxy-Authenticate headers, the [INTERNET\_FLAG\_NO\_AUTH](api-flags.md) flag should be set to disable authentication.</span></span>

<span data-ttu-id="cc135-209">Im folgenden Beispiel wird gezeigt, wie mit [**internetterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) die HTTP-Authentifizierung behandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cc135-209">The following example shows how [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) can be used to handle HTTP authentication.</span></span>


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



<span data-ttu-id="cc135-210">Im Beispiel wird dwErrorCode verwendet, um alle Fehler zu speichern, die mit dem-Befehl von [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="cc135-210">In the example, dwErrorCode is used to store any errors associated with the call to [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="cc135-211">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) wird erfolgreich abgeschlossen, auch wenn für den Proxy oder Server eine Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cc135-211">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) completes successfully, even if the proxy or server requires authentication.</span></span> <span data-ttu-id="cc135-212">Wenn das \_ Flag Fehler UI-Filter für Fehler der Flags-Fehlermeldung \_ \_ \_ \_ an [**internetterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)übermittelt wird, prüft die Funktion die Header auf alle verdeckten Fehler.</span><span class="sxs-lookup"><span data-stu-id="cc135-212">When the FLAGS\_ERROR\_UI\_FILTER\_FOR\_ERRORS flag is passed to [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), the function checks the headers for any hidden errors.</span></span> <span data-ttu-id="cc135-213">Diese ausgeblendeten Fehler würden alle Authentifizierungsanforderungen einschließen.</span><span class="sxs-lookup"><span data-stu-id="cc135-213">These hidden errors would include any requests for authentication.</span></span> <span data-ttu-id="cc135-214">[**Interneterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) zeigt das entsprechende Dialogfeld an, in dem der Benutzer zur Eingabe der erforderlichen Daten aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="cc135-214">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) displays the appropriate dialog box to prompt the user for the necessary data.</span></span> <span data-ttu-id="cc135-215">Die Flags \_ \_ -Fehler \_ - \_ UI \_ -Flags Daten generieren Daten und Flags \_ Fehler \_ UI \_ Flags ändern-Flags \_ \_ müssen auch an [**interneterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)übermittelt werden, damit die Funktion die entsprechende Datenstruktur für den Fehler erstellt und die Ergebnisse des Dialog Felds im [**HINTERNET**](appendix-a-hinternet-handles.md) -handle speichert.</span><span class="sxs-lookup"><span data-stu-id="cc135-215">The FLAGS\_ERROR\_UI\_FLAGS\_GENERATE\_DATA and FLAGS\_ERROR\_UI\_FLAGS\_CHANGE\_OPTIONS flags should also be passed to [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), so that the function constructs the appropriate data structure for the error and stores the results of the dialog box in the [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>

<span data-ttu-id="cc135-216">Der folgende Beispielcode zeigt, wie die Authentifizierung mithilfe von [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="cc135-216">The following example code shows how authentication could be handled using [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


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
> <span data-ttu-id="cc135-217">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="cc135-217">WinINet does not support server implementations.</span></span> <span data-ttu-id="cc135-218">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc135-218">In addition, it should not be used from a service.</span></span> <span data-ttu-id="cc135-219">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="cc135-219">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 