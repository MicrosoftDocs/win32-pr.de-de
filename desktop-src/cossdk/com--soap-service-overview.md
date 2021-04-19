---
description: HTTP revolutionierte Computer Verwendung, indem es Benutzern ermöglicht wird, einen Webbrowser für den einfachen Zugriff auf Informationen auf einem Remote Server über ein Netzwerk zu verwenden.
ms.assetid: 44f3ff21-4978-4902-aa74-ddeef60881db
title: Übersicht über den COM+ SOAP-Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93ce7d80753f306777d3ac0b77dc46dc4e08d22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338908"
---
# <a name="com-soap-service-overview"></a><span data-ttu-id="07f57-103">Übersicht über den COM+ SOAP-Dienst</span><span class="sxs-lookup"><span data-stu-id="07f57-103">COM+ SOAP Service Overview</span></span>

<span data-ttu-id="07f57-104">HTTP revolutionierte Computer Verwendung, indem es Benutzern ermöglicht wird, einen Webbrowser für den einfachen Zugriff auf Informationen auf einem Remote Server über ein Netzwerk zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="07f57-104">HTTP revolutionized computer use by allowing people to use a Web browser for easy access to information on a remote server over a network.</span></span> <span data-ttu-id="07f57-105">XML-Webdienste haben jetzt die Anwendungsentwicklung revolutioniert, da Client Anwendungen Remote Methoden problemlos über ein Netzwerk abrufen können.</span><span class="sxs-lookup"><span data-stu-id="07f57-105">XML web services have now revolutionized application development by allowing client applications to easily call remote methods over a network.</span></span>

<span data-ttu-id="07f57-106">Es ist häufig nützlich, wenn eine Client Anwendung eine auf einem Remote Server implementierte Methode abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="07f57-106">It is often useful for a client application to be able to call a method implemented on a remote server.</span></span> <span data-ttu-id="07f57-107">In manchen Fällen verwendet die Methode flüchtige Informationen, die auf dem Remote Server gespeichert sind (z. b. eine Methode, die den aktuellen Preis der Aktie zurückgibt, die einem bestimmten Ticker-Symbol entspricht).</span><span class="sxs-lookup"><span data-stu-id="07f57-107">Sometimes the method makes use of volatile information stored on the remote server (for example, a method that returns the current price of the stock corresponding to a given ticker symbol).</span></span> <span data-ttu-id="07f57-108">Zu anderen Zeiten möchte der Entwickler die Methoden Implementierung aktualisieren, ohne alle Anwendungen erneut bereitstellen zu müssen, die ihn verwenden.</span><span class="sxs-lookup"><span data-stu-id="07f57-108">At other times, the developer wants the ability to upgrade the methods implementation without having to redeploy all the applications that use it.</span></span>

<span data-ttu-id="07f57-109">Wie Webseiten erfolgt der Zugriff auf XML-Webdienste über einen Webserver, wie z. b. IIS, mithilfe von http.</span><span class="sxs-lookup"><span data-stu-id="07f57-109">Like webpages, XML web services are accessed via a web server, such as IIS, using HTTP.</span></span> <span data-ttu-id="07f57-110">Anstelle von Webseiten, die in HTML codiert sind, enthalten diese HTTP-Pakete jedoch die Eingabe-und Ausgabeparameter von Aufrufen einer Methode, die auf dem Server implementiert und in SOAP codiert ist.</span><span class="sxs-lookup"><span data-stu-id="07f57-110">However, instead of webpages encoded in HTML, these HTTP packets contain the input and output parameters of calls to a method implemented on the server, encoded in SOAP.</span></span>

