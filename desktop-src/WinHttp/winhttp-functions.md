---
description: In diesem Thema werden die Funktionen identifiziert, die WinHTTP bereitstellt.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: WinHTTP-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e45289230c1cc22a7f8799dfbbe1dafddccf38
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113174974"
---
# <a name="winhttp-functions"></a><span data-ttu-id="cc6bf-103">WinHTTP-Funktionen</span><span class="sxs-lookup"><span data-stu-id="cc6bf-103">WinHTTP Functions</span></span>

<span data-ttu-id="cc6bf-104">WinHTTP stellt die folgenden Funktionen bereit:</span><span class="sxs-lookup"><span data-stu-id="cc6bf-104">WinHTTP provides the following functions:</span></span>

<dl> <dt>

[<span data-ttu-id="cc6bf-105">**WinHttpAddRequestHeaders**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-105">**WinHttpAddRequestHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

<span data-ttu-id="cc6bf-106">Fügt dem HTTP-Anforderungshandle mindestens einen HTTP-Anforderungsheader hinzu.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-106">Adds one or more HTTP request headers to the HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-107">**WinHttpAddRequestHeadersEx**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-107">**WinHttpAddRequestHeadersEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheadersex)
</dt> <dd>

<span data-ttu-id="cc6bf-108">Fügt einem HTTP-Anforderungshandle mindestens einen HTTP-Anforderungsheader hinzu, sodass Sie separate Namens-/Wertzeichenfolgen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-108">Adds one or more HTTP request headers to an HTTP request handle, allowing you to use separate name/value strings.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-109">**WinHttpCheckPlatform**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-109">**WinHttpCheckPlatform**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

<span data-ttu-id="cc6bf-110">Bestimmt, ob die aktuelle Plattform von WinHTTP unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-110">Determines whether the current platform is supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-111">**WinHttpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-111">**WinHttpCloseHandle**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

<span data-ttu-id="cc6bf-112">Schließt ein einzelnes [HINTERNET-Handle.](hinternet-handles-in-winhttp.md)</span><span class="sxs-lookup"><span data-stu-id="cc6bf-112">Closes a single [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-113">**WinHttpConnect**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-113">**WinHttpConnect**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

<span data-ttu-id="cc6bf-114">Gibt den ursprünglichen Zielserver einer HTTP-Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-114">Specifies the initial target server of an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-115">**WinHttpCrackUrl**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-115">**WinHttpCrackUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

<span data-ttu-id="cc6bf-116">Trennt eine URL in ihre Komponenten, z. B. Hostname und Pfad.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-116">Separates a URL into its component parts, for example, host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-117">**WinHttpCreateProxyResolver**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-117">**WinHttpCreateProxyResolver**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

<span data-ttu-id="cc6bf-118">Erstellt ein Handle für die Verwendung durch [**WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)</span><span class="sxs-lookup"><span data-stu-id="cc6bf-118">Creates a handle for use by [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-119">**WinHttpCreateUrl**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-119">**WinHttpCreateUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

<span data-ttu-id="cc6bf-120">Erstellt eine URL aus Komponententeilen, z. B. dem Hostnamen und dem Pfad.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-120">Creates a URL from component parts, for example, the host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-121">**WinHttpDetectAutoProxyConfigUrl**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-121">**WinHttpDetectAutoProxyConfigUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

<span data-ttu-id="cc6bf-122">Sucht die URL für die PAC-Datei (Proxy Auto-Configuration).</span><span class="sxs-lookup"><span data-stu-id="cc6bf-122">Finds the URL for the Proxy Auto-Configuration (PAC) file.</span></span> <span data-ttu-id="cc6bf-123">Diese Funktion meldet die URL der PAC-Datei, lädt die Datei jedoch nicht herunter.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-123">This function reports the URL of the PAC file, but it does not download the file.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-124">**WinHttpFreeProxyResult**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-124">**WinHttpFreeProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

<span data-ttu-id="cc6bf-125">Gibt die Daten frei, die aus einem vorherigen Aufruf von [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-125">Frees the data retrieved from a previous call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-126">**WinHttpFreeQueryConnectionGroupResult**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-126">**WinHttpFreeQueryConnectionGroupResult**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpfreequeryconnectiongroupresult)
</dt> <dd>

<span data-ttu-id="cc6bf-127">Gibt den durch einen vorherigen Aufruf von [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)belegten Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-127">Frees the memory allocated by a previous call to [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup).</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-128">**WinHttpGetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-128">**WinHttpGetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="cc6bf-129">Ruft die WinHTTP-Standardproxykonfiguration aus der Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-129">Retrieves the default WinHTTP proxy configuration from the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-130">**WinHTTPGetIEProxyConfigForCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-130">**WinHTTPGetIEProxyConfigForCurrentUser**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

<span data-ttu-id="cc6bf-131">Ruft die Internet Explorer(IE)-Proxykonfiguration für den aktuellen Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-131">Obtains the Internet Explorer (IE) proxy configuration for the current user.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-132">**WinHttpGetProxyForUrl**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-132">**WinHttpGetProxyForUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

<span data-ttu-id="cc6bf-133">Ruft die Proxyinformationen für die angegebene URL ab.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-133">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-134">**WinHttpGetProxyForUrlEx**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-134">**WinHttpGetProxyForUrlEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

<span data-ttu-id="cc6bf-135">Ruft die Proxyinformationen für die angegebene URL ab.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-135">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-136">**WinHttpGetProxyResult**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-136">**WinHttpGetProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

<span data-ttu-id="cc6bf-137">Ruft die Ergebnisse eines Aufrufs von [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)ab.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-137">Retrieves the results of a call to [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-138">**WinHttpOpen**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-138">**WinHttpOpen**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

<span data-ttu-id="cc6bf-139">Initialisiert die Verwendung der WinHTTP-Funktionen durch eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-139">Initializes an application's use of the WinHTTP functions.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-140">**WinHttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-140">**WinHttpOpenRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

<span data-ttu-id="cc6bf-141">Erstellt ein HTTP-Anforderungshandle.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-141">Creates an HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-142">**WinHttpQueryAuthSchemes**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-142">**WinHttpQueryAuthSchemes**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

<span data-ttu-id="cc6bf-143">Gibt die Autorisierungsschemas zurück, die der Server unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-143">Returns the authorization schemes that the server supports.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-144">**WinHttpQueryConnectionGroup**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-144">**WinHttpQueryConnectionGroup**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)
</dt> <dd>

<span data-ttu-id="cc6bf-145">Ruft eine Beschreibung des aktuellen Status der WinHttp-Verbindungen ab.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-145">Retrieves a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-146">**WinHttpQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-146">**WinHttpQueryDataAvailable**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

<span data-ttu-id="cc6bf-147">Gibt die Anzahl der Datenbytes zurück, die sofort zum Lesen mit [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-147">Returns the number of bytes of data that are available immediately to be read with [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-148">**WinHttpQueryHeaders**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-148">**WinHttpQueryHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

<span data-ttu-id="cc6bf-149">Ruft Headerinformationen ab, die einer HTTP-Anforderung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-149">Retrieves header information associated with an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-150">**WinHttpQueryHeadersEx**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-150">**WinHttpQueryHeadersEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheadersex)
</dt> <dd>

<span data-ttu-id="cc6bf-151">Ruft Headerinformationen ab, die einer HTTP-Anforderung zugeordnet sind. bietet eine Möglichkeit, analysierte Headernamen und Wertzeichenfolgen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-151">Retrieves header information associated with an HTTP request; offers a way to retrieve parsed header name and value strings.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-152">**WinHttpQueryOption**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-152">**WinHttpQueryOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

<span data-ttu-id="cc6bf-153">Fragt eine Internetoption für das angegebene Handle ab.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-153">Queries an Internet option on the specified handle.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-154">**WinHttpReadData**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-154">**WinHttpReadData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

<span data-ttu-id="cc6bf-155">Liest Daten aus einem Handle, das von der [**WinHttpOpenRequest-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-155">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-156">**WinHttpReadDataEx**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-156">**WinHttpReadDataEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddataex)
</dt> <dd>

<span data-ttu-id="cc6bf-157">Liest Daten aus einem Handle, das von der [**WinHttpOpenRequest-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-157">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-158">**WinHttpReceiveResponse**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-158">**WinHttpReceiveResponse**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

<span data-ttu-id="cc6bf-159">Beendet eine HTTP-Anforderung, die von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-159">Ends an HTTP request that is initiated by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-160">**WinHttpResetAutoProxy**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-160">**WinHttpResetAutoProxy**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

<span data-ttu-id="cc6bf-161">Setzt den automatischen Proxy zurück.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-161">Resets the auto-proxy.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-162">**WinHttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-162">**WinHttpSendRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

<span data-ttu-id="cc6bf-163">Sendet die angegebene Anforderung an den HTTP-Server.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-163">Sends the specified request to the HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-164">**WinHttpSetCredentials**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-164">**WinHttpSetCredentials**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

<span data-ttu-id="cc6bf-165">Übergibt die erforderlichen Autorisierungsanmeldeinformationen an den Server.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-165">Passes the required authorization credentials to the server.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-166">**WinHttpSetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-166">**WinHttpSetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="cc6bf-167">Legt die WinHTTP-Standardproxykonfiguration in der Registrierung fest.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-167">Sets the default WinHTTP proxy configuration in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-168">**WinHttpSetOption**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-168">**WinHttpSetOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

<span data-ttu-id="cc6bf-169">Legt eine Internetoption fest.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-169">Sets an Internet option.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-170">**WinHttpSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-170">**WinHttpSetStatusCallback**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

<span data-ttu-id="cc6bf-171">Richtet eine Rückruffunktion ein, die WinHTTP aufrufen kann, wenn der Fortschritt während eines Vorgangs erfolgt.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-171">Sets up a callback function that WinHTTP can call as progress is made during an operation.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-172">**WinHttpSetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-172">**WinHttpSetTimeouts**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

<span data-ttu-id="cc6bf-173">Legt die verschiedenen Time outs fest, die an HTTP-Transaktionen beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-173">Sets the various time-outs that are involved with HTTP transactions.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-174">**WinHttpTimeFromSystemTime**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-174">**WinHttpTimeFromSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

<span data-ttu-id="cc6bf-175">Formatiert ein Datum und eine Uhrzeit gemäß der HTTP-Version 1.0-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-175">Formats a date and time according to the HTTP version 1.0 specification.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-176">**WinHttpTimeToSystemTime**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-176">**WinHttpTimeToSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

<span data-ttu-id="cc6bf-177">Verwendet eine HTTP-Zeit-/Datumszeichenfolge und konvertiert sie in eine [**SYSTEMTIME-Struktur.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)</span><span class="sxs-lookup"><span data-stu-id="cc6bf-177">Takes an HTTP time/date string and converts it to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-178">**WinHttpWriteData**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-178">**WinHttpWriteData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

<span data-ttu-id="cc6bf-179">Schreibt Anforderungsdaten auf einen HTTP-Server.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-179">Writes request data to an HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-180">**WinHttpWebSocketClose**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-180">**WinHttpWebSocketClose**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

<span data-ttu-id="cc6bf-181">Schließt eine WebSocket-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-181">Closes a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-182">**WinHttpWebSocketCompleteUpgrade**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-182">**WinHttpWebSocketCompleteUpgrade**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

<span data-ttu-id="cc6bf-183">Schließt einen Von [**WinHttpSendRequest gestarteten**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)WebSocket-Handshake ab.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-183">Completes a WebSocket handshake started by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-184">**WinHttpWebSocketQueryCloseStatus**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-184">**WinHttpWebSocketQueryCloseStatus**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

<span data-ttu-id="cc6bf-185">Ruft den von einem Server gesendeten Schließstatus ab.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-185">Gets the close status sent by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-186">**WinHttpWebSocketReceive**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-186">**WinHttpWebSocketReceive**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

<span data-ttu-id="cc6bf-187">Empfängt Daten von einer WebSocket-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-187">Receives data from a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-188">**WinHttpWebSocketSend**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-188">**WinHttpWebSocketSend**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

<span data-ttu-id="cc6bf-189">Sendet Daten über eine WebSocket-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-189">Sends data over a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="cc6bf-190">**WinHttpWebSocketShutdown**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-190">**WinHttpWebSocketShutdown**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

<span data-ttu-id="cc6bf-191">Sendet einen schließenden Frame an eine WebSocket-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-191">Sends a close frame to a WebSocket connection.</span></span>

</dd> </dl>


