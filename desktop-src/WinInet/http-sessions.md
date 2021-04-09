---
title: HTTP-Sitzungen
description: Der Zugriff auf die Ressourcen auf dem www erfolgt über http.
ms.assetid: 0f307e28-9c38-41e7-9795-7eef08e99a3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b0b4d30bc86c588495a55ed4867a4084c43a09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101866"
---
# <a name="http-sessions"></a><span data-ttu-id="06128-103">HTTP-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="06128-103">HTTP Sessions</span></span>

<span data-ttu-id="06128-104">WinInet ermöglicht Ihnen den Zugriff auf Ressourcen auf dem World Wide Web (www).</span><span class="sxs-lookup"><span data-stu-id="06128-104">WinINet enables you to access resources on the World Wide Web (WWW).</span></span> <span data-ttu-id="06128-105">Der Zugriff auf diese Ressourcen erfolgt direkt über [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (Weitere Informationen finden Sie unter Direktes [Aufrufen von URLs](handling-uniform-resource-locators.md)).</span><span class="sxs-lookup"><span data-stu-id="06128-105">These resources can be accessed directly by using [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for more information, see [Accessing URLs Directly](handling-uniform-resource-locators.md)).</span></span>

<span data-ttu-id="06128-106">Der Zugriff auf die Ressourcen auf dem www erfolgt über http.</span><span class="sxs-lookup"><span data-stu-id="06128-106">Resources on the WWW are accessed by using http.</span></span> <span data-ttu-id="06128-107">Die HTTP-Funktionen verarbeiten die zugrunde liegenden Protokolle und ermöglichen Ihrer Anwendung den Zugriff auf Informationen über das www.</span><span class="sxs-lookup"><span data-stu-id="06128-107">The HTTP functions handle the underlying protocols, while allowing your application to access information on the WWW.</span></span> <span data-ttu-id="06128-108">Wenn das HTTP-Protokoll weiterentwickelt wird, werden die zugrunde liegenden Protokolle aktualisiert, um das Funktionsverhalten aufrechtzuerhalten.</span><span class="sxs-lookup"><span data-stu-id="06128-108">As the HTTP protocol evolves, the underlying protocols are updated to maintain function behavior.</span></span>

<span data-ttu-id="06128-109">Das folgende Diagramm zeigt die Beziehungen der Funktionen, die mit dem HTTP-Protokoll verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06128-109">The following diagram shows the relationships of the functions that are used with the HTTP protocol.</span></span> <span data-ttu-id="06128-110">Die schattierten Felder stellen Funktionen dar, die [**hinternethandles**](appendix-a-hinternet-handles.md) zurückgeben, während die einfachen Felder Funktionen darstellen, die das **hinternethandle** verwenden, das von der Funktion erstellt wurde, von der Sie abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="06128-110">The shaded boxes represent functions that return [**HINTERNET**](appendix-a-hinternet-handles.md) handles, while the plain boxes represent functions that use the **HINTERNET** handle created by the function on which they depend.</span></span>

![für http verwendete WinInet-Funktionen](images/ax-wnt05.png)

<span data-ttu-id="06128-112">Weitere Informationen finden Sie unter [HINTERNET Handles](appendix-a-hinternet-handles.md).</span><span class="sxs-lookup"><span data-stu-id="06128-112">For more information, see [HINTERNET Handles](appendix-a-hinternet-handles.md).</span></span>

## <a name="using-the-wininet-functions-to-access-the-www"></a><span data-ttu-id="06128-113">Verwenden der WinInet-Funktionen für den Zugriff auf das www</span><span class="sxs-lookup"><span data-stu-id="06128-113">Using the WinINet Functions to Access the WWW</span></span>

-   [<span data-ttu-id="06128-114">Initiieren einer Verbindung mit dem www</span><span class="sxs-lookup"><span data-stu-id="06128-114">Initiating a Connection to the WWW</span></span>](#initiating-a-connection-to-the-www)
-   [<span data-ttu-id="06128-115">Öffnen einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="06128-115">Opening a Request</span></span>](#opening-a-request)
-   [<span data-ttu-id="06128-116">Anforderungs Header werden hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="06128-116">Adding Request Headers</span></span>](#adding-request-headers)
-   [<span data-ttu-id="06128-117">Senden einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="06128-117">Sending a Request</span></span>](#sending-a-request)
-   [<span data-ttu-id="06128-118">Veröffentlichen von Daten auf dem Server</span><span class="sxs-lookup"><span data-stu-id="06128-118">Posting Data to the Server</span></span>](#posting-data-to-the-server)
-   [<span data-ttu-id="06128-119">Informationen zu einer Anforderung erhalten</span><span class="sxs-lookup"><span data-stu-id="06128-119">Getting Information About a Request</span></span>](#getting-information-about-a-request)
-   [<span data-ttu-id="06128-120">Herunterladen von Ressourcen aus dem www</span><span class="sxs-lookup"><span data-stu-id="06128-120">Downloading Resources from the WWW</span></span>](#downloading-resources-from-the-www)

<span data-ttu-id="06128-121">Die folgenden Funktionen werden während der HTTP-Sitzungen verwendet, um auf das www zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="06128-121">The following functions are used during HTTP sessions to access the WWW.</span></span>



| <span data-ttu-id="06128-122">Funktion</span><span class="sxs-lookup"><span data-stu-id="06128-122">Function</span></span>                                               | <span data-ttu-id="06128-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06128-123">Description</span></span>                                                                                                                                                                                  |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06128-124">**Httpadressquestheaders**</span><span class="sxs-lookup"><span data-stu-id="06128-124">**HttpAddRequestHeaders**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) | <span data-ttu-id="06128-125">Fügt dem HTTP-Anforderungs handle HTTP-Anforderungs Header hinzu.</span><span class="sxs-lookup"><span data-stu-id="06128-125">Adds HTTP request headers to the HTTP request handle.</span></span> <span data-ttu-id="06128-126">Diese Funktion erfordert ein Handle, das von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="06128-126">This function requires a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                 |
| [<span data-ttu-id="06128-127">**Httpopanrequest**</span><span class="sxs-lookup"><span data-stu-id="06128-127">**HttpOpenRequest**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)             | <span data-ttu-id="06128-128">Öffnet ein HTTP-Anforderungs handle.</span><span class="sxs-lookup"><span data-stu-id="06128-128">Opens an HTTP request handle.</span></span> <span data-ttu-id="06128-129">Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="06128-129">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                                                         |
| [<span data-ttu-id="06128-130">**HttpQueryInfo**</span><span class="sxs-lookup"><span data-stu-id="06128-130">**HttpQueryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)                 | <span data-ttu-id="06128-131">Fragt Informationen über eine HTTP-Anforderung ab.</span><span class="sxs-lookup"><span data-stu-id="06128-131">Queries information about an HTTP request.</span></span> <span data-ttu-id="06128-132">Diese Funktion erfordert ein Handle, das von der [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) -Funktion oder der [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) -Funktion erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="06128-132">This function requires a handle created by the [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> |
| [<span data-ttu-id="06128-133">**HttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="06128-133">**HttpSendRequest**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)             | <span data-ttu-id="06128-134">Sendet die angegebene HTTP-Anforderung an den HTTP-Server.</span><span class="sxs-lookup"><span data-stu-id="06128-134">Sends the specified HTTP request to the HTTP server.</span></span> <span data-ttu-id="06128-135">Diese Funktion erfordert ein Handle, das von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="06128-135">This function requires a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                  |
| [<span data-ttu-id="06128-136">**Internetzterrordlg**</span><span class="sxs-lookup"><span data-stu-id="06128-136">**InternetErrorDlg**</span></span>](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)           | <span data-ttu-id="06128-137">Zeigt vordefinierte Dialogfelder für häufige Internet Fehlerbedingungen an.</span><span class="sxs-lookup"><span data-stu-id="06128-137">Displays predefined dialog boxes for common Internet error conditions.</span></span> <span data-ttu-id="06128-138">Diese Funktion erfordert das Handle, das im-Befehl von [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="06128-138">This function requires the handle used in the call to [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span>                     |



 

### <a name="initiating-a-connection-to-the-www"></a><span data-ttu-id="06128-139">Initiieren einer Verbindung mit dem www</span><span class="sxs-lookup"><span data-stu-id="06128-139">Initiating a Connection to the WWW</span></span>

<span data-ttu-id="06128-140">Zum Starten einer Verbindung mit dem www muss die Anwendung die [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -Funktion für das von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)zurückgegebene Stamm- [**HINTERNET**](appendix-a-hinternet-handles.md) anrufen.</span><span class="sxs-lookup"><span data-stu-id="06128-140">To start a connection to the WWW, the application must call the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function on the root [**HINTERNET**](appendix-a-hinternet-handles.md) returned by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="06128-141">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) muss eine HTTP-Sitzung einrichten, indem der \_ http-Diensttyp "Internet Dienst" deklariert wird \_ .</span><span class="sxs-lookup"><span data-stu-id="06128-141">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) must establish an HTTP session by declaring the INTERNET\_SERVICE\_HTTP service type.</span></span> <span data-ttu-id="06128-142">Weitere Informationen zur Verwendung von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)finden Sie unter [Verwenden von InternetConnect](enabling-internet-functionality.md).</span><span class="sxs-lookup"><span data-stu-id="06128-142">For more information on using [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), see [Using InternetConnect](enabling-internet-functionality.md).</span></span>

### <a name="opening-a-request"></a><span data-ttu-id="06128-143">Öffnen einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="06128-143">Opening a Request</span></span>

<span data-ttu-id="06128-144">Die [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) -Funktion öffnet eine HTTP-Anforderung und gibt ein [**HINTERNET**](appendix-a-hinternet-handles.md) -Handle zurück, das von den anderen HTTP-Funktionen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="06128-144">The [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function opens an HTTP request and returns an [**HINTERNET**](appendix-a-hinternet-handles.md) handle that can be used by the other HTTP functions.</span></span> <span data-ttu-id="06128-145">Anders als bei den anderen geöffneten Funktionen (z. b. [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)) sendet [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) die Anforderung nicht an das Internet, wenn aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="06128-145">Unlike the other open functions (such as [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) does not send the request to the Internet when called.</span></span> <span data-ttu-id="06128-146">Die [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) -Funktion sendet die Anforderung und stellt eine Verbindung über das Netzwerk her.</span><span class="sxs-lookup"><span data-stu-id="06128-146">The [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) function sends the request and establishes a connection over the network.</span></span>

<span data-ttu-id="06128-147">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) nimmt ein HTTP-Sitzungs handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt wurde, und ein HTTP-Verb, einen Objektnamen, eine Versions Zeichenfolge, einen referenrer, accept-Typen, Flags und einen Kontextwert</span><span class="sxs-lookup"><span data-stu-id="06128-147">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) takes an HTTP session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and an HTTP verb, object name, version string, referrer, accept types, flags, and context value.</span></span>

<span data-ttu-id="06128-148">Das HTTP-Verb ist eine Zeichenfolge, die in der Anforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="06128-148">The HTTP verb is a string to be used in the request.</span></span> <span data-ttu-id="06128-149">Allgemeine HTTP-Verben, die in Anforderungen verwendet werden, sind Get, Put und Post.</span><span class="sxs-lookup"><span data-stu-id="06128-149">Common HTTP verbs used in requests include GET, PUT, and POST.</span></span> <span data-ttu-id="06128-150">Wenn dieser Wert auf **null** festgelegt ist, verwendet [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) den Standardwert Get.</span><span class="sxs-lookup"><span data-stu-id="06128-150">If this value is set to **NULL**, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) uses the default value GET.</span></span>

<span data-ttu-id="06128-151">Der Objektname ist eine Zeichenfolge, die den Namen des angegebenen Zielobjekts des HTTP-Verbs enthält.</span><span class="sxs-lookup"><span data-stu-id="06128-151">The object name is a string that contains the name of the specified HTTP verb's target object.</span></span> <span data-ttu-id="06128-152">Dies ist im Allgemeinen ein Dateiname, ein ausführbares Modul oder ein suchspezifizierer.</span><span class="sxs-lookup"><span data-stu-id="06128-152">This is generally a file name, an executable module, or a search specifier.</span></span> <span data-ttu-id="06128-153">Wenn der angegebene Objektname eine leere Zeichenfolge ist, sucht [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) nach der Standardseite.</span><span class="sxs-lookup"><span data-stu-id="06128-153">If the object name supplied is an empty string, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) looks for the default page.</span></span>

<span data-ttu-id="06128-154">Die Versions Zeichenfolge sollte die HTTP-Version enthalten.</span><span class="sxs-lookup"><span data-stu-id="06128-154">The version string should contain the HTTP version.</span></span> <span data-ttu-id="06128-155">Wenn dieser Parameter **null** ist, verwendet die Funktion "" http/1.1 "".</span><span class="sxs-lookup"><span data-stu-id="06128-155">If this parameter is **NULL**, the function uses ""HTTP/1.1"".</span></span>

<span data-ttu-id="06128-156">Der Verweiser gibt die Adresse des Dokuments an, aus dem der Objektname abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="06128-156">The referrer specifies the address of the document from which the object name was obtained.</span></span> <span data-ttu-id="06128-157">Wenn dieser Parameter **null** ist, wird kein Verweiser angegeben.</span><span class="sxs-lookup"><span data-stu-id="06128-157">If this parameter is **NULL**, no referrer is specified.</span></span>

<span data-ttu-id="06128-158">Die **null**-terminierte Zeichenfolge, die die Accept-Typen enthält, gibt die von der Anwendung akzeptierten Inhaltstypen an.</span><span class="sxs-lookup"><span data-stu-id="06128-158">The **null**-terminated string that contains the accept types indicates the content types accepted by the application.</span></span> <span data-ttu-id="06128-159">Durch Festlegen dieses Parameters auf **null** wird angegeben, dass von der Anwendung keine Inhaltstypen akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="06128-159">Setting this parameter to **NULL** indicates that no content types are accepted by the application.</span></span> <span data-ttu-id="06128-160">Wenn eine leere Zeichenfolge angegeben wird, gibt die Anwendung an, dass nur Dokumente vom Typ "Text/" akzeptiert werden \* .</span><span class="sxs-lookup"><span data-stu-id="06128-160">If an empty string is supplied, the application indicates it accepts only documents of type ""text/\*"".</span></span> <span data-ttu-id="06128-161">Der Wert "" Text/ \* "" zeigt nur-Text-Dokumente an – nicht Bilder oder andere Binärdateien.</span><span class="sxs-lookup"><span data-stu-id="06128-161">The value ""text/\*"" indicates text-only documents—not pictures or other binary files.</span></span>

<span data-ttu-id="06128-162">Die Flagwerte Steuern Zwischenspeicherung, Cookies und Sicherheitsprobleme.</span><span class="sxs-lookup"><span data-stu-id="06128-162">The flag values control caching, cookies, and security issues.</span></span> <span data-ttu-id="06128-163">Legen Sie für Microsoft Network (MSN), NTLM und andere Authentifizierungs Typen das Flag [Internet \_ Flag \_ Keep \_ Connection](api-flags.md) fest.</span><span class="sxs-lookup"><span data-stu-id="06128-163">For Microsoft Network (MSN), NTLM, and other types of authentication, set the [INTERNET\_FLAG\_KEEP\_CONNECTION](api-flags.md) flag.</span></span>

<span data-ttu-id="06128-164">Wenn das [Internet \_ Flag \_ Async](api-flags.md) -Flag im Aufrufen von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)festgelegt wurde, sollte für den ordnungsgemäßen asynchronen Vorgang ein Kontextwert ungleich NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="06128-164">If the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag was set in the call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), a nonzero context value should be set for proper asynchronous operation.</span></span>

<span data-ttu-id="06128-165">Das folgende Beispiel ist ein Beispiel für [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="06128-165">The following example is a sample call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>

`hHttpRequest = HttpOpenRequest( hHttpSession, "GET", "", NULL, "", NULL, 0, 0);`

### <a name="adding-request-headers"></a><span data-ttu-id="06128-166">Anforderungs Header werden hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="06128-166">Adding Request Headers</span></span>

<span data-ttu-id="06128-167">Die [**httpadressquestheaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) -Funktion ermöglicht Anwendungen das Hinzufügen eines oder mehrerer Anforderungs Header zur ursprünglichen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="06128-167">The [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) function enables applications to add one or more request headers to the initial request.</span></span> <span data-ttu-id="06128-168">Diese Funktion ermöglicht es einer Anwendung, zusätzliche Header mit freiem Format an das HTTP-Anforderungs handle anzufügen. Es ist für die Verwendung durch anspruchsvolle Anwendungen vorgesehen, die eine genaue Kontrolle über die an den HTTP-Server gesendete Anforderung erfordern.</span><span class="sxs-lookup"><span data-stu-id="06128-168">This function allows an application to append additional free-format headers to the HTTP request handle; it is intended for use by sophisticated applications that require precise control over the request sent to the HTTP server.</span></span>

<span data-ttu-id="06128-169">[**Httpadressquestheaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) benötigt ein von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)erstelltes HTTP-Anforderungs handle, eine Zeichenfolge, die die Header, die Länge der Header und Modifizierer enthält.</span><span class="sxs-lookup"><span data-stu-id="06128-169">[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) needs an HTTP request handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), a string that contains the headers, the length of the headers, and modifiers.</span></span>

### <a name="sending-a-request"></a><span data-ttu-id="06128-170">Senden einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="06128-170">Sending a Request</span></span>

<span data-ttu-id="06128-171">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) stellt eine Verbindung mit dem Internet her und sendet die Anforderung an den angegebenen Standort.</span><span class="sxs-lookup"><span data-stu-id="06128-171">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) establishes a connection to the Internet and sends the request to the specified site.</span></span> <span data-ttu-id="06128-172">Diese Funktion erfordert ein [**hinternethandle**](appendix-a-hinternet-handles.md) , das von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="06128-172">This function requires an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="06128-173">Mit [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) können auch zusätzliche Header oder optionale Informationen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="06128-173">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) can also send additional headers or optional information.</span></span> <span data-ttu-id="06128-174">Die optionalen Informationen werden im Allgemeinen für Vorgänge verwendet, die Informationen auf dem Server schreiben, z. b. Put und Post.</span><span class="sxs-lookup"><span data-stu-id="06128-174">The optional information is generally used for operations that write information to the server, such as PUT and POST.</span></span>

<span data-ttu-id="06128-175">Nachdem [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) die Anforderung gesendet hat, kann die Anwendung die Funktionen [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)und [**internetsetfilepointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) für das [**hinternethandle**](appendix-a-hinternet-handles.md) verwenden, das von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) erstellt wurde, um die Ressourcen des Servers herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="06128-175">After [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) sends the request, the application can use the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) functions on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) to download the server's resources.</span></span>