<span data-ttu-id="07f57-111">Wenn Sie einen XML-Webdienst verwenden möchten, müssen Sie die URL kennen, unter der der Dienst verfügbar gemacht wird, sowie den Namen der Methode, die Sie aufzurufen haben, und Sie müssen die Eingabeparameter für die Methode bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="07f57-111">To use an XML web service, you need to know the URL where the service is exposed and the name of the method you want to call, and you must provide the input parameters to the method.</span></span> <span data-ttu-id="07f57-112">[Der SOAP 1,1-Standard](https://www.w3.org/TR/SOAP/) bietet das folgende Beispiel für ein HTTP-Paket mit einem Remote-Befehl an einen XML-Webdienst unter https://www.stockquoteserver.com/StockQuote , der den aktuellen Preis der Aktie zurückgibt, die einem bestimmten Ticker-Symbol entspricht.</span><span class="sxs-lookup"><span data-stu-id="07f57-112">[The SOAP 1.1 standard](https://www.w3.org/TR/SOAP/) provides the following example of an HTTP packet containing a remote call to an XML web service at https://www.stockquoteserver.com/StockQuote, which returns the current price of the stock corresponding to a given ticker symbol.</span></span>

``` syntax
POST /StockQuote HTTP/1.1
Host: www.stockquoteserver.com
Content-Type: text/xml; "charset=utf-8"
Content-Length: nnnn
SOAPAction: "Some-URI"

<SOAP-ENV:Envelope
xmlns:SOAP-ENV="https://schemas.xmlsoap.org/soap/envelope/"
SOAP-ENV:encodingStyle="https://schemas.xmlsoap.org/soap/encoding/">
<SOAP-ENV:Body>
<m:GetLastTradePrice xmlns:m="Some-URI">
<symbol>DIS</symbol>
</m:GetLastTradePrice>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

<span data-ttu-id="07f57-113">Wie das vorherige Beispiel veranschaulicht, ist SOAP eine XML-Instanz, die in eine HTTP-Anforderung eingebettet werden kann.</span><span class="sxs-lookup"><span data-stu-id="07f57-113">As the preceding example illustrates, SOAP is an XML instance that can be embedded in an HTTP request.</span></span> <span data-ttu-id="07f57-114">Ebenso wird das Ergebnis als HTTP-Paket mit einer SOAP-Nutzlast zurückgegeben, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="07f57-114">Similarly, the result is returned as an HTTP packet with a SOAP payload, as shown in the following example.</span></span>

``` syntax
HTTP/1.1 200 OK
Content-Type: text/xml; "charset=utf-8"
Content-Length: nnnn

<SOAP-ENV:Envelope
xmlns:SOAP-ENV="https://schemas.xmlsoap.org/soap/envelope/"
SOAP-ENV:encodingStyle="https://schemas.xmlsoap.org/soap/encoding//">
<SOAP-ENV:Body>
<m:GetLastTradePriceResponse xmlns:m="Some-URI">
<Price>34.5</Price>
</m:GetLastTradePriceResponse>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

<span data-ttu-id="07f57-115">Obwohl es hilfreich ist, sich mit der Infrastruktur vertraut zu machen, die XML-Webdiensten zugrunde liegt, vereinfacht com+ so das Erstellen und Verwenden von XML-Webdiensten, die Sie nicht oft auf diese Ebene hin finden müssen.</span><span class="sxs-lookup"><span data-stu-id="07f57-115">While it is helpful to have some understanding of the infrastructure that underlies XML web services, COM+ makes it so easy to create and use XML web services that you won't often have to delve to this level.</span></span>

<span data-ttu-id="07f57-116">Sie können die Methoden in den Standardschnittstellen der konfigurierten COM-Komponenten in einer COM+-Anwendung als XML-Webdienst verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="07f57-116">You can expose the methods in the default interfaces of the configured COM components in any COM+ application as an XML web service.</span></span> <span data-ttu-id="07f57-117">Beim Schreiben der Komponenten sind keine besonderen Überlegungen zur Programmierung erforderlich, mit der Ausnahme, dass sich die Methoden, die Sie verfügbar machen möchten, in der Standardschnittstelle befinden müssen und die Komponente konfiguriert werden muss (im com+-Katalog Ihres Servers).</span><span class="sxs-lookup"><span data-stu-id="07f57-117">No special programming considerations are necessary when writing the components, except that the methods you want to expose must be in the default interface and the component must be configured (in your server's COM+ catalog).</span></span> <span data-ttu-id="07f57-118">Sie müssen keinen Code schreiben, um über eine Netzwerkschnittstelle zu kommunizieren oder um SOAP zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="07f57-118">You need not write code to communicate via a network interface or to parse SOAP.</span></span> <span data-ttu-id="07f57-119">Ausführliche Anweisungen zur Verwendung des COM+-SOAP-Diensts zum Erstellen eines XML-Webdiensts finden Sie unter [Erstellen von XML-Webdiensten](creating-xml-web-services.md).</span><span class="sxs-lookup"><span data-stu-id="07f57-119">For detailed instructions about using the COM+ SOAP service to create an XML web service, see [Creating XML Web Services](creating-xml-web-services.md).</span></span>

<span data-ttu-id="07f57-120">Wenn Sie eine COM+-Anwendung als XML-Webdienst verfügbar machen, werden ausführliche Informationen über die Syntax aller Methoden, die in einem XML-Webdienst verfügbar sind, mithilfe des Web Services Description Language (WSDL) automatisch veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="07f57-120">When you expose a COM+ application as an XML web service, detailed information about the syntax of all the methods available from an XML web service is published automatically, using the Web Services Description Language (WSDL).</span></span> <span data-ttu-id="07f57-121">Diese Informationen werden von Clients verwendet, die Ihren XML-Webdienst verwenden.</span><span class="sxs-lookup"><span data-stu-id="07f57-121">This information is used by clients that use your XML web service.</span></span>

<span data-ttu-id="07f57-122">Com+ bietet zwei Möglichkeiten für den Zugriff auf und die Verwendung eines XML-Remote Webdiensts wie folgt:</span><span class="sxs-lookup"><span data-stu-id="07f57-122">COM+ provides two ways for you to access and use a remote XML web service, as follows:</span></span>

-   <span data-ttu-id="07f57-123">Der WKO-Modus ( *well-known Object* ) kann verwendet werden, um auf alle XML-Webdienste zuzugreifen, die die Syntax mithilfe von WSDL veröffentlichen, auch wenn dieser XML-Webdienst nicht mit com+ oder sogar Microsoft Windows erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="07f57-123">The *well-known object* (WKO) mode can be used to access any XML web service that publishes its syntax using WSDL, even if that XML web service was not created using COM+ or even Microsoft Windows.</span></span>
-   <span data-ttu-id="07f57-124">Der *-Client aktivierte Objekt* Modus (Cao) kann nur für den Zugriff auf XML-Webdienste verwendet werden, die durch Bereitstellen von com+-Anwendungen erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="07f57-124">The *client-activated object* (CAO) mode can be used only to access XML web services created by exposing COM+ applications.</span></span> <span data-ttu-id="07f57-125">Der Modus "Cao" steigert die Leistung mithilfe von permanenten Verbindungen, einer Funktion, die vom aktuellen SOAP-Standard nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="07f57-125">CAO mode increases performance by using persistent connections, a feature not supported by the current SOAP standard.</span></span>

<span data-ttu-id="07f57-126">Beide Methoden ermöglichen es Client Anwendungen, die Methoden von XML-Webdiensten auf einfache Weise Remote aufzurufen, ohne Code zum kommunizieren über eine Netzwerkschnittstelle oder zum Analysieren von SOAP schreiben zu müssen.</span><span class="sxs-lookup"><span data-stu-id="07f57-126">Both methods allow client applications to call the methods of XML web services remotely in a straightforward fashion, without having to write code to communicate via a network interface or parse SOAP.</span></span> <span data-ttu-id="07f57-127">Ausführliche Informationen zum Zugreifen auf XML-Webdienste in einem der beiden Modi finden Sie unter [zugreifen auf XML-Webdienste im Cao-Modus](accessing-xml-web-services-in-cao-mode.md) und [zugreifen auf XML-Webdienste im WKO-Modus](accessing-xml-web-services-in-wko-mode.md).</span><span class="sxs-lookup"><span data-stu-id="07f57-127">For details about how to access XML web services in either mode, see [Accessing XML Web Services in CAO Mode](accessing-xml-web-services-in-cao-mode.md) and [Accessing XML Web Services in WKO Mode](accessing-xml-web-services-in-wko-mode.md).</span></span>

> [!Note]  
> <span data-ttu-id="07f57-128">Com+ unterstützt nur die SOAP-RPC-Spezifikation, nicht die SOAP-Document Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="07f57-128">COM+ supports only the SOAP-RPC specification, not the SOAP-Document specification.</span></span>

 

<span data-ttu-id="07f57-129">Com+ vereinfacht die Verwendung von XML-Webdiensten, indem es Ihnen ermöglicht wird, vorhandene COM+-Anwendungen als XML-Webdienste in einem vollständig transparenten Modus als XML-Webdienste zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="07f57-129">COM+ makes using XML web services especially easy by allowing you to use existing COM+ applications as XML web services in CAO mode in a completely transparent fashion.</span></span> <span data-ttu-id="07f57-130">Wenn Sie eine COM+-Anwendung [exportieren](exporting-a-soap-enabled-application.md) , die von Ihrem Server als XML-Webdienst verfügbar gemacht wurde, kann jeder Client, der die Anwendung [importiert](importing-a-soap-enabled-application.md) , den XML-Webdienst des Servers bei jeder Verwendung der importierten Anwendung transparent verwenden.</span><span class="sxs-lookup"><span data-stu-id="07f57-130">If you [export](exporting-a-soap-enabled-application.md) a COM+ application that has been exposed as an XML web service from your server, any client that [imports](importing-a-soap-enabled-application.md) the application can transparently use the server's XML web service whenever the imported application is used.</span></span> <span data-ttu-id="07f57-131">Durch diese Funktion wird die Konvertierung vorhandener COM+-Anwendungen in XML-Webdienste und die Bereitstellung dieser Dienste über ein Netzwerk sehr einfach.</span><span class="sxs-lookup"><span data-stu-id="07f57-131">This facility makes the conversion of existing COM+ applications to XML web services and the deployment of those services over a network very easy.</span></span>

<span data-ttu-id="07f57-132">Die Verwendung von XML-Webdiensten bietet verschiedene Vorteile gegenüber alternativen Implementierungen von Remote Prozedur aufrufen (RPC), einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="07f57-132">Using XML web services has several unique advantages over alternative implementations of remote procedure calls (RPC), including the following:</span></span>

-   <span data-ttu-id="07f57-133">SOAP ist eine echte plattformübergreifende RPC-Implementierung, die die Interoperabilität steigert.</span><span class="sxs-lookup"><span data-stu-id="07f57-133">SOAP is a true cross-platform RPC implementation, which increases interoperability.</span></span>
-   <span data-ttu-id="07f57-134">XML-Webdienste unterstützen Methoden mit Eingabe-und Ausgabeparametern.</span><span class="sxs-lookup"><span data-stu-id="07f57-134">XML web services support methods with both input and output parameters.</span></span>
-   <span data-ttu-id="07f57-135">XML-Webdienste werden über HTTP ausgeführt und können normalerweise Firewalls durchdringen, die andere RPC-Implementierungen blockieren können.</span><span class="sxs-lookup"><span data-stu-id="07f57-135">XML web services run over HTTP, which can usually penetrate firewalls that might block other RPC implementations.</span></span>
-   <span data-ttu-id="07f57-136">Wenn ein XML-Webdienst mit com+ implementiert wird, muss der Entwickler keinen speziellen Code schreiben. Dies ist ein großer Vorteil gegenüber alternativen RPC-Mechanismen.</span><span class="sxs-lookup"><span data-stu-id="07f57-136">When an XML web service is implemented using COM+, the developer does not have to write any specialized code; this is a tremendous advantage over alternative RPC mechanisms.</span></span>

> [!Note]  
> <span data-ttu-id="07f57-137">XML-Webdienste unterstützen keine asynchronen oder transparenten transaktionalen Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="07f57-137">XML web services do not support asynchronous or transparently transactional calls.</span></span> <span data-ttu-id="07f57-138">Verwenden Sie den com+-Dienst in der [Warteschlange](com--queued-components.md) , wenn Sie diese Funktion benötigen.</span><span class="sxs-lookup"><span data-stu-id="07f57-138">Use the [COM+ Queued Components](com--queued-components.md) service when you require this functionality.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="07f57-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="07f57-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07f57-140">Sicherheitsüberlegungen für COM+-SOAP-Dienste</span><span class="sxs-lookup"><span data-stu-id="07f57-140">COM+ SOAP Service Security Considerations</span></span>](com--soap-service-security-considerations.md)
</dt> </dl>

 

 



