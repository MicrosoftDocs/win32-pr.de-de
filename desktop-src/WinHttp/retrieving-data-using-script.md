---
description: Dieses Thema enthält ein Beispiel für das Schreiben eines Skripts, mit dem Daten über Microsoft Windows HTTP-Dienste (WinHTTP) entweder synchron oder asynchron abgerufen werden.
ms.assetid: 84b847f8-4d9e-4fea-9e87-df4c65b54a02
title: Abrufen von Daten mithilfe eines Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734516cf75f92cc43ab4cb15f22bd97aa803ec33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958669"
---
# <a name="retrieving-data-using-script"></a><span data-ttu-id="54549-103">Abrufen von Daten mithilfe eines Skripts</span><span class="sxs-lookup"><span data-stu-id="54549-103">Retrieving Data Using Script</span></span>

<span data-ttu-id="54549-104">Dieses Thema enthält ein Beispiel für das Schreiben eines Skripts, mit dem Daten über Microsoft Windows HTTP-Dienste (WinHTTP) entweder synchron oder asynchron abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="54549-104">This topic includes an example of how to write a script that obtains data through Microsoft Windows HTTP Services (WinHTTP) either synchronously or asynchronously.</span></span> <span data-ttu-id="54549-105">Die in diesem Beispiel dargestellten Konzepte stellen die Grundlage für das Schreiben von Client-oder Server Anwendungen mittlerer Ebene dar, die über das HTTP-Protokoll Zugriff auf Daten benötigen.</span><span class="sxs-lookup"><span data-stu-id="54549-105">The concepts demonstrated in this example provide the basis for writing client or middle-tier server applications that require access to data using the HTTP protocol.</span></span>

