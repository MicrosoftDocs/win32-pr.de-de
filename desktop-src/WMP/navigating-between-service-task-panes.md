---
title: Navigieren zwischen Dienstaufgaben Bereichen
description: Navigieren zwischen Dienstaufgaben Bereichen
ms.assetid: cb26a26d-a80d-4af5-9c5f-fab01129d83c
keywords:
- Windows Media Player Online Stores, navigieren
- Online Stores, navigieren
- Geben Sie 2 Online Stores ein, navigieren Sie zu
- Windows Media Player Online Stores, Aufgabenbereiche für Dienste
- Online Stores, Aufgabenbereiche für Dienste
- Typ 2 Online Stores, Dienstaufgaben Bereiche
- Windows Media Player Online Stores, Aufgabenbereiche
- Online Stores, Aufgabenbereiche
- Typ 2 Online Stores, Aufgabenbereiche
- Navigieren zu Typ 2 Online Stores
- Aufgabenbereiche für Windows Media Player, Dienste
- Windows Media Player, Aufgabenbereiche
- Aufgabenbereiche für Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86035215f822c67bb40c528f141422977efc8653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310031"
---
# <a name="navigating-between-service-task-panes"></a><span data-ttu-id="f434c-116">Navigieren zwischen Dienstaufgaben Bereichen</span><span class="sxs-lookup"><span data-stu-id="f434c-116">Navigating between Service Task Panes</span></span>

<span data-ttu-id="f434c-117">Um zwischen Dienstaufgaben Bereichen in Windows Media Player zu navigieren, verwenden Sie die **navigatetaskpaneurl** -Methode, die über das **Window. extern** -Objekt verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f434c-117">To navigate between service task panes in Windows Media Player, you use the **NavigateTaskPaneURL** method, which is available by using the **window.external** object.</span></span> <span data-ttu-id="f434c-118">Wenn Sie diese Methode verwenden, geben Sie Werte für drei Parameter an:</span><span class="sxs-lookup"><span data-stu-id="f434c-118">When you use this method, you specify values for three parameters:</span></span>

-   <span data-ttu-id="f434c-119">*btrekeyname*.</span><span class="sxs-lookup"><span data-stu-id="f434c-119">*bstrKeyName*.</span></span> <span data-ttu-id="f434c-120">Dies ist der Schlüssel Name des Online Stores.</span><span class="sxs-lookup"><span data-stu-id="f434c-120">This is the key name of the online store.</span></span> <span data-ttu-id="f434c-121">Wenn Sie in einem Online Shop navigieren, verwenden Sie den Schlüsselnamen des aktuellen Stores.</span><span class="sxs-lookup"><span data-stu-id="f434c-121">When navigating within an online store, use the key name of the current store.</span></span>
-   <span data-ttu-id="f434c-122">*bstrautaskpane*.</span><span class="sxs-lookup"><span data-stu-id="f434c-122">*bstrTaskPane*.</span></span> <span data-ttu-id="f434c-123">Diese Zeichenfolge enthält den Namen des Aufgabenbereichs Dienst, zu dem Sie navigieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f434c-123">This string contains the name of the service task pane to which you want to navigate.</span></span>
-   <span data-ttu-id="f434c-124">*bstrinbiams*.</span><span class="sxs-lookup"><span data-stu-id="f434c-124">*bstrParams*.</span></span> <span data-ttu-id="f434c-125">Diese Zeichenfolge enthält die Abfrage Zeichenfolgen-Parameter, die Sie an die URL für die Webseite anfügen möchten, die vom Aufgabenbereich Dienst gehostet wird, zu dem Sie navigieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f434c-125">This string contains the query string parameters you want to append to the URL for the webpage hosted by the service task pane to which you want to navigate.</span></span>

