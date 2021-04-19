---
description: Einige HTTP-Server und Proxys erfordern eine Authentifizierung, bevor der Zugriff auf Ressourcen im Internet zugelassen wird. Die WinHTTP-Funktionen (Microsoft Windows HTTP Services) unterstützen die Server- und Proxyauthentifizierung für HTTP-Sitzungen.
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: Authentifizierung in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75c6703e9d28902c5705f0b8ab8433193c4d085
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380826"
---
# <a name="authentication-in-winhttp"></a><span data-ttu-id="fcfe5-104">Authentifizierung in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fcfe5-104">Authentication in WinHTTP</span></span>

<span data-ttu-id="fcfe5-105">Einige HTTP-Server und Proxys erfordern eine Authentifizierung, bevor der Zugriff auf Ressourcen im Internet zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-105">Some HTTP servers and proxies require authentication before allowing access to resources on the Internet.</span></span> <span data-ttu-id="fcfe5-106">Die WinHTTP-Funktionen (Microsoft Windows HTTP Services) unterstützen die Server- und Proxyauthentifizierung für HTTP-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-106">The Microsoft Windows HTTP Services (WinHTTP) functions support server and proxy authentication for HTTP sessions.</span></span>

## <a name="about-http-authentication"></a><span data-ttu-id="fcfe5-107">Informationen zur HTTP-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="fcfe5-107">About HTTP Authentication</span></span>

<span data-ttu-id="fcfe5-108">Wenn eine Authentifizierung erforderlich ist, erhält die HTTP-Anwendung den Statuscode 401 (Server erfordert Authentifizierung) oder 407 (Proxy erfordert Authentifizierung).</span><span class="sxs-lookup"><span data-stu-id="fcfe5-108">If authentication is required, the HTTP application receives a status code of 401 (server requires authentication) or 407 (proxy requires authentication).</span></span> <span data-ttu-id="fcfe5-109">Zusammen mit dem Statuscode sendet der Proxy oder Server einen oder mehrere Authentifizierungsheader: WWW-Authenticate (für die Serverauthentifizierung) oder Proxy-Authenticate (für die Proxyauthentifizierung).</span><span class="sxs-lookup"><span data-stu-id="fcfe5-109">Along with the status code, the proxy or server sends one or more authenticate headers: WWW-Authenticate (for server authentication) or Proxy-Authenticate (for proxy authentication).</span></span>

<span data-ttu-id="fcfe5-110">Jeder Authentifizierungsheader enthält ein unterstütztes Authentifizierungsschema und für die Schemas Basic und Digest einen Bereich.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-110">Each authenticate header contains a supported authentication scheme and, for the Basic and Digest schemes, a realm.</span></span> <span data-ttu-id="fcfe5-111">Wenn mehrere Authentifizierungsschemas unterstützt werden, gibt der Server mehrere Authentifizierungsheader zurück.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-111">If multiple authentication schemes are supported, the server returns multiple authenticate headers.</span></span> <span data-ttu-id="fcfe5-112">Beim Bereichswert wird die Groß-/Kleinschreibung beachtet, und es wird ein Satz von Servern oder Proxys definiert, für die die gleichen Anmeldeinformationen akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-112">The realm value is case-sensitive and defines a set of servers or proxies for which the same credentials are accepted.</span></span> <span data-ttu-id="fcfe5-113">Beispielsweise kann der Header "WWW-Authenticate: Basic Realm="example" zurückgegeben werden, wenn eine Serverauthentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-113">For example, the header "WWW-Authenticate: Basic Realm="example"" might be returned when server authentication is required.</span></span> <span data-ttu-id="fcfe5-114">Dieser Header gibt an, dass Benutzeranmeldeinformationen für die Domäne "example" angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-114">This header specifies that user credentials must be supplied for the "example" domain.</span></span>

