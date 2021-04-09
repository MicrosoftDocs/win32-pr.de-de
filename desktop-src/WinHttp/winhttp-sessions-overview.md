---
description: Die Microsoft Windows HTTP-Dienste (WinHTTP) machen einen Satz von C/C++-Funktionen verfügbar, die Ihrer Anwendung den Zugriff auf http-Ressourcen im Web ermöglichen. Dieses Thema bietet einen Überblick darüber, wie diese Funktionen für die Interaktion mit einem HTTP-Server verwendet werden.
ms.assetid: 66a1616b-0cf3-45c7-880b-e36728b5a9c4
title: Übersicht über WinHTTP-Sitzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98dc8116dff75f279b87cb5f5ee6af607034176f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129257"
---
# <a name="winhttp-sessions-overview"></a><span data-ttu-id="633ba-104">Übersicht über WinHTTP-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="633ba-104">WinHTTP Sessions Overview</span></span>

<span data-ttu-id="633ba-105">Die Microsoft Windows HTTP-Dienste (WinHTTP) machen einen Satz von C/C++-Funktionen verfügbar, die Ihrer Anwendung den Zugriff auf http-Ressourcen im Web ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="633ba-105">The Microsoft Windows HTTP Services (WinHTTP) exposes a set of C/C++ functions that enable your application to access HTTP resources on the Web.</span></span> <span data-ttu-id="633ba-106">Dieses Thema bietet einen Überblick darüber, wie diese Funktionen für die Interaktion mit einem HTTP-Server verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="633ba-106">This topic provides an overview of how these functions are used to interact with an HTTP server.</span></span>

