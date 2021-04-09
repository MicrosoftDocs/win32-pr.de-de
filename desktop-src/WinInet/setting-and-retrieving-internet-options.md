---
title: Festlegen und Abrufen von Internet Optionen
description: In diesem Thema wird beschrieben, wie Internet Optionen mithilfe der Funktionen InternetSetOption und InternetQueryOption festgelegt und abgerufen werden.
ms.assetid: b596a4a9-c34a-402a-af76-b930fe5f0901
keywords:
- Festlegen und Abrufen von Internet Optionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418bf21620cf7b7c4426844c95a39ef1fde04e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858409"
---
# <a name="setting-and-retrieving-internet-options"></a><span data-ttu-id="f9b3e-104">Festlegen und Abrufen von Internet Optionen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-104">Setting and Retrieving Internet Options</span></span>

<span data-ttu-id="f9b3e-105">In diesem Thema wird beschrieben, wie Internet Optionen mithilfe der Funktionen [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) und [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) festgelegt und abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-105">This topic describes how to set and retrieve Internet options using the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) functions.</span></span>

<span data-ttu-id="f9b3e-106">Internet Optionen können mit einem angegebenen [**hinternethandle**](appendix-a-hinternet-handles.md) oder den aktuellen Einstellungen in Microsoft Internet Explorer festgelegt oder abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-106">Internet options can be set on, or retrieved from, a specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle or the current settings in Microsoft Internet Explorer.</span></span>