-   [<span data-ttu-id="54549-106">Voraussetzungen und Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54549-106">Prerequisites and Requirements</span></span>](#prerequisites-and-requirements)
-   [<span data-ttu-id="54549-107">Synchrones Abrufen von Daten</span><span class="sxs-lookup"><span data-stu-id="54549-107">Retrieving Data Synchronously</span></span>](#retrieving-data-synchronously)
-   [<span data-ttu-id="54549-108">Asynchrones Abrufen von Daten</span><span class="sxs-lookup"><span data-stu-id="54549-108">Retrieving Data Asynchronously</span></span>](#retrieving-data-asynchronously)
-   [<span data-ttu-id="54549-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="54549-109">Related topics</span></span>](#related-topics)

## <a name="prerequisites-and-requirements"></a><span data-ttu-id="54549-110">Voraussetzungen und Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54549-110">Prerequisites and Requirements</span></span>

<span data-ttu-id="54549-111">Zusätzlich zu den in Microsoft JScript funktionierenden Kenntnissen erfordert dieses Beispiel Folgendes:</span><span class="sxs-lookup"><span data-stu-id="54549-111">In addition to a working knowledge of Microsoft JScript, this example requires the following:</span></span>

-   <span data-ttu-id="54549-112">Die aktuelle Version des Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="54549-112">The current version of the Microsoft Windows Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="54549-113">Das Proxy Konfigurationstool zum Einrichten der Proxy Einstellungen für Microsoft Windows HTTP-Dienste (WinHTTP), wenn die Internetverbindung über einen Proxy Server erfolgt.</span><span class="sxs-lookup"><span data-stu-id="54549-113">The proxy configuration tool to establish the proxy settings for Microsoft Windows HTTP Services (WinHTTP), if your connection to the Internet is through a proxy server.</span></span> <span data-ttu-id="54549-114">Weitere Informationen finden Sie unter [ProxyCfg.exe, einem Proxy Konfigurations Tool](proxycfg-exe--a-proxy-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="54549-114">For more information, see [ProxyCfg.exe, a Proxy Configuration Tool](proxycfg-exe--a-proxy-configuration-tool.md).</span></span>
-   <span data-ttu-id="54549-115">Eine Vertrautheit mit der [Netzwerkterminologie](network-terminology.md) und den Konzepten.</span><span class="sxs-lookup"><span data-stu-id="54549-115">A familiarity with [network terminology](network-terminology.md) and concepts.</span></span>

## <a name="retrieving-data-synchronously"></a><span data-ttu-id="54549-116">Synchrones Abrufen von Daten</span><span class="sxs-lookup"><span data-stu-id="54549-116">Retrieving Data Synchronously</span></span>

<span data-ttu-id="54549-117">**Gehen Sie folgendermaßen vor, um ein Skript zu erstellen, mit dem der Text von einer Webseite synchron abgerufen wird:**</span><span class="sxs-lookup"><span data-stu-id="54549-117">**To create a script that obtains the text from a Web page synchronously, do the following:**</span></span>

1.  <span data-ttu-id="54549-118">Öffnen Sie einen Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="54549-118">Open a text editor.</span></span>
2.  <span data-ttu-id="54549-119">Kopieren Sie den folgenden Code in den Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="54549-119">Copy the following code into the text editor.</span></span>

    ```JScript
    function getText(strURL)
    {
        var strResult;
        
        try
        {
            // Create the WinHTTPRequest ActiveX Object.
            var WinHttpReq = new ActiveXObject(
                                      "WinHttp.WinHttpRequest.5.1");
            
            //  Create an HTTP request.
            var temp = WinHttpReq.Open("GET", strURL, false);

            //  Send the HTTP request.
            WinHttpReq.Send();
            
            //  Retrieve the response text.
            strResult = WinHttpReq.ResponseText;
        }
        catch (objError)
        {
            strResult = objError + "\n"
            strResult += "WinHTTP returned error: " + 
                (objError.number & 0xFFFF).toString() + "\n\n";
            strResult += objError.description;
        }
        
        //  Return the response text.
        return strResult;
    }

    WScript.Echo(getText("https://www.microsoft.com/default.htm"));
    ```

    

3.  <span data-ttu-id="54549-120">Speichern Sie die Datei als "Retrieve.js".</span><span class="sxs-lookup"><span data-stu-id="54549-120">Save the file as "Retrieve.js".</span></span>
4.  <span data-ttu-id="54549-121">Geben Sie an einer Eingabeaufforderung "Cscript Retrieve.js" ein, und drücken Sie die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="54549-121">From a command prompt, type "cscript Retrieve.js" and press ENTER.</span></span>

<span data-ttu-id="54549-122">Sie verfügen jetzt über ein Skript, das ein [**WinHttpRequest**](winhttprequest.md) -Objekt verwendet, um den HTML-Quellcode für die Webseite unter zu erhalten https://www.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="54549-122">You now have a script that uses a [**WinHttpRequest**](winhttprequest.md) object to obtain the HTML source code for the Web page at https://www.microsoft.com.</span></span> <span data-ttu-id="54549-123">Möglicherweise müssen Sie einige Sekunden warten, bis der Code angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="54549-123">You might have to wait several seconds for the code to appear.</span></span>

<span data-ttu-id="54549-124">Die Anwendung enthält nur eine Funktion, "gettext".</span><span class="sxs-lookup"><span data-stu-id="54549-124">The application contains only one function, "getText".</span></span> <span data-ttu-id="54549-125">Die erste Zeile des Skripts erstellt das [**WinHttpRequest**](winhttprequest.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="54549-125">The first line of the script creates the [**WinHttpRequest**](winhttprequest.md) object.</span></span>


```JScript
    // Create the WinHTTPRequest ActiveX Object.
    var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```



<span data-ttu-id="54549-126">Wenn die JScript-Engine auf diese Zeile stößt, wird eine Instanz dieses Objekts erstellt.</span><span class="sxs-lookup"><span data-stu-id="54549-126">When the JScript engine encounters this line, it creates an instance of this object.</span></span> <span data-ttu-id="54549-127">Wenn Sie die Fehlermeldung "ActiveX Component Can Can Create Object" (ActiveX-Komponente kann nicht erstellt werden) erhalten, ist die WinHttp.dll in dieser Zeile höchstwahrscheinlich nicht ordnungsgemäß registriert oder nicht auf dem System vorhanden.</span><span class="sxs-lookup"><span data-stu-id="54549-127">If you get the error message, "ActiveX component can't create object", on this line, most likely the WinHttp.dll was not properly registered or is not present on the system.</span></span>

<span data-ttu-id="54549-128">Die nächste Zeile des Skripts Ruft die [**Open**](iwinhttprequest-open.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="54549-128">The next line of the script calls the [**Open**](iwinhttprequest-open.md) method.</span></span>


```JScript
    //  Create an HTTP request.
    WinHttpReq.Open("GET", "https://www.microsoft.com", false);
```



<span data-ttu-id="54549-129">Drei Parameter geben an, welches [*http-Verb*](glossary.md) verwendet werden soll, den Namen der Ressource und ob WinHTTP synchron oder asynchron verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="54549-129">Three parameters specify which [*HTTP verb*](glossary.md) to use, the name of the resource, and whether to use WinHTTP synchronously or asynchronously.</span></span> <span data-ttu-id="54549-130">In diesem Beispiel verwendet die-Methode das *http-Verb*"Get" zum Abrufen von Daten aus https://www.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="54549-130">In this example, the method is using the *HTTP verb*"GET" to obtain data from https://www.microsoft.com.</span></span> <span data-ttu-id="54549-131">Wenn Sie für den letzten Parameter **false** angeben, wird festgelegt, dass die Transaktion synchron erfolgt.</span><span class="sxs-lookup"><span data-stu-id="54549-131">Specifying **FALSE** for the last parameter determines that the transaction occurs synchronously.</span></span> <span data-ttu-id="54549-132">Die [**Open**](iwinhttprequest-open.md) -Methode stellt keine Verbindung mit der Ressource her, wie der Name vermuten könnte.</span><span class="sxs-lookup"><span data-stu-id="54549-132">The [**Open**](iwinhttprequest-open.md) method does not establish a connection to the resource as the name might imply.</span></span> <span data-ttu-id="54549-133">Stattdessen werden die internen Datenstrukturen initialisiert, die Informationen über die Sitzung, die Verbindung und die Anforderung verwalten.</span><span class="sxs-lookup"><span data-stu-id="54549-133">Rather, it initializes the internal data structures that maintain information about the session, connection, and request.</span></span>

<span data-ttu-id="54549-134">Die [**Send**](iwinhttprequest-send.md) -Methode assembliert die Anforderungs Header und sendet die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="54549-134">The [**Send**](iwinhttprequest-send.md) method assembles the request headers and sends the request.</span></span> <span data-ttu-id="54549-135">Wenn Sie im synchronen Modus aufgerufen wird, wartet die [**Send**](iwinhttprequest-send.md) -Methode auch auf eine Antwort, bevor die Anwendung fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="54549-135">When called in synchronous mode, the [**Send**](iwinhttprequest-send.md) method also waits for a response before allowing the application to continue.</span></span>


```JScript
    // Send the HTTP request.
    WinHttpReq.Send();
```



<span data-ttu-id="54549-136">Nach dem Senden der Anforderung gibt das Skript den Wert der [**responseText**](iwinhttprequest-responsetext.md) -Eigenschaft des [**WinHttpRequest**](winhttprequest.md) -Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="54549-136">After sending the request, the script returns the value of the [**ResponseText**](iwinhttprequest-responsetext.md) property of the [**WinHttpRequest**](winhttprequest.md) object.</span></span> <span data-ttu-id="54549-137">Diese Eigenschaft enthält den Entitäts Text der Antwort, in diesem Fall die Quelle eines Dokuments.</span><span class="sxs-lookup"><span data-stu-id="54549-137">This property contains the entity body of the response, in this case, the source of a document.</span></span>


```JScript
    // Get the response text.
    return WinHttpReq.ResponseText;
```



<span data-ttu-id="54549-138">Die Ausführung des Skripts wird angehalten, während der gesamte Text der Ressource abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="54549-138">Execution of the script pauses while the entire text of the resource is retrieved.</span></span> <span data-ttu-id="54549-139">Der Ressourcen Text wird von der Funktion zurückgegeben und angezeigt.</span><span class="sxs-lookup"><span data-stu-id="54549-139">The resource text is returned from the function and displayed.</span></span>

<span data-ttu-id="54549-140">Das [**WinHttpRequest**](winhttprequest.md) -Objekt stellt sicher, dass alle internen Ressourcen, die für die HTTP-Transaktion zugeordnet sind, freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="54549-140">The [**WinHttpRequest**](winhttprequest.md) object ensures that any internal resources that are allocated for the HTTP transaction are released.</span></span>

## <a name="retrieving-data-asynchronously"></a><span data-ttu-id="54549-141">Asynchrones Abrufen von Daten</span><span class="sxs-lookup"><span data-stu-id="54549-141">Retrieving Data Asynchronously</span></span>

<span data-ttu-id="54549-142">Das asynchrone Abrufen von Daten mithilfe von WinHTTP ähnelt dem synchronen Abrufen von Daten.</span><span class="sxs-lookup"><span data-stu-id="54549-142">Retrieving data asynchronously using WinHTTP is very similar to retrieving data synchronously.</span></span> <span data-ttu-id="54549-143">Ändern Sie das Skript aus dem vorherigen Abschnitt, indem Sie zwei kleine Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="54549-143">Modify the script from the previous section by making two small changes.</span></span>

1.  <span data-ttu-id="54549-144">Legen Sie den dritten Parameter der [**Open**](iwinhttprequest-open.md) -Methode auf "true" anstelle von "false" fest, um anzugeben, dass WinHTTP-Methoden asynchron ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="54549-144">Set the third parameter of the [**Open**](iwinhttprequest-open.md) method to "true" instead of "false" to specify that WinHTTP methods should be performed asynchronously.</span></span>
    ```JScript
       //  Create a HTTP request.
        var temp = WinHttpReq.Open("GET", strURL, true);
    ```

    

2.  <span data-ttu-id="54549-145">Rufen Sie die [**WaitForResponse**](iwinhttprequest-waitforresponse.md) -Methode auf, bevor Sie auf die Response [**Text**](iwinhttprequest-responsetext.md) -Eigenschaft zugreifen, um sicherzustellen, dass die gesamte Antwort empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="54549-145">Invoke the [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method before accessing the [**ResponseText**](iwinhttprequest-responsetext.md) property to ensure that the entire response has been received.</span></span>
    ```JScript
        //  Send the HTTP request.
        WinHttpReq.Send();
            
        // Wait for the entire response.
        WinHttpReq.WaitForResponse();
            
        //  Retrieve the response text.
        strResult = WinHttpReq.ResponseText;
    ```

    

<span data-ttu-id="54549-146">Der Hauptvorteil der asynchronen Verwendung von WinHTTP im Skript besteht darin, dass die [**Send**](iwinhttprequest-send.md) -Methode sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="54549-146">The main advantage to using WinHTTP asynchronously in script is that the [**Send**](iwinhttprequest-send.md) method returns immediately.</span></span> <span data-ttu-id="54549-147">Die Anforderung wird von einem Arbeits Thread vorbereitet und gesendet.</span><span class="sxs-lookup"><span data-stu-id="54549-147">The request is prepared and sent by a worker thread.</span></span> <span data-ttu-id="54549-148">Dadurch kann Ihre Anwendung andere Aufgaben ausführen, während Sie auf die Antwort wartet.</span><span class="sxs-lookup"><span data-stu-id="54549-148">This enables your application to do other things while it is waiting for the response.</span></span> <span data-ttu-id="54549-149">Bevor Sie versuchen, auf die Antwort zuzugreifen, stellen Sie sicher, dass die gesamte Antwort empfangen wurde, indem Sie die [**WaitForResponse**](iwinhttprequest-waitforresponse.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="54549-149">Before attempting to access the response, ensure that the entire response has been received by calling the [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method.</span></span> <span data-ttu-id="54549-150">Andernfalls kann ein Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="54549-150">Otherwise an error can occur.</span></span>

<span data-ttu-id="54549-151">Die [**WaitForResponse**](iwinhttprequest-waitforresponse.md) -Methode kann auch verwendet werden, um einen Timeout Wert für die Transaktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="54549-151">The [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method can also be used to specify a time-out value for the transaction.</span></span> <span data-ttu-id="54549-152">Mit einem optionalen Parameter können Sie den Timeout Wert in Sekunden angeben.</span><span class="sxs-lookup"><span data-stu-id="54549-152">An optional parameter enables you to specify the time-out value in seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54549-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="54549-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54549-154">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="54549-154">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="54549-155">HTTP/1.1-Anforderung für Kommentare (RFC 2616)</span><span class="sxs-lookup"><span data-stu-id="54549-155">HTTP/1.1 Request for Comments (RFC 2616)</span></span>](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



