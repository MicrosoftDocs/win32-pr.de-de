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
# <a name="com-soap-service-overview"></a>Übersicht über den COM+ SOAP-Dienst

HTTP revolutionierte Computer Verwendung, indem es Benutzern ermöglicht wird, einen Webbrowser für den einfachen Zugriff auf Informationen auf einem Remote Server über ein Netzwerk zu verwenden. XML-Webdienste haben jetzt die Anwendungsentwicklung revolutioniert, da Client Anwendungen Remote Methoden problemlos über ein Netzwerk abrufen können.

Es ist häufig nützlich, wenn eine Client Anwendung eine auf einem Remote Server implementierte Methode abrufen kann. In manchen Fällen verwendet die Methode flüchtige Informationen, die auf dem Remote Server gespeichert sind (z. b. eine Methode, die den aktuellen Preis der Aktie zurückgibt, die einem bestimmten Ticker-Symbol entspricht). Zu anderen Zeiten möchte der Entwickler die Methoden Implementierung aktualisieren, ohne alle Anwendungen erneut bereitstellen zu müssen, die ihn verwenden.

Wie Webseiten erfolgt der Zugriff auf XML-Webdienste über einen Webserver, wie z. b. IIS, mithilfe von http. Anstelle von Webseiten, die in HTML codiert sind, enthalten diese HTTP-Pakete jedoch die Eingabe-und Ausgabeparameter von Aufrufen einer Methode, die auf dem Server implementiert und in SOAP codiert ist.

Wenn Sie einen XML-Webdienst verwenden möchten, müssen Sie die URL kennen, unter der der Dienst verfügbar gemacht wird, sowie den Namen der Methode, die Sie aufzurufen haben, und Sie müssen die Eingabeparameter für die Methode bereitstellen. [Der SOAP 1,1-Standard](https://www.w3.org/TR/SOAP/) bietet das folgende Beispiel für ein HTTP-Paket mit einem Remote-Befehl an einen XML-Webdienst unter https://www.stockquoteserver.com/StockQuote , der den aktuellen Preis der Aktie zurückgibt, die einem bestimmten Ticker-Symbol entspricht.

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

Wie das vorherige Beispiel veranschaulicht, ist SOAP eine XML-Instanz, die in eine HTTP-Anforderung eingebettet werden kann. Ebenso wird das Ergebnis als HTTP-Paket mit einer SOAP-Nutzlast zurückgegeben, wie im folgenden Beispiel gezeigt.

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

Obwohl es hilfreich ist, sich mit der Infrastruktur vertraut zu machen, die XML-Webdiensten zugrunde liegt, vereinfacht com+ so das Erstellen und Verwenden von XML-Webdiensten, die Sie nicht oft auf diese Ebene hin finden müssen.

Sie können die Methoden in den Standardschnittstellen der konfigurierten COM-Komponenten in einer COM+-Anwendung als XML-Webdienst verfügbar machen. Beim Schreiben der Komponenten sind keine besonderen Überlegungen zur Programmierung erforderlich, mit der Ausnahme, dass sich die Methoden, die Sie verfügbar machen möchten, in der Standardschnittstelle befinden müssen und die Komponente konfiguriert werden muss (im com+-Katalog Ihres Servers). Sie müssen keinen Code schreiben, um über eine Netzwerkschnittstelle zu kommunizieren oder um SOAP zu analysieren. Ausführliche Anweisungen zur Verwendung des COM+-SOAP-Diensts zum Erstellen eines XML-Webdiensts finden Sie unter [Erstellen von XML-Webdiensten](creating-xml-web-services.md).

Wenn Sie eine COM+-Anwendung als XML-Webdienst verfügbar machen, werden ausführliche Informationen über die Syntax aller Methoden, die in einem XML-Webdienst verfügbar sind, mithilfe des Web Services Description Language (WSDL) automatisch veröffentlicht. Diese Informationen werden von Clients verwendet, die Ihren XML-Webdienst verwenden.

Com+ bietet zwei Möglichkeiten für den Zugriff auf und die Verwendung eines XML-Remote Webdiensts wie folgt:

-   Der WKO-Modus ( *well-known Object* ) kann verwendet werden, um auf alle XML-Webdienste zuzugreifen, die die Syntax mithilfe von WSDL veröffentlichen, auch wenn dieser XML-Webdienst nicht mit com+ oder sogar Microsoft Windows erstellt wurde.
-   Der *-Client aktivierte Objekt* Modus (Cao) kann nur für den Zugriff auf XML-Webdienste verwendet werden, die durch Bereitstellen von com+-Anwendungen erstellt wurden Der Modus "Cao" steigert die Leistung mithilfe von permanenten Verbindungen, einer Funktion, die vom aktuellen SOAP-Standard nicht unterstützt wird.

Beide Methoden ermöglichen es Client Anwendungen, die Methoden von XML-Webdiensten auf einfache Weise Remote aufzurufen, ohne Code zum kommunizieren über eine Netzwerkschnittstelle oder zum Analysieren von SOAP schreiben zu müssen. Ausführliche Informationen zum Zugreifen auf XML-Webdienste in einem der beiden Modi finden Sie unter [zugreifen auf XML-Webdienste im Cao-Modus](accessing-xml-web-services-in-cao-mode.md) und [zugreifen auf XML-Webdienste im WKO-Modus](accessing-xml-web-services-in-wko-mode.md).

> [!Note]  
> Com+ unterstützt nur die SOAP-RPC-Spezifikation, nicht die SOAP-Document Spezifikation.

 

Com+ vereinfacht die Verwendung von XML-Webdiensten, indem es Ihnen ermöglicht wird, vorhandene COM+-Anwendungen als XML-Webdienste in einem vollständig transparenten Modus als XML-Webdienste zu verwenden. Wenn Sie eine COM+-Anwendung [exportieren](exporting-a-soap-enabled-application.md) , die von Ihrem Server als XML-Webdienst verfügbar gemacht wurde, kann jeder Client, der die Anwendung [importiert](importing-a-soap-enabled-application.md) , den XML-Webdienst des Servers bei jeder Verwendung der importierten Anwendung transparent verwenden. Durch diese Funktion wird die Konvertierung vorhandener COM+-Anwendungen in XML-Webdienste und die Bereitstellung dieser Dienste über ein Netzwerk sehr einfach.

Die Verwendung von XML-Webdiensten bietet verschiedene Vorteile gegenüber alternativen Implementierungen von Remote Prozedur aufrufen (RPC), einschließlich der folgenden:

-   SOAP ist eine echte plattformübergreifende RPC-Implementierung, die die Interoperabilität steigert.
-   XML-Webdienste unterstützen Methoden mit Eingabe-und Ausgabeparametern.
-   XML-Webdienste werden über HTTP ausgeführt und können normalerweise Firewalls durchdringen, die andere RPC-Implementierungen blockieren können.
-   Wenn ein XML-Webdienst mit com+ implementiert wird, muss der Entwickler keinen speziellen Code schreiben. Dies ist ein großer Vorteil gegenüber alternativen RPC-Mechanismen.

> [!Note]  
> XML-Webdienste unterstützen keine asynchronen oder transparenten transaktionalen Aufrufe. Verwenden Sie den com+-Dienst in der [Warteschlange](com--queued-components.md) , wenn Sie diese Funktion benötigen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheitsüberlegungen für COM+-SOAP-Dienste](com--soap-service-security-considerations.md)
</dt> </dl>

 

 



