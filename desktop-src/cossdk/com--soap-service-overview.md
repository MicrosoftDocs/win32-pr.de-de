---
description: HTTP hat die Computernutzung revolutioniert, indem es Personen ermöglicht wird, einen Webbrowser für den einfachen Zugriff auf Informationen auf einem Remoteserver über ein Netzwerk zu verwenden.
ms.assetid: 44f3ff21-4978-4902-aa74-ddeef60881db
title: Übersicht über den COM+-SOAP-Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68501d80596d8547715cb1694fe77a17a3ab4b6955ad1e1acd596f249be5f231
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096870"
---
# <a name="com-soap-service-overview"></a>Übersicht über den COM+-SOAP-Dienst

HTTP hat die Computernutzung revolutioniert, indem es Personen ermöglicht wird, einen Webbrowser für den einfachen Zugriff auf Informationen auf einem Remoteserver über ein Netzwerk zu verwenden. XML-Webdienste haben nun die Anwendungsentwicklung revolutioniert, da Clientanwendungen remote Methoden problemlos über ein Netzwerk aufrufen können.

Es ist häufig hilfreich, wenn eine Clientanwendung eine methode aufrufen kann, die auf einem Remoteserver implementiert ist. Manchmal verwendet die Methode flüchtige Informationen, die auf dem Remoteserver gespeichert sind (z. B. eine Methode, die den aktuellen Kurs der Aktien zurückgibt, die einem bestimmten Tickersymbol entsprechen). In anderen Fällen möchte der Entwickler die Möglichkeit haben, die Implementierung der Methoden zu aktualisieren, ohne alle Anwendungen, die sie verwenden, erneut bereitstellen zu müssen.

Wie Webseiten erfolgt der Zugriff auf XML-Webdienste über einen Webserver, z. B. IIS, über HTTP. Anstelle von Webseiten, die in HTML codiert sind, enthalten diese HTTP-Pakete jedoch die Eingabe- und Ausgabeparameter von Aufrufen einer methode, die auf dem Server implementiert und in SOAP codiert ist.