<span data-ttu-id="f434c-126">Die Navigation wird von einer von Ihnen erstellten Webseite verwaltet, die als Navigationsseite bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="f434c-126">Navigation is managed by a webpage you create, called the navigate page.</span></span> <span data-ttu-id="f434c-127">Die URL für die Navigationsseite wird vom **Navigate** -Element im servicinput Info-Dokument angegeben.</span><span class="sxs-lookup"><span data-stu-id="f434c-127">The URL for the navigate page is specified by the **Navigate** element in the ServiceInfo document.</span></span> <span data-ttu-id="f434c-128">Wenn Sie **navigatetaskpaneurl** aufzurufen, öffnet Windows Media Player die Navigationsseite und nicht die Webseite, die von den Elementen **ServiceTask1**, **ServiceTask2** oder **ServiceTask3** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f434c-128">When you call **NavigateTaskPaneURL**, Windows Media Player opens the navigate page, not the webpage specified by the **ServiceTask1**, **ServiceTask2**, or **ServiceTask3** elements.</span></span> <span data-ttu-id="f434c-129">Dabei handelt es sich um die Navigationsseite, die die von *bstrinparameams* angegebene Abfrage Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="f434c-129">It is the navigate page that receives the query string specified by *bstrParams*.</span></span> <span data-ttu-id="f434c-130">Die Navigationsseite sollte die Regeln enthalten, mit denen bestimmt wird, welcher Inhalt nach der Navigation in einem Dienstaufgaben Bereich angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f434c-130">The navigate page should contain the rules that determine which content displays in a service task pane after navigation.</span></span>

<span data-ttu-id="f434c-131">Angenommen, Sie möchten, dass Benutzer auf einen Link klicken, um von **ServiceTask1** zu **ServiceTask2** zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="f434c-131">For example, suppose you want users to click a link to navigate from **ServiceTask1** to **ServiceTask2**.</span></span> <span data-ttu-id="f434c-132">Zum Erstellen des Links können Sie den folgenden HTML-Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="f434c-132">You could use the following HTML to create the link:</span></span>


```C++
<A HREF = "javascript:window.external.NavigateTaskPaneURL('MSSampleMusic', 'ServiceTask2', 'From=Music&To=2')">Video</A>

```



<span data-ttu-id="f434c-133">Wenn der Benutzer auf den Videolink klickt, wechselt Windows Media Player zu **ServiceTask2** und öffnet die Navigationsseite, wobei die folgende Abfrage Zeichenfolge an die zugehörige URL angehängt wird.</span><span class="sxs-lookup"><span data-stu-id="f434c-133">When the user clicks the Video link, Windows Media Player switches to **ServiceTask2** and opens the navigate page, appending the following query string to its URL.</span></span>


```C++
?From=Music&To=2

```



<span data-ttu-id="f434c-134">Der from-Parameter identifiziert die Seite, auf der der Benutzer auf den Link geklickt hat, und der to-Parameter gibt die Nummer des Dienstaufgaben Bereichs an, zu dem er navigieren möchte.</span><span class="sxs-lookup"><span data-stu-id="f434c-134">The From parameter identifies the page from which the user clicked the link and the To parameter identifies the number of the service task pane to which he or she wants to navigate.</span></span> <span data-ttu-id="f434c-135">(Beachten Sie, dass es keine besonderen Informationen zu diesen Parametern gibt.</span><span class="sxs-lookup"><span data-stu-id="f434c-135">(Note that there is nothing special about these parameters.</span></span> <span data-ttu-id="f434c-136">Sie können beliebige Parameter für beliebige Zwecke verwenden, die Sie auswählen möchten.)</span><span class="sxs-lookup"><span data-stu-id="f434c-136">You can use any parameters you like for any purpose you choose.)</span></span>

<span data-ttu-id="f434c-137">Der folgende Beispielcode zeigt z. b. das **Navigate** -Element in einem serviceInfo-Dokument:</span><span class="sxs-lookup"><span data-stu-id="f434c-137">For instance, the following example code shows the **Navigate** element in a ServiceInfo document:</span></span>


```C++
<Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
```



<span data-ttu-id="f434c-138">Die resultierende URL, die mit der Abfrage Zeichenfolge vervollständigt wird, wird im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="f434c-138">The resulting URL, complete with query string, is shown in the following example:</span></span>


```C++
https://www.proseware.com/service/html/navigate.asp?From=Music&To=2

```



<span data-ttu-id="f434c-139">Der folgende Beispielcode zeigt die Navigationsseite:</span><span class="sxs-lookup"><span data-stu-id="f434c-139">The following example code shows the navigate page:</span></span>


