---
title: HTTP-Cookies
description: HTTP-Cookies bieten dem Server einen Mechanismus zum Speichern und Abrufen von Zustandsinformationen im System der Client Anwendung.
ms.assetid: c3574592-572f-4fde-adfa-aed3e862f13f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6855f0b105dc73760541bf9eb7a6da80dfb38e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342355"
---
# <a name="http-cookies"></a><span data-ttu-id="00a64-103">HTTP-Cookies</span><span class="sxs-lookup"><span data-stu-id="00a64-103">HTTP Cookies</span></span>

<span data-ttu-id="00a64-104">HTTP-Cookies bieten dem Server einen Mechanismus zum Speichern und Abrufen von Zustandsinformationen im System der Client Anwendung.</span><span class="sxs-lookup"><span data-stu-id="00a64-104">HTTP cookies provide the server with a mechanism to store and retrieve state information on the client application's system.</span></span> <span data-ttu-id="00a64-105">Dieser Mechanismus ermöglicht webbasierten Anwendungen die Speicherung von Informationen über ausgewählte Elemente, Benutzereinstellungen, Registrierungsinformationen und andere Informationen, die später abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="00a64-105">This mechanism allows web-based applications the ability to store information about selected items, user preferences, registration information, and other information that can be retrieved later.</span></span>

## <a name="cookie-related-headers"></a><span data-ttu-id="00a64-106">Cookie-Related-Header</span><span class="sxs-lookup"><span data-stu-id="00a64-106">Cookie-Related Headers</span></span>

<span data-ttu-id="00a64-107">Es gibt zwei Header (Set-Cookie und Cookie), die mit Cookies in Beziehung stehen.</span><span class="sxs-lookup"><span data-stu-id="00a64-107">There are two headers, Set-Cookie and Cookie, that are related to cookies.</span></span> <span data-ttu-id="00a64-108">Der Set-Cookie-Header wird vom Server als Antwort auf eine HTTP-Anforderung gesendet, die zum Erstellen eines Cookies im System des Benutzers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00a64-108">The Set-Cookie header is sent by the server in response to an HTTP request, which is used to create a cookie on the user's system.</span></span> <span data-ttu-id="00a64-109">Der Cookie-Header ist in der Client Anwendung enthalten, wenn eine HTTP-Anforderung an einen Server gesendet wird, wenn ein Cookie vorhanden ist, das über eine übereinstimmende Domäne und einen entsprechenden Pfad verfügt.</span><span class="sxs-lookup"><span data-stu-id="00a64-109">The Cookie header is included by the client application with an HTTP request sent to a server, if there is a cookie that has a matching domain and path.</span></span>

### <a name="set-cookie-header"></a><span data-ttu-id="00a64-110">Set-Cookie-Header</span><span class="sxs-lookup"><span data-stu-id="00a64-110">Set-Cookie Header</span></span>

<span data-ttu-id="00a64-111">Der Set-Cookie-Antwortheader verwendet das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="00a64-111">The Set-Cookie response header uses the following format:</span></span>

``` syntax
Set-Cookie: <name>=<value>[; <name>=<value>]...
[; expires=<date>][; domain=<domain_name>]
[; path=<some_path>][; secure][; httponly]
```

<span data-ttu-id="00a64-112">Eine oder mehrere Zeichen folgen Sequenzen (getrennt durch Semikolons), die dem Wert des Muster *namens* folgen, =  müssen in den Set-Cookie-Antwortheader eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="00a64-112">One or more string sequences (separated by semicolons) that follow the pattern *name*=*value* must be included in the Set-Cookie response header.</span></span> <span data-ttu-id="00a64-113">Der Server kann diese Zeichen folgen Sequenzen verwenden, um Daten im System des Clients zu speichern.</span><span class="sxs-lookup"><span data-stu-id="00a64-113">The server can use these string sequences to store data on the client's system.</span></span>

<span data-ttu-id="00a64-114">Das Ablaufdatum wird mit dem Format läuft =*Date* festgelegt, wobei *Date* das Ablaufdatum in Greenwich Mean Time (GMT) ist.</span><span class="sxs-lookup"><span data-stu-id="00a64-114">The expiration date is set by using the format expires=*date*, where *date* is the expiration date in Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="00a64-115">Wenn das Ablaufdatum nicht festgelegt ist, läuft das Cookie ab, nachdem die Internet Sitzung beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="00a64-115">If the expiration date is not set, the cookie expires after the Internet session ends.</span></span> <span data-ttu-id="00a64-116">Andernfalls wird das Cookie bis zum Ablaufdatum im Cache beibehalten.</span><span class="sxs-lookup"><span data-stu-id="00a64-116">Otherwise, the cookie is persisted in the cache until the expiration date.</span></span> <span data-ttu-id="00a64-117">Für das Datum muss folgendes Format verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="00a64-117">The date must use the following format:</span></span>

