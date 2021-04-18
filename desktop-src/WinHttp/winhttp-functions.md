---
description: In diesem Thema werden die von WinHTTP bereitgestellten Funktionen beschrieben.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: WinHTTP-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6511d2e66acc923072cc7a961aae3cb572b8e466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347766"
---
# <a name="winhttp-functions"></a><span data-ttu-id="d1bf6-103">WinHTTP-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d1bf6-103">WinHTTP Functions</span></span>

<span data-ttu-id="d1bf6-104">WinHTTP bietet die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="d1bf6-104">WinHTTP provides the following functions:</span></span>

<dl> <dt>

[<span data-ttu-id="d1bf6-105">**Winhttpadressquestheaders**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-105">**WinHttpAddRequestHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

<span data-ttu-id="d1bf6-106">Fügt dem HTTP-Anforderungs handle mindestens einen HTTP-Anforderungs Header hinzu.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-106">Adds one or more HTTP request headers to the HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-107">**Winhttpcheckplatform**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-107">**WinHttpCheckPlatform**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

<span data-ttu-id="d1bf6-108">Bestimmt, ob die aktuelle Plattform von WinHTTP unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-108">Determines whether the current platform is supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-109">**WinHttpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-109">**WinHttpCloseHandle**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

<span data-ttu-id="d1bf6-110">Schließt ein einzelnes [HINTERNET](hinternet-handles-in-winhttp.md) -handle.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-110">Closes a single [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-111">**WinHttpConnect**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-111">**WinHttpConnect**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

<span data-ttu-id="d1bf6-112">Gibt den ursprünglichen Zielserver einer HTTP-Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-112">Specifies the initial target server of an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-113">**Winhttpcrackurl**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-113">**WinHttpCrackUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

<span data-ttu-id="d1bf6-114">Trennt eine URL in Ihre Komponenten Teile, z. b. Hostname und Pfad.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-114">Separates a URL into its component parts, for example, host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-115">**Winhttpkreateproxyresolver**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-115">**WinHttpCreateProxyResolver**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

<span data-ttu-id="d1bf6-116">Erstellt ein Handle für die Verwendung durch [**winhttpgetproxyforurlex**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="d1bf6-116">Creates a handle for use by [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-117">**Winhttpkreateurl**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-117">**WinHttpCreateUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

<span data-ttu-id="d1bf6-118">Erstellt eine URL aus Komponenten teilen, z. b. den Hostnamen und den Pfad.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-118">Creates a URL from component parts, for example, the host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-119">**Winhttpdetectautoproxyconfigurl**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-119">**WinHttpDetectAutoProxyConfigUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

<span data-ttu-id="d1bf6-120">Sucht die URL für die Datei mit der Proxy automatischen Konfiguration (PAC).</span><span class="sxs-lookup"><span data-stu-id="d1bf6-120">Finds the URL for the Proxy Auto-Configuration (PAC) file.</span></span> <span data-ttu-id="d1bf6-121">Diese Funktion meldet die URL der PAC-Datei, aber Sie lädt die Datei nicht herunter.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-121">This function reports the URL of the PAC file, but it does not download the file.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-122">**Winhttpfreproxyresult**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-122">**WinHttpFreeProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

<span data-ttu-id="d1bf6-123">Gibt die Daten frei, die von einem vorherigen Aufrufen von " [**winhttpgetproxyresult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)" abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-123">Frees the data retrieved from a previous call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-124">**WinHttpGetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-124">**WinHttpGetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="d1bf6-125">Ruft die standardmäßige WinHTTP-Proxykonfiguration aus der Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-125">Retrieves the default WinHTTP proxy configuration from the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-126">**WinHttpGetIEProxyConfigForCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-126">**WinHTTPGetIEProxyConfigForCurrentUser**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

<span data-ttu-id="d1bf6-127">Ruft die Internet Explorer-Proxykonfiguration für den aktuellen Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-127">Obtains the Internet Explorer (IE) proxy configuration for the current user.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-128">**WinHttpGetProxyForUrl**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-128">**WinHttpGetProxyForUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

<span data-ttu-id="d1bf6-129">Ruft die Proxy Informationen für die angegebene URL ab.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-129">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-130">**Winhttpgetproxyforurlex**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-130">**WinHttpGetProxyForUrlEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

<span data-ttu-id="d1bf6-131">Ruft die Proxy Informationen für die angegebene URL ab.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-131">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-132">**Winhttpgetproxyresult**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-132">**WinHttpGetProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

<span data-ttu-id="d1bf6-133">Ruft die Ergebnisse eines Aufrufens von [**winhttpgetproxyforurlex**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)ab.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-133">Retrieves the results of a call to [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-134">**WinHttpOpen**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-134">**WinHttpOpen**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

<span data-ttu-id="d1bf6-135">Initialisiert die Verwendung der WinHTTP-Funktionen einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-135">Initializes an application's use of the WinHTTP functions.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-136">**Winhttpopanrequest**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-136">**WinHttpOpenRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

<span data-ttu-id="d1bf6-137">Erstellt ein HTTP-Anforderungs handle.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-137">Creates an HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-138">**Winhttpqueryauthschemas**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-138">**WinHttpQueryAuthSchemes**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

<span data-ttu-id="d1bf6-139">Gibt die Autorisierungs Schemas zurück, die der Server unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-139">Returns the authorization schemes that the server supports.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-140">**WinHttpQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-140">**WinHttpQueryDataAvailable**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

<span data-ttu-id="d1bf6-141">Gibt die Anzahl der Daten Bytes zurück, die sofort verfügbar sind, um mit [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)gelesen zu werden.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-141">Returns the number of bytes of data that are available immediately to be read with [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-142">**WinHttpQueryHeaders**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-142">**WinHttpQueryHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

<span data-ttu-id="d1bf6-143">Ruft Header Informationen ab, die einer HTTP-Anforderung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-143">Retrieves header information associated with an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-144">**WinHttpQueryOption**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-144">**WinHttpQueryOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

<span data-ttu-id="d1bf6-145">Fragt eine Internet Option für das angegebene Handle ab.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-145">Queries an Internet option on the specified handle.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-146">**WinHttpReadData**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-146">**WinHttpReadData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

<span data-ttu-id="d1bf6-147">Liest Daten aus einem Handle, das von der [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) -Funktion geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-147">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-148">**WinHttpReceiveResponse**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-148">**WinHttpReceiveResponse**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

<span data-ttu-id="d1bf6-149">Beendet eine HTTP-Anforderung, die von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-149">Ends an HTTP request that is initiated by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-150">**Winhttpre\tautoproxy**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-150">**WinHttpResetAutoProxy**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

<span data-ttu-id="d1bf6-151">Setzt den automatischen Proxy zurück.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-151">Resets the auto-proxy.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-152">**WinHttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-152">**WinHttpSendRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

<span data-ttu-id="d1bf6-153">Sendet die angegebene Anforderung an den HTTP-Server.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-153">Sends the specified request to the HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-154">**Winhttpsetanmelde Informationen**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-154">**WinHttpSetCredentials**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

<span data-ttu-id="d1bf6-155">Übergibt die erforderlichen Autorisierungs Anmelde Informationen an den Server.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-155">Passes the required authorization credentials to the server.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-156">**WinHttpSetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-156">**WinHttpSetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="d1bf6-157">Legt die WinHTTP-Standard Proxykonfiguration in der Registrierung fest.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-157">Sets the default WinHTTP proxy configuration in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-158">**WinHttpSetOption**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-158">**WinHttpSetOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

<span data-ttu-id="d1bf6-159">Legt eine Internet Option fest.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-159">Sets an Internet option.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-160">**Winhttpsetstatus-Rückruf**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-160">**WinHttpSetStatusCallback**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

<span data-ttu-id="d1bf6-161">Richtet eine Rückruffunktion ein, die von WinHTTP aufgerufen werden kann, während ein Vorgang durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-161">Sets up a callback function that WinHTTP can call as progress is made during an operation.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-162">**Winhttpsettimeouts**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-162">**WinHttpSetTimeouts**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

<span data-ttu-id="d1bf6-163">Legt die verschiedenen Timeouts fest, die an http-Transaktionen beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-163">Sets the various time-outs that are involved with HTTP transactions.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-164">**Winhttptimefromsystemtime**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-164">**WinHttpTimeFromSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

<span data-ttu-id="d1bf6-165">Formatiert ein Datum und eine Uhrzeit gemäß der Spezifikation der HTTP-Version 1,0.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-165">Formats a date and time according to the HTTP version 1.0 specification.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-166">**Winhttptimeumsystemtime**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-166">**WinHttpTimeToSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

<span data-ttu-id="d1bf6-167">Nimmt eine HTTP-Zeit-/Datum-Zeichenfolge und konvertiert sie in eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-167">Takes an HTTP time/date string and converts it to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-168">**Winhttpschreitedata**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-168">**WinHttpWriteData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

<span data-ttu-id="d1bf6-169">Schreibt Anforderungs Daten auf einen HTTP-Server.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-169">Writes request data to an HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-170">**Winhttpwebsocketclose**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-170">**WinHttpWebSocketClose**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

<span data-ttu-id="d1bf6-171">Schließt eine WebSocket-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-171">Closes a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-172">**Winhttpwebsocketcompleteupgrade**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-172">**WinHttpWebSocketCompleteUpgrade**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

<span data-ttu-id="d1bf6-173">Schließt einen WebSocket-Handshake ab, der von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-173">Completes a WebSocket handshake started by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-174">**Winhttpwebsocketqueryclosestatus**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-174">**WinHttpWebSocketQueryCloseStatus**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

<span data-ttu-id="d1bf6-175">Ruft den von einem Server gesendeten Schluss Status ab.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-175">Gets the close status sent by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-176">**Winhttpwebsocketreceive**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-176">**WinHttpWebSocketReceive**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

<span data-ttu-id="d1bf6-177">Empfängt Daten von einer WebSocket-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-177">Receives data from a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-178">**Winhttpwebsocketsend**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-178">**WinHttpWebSocketSend**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

<span data-ttu-id="d1bf6-179">Sendet Daten über eine WebSocket-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-179">Sends data over a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="d1bf6-180">**Winhttpwebsocketshutdown**</span><span class="sxs-lookup"><span data-stu-id="d1bf6-180">**WinHttpWebSocketShutdown**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

<span data-ttu-id="d1bf6-181">Sendet einen close-Frame an eine WebSocket-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="d1bf6-181">Sends a close frame to a WebSocket connection.</span></span>

</dd> </dl>

 

 
