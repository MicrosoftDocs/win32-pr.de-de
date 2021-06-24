---
description: In diesem Thema werden die Funktionen identifiziert, die WinHTTP bereitstellt.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: WinHTTP-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5f9db8fcde5589a86556111bec6df3b2b18c76
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587752"
---
# <a name="winhttp-functions"></a><span data-ttu-id="af235-103">WinHTTP-Funktionen</span><span class="sxs-lookup"><span data-stu-id="af235-103">WinHTTP Functions</span></span>

<span data-ttu-id="af235-104">WinHTTP stellt die folgenden Funktionen bereit:</span><span class="sxs-lookup"><span data-stu-id="af235-104">WinHTTP provides the following functions:</span></span>

<dl> <dt>

[<span data-ttu-id="af235-105">**WinHttpAddRequestHeaders**</span><span class="sxs-lookup"><span data-stu-id="af235-105">**WinHttpAddRequestHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

<span data-ttu-id="af235-106">Fügt dem HTTP-Anforderungshandle mindestens einen HTTP-Anforderungsheader hinzu.</span><span class="sxs-lookup"><span data-stu-id="af235-106">Adds one or more HTTP request headers to the HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-107">**WinHttpCheckPlatform**</span><span class="sxs-lookup"><span data-stu-id="af235-107">**WinHttpCheckPlatform**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

<span data-ttu-id="af235-108">Bestimmt, ob die aktuelle Plattform von WinHTTP unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="af235-108">Determines whether the current platform is supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-109">**WinHttpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="af235-109">**WinHttpCloseHandle**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

<span data-ttu-id="af235-110">Schließt ein einzelnes [HINTERNET-Handle.](hinternet-handles-in-winhttp.md)</span><span class="sxs-lookup"><span data-stu-id="af235-110">Closes a single [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-111">**WinHttpConnect**</span><span class="sxs-lookup"><span data-stu-id="af235-111">**WinHttpConnect**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

<span data-ttu-id="af235-112">Gibt den ursprünglichen Zielserver einer HTTP-Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="af235-112">Specifies the initial target server of an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-113">**WinHttpCrackUrl**</span><span class="sxs-lookup"><span data-stu-id="af235-113">**WinHttpCrackUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

<span data-ttu-id="af235-114">Trennt eine URL in seine Komponenten, z. B. Hostname und Pfad.</span><span class="sxs-lookup"><span data-stu-id="af235-114">Separates a URL into its component parts, for example, host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-115">**WinHttpCreateProxyResolver**</span><span class="sxs-lookup"><span data-stu-id="af235-115">**WinHttpCreateProxyResolver**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

<span data-ttu-id="af235-116">Erstellt ein Handle für die Verwendung durch [**WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)</span><span class="sxs-lookup"><span data-stu-id="af235-116">Creates a handle for use by [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="af235-117">**WinHttpCreateUrl**</span><span class="sxs-lookup"><span data-stu-id="af235-117">**WinHttpCreateUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

<span data-ttu-id="af235-118">Erstellt eine URL aus Komponententeilen, z. B. dem Hostnamen und dem Pfad.</span><span class="sxs-lookup"><span data-stu-id="af235-118">Creates a URL from component parts, for example, the host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-119">**WinHttpDetectAutoProxyConfigUrl**</span><span class="sxs-lookup"><span data-stu-id="af235-119">**WinHttpDetectAutoProxyConfigUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

<span data-ttu-id="af235-120">Sucht die URL für die PAC-Datei (Proxy Auto-Configuration).</span><span class="sxs-lookup"><span data-stu-id="af235-120">Finds the URL for the Proxy Auto-Configuration (PAC) file.</span></span> <span data-ttu-id="af235-121">Diese Funktion meldet die URL der PAC-Datei, lädt die Datei jedoch nicht herunter.</span><span class="sxs-lookup"><span data-stu-id="af235-121">This function reports the URL of the PAC file, but it does not download the file.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-122">**WinHttpFreeProxyResult**</span><span class="sxs-lookup"><span data-stu-id="af235-122">**WinHttpFreeProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

<span data-ttu-id="af235-123">Gibt die Daten frei, die aus einem vorherigen Aufruf von [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="af235-123">Frees the data retrieved from a previous call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="af235-124">**WinHttpFreeQueryConnectionGroupResult**</span><span class="sxs-lookup"><span data-stu-id="af235-124">**WinHttpFreeQueryConnectionGroupResult**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpfreequeryconnectiongroupresult)
</dt> <dd>

<span data-ttu-id="af235-125">Gibt den durch einen vorherigen Aufruf von [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)belegten Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="af235-125">Frees the memory allocated by a previous call to [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup).</span></span>

</dd> <dt>

[<span data-ttu-id="af235-126">**WinHttpGetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="af235-126">**WinHttpGetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="af235-127">Ruft die WinHTTP-Standardproxykonfiguration aus der Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="af235-127">Retrieves the default WinHTTP proxy configuration from the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-128">**WinHTTPGetIEProxyConfigForCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="af235-128">**WinHTTPGetIEProxyConfigForCurrentUser**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

<span data-ttu-id="af235-129">Ruft die Proxykonfiguration für Internet Explorer (IE) für den aktuellen Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="af235-129">Obtains the Internet Explorer (IE) proxy configuration for the current user.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-130">**WinHttpGetProxyForUrl**</span><span class="sxs-lookup"><span data-stu-id="af235-130">**WinHttpGetProxyForUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

<span data-ttu-id="af235-131">Ruft die Proxyinformationen für die angegebene URL ab.</span><span class="sxs-lookup"><span data-stu-id="af235-131">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-132">**WinHttpGetProxyForUrlEx**</span><span class="sxs-lookup"><span data-stu-id="af235-132">**WinHttpGetProxyForUrlEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

<span data-ttu-id="af235-133">Ruft die Proxyinformationen für die angegebene URL ab.</span><span class="sxs-lookup"><span data-stu-id="af235-133">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-134">**WinHttpGetProxyResult**</span><span class="sxs-lookup"><span data-stu-id="af235-134">**WinHttpGetProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

<span data-ttu-id="af235-135">Ruft die Ergebnisse eines Aufrufs von [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)ab.</span><span class="sxs-lookup"><span data-stu-id="af235-135">Retrieves the results of a call to [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="af235-136">**WinHttpOpen**</span><span class="sxs-lookup"><span data-stu-id="af235-136">**WinHttpOpen**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

<span data-ttu-id="af235-137">Initialisiert die Verwendung der WinHTTP-Funktionen durch eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="af235-137">Initializes an application's use of the WinHTTP functions.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-138">**WinHttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="af235-138">**WinHttpOpenRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

<span data-ttu-id="af235-139">Erstellt ein HTTP-Anforderungshandle.</span><span class="sxs-lookup"><span data-stu-id="af235-139">Creates an HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-140">**WinHttpQueryAuthSchemes**</span><span class="sxs-lookup"><span data-stu-id="af235-140">**WinHttpQueryAuthSchemes**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

<span data-ttu-id="af235-141">Gibt die Autorisierungsschemas zurück, die der Server unterstützt.</span><span class="sxs-lookup"><span data-stu-id="af235-141">Returns the authorization schemes that the server supports.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-142">**WinHttpQueryConnectionGroup**</span><span class="sxs-lookup"><span data-stu-id="af235-142">**WinHttpQueryConnectionGroup**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)
</dt> <dd>

<span data-ttu-id="af235-143">Ruft eine Beschreibung des aktuellen Status der WinHttp-Verbindungen ab.</span><span class="sxs-lookup"><span data-stu-id="af235-143">Retrieves a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-144">**WinHttpQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="af235-144">**WinHttpQueryDataAvailable**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

<span data-ttu-id="af235-145">Gibt die Anzahl der Datenbytes zurück, die sofort zum Lesen mit [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="af235-145">Returns the number of bytes of data that are available immediately to be read with [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span></span>

</dd> <dt>

[<span data-ttu-id="af235-146">**WinHttpQueryHeaders**</span><span class="sxs-lookup"><span data-stu-id="af235-146">**WinHttpQueryHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

<span data-ttu-id="af235-147">Ruft Headerinformationen ab, die einer HTTP-Anforderung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="af235-147">Retrieves header information associated with an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-148">**WinHttpQueryOption**</span><span class="sxs-lookup"><span data-stu-id="af235-148">**WinHttpQueryOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

<span data-ttu-id="af235-149">Fragt eine Internetoption für das angegebene Handle ab.</span><span class="sxs-lookup"><span data-stu-id="af235-149">Queries an Internet option on the specified handle.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-150">**WinHttpReadData**</span><span class="sxs-lookup"><span data-stu-id="af235-150">**WinHttpReadData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

<span data-ttu-id="af235-151">Liest Daten aus einem Handle, das von der [**WinHttpOpenRequest-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="af235-151">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-152">**WinHttpReceiveResponse**</span><span class="sxs-lookup"><span data-stu-id="af235-152">**WinHttpReceiveResponse**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

<span data-ttu-id="af235-153">Beendet eine HTTP-Anforderung, die von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="af235-153">Ends an HTTP request that is initiated by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="af235-154">**WinHttpResetAutoProxy**</span><span class="sxs-lookup"><span data-stu-id="af235-154">**WinHttpResetAutoProxy**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

<span data-ttu-id="af235-155">Setzt den automatischen Proxy zurück.</span><span class="sxs-lookup"><span data-stu-id="af235-155">Resets the auto-proxy.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-156">**WinHttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="af235-156">**WinHttpSendRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

<span data-ttu-id="af235-157">Sendet die angegebene Anforderung an den HTTP-Server.</span><span class="sxs-lookup"><span data-stu-id="af235-157">Sends the specified request to the HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-158">**WinHttpSetCredentials**</span><span class="sxs-lookup"><span data-stu-id="af235-158">**WinHttpSetCredentials**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

<span data-ttu-id="af235-159">Übergibt die erforderlichen Autorisierungsanmeldeinformationen an den Server.</span><span class="sxs-lookup"><span data-stu-id="af235-159">Passes the required authorization credentials to the server.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-160">**WinHttpSetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="af235-160">**WinHttpSetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="af235-161">Legt die WinHTTP-Standardproxykonfiguration in der Registrierung fest.</span><span class="sxs-lookup"><span data-stu-id="af235-161">Sets the default WinHTTP proxy configuration in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-162">**WinHttpSetOption**</span><span class="sxs-lookup"><span data-stu-id="af235-162">**WinHttpSetOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

<span data-ttu-id="af235-163">Legt eine Internetoption fest.</span><span class="sxs-lookup"><span data-stu-id="af235-163">Sets an Internet option.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-164">**WinHttpSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="af235-164">**WinHttpSetStatusCallback**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

<span data-ttu-id="af235-165">Richtet eine Rückruffunktion ein, die WinHTTP aufrufen kann, wenn der Fortschritt während eines Vorgangs erfolgt.</span><span class="sxs-lookup"><span data-stu-id="af235-165">Sets up a callback function that WinHTTP can call as progress is made during an operation.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-166">**WinHttpSetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="af235-166">**WinHttpSetTimeouts**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

<span data-ttu-id="af235-167">Legt die verschiedenen Time outs fest, die an HTTP-Transaktionen beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="af235-167">Sets the various time-outs that are involved with HTTP transactions.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-168">**WinHttpTimeFromSystemTime**</span><span class="sxs-lookup"><span data-stu-id="af235-168">**WinHttpTimeFromSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

<span data-ttu-id="af235-169">Formatiert ein Datum und eine Uhrzeit gemäß der HTTP-Version 1.0-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="af235-169">Formats a date and time according to the HTTP version 1.0 specification.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-170">**WinHttpTimeToSystemTime**</span><span class="sxs-lookup"><span data-stu-id="af235-170">**WinHttpTimeToSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

<span data-ttu-id="af235-171">Verwendet eine HTTP-Zeit-/Datumszeichenfolge und konvertiert sie in eine [**SYSTEMTIME-Struktur.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)</span><span class="sxs-lookup"><span data-stu-id="af235-171">Takes an HTTP time/date string and converts it to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-172">**WinHttpWriteData**</span><span class="sxs-lookup"><span data-stu-id="af235-172">**WinHttpWriteData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

<span data-ttu-id="af235-173">Schreibt Anforderungsdaten auf einen HTTP-Server.</span><span class="sxs-lookup"><span data-stu-id="af235-173">Writes request data to an HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-174">**WinHttpWebSocketClose**</span><span class="sxs-lookup"><span data-stu-id="af235-174">**WinHttpWebSocketClose**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

<span data-ttu-id="af235-175">Schließt eine WebSocket-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="af235-175">Closes a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-176">**WinHttpWebSocketCompleteUpgrade**</span><span class="sxs-lookup"><span data-stu-id="af235-176">**WinHttpWebSocketCompleteUpgrade**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

<span data-ttu-id="af235-177">Schließt einen Von [**WinHttpSendRequest gestarteten**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)WebSocket-Handshake ab.</span><span class="sxs-lookup"><span data-stu-id="af235-177">Completes a WebSocket handshake started by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="af235-178">**WinHttpWebSocketQueryCloseStatus**</span><span class="sxs-lookup"><span data-stu-id="af235-178">**WinHttpWebSocketQueryCloseStatus**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

<span data-ttu-id="af235-179">Ruft den von einem Server gesendeten Schließstatus ab.</span><span class="sxs-lookup"><span data-stu-id="af235-179">Gets the close status sent by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-180">**WinHttpWebSocketReceive**</span><span class="sxs-lookup"><span data-stu-id="af235-180">**WinHttpWebSocketReceive**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

<span data-ttu-id="af235-181">Empfängt Daten von einer WebSocket-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="af235-181">Receives data from a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-182">**WinHttpWebSocketSend**</span><span class="sxs-lookup"><span data-stu-id="af235-182">**WinHttpWebSocketSend**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

<span data-ttu-id="af235-183">Sendet Daten über eine WebSocket-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="af235-183">Sends data over a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="af235-184">**WinHttpWebSocketShutdown**</span><span class="sxs-lookup"><span data-stu-id="af235-184">**WinHttpWebSocketShutdown**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

<span data-ttu-id="af235-185">Sendet einen schließenden Frame an eine WebSocket-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="af235-185">Sends a close frame to a WebSocket connection.</span></span>

</dd> </dl>

 

 
