---
description: Einige HTTP-Server und Proxys erfordern eine Authentifizierung, bevor Sie den Zugriff auf Ressourcen im Internet zulassen. Die Microsoft Windows HTTP-Dienste (WinHTTP) unterstützen die Server-und Proxy Authentifizierung für HTTP-Sitzungen.
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: Authentifizierung in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dd40e6da1f455e04e24fa740cf4d83da7e0472e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216172"
---
# <a name="authentication-in-winhttp"></a><span data-ttu-id="50023-104">Authentifizierung in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="50023-104">Authentication in WinHTTP</span></span>

<span data-ttu-id="50023-105">Einige HTTP-Server und Proxys erfordern eine Authentifizierung, bevor Sie den Zugriff auf Ressourcen im Internet zulassen.</span><span class="sxs-lookup"><span data-stu-id="50023-105">Some HTTP servers and proxies require authentication before allowing access to resources on the Internet.</span></span> <span data-ttu-id="50023-106">Die Microsoft Windows HTTP-Dienste (WinHTTP) unterstützen die Server-und Proxy Authentifizierung für HTTP-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="50023-106">The Microsoft Windows HTTP Services (WinHTTP) functions support server and proxy authentication for HTTP sessions.</span></span>

## <a name="about-http-authentication"></a><span data-ttu-id="50023-107">Informationen zur HTTP-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="50023-107">About HTTP Authentication</span></span>

<span data-ttu-id="50023-108">Wenn eine Authentifizierung erforderlich ist, empfängt die HTTP-Anwendung den Statuscode 401 (Server erfordert Authentifizierung) oder 407 (Proxy erfordert Authentifizierung).</span><span class="sxs-lookup"><span data-stu-id="50023-108">If authentication is required, the HTTP application receives a status code of 401 (server requires authentication) or 407 (proxy requires authentication).</span></span> <span data-ttu-id="50023-109">Zusammen mit dem Statuscode sendet der Proxy oder Server einen oder mehrere Authentifizierungsheader: WWW-Authenticate (für die Server Authentifizierung) oder Proxy-Authenticate (für die Proxy Authentifizierung).</span><span class="sxs-lookup"><span data-stu-id="50023-109">Along with the status code, the proxy or server sends one or more authenticate headers: WWW-Authenticate (for server authentication) or Proxy-Authenticate (for proxy authentication).</span></span>

<span data-ttu-id="50023-110">Jeder authentifizieren-Header enthält ein unterstütztes Authentifizierungsschema und für das Basis-und Digest-Schema einen Bereich.</span><span class="sxs-lookup"><span data-stu-id="50023-110">Each authenticate header contains a supported authentication scheme and, for the Basic and Digest schemes, a realm.</span></span> <span data-ttu-id="50023-111">Wenn mehrere Authentifizierungs Schemas unterstützt werden, gibt der Server mehrere authentifizieren-Header zurück.</span><span class="sxs-lookup"><span data-stu-id="50023-111">If multiple authentication schemes are supported, the server returns multiple authenticate headers.</span></span> <span data-ttu-id="50023-112">Beim Bereichs Wert wird die Groß-/Kleinschreibung beachtet, und es wird eine Gruppe von Servern oder Proxys definiert, für die dieselben Anmelde Informationen akzeptiert werden</span><span class="sxs-lookup"><span data-stu-id="50023-112">The realm value is case-sensitive and defines a set of servers or proxies for which the same credentials are accepted.</span></span> <span data-ttu-id="50023-113">Beispielsweise kann der Header "www-Authenticate: Basic Realm =" example "" zurückgegeben werden, wenn eine Server Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="50023-113">For example, the header "WWW-Authenticate: Basic Realm="example"" might be returned when server authentication is required.</span></span> <span data-ttu-id="50023-114">Dieser Header gibt an, dass Benutzer Anmelde Informationen für die "Beispiel Domäne" angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="50023-114">This header specifies that user credentials must be supplied for the "example" domain.</span></span>

<span data-ttu-id="50023-115">Eine HTTP-Anwendung kann ein Autorisierungs Header Feld mit einer Anforderung enthalten, die Sie an den Server sendet.</span><span class="sxs-lookup"><span data-stu-id="50023-115">An HTTP application can include an authorization header field with a request it sends to the server.</span></span> <span data-ttu-id="50023-116">Der Autorisierungs Header enthält das Authentifizierungsschema und die entsprechende Antwort, die für dieses Schema erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="50023-116">The authorization header contains the authentication scheme and the appropriate response required by that scheme.</span></span> <span data-ttu-id="50023-117">Beispielsweise würde die Kopfzeile "Authorization: Basic <username: Password>" der Anforderung hinzugefügt und an den Server gesendet, wenn der Client den Antwortheader "www-Authenticate: Basic Realm =" example "" empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="50023-117">For example, the header "Authorization: Basic <username:password>" would be added to the request and sent to the server if the client received the response header "WWW-Authenticate: Basic Realm="example"".</span></span>