```C++
<%
    Dim sURL
    Dim sQS
    Dim sTo

    sURL = ""
    sQS = Request.ServerVariables("QUERY_STRING")
    sTo = "" & Request.QueryString("To")
 
    Select Case sTo
       Case "1" sURL = sURL & "Music_Music.asp"
       Case "2" sURL = sURL & "Music_Video.asp"
       Case "3" sURL = sURL & "Music_Radio.asp"
       Case Else sURL = sURL & "Music_Music.asp"
    End Select
     
    sURL = sURL & "?" & sQS

    Response.Redirect(sURL)    
%>

```



<span data-ttu-id="f434c-140">Der vorangehende Code erstellt einfach eine URL und leitet den Browser an ihn weiter.</span><span class="sxs-lookup"><span data-stu-id="f434c-140">The preceding code simply creates a URL and redirects the browser to it.</span></span> <span data-ttu-id="f434c-141">Zuerst ruft der Code Werte aus der URL-Abfrage Zeichenfolge und der Abfrage Zeichenfolge selbst ab.</span><span class="sxs-lookup"><span data-stu-id="f434c-141">First, the code retrieves To values from the URL query string and the query string itself.</span></span> <span data-ttu-id="f434c-142">Er verwendet den Wert des to-Parameters, um zu bestimmen, welche Seite angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f434c-142">It uses the value of the To parameter to determine which page to display.</span></span> <span data-ttu-id="f434c-143">Anschließend wird die ursprüngliche Abfrage Zeichenfolge an die URL angefügt.</span><span class="sxs-lookup"><span data-stu-id="f434c-143">It then appends the original query string to the URL.</span></span> <span data-ttu-id="f434c-144">Zum Schluss navigiert der Browser mit einer URL, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="f434c-144">Finally, it navigates the browser using a URL similar to the following:</span></span>


```C++
https://www.proseware.com/service/html/Video.asp?locale=409&geoid=f4&version=10.0.0.3600&userlocale=409&From=Music&To=2

```



<span data-ttu-id="f434c-145">Wenn Sie auf diese Weise eine Navigation ausführen, müssen Sie " [extern. selectedtaskpane](external-selectedtaskpane.md) " angeben, um sicherzustellen, dass die Schaltfläche für die korrekte Aufgabe hervorgehoben ist.</span><span class="sxs-lookup"><span data-stu-id="f434c-145">Whenever you perform navigation in this manner, be sure to specify [External.SelectedTaskPane](external-selectedtaskpane.md) to ensure that the correct task button is highlighted.</span></span>

-   <span data-ttu-id="f434c-146">**Warnung** Achten Sie darauf, wie Sie Abfrage Zeichen folgen Parameter für die Navigation verwenden.</span><span class="sxs-lookup"><span data-stu-id="f434c-146">**Warning** Be careful how you use query string parameters for navigation.</span></span>

<span data-ttu-id="f434c-147">HtmlView-Webseiten können von allen Benutzern bereitgestellt werden, die eine ASX-Wiedergabeliste erstellen.</span><span class="sxs-lookup"><span data-stu-id="f434c-147">HTMLView webpages can be provided by anyone who creates an ASX playlist.</span></span> <span data-ttu-id="f434c-148">Dies bedeutet, dass böswillige Websites Abfrage Zeichenfolgen-Werte mithilfe von **navigatetaskpaneurl** an Ihren Online Store übergeben können.</span><span class="sxs-lookup"><span data-stu-id="f434c-148">This means that malicious websites can pass query string values to your online store using **NavigateTaskPaneURL**.</span></span> <span data-ttu-id="f434c-149">Sie müssen diese Möglichkeit planen, um den Online Store sicher zu halten.</span><span class="sxs-lookup"><span data-stu-id="f434c-149">You must plan for this possibility to keep your online store secure.</span></span> <span data-ttu-id="f434c-150">Wenn Ihr Online Store z. b. einfach einen Abfrage Zeichen folgen Wert für den Benutzer anzeigt, könnte eine böswillige Website einen unerwarteten Text anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f434c-150">For example, if your online store simply displays a query string value to the user, a malicious website could display unexpected text.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f434c-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f434c-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f434c-152">**Anzeigen von Webseiten in Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="f434c-152">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="f434c-153">**Navigate-Element**</span><span class="sxs-lookup"><span data-stu-id="f434c-153">**Navigate Element**</span></span>](navigate-element.md)
</dt> <dt>

[<span data-ttu-id="f434c-154">**Navigation für den Typ 2-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="f434c-154">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