<span data-ttu-id="fcfe5-115">Eine HTTP-Anwendung kann ein Autorisierungsheaderfeld mit einer Anforderung enthalten, die sie an den Server sendet.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-115">An HTTP application can include an authorization header field with a request it sends to the server.</span></span> <span data-ttu-id="fcfe5-116">Der Autorisierungsheader enthält das Authentifizierungsschema und die entsprechende Antwort, die für dieses Schema erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-116">The authorization header contains the authentication scheme and the appropriate response required by that scheme.</span></span> <span data-ttu-id="fcfe5-117">Beispielsweise würde der Header "Authorization: Basic \<username:password> " der Anforderung hinzugefügt und an den Server gesendet, wenn der Client den Antwortheader "WWW-Authenticate: Basic Realm="example" erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-117">For example, the header "Authorization: Basic \<username:password>" would be added to the request and sent to the server if the client received the response header "WWW-Authenticate: Basic Realm="example"".</span></span>

> [!Note]  
> <span data-ttu-id="fcfe5-118">Obwohl sie hier als Nur-Text angezeigt werden, sind der Benutzername und das Kennwort tatsächlich [*base64-codiert.*](glossary.md)</span><span class="sxs-lookup"><span data-stu-id="fcfe5-118">Although they are shown here as plain text, the username and password are actually [*base64 encoded*](glossary.md).</span></span>

 

<span data-ttu-id="fcfe5-119">Es gibt zwei allgemeine Arten von Authentifizierungsschemas:</span><span class="sxs-lookup"><span data-stu-id="fcfe5-119">There are two general types of authentication schemes:</span></span>

-   <span data-ttu-id="fcfe5-120">Standardauthentifizierungsschema, bei dem Benutzername und Kennwort in Klartext an den Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-120">Basic authentication scheme, in which the user name and password are sent in clear text to the server.</span></span>

    <span data-ttu-id="fcfe5-121">Das Standardauthentifizierungsschema basiert auf dem Modell, das sich ein Client mit einem Benutzernamen und Kennwort für jeden Bereich identifizieren muss.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-121">The Basic authentication scheme is based on the model that a client must identify itself with a user name and password for each realm.</span></span> <span data-ttu-id="fcfe5-122">Der Server unterstützt die Anforderung nur, wenn die Anforderung mit einem Autorisierungsheader gesendet wird, der einen gültigen Benutzernamen und ein gültiges Kennwort enthält.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-122">The server services the request only if the request is sent with an authorization header that includes a valid user name and password.</span></span>

-   <span data-ttu-id="fcfe5-123">Challenge-Response-Schemas, z. B. Kerberos, bei denen der Server den Client mit [*Authentifizierungsdaten herausfordert.*](glossary.md)</span><span class="sxs-lookup"><span data-stu-id="fcfe5-123">Challenge-response schemes, such as Kerberos, in which the server challenges the client with [*authentication data*](glossary.md).</span></span> <span data-ttu-id="fcfe5-124">Der Client transformiert die Daten mit den Benutzeranmeldeinformationen und sendet die transformierten Daten zur Authentifizierung zurück an den Server.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-124">The client transforms the data with the user credentials and sends the transformed data back to the server for authentication.</span></span>

    <span data-ttu-id="fcfe5-125">Challenge-Response-Schemas ermöglichen eine sicherere Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-125">Challenge-response schemes enable a more secure authentication.</span></span> <span data-ttu-id="fcfe5-126">In einem Challenge-Response-Schema werden Benutzername und Kennwort nie über das Netzwerk übertragen.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-126">In a challenge-response scheme, the username and password are never transmitted over the network.</span></span> <span data-ttu-id="fcfe5-127">Nachdem der Client ein Challenge-Response-Schema ausgewählt hat, gibt der Server einen entsprechenden Statuscode mit einer Herausforderung zurück, die die Authentifizierungsdaten [*für*](glossary.md) dieses Schema enthält.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-127">After the client selects a challenge-response scheme, the server returns an appropriate status code with a challenge that contains the [*authentication data*](glossary.md) for that scheme.</span></span> <span data-ttu-id="fcfe5-128">Der Client gibt dann die Anforderung erneut mit der richtigen Antwort zurück, um den angeforderten Dienst zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-128">The client then resends the request with the proper response to obtain the requested service.</span></span> <span data-ttu-id="fcfe5-129">Für Challenge-Response-Schemas kann es mehrere Austauschzeiten geben.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-129">Challenge-response schemes can take multiple exchanges to complete.</span></span>