### <a name="posting-data-to-the-server"></a><span data-ttu-id="06128-176">Veröffentlichen von Daten auf dem Server</span><span class="sxs-lookup"><span data-stu-id="06128-176">Posting Data to the Server</span></span>

<span data-ttu-id="06128-177">Zum Bereitstellen von Daten auf einem Server muss das HTTP-Verb im [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) -Befehl entweder Post oder Put lauten.</span><span class="sxs-lookup"><span data-stu-id="06128-177">To post data to a server, the HTTP verb in the call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) must be either POST or PUT.</span></span> <span data-ttu-id="06128-178">Die Adresse des Puffers, der die Post-Daten enthält, sollte dann in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)an den *lpoptional* -Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="06128-178">The address of the buffer that contains the POST data should then be passed to the *lpOptional* parameter in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="06128-179">Der Parameter " *dwoptionallength* " sollte auf die Größe der Daten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="06128-179">The *dwOptionalLength* parameter should be set to the size of the data.</span></span>

<span data-ttu-id="06128-180">Sie können auch die [**internetwrite File**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) -Funktion verwenden, um Daten in einem [**hinternethandle**](appendix-a-hinternet-handles.md) zu veröffentlichen, das mit [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="06128-180">You can also use the [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) function to post data on an [**HINTERNET**](appendix-a-hinternet-handles.md) handle sent using [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa).</span></span>

### <a name="getting-information-about-a-request"></a><span data-ttu-id="06128-181">Informationen zu einer Anforderung erhalten</span><span class="sxs-lookup"><span data-stu-id="06128-181">Getting Information About a Request</span></span>

<span data-ttu-id="06128-182">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) ermöglicht einer Anwendung das Abrufen von Informationen zu einer HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="06128-182">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) allows an application to retrieve information about an HTTP request.</span></span> <span data-ttu-id="06128-183">Die Funktion erfordert ein [**hinternethandle**](appendix-a-hinternet-handles.md) , das von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) oder [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), einem Wert auf Informationsebene und einer Pufferlänge erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="06128-183">The function requires an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), an information level value, and a buffer length.</span></span> <span data-ttu-id="06128-184">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) akzeptiert auch einen Puffer, in dem die Informationen gespeichert sind, sowie einen NULL basierten Header Index, der mehrere Header mit demselben Namen auflistet.</span><span class="sxs-lookup"><span data-stu-id="06128-184">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) also accepts a buffer that stores the information and a zero-based header index that enumerates multiple headers with the same name.</span></span>