> [!Note]  
> <span data-ttu-id="50023-118">Obwohl Sie hier als nur-Text angezeigt werden, sind der Benutzername und das Kennwort tatsächlich [*Base64-codiert*](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="50023-118">Although they are shown here as plain text, the username and password are actually [*base64 encoded*](glossary.md).</span></span>

 

<span data-ttu-id="50023-119">Es gibt zwei allgemeine Arten von Authentifizierungs Schemas:</span><span class="sxs-lookup"><span data-stu-id="50023-119">There are two general types of authentication schemes:</span></span>

-   <span data-ttu-id="50023-120">Standard Authentifizierungsschema, in dem der Benutzername und das Kennwort als Klartext an den Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="50023-120">Basic authentication scheme, in which the user name and password are sent in clear text to the server.</span></span>

    <span data-ttu-id="50023-121">Das Standard Authentifizierungsschema basiert auf dem Modell, das von einem Client mit einem Benutzernamen und einem Kennwort für jeden Bereich identifiziert werden muss.</span><span class="sxs-lookup"><span data-stu-id="50023-121">The Basic authentication scheme is based on the model that a client must identify itself with a user name and password for each realm.</span></span> <span data-ttu-id="50023-122">Der Server verwendet die Anforderung nur, wenn die Anforderung mit einem Autorisierungs Header gesendet wird, der einen gültigen Benutzernamen und ein gültiges Kennwort enthält.</span><span class="sxs-lookup"><span data-stu-id="50023-122">The server services the request only if the request is sent with an authorization header that includes a valid user name and password.</span></span>

-   <span data-ttu-id="50023-123">Challenge-Response-Schemas, wie z. b. Kerberos, bei denen der Client den Client mit [*Authentifizierungsdaten*](glossary.md)herausfordert.</span><span class="sxs-lookup"><span data-stu-id="50023-123">Challenge-response schemes, such as Kerberos, in which the server challenges the client with [*authentication data*](glossary.md).</span></span> <span data-ttu-id="50023-124">Der Client wandelt die Daten mit den Benutzer Anmelde Informationen um und sendet die transformierten Daten zur Authentifizierung an den Server zurück.</span><span class="sxs-lookup"><span data-stu-id="50023-124">The client transforms the data with the user credentials and sends the transformed data back to the server for authentication.</span></span>

    <span data-ttu-id="50023-125">Mit Challenge-Response-Schemas wird eine sicherere Authentifizierung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="50023-125">Challenge-response schemes enable a more secure authentication.</span></span> <span data-ttu-id="50023-126">In einem Challenge-Response-Schema werden Benutzername und Kennwort niemals über das Netzwerk übertragen.</span><span class="sxs-lookup"><span data-stu-id="50023-126">In a challenge-response scheme, the username and password are never transmitted over the network.</span></span> <span data-ttu-id="50023-127">Nachdem der Client ein Challenge-Response-Schema ausgewählt hat, gibt der Server einen entsprechenden Statuscode mit einer Herausforderung zurück, die die [*Authentifizierungsdaten*](glossary.md) für dieses Schema enthält.</span><span class="sxs-lookup"><span data-stu-id="50023-127">After the client selects a challenge-response scheme, the server returns an appropriate status code with a challenge that contains the [*authentication data*](glossary.md) for that scheme.</span></span> <span data-ttu-id="50023-128">Der Client sendet die Anforderung dann erneut mit der richtigen Antwort, um den angeforderten Dienst abzurufen.</span><span class="sxs-lookup"><span data-stu-id="50023-128">The client then resends the request with the proper response to obtain the requested service.</span></span> <span data-ttu-id="50023-129">Mit Challenge-Response-Schemas können mehrere Austausch Vorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="50023-129">Challenge-response schemes can take multiple exchanges to complete.</span></span>

<span data-ttu-id="50023-130">Die folgende Tabelle enthält die Authentifizierungs Schemas, die von WinHTTP unterstützt werden, den Authentifizierungstyp und eine Beschreibung des Schemas.</span><span class="sxs-lookup"><span data-stu-id="50023-130">The following table contains the authentication schemes that are supported by WinHTTP, the authentication type, and a description of the scheme.</span></span>



| <span data-ttu-id="50023-131">Schema</span><span class="sxs-lookup"><span data-stu-id="50023-131">Scheme</span></span>            | <span data-ttu-id="50023-132">type</span><span class="sxs-lookup"><span data-stu-id="50023-132">Type</span></span>               | <span data-ttu-id="50023-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50023-133">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50023-134">Basic (nur-Text)</span><span class="sxs-lookup"><span data-stu-id="50023-134">Basic (plaintext)</span></span> | <span data-ttu-id="50023-135">Basic</span><span class="sxs-lookup"><span data-stu-id="50023-135">Basic</span></span>              | <span data-ttu-id="50023-136">Verwendet eine [*Base64-codierte*](glossary.md) Zeichenfolge, die den Benutzernamen und das Kennwort enthält.</span><span class="sxs-lookup"><span data-stu-id="50023-136">Uses a [*base64 encoded*](glossary.md) string that contains the user name and password.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="50023-137">Digest</span><span class="sxs-lookup"><span data-stu-id="50023-137">Digest</span></span>            | <span data-ttu-id="50023-138">Challenge-Response</span><span class="sxs-lookup"><span data-stu-id="50023-138">Challenge-response</span></span> | <span data-ttu-id="50023-139">Herausforderungen bei der Verwendung eines Nonce-Werts (eine vom Server angegebene Daten Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="50023-139">Challenges using a nonce (a server-specified data string) value.</span></span> <span data-ttu-id="50023-140">Eine gültige Antwort enthält eine Prüfsumme aus dem Benutzernamen, dem Kennwort, dem angegebenen Nonce-Wert, dem [*http-Verb*](glossary.md)und dem angeforderten Uniform Resource Identifier (URI).</span><span class="sxs-lookup"><span data-stu-id="50023-140">A valid response contains a checksum of the user name, the password, the given nonce value, the [*HTTP verb*](glossary.md), and the requested Uniform Resource Identifier (URI).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="50023-141">NTLM</span><span class="sxs-lookup"><span data-stu-id="50023-141">NTLM</span></span>              | <span data-ttu-id="50023-142">Challenge-Response</span><span class="sxs-lookup"><span data-stu-id="50023-142">Challenge-response</span></span> | <span data-ttu-id="50023-143">Erfordert, dass die [*Authentifizierungsdaten*](glossary.md) mit den Benutzer Anmelde Informationen transformiert werden, um die Identität nachzuweisen.</span><span class="sxs-lookup"><span data-stu-id="50023-143">Requires the [*authentication data*](glossary.md) to be transformed with the user credentials to prove identity.</span></span> <span data-ttu-id="50023-144">Damit die NTLM-Authentifizierung ordnungsgemäß funktioniert, müssen mehrere Austausch Vorgänge für dieselbe Verbindung stattfinden.</span><span class="sxs-lookup"><span data-stu-id="50023-144">For NTLM authentication to function correctly, several exchanges must take place on the same connection.</span></span> <span data-ttu-id="50023-145">Daher kann die NTLM-Authentifizierung nicht verwendet werden, wenn ein zwischengeschalteter Proxy keine Keep-Alive-Verbindungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="50023-145">Therefore, NTLM authentication cannot be used if an intervening proxy does not support keep-alive connections.</span></span> <span data-ttu-id="50023-146">Die NTLM-Authentifizierung schlägt auch fehl, wenn [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit dem WinHTTP-Flag " [**\_ Keep- \_ \_ Alive deaktivieren**](option-flags.md) " verwendet wird, das die Keep-Alive-Semantik deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="50023-146">NTLM authentication also fails if [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) is used with the [**WINHTTP\_DISABLE\_KEEP\_ALIVE**](option-flags.md) flag that disables keep-alive semantics.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="50023-147">Passport</span><span class="sxs-lookup"><span data-stu-id="50023-147">Passport</span></span>          | <span data-ttu-id="50023-148">Challenge-Response</span><span class="sxs-lookup"><span data-stu-id="50023-148">Challenge-response</span></span> | <span data-ttu-id="50023-149">Verwendet [Microsoft Passport 1,4](passport-authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="50023-149">Uses [Microsoft Passport 1.4](passport-authentication-in-winhttp.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="50023-150">Aushandeln</span><span class="sxs-lookup"><span data-stu-id="50023-150">Negotiate</span></span>         | <span data-ttu-id="50023-151">Challenge-Response</span><span class="sxs-lookup"><span data-stu-id="50023-151">Challenge-response</span></span> | <span data-ttu-id="50023-152">Wenn sowohl der Server als auch der Client Windows 2000 oder höher verwenden, wird die Kerberos-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="50023-152">If both the server and client are using Windows 2000 or later, Kerberos authentication is used.</span></span> <span data-ttu-id="50023-153">Andernfalls wird die NTLM-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="50023-153">Otherwise NTLM authentication is used.</span></span> <span data-ttu-id="50023-154">Kerberos ist in Windows 2000 und höheren Betriebssystemen verfügbar und wird als sicherer als die NTLM-Authentifizierung eingestuft.</span><span class="sxs-lookup"><span data-stu-id="50023-154">Kerberos is available in Windows 2000 and later operating systems and is considered to be more secure than NTLM authentication.</span></span> <span data-ttu-id="50023-155">Damit die Aushandlungs Authentifizierung ordnungsgemäß funktioniert, müssen mehrere Austausch Vorgänge für dieselbe Verbindung stattfinden.</span><span class="sxs-lookup"><span data-stu-id="50023-155">For Negotiate authentication to function correctly, several exchanges must take place on the same connection.</span></span> <span data-ttu-id="50023-156">Daher können Aushandlungs Authentifizierung nicht verwendet werden, wenn ein zwischengeschalteter Proxy keine Keep-Alive-Verbindungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="50023-156">Therefore, Negotiate authentication cannot be used if an intervening proxy does not support keep-alive connections.</span></span> <span data-ttu-id="50023-157">Bei der Aushandlung der Authentifizierung tritt auch dann ein Fehler auf, wenn [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit dem WinHTTP-Flag zum Aktivieren von [**\_ Keep- \_ \_ Alive**](option-flags.md) verwendet wird</span><span class="sxs-lookup"><span data-stu-id="50023-157">Negotiate authentication also fails if [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) is used with the [**WINHTTP\_DISABLE\_KEEP\_ALIVE**](option-flags.md) flag that disables keep-alive semantics.</span></span> <span data-ttu-id="50023-158">Das Aushandlungs Authentifizierungsschema wird manchmal als integrierte Windows-Authentifizierung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="50023-158">The Negotiate authentication scheme is sometimes called Integrated Windows authentication.</span></span> |



 

## <a name="authentication-in-winhttp-applications"></a><span data-ttu-id="50023-159">Authentifizierung in WinHTTP-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="50023-159">Authentication in WinHTTP Applications</span></span>

<span data-ttu-id="50023-160">Die WinHTTP-API (Application Programming Interface) stellt zwei Funktionen bereit, die für den Zugriff auf Internet Ressourcen in Situationen verwendet werden, in denen eine Authentifizierung erforderlich ist: [**winhttpsetanmelde**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) Informationen und [**winhttpqueryauthschemas**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).</span><span class="sxs-lookup"><span data-stu-id="50023-160">The WinHTTP application programming interface (API) provides two functions used to access Internet resources in situations where authentication is required: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) and [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).</span></span>