<span data-ttu-id="fcfe5-130">Die folgende Tabelle enthält die von WinHTTP unterstützten Authentifizierungsschemas, den Authentifizierungstyp und eine Beschreibung des Schemas.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-130">The following table contains the authentication schemes that are supported by WinHTTP, the authentication type, and a description of the scheme.</span></span>



| <span data-ttu-id="fcfe5-131">Schema</span><span class="sxs-lookup"><span data-stu-id="fcfe5-131">Scheme</span></span>            | <span data-ttu-id="fcfe5-132">type</span><span class="sxs-lookup"><span data-stu-id="fcfe5-132">Type</span></span>               | <span data-ttu-id="fcfe5-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fcfe5-133">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcfe5-134">Basic (Klartext)</span><span class="sxs-lookup"><span data-stu-id="fcfe5-134">Basic (plaintext)</span></span> | <span data-ttu-id="fcfe5-135">Basic</span><span class="sxs-lookup"><span data-stu-id="fcfe5-135">Basic</span></span>              | <span data-ttu-id="fcfe5-136">Verwendet eine [*Base64-codierte Zeichenfolge,*](glossary.md) die den Benutzernamen und das Kennwort enthält.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-136">Uses a [*base64 encoded*](glossary.md) string that contains the user name and password.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="fcfe5-137">Digest</span><span class="sxs-lookup"><span data-stu-id="fcfe5-137">Digest</span></span>            | <span data-ttu-id="fcfe5-138">Challenge-Response</span><span class="sxs-lookup"><span data-stu-id="fcfe5-138">Challenge-response</span></span> | <span data-ttu-id="fcfe5-139">Herausforderungen bei der Verwendung eines Nonce-Werts (einer vom Server angegebenen Datenzeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="fcfe5-139">Challenges using a nonce (a server-specified data string) value.</span></span> <span data-ttu-id="fcfe5-140">Eine gültige Antwort enthält eine Prüfsumme des Benutzernamens, des Kennworts, des angegebenen Nonce-Werts, des [*HTTP-Verbs*](glossary.md)und des angeforderten Uniform Resource Identifier (URI).</span><span class="sxs-lookup"><span data-stu-id="fcfe5-140">A valid response contains a checksum of the user name, the password, the given nonce value, the [*HTTP verb*](glossary.md), and the requested Uniform Resource Identifier (URI).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="fcfe5-141">NTLM</span><span class="sxs-lookup"><span data-stu-id="fcfe5-141">NTLM</span></span>              | <span data-ttu-id="fcfe5-142">Challenge-Response</span><span class="sxs-lookup"><span data-stu-id="fcfe5-142">Challenge-response</span></span> | <span data-ttu-id="fcfe5-143">Erfordert, [*dass die Authentifizierungsdaten*](glossary.md) mit den Benutzeranmeldeinformationen transformiert werden, um die Identität nachzuweisen.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-143">Requires the [*authentication data*](glossary.md) to be transformed with the user credentials to prove identity.</span></span> <span data-ttu-id="fcfe5-144">Damit die NTLM-Authentifizierung ordnungsgemäß funktioniert, müssen mehrere Austausche für dieselbe Verbindung stattfinden.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-144">For NTLM authentication to function correctly, several exchanges must take place on the same connection.</span></span> <span data-ttu-id="fcfe5-145">Daher kann die NTLM-Authentifizierung nicht verwendet werden, wenn ein intervening-Proxy keep-alive-Verbindungen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-145">Therefore, NTLM authentication cannot be used if an intervening proxy does not support keep-alive connections.</span></span> <span data-ttu-id="fcfe5-146">Die NTLM-Authentifizierung schlägt auch fehl, wenn [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit dem [**WINHTTP \_ DISABLE KEEP \_ \_ ALIVE-Flag**](option-flags.md) verwendet wird, das die Keep-Alive-Semantik deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-146">NTLM authentication also fails if [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) is used with the [**WINHTTP\_DISABLE\_KEEP\_ALIVE**](option-flags.md) flag that disables keep-alive semantics.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="fcfe5-147">Passport</span><span class="sxs-lookup"><span data-stu-id="fcfe5-147">Passport</span></span>          | <span data-ttu-id="fcfe5-148">Abfrageantwort</span><span class="sxs-lookup"><span data-stu-id="fcfe5-148">Challenge-response</span></span> | <span data-ttu-id="fcfe5-149">Verwendet [Microsoft Passport 1.4.](passport-authentication-in-winhttp.md)</span><span class="sxs-lookup"><span data-stu-id="fcfe5-149">Uses [Microsoft Passport 1.4](passport-authentication-in-winhttp.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="fcfe5-150">Aushandeln</span><span class="sxs-lookup"><span data-stu-id="fcfe5-150">Negotiate</span></span>         | <span data-ttu-id="fcfe5-151">Abfrageantwort</span><span class="sxs-lookup"><span data-stu-id="fcfe5-151">Challenge-response</span></span> | <span data-ttu-id="fcfe5-152">Wenn sowohl der Server als auch der Client Windows 2000 oder höher verwenden, wird die Kerberos-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-152">If both the server and client are using Windows 2000 or later, Kerberos authentication is used.</span></span> <span data-ttu-id="fcfe5-153">Andernfalls wird die NTLM-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-153">Otherwise NTLM authentication is used.</span></span> <span data-ttu-id="fcfe5-154">Kerberos ist unter Windows 2000 und höher verfügbar und gilt als sicherer als die NTLM-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-154">Kerberos is available in Windows 2000 and later operating systems and is considered to be more secure than NTLM authentication.</span></span> <span data-ttu-id="fcfe5-155">Damit die Negotiate-Authentifizierung ordnungsgemäß funktioniert, müssen mehrere Austauschvorgänge für dieselbe Verbindung erfolgen.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-155">For Negotiate authentication to function correctly, several exchanges must take place on the same connection.</span></span> <span data-ttu-id="fcfe5-156">Daher kann die Negotiate-Authentifizierung nicht verwendet werden, wenn ein dazwischen liegender Proxy keine Keep-Alive-Verbindungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-156">Therefore, Negotiate authentication cannot be used if an intervening proxy does not support keep-alive connections.</span></span> <span data-ttu-id="fcfe5-157">Die Negotiate-Authentifizierung schlägt auch fehl, wenn [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit dem [**WINHTTP \_ DISABLE KEEP \_ \_ ALIVE-Flag**](option-flags.md) verwendet wird, das die Keep-Alive-Semantik deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-157">Negotiate authentication also fails if [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) is used with the [**WINHTTP\_DISABLE\_KEEP\_ALIVE**](option-flags.md) flag that disables keep-alive semantics.</span></span> <span data-ttu-id="fcfe5-158">Das Negotiate-Authentifizierungsschema wird manchmal als Integrierte Windows-Authentifizierung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-158">The Negotiate authentication scheme is sometimes called Integrated Windows authentication.</span></span> |



 

## <a name="authentication-in-winhttp-applications"></a><span data-ttu-id="fcfe5-159">Authentifizierung in WinHTTP-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="fcfe5-159">Authentication in WinHTTP Applications</span></span>

<span data-ttu-id="fcfe5-160">Die WinHTTP-Api (Application Programming Interface, Anwendungsprogrammierschnittstelle) stellt zwei Funktionen für den Zugriff auf Internetressourcen in Situationen bereit, in denen eine Authentifizierung erforderlich ist: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) und [**WinHttpQueryAuthSchemes.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)</span><span class="sxs-lookup"><span data-stu-id="fcfe5-160">The WinHTTP application programming interface (API) provides two functions used to access Internet resources in situations where authentication is required: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) and [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).</span></span>