### <a name="downloading-resources-from-the-www"></a><span data-ttu-id="06128-185">Herunterladen von Ressourcen aus dem www</span><span class="sxs-lookup"><span data-stu-id="06128-185">Downloading Resources from the WWW</span></span>

<span data-ttu-id="06128-186">Nachdem eine Anforderung mit [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) geöffnet und mit [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)an den Server gesendet wurde, kann die Anwendung die Funktionen " [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)", " [**internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)" und " [**internetsetfilepointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) " verwenden, um die Ressource vom HTTP-Server herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="06128-186">After opening a request with [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and sending it to the server with [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), the application can use the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) functions to download the resource from the HTTP server.</span></span>

<span data-ttu-id="06128-187">Im folgenden Beispiel wird eine Ressource heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="06128-187">The following example downloads a resource.</span></span> <span data-ttu-id="06128-188">Die-Funktion akzeptiert das Handle für das aktuelle Fenster, die ID eines Bearbeitungs Felds und ein [**hinternethandle**](appendix-a-hinternet-handles.md) , das von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) erstellt und von [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="06128-188">The function accepts the handle to the current window, the identification number of an edit box, and an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and sent by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="06128-189">Er verwendet [**internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) , um die Größe der Ressource zu ermitteln, und lädt Sie dann mithilfe von " [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)" herunter.</span><span class="sxs-lookup"><span data-stu-id="06128-189">It uses [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) to determine the size of the resource and then downloads it using [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span> <span data-ttu-id="06128-190">Der Inhalt wird dann im Bearbeitungsfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="06128-190">The contents are then displayed in the edit box.</span></span>


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR lpszData;    // buffer for the data
    DWORD  dwSize;       // size of the data available
    DWORD  dwDownloaded; // size of the downloaded data
    DWORD  dwSizeSum=0;  // size of the data in the textbox
    LPTSTR lpszHolding;  // buffer to merge the textbox data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            printf("InternetQueryDataAvailable failed (%d)\n", GetLastError());
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,
                                 (LPVOID)lpszData,
                                 dwSize,
                                 &dwDownloaded))
            {
                printf("InternetReadFile failed (%d)\n", GetLastError());
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the data buffer
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];

                // Check if there has been any data written
                // to the textbox.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the textbox if any
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding,
                                   dwSizeSum);

                    // Add a null terminator at the end of the
                    // textbox data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string.
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + dwDownloaded + 1;
                LPTSTR* ppszDestEnd = 0;
                size_t* pcchRemaining = 0;

                // Add the new data to the holding buffer
                HRESULT hr = StringCchCatEx(lpszHolding,
                                            cchDest,
                                            lpszData,
                                            ppszDestEnd,
                                            pcchRemaining,
                                            STRSAFE_NO_TRUNCATION);

                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the textbox.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to the
                    // textbox data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                        break;
                    else
                    {
                    //  TODO: Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    return TRUE;
}
```



> [!Note]  
> <span data-ttu-id="06128-191">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="06128-191">WinINet does not support server implementations.</span></span> <span data-ttu-id="06128-192">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06128-192">In addition, it should not be used from a service.</span></span> <span data-ttu-id="06128-193">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="06128-193">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 