-   [<span data-ttu-id="f9b3e-107">Implementierungs Schritte</span><span class="sxs-lookup"><span data-stu-id="f9b3e-107">Implementation Steps</span></span>](#implementation-steps)
    -   [<span data-ttu-id="f9b3e-108">Auswählen von Internet Optionen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-108">Choosing Internet Options</span></span>](#choosing-internet-options)
    -   [<span data-ttu-id="f9b3e-109">Auswählen des HINTERNET-Handles</span><span class="sxs-lookup"><span data-stu-id="f9b3e-109">Choosing the HINTERNET Handle</span></span>](#choosing-the-hinternet-handle)
    -   [<span data-ttu-id="f9b3e-110">Festlegen oder Abrufen der Optionen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-110">Setting or Retrieving the Options</span></span>](#setting-or-retrieving-the-options)
-   [<span data-ttu-id="f9b3e-111">Bereich des hinternethandles</span><span class="sxs-lookup"><span data-stu-id="f9b3e-111">Scope of HINTERNET Handle</span></span>](#scope-of-hinternet-handle)
-   [<span data-ttu-id="f9b3e-112">Festlegen einzelner Optionen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-112">Setting Individual Options</span></span>](#setting-individual-options)
-   [<span data-ttu-id="f9b3e-113">Abrufen einzelner Optionen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-113">Retrieving Individual Options</span></span>](#retrieving-individual-options)
    -   [<span data-ttu-id="f9b3e-114">Beispiel zum Vervollständigen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-114">Complete Sample</span></span>](#complete-sample)
-   [<span data-ttu-id="f9b3e-115">Festlegen von Verbindungsoptionen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-115">Setting Connection Options</span></span>](#setting-connection-options)
-   [<span data-ttu-id="f9b3e-116">Abrufen von Verbindungsoptionen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-116">Retrieving Connection Options</span></span>](#retrieving-connection-options)
-   [<span data-ttu-id="f9b3e-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-117">Related topics</span></span>](#related-topics)

## <a name="implementation-steps"></a><span data-ttu-id="f9b3e-118">Implementierungs Schritte</span><span class="sxs-lookup"><span data-stu-id="f9b3e-118">Implementation Steps</span></span>

<span data-ttu-id="f9b3e-119">Um Internet Optionen festzulegen oder abzurufen, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="f9b3e-119">To set or retrieve Internet options complete the following:</span></span>

-   [<span data-ttu-id="f9b3e-120">Auswählen von Internet Optionen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-120">Choosing Internet Options</span></span>](#choosing-internet-options)
-   [<span data-ttu-id="f9b3e-121">Auswählen des HINTERNET-Handles</span><span class="sxs-lookup"><span data-stu-id="f9b3e-121">Choosing the HINTERNET Handle</span></span>](#choosing-the-hinternet-handle)
-   [<span data-ttu-id="f9b3e-122">Festlegen oder Abrufen der Optionen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-122">Setting or Retrieving the Options</span></span>](#setting-or-retrieving-the-options)

### <a name="choosing-internet-options"></a><span data-ttu-id="f9b3e-123">Auswählen von Internet Optionen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-123">Choosing Internet Options</span></span>

<span data-ttu-id="f9b3e-124">Da es so viele Internet Optionen gibt, ist es wichtig, die richtigen Optionen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-124">Because there are so many Internet options, choosing the right options is important.</span></span> <span data-ttu-id="f9b3e-125">Viele Internetoptionen wirken sich auf das Verhalten der WinInet-Funktionen und Internet Explorer aus:</span><span class="sxs-lookup"><span data-stu-id="f9b3e-125">Many Internet options affect the behavior of the WinINet functions and Internet Explorer:</span></span>

<span data-ttu-id="f9b3e-126">Beispielsweise können Sie folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="f9b3e-126">For example, you can:</span></span>

-   <span data-ttu-id="f9b3e-127">Behandeln Sie die grundlegende Server-und Proxy Authentifizierung durch Festlegen von Benutzernamen und Kenn Wörtern.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-127">Handle basic server and proxy authentication by setting user names and passwords.</span></span>
-   <span data-ttu-id="f9b3e-128">Legen Sie die Benutzer-Agent-Zeichenfolge fest, die von Servern verwendet wird, um die Funktionen der Client Anwendung oder des Browsers zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-128">Set or retrieve the user agent string used by servers to identify the features of the client application or browser.</span></span>
-   <span data-ttu-id="f9b3e-129">Ruft den Handlertyp des angegebenen [**HINTERNET**](appendix-a-hinternet-handles.md) -Handles ab.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-129">Retrieve the handle type of the specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>

<span data-ttu-id="f9b3e-130">Weitere Informationen und eine Liste der Internet Optionen finden Sie unter [**Optionsflags**](option-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f9b3e-130">For more information and a list of the Internet options, see [**Option Flags**](option-flags.md).</span></span>

<span data-ttu-id="f9b3e-131">In Internet Explorer 5 und höher können einige Optionen über eine bestimmte Internetverbindung festgelegt oder abgerufen werden, indem die options [**Liste "Internet \_ pro \_ conn \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) " und die Optionen " [**Internet \_ pro \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) conn" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-131">In Internet Explorer 5 and later, some options can be set or retrieved from a specific Internet connection using the [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) and [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span> <span data-ttu-id="f9b3e-132">Weitere Informationen und eine Liste der Optionen, die von einer bestimmten Internet Verbindung festgelegt oder abgerufen werden können, finden Sie unter dem **dwOptions** -Member der [**Option "Internet \_ pro \_ conn \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) ".</span><span class="sxs-lookup"><span data-stu-id="f9b3e-132">For more information and a list of options that can be set or retrieved from a specific Internet connection, see the **dwOptions** member of the [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structure.</span></span>

### <a name="choosing-the-hinternet-handle"></a><span data-ttu-id="f9b3e-133">Auswählen des HINTERNET-Handles</span><span class="sxs-lookup"><span data-stu-id="f9b3e-133">Choosing the HINTERNET Handle</span></span>

<span data-ttu-id="f9b3e-134">Das [**HINTERNET**](appendix-a-hinternet-handles.md) -handle, das zum Festlegen oder Abrufen von Internet Optionen verwendet wird, bestimmt den Gültigkeitsbereich des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-134">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle used to set or retrieve Internet options determines the scope of the operation.</span></span> <span data-ttu-id="f9b3e-135">Alle Handles, die über diesen Handle erstellt werden, erben die für dieses Handle festgelegten Optionen.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-135">All the handles created through this handle will inherit the options set on this handle.</span></span>

<span data-ttu-id="f9b3e-136">Beispielsweise müssen Client Anwendungen, die einen Proxy mit Authentifizierung erfordern, wahrscheinlich nicht jedes Mal, wenn die Anwendung versucht, auf eine Internet Ressource zuzugreifen, den Proxy Benutzernamen und das Kennwort festlegen.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-136">For example, client applications that require a proxy with authentication, probably do not require setting the proxy user name and password every time the application attempts to access an Internet resource.</span></span> <span data-ttu-id="f9b3e-137">Wenn alle Anforderungen für eine bestimmte Verbindung vom gleichen Proxy verarbeitet werden und der Proxy Benutzername und das Kennwort für einen Verbindungstyp des [**hinternethandles**](appendix-a-hinternet-handles.md) festgelegt werden, d. h. ein Handle, das durch einen Aufruf von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde, können alle Aufrufe, die von diesem **HINTERNET** handle abgeleitet sind, denselben Proxy Benutzernamen und dasselbe Kennwort verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-137">If all requests on a given connection are handled by the same proxy, setting the proxy user name and password on a connection type [**HINTERNET**](appendix-a-hinternet-handles.md) handle, that is, a handle created by a call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), would allow any calls derived from this **HINTERNET** handle to use the same proxy user name and password.</span></span> <span data-ttu-id="f9b3e-138">Wenn Sie den Proxy Benutzernamen und das Kennwort jedes Mal festlegen, wenn ein **hinternethandle** von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) erstellt wird, ist zusätzlicher und unnötiger Verwaltungsaufwand erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-138">Setting the proxy user name and password every time an **HINTERNET** handle is created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) would require extra and unnecessary overhead.</span></span> <span data-ttu-id="f9b3e-139">Beachten Sie, dass bei Verwendung eines Proxys, für den eine Authentifizierung erforderlich ist, die Proxy Anmelde Informationen für jede neue Verbindung festgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-139">Be aware that if the application uses a proxy that requires authentication, it should set the proxy credentials on every new connection.</span></span>

### <a name="setting-or-retrieving-the-options"></a><span data-ttu-id="f9b3e-140">Festlegen oder Abrufen der Optionen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-140">Setting or Retrieving the Options</span></span>

<span data-ttu-id="f9b3e-141">Wenn Sie ermittelt haben, welche Internetoptionen und welches [**hinternethandle**](appendix-a-hinternet-handles.md) verwendet werden sollen, rufen Sie diese Internetoptionen ab.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-141">When you have determined what Internet options and [**HINTERNET**](appendix-a-hinternet-handles.md) handle to use, retrieve those Internet options.</span></span> <span data-ttu-id="f9b3e-142">Um Optionen festzulegen oder abzurufen, rufen Sie entweder [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) oder [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)auf.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-142">To set or retrieve options, call either [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

## <a name="scope-of-hinternet-handle"></a><span data-ttu-id="f9b3e-143">Bereich des hinternethandles</span><span class="sxs-lookup"><span data-stu-id="f9b3e-143">Scope of HINTERNET Handle</span></span>

<span data-ttu-id="f9b3e-144">Das [**hinternethandle**](appendix-a-hinternet-handles.md) , mit dem Internet Optionen festgelegt oder abgerufen werden, bestimmt die Aktionen, für die die Optionen gültig sind.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-144">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle used to set or retrieve Internet options determines the actions for which the options are valid.</span></span>

<span data-ttu-id="f9b3e-145">Diese Handles haben drei Ebenen:</span><span class="sxs-lookup"><span data-stu-id="f9b3e-145">These handles have three levels:</span></span>

-   <span data-ttu-id="f9b3e-146">Das [**HINTERNET**](appendix-a-hinternet-handles.md) -Stamm handle (das durch einen [**Internet Open**](/windows/desktop/api/Wininet/nf-wininet-internetopena)-Rückruf erstellt wurde) würde alle Internet Optionen enthalten, die diese Instanz von WinInet betreffen.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-146">The root [**HINTERNET**](appendix-a-hinternet-handles.md) handle (created by a call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) would contain all the Internet options that affect this instance of WinINet.</span></span>
-   <span data-ttu-id="f9b3e-147">[**HINTERNET**](appendix-a-hinternet-handles.md) Handles, die eine Verbindung mit einem Server herstellen (durch einen [**Internet Verbindungs**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)Gespräch erstellt)</span><span class="sxs-lookup"><span data-stu-id="f9b3e-147">[**HINTERNET**](appendix-a-hinternet-handles.md) handles that connect to a server (created by a call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta))</span></span>
-   <span data-ttu-id="f9b3e-148">[**Hinternethandles**](appendix-a-hinternet-handles.md) , die einer Ressource oder einer Enumeration von Ressourcen auf einem bestimmten Server zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-148">[**HINTERNET**](appendix-a-hinternet-handles.md) handles associated with a resource or enumeration of resources on a particular server.</span></span>

<span data-ttu-id="f9b3e-149">Zusätzlich zu den verschiedenen [**HINTERNET**](appendix-a-hinternet-handles.md) -Handles kann eine Anwendung auch **null** verwenden, um die Standardwerte der Internetoptionen, die von Internet Explorer und den WinInet-Funktionen verwendet werden, festzulegen oder abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-149">In addition to the various [**HINTERNET**](appendix-a-hinternet-handles.md) handles, an application can also use **NULL** to set or retrieve the default values of the Internet options used by Internet Explorer and the WinINet functions.</span></span> <span data-ttu-id="f9b3e-150">Wenn Sie beim Verwenden von **null** als handle Internet Optionen festlegen, werden die Standardwerte der Optionen geändert, die derzeit in der Registrierung gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-150">Setting Internet options when using **NULL** as the handle changes the default values of the options, which are currently stored in the registry.</span></span> <span data-ttu-id="f9b3e-151">Client Anwendungen sollten keine Registrierungsfunktionen verwenden, um die Standardwerte der Internet Optionen zu ändern, da die Implementierung der gespeicherten Optionen in Zukunft geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-151">Client applications should not use registry functions to change the default values of the Internet options, because the implementation of how the options are stored can be altered in the future.</span></span>

<span data-ttu-id="f9b3e-152">In der folgenden Tabelle sind die Typen der [**hinternethandles**](appendix-a-hinternet-handles.md) und der Bereich der Ihnen zugeordneten Internet Optionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-152">The following table lists the type of [**HINTERNET**](appendix-a-hinternet-handles.md) handles and the scope of the Internet options associated with them.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9b3e-153">Handle-Typ</span><span class="sxs-lookup"><span data-stu-id="f9b3e-153">Handle Type</span></span></th>
<th><span data-ttu-id="f9b3e-154">Bereich</span><span class="sxs-lookup"><span data-stu-id="f9b3e-154">Scope</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9b3e-155"><strong>NULL</strong></span><span class="sxs-lookup"><span data-stu-id="f9b3e-155"><strong>NULL</strong></span></span></td>
<td><span data-ttu-id="f9b3e-156">Die Standard Options Einstellungen für Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-156">The default option settings for Internet Explorer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9b3e-157">INTERNET_HANDLE_TYPE_CONNECT_FTP</span><span class="sxs-lookup"><span data-stu-id="f9b3e-157">INTERNET_HANDLE_TYPE_CONNECT_FTP</span></span></td>
<td><span data-ttu-id="f9b3e-158">Die Options Einstellungen für diese Verbindung mit einem FTP-Server.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-158">The option settings for this connection to an FTP server.</span></span> <span data-ttu-id="f9b3e-159">Diese Optionen wirken sich auf alle von diesem <a href="appendix-a-hinternet-handles.md"><strong>hinternethandle</strong></a> initiierten Vorgänge aus, z. b. Dateidownloads.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-159">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9b3e-160">INTERNET_HANDLE_TYPE_CONNECT_GOPHER</span><span class="sxs-lookup"><span data-stu-id="f9b3e-160">INTERNET_HANDLE_TYPE_CONNECT_GOPHER</span></span></td>
<td><span data-ttu-id="f9b3e-161">Die Options Einstellungen für diese Verbindung mit einem Gopher-Server.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-161">The option settings for this connection to a Gopher server.</span></span> <span data-ttu-id="f9b3e-162">Diese Optionen wirken sich auf alle von diesem <a href="appendix-a-hinternet-handles.md"><strong>hinternethandle</strong></a> initiierten Vorgänge aus, z. b. Dateidownloads.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-162">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="f9b3e-163">Nur Windows XP und Windows Server 2003 R2 und früher.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-163">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9b3e-164">INTERNET_HANDLE_TYPE_CONNECT_HTTP</span><span class="sxs-lookup"><span data-stu-id="f9b3e-164">INTERNET_HANDLE_TYPE_CONNECT_HTTP</span></span></td>
<td><span data-ttu-id="f9b3e-165">Die Options Einstellungen für diese Verbindung mit einem HTTP-Server.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-165">The option settings for this connection to an HTTP server.</span></span> <span data-ttu-id="f9b3e-166">Diese Optionen wirken sich auf alle von diesem <a href="appendix-a-hinternet-handles.md"><strong>hinternethandle</strong></a> initiierten Vorgänge aus, z. b. Dateidownloads.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-166">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9b3e-167">INTERNET_HANDLE_TYPE_FILE_REQUEST</span><span class="sxs-lookup"><span data-stu-id="f9b3e-167">INTERNET_HANDLE_TYPE_FILE_REQUEST</span></span></td>
<td><span data-ttu-id="f9b3e-168">Die Options Einstellungen, die dieser Datei Anforderung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-168">The option settings associated with this file request.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9b3e-169">INTERNET_HANDLE_TYPE_FTP_FILE</span><span class="sxs-lookup"><span data-stu-id="f9b3e-169">INTERNET_HANDLE_TYPE_FTP_FILE</span></span></td>
<td><span data-ttu-id="f9b3e-170">Die Options Einstellungen, die mit diesem FTP-Ressourcen Download verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-170">The option settings associated with this FTP resource download.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9b3e-171">INTERNET_HANDLE_TYPE_FTP_FILE_HTML</span><span class="sxs-lookup"><span data-stu-id="f9b3e-171">INTERNET_HANDLE_TYPE_FTP_FILE_HTML</span></span></td>
<td><span data-ttu-id="f9b3e-172">Die Options Einstellungen, die diesem FTP-Ressourcen Download zugeordnet sind, sind in HTML formatiert.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-172">The option settings associated with this FTP resource download formatted in HTML.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9b3e-173">INTERNET_HANDLE_TYPE_FTP_FIND</span><span class="sxs-lookup"><span data-stu-id="f9b3e-173">INTERNET_HANDLE_TYPE_FTP_FIND</span></span></td>
<td><span data-ttu-id="f9b3e-174">Die Options Einstellungen, die dieser Suche nach Dateien auf einem FTP-Server zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-174">The option settings associated with this search of files on an FTP server.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9b3e-175">INTERNET_HANDLE_TYPE_FTP_FIND_HTML</span><span class="sxs-lookup"><span data-stu-id="f9b3e-175">INTERNET_HANDLE_TYPE_FTP_FIND_HTML</span></span></td>
<td><span data-ttu-id="f9b3e-176">Die Options Einstellungen, die dieser Suche nach Dateien auf einem FTP-Server zugeordnet sind, die in HTML formatiert sind.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-176">The option settings associated with this search of files on an FTP server formatted in HTML.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9b3e-177">INTERNET_HANDLE_TYPE_GOPHER_FILE</span><span class="sxs-lookup"><span data-stu-id="f9b3e-177">INTERNET_HANDLE_TYPE_GOPHER_FILE</span></span></td>
<td><span data-ttu-id="f9b3e-178">Die Options Einstellungen, die diesem Gopher-Ressourcen Download zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-178">The option settings associated with this Gopher resource download.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="f9b3e-179">Nur Windows XP und Windows Server 2003 R2 und früher.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-179">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9b3e-180">INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</span><span class="sxs-lookup"><span data-stu-id="f9b3e-180">INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</span></span></td>
<td><span data-ttu-id="f9b3e-181">Die Options Einstellungen, die diesem Gopher-Ressourcen Download zugeordnet sind, sind in HTML formatiert.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-181">The option settings associated with this Gopher resource download formatted in HTML.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="f9b3e-182">Nur Windows XP und Windows Server 2003 R2 und früher.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-182">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9b3e-183">INTERNET_HANDLE_TYPE_GOPHER_FIND</span><span class="sxs-lookup"><span data-stu-id="f9b3e-183">INTERNET_HANDLE_TYPE_GOPHER_FIND</span></span></td>
<td><span data-ttu-id="f9b3e-184">Die Options Einstellungen, die dieser Suche nach Dateien auf einem Gopher-Server zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-184">The option settings associated with this search of files on an Gopher server.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="f9b3e-185">Nur Windows XP und Windows Server 2003 R2 und früher.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-185">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9b3e-186">INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</span><span class="sxs-lookup"><span data-stu-id="f9b3e-186">INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</span></span></td>
<td><span data-ttu-id="f9b3e-187">Die Options Einstellungen, die dieser Suche nach Dateien auf einem Gopher-Server zugeordnet sind, der in HTML formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-187">The option settings associated with this search of files on an Gopher server formatted in HTML.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="f9b3e-188">Nur Windows XP und Windows Server 2003 R2 und früher.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-188">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9b3e-189">INTERNET_HANDLE_TYPE_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="f9b3e-189">INTERNET_HANDLE_TYPE_HTTP_REQUEST</span></span></td>
<td><span data-ttu-id="f9b3e-190">Die Options Einstellungen, die dieser HTTP-Anforderung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-190">The option settings associated with this HTTP request.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9b3e-191">INTERNET_HANDLE_TYPE_INTERNET</span><span class="sxs-lookup"><span data-stu-id="f9b3e-191">INTERNET_HANDLE_TYPE_INTERNET</span></span></td>
<td><span data-ttu-id="f9b3e-192">Die Options Einstellungen, die dieser Instanz der WinInet-Funktionen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-192">The option settings associated with this instance of the WinINet functions.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="setting-individual-options"></a><span data-ttu-id="f9b3e-193">Festlegen einzelner Optionen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-193">Setting Individual Options</span></span>

<span data-ttu-id="f9b3e-194">Nachdem Sie die Internetoptionen festgelegt haben, die Sie festlegen möchten, und den von diesen Optionen betroffenen Bereich festlegen, ist das Festlegen von Internetoptionen nicht kompliziert.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-194">After determining the Internet options you want to set and the scope you want affected by these options, setting Internet options is not complicated.</span></span> <span data-ttu-id="f9b3e-195">Sie müssen lediglich die [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) -Funktion mit dem gewünschten [**HINTERNET**](appendix-a-hinternet-handles.md) handle, dem Internet Optionsflag und einem Puffer, der die Informationen enthält, die Sie festlegen möchten, abrufen.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-195">All you would need to do is call the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function with desired [**HINTERNET**](appendix-a-hinternet-handles.md) handle, Internet option flag, and a buffer that contains the information you want set.</span></span>

<span data-ttu-id="f9b3e-196">Im folgenden Beispiel wird gezeigt, wie der Proxy Benutzername und das Kennwort für ein angegebenes [**HINTERNET**](appendix-a-hinternet-handles.md) -handle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-196">The following example shows how to set the proxy user name and password on a specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>


```C++
// strUsername is a string buffer of cchMax characters or less.
// It contains the proxy user name.
size_t cchMax = 80;
size_t cchUserLength, cchPasswordLength;
HRESULT hr = StringCchLength(strUsername, cchMax, &cchUserLength);

if (SUCCEEDED(hr))
{
   // hOpen is the HINTERNET handle created by InternetConnect.
   InternetSetOption(hConnect, INTERNET_OPTION_PROXY_USERNAME,
      strUsername, DWORD(cchUserLength)+1);
}
else
{
   // Insert error handling code here.
}

// strPassword is the string buffer that contains the proxy password.
hr = StringCchLength(strPassword, cchMax, &cchPasswordLength);

InternetSetOption(hOpen, INTERNET_OPTION_PROXY_PASSWORD,
    strPassword, DWORD(cchPasswordLength)+1);
```



## <a name="retrieving-individual-options"></a><span data-ttu-id="f9b3e-197">Abrufen einzelner Optionen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-197">Retrieving Individual Options</span></span>

<span data-ttu-id="f9b3e-198">Internet Optionen können mithilfe der [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) -Funktion abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-198">Internet options can be retrieved using the [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) function.</span></span> <span data-ttu-id="f9b3e-199">So rufen Sie Internet Optionen ab:</span><span class="sxs-lookup"><span data-stu-id="f9b3e-199">To retrieve Internet options:</span></span>

1.  <span data-ttu-id="f9b3e-200">Bestimmen Sie die Puffergröße, die zum Abrufen der Internet Options Informationen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-200">Determine the buffer size necessary to retrieve the Internet option information.</span></span>

    <span data-ttu-id="f9b3e-201">Die Puffergröße kann ermittelt werden, indem für die Adresse des Puffers **null** verwendet und eine Puffergröße von NULL übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-201">The buffer size can be determined by using **NULL** for the address of the buffer and passing it a buffer size of zero.</span></span>

    ```C++
    DWORD dwSize;
    InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);
    ```

    

    <span data-ttu-id="f9b3e-202">Der von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) zurückgegebene Wert ist die Menge an Arbeitsspeicher, die zum Abrufen der Informationen benötigt wird (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="f9b3e-202">The value returned by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) is the amount of memory required to retrieve the information, in bytes.</span></span>

2.  <span data-ttu-id="f9b3e-203">Zuordnen eines Speichers für den Puffer.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-203">Allocate a memory for the buffer.</span></span>
    ```C++
    char *lpszData;
    lpszData = new char[dwSize];
    ```

    

3.  <span data-ttu-id="f9b3e-204">Rufen Sie die Daten ab.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-204">Retrieve the data.</span></span>
    ```C++
    InternetQueryOption( NULL, 
                         INTERNET_OPTION_USER_AGENT,
                         lpszData, &dwSize );
    ```

    

4.  <span data-ttu-id="f9b3e-205">Freigeben des Speichers.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-205">Free the memory.</span></span>
    ```C++
    delete [] lpszData;
    ```

    

### <a name="complete-sample"></a><span data-ttu-id="f9b3e-206">Beispiel zum Vervollständigen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-206">Complete Sample</span></span>

<span data-ttu-id="f9b3e-207">Im folgenden finden Sie das gesamte Beispiel, das im vorherigen Abschnitt verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-207">The following is the complete sample used in the previous section.</span></span> <span data-ttu-id="f9b3e-208">Dieses Beispiel zeigt, wie die standardmäßige Benutzer-Agent-Zeichenfolge abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-208">This sample shows how to retrieve the default user agent string.</span></span>


```C++
// This call determines the required buffer size.
DWORD dwSize;
InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);

// Allocate the necessary memory.
char *lpszData;
lpszData = new char[dwSize];

// Call InternetQueryOption again with the provided buffer.
InternetQueryOption( NULL, 
                     INTERNET_OPTION_USER_AGENT,
                     lpszData, &dwSize );

// Insert code here to use the user agent string data.

// Free the allocated memory.
delete [] lpszData;
```



## <a name="setting-connection-options"></a><span data-ttu-id="f9b3e-209">Festlegen von Verbindungsoptionen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-209">Setting Connection Options</span></span>

<span data-ttu-id="f9b3e-210">In Internet Explorer 5 und höher können Internetoptionen für eine bestimmte Verbindung auf festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-210">In Internet Explorer 5 and later, Internet options can be set for on a specific connection.</span></span> <span data-ttu-id="f9b3e-211">Zuvor wurden für alle Verbindungen dieselben Internet Options Einstellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-211">Previously, all connections shared the same Internet option settings.</span></span> <span data-ttu-id="f9b3e-212">So legen Sie Optionen für eine bestimmte Verbindung fest:</span><span class="sxs-lookup"><span data-stu-id="f9b3e-212">To set options for a particular connection:</span></span>

1.  <span data-ttu-id="f9b3e-213">Erstellen Sie [**eine \_ \_ \_ options \_ Listenstruktur für das Internet pro Conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .</span><span class="sxs-lookup"><span data-stu-id="f9b3e-213">Create an [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure.</span></span>
2.  <span data-ttu-id="f9b3e-214">Weisen Sie den Arbeitsspeicher für die einzelnen Internet Optionen zu, die Sie für die Verbindung festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-214">Allocate the memory for the individual Internet options that you want to set for the connection.</span></span>
3.  <span data-ttu-id="f9b3e-215">Legen Sie die Optionen im [**Internet \_ pro Conn- \_ \_ options**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) Strukturen fest.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-215">Set the options in [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span>
4.  <span data-ttu-id="f9b3e-216">Legen Sie die Optionen mithilfe von [**internettoption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)fest.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-216">Set the options using [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="f9b3e-217">Im folgenden Codebeispiel wird gezeigt, wie Proxy Daten für eine LAN-Verbindung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-217">The following code example shows how to set proxy data for a LAN connection.</span></span>


```C++
BOOL SetConnectionOptions()
{
    INTERNET_PER_CONN_OPTION_LIST list;
    BOOL    bReturn;
    DWORD   dwBufSize = sizeof(list);

    // Fill the list structure.
    list.dwSize = sizeof(list);

    // NULL == LAN, otherwise connectoid name.
    list.pszConnection = NULL;

    // Set three options.
    list.dwOptionCount = 3;
    list.pOptions = new INTERNET_PER_CONN_OPTION[3];

    // Ensure that the memory was allocated.
    if(NULL == list.pOptions)
    {
        // Return FALSE if the memory wasn't allocated.
        return FALSE;
    }

    // Set flags.
    list.pOptions[0].dwOption = INTERNET_PER_CONN_FLAGS;
    list.pOptions[0].Value.dwValue = PROXY_TYPE_DIRECT |
        PROXY_TYPE_PROXY;

    // Set proxy name.
    list.pOptions[1].dwOption = INTERNET_PER_CONN_PROXY_SERVER;
    list.pOptions[1].Value.pszValue = TEXT("https://proxy:80");

    // Set proxy override.
    list.pOptions[2].dwOption = INTERNET_PER_CONN_PROXY_BYPASS;
    list.pOptions[2].Value.pszValue = TEXT("local");

    // Set the options on the connection.
    bReturn = InternetSetOption(NULL,
        INTERNET_OPTION_PER_CONNECTION_OPTION, &list, dwBufSize);

    // Free the allocated memory.
    delete [] list.pOptions;

    return bReturn;
}
```



## <a name="retrieving-connection-options"></a><span data-ttu-id="f9b3e-218">Abrufen von Verbindungsoptionen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-218">Retrieving Connection Options</span></span>

<span data-ttu-id="f9b3e-219">In Internet Explorer 5 und höher können Internetoptionen über eine bestimmte Verbindung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-219">In Internet Explorer 5 and later, Internet options can be retrieved from a specific connection.</span></span> <span data-ttu-id="f9b3e-220">So rufen Sie Optionen von einer bestimmten Verbindung ab</span><span class="sxs-lookup"><span data-stu-id="f9b3e-220">To retrieve options from a particular connection:</span></span>

1.  <span data-ttu-id="f9b3e-221">Erstellen Sie [**eine \_ \_ \_ options \_ Listenstruktur für das Internet pro Conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .</span><span class="sxs-lookup"><span data-stu-id="f9b3e-221">Create a [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure.</span></span>
2.  <span data-ttu-id="f9b3e-222">Weisen Sie den Arbeitsspeicher für die einzelnen Internet Optionen zu, die von der Verbindung abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-222">Allocate the memory for the individual Internet options to retrieve from the connection.</span></span>
3.  <span data-ttu-id="f9b3e-223">Geben Sie die Optionen mithilfe der Optionen [**Internet \_ pro \_ conn- \_ Option**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) an.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-223">Specify the options using [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span>
4.  <span data-ttu-id="f9b3e-224">Rufen Sie die Optionen mithilfe von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)ab.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-224">Retrieve the options using [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>
5.  <span data-ttu-id="f9b3e-225">Verwenden Sie die Option Data.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-225">Utilize the option data.</span></span>
6.  <span data-ttu-id="f9b3e-226">Verwenden Sie die [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) -Funktion, um den Arbeitsspeicher freizugeben, der den Options Daten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-226">Free the memory, allocated to hold the option data, using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span>

> [!Note]  
> <span data-ttu-id="f9b3e-227">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-227">WinINet does not support server implementations.</span></span> <span data-ttu-id="f9b3e-228">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9b3e-228">In addition, it should not be used from a service.</span></span> <span data-ttu-id="f9b3e-229">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="f9b3e-229">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f9b3e-230">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9b3e-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9b3e-231">Behandeln der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="f9b3e-231">Handling Authentication</span></span>](handling-authentication.md)
</dt> <dt>

[<span data-ttu-id="f9b3e-232">HINTERNET-Handles</span><span class="sxs-lookup"><span data-stu-id="f9b3e-232">HINTERNET Handles</span></span>](appendix-a-hinternet-handles.md)
</dt> </dl>

 