Um einen XML-Webdienst zu verwenden, müssen Sie die URL kennen, unter der der Dienst verfügbar gemacht wird, und den Namen der Methode, die Sie aufrufen möchten, und Sie müssen die Eingabeparameter für die Methode angeben. [Der SOAP 1.1-Standard](https://www.w3.org/TR/SOAP/) stellt das folgende Beispiel für ein HTTP-Paket bereit, das einen Remoteaufruf eines XML-Webdiensts unter enthält, https://www.stockquoteserver.com/StockQuote der den aktuellen Kurs der Aktien entsprechend einem bestimmten Tickersymbol zurückgibt.

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

Wie im vorherigen Beispiel veranschaulicht, ist SOAP eine XML-Instanz, die in eine HTTP-Anforderung eingebettet werden kann. Ebenso wird das Ergebnis als HTTP-Paket mit einer SOAP-Nutzlast zurückgegeben, wie im folgenden Beispiel gezeigt.

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

Obwohl es hilfreich ist, ein gewisses Verständnis der Infrastruktur zu haben, die XML-Webdiensten zugrunde liegt, erleichtert COM+ das Erstellen und Verwenden von XML-Webdiensten, die Sie nicht häufig auf diese Ebene schieben müssen.

Sie können die Methoden in den Standardschnittstellen der konfigurierten COM-Komponenten in jeder COM+-Anwendung als XML-Webdienst verfügbar machen. Beim Schreiben der Komponenten sind keine besonderen Programmierüberlegungen erforderlich, außer dass die Methoden, die Sie verfügbar machen möchten, sich in der Standardschnittstelle befinden und die Komponente konfiguriert werden muss (im COM+-Katalog Ihres Servers). Sie müssen keinen Code schreiben, um über eine Netzwerkschnittstelle zu kommunizieren oder SOAP zu analysieren. Ausführliche Anweisungen zur Verwendung des COM+-SOAP-Diensts zum Erstellen eines XML-Webdiensts finden Sie unter [Erstellen von XML-Webdiensten.](creating-xml-web-services.md)

Wenn Sie eine COM+-Anwendung als XML-Webdienst verfügbar machen, werden detaillierte Informationen zur Syntax aller methoden, die von einem XML-Webdienst verfügbar sind, automatisch mithilfe der Web Services Description Language (WSDL) veröffentlicht. Diese Informationen werden von Clients verwendet, die Ihren XML-Webdienst verwenden.

COM+ bietet zwei Möglichkeiten für den Zugriff auf und die Verwendung eines XML-Remotewebdiensts:

-   Der *WKO-Modus (Well-Known Object)* kann verwendet werden, um auf jeden XML-Webdienst zuzugreifen, der seine Syntax mit WSDL veröffentlicht, auch wenn dieser XML-Webdienst nicht mit COM+ oder sogar Microsoft Windows erstellt wurde.
-   Der *CAO-Modus (Client-Activated Object)* kann nur für den Zugriff auf XML-Webdienste verwendet werden, die durch verfügbarmachen von COM+-Anwendungen erstellt wurden. Der CAO-Modus erhöht die Leistung durch die Verwendung persistenter Verbindungen, ein Feature, das vom aktuellen SOAP-Standard nicht unterstützt wird.

Mit beiden Methoden können Clientanwendungen die Methoden von XML-Webdiensten auf einfache Weise remote aufrufen, ohne Code schreiben zu müssen, um über eine Netzwerkschnittstelle zu kommunizieren oder SOAP zu analysieren. Ausführliche Informationen zum Zugriff auf XML-Webdienste in beiden Modi finden Sie unter [Zugreifen auf XML-Webdienste im CAO-Modus](accessing-xml-web-services-in-cao-mode.md) und [Zugreifen auf XML-Webdienste im WKO-Modus.](accessing-xml-web-services-in-wko-mode.md)

> [!Note]  
> COM+ unterstützt nur die SOAP-RPC-Spezifikation, nicht die SOAP-Document Spezifikation.

 

COM+ erleichtert die Verwendung von XML-Webdiensten besonders, da Sie vorhandene COM+-Anwendungen als XML-Webdienste im CAO-Modus vollständig transparent verwenden können. Wenn Sie eine COM+-Anwendung [exportieren,](exporting-a-soap-enabled-application.md) die als XML-Webdienst von Ihrem Server verfügbar gemacht wurde, kann jeder Client, der die Anwendung [importiert,](importing-a-soap-enabled-application.md) den XML-Webdienst des Servers transparent verwenden, wenn die importierte Anwendung verwendet wird. Diese Funktion erleichtert die Konvertierung vorhandener COM+-Anwendungen in XML-Webdienste und die Bereitstellung dieser Dienste über ein Netzwerk.

Die Verwendung von XML-Webdiensten bietet gegenüber alternativen Implementierungen von Remoteprozeduraufrufen (REMOTE Procedure Calls, RPC) mehrere einzigartige Vorteile, einschließlich der folgenden:

-   SOAP ist eine echte plattformübergreifende RPC-Implementierung, die die Interoperabilität erhöht.
-   XML-Webdienste unterstützen Methoden mit Eingabe- und Ausgabeparametern.
-   XML-Webdienste werden über HTTP ausgeführt, was normalerweise Firewalls durchlaufen kann, die andere RPC-Implementierungen blockieren können.
-   Wenn ein XML-Webdienst mit COM+ implementiert wird, muss der Entwickler keinen speziellen Code schreiben. dies ist ein enormer Vorteil gegenüber alternativen RPC-Mechanismen.

> [!Note]  
> XML-Webdienste unterstützen keine asynchronen oder transparenten Transaktionsaufrufe. Verwenden Sie den [COM+-Komponentendienst in der Warteschlange,](com--queued-components.md) wenn Sie diese Funktionalität benötigen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheitsüberlegungen zum COM+-SOAP-Dienst](com--soap-service-security-considerations.md)
</dt> </dl>

 

 