<span data-ttu-id="fcfe5-161">Wenn eine Antwort mit dem Statuscode 401 oder 407 empfangen wird, kann [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) verwendet werden, um die Authentifizierungsheader zu analysieren, um die unterstützten Authentifizierungsschemas und das Authentifizierungsziel zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-161">When a response is received with a 401 or 407 status code, [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) can be used to parse the authentication headers to determine the supported authentication schemes and the authentication target.</span></span> <span data-ttu-id="fcfe5-162">Das Authentifizierungsziel ist der Server oder Proxy, der die Authentifizierung anfordert.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-162">The authentication target is the server or proxy that requests authentication.</span></span> <span data-ttu-id="fcfe5-163">**WinHttpQueryAuthSchemes** bestimmt auch das erste Authentifizierungsschema anhand der verfügbaren Schemas basierend auf den vom Server vorgeschlagenen Authentifizierungsschemaeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-163">**WinHttpQueryAuthSchemes** also determines the first authentication scheme, from the available schemes, based on the authentication scheme preferences suggested by the server.</span></span> <span data-ttu-id="fcfe5-164">Diese Methode zum Auswählen eines Authentifizierungsschemas ist das von [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)vorgeschlagene Verhalten.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-164">This method for choosing an authentication scheme is the behavior suggested by [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

<span data-ttu-id="fcfe5-165">[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) ermöglicht einer Anwendung, das Authentifizierungsschema anzugeben, das zusammen mit einem gültigen Benutzernamen und Kennwort für die Verwendung auf dem Zielserver oder Proxy verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-165">[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) enables an application to specify the authentication scheme that is used along with a valid username and password for use on the target server or proxy.</span></span> <span data-ttu-id="fcfe5-166">Nach dem Festlegen der Anmeldeinformationen und dem erneuten Senden der Anforderung werden die erforderlichen Header generiert und der Anforderung automatisch hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-166">After setting the credentials and resending the request, the necessary headers are generated and added to the request automatically.</span></span> <span data-ttu-id="fcfe5-167">Da einige Authentifizierungsschemas mehrere Transaktionen erfordern, kann [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) den Fehler ERROR \_ WINHTTP \_ RESEND \_ REQUEST zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-167">Because some authentication schemes require multiple transactions [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) could return the error, ERROR\_WINHTTP\_RESEND\_REQUEST.</span></span> <span data-ttu-id="fcfe5-168">Wenn dieser Fehler auftritt, sollte die Anwendung die Anforderung so lange erneut senden, bis eine Antwort empfangen wird, die keinen Statuscode 401 oder 407 enthält.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-168">When this error is encountered, the application should continue to resend the request until a response is received that does not contain a 401 or 407 status code.</span></span> <span data-ttu-id="fcfe5-169">Der Statuscode 200 gibt an, dass die Ressource verfügbar ist und die Anforderung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-169">A 200 status code indicates that the resource is available and the request is successful.</span></span> <span data-ttu-id="fcfe5-170">Weitere Statuscodes, die zurückgegeben werden können, finden Sie unter [**HTTP-Statuscodes.**](http-status-codes.md)</span><span class="sxs-lookup"><span data-stu-id="fcfe5-170">See [**HTTP Status Codes**](http-status-codes.md) for additional status codes that can be returned.</span></span>

<span data-ttu-id="fcfe5-171">Wenn ein akzeptables Authentifizierungsschema und Anmeldeinformationen bekannt sind, bevor eine Anforderung an den Server gesendet wird, kann eine Anwendung [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) aufrufen, bevor [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-171">If an acceptable authentication scheme and credentials are known before a request is sent to the server, an application can call [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) before calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="fcfe5-172">In diesem Fall versucht WinHTTP die Vorauthentifizierung mit dem Server, indem anmeldeinformationen oder [*Authentifizierungsdaten*](glossary.md) in der ersten Anforderung an den Server angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-172">In this case, WinHTTP attempts pre-authentication with the server by providing credentials or [*authentication data*](glossary.md) in the initial request to the server.</span></span> <span data-ttu-id="fcfe5-173">Die Vorauthentifizierung kann die Anzahl der Austauschvorgänge im Authentifizierungsprozess verringern und somit die Anwendungsleistung verbessern.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-173">Pre-authentication can decrease the number of exchanges in the authentication process and therefore improve application performance.</span></span>

<span data-ttu-id="fcfe5-174">Die Vorauthentifizierung kann mit den folgenden Authentifizierungsschemas verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="fcfe5-174">Preauthentication can be used with the following authentication schemes:</span></span>

-   <span data-ttu-id="fcfe5-175">Basic : immer möglich.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-175">Basic - always possible.</span></span>
-   <span data-ttu-id="fcfe5-176">Aushandeln der Auflösung in Kerberos – sehr wahrscheinlich möglich; Die einzige Ausnahme ist, wenn die Zeitabweichungen zwischen dem Client und dem Domänencontroller ausgeschaltet sind.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-176">Negotiate resolving into Kerberos - very likely possible; the only exception is when the time-skews are off between the client and the domain controller.</span></span>
-   <span data-ttu-id="fcfe5-177">(Auflösen in NTLM aushandeln) – nie möglich.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-177">(Negotiate resolving into NTLM) - never possible.</span></span>
-   <span data-ttu-id="fcfe5-178">NTLM: nur in Windows Server 2008 R2 möglich.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-178">NTLM - possible in Windows Server 2008 R2 only.</span></span>
-   <span data-ttu-id="fcfe5-179">Digest: nie möglich.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-179">Digest - never possible.</span></span>
-   <span data-ttu-id="fcfe5-180">Passport – nie möglich; Nach der ersten Abfrageantwort verwendet WinHTTP Cookies für die Vorabauthentifizierung bei Passport.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-180">Passport - never possible; after the initial challenge-response, WinHTTP uses cookies to pre-authenticate to Passport.</span></span>

<span data-ttu-id="fcfe5-181">Eine typische WinHTTP-Anwendung schließt die folgenden Schritte ab, um die Authentifizierung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-181">A typical WinHTTP application completes the following steps in order to handle authentication.</span></span>

-   <span data-ttu-id="fcfe5-182">Fordern Sie eine Ressource mit [**WinHttpOpenRequest und**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) [**WinHttpSendRequest an.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="fcfe5-182">Request a resource with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) and [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>
-   <span data-ttu-id="fcfe5-183">Überprüfen Sie die Antwortheader mit [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="fcfe5-183">Check the response headers with [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>
-   <span data-ttu-id="fcfe5-184">Wenn ein Statuscode 401 oder 407 zurückgegeben wird, der angibt, dass eine Authentifizierung erforderlich ist, rufen Sie [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) auf, um ein akzeptables Schema zu finden.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-184">If a 401 or 407 status code is returned indicating that authentication is required, call [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) to find an acceptable scheme.</span></span>
-   <span data-ttu-id="fcfe5-185">Legen Sie das Authentifizierungsschema, den Benutzernamen und das Kennwort mit [**WinHttpSetCredentials fest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)</span><span class="sxs-lookup"><span data-stu-id="fcfe5-185">Set the authentication scheme, username, and password with [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).</span></span>
-   <span data-ttu-id="fcfe5-186">Senden Sie die Anforderung erneut mit dem gleichen Anforderungshand handle, indem [**Sie WinHttpSendRequest aufrufen.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="fcfe5-186">Resend the request with the same request handle by calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

<span data-ttu-id="fcfe5-187">Die von [**WinHttpSetCredentials festgelegten**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) Anmeldeinformationen werden nur für eine Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-187">The credentials set by [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) are only used for one request.</span></span> <span data-ttu-id="fcfe5-188">WinHTTP speichert die Anmeldeinformationen nicht zwischen, die in anderen Anforderungen verwendet werden sollen. Das bedeutet, dass Anwendungen geschrieben werden müssen, die auf mehrere Anforderungen reagieren können.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-188">WinHTTP does not cache the credentials to use in other requests, which means that applications must be written that can respond to multiple requests.</span></span> <span data-ttu-id="fcfe5-189">Wenn eine authentifizierte Verbindung erneut verwendet wird, werden andere Anforderungen möglicherweise nicht in Frage gestellt, aber Ihr Code sollte jederzeit auf eine Anforderung reagieren können.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-189">If an authenticated connection is re-used, other requests may not be challenged, but your code should be able to respond to a request at any time.</span></span>

### <a name="example-retrieving-a-document"></a><span data-ttu-id="fcfe5-190">Beispiel: Abrufen eines Dokuments</span><span class="sxs-lookup"><span data-stu-id="fcfe5-190">Example: Retrieving a Document</span></span>

<span data-ttu-id="fcfe5-191">Der folgende Beispielcode versucht, ein angegebenes Dokument von einem HTTP-Server abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-191">The following sample code attempts to retrieve a specified document from an HTTP server.</span></span> <span data-ttu-id="fcfe5-192">Der Statuscode wird aus der Antwort abgerufen, um zu bestimmen, ob eine Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-192">The status code is retrieved from the response to determine if authentication is required.</span></span> <span data-ttu-id="fcfe5-193">Wenn der Statuscode 200 gefunden wird, ist das Dokument verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-193">If a 200 status code is found, the document is available.</span></span> <span data-ttu-id="fcfe5-194">Wenn der Statuscode 401 oder 407 gefunden wird, ist eine Authentifizierung erforderlich, bevor das Dokument abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-194">If a status code of 401 or 407 is found, authentication is required before the document can be retrieved.</span></span> <span data-ttu-id="fcfe5-195">Für jeden anderen Statuscode wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-195">For any other status code, an error message is displayed.</span></span> <span data-ttu-id="fcfe5-196">Eine [**Liste der möglichen Statuscodes**](http-status-codes.md) finden Sie unter HTTP-Statuscodes.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-196">See [**HTTP Status Codes**](http-status-codes.md) for a list of possible status codes.</span></span>


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



## <a name="automatic-logon-policy"></a><span data-ttu-id="fcfe5-197">Richtlinie für die automatische Anmeldung</span><span class="sxs-lookup"><span data-stu-id="fcfe5-197">Automatic Logon Policy</span></span>

<span data-ttu-id="fcfe5-198">Die Richtlinie für die automatische Anmeldung bestimmt, wann winHTTP die Standardanmeldeinformationen in einer Anforderung enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-198">The automatic logon (auto-logon) policy determines when it is acceptable for WinHTTP to include the default credentials in a request.</span></span> <span data-ttu-id="fcfe5-199">Die Standardanmeldeinformationen sind entweder das aktuelle Threadtoken oder das Sitzungstoken, je nachdem, ob WinHTTP im synchronen oder asynchronen Modus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-199">The default credentials are either the current thread token or the session token depending on whether WinHTTP is used in synchronous or asynchronous mode.</span></span> <span data-ttu-id="fcfe5-200">Das Threadtoken wird im synchronen Modus und das Sitzungstoken im asynchronen Modus verwendet.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-200">The thread token is used in synchronous mode, and the session token is used in asynchronous mode.</span></span> <span data-ttu-id="fcfe5-201">Diese Standardanmeldeinformationen sind häufig der Benutzername und das Kennwort, die für die Anmeldung bei Microsoft Windows verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-201">These default credentials are often the username and password used to log on to Microsoft Windows.</span></span>

<span data-ttu-id="fcfe5-202">Die Richtlinie für die automatische Anmeldung wurde implementiert, um zu verhindern, dass diese Anmeldeinformationen gelegentlich für die Authentifizierung bei einem nicht vertrauenswürdigen Server verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-202">The auto-logon policy was implemented to prevent these credentials from being casually used to authenticate against an untrusted server.</span></span> <span data-ttu-id="fcfe5-203">Standardmäßig ist die Sicherheitsstufe auf WINHTTP \_ AUTOLOGON \_ SECURITY LEVEL MEDIUM \_ \_ festgelegt, wodurch die Standardanmeldeinformationen nur für Intranetanforderungen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-203">By default, the security level is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM, which allows the default credentials to be used only for Intranet requests.</span></span> <span data-ttu-id="fcfe5-204">Die Richtlinie für die automatische Anmeldung gilt nur für die Authentifizierungsschemas NTLM und Negotiate.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-204">The auto-logon policy only applies to the NTLM and Negotiate authentication schemes.</span></span> <span data-ttu-id="fcfe5-205">Anmeldeinformationen werden nie automatisch mit anderen Schemas übertragen.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-205">Credentials are never automatically transmitted with other schemes.</span></span>

<span data-ttu-id="fcfe5-206">Die Richtlinie für die automatische Anmeldung kann mithilfe der [**WinHttpSetOption-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit dem [**WINHTTP \_ OPTION \_ AUTOLOGON \_ POLICY-Flag**](option-flags.md) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-206">The auto-logon policy can be set using the [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) function with the [**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**](option-flags.md) flag.</span></span> <span data-ttu-id="fcfe5-207">Dieses Flag gilt nur für das Anforderungshandle.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-207">This flag applies only to the request handle.</span></span> <span data-ttu-id="fcfe5-208">Wenn die Richtlinie auf WINHTTP \_ AUTOLOGON SECURITY LEVEL LOW festgelegt \_ \_ \_ ist, können Standardanmeldeinformationen an alle Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-208">When the policy is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW, default credentials can be sent to all servers.</span></span> <span data-ttu-id="fcfe5-209">Wenn die Richtlinie auf WINHTTP \_ AUTOLOGON SECURITY LEVEL HIGH festgelegt \_ \_ \_ ist, können keine Standardanmeldeinformationen für die Authentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-209">When the policy is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH, default credentials cannot be used for authentication.</span></span> <span data-ttu-id="fcfe5-210">Es wird dringend empfohlen, die automatische Anmeldung auf der Ebene MEDIUM zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-210">It is strongly recommended that you use the auto-logon at the MEDIUM level.</span></span>

## <a name="stored-user-names-and-passwords"></a><span data-ttu-id="fcfe5-211">Gespeicherte Benutzernamen und Kennwörter</span><span class="sxs-lookup"><span data-stu-id="fcfe5-211">Stored User Names and Passwords</span></span>

<span data-ttu-id="fcfe5-212">In Windows XP wurde das Konzept der gespeicherten Benutzernamen und Kennwörter eingeführt.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-212">Windows XP introduced the concept of Stored User Names and Passwords.</span></span> <span data-ttu-id="fcfe5-213">Wenn die Passport-Anmeldeinformationen eines Benutzers über den **Passport-Registrierungs-Assistenten** oder das **Standarddialogfeld für Anmeldeinformationen** gespeichert werden, werden sie in den gespeicherten Benutzernamen und Kennwörtern gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-213">If a user's Passport credentials are saved through the **Passport Registration Wizard** or the standard **Credential Dialog**, it is saved in the Stored User Names and Passwords.</span></span> <span data-ttu-id="fcfe5-214">Bei Verwendung von WinHTTP unter Windows XP oder höher verwendet WinHTTP automatisch die Anmeldeinformationen in den gespeicherten Benutzernamen und Kennwörtern, wenn die Anmeldeinformationen nicht explizit festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-214">When using WinHTTP on Windows XP or later, WinHTTP automatically uses the credentials in the Stored User Names and Passwords if credentials are not explicitly set.</span></span> <span data-ttu-id="fcfe5-215">Dies ähnelt der Unterstützung von Standardanmeldeinformationen für NTLM/Kerberos.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-215">This is similar to the support of default logon credentials for NTLM/Kerberos.</span></span> <span data-ttu-id="fcfe5-216">Die Verwendung von Passport-Standardanmeldeinformationen unterliegt jedoch nicht den Einstellungen für automatische Anmelderichtlinien.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-216">However, use of default Passport credentials is not subject to the automatic logon policy settings.</span></span>

 

 