<span data-ttu-id="00a64-118">*Tag*, *DD* - *mmm* - *yyyy* *HH*:*mm*:*SS* GMT</span><span class="sxs-lookup"><span data-stu-id="00a64-118">*DAY*, *DD*-*MMM*-*YYYY* *HH*:*MM*:*SS* GMT</span></span>

<dl> <dt>

<span data-ttu-id="00a64-119"><span id="DAY"></span><span id="day"></span>*Ertag*</span><span class="sxs-lookup"><span data-stu-id="00a64-119"><span id="DAY"></span><span id="day"></span>*DAY*</span></span>
</dt> <dd>

<span data-ttu-id="00a64-120">Der Wochentag (Sun, Mon, di, Wed, Do, Fri, Sat).</span><span class="sxs-lookup"><span data-stu-id="00a64-120">The day of the week (Sun, Mon, Tue, Wed, Thu, Fri, Sat).</span></span>

</dd> <dt>

<span data-ttu-id="00a64-121"><span id="DD"></span><span id="dd"></span>*Benutzen*</span><span class="sxs-lookup"><span data-stu-id="00a64-121"><span id="DD"></span><span id="dd"></span>*DD*</span></span>
</dt> <dd>

<span data-ttu-id="00a64-122">Der Tag im Monat (z. b. 01 für den ersten Tag des Monats).</span><span class="sxs-lookup"><span data-stu-id="00a64-122">The day in the month (such as 01 for the first day of the month).</span></span>

</dd> <dt>

<span data-ttu-id="00a64-123"><span id="MMM"></span><span id="mmm"></span>*Schlampe*</span><span class="sxs-lookup"><span data-stu-id="00a64-123"><span id="MMM"></span><span id="mmm"></span>*MMM*</span></span>
</dt> <dd>

<span data-ttu-id="00a64-124">Die drei buchstabige Abkürzung für den Monat (Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec).</span><span class="sxs-lookup"><span data-stu-id="00a64-124">The three-letter abbreviation for the month (Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec).</span></span>

</dd> <dt>

<span data-ttu-id="00a64-125"><span id="YYYY"></span><span id="yyyy"></span>*JJJJ*</span><span class="sxs-lookup"><span data-stu-id="00a64-125"><span id="YYYY"></span><span id="yyyy"></span>*YYYY*</span></span>
</dt> <dd>

<span data-ttu-id="00a64-126">Das Jahr.</span><span class="sxs-lookup"><span data-stu-id="00a64-126">The year.</span></span>

</dd> <dt>

<span data-ttu-id="00a64-127"><span id="HH"></span><span id="hh"></span>*HH*</span><span class="sxs-lookup"><span data-stu-id="00a64-127"><span id="HH"></span><span id="hh"></span>*HH*</span></span>
</dt> <dd>

<span data-ttu-id="00a64-128">Der Stunden Wert in der militärischen Zeit (z. b. 10:00 22 Uhr).</span><span class="sxs-lookup"><span data-stu-id="00a64-128">The hour value in military time (22 would be 10:00 P.M., for example).</span></span>

</dd> <dt>

<span data-ttu-id="00a64-129"><span id="MM"></span><span id="mm"></span>*MM*</span><span class="sxs-lookup"><span data-stu-id="00a64-129"><span id="MM"></span><span id="mm"></span>*MM*</span></span>
</dt> <dd>

<span data-ttu-id="00a64-130">Der Wert für die Minute.</span><span class="sxs-lookup"><span data-stu-id="00a64-130">The minute value.</span></span>

</dd> <dt>

<span data-ttu-id="00a64-131"><span id="SS"></span><span id="ss"></span>*Schaden*</span><span class="sxs-lookup"><span data-stu-id="00a64-131"><span id="SS"></span><span id="ss"></span>*SS*</span></span>
</dt> <dd>

<span data-ttu-id="00a64-132">Der zweite Wert.</span><span class="sxs-lookup"><span data-stu-id="00a64-132">The second value.</span></span>

</dd> </dl>