-   [<span data-ttu-id="633ba-107">Verwenden der WinHTTP-API für den Zugriff auf das Web</span><span class="sxs-lookup"><span data-stu-id="633ba-107">Using the WinHTTP API to Access the Web</span></span>](#using-the-winhttp-api-to-access-the-web)
-   [<span data-ttu-id="633ba-108">Initialisieren von WinHTTP</span><span class="sxs-lookup"><span data-stu-id="633ba-108">Initializing WinHTTP</span></span>](#initializing-winhttp)
-   [<span data-ttu-id="633ba-109">Öffnen einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="633ba-109">Opening a Request</span></span>](#opening-a-request)
-   [<span data-ttu-id="633ba-110">Anforderungs Header werden hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="633ba-110">Adding Request Headers</span></span>](#adding-request-headers)
-   [<span data-ttu-id="633ba-111">Senden einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="633ba-111">Sending a Request</span></span>](#sending-a-request)
-   [<span data-ttu-id="633ba-112">Veröffentlichen von Daten auf dem Server</span><span class="sxs-lookup"><span data-stu-id="633ba-112">Posting Data to the Server</span></span>](#posting-data-to-the-server)
-   [<span data-ttu-id="633ba-113">Informationen zu einer Anforderung erhalten</span><span class="sxs-lookup"><span data-stu-id="633ba-113">Getting Information About a Request</span></span>](#getting-information-about-a-request)
-   [<span data-ttu-id="633ba-114">Herunterladen von Ressourcen aus dem Web</span><span class="sxs-lookup"><span data-stu-id="633ba-114">Downloading Resources from the Web</span></span>](#downloading-resources-from-the-web)

## <a name="using-the-winhttp-api-to-access-the-web"></a><span data-ttu-id="633ba-115">Verwenden der WinHTTP-API für den Zugriff auf das Web</span><span class="sxs-lookup"><span data-stu-id="633ba-115">Using the WinHTTP API to Access the Web</span></span>

<span data-ttu-id="633ba-116">Das folgende Diagramm zeigt die Reihenfolge, in der WinHTTP-Funktionen in der Regel bei der Interaktion mit einem HTTP-Server aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="633ba-116">The following diagram shows the order in which WinHTTP functions are typically called when interacting with an HTTP server.</span></span> <span data-ttu-id="633ba-117">Die schattierten Felder stellen Funktionen dar, die ein [hinternethandle](hinternet-handles-in-winhttp.md) generieren, während die einfachen Felder Funktionen darstellen, die diese Handles verwenden.</span><span class="sxs-lookup"><span data-stu-id="633ba-117">The shaded boxes represent functions that generate an [HINTERNET](hinternet-handles-in-winhttp.md) handle, while the plain boxes represent functions that use those handles.</span></span>

![Funktionen zum Erstellen von Handles](images/art-winhttp3.png)

## <a name="initializing-winhttp"></a><span data-ttu-id="633ba-119">Initialisieren von WinHTTP</span><span class="sxs-lookup"><span data-stu-id="633ba-119">Initializing WinHTTP</span></span>

<span data-ttu-id="633ba-120">Vor der Interaktion mit einem Server muss WinHTTP durch Aufrufen von [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="633ba-120">Before interacting with a server, WinHTTP must be initialized by calling [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen).</span></span> <span data-ttu-id="633ba-121">[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) erstellt einen Sitzungs Kontext, um Details zur HTTP-Sitzung beizubehalten, und gibt ein Sitzungs Handle zurück.</span><span class="sxs-lookup"><span data-stu-id="633ba-121">[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) creates a session context to maintain details about the HTTP session, and returns a session handle.</span></span> <span data-ttu-id="633ba-122">Mithilfe dieses Handles kann die [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) -Funktion einen HTTP-oder Secure Hypertext Transfer Protocol (HTTPS)-Zielserver angeben.</span><span class="sxs-lookup"><span data-stu-id="633ba-122">Using this handle, the [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) function is then able to specify a target HTTP or Secure Hypertext Transfer Protocol (HTTPS) server.</span></span>

> [!Note]  
> <span data-ttu-id="633ba-123">Ein [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) -Aufrufe führt nicht zu einer tatsächlichen Verbindung mit dem HTTP-Server, bis eine Anforderung für eine bestimmte Ressource erfolgt.</span><span class="sxs-lookup"><span data-stu-id="633ba-123">A call to [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) does not result in an actual connection to the HTTP server until a request is made for a specific resource.</span></span>

 

## <a name="opening-a-request"></a><span data-ttu-id="633ba-124">Öffnen einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="633ba-124">Opening a Request</span></span>

<span data-ttu-id="633ba-125">Die [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) -Funktion öffnet eine HTTP-Anforderung für eine bestimmte Ressource und gibt ein [HINTERNET](hinternet-handles-in-winhttp.md) -Handle zurück, das von den anderen HTTP-Funktionen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="633ba-125">The [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function opens an HTTP request for a particular resource and returns an [HINTERNET](hinternet-handles-in-winhttp.md) handle that can be used by the other HTTP functions.</span></span> <span data-ttu-id="633ba-126">[**Winhttpopanrequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) sendet die Anforderung nicht an den Server, wenn Sie aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="633ba-126">[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) does not send the request to the server when called.</span></span> <span data-ttu-id="633ba-127">Die [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) -Funktion stellt tatsächlich eine Verbindung über das Netzwerk her und sendet die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="633ba-127">The [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function actually establishes a connection over the network and sends the request.</span></span>

<span data-ttu-id="633ba-128">Das folgende Beispiel zeigt einen Beispiel Aufrufe von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) , der die Standardoptionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="633ba-128">The following example shows a sample call to [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) that uses the default options.</span></span>

`HINTERNET hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL, NULL, NULL, NULL, 0);`

## <a name="adding-request-headers"></a><span data-ttu-id="633ba-129">Anforderungs Header werden hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="633ba-129">Adding Request Headers</span></span>

<span data-ttu-id="633ba-130">Mit der [**winhttpadressquestheaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) -Funktion kann eine Anwendung zusätzliche freiformat-Anforderungs Header an das HTTP-Anforderungs handle anfügen.</span><span class="sxs-lookup"><span data-stu-id="633ba-130">The [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) function allows an application to append additional free-format request headers to the HTTP request handle.</span></span> <span data-ttu-id="633ba-131">Es ist für die Verwendung durch anspruchsvolle Anwendungen vorgesehen, die eine genaue Kontrolle über die an den HTTP-Server gesendeten Anforderungen erfordern.</span><span class="sxs-lookup"><span data-stu-id="633ba-131">It is intended for use by sophisticated applications that require precise control over the requests sent to the HTTP server.</span></span>

<span data-ttu-id="633ba-132">Die [**winhttpadressquestheaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) -Funktion erfordert ein von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstelltes HTTP-Anforderungs handle, eine Zeichenfolge, die die Header, die Länge der Header und alle Modifizierer enthält.</span><span class="sxs-lookup"><span data-stu-id="633ba-132">The [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) function requires an HTTP request handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), a string that contains the headers, the length of the headers, and any modifiers.</span></span>

<span data-ttu-id="633ba-133">Die folgenden modifiziererer können mit [**winhttpadressquestheaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="633ba-133">The following modifiers can be used with [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span></span>



| <span data-ttu-id="633ba-134">Modifizierer</span><span class="sxs-lookup"><span data-stu-id="633ba-134">Modifier</span></span>                                                                                         | <span data-ttu-id="633ba-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="633ba-135">Description</span></span>                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="633ba-136">**WinHTTP- \_ adressq- \_ Flag \_ Hinzufügen**</span><span class="sxs-lookup"><span data-stu-id="633ba-136">**WINHTTP\_ADDREQ\_FLAG\_ADD**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                       | <span data-ttu-id="633ba-137">Fügt den Header hinzu, wenn er nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="633ba-137">Adds the header if it does not exist.</span></span> <span data-ttu-id="633ba-138">Wird mit dem [**WinHTTP- \_ adressq- \_ Flag \_ ersetzen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)verwendet.</span><span class="sxs-lookup"><span data-stu-id="633ba-138">Used with [**WINHTTP\_ADDREQ\_FLAG\_REPLACE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="633ba-139">**WinHTTP- \_ adressq- \_ Flag \_ Add, \_ Wenn \_ neu**</span><span class="sxs-lookup"><span data-stu-id="633ba-139">**WINHTTP\_ADDREQ\_FLAG\_ADD\_IF\_NEW**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)              | <span data-ttu-id="633ba-140">Fügt den Header nur hinzu, wenn er nicht bereits vorhanden ist. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="633ba-140">Adds the header only if it does not already exist; otherwise, an error is returned.</span></span>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="633ba-141">**WinHTTP- \_ adressq- \_ Flag \_ COALESCE**</span><span class="sxs-lookup"><span data-stu-id="633ba-141">**WINHTTP\_ADDREQ\_FLAG\_COALESCE**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                  | <span data-ttu-id="633ba-142">Führt Header desselben Namens zusammen.</span><span class="sxs-lookup"><span data-stu-id="633ba-142">Merges headers of the same name.</span></span>                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="633ba-143">**WinHTTP- \_ adressq- \_ Flag \_ COALESCE \_ mit \_ Komma**</span><span class="sxs-lookup"><span data-stu-id="633ba-143">**WINHTTP\_ADDREQ\_FLAG\_COALESCE\_WITH\_COMMA**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)     | <span data-ttu-id="633ba-144">Führt mit einem Komma Header desselben Namens zusammen.</span><span class="sxs-lookup"><span data-stu-id="633ba-144">Merges headers of the same name using a comma.</span></span> <span data-ttu-id="633ba-145">Das Hinzufügen von "Accept: Text/ \* " gefolgt von "Accept: Audio/ \* " mit diesem Flag bildet z. b. den einzelnen Header "Accept: Text/ \* , Audio/ \* " und bewirkt, dass der erste Header zusammengeführt wird.</span><span class="sxs-lookup"><span data-stu-id="633ba-145">For example, adding "Accept: text/\*" followed by "Accept: audio/\*" with this flag forms the single header "Accept: text/\*, audio/\*", causing the first header found to be merged.</span></span> <span data-ttu-id="633ba-146">Es liegt an der aufrufenden Anwendung, ein zusammenhängendes Schema in Bezug auf zusammengeführte/separate Header sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="633ba-146">It is up to the calling application to ensure a cohesive scheme with respect to merged/separate headers.</span></span> |
| [<span data-ttu-id="633ba-147">**WinHTTP- \_ adressq- \_ Flag \_ COALESCE \_ mit \_ Semikolon**</span><span class="sxs-lookup"><span data-stu-id="633ba-147">**WINHTTP\_ADDREQ\_FLAG\_COALESCE\_WITH\_SEMICOLON**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) | <span data-ttu-id="633ba-148">Führt mit einem Semikolon Header desselben Namens zusammen.</span><span class="sxs-lookup"><span data-stu-id="633ba-148">Merges headers of the same name using a semicolon.</span></span>                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="633ba-149">**WinHTTP- \_ adressq- \_ Flag \_ ersetzen**</span><span class="sxs-lookup"><span data-stu-id="633ba-149">**WINHTTP\_ADDREQ\_FLAG\_REPLACE**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                   | <span data-ttu-id="633ba-150">Ersetzt oder entfernt einen Header.</span><span class="sxs-lookup"><span data-stu-id="633ba-150">Replaces or removes a header.</span></span> <span data-ttu-id="633ba-151">Wenn der Header Wert leer ist und der Header gefunden wird, wird er entfernt.</span><span class="sxs-lookup"><span data-stu-id="633ba-151">If the header value is empty and the header is found, it is removed.</span></span> <span data-ttu-id="633ba-152">Wenn der Header Wert nicht leer ist, wird der Header Wert ersetzt.</span><span class="sxs-lookup"><span data-stu-id="633ba-152">If the header value is not empty, the header value is replaced.</span></span>                                                                                                                                                                            |



 

## <a name="sending-a-request"></a><span data-ttu-id="633ba-153">Senden einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="633ba-153">Sending a Request</span></span>

<span data-ttu-id="633ba-154">Die [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) -Funktion stellt eine Verbindung mit dem Server her und sendet die Anforderung an die angegebene Site.</span><span class="sxs-lookup"><span data-stu-id="633ba-154">The [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function establishes a connection to the server and sends the request to the specified site.</span></span> <span data-ttu-id="633ba-155">Diese Funktion erfordert ein [hinternethandle](hinternet-handles-in-winhttp.md) , das von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="633ba-155">This function requires an [HINTERNET](hinternet-handles-in-winhttp.md) handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span></span> <span data-ttu-id="633ba-156">[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) kann auch zusätzliche Header oder optionale Informationen senden.</span><span class="sxs-lookup"><span data-stu-id="633ba-156">[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) can also send additional headers or optional information.</span></span> <span data-ttu-id="633ba-157">Die optionalen Informationen werden im Allgemeinen für Vorgänge verwendet, die Informationen auf dem Server schreiben, z. b. Put und Post.</span><span class="sxs-lookup"><span data-stu-id="633ba-157">The optional information is generally used for operations that write information to the server, such as PUT and POST.</span></span>

<span data-ttu-id="633ba-158">Nachdem die Funktion " [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) " die Anforderung gesendet hat, kann die Anwendung die Funktionen " [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) " und " [**winhttpquerydataavailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) " im [HINTERNET](hinternet-handles-in-winhttp.md) -Handle verwenden, um die Ressourcen des Servers herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="633ba-158">After the [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function sends the request, the application can use the [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) and [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) functions on the [HINTERNET](hinternet-handles-in-winhttp.md) handle to download the server's resources.</span></span>

## <a name="posting-data-to-the-server"></a><span data-ttu-id="633ba-159">Veröffentlichen von Daten auf dem Server</span><span class="sxs-lookup"><span data-stu-id="633ba-159">Posting Data to the Server</span></span>

<span data-ttu-id="633ba-160">Zum Bereitstellen von Daten auf einem Server muss das [*http-Verb*](glossary.md) im [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) -Befehl entweder Post oder Put lauten.</span><span class="sxs-lookup"><span data-stu-id="633ba-160">To post data to a server, the [*HTTP verb*](glossary.md) in the call to [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) must be either POST or PUT.</span></span> <span data-ttu-id="633ba-161">Wenn " [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) " aufgerufen wird, sollte der Parameter " *dwtotallength* " auf die Größe der Daten in Byte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="633ba-161">When [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) is called, the *dwTotalLength* parameter should be set to the size of the data in bytes.</span></span> <span data-ttu-id="633ba-162">Verwenden Sie dann [**winhttpschreitedata**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) , um die Daten an den Server zu senden.</span><span class="sxs-lookup"><span data-stu-id="633ba-162">Then use [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) to post the data to the server.</span></span>

<span data-ttu-id="633ba-163">Alternativ können Sie den *lpoptional* -Parameter von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) auf die Adresse eines Puffers festlegen, der Daten enthält, die an den Server gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="633ba-163">Alternatively, set the *lpOptional* parameter of [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) to the address of a buffer that contains data to post to the server.</span></span> <span data-ttu-id="633ba-164">Wenn Sie dieses Verfahren verwenden, müssen Sie die Parameter " *dwoptionallength* " und " *dwtotallength* " von " [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) " auf die Größe der Daten festlegen, die gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="633ba-164">When using this technique, you must set both the *dwOptionalLength* and *dwTotalLength* parameters of [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) to be the size of the data being posted.</span></span> <span data-ttu-id="633ba-165">Wenn Sie [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) auf diese Weise aufrufen, entfällt die Notwendigkeit, [**winhttpschreitedata**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="633ba-165">Calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) in this manner eliminates the need to call [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata).</span></span>

## <a name="getting-information-about-a-request"></a><span data-ttu-id="633ba-166">Informationen zu einer Anforderung erhalten</span><span class="sxs-lookup"><span data-stu-id="633ba-166">Getting Information About a Request</span></span>

<span data-ttu-id="633ba-167">Die Funktion [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) ermöglicht einer Anwendung das Abrufen von Informationen zu einer HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="633ba-167">The [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) function allows an application to retrieve information about an HTTP request.</span></span> <span data-ttu-id="633ba-168">Die Funktion erfordert ein [hinternethandle](hinternet-handles-in-winhttp.md) , das von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), einem Wert auf Informationsebene und einer Pufferlänge erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="633ba-168">The function requires an [HINTERNET](hinternet-handles-in-winhttp.md) handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), an information level value, and a buffer length.</span></span> <span data-ttu-id="633ba-169">[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) akzeptiert auch einen Puffer, in dem die Informationen gespeichert sind, sowie einen NULL basierten Header Index, der mehrere Header mit demselben Namen auflistet.</span><span class="sxs-lookup"><span data-stu-id="633ba-169">[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) also accepts a buffer that stores the information and a zero-based header index that enumerates multiple headers with the same name.</span></span>

<span data-ttu-id="633ba-170">Verwenden Sie einen der auf der Seite [**abfrageinfoflags**](query-info-flags.md) gefundenen Werte auf Informationsebene mit einem-Modifizierer, um das Format zu steuern, in dem die Informationen im *lpvbuffer* -Parameter von [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="633ba-170">Use any of the information level values found on the [**Query Info Flags**](query-info-flags.md) page with a modifier to control the format in which the information is stored in the *lpvBuffer* parameter of [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

## <a name="downloading-resources-from-the-web"></a><span data-ttu-id="633ba-171">Herunterladen von Ressourcen aus dem Web</span><span class="sxs-lookup"><span data-stu-id="633ba-171">Downloading Resources from the Web</span></span>

<span data-ttu-id="633ba-172">Nachdem Sie eine Anforderung mit der [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) -Funktion geöffnet, Sie mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)an den Server gesendet und das Anforderungs Handle für den Empfang einer Antwort mit [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)vorbereitet haben, kann die Anwendung die Funktionen [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) und [**winhttpquerydataavailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) zum Herunterladen der Ressource vom HTTP-Server verwenden.</span><span class="sxs-lookup"><span data-stu-id="633ba-172">After opening a request with the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function, sending it to the server with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), and preparing the request handle to receive a response with [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse), the application can use the [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) and [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) functions to download the resource from the HTTP server.</span></span>

<span data-ttu-id="633ba-173">Der folgende Beispielcode zeigt, wie Sie eine Ressource mit einer sicheren Transaktions Semantik herunterladen.</span><span class="sxs-lookup"><span data-stu-id="633ba-173">The following sample code shows how to download a resource with secure transaction semantics.</span></span> <span data-ttu-id="633ba-174">Der Beispielcode initialisiert die WinHTTP-API (Application Programming Interface), wählt einen HTTPS-Zielserver aus und öffnet dann eine Anforderung für diese sichere Ressource.</span><span class="sxs-lookup"><span data-stu-id="633ba-174">The sample code initializes the WinHTTP application programming interface (API), selects a target HTTPS server, and then opens and sends a request for this secure resource.</span></span> <span data-ttu-id="633ba-175">[**Winhttpquerydataavailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) wird mit dem Anforderungs Handle verwendet, um zu bestimmen, wie viele Daten heruntergeladen werden können, und anschließend wird [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) verwendet, um diese Daten zu lesen.</span><span class="sxs-lookup"><span data-stu-id="633ba-175">[**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) is used with the request handle to determine how much data is available for download, and then [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) is used to read that data.</span></span> <span data-ttu-id="633ba-176">Dieser Vorgang wird wiederholt, bis das gesamte Dokument abgerufen und angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="633ba-176">This process is repeated until the entire document has been retrieved and displayed.</span></span>


```C++
  DWORD dwSize = 0;
  DWORD dwDownloaded = 0;
  LPSTR pszOutBuffer;
  BOOL  bResults = FALSE;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, L"www.microsoft.com",
                               INTERNET_DEFAULT_HTTPS_PORT, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL,
                                   NULL, WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES, 
                                   WINHTTP_FLAG_SECURE );

  // Send a request.
  if( hRequest )
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS, 0,
                                   WINHTTP_NO_REQUEST_DATA, 0, 
                                   0, 0 );


  // End the request.
  if( bResults )
    bResults = WinHttpReceiveResponse( hRequest, NULL );

  // Keep checking for data until there is nothing left.
  if( bResults )
  {
    do 
    {
      // Check for available data.
      dwSize = 0;
      if( !WinHttpQueryDataAvailable( hRequest, &dwSize ) )
        printf( "Error %u in WinHttpQueryDataAvailable.\n",
                GetLastError( ) );

      // Allocate space for the buffer.
      pszOutBuffer = new char[dwSize+1];
      if( !pszOutBuffer )
      {
        printf( "Out of memory\n" );
        dwSize=0;
      }
      else
      {
        // Read the data.
        ZeroMemory( pszOutBuffer, dwSize+1 );

        if( !WinHttpReadData( hRequest, (LPVOID)pszOutBuffer, 
                              dwSize, &dwDownloaded ) )
          printf( "Error %u in WinHttpReadData.\n", GetLastError( ) );
        else
          printf( "%s", pszOutBuffer );

        // Free the memory allocated to the buffer.
        delete [] pszOutBuffer;
      }
    } while( dwSize > 0 );
  }


  // Report any errors.
  if( !bResults )
    printf( "Error %d has occurred.\n", GetLastError( ) );

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
```



 

 