<span data-ttu-id="50023-161">Wenn eine Antwort mit einem 401-oder 407-Statuscode empfangen wird, kann [**winhttpqueryauthschemas**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) zum Analysieren der Authentifizierungs Header verwendet werden, um die unterstützten Authentifizierungs Schemas und das Authentifizierungs Ziel zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="50023-161">When a response is received with a 401 or 407 status code, [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) can be used to parse the authentication headers to determine the supported authentication schemes and the authentication target.</span></span> <span data-ttu-id="50023-162">Das Authentifizierungs Ziel ist der Server oder Proxy, der die Authentifizierung anfordert.</span><span class="sxs-lookup"><span data-stu-id="50023-162">The authentication target is the server or proxy that requests authentication.</span></span> <span data-ttu-id="50023-163">**Winhttpqueryauthschemas** bestimmt auch das erste Authentifizierungsschema aus den verfügbaren Schemas, basierend auf den vom Server empfohlenen Authentifizierungsschema Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="50023-163">**WinHttpQueryAuthSchemes** also determines the first authentication scheme, from the available schemes, based on the authentication scheme preferences suggested by the server.</span></span> <span data-ttu-id="50023-164">Diese Methode zum Auswählen eines Authentifizierungs Schemas ist das von [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)vorgeschlagene Verhalten.</span><span class="sxs-lookup"><span data-stu-id="50023-164">This method for choosing an authentication scheme is the behavior suggested by [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

<span data-ttu-id="50023-165">Mit [**winhttpsetanmelde**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) Informationen kann eine Anwendung das Authentifizierungsschema angeben, das zusammen mit einem gültigen Benutzernamen und Kennwort für die Verwendung auf dem Zielserver oder Proxy verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="50023-165">[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) enables an application to specify the authentication scheme that is used along with a valid username and password for use on the target server or proxy.</span></span> <span data-ttu-id="50023-166">Nachdem Sie die Anmelde Informationen festgelegt und die Anforderung erneut gesendet haben, werden die erforderlichen Header generiert und automatisch der Anforderung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="50023-166">After setting the credentials and resending the request, the necessary headers are generated and added to the request automatically.</span></span> <span data-ttu-id="50023-167">Da für einige Authentifizierungs Schemas mehrere Transaktionen erforderlich sind, kann [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) den Fehler "Fehler bei \_ WinHTTP \_ Resend Request" zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="50023-167">Because some authentication schemes require multiple transactions [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) could return the error, ERROR\_WINHTTP\_RESEND\_REQUEST.</span></span> <span data-ttu-id="50023-168">Wenn dieser Fehler auftritt, sollte die Anwendung die Anforderung weiter senden, bis eine Antwort empfangen wird, die keinen 401-oder 407-Statuscode enthält.</span><span class="sxs-lookup"><span data-stu-id="50023-168">When this error is encountered, the application should continue to resend the request until a response is received that does not contain a 401 or 407 status code.</span></span> <span data-ttu-id="50023-169">Der 200-Statuscode gibt an, dass die Ressource verfügbar ist und die Anforderung erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="50023-169">A 200 status code indicates that the resource is available and the request is successful.</span></span> <span data-ttu-id="50023-170">Weitere Status Codes, die zurückgegeben werden können, finden Sie unter [**HTTP-Statuscodes**](http-status-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="50023-170">See [**HTTP Status Codes**](http-status-codes.md) for additional status codes that can be returned.</span></span>

<span data-ttu-id="50023-171">Wenn ein akzeptables Authentifizierungsschema und Anmelde Informationen bekannt sind, bevor eine Anforderung an den Server gesendet wird, kann eine Anwendung [**winhttpsetanmelde**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) Informationen aufrufen, bevor [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="50023-171">If an acceptable authentication scheme and credentials are known before a request is sent to the server, an application can call [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) before calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="50023-172">In diesem Fall versucht WinHTTP die Vorauthentifizierung beim Server durch Bereitstellen von Anmelde Informationen oder [*Authentifizierungsdaten*](glossary.md) in der ursprünglichen Anforderung an den Server.</span><span class="sxs-lookup"><span data-stu-id="50023-172">In this case, WinHTTP attempts pre-authentication with the server by providing credentials or [*authentication data*](glossary.md) in the initial request to the server.</span></span> <span data-ttu-id="50023-173">Die Vorauthentifizierung kann die Anzahl der Austausch Vorgänge im Authentifizierungsprozess verringern und somit die Anwendungsleistung verbessern.</span><span class="sxs-lookup"><span data-stu-id="50023-173">Pre-authentication can decrease the number of exchanges in the authentication process and therefore improve application performance.</span></span>

<span data-ttu-id="50023-174">Die Vorauthentifizierung kann mit den folgenden Authentifizierungs Schemas verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="50023-174">Preauthentication can be used with the following authentication schemes:</span></span>

-   <span data-ttu-id="50023-175">Basic: immer möglich.</span><span class="sxs-lookup"><span data-stu-id="50023-175">Basic - always possible.</span></span>
-   <span data-ttu-id="50023-176">Aushandlung in Kerberos aushandeln (sehr wahrscheinlich möglich) die einzige Ausnahme ist, wenn die Zeitverschiebung zwischen dem Client und dem Domänen Controller deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="50023-176">Negotiate resolving into Kerberos - very likely possible; the only exception is when the time-skews are off between the client and the domain controller.</span></span>
-   <span data-ttu-id="50023-177">(Aushandeln in NTLM aushandeln)-nie möglich.</span><span class="sxs-lookup"><span data-stu-id="50023-177">(Negotiate resolving into NTLM) - never possible.</span></span>
-   <span data-ttu-id="50023-178">NTLM-möglich nur in Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="50023-178">NTLM - possible in Windows Server 2008 R2 only.</span></span>
-   <span data-ttu-id="50023-179">Digest: nie möglich.</span><span class="sxs-lookup"><span data-stu-id="50023-179">Digest - never possible.</span></span>
-   <span data-ttu-id="50023-180">Passport-nie möglich; nach der anfänglichen Abfrage Antwort verwendet WinHTTP Cookies, um sich vorab bei Passport zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="50023-180">Passport - never possible; after the initial challenge-response, WinHTTP uses cookies to pre-authenticate to Passport.</span></span>

<span data-ttu-id="50023-181">Eine typische WinHTTP-Anwendung führt die folgenden Schritte aus, um die Authentifizierung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="50023-181">A typical WinHTTP application completes the following steps in order to handle authentication.</span></span>

-   <span data-ttu-id="50023-182">Fordern Sie eine Ressource mit " [**winhttpopanrequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) " und " [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)" an.</span><span class="sxs-lookup"><span data-stu-id="50023-182">Request a resource with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) and [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>
-   <span data-ttu-id="50023-183">Überprüfen Sie die Antwortheader mit [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="50023-183">Check the response headers with [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>
-   <span data-ttu-id="50023-184">Wenn ein 401-oder 407-Statuscode zurückgegeben wird, der angibt, dass eine Authentifizierung erforderlich ist, wenden Sie [**winhttpqueryauthschemas**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) an, um ein akzeptables Schema</span><span class="sxs-lookup"><span data-stu-id="50023-184">If a 401 or 407 status code is returned indicating that authentication is required, call [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) to find an acceptable scheme.</span></span>
-   <span data-ttu-id="50023-185">Legen Sie das Authentifizierungsschema, den Benutzernamen und das Kennwort mit [**winhttpsetanmelde**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)Informationen fest.</span><span class="sxs-lookup"><span data-stu-id="50023-185">Set the authentication scheme, username, and password with [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).</span></span>
-   <span data-ttu-id="50023-186">Senden Sie die Anforderung mit dem gleichen Anforderungs handle erneut, indem Sie [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="50023-186">Resend the request with the same request handle by calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

<span data-ttu-id="50023-187">Die von [**winhttpsetanmelde**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) Informationen festgelegten Anmelde Informationen werden nur für eine Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="50023-187">The credentials set by [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) are only used for one request.</span></span> <span data-ttu-id="50023-188">WinHTTP speichert die Anmelde Informationen für die Verwendung in anderen Anforderungen nicht zwischen, was bedeutet, dass Anwendungen geschrieben werden müssen, die auf mehrere Anforderungen reagieren können.</span><span class="sxs-lookup"><span data-stu-id="50023-188">WinHTTP does not cache the credentials to use in other requests, which means that applications must be written that can respond to multiple requests.</span></span> <span data-ttu-id="50023-189">Wenn eine authentifizierte Verbindung wieder verwendet wird, werden andere Anforderungen möglicherweise nicht gestellt, aber Ihr Code sollte jederzeit auf eine Anforderung Antworten können.</span><span class="sxs-lookup"><span data-stu-id="50023-189">If an authenticated connection is re-used, other requests may not be challenged, but your code should be able to respond to a request at any time.</span></span>

### <a name="example-retrieving-a-document"></a><span data-ttu-id="50023-190">Beispiel: Abrufen eines Dokuments</span><span class="sxs-lookup"><span data-stu-id="50023-190">Example: Retrieving a Document</span></span>

<span data-ttu-id="50023-191">Der folgende Beispielcode versucht, ein angegebenes Dokument von einem HTTP-Server abzurufen.</span><span class="sxs-lookup"><span data-stu-id="50023-191">The following sample code attempts to retrieve a specified document from an HTTP server.</span></span> <span data-ttu-id="50023-192">Der Statuscode wird aus der Antwort abgerufen, um zu bestimmen, ob eine Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="50023-192">The status code is retrieved from the response to determine if authentication is required.</span></span> <span data-ttu-id="50023-193">Wenn ein 200-Statuscode gefunden wird, ist das Dokument verfügbar.</span><span class="sxs-lookup"><span data-stu-id="50023-193">If a 200 status code is found, the document is available.</span></span> <span data-ttu-id="50023-194">Wenn ein Statuscode von 401 oder 407 gefunden wird, ist eine Authentifizierung erforderlich, bevor das Dokument abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="50023-194">If a status code of 401 or 407 is found, authentication is required before the document can be retrieved.</span></span> <span data-ttu-id="50023-195">Bei jedem anderen Statuscode wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="50023-195">For any other status code, an error message is displayed.</span></span> <span data-ttu-id="50023-196">Eine Liste der möglichen Status Codes finden Sie unter [**HTTP-Statuscodes**](http-status-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="50023-196">See [**HTTP Status Codes**](http-status-codes.md) for a list of possible status codes.</span></span>


```C++
#include <windows.h>
#include <winhttp.h>
#include <stdio.h>

#pragma comment(lib, "winhttp.lib")

DWORD ChooseAuthScheme( DWORD dwSupportedSchemes )
{
  //  It is the server's responsibility only to accept 
  //  authentication schemes that provide a sufficient
  //  level of security to protect the servers resources.
  //
  //  The client is also obligated only to use an authentication
  //  scheme that adequately protects its username and password.
  //
  //  Thus, this sample code does not use Basic authentication  
  //  becaus Basic authentication exposes the client's username
  //  and password to anyone monitoring the connection.
  
  if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NEGOTIATE )
    return WINHTTP_AUTH_SCHEME_NEGOTIATE;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NTLM )
    return WINHTTP_AUTH_SCHEME_NTLM;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_PASSPORT )
    return WINHTTP_AUTH_SCHEME_PASSPORT;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_DIGEST )
    return WINHTTP_AUTH_SCHEME_DIGEST;
  else
    return 0;
}

struct SWinHttpSampleGet
{
  LPCWSTR szServer;
  LPCWSTR szPath;
  BOOL fUseSSL;
  LPCWSTR szServerUsername;
  LPCWSTR szServerPassword;
  LPCWSTR szProxyUsername;
  LPCWSTR szProxyPassword;
};

void WinHttpAuthSample( IN SWinHttpSampleGet *pGetRequest )
{
  DWORD dwStatusCode = 0;
  DWORD dwSupportedSchemes;
  DWORD dwFirstScheme;
  DWORD dwSelectedScheme;
  DWORD dwTarget;
  DWORD dwLastStatus = 0;
  DWORD dwSize = sizeof(DWORD);
  BOOL  bResults = FALSE;
  BOOL  bDone = FALSE;

  DWORD dwProxyAuthScheme = 0;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  INTERNET_PORT nPort = ( pGetRequest->fUseSSL ) ? 
                        INTERNET_DEFAULT_HTTPS_PORT  :
                        INTERNET_DEFAULT_HTTP_PORT;

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, 
                               pGetRequest->szServer, 
                               nPort, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, 
                                   L"GET", 
                                   pGetRequest->szPath,
                                   NULL, 
                                   WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES,
                                   ( pGetRequest->fUseSSL ) ? 
                                       WINHTTP_FLAG_SECURE : 0 );

  // Continue to send a request until status code 
  // is not 401 or 407.
  if( hRequest == NULL )
    bDone = TRUE;

  while( !bDone )
  {
    //  If a proxy authentication challenge was responded to, reset
    //  those credentials before each SendRequest, because the proxy  
    //  may require re-authentication after responding to a 401 or  
    //  to a redirect. If you don't, you can get into a 
    //  407-401-407-401- loop.
    if( dwProxyAuthScheme != 0 )
      bResults = WinHttpSetCredentials( hRequest, 
                                        WINHTTP_AUTH_TARGET_PROXY, 
                                        dwProxyAuthScheme, 
                                        pGetRequest->szProxyUsername,
                                        pGetRequest->szProxyPassword,
                                        NULL );
    // Send a request.
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS,
                                   0,
                                   WINHTTP_NO_REQUEST_DATA,
                                   0, 
                                   0, 
                                   0 );

    // End the request.
    if( bResults )
      bResults = WinHttpReceiveResponse( hRequest, NULL );

    // Resend the request in case of 
    // ERROR_WINHTTP_RESEND_REQUEST error.
    if( !bResults && GetLastError( ) == ERROR_WINHTTP_RESEND_REQUEST)
        continue;

    // Check the status code.
    if( bResults ) 
      bResults = WinHttpQueryHeaders( hRequest, 
                                      WINHTTP_QUERY_STATUS_CODE |
                                      WINHTTP_QUERY_FLAG_NUMBER,
                                      NULL, 
                                      &dwStatusCode, 
                                      &dwSize, 
                                      NULL );

    if( bResults )
    {
      switch( dwStatusCode )
      {
        case 200: 
          // The resource was successfully retrieved.
          // You can use WinHttpReadData to read the 
          // contents of the server's response.
          printf( "The resource was successfully retrieved.\n" );
          bDone = TRUE;
          break;

        case 401:
          // The server requires authentication.
          printf(" The server requires authentication. Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
          {
            dwSelectedScheme = ChooseAuthScheme( dwSupportedSchemes);

            if( dwSelectedScheme == 0 )
              bDone = TRUE;
            else
              bResults = WinHttpSetCredentials( hRequest, 
                                        dwTarget, 
                                        dwSelectedScheme,
                                        pGetRequest->szServerUsername,
                                        pGetRequest->szServerPassword,
                                        NULL );
          }

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check
          // for a repeated sequence of status codes.
          if( dwLastStatus == 401 )
            bDone = TRUE;

          break;

        case 407:
          // The proxy requires authentication.
          printf( "The proxy requires authentication.  Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
            dwProxyAuthScheme = ChooseAuthScheme(dwSupportedSchemes);

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check 
          // for a repeated sequence of status codes.
          if( dwLastStatus == 407 )
            bDone = TRUE;
          break;

        default:
          // The status code does not indicate success.
          printf("Error. Status code %d returned.\n", dwStatusCode);
          bDone = TRUE;
      }
    }

    // Keep track of the last status code.
    dwLastStatus = dwStatusCode;

    // If there are any errors, break out of the loop.
    if( !bResults ) 
        bDone = TRUE;
  }

  // Report any errors.
  if( !bResults )
  {
    DWORD dwLastError = GetLastError( );
    printf( "Error %d has occurred.\n", dwLastError );
  }

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
}

```



## <a name="automatic-logon-policy"></a><span data-ttu-id="50023-197">Richtlinie für automatische Anmeldung</span><span class="sxs-lookup"><span data-stu-id="50023-197">Automatic Logon Policy</span></span>

<span data-ttu-id="50023-198">Die Richtlinie für die automatische Anmeldung (automatische Anmeldung) bestimmt, wann WinHTTP die Standard Anmelde Informationen in eine Anforderung aufnehmen kann.</span><span class="sxs-lookup"><span data-stu-id="50023-198">The automatic logon (auto-logon) policy determines when it is acceptable for WinHTTP to include the default credentials in a request.</span></span> <span data-ttu-id="50023-199">Die Standard Anmelde Informationen sind entweder das aktuelle Thread Token oder das Sitzungs Token, abhängig davon, ob WinHTTP im synchronen oder asynchronen Modus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="50023-199">The default credentials are either the current thread token or the session token depending on whether WinHTTP is used in synchronous or asynchronous mode.</span></span> <span data-ttu-id="50023-200">Das Thread Token wird im synchronen Modus verwendet, und das Sitzungs Token wird im asynchronen Modus verwendet.</span><span class="sxs-lookup"><span data-stu-id="50023-200">The thread token is used in synchronous mode, and the session token is used in asynchronous mode.</span></span> <span data-ttu-id="50023-201">Diese Standard Anmelde Informationen sind häufig der Benutzername und das Kennwort, die für die Anmeldung bei Microsoft Windows verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50023-201">These default credentials are often the username and password used to log on to Microsoft Windows.</span></span>

<span data-ttu-id="50023-202">Die Richtlinie für die automatische Anmeldung wurde implementiert, um zu verhindern, dass diese Anmelde Informationen für die Authentifizierung bei einem nicht vertrauenswürdigen Server verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50023-202">The auto-logon policy was implemented to prevent these credentials from being casually used to authenticate against an untrusted server.</span></span> <span data-ttu-id="50023-203">Standardmäßig ist die Sicherheitsstufe auf WinHTTP \_ Autologon \_ Security \_ Level Medium festgelegt, sodass \_ die Standard Anmelde Informationen nur für Intranetanforderungen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="50023-203">By default, the security level is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM, which allows the default credentials to be used only for Intranet requests.</span></span> <span data-ttu-id="50023-204">Die Richtlinie für die automatische Anmeldung gilt nur für NTLM-und Aushandlungs Authentifizierungs Schemas.</span><span class="sxs-lookup"><span data-stu-id="50023-204">The auto-logon policy only applies to the NTLM and Negotiate authentication schemes.</span></span> <span data-ttu-id="50023-205">Anmelde Informationen werden nie automatisch mit anderen Schemas übertragen.</span><span class="sxs-lookup"><span data-stu-id="50023-205">Credentials are never automatically transmitted with other schemes.</span></span>

<span data-ttu-id="50023-206">Die Richtlinie für die automatische Anmeldung kann mithilfe der [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) -Funktion mit der [**WinHTTP- \_ Option \_ Autologon \_**](option-flags.md) -Richtlinienflag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="50023-206">The auto-logon policy can be set using the [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) function with the [**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**](option-flags.md) flag.</span></span> <span data-ttu-id="50023-207">Dieses Flag gilt nur für das Anforderungs handle.</span><span class="sxs-lookup"><span data-stu-id="50023-207">This flag applies only to the request handle.</span></span> <span data-ttu-id="50023-208">Wenn die Richtlinie auf WinHTTP \_ Autologon \_ Security Level Low festgelegt ist \_ \_ , können Standard Anmelde Informationen an alle Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="50023-208">When the policy is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW, default credentials can be sent to all servers.</span></span> <span data-ttu-id="50023-209">Wenn die Richtlinie auf WinHTTP \_ Autologon \_ Security Level High festgelegt ist \_ \_ , können keine Standard Anmelde Informationen für die Authentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50023-209">When the policy is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH, default credentials cannot be used for authentication.</span></span> <span data-ttu-id="50023-210">Es wird dringend empfohlen, die automatische Anmeldung auf mittlerer Ebene zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="50023-210">It is strongly recommended that you use the auto-logon at the MEDIUM level.</span></span>

## <a name="stored-user-names-and-passwords"></a><span data-ttu-id="50023-211">Gespeicherte Benutzernamen und Kennwörter</span><span class="sxs-lookup"><span data-stu-id="50023-211">Stored User Names and Passwords</span></span>

<span data-ttu-id="50023-212">In Windows XP wurde das Konzept von gespeicherten Benutzernamen und Kenn Wörtern eingeführt.</span><span class="sxs-lookup"><span data-stu-id="50023-212">Windows XP introduced the concept of Stored User Names and Passwords.</span></span> <span data-ttu-id="50023-213">Wenn die Passport-Anmelde Informationen eines Benutzers über den **Passport-Registrierungs-Assistenten** oder das Standard **Dialogfeld** Anmelde Informationen gespeichert werden, werden diese in den gespeicherten Benutzernamen und Kenn Wörtern gespeichert.</span><span class="sxs-lookup"><span data-stu-id="50023-213">If a user's Passport credentials are saved through the **Passport Registration Wizard** or the standard **Credential Dialog**, it is saved in the Stored User Names and Passwords.</span></span> <span data-ttu-id="50023-214">Bei Verwendung von WinHTTP unter Windows XP oder höher verwendet WinHTTP automatisch die Anmelde Informationen in den gespeicherten Benutzernamen und Kenn Wörtern, wenn die Anmelde Informationen nicht explizit festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="50023-214">When using WinHTTP on Windows XP or later, WinHTTP automatically uses the credentials in the Stored User Names and Passwords if credentials are not explicitly set.</span></span> <span data-ttu-id="50023-215">Dies ähnelt der Unterstützung von Standard Anmelde Informationen für NTLM/Kerberos.</span><span class="sxs-lookup"><span data-stu-id="50023-215">This is similar to the support of default logon credentials for NTLM/Kerberos.</span></span> <span data-ttu-id="50023-216">Die Verwendung von standardmäßigen Passport-Anmelde Informationen unterliegt jedoch nicht den Einstellungen für die automatische Anmelde Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="50023-216">However, use of default Passport credentials is not subject to the automatic logon policy settings.</span></span>

 

 