<span data-ttu-id="00a64-133">Das Angeben des Domänen Namens mit dem Muster Domain =*Domain \_ Name* ist für persistente Cookies optional und wird verwendet, um das Ende der Domäne anzugeben, für die das Cookie gültig ist.</span><span class="sxs-lookup"><span data-stu-id="00a64-133">Specifying the domain name, using the pattern domain=*domain\_name*, is optional for persistent cookies and is used to indicate the end of the domain for which the cookie is valid.</span></span> <span data-ttu-id="00a64-134">Sitzungs Cookies, die eine Domäne angeben, werden abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="00a64-134">Session cookies that specify a domain are rejected.</span></span> <span data-ttu-id="00a64-135">Wenn der angegebene Domänen Name mit der Anforderung übereinstimmt, versucht das Cookie, den Pfad abzugleichen, um zu bestimmen, ob das Cookie gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="00a64-135">If the specified domain name ending matches the request, the cookie tries to match the path to determine if the cookie should be sent.</span></span> <span data-ttu-id="00a64-136">Wenn der Domänen Name z. b. ". Microsoft.com" lautet, werden Anforderungen an Home.Microsoft.com und Support.Microsoft.com geprüft, um festzustellen, ob das angegebene Muster mit der Anforderung übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="00a64-136">For example, if the domain name ending is .microsoft.com, requests to home.microsoft.com and support.microsoft.com would be checked to see if the specified pattern matches the request.</span></span> <span data-ttu-id="00a64-137">Der Domänen Name muss mindestens zwei oder drei Zeiträume enthalten, um zu verhindern, dass Cookies für häufig verwendete Domänen namens enden festgelegt werden, z. b.. com,. edu und Co.JP.</span><span class="sxs-lookup"><span data-stu-id="00a64-137">The domain name must have at least two or three periods in it to prevent cookies from being set for widely used domain name endings, such as .com, .edu, and co.jp.</span></span> <span data-ttu-id="00a64-138">Zulässige Domänen Namen ähneln. Microsoft.com,. someschool.edu und. someserver.co.JP.</span><span class="sxs-lookup"><span data-stu-id="00a64-138">Allowable domain names would be similar to .microsoft.com, .someschool.edu, and .someserver.co.jp.</span></span> <span data-ttu-id="00a64-139">Nur Hosts innerhalb der angegebenen Domäne können ein Cookie für eine Domäne festlegen.</span><span class="sxs-lookup"><span data-stu-id="00a64-139">Only hosts within the specified domain can set a cookie for a domain.</span></span>

<span data-ttu-id="00a64-140">Das Festlegen des Pfads unter Verwendung des Muster Pfads = Pfad ist optional und kann verwendet werden, um eine Teilmenge der URLs *anzugeben, für \_* die das Cookie gültig ist.</span><span class="sxs-lookup"><span data-stu-id="00a64-140">Setting the path, using the pattern path=*some\_path*, is optional and can be used to specify a subset of the URLs for which the cookie is valid.</span></span> <span data-ttu-id="00a64-141">Wenn ein Pfad angegeben wird, gilt das Cookie als gültig für alle Anforderungen, die diesem Pfad entsprechen.</span><span class="sxs-lookup"><span data-stu-id="00a64-141">If a path is specified, the cookie is considered valid for any requests that match that path.</span></span> <span data-ttu-id="00a64-142">Wenn der angegebene Pfad z. b./example lautet, entsprechen Anforderungen mit den Pfaden/examplecode und/Example/code.htm.</span><span class="sxs-lookup"><span data-stu-id="00a64-142">For example, if the specified path is /example, requests with the paths /examplecode and /example/code.htm would match.</span></span> <span data-ttu-id="00a64-143">Wenn kein Pfad angegeben wird, wird davon ausgegangen, dass es sich bei dem Pfad um den Pfad der Ressource handelt, die dem Set-Cookie-Header zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="00a64-143">If no path is specified, the path is assumed to be the path of the resource associated with the Set-Cookie header.</span></span>

<span data-ttu-id="00a64-144">Das Cookie kann auch als sicher gekennzeichnet werden, was angibt, dass das Cookie nur an HTTPS-Server gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="00a64-144">The cookie can also be marked as secure, which specifies that the cookie can be sent only to https servers.</span></span>

<span data-ttu-id="00a64-145">Schließlich kann ein Cookie als HttpOnly gekennzeichnet werden (bei Attributen wird die Groß-/Kleinschreibung nicht beachtet), um anzugeben, dass das Cookie nicht skriptfähig ist und nicht für die Client Anwendung offengelegt werden sollte, aus Sicherheitsgründen.</span><span class="sxs-lookup"><span data-stu-id="00a64-145">Finally, a cookie can be marked as HttpOnly (attributes are not case-sensitive), to indicate that the cookie is non-scriptable and should not be revealed to the client application, for security reasons.</span></span> <span data-ttu-id="00a64-146">Innerhalb von Windows Internet bedeutet dies, dass das Cookie nicht über die **InternetGetCookie** -Funktion abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="00a64-146">Within Windows Internet, this means that the cookie cannot be retrieved through the **InternetGetCookie** function.</span></span>

### <a name="cookie-header"></a><span data-ttu-id="00a64-147">Cookie-Header</span><span class="sxs-lookup"><span data-stu-id="00a64-147">Cookie Header</span></span>

