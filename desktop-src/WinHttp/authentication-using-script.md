---
description: In diesem Abschnitt wird veranschaulicht, wie Sie ein Skript schreiben, das das WinHttpRequest-Objekt verwendet, um auf Daten von einem Server zuzugreifen, für den HTTP-Authentifizierung
ms.assetid: 9e46777c-4d79-4f9b-9b31-1280ed1e3289
title: Authentifizierung mithilfe eines Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1d33b8042cd1fd15d46e15dfb3624e0d3b4a885b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358484"
---
# <a name="authentication-using-script"></a><span data-ttu-id="9234e-103">Authentifizierung mithilfe eines Skripts</span><span class="sxs-lookup"><span data-stu-id="9234e-103">Authentication Using Script</span></span>

<span data-ttu-id="9234e-104">In diesem Abschnitt wird veranschaulicht, wie Sie ein Skript schreiben, das das [**WinHttpRequest**](winhttprequest.md) -Objekt verwendet, um auf Daten von einem Server zuzugreifen, für den HTTP-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="9234e-104">This section demonstrates how to write script that uses the [**WinHttpRequest**](winhttprequest.md) object to access data from a server that requires HTTP authentication.</span></span>

-   [<span data-ttu-id="9234e-105">Voraussetzungen und Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9234e-105">Prerequisites and Requirements</span></span>](#prerequisites-and-requirements)
-   [<span data-ttu-id="9234e-106">Zugreifen auf eine Website mit Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="9234e-106">Accessing a Web Site With Authentication</span></span>](#accessing-a-web-site-with-authentication)
-   [<span data-ttu-id="9234e-107">Überprüfen der Status Codes</span><span class="sxs-lookup"><span data-stu-id="9234e-107">Checking the Status Codes</span></span>](#checking-the-status-codes)
-   [<span data-ttu-id="9234e-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9234e-108">Related topics</span></span>](#related-topics)

## <a name="prerequisites-and-requirements"></a><span data-ttu-id="9234e-109">Voraussetzungen und Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9234e-109">Prerequisites and Requirements</span></span>

<span data-ttu-id="9234e-110">Zusätzlich zu den in Microsoft JScript funktionierenden Kenntnissen erfordert dieses Beispiel Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9234e-110">In addition to a working knowledge of Microsoft JScript, this example requires the following:</span></span>

-   <span data-ttu-id="9234e-111">Die aktuelle Version des Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="9234e-111">The current version of the Microsoft Windows Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="9234e-112">Das Proxy Konfigurationstool zum Einrichten der Proxy Einstellungen für Microsoft Windows HTTP-Dienste (WinHTTP), wenn die Internetverbindung über einen Proxy Server erfolgt.</span><span class="sxs-lookup"><span data-stu-id="9234e-112">The proxy configuration tool to establish the proxy settings for Microsoft Windows HTTP Services (WinHTTP), if your connection to the Internet is through a proxy server.</span></span> <span data-ttu-id="9234e-113">Weitere Informationen finden Sie [ unterProxycfg.exe, einem Proxy Konfigurations Tool](proxycfg-exe--a-proxy-configuration-tool.md) .</span><span class="sxs-lookup"><span data-stu-id="9234e-113">See [Proxycfg.exe, a Proxy Configuration Tool](proxycfg-exe--a-proxy-configuration-tool.md) for more information.</span></span>
-   <span data-ttu-id="9234e-114">Eine Vertrautheit mit der [Netzwerkterminologie](network-terminology.md) und den Konzepten.</span><span class="sxs-lookup"><span data-stu-id="9234e-114">A familiarity with [network terminology](network-terminology.md) and concepts.</span></span>

## <a name="accessing-a-web-site-with-authentication"></a><span data-ttu-id="9234e-115">Zugreifen auf eine Website mit Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="9234e-115">Accessing a Web Site With Authentication</span></span>

<span data-ttu-id="9234e-116">**Gehen Sie folgendermaßen vor, um ein Skript zu erstellen, das die Authentifizierung veranschaulicht:**</span><span class="sxs-lookup"><span data-stu-id="9234e-116">**To create a script that demonstrates authentication, do the following:**</span></span>

1.  <span data-ttu-id="9234e-117">Öffnen Sie einen Text-Editor, z. b. Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="9234e-117">Open a text editor such as Microsoft Notepad.</span></span>
2.  <span data-ttu-id="9234e-118">Kopieren Sie den folgenden Code in den Text-Editor \[ , nachdem Sie "authenticationsite \] " durch den entsprechenden Text ersetzt haben, um die URL einer Website anzugeben, die die HTTP-Authentifizierung erfordert.</span><span class="sxs-lookup"><span data-stu-id="9234e-118">Copy the following code into the text editor after replacing "\[authenticationSite\]" with the appropriate text to specify the URL of a site that requires HTTP authentication.</span></span>

    ```VB
    // Load the WinHttpRequest object.
    var WinHttpReq = 
              new ActiveXObject("WinHttp.WinHttpRequest.5.1");

    function getText1( )
    {
      // Specify the target resource.
      WinHttpReq.open( "GET", 
                       "https://[authenticationSite]", 
                       false;

      // Send a request to the server and wait for a response.
      WinHttpReq.send( );

      // Display the results of the request.
      WScript.Echo( "No Credentials: " );
      WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText);
      WScript.Echo( WinHttpReq.GetAllResponseHeaders);
      WScript.Echo( );
    };

    function getText2( )
    {
      // HttpRequest SetCredentials flags
      HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;

      // Specify the target resource.
      WinHttpReq.open( "GET", 
                       "https://[authenticationSite]", 
                       false );

      // Set credentials for server.
      WinHttpReq.SetCredentials( "User Name", 
                                 "Password",
                                 HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);

      // It might also be necessary to supply credentials 
      // to the proxy if you connect to the Internet 
      // through a proxy that requires authentication.

      // Send a request to the server and wait for 
      // a response.
      WinHttpReq.send( );

      // Display the results of the request.
      WScript.Echo( "Credentials: " );
      WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText );
      WScript.Echo( WinHttpReq.GetAllResponseHeaders( ) );
      WScript.Echo( );
    };

    getText1( );
    getText2( );
    ```

    

3.  <span data-ttu-id="9234e-119">Speichern Sie die Datei als "Auth.js".</span><span class="sxs-lookup"><span data-stu-id="9234e-119">Save the file as "Auth.js".</span></span>
4.  <span data-ttu-id="9234e-120">Geben Sie an einer Eingabeaufforderung "Cscript Auth.js" ein, und drücken Sie die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="9234e-120">From a command prompt, type "cscript Auth.js" and press ENTER.</span></span>

<span data-ttu-id="9234e-121">Sie verfügen jetzt über ein Programm, das eine Ressource auf zwei verschiedene Arten anfordert.</span><span class="sxs-lookup"><span data-stu-id="9234e-121">You now have a program that requests a resource two different ways.</span></span> <span data-ttu-id="9234e-122">Die erste Methode fordert die Ressource ohne Angabe von Anmelde Informationen an.</span><span class="sxs-lookup"><span data-stu-id="9234e-122">The first method requests the resource without supplying credentials.</span></span> <span data-ttu-id="9234e-123">Der Statuscode 401 wird zurückgegeben, um anzugeben, dass für den Server eine Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9234e-123">A 401 status code is returned to indicate that the server requires authentication.</span></span> <span data-ttu-id="9234e-124">Die Antwortheader werden ebenfalls angezeigt und sollten in etwa wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="9234e-124">The response headers are also displayed and should look similar to the following:</span></span>

``` syntax
Connection: Keep-Alive
Content-Length: 0
Date: Fri, 27 Apr 2001 01:47:18 GMT
Content-Type: text/html
Server: Microsoft-IIS/5.0
WWW-Authenticate: NTLM
WWW-Authenticate: Negotiate
Cache-control: private
```

<span data-ttu-id="9234e-125">Obwohl die Antwort anzeigt, dass der Zugriff auf die Ressource verweigert wurde, gibt Sie weiterhin mehrere Header zurück, die einige Informationen über die Ressource bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9234e-125">Although the response indicates that access to the resource was denied, it still returns several headers that provide some information about the resource.</span></span> <span data-ttu-id="9234e-126">Der Header mit dem Namen "www-Authenticate" gibt an, dass der Server eine Authentifizierung für diese Ressource erfordert.</span><span class="sxs-lookup"><span data-stu-id="9234e-126">The header named "WWW-Authenticate" indicates that the server requires authentication for this resource.</span></span> <span data-ttu-id="9234e-127">Wenn ein Header mit dem Namen "Proxy-Authenticate" vorhanden ist, weist dies darauf hin, dass für den Proxy Server eine Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9234e-127">If there was a header named "Proxy-Authenticate", it would indicate that the proxy server requires authentication.</span></span> <span data-ttu-id="9234e-128">Jeder authentifizieren-Header enthält ein verfügbares Authentifizierungsschema und manchmal einen Bereich.</span><span class="sxs-lookup"><span data-stu-id="9234e-128">Each authenticate header contains an available authentication scheme and sometimes a realm.</span></span> <span data-ttu-id="9234e-129">Beim Bereichs Wert wird die Groß-/Kleinschreibung beachtet, und es wird eine Gruppe von Servern oder Proxys definiert, für die dieselben Anmelde Informationen akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="9234e-129">The realm value is case-sensitive and defines a set of servers or proxies for which the same credentials should be accepted.</span></span>

<span data-ttu-id="9234e-130">Es gibt zwei Header mit dem Namen "www-Authenticate", die angeben, dass mehrere Authentifizierungs Schemas unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9234e-130">There are two headers named "WWW-Authenticate", which indicate that multiple authentication schemes are supported.</span></span> <span data-ttu-id="9234e-131">Wenn Sie die [**getrespontsheader**](iwinhttprequest-getresponseheader.md) -Methode für die Suche nach "www-Authenticate"-Headern aufzurufen, gibt die Methode nur den Inhalt des ersten Headers dieses Namens zurück.</span><span class="sxs-lookup"><span data-stu-id="9234e-131">If you call the [**GetResponseHeader**](iwinhttprequest-getresponseheader.md) method to find "WWW-Authenticate" headers, the method only returns the contents of the first header of that name.</span></span> <span data-ttu-id="9234e-132">In diesem Fall wird der Wert "NTLM" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9234e-132">In this case, it returns a value of "NTLM".</span></span> <span data-ttu-id="9234e-133">Um sicherzustellen, dass alle Vorkommen eines Headers verarbeitet werden, verwenden Sie stattdessen die [**getallresponsheaders**](iwinhttprequest-getallresponseheaders.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9234e-133">To ensure that all occurrences of a header are processed, use the [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) method instead.</span></span>

<span data-ttu-id="9234e-134">Der zweite Methodenaufruf fordert dieselbe Ressource an, gibt jedoch zuerst Anmelde Informationen für die Authentifizierung an, indem die [**setanmelde**](iwinhttprequest-setcredentials.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9234e-134">The second method call requests the same resource, but first supplies authentication credentials by calling the [**SetCredentials**](iwinhttprequest-setcredentials.md) method.</span></span> <span data-ttu-id="9234e-135">Der folgende Code Abschnitt zeigt, wie diese Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9234e-135">The following section of code shows how this method is used.</span></span>


```VB
WinHttpReq.SetCredentials( "User Name", "Password",
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
```



<span data-ttu-id="9234e-136">Mit dieser Methode wird der Benutzername auf "username" und das Kennwort auf "Password" festgelegt, und es wird angegeben, dass die Anmelde Informationen für die Autorisierung für den Ressourcen Server gelten</span><span class="sxs-lookup"><span data-stu-id="9234e-136">This method sets the user name to "UserName", the password to "Password", and indicates that the authorization credentials apply to the resource server.</span></span> <span data-ttu-id="9234e-137">Anmelde Informationen für die Authentifizierung können auch an einen Proxy gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9234e-137">Authentication credentials can also be sent to a proxy.</span></span>

<span data-ttu-id="9234e-138">Wenn Anmelde Informationen angegeben werden, gibt der Server den Statuscode 200 zurück, der angibt, dass das Dokument abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="9234e-138">When credentials are supplied, the server returns a 200 status code that indicates that the document can be retrieved.</span></span>

## <a name="checking-the-status-codes"></a><span data-ttu-id="9234e-139">Überprüfen der Status Codes</span><span class="sxs-lookup"><span data-stu-id="9234e-139">Checking the Status Codes</span></span>

<span data-ttu-id="9234e-140">Das vorherige Beispiel ist Anweisungs basiert, erfordert jedoch, dass der Benutzer explizit Anmelde Informationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9234e-140">The previous example is instructional, but it requires that the user explicitly supply credentials.</span></span> <span data-ttu-id="9234e-141">Eine Anwendung, die Anmelde Informationen bei Bedarf bereitstellt und keine Anmelde Informationen bereitstellt, wenn dies nicht erforderlich ist, ist nützlicher.</span><span class="sxs-lookup"><span data-stu-id="9234e-141">An application that supplies credentials when it is necessary and does not supply credentials when it is not necessary is more useful.</span></span> <span data-ttu-id="9234e-142">Zum Implementieren eines Features, das dies bewirkt, müssen Sie das Beispiel ändern, um den mit der Antwort zurückgegebenen Statuscode zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="9234e-142">To implement a feature that does this, you must modify your example to examine the status code returned with the response.</span></span>

<span data-ttu-id="9234e-143">Eine umfassende Liste der möglichen Statuscodes sowie Beschreibungen finden Sie unter http- [**Statuscodes**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9234e-143">For a complete list of possible status codes, along with descriptions, see [**HTTP Status Codes**](http-status-codes.md).</span></span> <span data-ttu-id="9234e-144">In diesem Beispiel sollten Sie jedoch nur einen von drei Codes sehen.</span><span class="sxs-lookup"><span data-stu-id="9234e-144">For this example, however, you should encounter only one of three codes.</span></span> <span data-ttu-id="9234e-145">Der Statuscode 200 zeigt an, dass eine Ressource verfügbar ist und mit der Antwort gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="9234e-145">A status code of 200 indicates that a resource is available and is being sent with the response.</span></span> <span data-ttu-id="9234e-146">Der Statuscode 401 zeigt an, dass für den Server eine Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9234e-146">A status code of 401 indicates that the server requires authentication.</span></span> <span data-ttu-id="9234e-147">Der Statuscode 407 zeigt an, dass für den Proxy eine Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9234e-147">A status code of 407 indicates that the proxy requires authentication.</span></span>

<span data-ttu-id="9234e-148">Ändern Sie das Beispiel, das Sie im letzten Abschnitt erstellt haben, indem Sie die Funktion "getText2" durch den folgenden Code ersetzen (ersetzen \[ Sie "authenticationsite \] " durch ihren eigenen Text, und geben Sie die URL einer Website an, die die HTTP-Authentifizierung erfordert):</span><span class="sxs-lookup"><span data-stu-id="9234e-148">Modify the example you created in the last section by replacing the "getText2" function with the following code (replace "\[authenticationSite\]" with your own text to specifies the URL of a site that requires HTTP authentication):</span></span>


```VB
function getText2() {
  WScript.Echo( "Credentials: " );

  // HttpRequest SetCredentials flags.
  HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;
  HTTPREQUEST_SETCREDENTIALS_FOR_PROXY = 1;

  // Specify the target resource.
  var targURL = "https://[authenticationSite]";
  WinHttpReq.open( "GET", targURL, false );

  var Done = false;
  var Attempts = 0;
  do
  {
    // Keep track of the number of request attempts.
    Attempts++;

    // Send a request to the server and wait for a response.
    WinHttpReq.send( );

    // Obtain the status code from the response.
    var Status = WinHttpReq.Status;

    switch (Status)
    {
      // A 200 status indicates that the resource was retrieved.
      case 200:
        Done = true;
        break;

      // A 401 status indicates that the server 
      // requires authentication.
      case 401:
        WScript.Echo( "Requires Server UserName and Password." );

        // Specify the target resource.
        WinHttpReq.open( "GET", targURL, false );

        // Set credentials for the server.
        WinHttpReq.SetCredentials( "User Name", 
                             "Password",
                              HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
        break;

      // A 407 status indicates that the proxy 
      // requires authentication.
      case 407:
        WScript.Echo( "Requires Proxy UserName and Password." );

        // Specify the target resource.
        WinHttpReq.open( "GET", targURL, false );

        // Set credentials for the proxy.
        WinHttpReq.SetCredentials( "User Name", 
                              "Password",
                              HTTPREQUEST_SETCREDENTIALS_FOR_PROXY );
        break;
    }
  } while( ( !Done ) && ( Attempts < 3 ) );

  // Display the results of the request.
  WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText );
  WScript.Echo( WinHttpReq.GetAllResponseHeaders( ) );
  WScript.Echo( );
};
```



<span data-ttu-id="9234e-149">Speichern Sie die Datei erneut, und führen Sie Sie aus.</span><span class="sxs-lookup"><span data-stu-id="9234e-149">Again, save and run the file.</span></span> <span data-ttu-id="9234e-150">Die zweite Methode ruft das Dokument weiterhin ab, stellt jedoch nur bei Bedarf Anmelde Informationen bereit.</span><span class="sxs-lookup"><span data-stu-id="9234e-150">The second method still retrieves the document, but it only provides credentials when required.</span></span> <span data-ttu-id="9234e-151">Die Funktion "getText2" führt die [**Open**](iwinhttprequest-open.md) -Methode und die [**Send**](iwinhttprequest-send.md) -Methode aus, als wäre keine Authentifizierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9234e-151">The "getText2" function executes the [**Open**](iwinhttprequest-open.md) and [**Send**](iwinhttprequest-send.md) methods as if authentication was not required.</span></span> <span data-ttu-id="9234e-152">Der Status wird mit der [**Status**](iwinhttprequest-status.md) -Eigenschaft abgerufen, und eine Switch-Anweisung antwortet auf den resultierenden Statuscode.</span><span class="sxs-lookup"><span data-stu-id="9234e-152">The status is retrieved with the [**Status**](iwinhttprequest-status.md) property and a switch statement responds to the resulting status code.</span></span> <span data-ttu-id="9234e-153">Wenn der Status 401 (Server erfordert Authentifizierung) oder 407 (Proxy erfordert Authentifizierung) lautet, wird die [**Open**](iwinhttprequest-open.md) -Methode erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9234e-153">If the status is 401 (server requires authentication) or 407 (proxy requires authentication), the [**Open**](iwinhttprequest-open.md) method is executed again.</span></span> <span data-ttu-id="9234e-154">Danach folgt die [**setanmelde**](iwinhttprequest-setcredentials.md) -Methode, mit der der Benutzername und das Kennwort festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9234e-154">This is followed by the [**SetCredentials**](iwinhttprequest-setcredentials.md) method, which sets the user name and password.</span></span> <span data-ttu-id="9234e-155">Der Code wird dann zurück zur [**Send**](iwinhttprequest-send.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9234e-155">The code then loops back to the [**Send**](iwinhttprequest-send.md) method.</span></span> <span data-ttu-id="9234e-156">Wenn die Ressource nach drei versuchen nicht erfolgreich abgerufen werden kann, wird die Ausführung beendet.</span><span class="sxs-lookup"><span data-stu-id="9234e-156">If, after three attempts, the resource cannot be successfully retrieved, then the function stops execution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9234e-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9234e-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9234e-158">Authentifizierung in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="9234e-158">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="9234e-159">WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="9234e-159">WinHttpRequest</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="9234e-160">**SetCredentials**</span><span class="sxs-lookup"><span data-stu-id="9234e-160">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)
</dt> <dt>

[<span data-ttu-id="9234e-161">HTTP/1.1-Anforderung für Kommentare (RFC 2616)</span><span class="sxs-lookup"><span data-stu-id="9234e-161">HTTP/1.1 Request for Comments (RFC 2616)</span></span>](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