<span data-ttu-id="00a64-148">Der Cookie-Header ist in HTTP-Anforderungen mit einem Cookie enthalten, dessen Domäne und Pfad der Anforderung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="00a64-148">The Cookie header is included with any HTTP requests that have a cookie whose domain and path match the request.</span></span> <span data-ttu-id="00a64-149">Der Cookie-Header weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="00a64-149">The Cookie header has the following format:</span></span>

``` syntax
Cookie: <name>=<value> [;<name>=<value>]...
```

<span data-ttu-id="00a64-150">Eine oder mehrere Zeichen folgen Sequenzen, bei denen der Format *Name*- = *Wert* verwendet wird, enthalten die Informationen, die im Cookie festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="00a64-150">One or more string sequences, using the format *name*=*value*, contain the information that was set in the cookie.</span></span>

## <a name="generating-cookies"></a><span data-ttu-id="00a64-151">Erstellen von Cookies</span><span class="sxs-lookup"><span data-stu-id="00a64-151">Generating Cookies</span></span>

<span data-ttu-id="00a64-152">Es gibt drei Methoden zum Erstellen von Cookies für Microsoft Internet Explorer: die Verwendung von Microsoft JScript, die Verwendung der WinInet-Funktionen und die Verwendung eines CGI-Skripts.</span><span class="sxs-lookup"><span data-stu-id="00a64-152">There are three methods for generating cookies for Microsoft Internet Explorer: using Microsoft JScript, using the WinINet functions, and using a CGI script.</span></span> <span data-ttu-id="00a64-153">Alle Methoden müssen die Informationen festlegen, die im Set-Cookie-Header enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="00a64-153">All of the methods need to set the information that is included in the Set-Cookie header.</span></span>

### <a name="generating-a-cookie-using-the-dhtml-object-model"></a><span data-ttu-id="00a64-154">Erstellen eines Cookies mit dem DHTML-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="00a64-154">Generating a Cookie Using the DHTML Object Model</span></span>

<span data-ttu-id="00a64-155">Mit **dem dynamischen** HTML-Objektmodell (DHTML) können Cookies durch Aufrufen der Cookieeigenschaft des Dokument Objekts festgelegt werden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="00a64-155">Using the Dynamic HTML (DHTML) object model, cookies can be set by calling the **cookie** property of the document object, as shown in the following example.</span></span>

``` syntax
<SCRIPT language="JavaScript">
<!--
    document.cookie = "SomeValueName = Some_Value";
-->
</SCRIPT>
```

### <a name="generating-a-cookie-using-the-wininet-functions"></a><span data-ttu-id="00a64-156">Erstellen eines Cookies mit den WinInet-Funktionen</span><span class="sxs-lookup"><span data-stu-id="00a64-156">Generating a Cookie Using the WinInet Functions</span></span>

<span data-ttu-id="00a64-157">Cookies können von Anwendungen mithilfe der [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) -Funktion erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="00a64-157">Cookies can be created by applications using the [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) function.</span></span> <span data-ttu-id="00a64-158">Weitere Informationen finden Sie unter [Festlegen eines Cookies](managing-cookies.md).</span><span class="sxs-lookup"><span data-stu-id="00a64-158">For more information, see [Setting a Cookie](managing-cookies.md).</span></span>

### <a name="generating-a-cookie-using-a-cgi-script"></a><span data-ttu-id="00a64-159">Erstellen eines Cookies mithilfe eines CGI-Skripts</span><span class="sxs-lookup"><span data-stu-id="00a64-159">Generating a Cookie Using a CGI Script</span></span>

<span data-ttu-id="00a64-160">Cookies werden generiert, indem ein Set-Cookie-Header als Teil eines CGI-Skripts hinzugefügt wird, das in der HTTP-Antwort für eine Anforderung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="00a64-160">Cookies are generated by including a Set-Cookie header as part of a CGI script included in the HTTP response to a request.</span></span>

<span data-ttu-id="00a64-161">Das folgende Beispiel ist ein CGI-Skript, das einen Set-Cookie-Header mit perl enthält.</span><span class="sxs-lookup"><span data-stu-id="00a64-161">The following example is a CGI script that includes a Set-Cookie header using Perl.</span></span>

``` syntax
print "Set-Cookie:Test=test_value; 
      expires=Sat, 01-Jan-2000 00:00:00 GMT;
      path=/;"
```

> [!Note]  
> <span data-ttu-id="00a64-162">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="00a64-162">WinINet does not support server implementations.</span></span> <span data-ttu-id="00a64-163">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00a64-163">In addition, it should not be used from a service.</span></span> <span data-ttu-id="00a64-164">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="00a64-164">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 